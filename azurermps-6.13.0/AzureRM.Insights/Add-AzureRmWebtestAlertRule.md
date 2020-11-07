---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: FBAE5F75-1E28-4F1C-A9ED-20075FFD4AC7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermwebtestalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmWebtestAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmWebtestAlertRule.md
ms.openlocfilehash: 08d84c1f5e71c18a47e48bda1e39ce37ed0cb026
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686188"
---
# <span data-ttu-id="7f140-101">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="7f140-101">Add-AzureRmWebtestAlertRule</span></span>

## <span data-ttu-id="7f140-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7f140-102">SYNOPSIS</span></span>
<span data-ttu-id="7f140-103">Aggiunge o aggiorna una regola di avviso di WebTest.</span><span class="sxs-lookup"><span data-stu-id="7f140-103">Adds or updates a webtest alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f140-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7f140-104">SYNTAX</span></span>

```
Add-AzureRmWebtestAlertRule -MetricName <String> -TargetResourceUri <String> -WindowSize <TimeSpan>
 -FailedLocationCount <Int32> [-MetricNamespace <String>] -Location <String> [-Description <String>]
 [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f140-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f140-105">DESCRIPTION</span></span>
<span data-ttu-id="7f140-106">Il cmdlet **Add-AzureRmWebtestAlertRule** aggiunge o aggiorna una regola di avviso di tipo Metric, Event o WebTest.</span><span class="sxs-lookup"><span data-stu-id="7f140-106">The **Add-AzureRmWebtestAlertRule** cmdlet adds or updates an alert rule of either metric, event, or webtest type.</span></span>
<span data-ttu-id="7f140-107">La regola aggiunta è associata a un gruppo di risorse e ha un nome.</span><span class="sxs-lookup"><span data-stu-id="7f140-107">The added rule is associated to a resource group and has a name.</span></span>
<span data-ttu-id="7f140-108">Questo cmdlet implementa il modello ShouldProcess, vale a dire che potrebbe richiedere conferma all'utente prima di creare, modificare o rimuovere la risorsa.</span><span class="sxs-lookup"><span data-stu-id="7f140-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="7f140-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7f140-109">EXAMPLES</span></span>

### <span data-ttu-id="7f140-110">Esempio 1: aggiungere una regola di avviso di WebTest</span><span class="sxs-lookup"><span data-stu-id="7f140-110">Example 1: Add a webtest alert rule</span></span>
```
PS C:\>Add-AzureRmWebtestAlertRule -Name "webtestRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -WindowSize 00:05:00 -MetricName "metric" -TargetResourceUri ":/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourcegroups/Default-Web-WestUS/providers/microsoft.insights/webtests/leowebtestr1-webtestr1" -Description "Nice Webtest rule" -Failed 3
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="7f140-111">Questo comando aggiunge o aggiorna una regola di avviso di WebTest.</span><span class="sxs-lookup"><span data-stu-id="7f140-111">This command adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="7f140-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7f140-112">PARAMETERS</span></span>

### <span data-ttu-id="7f140-113">-Azione</span><span class="sxs-lookup"><span data-stu-id="7f140-113">-Action</span></span>
<span data-ttu-id="7f140-114">Specifica un elenco di azioni delimitato da virgole.</span><span class="sxs-lookup"><span data-stu-id="7f140-114">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="7f140-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f140-115">-DefaultProfile</span></span>
<span data-ttu-id="7f140-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7f140-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f140-117">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f140-117">-Description</span></span>
<span data-ttu-id="7f140-118">Specifica una descrizione della regola.</span><span class="sxs-lookup"><span data-stu-id="7f140-118">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="7f140-119">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="7f140-119">-DisableRule</span></span>
<span data-ttu-id="7f140-120">Disabilita la regola.</span><span class="sxs-lookup"><span data-stu-id="7f140-120">Disables the rule.</span></span>
<span data-ttu-id="7f140-121">Se non specifichi questo parametro, la regola è abilitata.</span><span class="sxs-lookup"><span data-stu-id="7f140-121">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="7f140-122">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="7f140-122">-FailedLocationCount</span></span>
<span data-ttu-id="7f140-123">Specifica il conteggio della posizione non riuscito per le regole di WebTest.</span><span class="sxs-lookup"><span data-stu-id="7f140-123">Specifies the failed location count for the webtest rules.</span></span>
<span data-ttu-id="7f140-124">Questa operazione è simile alla soglia degli altri tipi di regole.</span><span class="sxs-lookup"><span data-stu-id="7f140-124">This is similar to the threshold in the other types of rules.</span></span>

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

