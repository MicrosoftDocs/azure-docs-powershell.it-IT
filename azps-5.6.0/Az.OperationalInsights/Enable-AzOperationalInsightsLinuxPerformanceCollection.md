---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 10141D75-B58D-42B0-B0A6-92FF630E534C
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/enable-azoperationalinsightslinuxperformancecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxPerformanceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxPerformanceCollection.md
ms.openlocfilehash: 85ff01bdbdf454f498366b33d4684532f8382c7d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997553"
---
# <span data-ttu-id="dfe9d-101">Enable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="dfe9d-101">Enable-AzOperationalInsightsLinuxPerformanceCollection</span></span>

## <span data-ttu-id="dfe9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfe9d-102">SYNOPSIS</span></span>
<span data-ttu-id="dfe9d-103">Avvia la raccolta di contatori delle prestazioni da computer Linux.</span><span class="sxs-lookup"><span data-stu-id="dfe9d-103">Starts collection of performance counters from Linux computers.</span></span>

## <span data-ttu-id="dfe9d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dfe9d-104">SYNTAX</span></span>

### <span data-ttu-id="dfe9d-105">ByWorkspaceName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dfe9d-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsLinuxPerformanceCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfe9d-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="dfe9d-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsLinuxPerformanceCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfe9d-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="dfe9d-107">DESCRIPTION</span></span>
<span data-ttu-id="dfe9d-108">Il cmdlet **Enable-AzOperationalInsightsLinuxPerformanceCollection avvia** la raccolta di contatori delle prestazioni dai computer Linux connessi in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="dfe9d-108">The **Enable-AzOperationalInsightsLinuxPerformanceCollection** cmdlet starts collection of performance counters from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="dfe9d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dfe9d-109">EXAMPLES</span></span>

## <span data-ttu-id="dfe9d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dfe9d-110">PARAMETERS</span></span>

### <span data-ttu-id="dfe9d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfe9d-111">-DefaultProfile</span></span>
<span data-ttu-id="dfe9d-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="dfe9d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dfe9d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfe9d-113">-ResourceGroupName</span></span>
<span data-ttu-id="dfe9d-114">Specifica il nome di un gruppo di risorse che contiene computer Linux.</span><span class="sxs-lookup"><span data-stu-id="dfe9d-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="dfe9d-115">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="dfe9d-115">-Workspace</span></span>
<span data-ttu-id="dfe9d-116">Specifica un'area di lavoro in cui viene eseguito il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfe9d-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="dfe9d-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="dfe9d-117">-WorkspaceName</span></span>
<span data-ttu-id="dfe9d-118">Specifica il nome di un'area di lavoro in cui viene eseguito il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfe9d-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="dfe9d-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dfe9d-119">-Confirm</span></span>
<span data-ttu-id="dfe9d-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfe9d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfe9d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfe9d-121">-WhatIf</span></span>
<span data-ttu-id="dfe9d-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dfe9d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfe9d-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dfe9d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfe9d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfe9d-124">CommonParameters</span></span>
<span data-ttu-id="dfe9d-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfe9d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfe9d-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfe9d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfe9d-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="dfe9d-127">INPUTS</span></span>

### <span data-ttu-id="dfe9d-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="dfe9d-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="dfe9d-129">System.String</span><span class="sxs-lookup"><span data-stu-id="dfe9d-129">System.String</span></span>

## <span data-ttu-id="dfe9d-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dfe9d-130">OUTPUTS</span></span>

### <span data-ttu-id="dfe9d-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="dfe9d-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="dfe9d-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="dfe9d-132">NOTES</span></span>
* <span data-ttu-id="dfe9d-133">Parole chiave: azure, azurerm, arm, risorsa, gestione, responsabile, operativo, approfondimenti</span><span class="sxs-lookup"><span data-stu-id="dfe9d-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="dfe9d-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dfe9d-134">RELATED LINKS</span></span>

[<span data-ttu-id="dfe9d-135">Disable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="dfe9d-135">Disable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzOperationalInsightsLinuxPerformanceCollection.md)


