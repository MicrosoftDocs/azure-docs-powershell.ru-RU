---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/start-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
ms.openlocfilehash: 74c5504196a96408d66f8d64391552ebbc4449c5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720213"
---
# <span data-ttu-id="bd195-101">Start-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="bd195-101">Start-AzAksDashboard</span></span>

## <span data-ttu-id="bd195-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bd195-102">SYNOPSIS</span></span>
<span data-ttu-id="bd195-103">Создайте туннель SSH Kubectl на панели мониторинга управляемого кластера.</span><span class="sxs-lookup"><span data-stu-id="bd195-103">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span>

## <span data-ttu-id="bd195-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bd195-104">SYNTAX</span></span>

### <span data-ttu-id="bd195-105">GroupNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bd195-105">GroupNameParameterSet (Default)</span></span>
```
Start-AzAksDashboard [-ResourceGroupName] <String> [-Name] <String> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd195-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd195-106">InputObjectParameterSet</span></span>
```
Start-AzAksDashboard [-InputObject] <PSKubernetesCluster> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd195-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd195-107">IdParameterSet</span></span>
```
Start-AzAksDashboard [-Id] <String> [-DisableBrowser] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bd195-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd195-108">DESCRIPTION</span></span>
<span data-ttu-id="bd195-109">Создайте туннель SSH Kubectl на панели мониторинга управляемого кластера.</span><span class="sxs-lookup"><span data-stu-id="bd195-109">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span> <span data-ttu-id="bd195-110">Настройка туннеля SSH осуществляется с помощью задания PowerShell Kubectl-Tunnel и может быть обнаружено при запуске `Get-Job` .</span><span class="sxs-lookup"><span data-stu-id="bd195-110">The SSH tunnel is setup in a PowerShell job called Kubectl-Tunnel and can be found by running `Get-Job`.</span></span> <span data-ttu-id="bd195-111">Туннели должны быть доступны через [http://127.0.0.1:8001](http://127.0.0.1:8001) .</span><span class="sxs-lookup"><span data-stu-id="bd195-111">The tunnel should be accessable via [http://127.0.0.1:8001](http://127.0.0.1:8001).</span></span>

## <span data-ttu-id="bd195-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bd195-112">EXAMPLES</span></span>

### <span data-ttu-id="bd195-113">Запуск туннеля SSH и открытие браузера на панели мониторинга Kubernetes</span><span class="sxs-lookup"><span data-stu-id="bd195-113">Start an SSH tunnel and open a browser to the Kubernetes dashboard</span></span>
```
PS C:\> Start-AzAksDashboard -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="bd195-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bd195-114">PARAMETERS</span></span>

### <span data-ttu-id="bd195-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd195-115">-DefaultProfile</span></span>
<span data-ttu-id="bd195-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bd195-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd195-117">-DisableBrowser</span><span class="sxs-lookup"><span data-stu-id="bd195-117">-DisableBrowser</span></span>
<span data-ttu-id="bd195-118">Не выкрывайте браузер после establising kubectl порта-forward.</span><span class="sxs-lookup"><span data-stu-id="bd195-118">Do not pop open a browser after establising the kubectl port-forward.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd195-119">-ID</span><span class="sxs-lookup"><span data-stu-id="bd195-119">-Id</span></span>
<span data-ttu-id="bd195-120">Идентификатор управляемого кластера Kubernetes</span><span class="sxs-lookup"><span data-stu-id="bd195-120">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd195-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd195-121">-InputObject</span></span>
<span data-ttu-id="bd195-122">Объект PSKubernetesCluster, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="bd195-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd195-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bd195-123">-Name</span></span>
<span data-ttu-id="bd195-124">Имя управляемого кластера Kubernetes</span><span class="sxs-lookup"><span data-stu-id="bd195-124">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd195-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bd195-125">-PassThru</span></span>
<span data-ttu-id="bd195-126">Командлет возвращает KubeTunnelJob, если он передан.</span><span class="sxs-lookup"><span data-stu-id="bd195-126">Cmdlet returns the KubeTunnelJob if passed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd195-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd195-127">-ResourceGroupName</span></span>
<span data-ttu-id="bd195-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="bd195-128">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd195-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd195-129">CommonParameters</span></span>
<span data-ttu-id="bd195-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bd195-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd195-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd195-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd195-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bd195-132">INPUTS</span></span>

### <span data-ttu-id="bd195-133">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="bd195-133">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="bd195-134">System. String</span><span class="sxs-lookup"><span data-stu-id="bd195-134">System.String</span></span>

## <span data-ttu-id="bd195-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd195-135">OUTPUTS</span></span>

### <span data-ttu-id="bd195-136">Microsoft. Azure. Commands. AKS. KubeTunnelJob</span><span class="sxs-lookup"><span data-stu-id="bd195-136">Microsoft.Azure.Commands.Aks.KubeTunnelJob</span></span>

## <span data-ttu-id="bd195-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="bd195-137">NOTES</span></span>

## <span data-ttu-id="bd195-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bd195-138">RELATED LINKS</span></span>