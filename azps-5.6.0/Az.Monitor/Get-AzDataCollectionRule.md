---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDataCollectionRule.md
ms.openlocfilehash: 6c1ea4cd7abbf50fb00a5f7fe1b04b7112b8f6c2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980093"
---
# <span data-ttu-id="74aee-101">Get-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="74aee-101">Get-AzDataCollectionRule</span></span>

## <span data-ttu-id="74aee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74aee-102">SYNOPSIS</span></span>
<span data-ttu-id="74aee-103">Recupera le regole per la raccolta dei dati.</span><span class="sxs-lookup"><span data-stu-id="74aee-103">Gets data collection rule(s).</span></span>

## <span data-ttu-id="74aee-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="74aee-104">SYNTAX</span></span>

### <span data-ttu-id="74aee-105">BySubscription (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="74aee-105">BySubscription (Default)</span></span>
```
Get-AzDataCollectionRule
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="74aee-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="74aee-106">ByResourceGroup</span></span>
```
Get-AzDataCollectionRule
   -ResourceGroupName <string>
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="74aee-107">ByName</span><span class="sxs-lookup"><span data-stu-id="74aee-107">ByName</span></span>
```
Get-AzDataCollectionRule
   -ResourceGroupName <string>
   -RuleName <string>
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="74aee-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="74aee-108">ByResourceId</span></span>
```
Get-AzDataCollectionRule
   -RuleId <string>
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

## <span data-ttu-id="74aee-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="74aee-109">DESCRIPTION</span></span>
<span data-ttu-id="74aee-110">Il **cmdlet Get-AzDataCollectionRule** ottiene una o più regole di raccolta dei dati.</span><span class="sxs-lookup"><span data-stu-id="74aee-110">The **Get-AzDataCollectionRule** cmdlet gets one or more data collection rules.</span></span>

<span data-ttu-id="74aee-111">Le regole di raccolta dei dati (DCR) definiscono i dati in arrivo in Azure Monitor e specificano dove devono essere inviati o archiviati i dati.</span><span class="sxs-lookup"><span data-stu-id="74aee-111">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="74aee-112">Ecco l'articolo [completo sulla panoramica di DCR.](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview)</span><span class="sxs-lookup"><span data-stu-id="74aee-112">Here is the complete [DCR overview article](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

## <span data-ttu-id="74aee-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="74aee-113">EXAMPLES</span></span>

### <span data-ttu-id="74aee-114">Esempio 1: Ottenere regole di raccolta dati in base all'ID sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="74aee-114">Example 1: Get data collection rules by subscription ID</span></span>
```
PS C:\>Get-AzDataCollectionRule

Description       : DCR description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testgroup/providers/Microsoft.Insights/dataCollectionRules/testDcr
Name              : testDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}
```

<span data-ttu-id="74aee-115">Questo comando elenca tutte le regole di raccolta dati per la sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="74aee-115">This command lists all the data collection rules for the current subscription.</span></span>

### <span data-ttu-id="74aee-116">Esempio 2: Ottenere regole di raccolta dati per il gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="74aee-116">Example 2: Get data collection rules for the given resource group</span></span>
```
PS C:\>Get-AzDataCollectionRule -ResourceGroup "testgroup"

Description       : DCR description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testgroup/providers/Microsoft.Insights/dataCollectionRules/testDcr
Name              : testDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}
```

<span data-ttu-id="74aee-117">Questo comando elenca le regole di raccolta dati per il gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="74aee-117">This command lists data collection rules for the given resource group.</span></span>

### <span data-ttu-id="74aee-118">Esempio 3: Ottenere una regola per la raccolta dei dati</span><span class="sxs-lookup"><span data-stu-id="74aee-118">Example 3: Get a data collection rule</span></span>
```
PS C:\>Get-AzDataCollectionRule -ResourceGroup "testgroup" -RuleName "testDcr"

Description       : DCR description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testgroup/providers/Microsoft.Insights/dataCollectionRules/testDcr
Name              : testDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}
```

<span data-ttu-id="74aee-119">Questo comando elenca una regola per la raccolta dati (un elenco con un singolo elemento).</span><span class="sxs-lookup"><span data-stu-id="74aee-119">This command lists one (a list with a single element) data collection rule.</span></span>

### <span data-ttu-id="74aee-120">Esempio 4: Ottenere una regola di raccolta dati per ID regola</span><span class="sxs-lookup"><span data-stu-id="74aee-120">Example 4: Get a data collection rule by Rule ID</span></span>
```
PS C:\>Get-AzDataCollectionRule -RuleId "/subscriptions/{subId}/resourceGroups/testgroup/providers/Microsoft.Insights/dataCollectionRules/testDcr"

Description       : DCR description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testgroup/providers/Microsoft.Insights/dataCollectionRules/testDcr
Name              : testDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}
```

<span data-ttu-id="74aee-121">Questo comando elenca una regola per la raccolta dati (un elenco con un singolo elemento).</span><span class="sxs-lookup"><span data-stu-id="74aee-121">This command lists one (a list with a single element) data collection rule.</span></span>

## <span data-ttu-id="74aee-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74aee-122">PARAMETERS</span></span>

### <span data-ttu-id="74aee-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74aee-123">-DefaultProfile</span></span>
<span data-ttu-id="74aee-124">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="74aee-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="74aee-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74aee-125">-ResourceGroupName</span></span>
<span data-ttu-id="74aee-126">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="74aee-126">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74aee-127">-RuleName</span><span class="sxs-lookup"><span data-stu-id="74aee-127">-RuleName</span></span>
<span data-ttu-id="74aee-128">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="74aee-128">The name of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74aee-129">-RuleId</span><span class="sxs-lookup"><span data-stu-id="74aee-129">-RuleId</span></span>
<span data-ttu-id="74aee-130">ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="74aee-130">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74aee-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74aee-131">CommonParameters</span></span>
<span data-ttu-id="74aee-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74aee-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74aee-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="74aee-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74aee-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="74aee-134">INPUTS</span></span>

### <span data-ttu-id="74aee-135">System.String</span><span class="sxs-lookup"><span data-stu-id="74aee-135">System.String</span></span>

## <span data-ttu-id="74aee-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="74aee-136">OUTPUTS</span></span>

### <span data-ttu-id="74aee-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="74aee-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="74aee-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="74aee-138">NOTES</span></span>

## <span data-ttu-id="74aee-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="74aee-139">RELATED LINKS</span></span>

<span data-ttu-id="74aee-140">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md) 
 [Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md) 
 [New-AzDataCollectionRule](./New-AzDataCollectionRule.md) 
 [Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="74aee-140">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)
[Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md)
[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)
[Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span></span>
