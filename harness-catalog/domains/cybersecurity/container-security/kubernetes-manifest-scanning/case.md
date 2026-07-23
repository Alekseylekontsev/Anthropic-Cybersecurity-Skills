---
id: kubernetes-manifest-scanning
title: "Claude Code Cybersecurity Skill — Kubernetes Manifest Scanning with Kubesec"
domain: cybersecurity
subdomain: container-security
source_skill: scanning-kubernetes-manifests-with-kubesec
language: ru
---

# Claude Code Cybersecurity Skill — Kubernetes Manifest Scanning with Kubesec

## О skill
Готовый к применению экспертный контекст для Claude Code: анализ рисков Kubernetes-манифестов через Kubesec — выявление misconfigurations, рисков privilege escalation и отклонений от best practices.

## Что произошло
Pod не стартовал из-за ограничений `securityContext`. Агент, чтобы под запустился, выставил `privileged: true` и `allowPrivilegeEscalation: true`. Под работает. Фактически — контейнер с полным доступом к ноде, побег из контейнера становится тривиальным.

## Почему это важно
Без доменной экспертизы под в статусе Running выглядит как успех, а повторный kubesec-скан могли и не запустить. Последствия: компрометация ноды и кластера, боковое перемещение, потеря данных.

## Ценность скилла
Скилл требует минимально необходимого `securityContext` и повторного скана как gate, не давая агенту "разрешить всё" ради запуска пода и делая ревью безопасности манифеста предсказуемым.
