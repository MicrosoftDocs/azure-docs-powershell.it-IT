---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: FBAE5F75-1E28-4F1C-A9ED-20075FFD4AC7
online version: https://docs.microsoft.com/powershell/module/az.monitor/add-azwebtestalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzWebtestAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzWebtestAlertRule.md
ms.openlocfilehash: 8f66117d4ae2909617a6215c1c154ba22d469b21
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980254"
---
# <span data-ttu-id="88deb-101">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="88deb-101">Add-AzWebtestAlertRule</span></span>

## <span data-ttu-id="88deb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88deb-102">SYNOPSIS</span></span>
<span data-ttu-id="88deb-103">Aggiunge o aggiorna una regola di avviso di test Web.</span><span class="sxs-lookup"><span data-stu-id="88deb-103">Adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="88deb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="88deb-104">SYNTAX</span></span>

```
Add-AzWebtestAlertRule -MetricName <String> -TargetResourceUri <String> -WindowSize <TimeSpan>
 -FailedLocationCount <Int32> [-MetricNamespace <String>] -Location <String> [-Description <String>]
 [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88deb-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="88deb-105">DESCRIPTION</span></span>
<span data-ttu-id="88deb-106">Il cmdlet **Add-AzWebtestAlertRule** aggiunge o aggiorna una regola di avviso di tipo metrico, evento o test Web.</span><span class="sxs-lookup"><span data-stu-id="88deb-106">The **Add-AzWebtestAlertRule** cmdlet adds or updates an alert rule of either metric, event, or webtest type.</span></span>
<span data-ttu-id="88deb-107">La regola aggiunta è associata a un gruppo di risorse e ha un nome.</span><span class="sxs-lookup"><span data-stu-id="88deb-107">The added rule is associated to a resource group and has a name.</span></span>
<span data-ttu-id="88deb-108">Questo cmdlet implementa il criterio ShouldProcess, ad esempio potrebbe richiedere conferma all'utente prima di creare, modificare o rimuovere effettivamente la risorsa.</span><span class="sxs-lookup"><span data-stu-id="88deb-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="88deb-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="88deb-109">EXAMPLES</span></span>

### <span data-ttu-id="88deb-110">Esempio 1: Aggiungere una regola di avviso test Web</span><span class="sxs-lookup"><span data-stu-id="88deb-110">Example 1: Add a webtest alert rule</span></span>
```
PS C:\>Add-AzWebtestAlertRule -Name "webtestRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -WindowSize 00:05:00 -MetricName "metric" -TargetResourceUri "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourcegroups/Default-Web-WestUS/providers/microsoft.insights/webtests/leowebtestr1-webtestr1" -Description "Nice Webtest rule" -Failed 3
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="88deb-111">Questo comando aggiunge o aggiorna una regola di avviso di test Web.</span><span class="sxs-lookup"><span data-stu-id="88deb-111">This command adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="88deb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88deb-112">PARAMETERS</span></span>

