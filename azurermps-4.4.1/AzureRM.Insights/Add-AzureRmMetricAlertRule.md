---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A90564B5-57D7-48EB-976D-38C03D930289
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmMetricAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmMetricAlertRule.md
ms.openlocfilehash: 9a215195ada1d804d2c139ed748eb844df46eed5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688293"
---
# <span data-ttu-id="cc615-101">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="cc615-101">Add-AzureRmMetricAlertRule</span></span>

## <span data-ttu-id="cc615-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cc615-102">SYNOPSIS</span></span>
<span data-ttu-id="cc615-103">Aggiunge o aggiorna una regola di avviso basata su metriche.</span><span class="sxs-lookup"><span data-stu-id="cc615-103">Adds or updates a metric-based alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc615-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cc615-104">SYNTAX</span></span>

```
Add-AzureRmMetricAlertRule -WindowSize <TimeSpan> -Operator <ConditionOperator> -Threshold <Double>
 -TargetResourceId <String> -MetricName <String> -TimeAggregationOperator <TimeAggregationOperator>
 -Location <String> [-Description <String>] [-DisableRule] -ResourceGroup <String> -Name <String>
 [-Actions <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc615-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cc615-105">DESCRIPTION</span></span>
<span data-ttu-id="cc615-106">Il cmdlet **Add-AzureRmMetricAlertRule** aggiunge o aggiorna una regola di avviso basata su metriche.</span><span class="sxs-lookup"><span data-stu-id="cc615-106">The **Add-AzureRmMetricAlertRule** cmdlet adds or updates a metric-based alert rule.</span></span>
<span data-ttu-id="cc615-107">La regola aggiunta è associata a un gruppo di risorse e ha un nome.</span><span class="sxs-lookup"><span data-stu-id="cc615-107">The added rule is associated with a resource group and has a name.</span></span>

## <span data-ttu-id="cc615-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cc615-108">EXAMPLES</span></span>

### <span data-ttu-id="cc615-109">Esempio 1: aggiungere una regola di avviso metrica a un sito Web</span><span class="sxs-lookup"><span data-stu-id="cc615-109">Example 1: Add a metric alert rule to a website</span></span>
```
PS C:\>Add-AzureRMMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -Description "Pura Vida" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
33574ccf-0b01-43b4-aa97-87e6bbcf1c11                                                                         Created
```

<span data-ttu-id="cc615-110">Questo comando crea una regola di avviso metrica per un sito Web.</span><span class="sxs-lookup"><span data-stu-id="cc615-110">This command creates a metric alert rule for a website.</span></span>

### <span data-ttu-id="cc615-111">Esempio 2: disabilitare una regola</span><span class="sxs-lookup"><span data-stu-id="cc615-111">Example 2: Disable a rule</span></span>
```
PS C:\>Add-AzureRMMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup Default-Web-EastUS -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -TimeAggregationOperator Total 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
96c489f1-8529-46e1-a76d-2c1463ca3116                                                                                 OK
```

<span data-ttu-id="cc615-112">Questo comando Disabilita una regola.</span><span class="sxs-lookup"><span data-stu-id="cc615-112">This command disables a rule.</span></span>
<span data-ttu-id="cc615-113">Se la regola non esiste, la crea disabilitata.</span><span class="sxs-lookup"><span data-stu-id="cc615-113">If the rule does not exist, it creates it disabled.</span></span>
<span data-ttu-id="cc615-114">Se la regola esiste, viene semplicemente disabilitata.</span><span class="sxs-lookup"><span data-stu-id="cc615-114">If the rule exists, then it just disables it.</span></span>

### <span data-ttu-id="cc615-115">Esempio 3: aggiungere una regola con le azioni</span><span class="sxs-lookup"><span data-stu-id="cc615-115">Example 3: Add a rule with actions</span></span>
```
PS C:\>Add-AzureRmMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 1 -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -MetricName "Requests" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="cc615-116">Questo comando crea una regola di avviso metrica per un sito Web.</span><span class="sxs-lookup"><span data-stu-id="cc615-116">This command creates a metric alert rule for a website.</span></span>

## <span data-ttu-id="cc615-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cc615-117">PARAMETERS</span></span>

### <span data-ttu-id="cc615-118">-Azioni</span><span class="sxs-lookup"><span data-stu-id="cc615-118">-Actions</span></span>
<span data-ttu-id="cc615-119">Specifica un elenco di azioni delimitato da virgole.</span><span class="sxs-lookup"><span data-stu-id="cc615-119">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="cc615-120">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="cc615-120">-Description</span></span>
<span data-ttu-id="cc615-121">Specifica una descrizione della regola.</span><span class="sxs-lookup"><span data-stu-id="cc615-121">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="cc615-122">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="cc615-122">-DisableRule</span></span>
<span data-ttu-id="cc615-123">Disabilita la regola.</span><span class="sxs-lookup"><span data-stu-id="cc615-123">Disables the rule.</span></span>
<span data-ttu-id="cc615-124">Se non specifichi questo parametro, la regola è abilitata.</span><span class="sxs-lookup"><span data-stu-id="cc615-124">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="cc615-125">-Posizione</span><span class="sxs-lookup"><span data-stu-id="cc615-125">-Location</span></span>
<span data-ttu-id="cc615-126">Specifica la posizione in cui è definita la regola.</span><span class="sxs-lookup"><span data-stu-id="cc615-126">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="cc615-127">-Metricname</span><span class="sxs-lookup"><span data-stu-id="cc615-127">-MetricName</span></span>
<span data-ttu-id="cc615-128">Specifica il nome della metrica che la regola sta monitorando.</span><span class="sxs-lookup"><span data-stu-id="cc615-128">Specifies the name of the metric the rule is monitoring.</span></span>
<span data-ttu-id="cc615-129">Specifica questo parametro solo per le regole basate su metriche.</span><span class="sxs-lookup"><span data-stu-id="cc615-129">Specify this parameter only for metric-based rules.</span></span>

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

