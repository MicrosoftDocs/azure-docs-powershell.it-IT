---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 36B3B1AC-6E7F-4607-A024-91583D952B62
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightswindowseventdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsEventDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsEventDataSource.md
ms.openlocfilehash: 29f109e0e4f063a72e188a908da8bc65723f5065
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989895"
---
# <span data-ttu-id="97de4-101">New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="97de4-101">New-AzOperationalInsightsWindowsEventDataSource</span></span>

## <span data-ttu-id="97de4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97de4-102">SYNOPSIS</span></span>
<span data-ttu-id="97de4-103">Raccoglie log eventi da computer che eseguono il sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="97de4-103">Collects event logs from computers that run the Windows operating system.</span></span>

## <span data-ttu-id="97de4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="97de4-104">SYNTAX</span></span>

### <span data-ttu-id="97de4-105">ByWorkspaceName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="97de4-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsWindowsEventDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97de4-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="97de4-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsWindowsEventDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97de4-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="97de4-107">DESCRIPTION</span></span>
<span data-ttu-id="97de4-108">Il cmdlet **New-AzOperationalInsightsWindowsEventDataSource** aggiunge un'origine dati che raccoglie log eventi di Windows dai computer connessi che eseguono il sistema operativo Windows in Azure Operational Insights.</span><span class="sxs-lookup"><span data-stu-id="97de4-108">The **New-AzOperationalInsightsWindowsEventDataSource** cmdlet adds a data source that collects Windows event logs from connected computers that run the Windows operating system in Azure Operational Insights.</span></span>

## <span data-ttu-id="97de4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="97de4-109">EXAMPLES</span></span>

### <span data-ttu-id="97de4-110">Esempio 1: Creare un'origine dati per gli eventi di Windows di sistema</span><span class="sxs-lookup"><span data-stu-id="97de4-110">Example 1: Create system Windows event data source</span></span>
```
$EventLogNames       = @()
$EventLogNames      += 'Directory Service'
$EventLogNames      += 'Microsoft-Windows-EventCollector/Operational'
$EventLogNames      += 'System'
$ResourceGroupName   = 'MyResourceGroup'
$WorkspaceName       = 'MyWorkspaceName'

$Count = 0
foreach ($EventLogName in $EventLogNames) {
    $Count++
    $null = New-AzOperationalInsightsWindowsEventDataSource `
    -ResourceGroupName $ResourceGroupName `
    -WorkspaceName $WorkspaceName `
    -Name "Windows-event-$($Count)" `
    -EventLogName $EventLogName `
    -CollectErrors `
    -CollectWarnings `
    -CollectInformation
}

Get-AzOperationalInsightsDataSource `
   -ResourceGroupName $ResourceGroupName `
   -WorkspaceName $WorkspaceName `
   -Kind 'WindowsEvent'
```

## <span data-ttu-id="97de4-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97de4-111">PARAMETERS</span></span>

### <span data-ttu-id="97de4-112">-CollectErrors</span><span class="sxs-lookup"><span data-stu-id="97de4-112">-CollectErrors</span></span>
<span data-ttu-id="97de4-113">Indica che Dati operativi raccoglie messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="97de4-113">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="97de4-114">-CollectInformation</span><span class="sxs-lookup"><span data-stu-id="97de4-114">-CollectInformation</span></span>
<span data-ttu-id="97de4-115">Indica che Dati operativi raccoglie messaggi informativi.</span><span class="sxs-lookup"><span data-stu-id="97de4-115">Indicates that Operational Insights collects information messages.</span></span>

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

### <span data-ttu-id="97de4-116">-CollectWarnings</span><span class="sxs-lookup"><span data-stu-id="97de4-116">-CollectWarnings</span></span>
<span data-ttu-id="97de4-117">Indica che Dati operativi raccoglie messaggi di avviso.</span><span class="sxs-lookup"><span data-stu-id="97de4-117">Indicates that Operational Insights collects warning messages.</span></span>

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

### <span data-ttu-id="97de4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97de4-118">-DefaultProfile</span></span>
<span data-ttu-id="97de4-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="97de4-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="97de4-120">-EventLogName</span><span class="sxs-lookup"><span data-stu-id="97de4-120">-EventLogName</span></span>
<span data-ttu-id="97de4-121">Specifica il nome del log eventi.</span><span class="sxs-lookup"><span data-stu-id="97de4-121">Specifies the name of the event log.</span></span>

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

### <span data-ttu-id="97de4-122">-Force</span><span class="sxs-lookup"><span data-stu-id="97de4-122">-Force</span></span>
<span data-ttu-id="97de4-123">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="97de4-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="97de4-124">-Name</span><span class="sxs-lookup"><span data-stu-id="97de4-124">-Name</span></span>
<span data-ttu-id="97de4-125">Specifica un nome per l'origine dati.</span><span class="sxs-lookup"><span data-stu-id="97de4-125">Specifies a name for the data source.</span></span> <span data-ttu-id="97de4-126">Il nome non viene esposto nel portale di Azure e può essere usato qualsiasi stringa purché sia univoca.</span><span class="sxs-lookup"><span data-stu-id="97de4-126">The name is not exposed in the Azure Portal and any string can be used as long as it is unique.</span></span>

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

### <span data-ttu-id="97de4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97de4-127">-ResourceGroupName</span></span>
<span data-ttu-id="97de4-128">Specifica il nome di un gruppo di risorse che contiene computer.</span><span class="sxs-lookup"><span data-stu-id="97de4-128">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="97de4-129">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="97de4-129">-Workspace</span></span>
<span data-ttu-id="97de4-130">Specifica un'area di lavoro in cui viene eseguito il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97de4-130">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="97de4-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="97de4-131">-WorkspaceName</span></span>
<span data-ttu-id="97de4-132">Specifica il nome di un'area di lavoro in cui viene eseguito il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97de4-132">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="97de4-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="97de4-133">-Confirm</span></span>
<span data-ttu-id="97de4-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97de4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97de4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97de4-135">-WhatIf</span></span>
<span data-ttu-id="97de4-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="97de4-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97de4-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="97de4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97de4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97de4-138">CommonParameters</span></span>
<span data-ttu-id="97de4-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97de4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97de4-140">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97de4-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97de4-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="97de4-141">INPUTS</span></span>

### <span data-ttu-id="97de4-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="97de4-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="97de4-143">System.String</span><span class="sxs-lookup"><span data-stu-id="97de4-143">System.String</span></span>

## <span data-ttu-id="97de4-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="97de4-144">OUTPUTS</span></span>

### <span data-ttu-id="97de4-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="97de4-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="97de4-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="97de4-146">NOTES</span></span>

## <span data-ttu-id="97de4-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="97de4-147">RELATED LINKS</span></span>
