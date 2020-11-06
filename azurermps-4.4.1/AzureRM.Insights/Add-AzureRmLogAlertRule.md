---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 11A521DF-E77C-4D6F-A2D9-1C2CF8972F57
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogAlertRule.md
ms.openlocfilehash: 38644018ac9ae19d1c413123ca071f564d336fa7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521642"
---
# <span data-ttu-id="529cf-101">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="529cf-101">Add-AzureRmLogAlertRule</span></span>

## <span data-ttu-id="529cf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="529cf-102">SYNOPSIS</span></span>
<span data-ttu-id="529cf-103">Aggiunge o sostituisce una regola di avviso del log.</span><span class="sxs-lookup"><span data-stu-id="529cf-103">Adds or replaces a log alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="529cf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="529cf-104">SYNTAX</span></span>

```
Add-AzureRmLogAlertRule [-TargetResourceGroup <String>] [-TargetResourceId <String>] [-Level <String>]
 -OperationName <String> [-TargetResourceProvider <String>] [-Status <String>] [-SubStatus <String>]
 -Location <String> [-Description <String>] [-DisableRule] -ResourceGroup <String> -Name <String>
 [-Actions <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="529cf-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="529cf-105">DESCRIPTION</span></span>
<span data-ttu-id="529cf-106">Il cmdlet **Add-AzureRmLogAlertRule** aggiunge o sostituisce una regola di avviso per gli eventi.</span><span class="sxs-lookup"><span data-stu-id="529cf-106">The **Add-AzureRmLogAlertRule** cmdlet adds or replaces an event alert rule.</span></span>
<span data-ttu-id="529cf-107">La regola aggiunta è associata a un gruppo di risorse e ha un nome.</span><span class="sxs-lookup"><span data-stu-id="529cf-107">The added rule is associated with a resource group and has a name.</span></span>

<span data-ttu-id="529cf-108">Come annunciato nelle versioni precedenti: **il cmdlet Add-AzureRMLogAlertRule sarà deprecato in una versione futura.**</span><span class="sxs-lookup"><span data-stu-id="529cf-108">As announced in previous releases: **Add-AzureRMLogAlertRule cmdlet will be deprecated in a future release.**</span></span> <span data-ttu-id="529cf-109">Dopo il 1 ° ottobre 2017 l'uso di questo cmdlet non avrà più alcun effetto poiché questa funzionalità viene trasformata in avvisi del log attività.</span><span class="sxs-lookup"><span data-stu-id="529cf-109">After October 1st 2017 using this cmdlet will no longer have any effect as this functionality is being transitioned to Activity Log Alerts.</span></span> <span data-ttu-id="529cf-110">**_https://aka.ms/migratemealerts_** Per altre informazioni, vedere.</span><span class="sxs-lookup"><span data-stu-id="529cf-110">Please see **_https://aka.ms/migratemealerts_** for more information.</span></span>

## <span data-ttu-id="529cf-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="529cf-111">EXAMPLES</span></span>

### <span data-ttu-id="529cf-112">Esempio 1: aggiungere una regola di avviso del log</span><span class="sxs-lookup"><span data-stu-id="529cf-112">Example 1: Add a log alert rule</span></span>
```
PS C:\>Add-AzureRmLogAlertRule -Name "logRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -OperationName "Create" -TargetResourceId "/subscriptions/abbfb07c-6c93-40be-bc9b-4f0deba32f4c/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/misitiooeltuyo" -Description "My log rule"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="529cf-113">Questo comando aggiunge o aggiorna una regola di avviso basata su eventi.</span><span class="sxs-lookup"><span data-stu-id="529cf-113">This command adds or updates an event-based alert rule.</span></span>

## <span data-ttu-id="529cf-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="529cf-114">PARAMETERS</span></span>

### <span data-ttu-id="529cf-115">-Azioni</span><span class="sxs-lookup"><span data-stu-id="529cf-115">-Actions</span></span>
<span data-ttu-id="529cf-116">Specifica un elenco di azioni delimitato da virgole.</span><span class="sxs-lookup"><span data-stu-id="529cf-116">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="529cf-117">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="529cf-117">-Description</span></span>
<span data-ttu-id="529cf-118">Specifica una descrizione della regola.</span><span class="sxs-lookup"><span data-stu-id="529cf-118">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="529cf-119">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="529cf-119">-DisableRule</span></span>
<span data-ttu-id="529cf-120">Disabilita una regola.</span><span class="sxs-lookup"><span data-stu-id="529cf-120">Disables a rule.</span></span>
<span data-ttu-id="529cf-121">Se non specifichi questo parametro, la regola è abilitata.</span><span class="sxs-lookup"><span data-stu-id="529cf-121">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="529cf-122">-Livello</span><span class="sxs-lookup"><span data-stu-id="529cf-122">-Level</span></span>
<span data-ttu-id="529cf-123">Specifica il livello dell'evento che la regola sta monitorando.</span><span class="sxs-lookup"><span data-stu-id="529cf-123">Specifies the level of the event the rule is monitoring.</span></span>
<span data-ttu-id="529cf-124">Specifica questo parametro solo per le regole basate su eventi.</span><span class="sxs-lookup"><span data-stu-id="529cf-124">Specify this parameter only for event-based rules.</span></span>

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

