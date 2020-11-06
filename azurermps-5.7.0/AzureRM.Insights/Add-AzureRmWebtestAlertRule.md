---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: FBAE5F75-1E28-4F1C-A9ED-20075FFD4AC7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermwebtestalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmWebtestAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmWebtestAlertRule.md
ms.openlocfilehash: da395b66cb4d63593c097f214701365370e06b75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514300"
---
# <span data-ttu-id="3ac48-101">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="3ac48-101">Add-AzureRmWebtestAlertRule</span></span>

## <span data-ttu-id="3ac48-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3ac48-102">SYNOPSIS</span></span>
<span data-ttu-id="3ac48-103">Aggiunge o aggiorna una regola di avviso di WebTest.</span><span class="sxs-lookup"><span data-stu-id="3ac48-103">Adds or updates a webtest alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ac48-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3ac48-104">SYNTAX</span></span>

```
Add-AzureRmWebtestAlertRule -MetricName <String> -TargetResourceUri <String> -WindowSize <TimeSpan>
 -FailedLocationCount <Int32> [-MetricNamespace <String>] -Location <String> [-Description <String>]
 [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ac48-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ac48-105">DESCRIPTION</span></span>
<span data-ttu-id="3ac48-106">Il cmdlet **Add-AzureRmWebtestAlertRule** aggiunge o aggiorna una regola di avviso di tipo Metric, Event o WebTest.</span><span class="sxs-lookup"><span data-stu-id="3ac48-106">The **Add-AzureRmWebtestAlertRule** cmdlet adds or updates an alert rule of either metric, event, or webtest type.</span></span>
<span data-ttu-id="3ac48-107">La regola aggiunta è associata a un gruppo di risorse e ha un nome.</span><span class="sxs-lookup"><span data-stu-id="3ac48-107">The added rule is associated to a resource group and has a name.</span></span>
<span data-ttu-id="3ac48-108">Questo cmdlet implementa il modello ShouldProcess, vale a dire che potrebbe richiedere conferma all'utente prima di creare, modificare o rimuovere la risorsa.</span><span class="sxs-lookup"><span data-stu-id="3ac48-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="3ac48-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3ac48-109">EXAMPLES</span></span>

### <span data-ttu-id="3ac48-110">Esempio 1: aggiungere una regola di avviso di WebTest</span><span class="sxs-lookup"><span data-stu-id="3ac48-110">Example 1: Add a webtest alert rule</span></span>
```
PS C:\>Add-AzureRmWebtestAlertRule -Name "webtestRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -WindowSize 00:05:00 -MetricName "metric" -TargetResourceUri ":/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourcegroups/Default-Web-WestUS/providers/microsoft.insights/webtests/leowebtestr1-webtestr1" -Description "Nice Webtest rule" -Failed 3
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="3ac48-111">Questo comando aggiunge o aggiorna una regola di avviso di WebTest.</span><span class="sxs-lookup"><span data-stu-id="3ac48-111">This command adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="3ac48-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3ac48-112">PARAMETERS</span></span>

### <span data-ttu-id="3ac48-113">-Azione</span><span class="sxs-lookup"><span data-stu-id="3ac48-113">-Action</span></span>
<span data-ttu-id="3ac48-114">Specifica un elenco di azioni delimitato da virgole.</span><span class="sxs-lookup"><span data-stu-id="3ac48-114">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="3ac48-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ac48-115">-DefaultProfile</span></span>
<span data-ttu-id="3ac48-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3ac48-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3ac48-117">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ac48-117">-Description</span></span>
<span data-ttu-id="3ac48-118">Specifica una descrizione della regola.</span><span class="sxs-lookup"><span data-stu-id="3ac48-118">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="3ac48-119">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="3ac48-119">-DisableRule</span></span>
<span data-ttu-id="3ac48-120">Disabilita la regola.</span><span class="sxs-lookup"><span data-stu-id="3ac48-120">Disables the rule.</span></span>
<span data-ttu-id="3ac48-121">Se non specifichi questo parametro, la regola è abilitata.</span><span class="sxs-lookup"><span data-stu-id="3ac48-121">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="3ac48-122">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="3ac48-122">-FailedLocationCount</span></span>
<span data-ttu-id="3ac48-123">Specifica il conteggio della posizione non riuscito per le regole di WebTest.</span><span class="sxs-lookup"><span data-stu-id="3ac48-123">Specifies the failed location count for the webtest rules.</span></span>
<span data-ttu-id="3ac48-124">Questa operazione è simile alla soglia degli altri tipi di regole.</span><span class="sxs-lookup"><span data-stu-id="3ac48-124">This is similar to the threshold in the other types of rules.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ac48-125">-Posizione</span><span class="sxs-lookup"><span data-stu-id="3ac48-125">-Location</span></span>
<span data-ttu-id="3ac48-126">Specifica la posizione in cui è definita la regola.</span><span class="sxs-lookup"><span data-stu-id="3ac48-126">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="3ac48-127">-Metricname</span><span class="sxs-lookup"><span data-stu-id="3ac48-127">-MetricName</span></span>
<span data-ttu-id="3ac48-128">Specifica il nome della metrica.</span><span class="sxs-lookup"><span data-stu-id="3ac48-128">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="3ac48-129">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="3ac48-129">-MetricNamespace</span></span>
<span data-ttu-id="3ac48-130">Specifica lo spazio dei nomi Metric per Rule.</span><span class="sxs-lookup"><span data-stu-id="3ac48-130">Specifies the metric namespace for rule.</span></span>

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

### <span data-ttu-id="3ac48-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="3ac48-131">-Name</span></span>
<span data-ttu-id="3ac48-132">Specifica il nome della regola.</span><span class="sxs-lookup"><span data-stu-id="3ac48-132">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="3ac48-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ac48-133">-ResourceGroupName</span></span>
<span data-ttu-id="3ac48-134">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3ac48-134">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="3ac48-135">-TargetResourceUri</span><span class="sxs-lookup"><span data-stu-id="3ac48-135">-TargetResourceUri</span></span>
<span data-ttu-id="3ac48-136">Specifica l'ID risorsa del WebTest.</span><span class="sxs-lookup"><span data-stu-id="3ac48-136">Specifies the resource ID of the webtest.</span></span>

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

### <span data-ttu-id="3ac48-137">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="3ac48-137">-WindowSize</span></span>
<span data-ttu-id="3ac48-138">Specifica le dimensioni della finestra temporale per la regola per calcolare i dati.</span><span class="sxs-lookup"><span data-stu-id="3ac48-138">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="3ac48-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ac48-139">CommonParameters</span></span>
<span data-ttu-id="3ac48-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ac48-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ac48-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ac48-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ac48-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3ac48-142">INPUTS</span></span>

### <span data-ttu-id="3ac48-143">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3ac48-143">None</span></span>
<span data-ttu-id="3ac48-144">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="3ac48-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3ac48-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3ac48-145">OUTPUTS</span></span>

### <span data-ttu-id="3ac48-146">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="3ac48-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="3ac48-147">Note</span><span class="sxs-lookup"><span data-stu-id="3ac48-147">NOTES</span></span>

## <span data-ttu-id="3ac48-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3ac48-148">RELATED LINKS</span></span>

[<span data-ttu-id="3ac48-149">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="3ac48-149">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="3ac48-150">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="3ac48-150">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="3ac48-151">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="3ac48-151">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="3ac48-152">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="3ac48-152">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


