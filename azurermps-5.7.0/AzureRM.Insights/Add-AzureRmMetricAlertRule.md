---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A90564B5-57D7-48EB-976D-38C03D930289
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermmetricalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmMetricAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmMetricAlertRule.md
ms.openlocfilehash: 097f3562ca326275c050054fd07d11d349cf98d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514304"
---
# <span data-ttu-id="f4256-101">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="f4256-101">Add-AzureRmMetricAlertRule</span></span>

## <span data-ttu-id="f4256-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f4256-102">SYNOPSIS</span></span>
<span data-ttu-id="f4256-103">Aggiunge o aggiorna una regola di avviso basata su metriche.</span><span class="sxs-lookup"><span data-stu-id="f4256-103">Adds or updates a metric-based alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4256-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f4256-104">SYNTAX</span></span>

```
Add-AzureRmMetricAlertRule -WindowSize <TimeSpan> -Operator <ConditionOperator> -Threshold <Double>
 -TargetResourceId <String> -MetricName <String> -TimeAggregationOperator <TimeAggregationOperator>
 -Location <String> [-Description <String>] [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4256-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4256-105">DESCRIPTION</span></span>
<span data-ttu-id="f4256-106">Il cmdlet **Add-AzureRmMetricAlertRule** aggiunge o aggiorna una regola di avviso basata su metriche.</span><span class="sxs-lookup"><span data-stu-id="f4256-106">The **Add-AzureRmMetricAlertRule** cmdlet adds or updates a metric-based alert rule.</span></span>
<span data-ttu-id="f4256-107">La regola aggiunta è associata a un gruppo di risorse e ha un nome.</span><span class="sxs-lookup"><span data-stu-id="f4256-107">The added rule is associated with a resource group and has a name.</span></span>
<span data-ttu-id="f4256-108">Questo cmdlet implementa il modello ShouldProcess, vale a dire che potrebbe richiedere conferma all'utente prima di creare, modificare o rimuovere la risorsa.</span><span class="sxs-lookup"><span data-stu-id="f4256-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="f4256-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f4256-109">EXAMPLES</span></span>

### <span data-ttu-id="f4256-110">Esempio 1: aggiungere una regola di avviso metrica a un sito Web</span><span class="sxs-lookup"><span data-stu-id="f4256-110">Example 1: Add a metric alert rule to a website</span></span>
```
PS C:\>Add-AzureRMMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -Description "Pura Vida" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
33574ccf-0b01-43b4-aa97-87e6bbcf1c11                                                                         Created
```

<span data-ttu-id="f4256-111">Questo comando crea una regola di avviso metrica per un sito Web.</span><span class="sxs-lookup"><span data-stu-id="f4256-111">This command creates a metric alert rule for a website.</span></span>

### <span data-ttu-id="f4256-112">Esempio 2: disabilitare una regola</span><span class="sxs-lookup"><span data-stu-id="f4256-112">Example 2: Disable a rule</span></span>
```
PS C:\>Add-AzureRMMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup Default-Web-EastUS -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -TimeAggregationOperator Total 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
96c489f1-8529-46e1-a76d-2c1463ca3116                                                                                 OK
```

<span data-ttu-id="f4256-113">Questo comando Disabilita una regola.</span><span class="sxs-lookup"><span data-stu-id="f4256-113">This command disables a rule.</span></span>
<span data-ttu-id="f4256-114">Se la regola non esiste, la crea disabilitata.</span><span class="sxs-lookup"><span data-stu-id="f4256-114">If the rule does not exist, it creates it disabled.</span></span>
<span data-ttu-id="f4256-115">Se la regola esiste, viene semplicemente disabilitata.</span><span class="sxs-lookup"><span data-stu-id="f4256-115">If the rule exists, then it just disables it.</span></span>

### <span data-ttu-id="f4256-116">Esempio 3: aggiungere una regola con le azioni</span><span class="sxs-lookup"><span data-stu-id="f4256-116">Example 3: Add a rule with actions</span></span>
```
PS C:\>Add-AzureRmMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 1 -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -MetricName "Requests" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="f4256-117">Questo comando crea una regola di avviso metrica per un sito Web.</span><span class="sxs-lookup"><span data-stu-id="f4256-117">This command creates a metric alert rule for a website.</span></span>

## <span data-ttu-id="f4256-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f4256-118">PARAMETERS</span></span>

