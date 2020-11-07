---
Module Name: Az.ManagedServices
Module Guid: d2a8f744-8dcb-4a13-ba80-eb181ff365ad
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.managedservices
Help Version: 0.0.1
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
ms.openlocfilehash: 41d7b3afa19de95b677ff5db18ca38294b8559af
ms.sourcegitcommit: 0b94b9566124331d0b15eb7f5a811305c254172e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/15/2019
ms.locfileid: "93720058"
---
# <span data-ttu-id="29abd-101">AZ. ManagedServices Module</span><span class="sxs-lookup"><span data-stu-id="29abd-101">Az.ManagedServices Module</span></span>
## <span data-ttu-id="29abd-102">Nописание</span><span class="sxs-lookup"><span data-stu-id="29abd-102">Description</span></span>
<span data-ttu-id="29abd-103">Эта функция используется клиентами управляемых поставщиков услуг (MSPs).</span><span class="sxs-lookup"><span data-stu-id="29abd-103">This feature is used by customers of Managed Service Providers (MSPs).</span></span> <span data-ttu-id="29abd-104">Пользователи предоставляют MSP возможность управлять подпиской на них.</span><span class="sxs-lookup"><span data-stu-id="29abd-104">Customers give an MSP the ability to manage their subscription.</span></span> <span data-ttu-id="29abd-105">В дополнение к предоставлению доступа клиент также может удалить доступ или просмотреть существующее делегирование доступа.</span><span class="sxs-lookup"><span data-stu-id="29abd-105">In addition to granting access, the customer can also remove access or view existing access delegations.</span></span> <span data-ttu-id="29abd-106">MSPs смогут просмотреть список пользователей, которым предоставлен доступ к подпискам.</span><span class="sxs-lookup"><span data-stu-id="29abd-106">MSPs are able to view the list of customers who have granted them access to subscriptions.</span></span> <span data-ttu-id="29abd-107">Этот процесс включает в себя два объекта: определение регистрации, которое определяет MSP и определения ролей, предоставленные MSP.</span><span class="sxs-lookup"><span data-stu-id="29abd-107">There are two objects involved in this process: A registration definition which identifies the MSP and the role definitions granted to the MSP.</span></span> <span data-ttu-id="29abd-108">MSP может дополнительно определять этот объект с помощью магазина управляемых служб, предлагающего назначения доступа, которые связывают подписку с определением.</span><span class="sxs-lookup"><span data-stu-id="29abd-108">The MSP can optionally define this object using a Managed Services marketplace offering Access assignments which associate a subscription with the definition.</span></span>

## <span data-ttu-id="29abd-109">Командлеты AZ. ManagedServices</span><span class="sxs-lookup"><span data-stu-id="29abd-109">Az.ManagedServices Cmdlets</span></span>
### [<span data-ttu-id="29abd-110">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="29abd-110">Get-AzManagedServicesAssignment</span></span>](Get-AzManagedServicesAssignment.md)
<span data-ttu-id="29abd-111">Получает список назначений регистрации.</span><span class="sxs-lookup"><span data-stu-id="29abd-111">Gets a list of the registration assignments.</span></span>

### [<span data-ttu-id="29abd-112">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="29abd-112">Get-AzManagedServicesDefinition</span></span>](Get-AzManagedServicesDefinition.md)
<span data-ttu-id="29abd-113">Получает список определений регистрации.</span><span class="sxs-lookup"><span data-stu-id="29abd-113">Gets a list of the registration definitions.</span></span>

### [<span data-ttu-id="29abd-114">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="29abd-114">New-AzManagedServicesAssignment</span></span>](New-AzManagedServicesAssignment.md)
<span data-ttu-id="29abd-115">Создание назначения регистрации.</span><span class="sxs-lookup"><span data-stu-id="29abd-115">Creates a registration assignment.</span></span>

### [<span data-ttu-id="29abd-116">New-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="29abd-116">New-AzManagedServicesDefinition</span></span>](New-AzManagedServicesDefinition.md)
<span data-ttu-id="29abd-117">Создает определение регистрации.</span><span class="sxs-lookup"><span data-stu-id="29abd-117">Creates a registration definition.</span></span>

### [<span data-ttu-id="29abd-118">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="29abd-118">Remove-AzManagedServicesAssignment</span></span>](Remove-AzManagedServicesAssignment.md)
<span data-ttu-id="29abd-119">Удаление назначения регистрации.</span><span class="sxs-lookup"><span data-stu-id="29abd-119">Deletes the registration assignment.</span></span>

### [<span data-ttu-id="29abd-120">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="29abd-120">Remove-AzManagedServicesDefinition</span></span>](Remove-AzManagedServicesDefinition.md)
<span data-ttu-id="29abd-121">Удаляет определение регистрации.</span><span class="sxs-lookup"><span data-stu-id="29abd-121">Deletes the registration definition.</span></span>
