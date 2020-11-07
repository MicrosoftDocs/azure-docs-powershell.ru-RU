---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/set-azurermrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 88f44a2b399f36f8edf6a57d2f1dc5821029a156
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561571"
---
# <span data-ttu-id="178c0-101">Set-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="178c0-101">Set-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="178c0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="178c0-102">SYNOPSIS</span></span>
<span data-ttu-id="178c0-103">Обновляет описание HybridConnection в указанном пространстве имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="178c0-103">Updates the description of a HybridConnection in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="178c0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="178c0-104">SYNTAX</span></span>

### <span data-ttu-id="178c0-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="178c0-105">HybridConnectionInputObjectSet</span></span>
```
Set-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <HybridConnectionAttibutes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="178c0-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="178c0-106">HybridConnectionPropertiesSet</span></span>
```
Set-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="178c0-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="178c0-107">DESCRIPTION</span></span>
<span data-ttu-id="178c0-108">Командлет Set-AzureRmRelayHybridConnection обновляет описание для HybridConnection в указанном пространстве имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="178c0-108">The Set-AzureRmRelayHybridConnection cmdlet updates the description for the HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="178c0-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="178c0-109">EXAMPLES</span></span>

### <span data-ttu-id="178c0-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="178c0-110">Example 1</span></span>
```
PS C:\>
PS C:\> $GetHybrid = Get-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
PS C:\> $GetHybrid.UserMetadata = "Test UserMetadata"
PS C:\> Set-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection -InputObject $GetHybrid

CreatedAt                   : 4/26/2017 10:04:15 PM
UpdatedAt                   : 4/26/2017 10:08:11 PM
ListenerCount               :
RequiresClientAuthorization : True
UserMetadata                : Test UserMetadata
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS
                              /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio
                              n2
Name                        : TestHybirdConnection2
Type                        : Microsoft.Relay/HybridConnections
```

### <span data-ttu-id="178c0-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="178c0-111">Example 2</span></span>
```
PS C:\> Set-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection -UserMetadata = "Test UserMetadata updated"

CreatedAt                   : 4/26/2017 10:04:15 PM
UpdatedAt                   : 4/26/2017 10:10:25 PM
ListenerCount               :
RequiresClientAuthorization : True
UserMetadata                : Test UserMetadata updated
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS
                              /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio
                              n1
Name                        : TestHybirdConnection1
Type                        : Microsoft.Relay/HybridConnections
```

<span data-ttu-id="178c0-112">Обновляет указанную HybridConnection с помощью нового описания в указанном пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="178c0-112">Updates the specified HybridConnection with a new description in the specified namespace.</span></span>
<span data-ttu-id="178c0-113">В этом примере свойство UserMetadata обновляется новым значением.</span><span class="sxs-lookup"><span data-stu-id="178c0-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="178c0-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="178c0-114">PARAMETERS</span></span>

### <span data-ttu-id="178c0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="178c0-115">-DefaultProfile</span></span>
<span data-ttu-id="178c0-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="178c0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="178c0-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="178c0-117">-InputObject</span></span>
<span data-ttu-id="178c0-118">Объект HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="178c0-118">HybridConnections object.</span></span>

```yaml
Type: HybridConnectionAttibutes
Parameter Sets: HybridConnectionInputObjectSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="178c0-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="178c0-119">-Name</span></span>
<span data-ttu-id="178c0-120">HybridConnections имя.</span><span class="sxs-lookup"><span data-stu-id="178c0-120">HybridConnections Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="178c0-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="178c0-121">-Namespace</span></span>
<span data-ttu-id="178c0-122">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="178c0-122">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="178c0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="178c0-123">-ResourceGroupName</span></span>
<span data-ttu-id="178c0-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="178c0-124">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="178c0-125">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="178c0-125">-UserMetadata</span></span>
<span data-ttu-id="178c0-126">Возвращает или задает usermetadata — заполнитель для хранения определенных пользователем строковых данных для конечной точки HybridConnection. Например: Он может использоваться для хранения описательных данных, таких как список групп и сведения о контактах, а также пользовательские параметры конфигурации.</span><span class="sxs-lookup"><span data-stu-id="178c0-126">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

```yaml
Type: String
Parameter Sets: HybridConnectionPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="178c0-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="178c0-127">-Confirm</span></span>
<span data-ttu-id="178c0-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="178c0-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="178c0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="178c0-129">-WhatIf</span></span>
<span data-ttu-id="178c0-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="178c0-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="178c0-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="178c0-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="178c0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="178c0-132">CommonParameters</span></span>
<span data-ttu-id="178c0-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="178c0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="178c0-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="178c0-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="178c0-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="178c0-135">INPUTS</span></span>

### <span data-ttu-id="178c0-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="178c0-136">-ResourceGroupName</span></span>
<span data-ttu-id="178c0-137">System. String</span><span class="sxs-lookup"><span data-stu-id="178c0-137">System.String</span></span>

### <span data-ttu-id="178c0-138">-+ +</span><span class="sxs-lookup"><span data-stu-id="178c0-138">-NamespaceName</span></span>
<span data-ttu-id="178c0-139">System. String</span><span class="sxs-lookup"><span data-stu-id="178c0-139">System.String</span></span>

### <span data-ttu-id="178c0-140">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="178c0-140">-WcfRelayName</span></span>
<span data-ttu-id="178c0-141">System. String</span><span class="sxs-lookup"><span data-stu-id="178c0-141">System.String</span></span>

### <span data-ttu-id="178c0-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="178c0-142">-InputObject</span></span>
<span data-ttu-id="178c0-143">Microsoft. Azure. Commands. Relay. Models. HybridConnectionAttibutes</span><span class="sxs-lookup"><span data-stu-id="178c0-143">Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes</span></span>

### <span data-ttu-id="178c0-144">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="178c0-144">-UserMetadata</span></span>
<span data-ttu-id="178c0-145">System. String</span><span class="sxs-lookup"><span data-stu-id="178c0-145">System.String</span></span>

## <span data-ttu-id="178c0-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="178c0-146">OUTPUTS</span></span>

### <span data-ttu-id="178c0-147">Microsoft. Azure. Commands. Relay. Models. HybridConnectionAttibutes</span><span class="sxs-lookup"><span data-stu-id="178c0-147">Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes</span></span>

## <span data-ttu-id="178c0-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="178c0-148">NOTES</span></span>

## <span data-ttu-id="178c0-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="178c0-149">RELATED LINKS</span></span>
