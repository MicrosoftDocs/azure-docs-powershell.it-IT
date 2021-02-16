---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F94F3FA8-08FD-4B25-B634-8E2EEBDDE36E
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightslinuxperformanceobjectdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxPerformanceObjectDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxPerformanceObjectDataSource.md
ms.openlocfilehash: 656d25e69e2739df7e196ba9e584c3890bf4028f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186750"
---
# <span data-ttu-id="3c5c7-101">New-AzOperationalInsightsLinuxPerformanceObjectDataSource</span><span class="sxs-lookup"><span data-stu-id="3c5c7-101">New-AzOperationalInsightsLinuxPerformanceObjectDataSource</span></span>

## <span data-ttu-id="3c5c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c5c7-102">SYNOPSIS</span></span>
<span data-ttu-id="3c5c7-103">Aggiunge i contatori delle prestazioni a tutti i computer Linux in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="3c5c7-103">Adds performance counters to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="3c5c7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3c5c7-104">SYNTAX</span></span>

### <span data-ttu-id="3c5c7-105">ByWorkspaceName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3c5c7-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsLinuxPerformanceObjectDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterNames] <String[]>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c5c7-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3c5c7-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsLinuxPerformanceObjectDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterNames] <String[]> [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c5c7-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3c5c7-107">DESCRIPTION</span></span>
<span data-ttu-id="3c5c7-108">Il cmdlet **New-AzOperationalInsightsLinuxPerformanceObjectDataSource** aggiunge i contatori delle prestazioni da cui Azure Operational Insights raccoglie dati in tutti i computer Linux in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="3c5c7-108">The **New-AzOperationalInsightsLinuxPerformanceObjectDataSource** cmdlet adds performance counters from which Azure Operational Insights collects data to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="3c5c7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3c5c7-109">EXAMPLES</span></span>

## <span data-ttu-id="3c5c7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c5c7-110">PARAMETERS</span></span>

### <span data-ttu-id="3c5c7-111">-CounterNames</span><span class="sxs-lookup"><span data-stu-id="3c5c7-111">-CounterNames</span></span>
<span data-ttu-id="3c5c7-112">Specifica una matrice di nomi di contatori.</span><span class="sxs-lookup"><span data-stu-id="3c5c7-112">Specifies an array of names of counters.</span></span>

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

### <span data-ttu-id="3c5c7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c5c7-113">-DefaultProfile</span></span>
<span data-ttu-id="3c5c7-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="3c5c7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3c5c7-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3c5c7-115">-Force</span></span>
<span data-ttu-id="3c5c7-116">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="3c5c7-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3c5c7-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="3c5c7-117">-InstanceName</span></span>
<span data-ttu-id="3c5c7-118">Specifica un nome di istanza.</span><span class="sxs-lookup"><span data-stu-id="3c5c7-118">Specifies an instance name.</span></span>

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

### <span data-ttu-id="3c5c7-119">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="3c5c7-119">-IntervalSeconds</span></span>
<span data-ttu-id="3c5c7-120">Specifica l'intervallo di raccolta.</span><span class="sxs-lookup"><span data-stu-id="3c5c7-120">Specifies the interval of collection.</span></span>

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

### <span data-ttu-id="3c5c7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3c5c7-121">-Name</span></span>
<span data-ttu-id="3c5c7-122">Specifica un nome per l'origine dati.</span><span class="sxs-lookup"><span data-stu-id="3c5c7-122">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="3c5c7-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="3c5c7-123">-ObjectName</span></span>
<span data-ttu-id="3c5c7-124">Specifica il nome di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="3c5c7-124">Specifies the name of an object.</span></span>

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

### <span data-ttu-id="3c5c7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c5c7-125">-ResourceGroupName</span></span>
<span data-ttu-id="3c5c7-126">Specifica il nome di un gruppo di risorse che contiene computer Linux.</span><span class="sxs-lookup"><span data-stu-id="3c5c7-126">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="3c5c7-127">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="3c5c7-127">-Workspace</span></span>
<span data-ttu-id="3c5c7-128">Specifica un'area di lavoro in cui viene eseguito il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c5c7-128">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="3c5c7-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3c5c7-129">-WorkspaceName</span></span>
<span data-ttu-id="3c5c7-130">Specifica il nome di un'area di lavoro in cui viene eseguito il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c5c7-130">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="3c5c7-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3c5c7-131">-Confirm</span></span>
<span data-ttu-id="3c5c7-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c5c7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c5c7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c5c7-133">-WhatIf</span></span>
<span data-ttu-id="3c5c7-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3c5c7-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c5c7-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3c5c7-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c5c7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c5c7-136">CommonParameters</span></span>
<span data-ttu-id="3c5c7-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c5c7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c5c7-138">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c5c7-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c5c7-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="3c5c7-139">INPUTS</span></span>

### <span data-ttu-id="3c5c7-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="3c5c7-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="3c5c7-141">System.String</span><span class="sxs-lookup"><span data-stu-id="3c5c7-141">System.String</span></span>

### <span data-ttu-id="3c5c7-142">System.String[]</span><span class="sxs-lookup"><span data-stu-id="3c5c7-142">System.String[]</span></span>

### <span data-ttu-id="3c5c7-143">System.Int32</span><span class="sxs-lookup"><span data-stu-id="3c5c7-143">System.Int32</span></span>

## <span data-ttu-id="3c5c7-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3c5c7-144">OUTPUTS</span></span>

### <span data-ttu-id="3c5c7-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="3c5c7-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="3c5c7-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="3c5c7-146">NOTES</span></span>

## <span data-ttu-id="3c5c7-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3c5c7-147">RELATED LINKS</span></span>

[<span data-ttu-id="3c5c7-148">Disable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="3c5c7-148">Disable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="3c5c7-149">Enable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="3c5c7-149">Enable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzOperationalInsightsLinuxPerformanceCollection.md)


