---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 47AFBAC7-8818-4788-B685-7AB4DCD6C2DE
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/disable-azoperationalinsightslinuxperformancecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxPerformanceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxPerformanceCollection.md
ms.openlocfilehash: 92fbc7e67bb81422e021a23810f3045b5cf32cba
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384957"
---
# <span data-ttu-id="823be-101">Disable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="823be-101">Disable-AzOperationalInsightsLinuxPerformanceCollection</span></span>

## <span data-ttu-id="823be-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="823be-102">SYNOPSIS</span></span>
<span data-ttu-id="823be-103">Interrompe la raccolta di contatori delle prestazioni da computer Linux.</span><span class="sxs-lookup"><span data-stu-id="823be-103">Stops collection of performance counters from Linux computers.</span></span>

## <span data-ttu-id="823be-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="823be-104">SYNTAX</span></span>

### <span data-ttu-id="823be-105">ByWorkspaceName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="823be-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsLinuxPerformanceCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="823be-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="823be-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsLinuxPerformanceCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="823be-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="823be-107">DESCRIPTION</span></span>
<span data-ttu-id="823be-108">Il cmdlet **Disable-AzOperationalInsightsLinuxPerformanceCollection** interrompe la raccolta di contatori delle prestazioni da computer Linux connessi in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="823be-108">The **Disable-AzOperationalInsightsLinuxPerformanceCollection** cmdlet stops collection of performance counters from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="823be-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="823be-109">EXAMPLES</span></span>

## <span data-ttu-id="823be-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="823be-110">PARAMETERS</span></span>

### <span data-ttu-id="823be-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="823be-111">-DefaultProfile</span></span>
<span data-ttu-id="823be-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="823be-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="823be-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="823be-113">-ResourceGroupName</span></span>
<span data-ttu-id="823be-114">Specifica il nome di un gruppo di risorse che contiene computer Linux.</span><span class="sxs-lookup"><span data-stu-id="823be-114">Specifies the name of a resource group that contains Linux computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="823be-115">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="823be-115">-Workspace</span></span>
<span data-ttu-id="823be-116">Specifica un'area di lavoro in cui funziona questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="823be-116">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="823be-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="823be-117">-WorkspaceName</span></span>
<span data-ttu-id="823be-118">Specifica il nome di un'area di lavoro in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="823be-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="823be-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="823be-119">-Confirm</span></span>
<span data-ttu-id="823be-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="823be-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="823be-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="823be-121">-WhatIf</span></span>
<span data-ttu-id="823be-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="823be-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="823be-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="823be-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="823be-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="823be-124">CommonParameters</span></span>
<span data-ttu-id="823be-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="823be-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="823be-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="823be-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="823be-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="823be-127">INPUTS</span></span>

### <span data-ttu-id="823be-128">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="823be-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="823be-129">System. String</span><span class="sxs-lookup"><span data-stu-id="823be-129">System.String</span></span>

## <span data-ttu-id="823be-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="823be-130">OUTPUTS</span></span>

### <span data-ttu-id="823be-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="823be-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="823be-132">Note</span><span class="sxs-lookup"><span data-stu-id="823be-132">NOTES</span></span>
* <span data-ttu-id="823be-133">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Operational, Insights</span><span class="sxs-lookup"><span data-stu-id="823be-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="823be-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="823be-134">RELATED LINKS</span></span>

[<span data-ttu-id="823be-135">Enable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="823be-135">Enable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="823be-136">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="823be-136">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzOperationalInsightsLinuxSyslogDataSource.md)