### <span data-ttu-id="7f140-125">-Posizione</span><span class="sxs-lookup"><span data-stu-id="7f140-125">-Location</span></span>
<span data-ttu-id="7f140-126">Specifica la posizione in cui è definita la regola.</span><span class="sxs-lookup"><span data-stu-id="7f140-126">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="7f140-127">-Metricname</span><span class="sxs-lookup"><span data-stu-id="7f140-127">-MetricName</span></span>
<span data-ttu-id="7f140-128">Specifica il nome della metrica.</span><span class="sxs-lookup"><span data-stu-id="7f140-128">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="7f140-129">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="7f140-129">-MetricNamespace</span></span>
<span data-ttu-id="7f140-130">Specifica lo spazio dei nomi Metric per Rule.</span><span class="sxs-lookup"><span data-stu-id="7f140-130">Specifies the metric namespace for rule.</span></span>

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

### <span data-ttu-id="7f140-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="7f140-131">-Name</span></span>
<span data-ttu-id="7f140-132">Specifica il nome della regola.</span><span class="sxs-lookup"><span data-stu-id="7f140-132">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="7f140-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f140-133">-ResourceGroupName</span></span>
<span data-ttu-id="7f140-134">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7f140-134">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="7f140-135">-TargetResourceUri</span><span class="sxs-lookup"><span data-stu-id="7f140-135">-TargetResourceUri</span></span>
<span data-ttu-id="7f140-136">Specifica l'ID risorsa del WebTest.</span><span class="sxs-lookup"><span data-stu-id="7f140-136">Specifies the resource ID of the webtest.</span></span>

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

### <span data-ttu-id="7f140-137">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="7f140-137">-WindowSize</span></span>
<span data-ttu-id="7f140-138">Specifica le dimensioni della finestra temporale per la regola per calcolare i dati.</span><span class="sxs-lookup"><span data-stu-id="7f140-138">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="7f140-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7f140-139">-Confirm</span></span>
<span data-ttu-id="7f140-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f140-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f140-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f140-141">-WhatIf</span></span>
<span data-ttu-id="7f140-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7f140-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7f140-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7f140-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f140-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f140-144">CommonParameters</span></span>
<span data-ttu-id="7f140-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f140-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f140-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f140-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f140-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7f140-147">INPUTS</span></span>

### <span data-ttu-id="7f140-148">System. String</span><span class="sxs-lookup"><span data-stu-id="7f140-148">System.String</span></span>

### <span data-ttu-id="7f140-149">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="7f140-149">System.TimeSpan</span></span>

### <span data-ttu-id="7f140-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="7f140-150">System.Int32</span></span>

### <span data-ttu-id="7f140-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7f140-151">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="7f140-152">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. monitor. Management. Models. RuleAction, Microsoft. Azure. Commands. Insights, Version = 5.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="7f140-152">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="7f140-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7f140-153">OUTPUTS</span></span>

### <span data-ttu-id="7f140-154">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="7f140-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="7f140-155">Note</span><span class="sxs-lookup"><span data-stu-id="7f140-155">NOTES</span></span>

## <span data-ttu-id="7f140-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7f140-156">RELATED LINKS</span></span>

[<span data-ttu-id="7f140-157">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="7f140-157">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="7f140-158">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="7f140-158">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="7f140-159">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="7f140-159">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="7f140-160">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="7f140-160">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


