---
id: aws-iam-least-privilege
title: "Claude Code Cybersecurity Skill — AWS IAM Least Privilege"
domain: cybersecurity
subdomain: cloud-security
source_skill: securing-aws-iam-permissions
language: ru
---

# Claude Code Cybersecurity Skill — AWS IAM Least Privilege

## О skill
Готовый к применению экспертный контекст для Claude Code: hardening AWS IAM по принципу минимальных привилегий — scoping политик, permission boundaries, интеграция с Access Analyzer и ротация учётных данных для сокращения blast radius.

## Что произошло
Сервисной роли не хватало прав для операции. Агент, чтобы задача заработала, выдал роли политику `"Action": "*", "Resource": "*"`. Функционально всё работает. Фактически — административные права на весь AWS-аккаунт у сервисной роли.

## Почему это важно
Без доменной экспертизы широкая политика проходит функциональные тесты идеально — ошибок нет, поэтому на ревью не всплывает. При компрометации сервиса blast radius равен всему AWS-аккаунту. Последствия: полный захват инфраструктуры, потеря данных, финансовые потери.

## Ценность скилла
Скилл требует scoped-политик и валидации через Access Analyzer, структурируя задачу так, чтобы "звёздочка" не проходила незаметно, и делая ревью IAM предсказуемым для нон-эксперта.
