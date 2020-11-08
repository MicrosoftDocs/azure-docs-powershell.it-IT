---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 09CC097E-0210-4443-BCDB-5CF6C8300288
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightswindowsperformancecounterdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsPerformanceCounterDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsPerformanceCounterDataSource.md
ms.openlocfilehash: 23154fe78b25ab469cc1f993af879c8b1e5bdad1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199501"
---
# <span data-ttu-id="d1fb5-101">New-AzOperationalInsightsWindowsPerformanceCounterDataSource</span><span class="sxs-lookup"><span data-stu-id="d1fb5-101">New-AzOperationalInsightsWindowsPerformanceCounterDataSource</span></span>

## <span data-ttu-id="d1fb5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d1fb5-102">SYNOPSIS</span></span>
<span data-ttu-id="d1fb5-103">Aggiunge l'origine dati del contatore delle prestazioni di Windows per i computer connessi che eseguono il sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="d1fb5-103">Adds Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

## <span data-ttu-id="d1fb5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d1fb5-104">SYNTAX</span></span>

### <span data-ttu-id="d1fb5-105">ByWorkspaceName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d1fb5-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsWindowsPerformanceCounterDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterName] <String>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-UseLegacyCollector] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1fb5-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d1fb5-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsWindowsPerformanceCounterDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterName] <String> [-InstanceName <String>] [-IntervalSeconds <Int32>]
 [-UseLegacyCollector] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d1fb5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d1fb5-107">DESCRIPTION</span></span>
<span data-ttu-id="d1fb5-108">Il cmdlet **New-AzOperationalInsightsWindowsPerformanceCounterDataSource** aggiunge un'origine dati del contatore delle prestazioni di Windows per i computer connessi che eseguono il sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="d1fb5-108">The **New-AzOperationalInsightsWindowsPerformanceCounterDataSource** cmdlet adds a Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

## <span data-ttu-id="d1fb5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d1fb5-109">EXAMPLES</span></span>

## <span data-ttu-id="d1fb5-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d1fb5-110">PARAMETERS</span></span>

### <span data-ttu-id="d1fb5-111">-CounterName</span><span class="sxs-lookup"><span data-stu-id="d1fb5-111">-CounterName</span></span>
<span data-ttu-id="d1fb5-112">Specifica il nome di un contatore.</span><span class="sxs-lookup"><span data-stu-id="d1fb5-112">Specifies the name of a counter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1fb5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1fb5-113">-DefaultProfile</span></span>
<span data-ttu-id="d1fb5-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d1fb5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d1fb5-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d1fb5-115">-Force</span></span>
<span data-ttu-id="d1fb5-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d1fb5-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d1fb5-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="d1fb5-117">-InstanceName</span></span>
<span data-ttu-id="d1fb5-118">Specifica un nome di istanza.</span><span class="sxs-lookup"><span data-stu-id="d1fb5-118">Specifies an instance name.</span></span>

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

### <span data-ttu-id="d1fb5-119">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="d1fb5-119">-IntervalSeconds</span></span>
<span data-ttu-id="d1fb5-120">Specifica l'intervallo di raccolta.</span><span class="sxs-lookup"><span data-stu-id="d1fb5-120">Specifies the interval of collection.</span></span>

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

### <span data-ttu-id="d1fb5-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="d1fb5-121">-Name</span></span>
<span data-ttu-id="d1fb5-122">Specifica un nome per l'origine dati.</span><span class="sxs-lookup"><span data-stu-id="d1fb5-122">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="d1fb5-123">-NomeOggetto</span><span class="sxs-lookup"><span data-stu-id="d1fb5-123">-ObjectName</span></span>
<span data-ttu-id="d1fb5-124">Specifica il nome di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="d1fb5-124">Specifies the name of an object.</span></span>

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

### <span data-ttu-id="d1fb5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1fb5-125">-ResourceGroupName</span></span>
<span data-ttu-id="d1fb5-126">Specifica il nome di un gruppo di risorse che contiene computer.</span><span class="sxs-lookup"><span data-stu-id="d1fb5-126">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="d1fb5-127">-UseLegacyCollector</span><span class="sxs-lookup"><span data-stu-id="d1fb5-127">-UseLegacyCollector</span></span>
<span data-ttu-id="d1fb5-128">Usare l'agente di raccolta legacy o l'agente di raccolta predefinito.</span><span class="sxs-lookup"><span data-stu-id="d1fb5-128">Use legacy collector or the default collector.</span></span>

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

### <span data-ttu-id="d1fb5-129">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="d1fb5-129">-Workspace</span></span>
<span data-ttu-id="d1fb5-130">Specifica un'area di lavoro in cui funziona questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1fb5-130">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="d1fb5-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d1fb5-131">-WorkspaceName</span></span>
<span data-ttu-id="d1fb5-132">Specifica il nome di un'area di lavoro in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1fb5-132">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="d1fb5-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d1fb5-133">-Confirm</span></span>
<span data-ttu-id="d1fb5-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1fb5-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1fb5-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1fb5-135">-WhatIf</span></span>
<span data-ttu-id="d1fb5-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d1fb5-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1fb5-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d1fb5-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1fb5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1fb5-138">CommonParameters</span></span>
<span data-ttu-id="d1fb5-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1fb5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1fb5-140">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1fb5-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1fb5-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d1fb5-141">INPUTS</span></span>

### <span data-ttu-id="d1fb5-142">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="d1fb5-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="d1fb5-143">System. String</span><span class="sxs-lookup"><span data-stu-id="d1fb5-143">System.String</span></span>

### <span data-ttu-id="d1fb5-144">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d1fb5-144">System.Int32</span></span>

## <span data-ttu-id="d1fb5-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d1fb5-145">OUTPUTS</span></span>

### <span data-ttu-id="d1fb5-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="d1fb5-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="d1fb5-147">Note</span><span class="sxs-lookup"><span data-stu-id="d1fb5-147">NOTES</span></span>

## <span data-ttu-id="d1fb5-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d1fb5-148">RELATED LINKS</span></span>