### <span data-ttu-id="cc615-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="cc615-130">-Name</span></span>
<span data-ttu-id="cc615-131">Specifica il nome della regola.</span><span class="sxs-lookup"><span data-stu-id="cc615-131">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="cc615-132">-Operator</span><span class="sxs-lookup"><span data-stu-id="cc615-132">-Operator</span></span>
<span data-ttu-id="cc615-133">Specifica l'operatore relazionale per la condizione della regola.</span><span class="sxs-lookup"><span data-stu-id="cc615-133">Specifies the relational operator for the condition of the rule.</span></span>
<span data-ttu-id="cc615-134">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="cc615-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cc615-135">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="cc615-135">GreaterThan</span></span>
- <span data-ttu-id="cc615-136">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="cc615-136">GreaterThanOrEqual</span></span>
-  <span data-ttu-id="cc615-137">LessThan</span><span class="sxs-lookup"><span data-stu-id="cc615-137">LessThan</span></span>
- <span data-ttu-id="cc615-138">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="cc615-138">LessThanOrEqual</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.ConditionOperator
Parameter Sets: (All)
Aliases: 
Accepted values: GreaterThan, GreaterThanOrEqual, LessThan, LessThanOrEqual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc615-139">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cc615-139">-ResourceGroup</span></span>
<span data-ttu-id="cc615-140">Specifica il nome del gruppo di risorse per la regola.</span><span class="sxs-lookup"><span data-stu-id="cc615-140">Specifies the name of the resource group for the rule.</span></span>

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

### <span data-ttu-id="cc615-141">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="cc615-141">-TargetResourceId</span></span>
<span data-ttu-id="cc615-142">Specifica l'ID della risorsa che la regola sta monitorando.</span><span class="sxs-lookup"><span data-stu-id="cc615-142">Specifies the ID of the resource the rule is monitoring.</span></span> <span data-ttu-id="cc615-143">Nota: non è possibile aggiornare questa proprietà per una regola di avviso esistente.</span><span class="sxs-lookup"><span data-stu-id="cc615-143">NOTE: This property cannot be updated for an existing alert rule.</span></span>

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

### <span data-ttu-id="cc615-144">-Soglia</span><span class="sxs-lookup"><span data-stu-id="cc615-144">-Threshold</span></span>
<span data-ttu-id="cc615-145">Specifica la soglia della regola.</span><span class="sxs-lookup"><span data-stu-id="cc615-145">Specifies the threshold of the rule.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc615-146">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="cc615-146">-TimeAggregationOperator</span></span>
<span data-ttu-id="cc615-147">Specifica l'operatore di aggregazione da applicare alla finestra temporale quando la regola viene valutata.</span><span class="sxs-lookup"><span data-stu-id="cc615-147">Specifies the aggregation operator to apply to the time window when the rule is being evaluated.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationOperator]
Parameter Sets: (All)
Aliases: 
Accepted values: Average, Minimum, Maximum, Total, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc615-148">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="cc615-148">-WindowSize</span></span>
<span data-ttu-id="cc615-149">Specifica le dimensioni della finestra temporale per la regola per calcolare i dati.</span><span class="sxs-lookup"><span data-stu-id="cc615-149">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="cc615-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc615-150">-DefaultProfile</span></span>
<span data-ttu-id="cc615-151">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cc615-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc615-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc615-152">CommonParameters</span></span>
<span data-ttu-id="cc615-153">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc615-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc615-154">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc615-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc615-155">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cc615-155">INPUTS</span></span>

## <span data-ttu-id="cc615-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cc615-156">OUTPUTS</span></span>

### <span data-ttu-id="cc615-157">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="cc615-157">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="cc615-158">Note</span><span class="sxs-lookup"><span data-stu-id="cc615-158">NOTES</span></span>

## <span data-ttu-id="cc615-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cc615-159">RELATED LINKS</span></span>

[<span data-ttu-id="cc615-160">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="cc615-160">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="cc615-161">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="cc615-161">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="cc615-162">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="cc615-162">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="cc615-163">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="cc615-163">Get-AzureRmAlertRule</span></span>](./Get-AzureRmAlertRule.md)

[<span data-ttu-id="cc615-164">New-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="cc615-164">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="cc615-165">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="cc615-165">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)

[<span data-ttu-id="cc615-166">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="cc615-166">Remove-AzureRmAlertRule</span></span>](./Remove-AzureRmAlertRule.md)


