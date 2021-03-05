---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRule.md
ms.openlocfilehash: 49863fd8102aef7b0175328edc0b4523f13921d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961821"
---
# <span data-ttu-id="86e8c-101">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="86e8c-101">New-AzScheduledQueryRule</span></span>

## <span data-ttu-id="86e8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86e8c-102">SYNOPSIS</span></span>
<span data-ttu-id="86e8c-103">Crea una regola di avviso per il log (tipo di regola di query pianificata)</span><span class="sxs-lookup"><span data-stu-id="86e8c-103">Creates a Log Alert Rule (Scheduled Query Rule type)</span></span>

## <span data-ttu-id="86e8c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="86e8c-104">SYNTAX</span></span>

```
New-AzScheduledQueryRule -Source <PSScheduledQueryRuleSource> -Schedule <PSScheduledQueryRuleSchedule>
 -Action <PSScheduledQueryRuleAlertingAction> -Location <String> [-Description <String>] -Name <String>
 -Enabled <Boolean> -ResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86e8c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="86e8c-105">DESCRIPTION</span></span>
<span data-ttu-id="86e8c-106">Crea una regola di avviso per il log (tipo di regola di query pianificata)</span><span class="sxs-lookup"><span data-stu-id="86e8c-106">Creates a Log Alert Rule (Scheduled Query Rule type)</span></span>

## <span data-ttu-id="86e8c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="86e8c-107">EXAMPLES</span></span>

### <span data-ttu-id="86e8c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="86e8c-108">Example 1</span></span>
```powershell
PS C:\> New-AzScheduledQueryRule -Location "West Europe" -Action $alertingAction -Enabled $true -Description "log alert foo" -Schedule $schedule -Source $source -Name "LogAlertRule1"
```

## <span data-ttu-id="86e8c-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86e8c-109">PARAMETERS</span></span>

### <span data-ttu-id="86e8c-110">-Action</span><span class="sxs-lookup"><span data-stu-id="86e8c-110">-Action</span></span>
<span data-ttu-id="86e8c-111">Azione di avviso per la regola di query pianificata</span><span class="sxs-lookup"><span data-stu-id="86e8c-111">The scheduled query rule Alerting Action</span></span>

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

### <span data-ttu-id="86e8c-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="86e8c-112">-AsJob</span></span>
<span data-ttu-id="86e8c-113">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="86e8c-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="86e8c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86e8c-114">-DefaultProfile</span></span>
<span data-ttu-id="86e8c-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="86e8c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86e8c-116">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="86e8c-116">-Description</span></span>
<span data-ttu-id="86e8c-117">Descrizione dell'avviso</span><span class="sxs-lookup"><span data-stu-id="86e8c-117">The description for this alert</span></span>

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

### <span data-ttu-id="86e8c-118">-Enabled</span><span class="sxs-lookup"><span data-stu-id="86e8c-118">-Enabled</span></span>
<span data-ttu-id="86e8c-119">Stato di avviso azure - valori validi - $true, $false</span><span class="sxs-lookup"><span data-stu-id="86e8c-119">The azure alert state - valid values - $true, $false</span></span>

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

### <span data-ttu-id="86e8c-120">-Location</span><span class="sxs-lookup"><span data-stu-id="86e8c-120">-Location</span></span>
<span data-ttu-id="86e8c-121">Posizione dell'avviso</span><span class="sxs-lookup"><span data-stu-id="86e8c-121">The location for this alert</span></span>

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

### <span data-ttu-id="86e8c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="86e8c-122">-Name</span></span>
<span data-ttu-id="86e8c-123">Nome dell'avviso</span><span class="sxs-lookup"><span data-stu-id="86e8c-123">The alert name</span></span>

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

### <span data-ttu-id="86e8c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86e8c-124">-ResourceGroupName</span></span>
<span data-ttu-id="86e8c-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="86e8c-125">The resource group name</span></span>

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

### <span data-ttu-id="86e8c-126">-Pianificazione</span><span class="sxs-lookup"><span data-stu-id="86e8c-126">-Schedule</span></span>
<span data-ttu-id="86e8c-127">Pianificazione delle regole di query pianificate</span><span class="sxs-lookup"><span data-stu-id="86e8c-127">The scheduled query rule schedule</span></span>

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

### <span data-ttu-id="86e8c-128">-Source</span><span class="sxs-lookup"><span data-stu-id="86e8c-128">-Source</span></span>
<span data-ttu-id="86e8c-129">Origine della regola di query pianificata</span><span class="sxs-lookup"><span data-stu-id="86e8c-129">The scheduled query rule source</span></span>

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

### <span data-ttu-id="86e8c-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="86e8c-130">-Tag</span></span>
<span data-ttu-id="86e8c-131">Tag di risorse</span><span class="sxs-lookup"><span data-stu-id="86e8c-131">Resource tags</span></span>

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

### <span data-ttu-id="86e8c-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="86e8c-132">-Confirm</span></span>
<span data-ttu-id="86e8c-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86e8c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86e8c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86e8c-134">-WhatIf</span></span>
<span data-ttu-id="86e8c-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="86e8c-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="86e8c-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="86e8c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86e8c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86e8c-137">CommonParameters</span></span>
<span data-ttu-id="86e8c-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86e8c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86e8c-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="86e8c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86e8c-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="86e8c-140">INPUTS</span></span>

### <span data-ttu-id="86e8c-141">System.String</span><span class="sxs-lookup"><span data-stu-id="86e8c-141">System.String</span></span>

## <span data-ttu-id="86e8c-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="86e8c-142">OUTPUTS</span></span>

### <span data-ttu-id="86e8c-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="86e8c-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="86e8c-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="86e8c-144">NOTES</span></span>

## <span data-ttu-id="86e8c-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="86e8c-145">RELATED LINKS</span></span>
