---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: FBAE5F75-1E28-4F1C-A9ED-20075FFD4AC7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azwebtestalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Add-AzWebtestAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Add-AzWebtestAlertRule.md
ms.openlocfilehash: 9ab1688931c39da6302edbec1f206ca905ea7916
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862961"
---
# <span data-ttu-id="aaab4-101">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="aaab4-101">Add-AzWebtestAlertRule</span></span>

## <span data-ttu-id="aaab4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aaab4-102">SYNOPSIS</span></span>
<span data-ttu-id="aaab4-103">Aggiunge o aggiorna una regola di avviso di WebTest.</span><span class="sxs-lookup"><span data-stu-id="aaab4-103">Adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="aaab4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aaab4-104">SYNTAX</span></span>

```
Add-AzWebtestAlertRule -MetricName <String> -TargetResourceUri <String> -WindowSize <TimeSpan>
 -FailedLocationCount <Int32> [-MetricNamespace <String>] -Location <String> [-Description <String>]
 [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aaab4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aaab4-105">DESCRIPTION</span></span>
<span data-ttu-id="aaab4-106">Il cmdlet **Add-AzWebtestAlertRule** aggiunge o aggiorna una regola di avviso di tipo Metric, Event o WebTest.</span><span class="sxs-lookup"><span data-stu-id="aaab4-106">The **Add-AzWebtestAlertRule** cmdlet adds or updates an alert rule of either metric, event, or webtest type.</span></span>
<span data-ttu-id="aaab4-107">La regola aggiunta è associata a un gruppo di risorse e ha un nome.</span><span class="sxs-lookup"><span data-stu-id="aaab4-107">The added rule is associated to a resource group and has a name.</span></span>
<span data-ttu-id="aaab4-108">Questo cmdlet implementa il modello ShouldProcess, vale a dire che potrebbe richiedere conferma all'utente prima di creare, modificare o rimuovere la risorsa.</span><span class="sxs-lookup"><span data-stu-id="aaab4-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="aaab4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aaab4-109">EXAMPLES</span></span>

### <span data-ttu-id="aaab4-110">Esempio 1: aggiungere una regola di avviso di WebTest</span><span class="sxs-lookup"><span data-stu-id="aaab4-110">Example 1: Add a webtest alert rule</span></span>
```
PS C:\>Add-AzWebtestAlertRule -Name "webtestRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -WindowSize 00:05:00 -MetricName "metric" -TargetResourceUri "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourcegroups/Default-Web-WestUS/providers/microsoft.insights/webtests/leowebtestr1-webtestr1" -Description "Nice Webtest rule" -Failed 3
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="aaab4-111">Questo comando aggiunge o aggiorna una regola di avviso di WebTest.</span><span class="sxs-lookup"><span data-stu-id="aaab4-111">This command adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="aaab4-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aaab4-112">PARAMETERS</span></span>

### <span data-ttu-id="aaab4-113">-Azione</span><span class="sxs-lookup"><span data-stu-id="aaab4-113">-Action</span></span>
<span data-ttu-id="aaab4-114">Specifica un elenco di azioni delimitato da virgole.</span><span class="sxs-lookup"><span data-stu-id="aaab4-114">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="aaab4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaab4-115">-DefaultProfile</span></span>
<span data-ttu-id="aaab4-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="aaab4-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aaab4-117">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="aaab4-117">-Description</span></span>
<span data-ttu-id="aaab4-118">Specifica una descrizione della regola.</span><span class="sxs-lookup"><span data-stu-id="aaab4-118">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="aaab4-119">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="aaab4-119">-DisableRule</span></span>
<span data-ttu-id="aaab4-120">Disabilita la regola.</span><span class="sxs-lookup"><span data-stu-id="aaab4-120">Disables the rule.</span></span>
<span data-ttu-id="aaab4-121">Se non specifichi questo parametro, la regola è abilitata.</span><span class="sxs-lookup"><span data-stu-id="aaab4-121">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="aaab4-122">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="aaab4-122">-FailedLocationCount</span></span>
<span data-ttu-id="aaab4-123">Specifica il conteggio della posizione non riuscito per le regole di WebTest.</span><span class="sxs-lookup"><span data-stu-id="aaab4-123">Specifies the failed location count for the webtest rules.</span></span>
<span data-ttu-id="aaab4-124">Questa operazione è simile alla soglia degli altri tipi di regole.</span><span class="sxs-lookup"><span data-stu-id="aaab4-124">This is similar to the threshold in the other types of rules.</span></span>

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

