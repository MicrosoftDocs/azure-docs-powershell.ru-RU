---
Module Name: Az.Support
Module Guid: 22d73af7-38c2-4bf6-b56f-4dc9db05d97a
Download Help Link: https://docs.microsoft.com/powershell/module/az.support
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
ms.openlocfilehash: b02401044f3b01a73954ac199cc15457cddb795a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979112"
---
# Модуль az.support
## Описание
В разделах этой статьи ются командылеты Azure PowerShell для создания и управления входами в службу поддержки Azure в платформе Azure Resource Manager (ARM). Командлеты существуют в области имен Microsoft.Azure.Commands.Support.

## Az.Support Cmdlets
### [Get-AzSupportService](Get-AzSupportService.md)
Возвращает текущий список служб Azure, для которых доступна поддержка. Каждая служба Azure имеет собственный набор категорий, называемых классификацией проблем. Получить текущий список классификации проблем для службы с помощью Get-AzSupportProblemClassification. С помощью GUID классификации службы и проблемы можно создать новый билет в службу поддержки с помощью New-AzSupportTicket.

### [Get-AzSupportProblemClassification](Get-AzSupportProblemClassification.md)
Возвращает текущий список классификации проблем для службы Azure. С помощью GUID классификации службы и проблемы можно создать новый билет в службу поддержки с помощью New-AzSupportTicket. 

### [New-AzSupportContactProfileObject](New-AzSupportContactProfileObject.md)
Дополнительный cmdlet для создания объекта профиля контакта службы поддержки. Этот объект можно использовать в New-AzSupportTicket.

### [New-AzSupportTicket](New-AzSupportTicket.md)
Создает новый билет в службу поддержки Azure. Эта операция смоделна с поведением страницы запроса на поддержку в Azure [New.](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview)

### [Get-AzSupportTicket](Get-AzSupportTicket.md)
Список билетов в службу поддержки. Вы можете получить полные сведения о билете в службу поддержки по имени билета или отфильтровать его по status *или* *CreatedDate.*

### [Update-AzSupportTicket](Update-AzSupportTicket.md)
Обновив уровень серьезности, статус или контактные данные клиента, обновив уровень обслуживания.

### [Get-AzSupportTicketCommunication](Get-AzSupportTicketCommunication.md)
Получает сообщения для билета в службу поддержки. Вы также можете фильтровать сообщения о сообщениях в службу поддержки *по CreatedDate* или *CommunicationType.* 

### [New-AzSupportTicketCommunication](New-AzSupportTicketCommunication.md)
Добавляет новое взаимодействие клиентов в билет в службу поддержки Azure. 



