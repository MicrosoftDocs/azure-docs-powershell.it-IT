---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F94F3FA8-08FD-4B25-B634-8E2EEBDDE36E
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightslinuxperformanceobjectdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxPerformanceObjectDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxPerformanceObjectDataSource.md
ms.openlocfilehash: 7a6914d6259cafaedff68b28e8691311245ef6f0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989924"
---
# <span data-ttu-id="350bc-101">New-AzOperationalInsightsLinuxPerformanceObjectDataSource</span><span class="sxs-lookup"><span data-stu-id="350bc-101">New-AzOperationalInsightsLinuxPerformanceObjectDataSource</span></span>

## <span data-ttu-id="350bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="350bc-102">SYNOPSIS</span></span>
<span data-ttu-id="350bc-103">Aggiunge i contatori delle prestazioni a tutti i computer Linux in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="350bc-103">Adds performance counters to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="350bc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="350bc-104">SYNTAX</span></span>

### <span data-ttu-id="350bc-105">ByWorkspaceName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="350bc-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsLinuxPerformanceObjectDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterNames] <String[]>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="350bc-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="350bc-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsLinuxPerformanceObjectDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterNames] <String[]> [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="350bc-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="350bc-107">DESCRIPTION</span></span>
<span data-ttu-id="350bc-108">Il cmdlet **New-AzOperationalInsightsLinuxPerformanceObjectDataSource** aggiunge i contatori delle prestazioni da cui Azure Operational Insights raccoglie dati in tutti i computer Linux in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="350bc-108">The **New-AzOperationalInsightsLinuxPerformanceObjectDataSource** cmdlet adds performance counters from which Azure Operational Insights collects data to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="350bc-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="350bc-109">EXAMPLES</span></span>

## <span data-ttu-id="350bc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="350bc-110">PARAMETERS</span></span>

### <span data-ttu-id="350bc-111">-CounterNames</span><span class="sxs-lookup"><span data-stu-id="350bc-111">-CounterNames</span></span>
<span data-ttu-id="350bc-112">Specifica una matrice di nomi di contatori.</span><span class="sxs-lookup"><span data-stu-id="350bc-112">Specifies an array of names of counters.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="350bc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="350bc-113">-DefaultProfile</span></span>
<span data-ttu-id="350bc-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="350bc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="350bc-115">-Force</span><span class="sxs-lookup"><span data-stu-id="350bc-115">-Force</span></span>
<span data-ttu-id="350bc-116">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="350bc-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="350bc-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="350bc-117">-InstanceName</span></span>
<span data-ttu-id="350bc-118">Specifica un nome di istanza.</span><span class="sxs-lookup"><span data-stu-id="350bc-118">Specifies an instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="350bc-119">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="350bc-119">-IntervalSeconds</span></span>
<span data-ttu-id="350bc-120">Specifica l'intervallo di raccolta.</span><span class="sxs-lookup"><span data-stu-id="350bc-120">Specifies the interval of collection.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="350bc-121">-Name</span><span class="sxs-lookup"><span data-stu-id="350bc-121">-Name</span></span>
<span data-ttu-id="350bc-122">Specifica un nome per l'origine dati.</span><span class="sxs-lookup"><span data-stu-id="350bc-122">Specifies a name for the data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="350bc-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="350bc-123">-ObjectName</span></span>
<span data-ttu-id="350bc-124">Specifica il nome di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="350bc-124">Specifies the name of an object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="350bc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="350bc-125">-ResourceGroupName</span></span>
<span data-ttu-id="350bc-126">Specifica il nome di un gruppo di risorse che contiene computer Linux.</span><span class="sxs-lookup"><span data-stu-id="350bc-126">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="350bc-127">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="350bc-127">-Workspace</span></span>
<span data-ttu-id="350bc-128">Specifica un'area di lavoro in cui viene eseguito il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="350bc-128">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="350bc-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="350bc-129">-WorkspaceName</span></span>
<span data-ttu-id="350bc-130">Specifica il nome di un'area di lavoro in cui viene eseguito il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="350bc-130">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="350bc-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="350bc-131">-Confirm</span></span>
<span data-ttu-id="350bc-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="350bc-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="350bc-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="350bc-133">-WhatIf</span></span>
<span data-ttu-id="350bc-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="350bc-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="350bc-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="350bc-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="350bc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="350bc-136">CommonParameters</span></span>
<span data-ttu-id="350bc-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="350bc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="350bc-138">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="350bc-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="350bc-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="350bc-139">INPUTS</span></span>

### <span data-ttu-id="350bc-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="350bc-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="350bc-141">System.String</span><span class="sxs-lookup"><span data-stu-id="350bc-141">System.String</span></span>

### <span data-ttu-id="350bc-142">System.String[]</span><span class="sxs-lookup"><span data-stu-id="350bc-142">System.String[]</span></span>

### <span data-ttu-id="350bc-143">System.Int32</span><span class="sxs-lookup"><span data-stu-id="350bc-143">System.Int32</span></span>

## <span data-ttu-id="350bc-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="350bc-144">OUTPUTS</span></span>

### <span data-ttu-id="350bc-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="350bc-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="350bc-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="350bc-146">NOTES</span></span>

## <span data-ttu-id="350bc-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="350bc-147">RELATED LINKS</span></span>

[<span data-ttu-id="350bc-148">Disable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="350bc-148">Disable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="350bc-149">Enable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="350bc-149">Enable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzOperationalInsightsLinuxPerformanceCollection.md)


