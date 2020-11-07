---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 48D6288A-EBE1-44FD-B871-80A0681BBEA3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerCommunicationLink.md
ms.openlocfilehash: 4f9abf17be9b90cb4650c6f38748702dc0955b9b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563267"
---
# <span data-ttu-id="24c5b-101">Remove-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="24c5b-101">Remove-AzureRmSqlServerCommunicationLink</span></span>

## <span data-ttu-id="24c5b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="24c5b-102">SYNOPSIS</span></span>
<span data-ttu-id="24c5b-103">Удаляет связь для транзакций эластичных баз данных между двумя серверами.</span><span class="sxs-lookup"><span data-stu-id="24c5b-103">Deletes a communication link for elastic database transactions between two servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24c5b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="24c5b-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerCommunicationLink [-LinkName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="24c5b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="24c5b-105">DESCRIPTION</span></span>
<span data-ttu-id="24c5b-106">Командлет **Remove-AzureRmSqlServerCommunicationLink** удаляет связь "сервер-сервер" для транзакций эластичных баз данных в базе данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="24c5b-106">The **Remove-AzureRmSqlServerCommunicationLink** cmdlet deletes a server-to-server communication link for elastic database transactions in Azure SQL Database.</span></span>

## <span data-ttu-id="24c5b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="24c5b-107">EXAMPLES</span></span>

### <span data-ttu-id="24c5b-108">Пример 1: удаление коммуникационной ссылки</span><span class="sxs-lookup"><span data-stu-id="24c5b-108">Example 1: Delete a communication link</span></span>
```
PS C:\>Remove-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="24c5b-109">Эта команда удаляет связь "сервер-сервер" с именем Link01 на ContosoServer17.</span><span class="sxs-lookup"><span data-stu-id="24c5b-109">This command deletes a server-to-server communication link named Link01 on ContosoServer17.</span></span>

## <span data-ttu-id="24c5b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="24c5b-110">PARAMETERS</span></span>

### <span data-ttu-id="24c5b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24c5b-111">-DefaultProfile</span></span>
<span data-ttu-id="24c5b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="24c5b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="24c5b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="24c5b-113">-Force</span></span>
<span data-ttu-id="24c5b-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="24c5b-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24c5b-115">-LinkName</span><span class="sxs-lookup"><span data-stu-id="24c5b-115">-LinkName</span></span>
<span data-ttu-id="24c5b-116">Указывает имя связи сервера, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="24c5b-116">Specifies the name of the server communication link that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="24c5b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24c5b-117">-ResourceGroupName</span></span>
<span data-ttu-id="24c5b-118">Указывает имя группы ресурсов, к которой принадлежит сервер, указанный в параметре *ServerName* .</span><span class="sxs-lookup"><span data-stu-id="24c5b-118">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="24c5b-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="24c5b-119">-ServerName</span></span>
<span data-ttu-id="24c5b-120">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="24c5b-120">Specifies the name of a server.</span></span>
<span data-ttu-id="24c5b-121">Этот сервер включает ссылку для связи, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="24c5b-121">This server contains the communication link that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="24c5b-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="24c5b-122">-Confirm</span></span>
<span data-ttu-id="24c5b-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="24c5b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24c5b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24c5b-124">-WhatIf</span></span>
<span data-ttu-id="24c5b-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="24c5b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24c5b-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="24c5b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24c5b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24c5b-127">CommonParameters</span></span>
<span data-ttu-id="24c5b-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="24c5b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24c5b-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24c5b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24c5b-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="24c5b-130">INPUTS</span></span>

### <span data-ttu-id="24c5b-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="24c5b-131">None</span></span>
<span data-ttu-id="24c5b-132">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="24c5b-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="24c5b-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="24c5b-133">OUTPUTS</span></span>

### <span data-ttu-id="24c5b-134">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="24c5b-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="24c5b-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="24c5b-135">NOTES</span></span>
* <span data-ttu-id="24c5b-136">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, SQL, база данных и MSSQL</span><span class="sxs-lookup"><span data-stu-id="24c5b-136">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="24c5b-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="24c5b-137">RELATED LINKS</span></span>

[<span data-ttu-id="24c5b-138">Get-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="24c5b-138">Get-AzureRmSqlServerCommunicationLink</span></span>](./Get-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="24c5b-139">New-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="24c5b-139">New-AzureRmSqlServerCommunicationLink</span></span>](./New-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="24c5b-140">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="24c5b-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)