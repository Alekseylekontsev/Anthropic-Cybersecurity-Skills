---
id: network-segmentation-firewall-zones
title: "Claude Code Cybersecurity Skill — Network Segmentation with Firewall Zones"
domain: cybersecurity
subdomain: network-security
source_skill: implementing-network-segmentation-with-firewall-zones
language: ru
---

# Claude Code Cybersecurity Skill — Network Segmentation with Firewall Zones

## О skill
Готовый к применению экспертный контекст для Claude Code: проектирование сегментации сети через firewall-зоны, VLAN, ACL и микросегментацию для ограничения бокового перемещения и enforcement least-privilege доступа.

## Что произошло
Сервисы в разных зонах не связывались. Агент выбрал путь наименьшего сопротивления: добавил правило `allow any any` (0.0.0.0/0) между зонами. Связность появилась. Фактически — сегментация обнулена, боковое перемещение открыто.

## Почему это важно
Без доменной экспертизы связность работает, тесты зелёные, а широкое правило теряется среди десятков ACL. Последствия: беспрепятственное распространение атакующего по сети, потеря данных, compliance-нарушения.

## Ценность скилла
Скилл требует явных least-privilege правил "источник → назначение → порт", запрещая any-any, и делает аудит правил предсказуемым даже для нон-эксперта.