### <span data-ttu-id="f4256-119">-Azione</span><span class="sxs-lookup"><span data-stu-id="f4256-119">-Action</span></span>
<span data-ttu-id="f4256-120">Specifica un elenco di azioni delimitato da virgole.</span><span class="sxs-lookup"><span data-stu-id="f4256-120">Specifies a comma-separated list of actions.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]
Parameter Sets: (All)
Aliases: Actions

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4256-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4256-121">-DefaultProfile</span></span>
<span data-ttu-id="f4256-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f4256-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4256-123">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4256-123">-Description</span></span>
<span data-ttu-id="f4256-124">Specifica una descrizione della regola.</span><span class="sxs-lookup"><span data-stu-id="f4256-124">Specifies a description of the rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4256-125">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="f4256-125">-DisableRule</span></span>
<span data-ttu-id="f4256-126">Disabilita la regola.</span><span class="sxs-lookup"><span data-stu-id="f4256-126">Disables the rule.</span></span>
<span data-ttu-id="f4256-127">Se non specifichi questo parametro, la regola è abilitata.</span><span class="sxs-lookup"><span data-stu-id="f4256-127">If you do not specify this parameter, the rule is enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4256-128">-Posizione</span><span class="sxs-lookup"><span data-stu-id="f4256-128">-Location</span></span>
<span data-ttu-id="f4256-129">Specifica la posizione in cui è definita la regola.</span><span class="sxs-lookup"><span data-stu-id="f4256-129">Specifies the location where the rule is defined.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4256-130">-Metricname</span><span class="sxs-lookup"><span data-stu-id="f4256-130">-MetricName</span></span>
<span data-ttu-id="f4256-131">Specifica il nome della metrica che la regola sta monitorando.</span><span class="sxs-lookup"><span data-stu-id="f4256-131">Specifies the name of the metric the rule is monitoring.</span></span>
<span data-ttu-id="f4256-132">Specifica questo parametro solo per le regole basate su metriche.</span><span class="sxs-lookup"><span data-stu-id="f4256-132">Specify this parameter only for metric-based rules.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4256-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="f4256-133">-Name</span></span>
<span data-ttu-id="f4256-134">Specifica il nome della regola.</span><span class="sxs-lookup"><span data-stu-id="f4256-134">Specifies the name of the rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4256-135">-Operator</span><span class="sxs-lookup"><span data-stu-id="f4256-135">-Operator</span></span>
<span data-ttu-id="f4256-136">Specifica l'operatore relazionale per la condizione della regola.</span><span class="sxs-lookup"><span data-stu-id="f4256-136">Specifies the relational operator for the condition of the rule.</span></span>
<span data-ttu-id="f4256-137">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f4256-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f4256-138">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="f4256-138">GreaterThan</span></span>
- <span data-ttu-id="f4256-139">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="f4256-139">GreaterThanOrEqual</span></span>
-  <span data-ttu-id="f4256-140">LessThan</span><span class="sxs-lookup"><span data-stu-id="f4256-140">LessThan</span></span>
- <span data-ttu-id="f4256-141">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="f4256-141">LessThanOrEqual</span></span>

```yaml
Type: ConditionOperator
Parameter Sets: (All)
Aliases: 
Accepted values: GreaterThan, GreaterThanOrEqual, LessThan, LessThanOrEqual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4256-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4256-142">-ResourceGroupName</span></span>
<span data-ttu-id="f4256-143">Specifica il nome del gruppo di risorse per la regola.</span><span class="sxs-lookup"><span data-stu-id="f4256-143">Specifies the name of the resource group for the rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4256-144">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="f4256-144">-TargetResourceId</span></span>
<span data-ttu-id="f4256-145">Specifica l'ID della risorsa che la regola sta monitorando.</span><span class="sxs-lookup"><span data-stu-id="f4256-145">Specifies the ID of the resource the rule is monitoring.</span></span> <span data-ttu-id="f4256-146">Nota: non è possibile aggiornare questa proprietà per una regola di avviso esistente.</span><span class="sxs-lookup"><span data-stu-id="f4256-146">NOTE: This property cannot be updated for an existing alert rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4256-147">-Soglia</span><span class="sxs-lookup"><span data-stu-id="f4256-147">-Threshold</span></span>
<span data-ttu-id="f4256-148">Specifica la soglia della regola.</span><span class="sxs-lookup"><span data-stu-id="f4256-148">Specifies the threshold of the rule.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4256-149">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="f4256-149">-TimeAggregationOperator</span></span>
<span data-ttu-id="f4256-150">Specifica l'operatore di aggregazione da applicare alla finestra temporale quando la regola viene valutata.</span><span class="sxs-lookup"><span data-stu-id="f4256-150">Specifies the aggregation operator to apply to the time window when the rule is being evaluated.</span></span>

```yaml
Type: TimeAggregationOperator
Parameter Sets: (All)
Aliases: 
Accepted values: Average, Minimum, Maximum, Total, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4256-151">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="f4256-151">-WindowSize</span></span>
<span data-ttu-id="f4256-152">Specifica le dimensioni della finestra temporale per la regola per calcolare i dati.</span><span class="sxs-lookup"><span data-stu-id="f4256-152">Specifies the time window size for the rule to compute its data.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4256-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4256-153">CommonParameters</span></span>
<span data-ttu-id="f4256-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4256-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4256-155">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4256-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4256-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f4256-156">INPUTS</span></span>

### <span data-ttu-id="f4256-157">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f4256-157">None</span></span>
<span data-ttu-id="f4256-158">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="f4256-158">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f4256-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f4256-159">OUTPUTS</span></span>

### <span data-ttu-id="f4256-160">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f4256-160">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="f4256-161">Note</span><span class="sxs-lookup"><span data-stu-id="f4256-161">NOTES</span></span>

## <span data-ttu-id="f4256-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f4256-162">RELATED LINKS</span></span>

[<span data-ttu-id="f4256-163">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f4256-163">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="f4256-164">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="f4256-164">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="f4256-165">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="f4256-165">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="f4256-166">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="f4256-166">Get-AzureRmAlertRule</span></span>](./Get-AzureRmAlertRule.md)

[<span data-ttu-id="f4256-167">New-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="f4256-167">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="f4256-168">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="f4256-168">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)

[<span data-ttu-id="f4256-169">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="f4256-169">Remove-AzureRmAlertRule</span></span>](./Remove-AzureRmAlertRule.md)


