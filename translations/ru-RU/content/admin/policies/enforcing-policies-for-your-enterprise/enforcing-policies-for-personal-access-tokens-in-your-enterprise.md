---
title: Применение политик для личных маркеров доступа в организации
intro: 'Владельцы предприятия могут контролировать, разрешать ли {% данные variables.product.pat_v2 %}s и {% данных variables.product.pat_v1_plural %}} и требовать утверждения для {% данных variables.product.pat_v2 %}s.'
versions:
  feature: pat-v2-enterprise
shortTitle: '{% data variables.product.pat_generic_caps %} policies'
ms.openlocfilehash: 6252f7ac67fe77cbe20ab85ff2cbd6f04ac17905
ms.sourcegitcommit: f638d569cd4f0dd6d0fb967818267992c0499110
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2022
ms.locfileid: '148107008'
---
{% note %}

**Примечание**. {% данных для повторного использования.user-settings.pat-v2-beta %}

В бета-версии предприятия должны принять участие в {% данных variables.product.pat_v2 %}s. Если ваше предприятие еще не согласилось, вам будет предложено принять участие и задать политики при выполнении приведенных ниже действий.

Даже если предприятие не предоставило согласие на {% данных variables.product.pat_v2 %}s, организации, принадлежащие организации, принадлежащие организации, по-прежнему могут согласиться. Все пользователи, включая {% данных variables.product.prodname_emus %}, могут создавать {% данных variables.product.pat_v2 %}s, которые могут получить доступ к ресурсам, принадлежащим пользователю (например, репозиториям, созданным в своей учетной записи), даже если предприятие не согласилось на {% данных variables.product.pat_v2 %}s.

{% endnote %}

## Ограничение доступа на {% данных variables.product.pat_v2 %}s

Владельцы предприятия могут предотвратить доступ к частным и внутренним ресурсам, принадлежащим организации, {% данных variables.product.pat_v2 %}s. {% данных variables.product.pat_v2_caps %}s по-прежнему смогут получать доступ к общедоступным ресурсам в организациях. Этот параметр управляет доступом только к {% данных variables.product.pat_v2 %}s, а не {% данных variables.product.pat_v1_plural %}. Дополнительные сведения об ограничении доступа с помощью {% данных variables.product.pat_v1_plural %}см. в разделе "[Ограничение доступа с помощью {% данных variables.product.pat_v1_plural %}](#restricting-access-by-personal-access-tokens-classic)" на этой странице.

{% data reusables.enterprise-accounts.access-enterprise %} {% data reusables.enterprise-accounts.policies-tab %}
1. В разделе {% octicon "law" aria-label="Значок закона" %} **Политики** щелкните **"Организации**".
1. В разделе **"Ограничить доступ через {% данных variables.product.pat_v2 %}s**" выберите вариант, соответствующий вашим потребностям:
   - **Разрешить организациям настраивать требования к доступу**: каждая организация, принадлежащей организации, может решить, следует ли ограничить доступ с помощью {% данных variables.product.pat_v2 %}s.
   - **Ограничение доступа через {% данных variables.product.pat_v2 %}s**: {% данных variables.product.pat_v2_caps %}s не могут получить доступ к организациям, принадлежащим организации. Ключи SSH, созданные {% данных variables.product.pat_v2 %}s, будут продолжать работать. Организации не могут переопределить этот параметр.
   - **Разрешить доступ через {% данных variables.product.pat_v2 %}s**: {% данных variables.product.pat_v2_caps %}s может получить доступ к организациям, принадлежащим организации. Организации не могут переопределить этот параметр.
1. Выберите команду **Сохранить**.

## Применение политики утверждения для {% данных variables.product.pat_v2 %}s

Владельцы предприятия могут требовать, чтобы все организации, принадлежащие организации, должны утвердить каждый {% данных variables.product.pat_v2 %}, которые могут получить доступ к организации. {% данных variables.product.pat_v2_caps %}s по-прежнему смогут читать общедоступные ресурсы в организации без утверждения. И наоборот, владельцы предприятия могут разрешить {% данных variables.product.pat_v2 %}s для доступа к организациям в организации без предварительного утверждения. Владельцы предприятия также могут позволить каждой организации в организации выбирать собственные параметры утверждения.

