---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRule.md
ms.openlocfilehash: 5a896bedd7e0dd6e220fb4b8dae2cc2e87ae0fcb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486860"
---
# <span data-ttu-id="af31d-101">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="af31d-101">New-AzScheduledQueryRule</span></span>

## <span data-ttu-id="af31d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="af31d-102">SYNOPSIS</span></span>
<span data-ttu-id="af31d-103">Crea una regola di avviso del log (tipo di regola di query pianificato)</span><span class="sxs-lookup"><span data-stu-id="af31d-103">Creates a Log Alert Rule (Scheduled Query Rule type)</span></span>

## <span data-ttu-id="af31d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="af31d-104">SYNTAX</span></span>

```
New-AzScheduledQueryRule -Source <PSScheduledQueryRuleSource> -Schedule <PSScheduledQueryRuleSchedule>
 -Action <PSScheduledQueryRuleAlertingAction> -Location <String> [-Description <String>] -Name <String>
 -Enabled <Boolean> -ResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af31d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="af31d-105">DESCRIPTION</span></span>
<span data-ttu-id="af31d-106">Crea una regola di avviso del log (tipo di regola di query pianificato)</span><span class="sxs-lookup"><span data-stu-id="af31d-106">Creates a Log Alert Rule (Scheduled Query Rule type)</span></span>

## <span data-ttu-id="af31d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="af31d-107">EXAMPLES</span></span>

### <span data-ttu-id="af31d-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="af31d-108">Example 1</span></span>
```powershell
PS C:\> New-AzScheduledQueryRule -Location "West Europe" -Action $alertingAction -Enabled $true -Description "log alert foo" -Schedule $schedule -Source $source -Name "LogAlertRule1"
```

## <span data-ttu-id="af31d-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="af31d-109">PARAMETERS</span></span>

### <span data-ttu-id="af31d-110">-Azione</span><span class="sxs-lookup"><span data-stu-id="af31d-110">-Action</span></span>
<span data-ttu-id="af31d-111">Azione di avviso della regola di query pianificata</span><span class="sxs-lookup"><span data-stu-id="af31d-111">The scheduled query rule Alerting Action</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af31d-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="af31d-112">-AsJob</span></span>
<span data-ttu-id="af31d-113">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="af31d-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="af31d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af31d-114">-DefaultProfile</span></span>
<span data-ttu-id="af31d-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="af31d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af31d-116">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="af31d-116">-Description</span></span>
<span data-ttu-id="af31d-117">Descrizione di questo avviso</span><span class="sxs-lookup"><span data-stu-id="af31d-117">The description for this alert</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af31d-118">-Enabled</span><span class="sxs-lookup"><span data-stu-id="af31d-118">-Enabled</span></span>
<span data-ttu-id="af31d-119">Stato di avviso di Azure-valori validi-$true $false</span><span class="sxs-lookup"><span data-stu-id="af31d-119">The azure alert state - valid values - $true, $false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af31d-120">-Posizione</span><span class="sxs-lookup"><span data-stu-id="af31d-120">-Location</span></span>
<span data-ttu-id="af31d-121">Posizione per l'avviso</span><span class="sxs-lookup"><span data-stu-id="af31d-121">The location for this alert</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af31d-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="af31d-122">-Name</span></span>
<span data-ttu-id="af31d-123">Nome avviso</span><span class="sxs-lookup"><span data-stu-id="af31d-123">The alert name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af31d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af31d-124">-ResourceGroupName</span></span>
<span data-ttu-id="af31d-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="af31d-125">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af31d-126">-Programmazione</span><span class="sxs-lookup"><span data-stu-id="af31d-126">-Schedule</span></span>
<span data-ttu-id="af31d-127">Pianificazione della regola di query pianificata</span><span class="sxs-lookup"><span data-stu-id="af31d-127">The scheduled query rule schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af31d-128">-Origine</span><span class="sxs-lookup"><span data-stu-id="af31d-128">-Source</span></span>
<span data-ttu-id="af31d-129">Origine della regola di query pianificata</span><span class="sxs-lookup"><span data-stu-id="af31d-129">The scheduled query rule source</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af31d-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="af31d-130">-Tag</span></span>
<span data-ttu-id="af31d-131">Tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="af31d-131">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af31d-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="af31d-132">-Confirm</span></span>
<span data-ttu-id="af31d-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af31d-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af31d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af31d-134">-WhatIf</span></span>
<span data-ttu-id="af31d-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="af31d-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="af31d-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="af31d-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af31d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af31d-137">CommonParameters</span></span>
<span data-ttu-id="af31d-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af31d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af31d-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af31d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af31d-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="af31d-140">INPUTS</span></span>

### <span data-ttu-id="af31d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="af31d-141">System.String</span></span>

## <span data-ttu-id="af31d-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="af31d-142">OUTPUTS</span></span>

### <span data-ttu-id="af31d-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="af31d-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="af31d-144">Note</span><span class="sxs-lookup"><span data-stu-id="af31d-144">NOTES</span></span>

## <span data-ttu-id="af31d-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="af31d-145">RELATED LINKS</span></span>
