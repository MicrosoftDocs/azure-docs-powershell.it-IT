---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 47AFBAC7-8818-4788-B685-7AB4DCD6C2DE
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/disable-azoperationalinsightslinuxperformancecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxPerformanceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxPerformanceCollection.md
ms.openlocfilehash: 0a39dae7ebdc6cc2c1fcc1b77ceb9b5d8e330d66
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677826"
---
# <span data-ttu-id="e0705-101">Disable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="e0705-101">Disable-AzOperationalInsightsLinuxPerformanceCollection</span></span>

## <span data-ttu-id="e0705-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e0705-102">SYNOPSIS</span></span>
<span data-ttu-id="e0705-103">Interrompe la raccolta di contatori delle prestazioni da computer Linux.</span><span class="sxs-lookup"><span data-stu-id="e0705-103">Stops collection of performance counters from Linux computers.</span></span>

## <span data-ttu-id="e0705-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e0705-104">SYNTAX</span></span>

### <span data-ttu-id="e0705-105">ByWorkspaceName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e0705-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsLinuxPerformanceCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0705-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e0705-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsLinuxPerformanceCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0705-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e0705-107">DESCRIPTION</span></span>
<span data-ttu-id="e0705-108">Il cmdlet **Disable-AzOperationalInsightsLinuxPerformanceCollection** interrompe la raccolta di contatori delle prestazioni da computer Linux connessi in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="e0705-108">The **Disable-AzOperationalInsightsLinuxPerformanceCollection** cmdlet stops collection of performance counters from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="e0705-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e0705-109">EXAMPLES</span></span>

## <span data-ttu-id="e0705-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e0705-110">PARAMETERS</span></span>

### <span data-ttu-id="e0705-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0705-111">-DefaultProfile</span></span>
<span data-ttu-id="e0705-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e0705-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0705-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0705-113">-ResourceGroupName</span></span>
<span data-ttu-id="e0705-114">Specifica il nome di un gruppo di risorse che contiene computer Linux.</span><span class="sxs-lookup"><span data-stu-id="e0705-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="e0705-115">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="e0705-115">-Workspace</span></span>
<span data-ttu-id="e0705-116">Specifica un'area di lavoro in cui funziona questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0705-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="e0705-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e0705-117">-WorkspaceName</span></span>
<span data-ttu-id="e0705-118">Specifica il nome di un'area di lavoro in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0705-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="e0705-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e0705-119">-Confirm</span></span>
<span data-ttu-id="e0705-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0705-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0705-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0705-121">-WhatIf</span></span>
<span data-ttu-id="e0705-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e0705-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0705-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e0705-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0705-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0705-124">CommonParameters</span></span>
<span data-ttu-id="e0705-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0705-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0705-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0705-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0705-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e0705-127">INPUTS</span></span>

### <span data-ttu-id="e0705-128">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="e0705-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="e0705-129">System. String</span><span class="sxs-lookup"><span data-stu-id="e0705-129">System.String</span></span>

## <span data-ttu-id="e0705-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e0705-130">OUTPUTS</span></span>

### <span data-ttu-id="e0705-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="e0705-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="e0705-132">Note</span><span class="sxs-lookup"><span data-stu-id="e0705-132">NOTES</span></span>
* <span data-ttu-id="e0705-133">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Operational, Insights</span><span class="sxs-lookup"><span data-stu-id="e0705-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="e0705-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e0705-134">RELATED LINKS</span></span>

[<span data-ttu-id="e0705-135">Enable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="e0705-135">Enable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="e0705-136">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="e0705-136">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzOperationalInsightsLinuxSyslogDataSource.md)