{% note %}

**Примечание.** Только {% данных variables.product.pat_v2 %}s, а не {% данных variables.product.pat_v1_plural %}, подлежат утверждению. Если у организации или предприятия нет ограниченного доступа с помощью {% данных variables.product.pat_v1_plural %}, любой {% данных variables.product.pat_v1 %} может получить доступ к ресурсам организации без предварительного утверждения. Дополнительные сведения об ограничении {% данных variables.product.pat_v1_plural %}см. в разделе "[Ограничение доступа к {% данных variables.product.pat_v1_plural %}](#restricting-access-by-personal-access-tokens-classic)" на этой странице и "[Настройка политики {% данных variables.product.pat_generic %} для вашей организации](/organizations/managing-programmatic-access-to-your-organization/setting-a-personal-access-token-policy-for-your-organization)".

{% endnote %}

{% data reusables.enterprise-accounts.access-enterprise %} {% data reusables.enterprise-accounts.policies-tab %}
1. В разделе {% octicon "law" aria-label="Значок закона" %} **Политики** щелкните **"Организации**".
1. В разделе **"Требовать утверждение {% данных variables.product.pat_v2 %}s**" выберите вариант, соответствующий вашим потребностям:
   - **Разрешить организациям настраивать требования к утверждению**: каждая организация, принадлежающая организации, может решить, требуется ли утверждение {% данных variables.product.pat_v2 %}, которые могут получить доступ к организации.
   - **Требовать от организаций использовать поток утверждения**: все организации, принадлежащие организации, должны утвердить каждый {% данных variables.product.pat_v2 %}, которые могут получить доступ к организации. {% данных variables.product.pat_v2_caps %}s, созданных владельцами организации, не требует утверждения. Организации не могут переопределить этот параметр.
   - **Отключите поток утверждения во всех организациях**: {% данных variables.product.pat_v2_caps %}s, созданных членами организации, могут получить доступ к организациям, принадлежащим организации без предварительного утверждения. Организации не могут переопределить этот параметр.
1. Выберите команду **Сохранить**.

## Ограничение доступа с помощью {% данных variables.product.pat_v1_plural %}

Владельцы предприятия могут предотвратить доступ к корпоративным и организациям, принадлежащим организации, {% данных variables.product.pat_v1_plural %}. {% данных variables.product.pat_v1_caps_plural %} по-прежнему смогут получать доступ к общедоступным ресурсам в организации. Этот параметр управляет доступом только к {% данных variables.product.pat_v1_plural %}, а не {% данных variables.product.pat_v2 %}s. Дополнительные сведения об ограничении доступа с помощью {% данных variables.product.pat_v2 %}s см. в разделе "[Ограничение доступа с помощью {% данных variables.product.pat_v2 %}s](#restricting-access-by-fine-grained-personal-access-tokens)" на этой странице.

{% data reusables.enterprise-accounts.access-enterprise %} {% data reusables.enterprise-accounts.policies-tab %}
1. В разделе {% octicon "law" aria-label="Значок закона" %} **Политики** щелкните **"Организации**".
1. В разделе **"Ограничение доступа к данным {% variables.product.pat_v1_plural %} для доступа к организациям** выберите вариант, соответствующий вашим потребностям:
   - **Разрешить организациям настраивать требования к доступу к {% variables.product.pat_v1_plural %}**: каждая организация, принадлежащей организации, может решить, следует ли ограничить доступ с помощью {% данных variables.product.pat_v1_plural %}.
   - **Ограничьте доступ через {% данных variables.product.pat_v1_plural %}: {% данных** variables.product.pat_v1_caps_plural %} не может получить доступ к предприятиям или организациям, принадлежащим организации. Ключи SSH, созданные {% данных variables.product.pat_v1_plural %}, будут продолжать работать. Организации не могут переопределить этот параметр.
   - **Разрешить доступ через {% данных variables.product.pat_v1_plural %}: {% данных variables.product.pat_v1_caps_plural %**} может получить доступ к предприятиям и организациям, принадлежащим организации. Организации не могут переопределить этот параметр.
1. Выберите команду **Сохранить**.