### <span data-ttu-id="aaab4-125">-Posizione</span><span class="sxs-lookup"><span data-stu-id="aaab4-125">-Location</span></span>
<span data-ttu-id="aaab4-126">Specifica la posizione in cui è definita la regola.</span><span class="sxs-lookup"><span data-stu-id="aaab4-126">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="aaab4-127">-Metricname</span><span class="sxs-lookup"><span data-stu-id="aaab4-127">-MetricName</span></span>
<span data-ttu-id="aaab4-128">Specifica il nome della metrica.</span><span class="sxs-lookup"><span data-stu-id="aaab4-128">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="aaab4-129">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="aaab4-129">-MetricNamespace</span></span>
<span data-ttu-id="aaab4-130">Specifica lo spazio dei nomi Metric per Rule.</span><span class="sxs-lookup"><span data-stu-id="aaab4-130">Specifies the metric namespace for rule.</span></span>

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

### <span data-ttu-id="aaab4-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="aaab4-131">-Name</span></span>
<span data-ttu-id="aaab4-132">Specifica il nome della regola.</span><span class="sxs-lookup"><span data-stu-id="aaab4-132">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="aaab4-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaab4-133">-ResourceGroupName</span></span>
<span data-ttu-id="aaab4-134">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="aaab4-134">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="aaab4-135">-TargetResourceUri</span><span class="sxs-lookup"><span data-stu-id="aaab4-135">-TargetResourceUri</span></span>
<span data-ttu-id="aaab4-136">Specifica l'ID risorsa del WebTest.</span><span class="sxs-lookup"><span data-stu-id="aaab4-136">Specifies the resource ID of the webtest.</span></span>

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

### <span data-ttu-id="aaab4-137">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="aaab4-137">-WindowSize</span></span>
<span data-ttu-id="aaab4-138">Specifica le dimensioni della finestra temporale per la regola per calcolare i dati.</span><span class="sxs-lookup"><span data-stu-id="aaab4-138">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="aaab4-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="aaab4-139">-Confirm</span></span>
<span data-ttu-id="aaab4-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aaab4-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aaab4-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aaab4-141">-WhatIf</span></span>
<span data-ttu-id="aaab4-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aaab4-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aaab4-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aaab4-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aaab4-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaab4-144">CommonParameters</span></span>
<span data-ttu-id="aaab4-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aaab4-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaab4-146">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aaab4-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaab4-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aaab4-147">INPUTS</span></span>

### <span data-ttu-id="aaab4-148">System. String</span><span class="sxs-lookup"><span data-stu-id="aaab4-148">System.String</span></span>

### <span data-ttu-id="aaab4-149">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="aaab4-149">System.TimeSpan</span></span>

### <span data-ttu-id="aaab4-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="aaab4-150">System.Int32</span></span>

### <span data-ttu-id="aaab4-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="aaab4-151">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="aaab4-152">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. monitor. Management. Models. RuleAction, Microsoft. Azure. PowerShell. cmdlet. monitor, versione = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="aaab4-152">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="aaab4-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aaab4-153">OUTPUTS</span></span>

### <span data-ttu-id="aaab4-154">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="aaab4-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="aaab4-155">Note</span><span class="sxs-lookup"><span data-stu-id="aaab4-155">NOTES</span></span>

## <span data-ttu-id="aaab4-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aaab4-156">RELATED LINKS</span></span>

[<span data-ttu-id="aaab4-157">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="aaab4-157">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="aaab4-158">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="aaab4-158">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="aaab4-159">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="aaab4-159">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="aaab4-160">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="aaab4-160">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)