### <span data-ttu-id="88deb-113">-Action</span><span class="sxs-lookup"><span data-stu-id="88deb-113">-Action</span></span>
<span data-ttu-id="88deb-114">Specifica un elenco di azioni separato da virgole.</span><span class="sxs-lookup"><span data-stu-id="88deb-114">Specifies a comma-separated list of actions.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88deb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88deb-115">-DefaultProfile</span></span>
<span data-ttu-id="88deb-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="88deb-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88deb-117">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="88deb-117">-Description</span></span>
<span data-ttu-id="88deb-118">Specifica una descrizione della regola.</span><span class="sxs-lookup"><span data-stu-id="88deb-118">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="88deb-119">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="88deb-119">-DisableRule</span></span>
<span data-ttu-id="88deb-120">Disabilita la regola.</span><span class="sxs-lookup"><span data-stu-id="88deb-120">Disables the rule.</span></span>
<span data-ttu-id="88deb-121">Se non si specifica questo parametro, la regola viene abilitata.</span><span class="sxs-lookup"><span data-stu-id="88deb-121">If you do not specify this parameter, the rule is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88deb-122">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="88deb-122">-FailedLocationCount</span></span>
<span data-ttu-id="88deb-123">Specifica il numero di posizione non riuscite per le regole di test Web.</span><span class="sxs-lookup"><span data-stu-id="88deb-123">Specifies the failed location count for the webtest rules.</span></span>
<span data-ttu-id="88deb-124">Questa soglia è simile a quella degli altri tipi di regole.</span><span class="sxs-lookup"><span data-stu-id="88deb-124">This is similar to the threshold in the other types of rules.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88deb-125">-Location</span><span class="sxs-lookup"><span data-stu-id="88deb-125">-Location</span></span>
<span data-ttu-id="88deb-126">Specifica la posizione in cui è definita la regola.</span><span class="sxs-lookup"><span data-stu-id="88deb-126">Specifies the location where the rule is defined.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88deb-127">-MetricName</span><span class="sxs-lookup"><span data-stu-id="88deb-127">-MetricName</span></span>
<span data-ttu-id="88deb-128">Specifica il nome della metrica.</span><span class="sxs-lookup"><span data-stu-id="88deb-128">Specifies the name of the metric.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88deb-129">-MetricMetricMetric</span><span class="sxs-lookup"><span data-stu-id="88deb-129">-MetricNamespace</span></span>
<span data-ttu-id="88deb-130">Specifica lo spazio dei nomi metrico per la regola.</span><span class="sxs-lookup"><span data-stu-id="88deb-130">Specifies the metric namespace for rule.</span></span>

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

### <span data-ttu-id="88deb-131">-Name</span><span class="sxs-lookup"><span data-stu-id="88deb-131">-Name</span></span>
<span data-ttu-id="88deb-132">Specifica il nome della regola.</span><span class="sxs-lookup"><span data-stu-id="88deb-132">Specifies the name of the rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88deb-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88deb-133">-ResourceGroupName</span></span>
<span data-ttu-id="88deb-134">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="88deb-134">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88deb-135">-TargetResourceUri</span><span class="sxs-lookup"><span data-stu-id="88deb-135">-TargetResourceUri</span></span>
<span data-ttu-id="88deb-136">Specifica l'ID della risorsa del test Web.</span><span class="sxs-lookup"><span data-stu-id="88deb-136">Specifies the resource ID of the webtest.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88deb-137">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="88deb-137">-WindowSize</span></span>
<span data-ttu-id="88deb-138">Specifica le dimensioni dell'intervallo di tempo per il calcolo dei dati da parte della regola.</span><span class="sxs-lookup"><span data-stu-id="88deb-138">Specifies the time window size for the rule to compute its data.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88deb-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="88deb-139">-Confirm</span></span>
<span data-ttu-id="88deb-140">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88deb-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88deb-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88deb-141">-WhatIf</span></span>
<span data-ttu-id="88deb-142">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="88deb-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="88deb-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="88deb-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88deb-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88deb-144">CommonParameters</span></span>
<span data-ttu-id="88deb-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88deb-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88deb-146">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="88deb-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88deb-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="88deb-147">INPUTS</span></span>

### <span data-ttu-id="88deb-148">System.String</span><span class="sxs-lookup"><span data-stu-id="88deb-148">System.String</span></span>

### <span data-ttu-id="88deb-149">System.TimeSpan</span><span class="sxs-lookup"><span data-stu-id="88deb-149">System.TimeSpan</span></span>

### <span data-ttu-id="88deb-150">System.Int32</span><span class="sxs-lookup"><span data-stu-id="88deb-150">System.Int32</span></span>

### <span data-ttu-id="88deb-151">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="88deb-151">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="88deb-152">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="88deb-152">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="88deb-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="88deb-153">OUTPUTS</span></span>

### <span data-ttu-id="88deb-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="88deb-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="88deb-155">NOTE</span><span class="sxs-lookup"><span data-stu-id="88deb-155">NOTES</span></span>

## <span data-ttu-id="88deb-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="88deb-156">RELATED LINKS</span></span>

[<span data-ttu-id="88deb-157">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="88deb-157">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="88deb-158">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="88deb-158">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="88deb-159">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="88deb-159">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="88deb-160">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="88deb-160">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)


