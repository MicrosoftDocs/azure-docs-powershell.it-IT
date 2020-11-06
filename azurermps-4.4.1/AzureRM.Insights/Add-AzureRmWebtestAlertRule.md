---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: FBAE5F75-1E28-4F1C-A9ED-20075FFD4AC7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmWebtestAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmWebtestAlertRule.md
ms.openlocfilehash: 52b3d39aef4c117fe8b26bb35f1bf50143e5fec5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521637"
---
# <span data-ttu-id="2adf2-101">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="2adf2-101">Add-AzureRmWebtestAlertRule</span></span>

## <span data-ttu-id="2adf2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2adf2-102">SYNOPSIS</span></span>
<span data-ttu-id="2adf2-103">Aggiunge o aggiorna una regola di avviso di WebTest.</span><span class="sxs-lookup"><span data-stu-id="2adf2-103">Adds or updates a webtest alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2adf2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2adf2-104">SYNTAX</span></span>

```
Add-AzureRmWebtestAlertRule -MetricName <String> -TargetResourceUri <String> -WindowSize <TimeSpan>
 -FailedLocationCount <Int32> [-MetricNamespace <String>] -Location <String> [-Description <String>]
 [-DisableRule] -ResourceGroup <String> -Name <String>
 [-Actions <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2adf2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2adf2-105">DESCRIPTION</span></span>
<span data-ttu-id="2adf2-106">Il cmdlet **Add-AzureRmWebtestAlertRule** aggiunge o aggiorna una regola di avviso di tipo Metric, Event o WebTest.</span><span class="sxs-lookup"><span data-stu-id="2adf2-106">The **Add-AzureRmWebtestAlertRule** cmdlet adds or updates an alert rule of either metric, event, or webtest type.</span></span>
<span data-ttu-id="2adf2-107">La regola aggiunta è associata a un gruppo di risorse e ha un nome.</span><span class="sxs-lookup"><span data-stu-id="2adf2-107">The added rule is associated to a resource group and has a name.</span></span>

## <span data-ttu-id="2adf2-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2adf2-108">EXAMPLES</span></span>

### <span data-ttu-id="2adf2-109">Esempio 1: aggiungere una regola di avviso di WebTest</span><span class="sxs-lookup"><span data-stu-id="2adf2-109">Example 1: Add a webtest alert rule</span></span>
```
PS C:\>Add-AzureRmWebtestAlertRule -Name "webtestRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -WindowSize 00:05:00 -MetricName "metric" -TargetResourceUri ":/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourcegroups/Default-Web-WestUS/providers/microsoft.insights/webtests/leowebtestr1-webtestr1" -Description "Nice Webtest rule" -Failed 3
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="2adf2-110">Questo comando aggiunge o aggiorna una regola di avviso di WebTest.</span><span class="sxs-lookup"><span data-stu-id="2adf2-110">This command adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="2adf2-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2adf2-111">PARAMETERS</span></span>

### <span data-ttu-id="2adf2-112">-Azioni</span><span class="sxs-lookup"><span data-stu-id="2adf2-112">-Actions</span></span>
<span data-ttu-id="2adf2-113">Specifica un elenco di azioni delimitato da virgole.</span><span class="sxs-lookup"><span data-stu-id="2adf2-113">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="2adf2-114">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="2adf2-114">-Description</span></span>
<span data-ttu-id="2adf2-115">Specifica una descrizione della regola.</span><span class="sxs-lookup"><span data-stu-id="2adf2-115">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="2adf2-116">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="2adf2-116">-DisableRule</span></span>
<span data-ttu-id="2adf2-117">Disabilita la regola.</span><span class="sxs-lookup"><span data-stu-id="2adf2-117">Disables the rule.</span></span>
<span data-ttu-id="2adf2-118">Se non specifichi questo parametro, la regola è abilitata.</span><span class="sxs-lookup"><span data-stu-id="2adf2-118">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="2adf2-119">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="2adf2-119">-FailedLocationCount</span></span>
<span data-ttu-id="2adf2-120">Specifica il conteggio della posizione non riuscito per le regole di WebTest.</span><span class="sxs-lookup"><span data-stu-id="2adf2-120">Specifies the failed location count for the webtest rules.</span></span>
<span data-ttu-id="2adf2-121">Questa operazione è simile alla soglia degli altri tipi di regole.</span><span class="sxs-lookup"><span data-stu-id="2adf2-121">This is similar to the threshold in the other types of rules.</span></span>

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

### <span data-ttu-id="2adf2-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="2adf2-122">-Location</span></span>
<span data-ttu-id="2adf2-123">Specifica la posizione in cui è definita la regola.</span><span class="sxs-lookup"><span data-stu-id="2adf2-123">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="2adf2-124">-Metricname</span><span class="sxs-lookup"><span data-stu-id="2adf2-124">-MetricName</span></span>
<span data-ttu-id="2adf2-125">Specifica il nome della metrica.</span><span class="sxs-lookup"><span data-stu-id="2adf2-125">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="2adf2-126">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="2adf2-126">-MetricNamespace</span></span>
<span data-ttu-id="2adf2-127">Specifica lo spazio dei nomi Metric per Rule.</span><span class="sxs-lookup"><span data-stu-id="2adf2-127">Specifies the metric namespace for rule.</span></span>

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

### <span data-ttu-id="2adf2-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="2adf2-128">-Name</span></span>
<span data-ttu-id="2adf2-129">Specifica il nome della regola.</span><span class="sxs-lookup"><span data-stu-id="2adf2-129">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="2adf2-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2adf2-130">-ResourceGroup</span></span>
<span data-ttu-id="2adf2-131">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2adf2-131">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="2adf2-132">-TargetResourceUri</span><span class="sxs-lookup"><span data-stu-id="2adf2-132">-TargetResourceUri</span></span>
<span data-ttu-id="2adf2-133">Specifica l'ID risorsa del WebTest.</span><span class="sxs-lookup"><span data-stu-id="2adf2-133">Specifies the resource ID of the webtest.</span></span>

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

### <span data-ttu-id="2adf2-134">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="2adf2-134">-WindowSize</span></span>
<span data-ttu-id="2adf2-135">Specifica le dimensioni della finestra temporale per la regola per calcolare i dati.</span><span class="sxs-lookup"><span data-stu-id="2adf2-135">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="2adf2-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2adf2-136">-DefaultProfile</span></span>
<span data-ttu-id="2adf2-137">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2adf2-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2adf2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2adf2-138">CommonParameters</span></span>
<span data-ttu-id="2adf2-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2adf2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2adf2-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2adf2-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2adf2-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2adf2-141">INPUTS</span></span>

## <span data-ttu-id="2adf2-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2adf2-142">OUTPUTS</span></span>

### <span data-ttu-id="2adf2-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="2adf2-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="2adf2-144">Note</span><span class="sxs-lookup"><span data-stu-id="2adf2-144">NOTES</span></span>

## <span data-ttu-id="2adf2-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2adf2-145">RELATED LINKS</span></span>

[<span data-ttu-id="2adf2-146">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="2adf2-146">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="2adf2-147">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="2adf2-147">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="2adf2-148">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="2adf2-148">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="2adf2-149">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="2adf2-149">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