### <span data-ttu-id="529cf-125">-Posizione</span><span class="sxs-lookup"><span data-stu-id="529cf-125">-Location</span></span>
<span data-ttu-id="529cf-126">Specifica il percorso della regola.</span><span class="sxs-lookup"><span data-stu-id="529cf-126">Specifies the location for the rule.</span></span>

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

### <span data-ttu-id="529cf-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="529cf-127">-Name</span></span>
<span data-ttu-id="529cf-128">Specifica il nome della regola.</span><span class="sxs-lookup"><span data-stu-id="529cf-128">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="529cf-129">-OperationName</span><span class="sxs-lookup"><span data-stu-id="529cf-129">-OperationName</span></span>
<span data-ttu-id="529cf-130">Specifica il nome dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="529cf-130">Specifies the name of the operation.</span></span>

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

### <span data-ttu-id="529cf-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="529cf-131">-ResourceGroup</span></span>
<span data-ttu-id="529cf-132">Specifica il nome del gruppo di risorse per la regola.</span><span class="sxs-lookup"><span data-stu-id="529cf-132">Specifies the name of the resource group for the rule.</span></span>

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

### <span data-ttu-id="529cf-133">-Stato</span><span class="sxs-lookup"><span data-stu-id="529cf-133">-Status</span></span>
<span data-ttu-id="529cf-134">Specifica lo stato.</span><span class="sxs-lookup"><span data-stu-id="529cf-134">Specifies the status.</span></span>

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

### <span data-ttu-id="529cf-135">-Stato secondario</span><span class="sxs-lookup"><span data-stu-id="529cf-135">-SubStatus</span></span>
<span data-ttu-id="529cf-136">Specifica lo stato secondario.</span><span class="sxs-lookup"><span data-stu-id="529cf-136">Specifies the substatus.</span></span>

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

### <span data-ttu-id="529cf-137">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="529cf-137">-TargetResourceGroup</span></span>
<span data-ttu-id="529cf-138">Specifica il gruppo di risorse della risorsa che la regola sta monitorando.</span><span class="sxs-lookup"><span data-stu-id="529cf-138">Specifies the resource group of the resource the rule is monitoring.</span></span>

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

### <span data-ttu-id="529cf-139">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="529cf-139">-TargetResourceId</span></span>
<span data-ttu-id="529cf-140">Specifica l'ID della risorsa che la regola sta monitorando.</span><span class="sxs-lookup"><span data-stu-id="529cf-140">Specifies the ID of the resource the rule is monitoring.</span></span>

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

### <span data-ttu-id="529cf-141">-TargetResourceProvider</span><span class="sxs-lookup"><span data-stu-id="529cf-141">-TargetResourceProvider</span></span>
<span data-ttu-id="529cf-142">Specifica il provider di risorse della risorsa che la regola sta monitorando.</span><span class="sxs-lookup"><span data-stu-id="529cf-142">Specifies the resource provider of the resource the rule is monitoring.</span></span>

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

### <span data-ttu-id="529cf-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="529cf-143">-DefaultProfile</span></span>
<span data-ttu-id="529cf-144">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="529cf-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="529cf-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="529cf-145">CommonParameters</span></span>
<span data-ttu-id="529cf-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="529cf-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="529cf-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="529cf-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="529cf-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="529cf-148">INPUTS</span></span>

## <span data-ttu-id="529cf-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="529cf-149">OUTPUTS</span></span>

### <span data-ttu-id="529cf-150">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="529cf-150">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="529cf-151">Note</span><span class="sxs-lookup"><span data-stu-id="529cf-151">NOTES</span></span>

## <span data-ttu-id="529cf-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="529cf-152">RELATED LINKS</span></span>

[<span data-ttu-id="529cf-153">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="529cf-153">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="529cf-154">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="529cf-154">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="529cf-155">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="529cf-155">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="529cf-156">New-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="529cf-156">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="529cf-157">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="529cf-157">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


