---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDataCollectionRule.md
ms.openlocfilehash: 8826dfdf8fe0152035319c576210088bcd5521e3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180191"
---
# <span data-ttu-id="4a517-101">Get-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="4a517-101">Get-AzDataCollectionRule</span></span>

## <span data-ttu-id="4a517-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a517-102">SYNOPSIS</span></span>
<span data-ttu-id="4a517-103">Recupera le regole per la raccolta dei dati.</span><span class="sxs-lookup"><span data-stu-id="4a517-103">Gets data collection rule(s).</span></span>

## <span data-ttu-id="4a517-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4a517-104">SYNTAX</span></span>

### <span data-ttu-id="4a517-105">BySubscription (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4a517-105">BySubscription (Default)</span></span>
```
Get-AzDataCollectionRule
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="4a517-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4a517-106">ByResourceGroup</span></span>
```
Get-AzDataCollectionRule
   -ResourceGroupName <string>
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="4a517-107">ByName</span><span class="sxs-lookup"><span data-stu-id="4a517-107">ByName</span></span>
```
Get-AzDataCollectionRule
   -ResourceGroupName <string>
   -RuleName <string>
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="4a517-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4a517-108">ByResourceId</span></span>
```
Get-AzDataCollectionRule
   -RuleId <string>
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

## <span data-ttu-id="4a517-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4a517-109">DESCRIPTION</span></span>
<span data-ttu-id="4a517-110">Il **cmdlet Get-AzDataCollectionRule** ottiene una o più regole di raccolta dati.</span><span class="sxs-lookup"><span data-stu-id="4a517-110">The **Get-AzDataCollectionRule** cmdlet gets one or more data collection rules.</span></span>

<span data-ttu-id="4a517-111">Le regole di raccolta dei dati (DCR) definiscono i dati in arrivo in Azure Monitor e specificano dove devono essere inviati o archiviati i dati.</span><span class="sxs-lookup"><span data-stu-id="4a517-111">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="4a517-112">Ecco l'articolo [completo sulla panoramica di DCR.](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview)</span><span class="sxs-lookup"><span data-stu-id="4a517-112">Here is the complete [DCR overview article](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

## <span data-ttu-id="4a517-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4a517-113">EXAMPLES</span></span>

### <span data-ttu-id="4a517-114">Esempio 1: Ottenere regole di raccolta dati in base all'ID sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="4a517-114">Example 1: Get data collection rules by subscription ID</span></span>
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

<span data-ttu-id="4a517-115">Questo comando elenca tutte le regole di raccolta dati per la sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="4a517-115">This command lists all the data collection rules for the current subscription.</span></span>

### <span data-ttu-id="4a517-116">Esempio 2: Ottenere regole di raccolta dati per il gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="4a517-116">Example 2: Get data collection rules for the given resource group</span></span>
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

<span data-ttu-id="4a517-117">Questo comando elenca le regole di raccolta dati per il gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="4a517-117">This command lists data collection rules for the given resource group.</span></span>

### <span data-ttu-id="4a517-118">Esempio 3: Ottenere una regola per la raccolta dei dati</span><span class="sxs-lookup"><span data-stu-id="4a517-118">Example 3: Get a data collection rule</span></span>
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

<span data-ttu-id="4a517-119">Questo comando elenca una regola per la raccolta dati (un elenco con un singolo elemento).</span><span class="sxs-lookup"><span data-stu-id="4a517-119">This command lists one (a list with a single element) data collection rule.</span></span>

### <span data-ttu-id="4a517-120">Esempio 4: Ottenere una regola di raccolta dati in base all'ID regola</span><span class="sxs-lookup"><span data-stu-id="4a517-120">Example 4: Get a data collection rule by Rule ID</span></span>
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

<span data-ttu-id="4a517-121">Questo comando elenca una regola per la raccolta dati (un elenco con un singolo elemento).</span><span class="sxs-lookup"><span data-stu-id="4a517-121">This command lists one (a list with a single element) data collection rule.</span></span>

## <span data-ttu-id="4a517-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a517-122">PARAMETERS</span></span>

### <span data-ttu-id="4a517-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a517-123">-DefaultProfile</span></span>
<span data-ttu-id="4a517-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="4a517-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a517-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a517-125">-ResourceGroupName</span></span>
<span data-ttu-id="4a517-126">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="4a517-126">The resource group name</span></span>

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

### <span data-ttu-id="4a517-127">-RuleName</span><span class="sxs-lookup"><span data-stu-id="4a517-127">-RuleName</span></span>
<span data-ttu-id="4a517-128">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="4a517-128">The name of the resource.</span></span>

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

### <span data-ttu-id="4a517-129">-RuleId</span><span class="sxs-lookup"><span data-stu-id="4a517-129">-RuleId</span></span>
<span data-ttu-id="4a517-130">ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="4a517-130">The ID of the resource.</span></span>

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

### <span data-ttu-id="4a517-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a517-131">CommonParameters</span></span>
<span data-ttu-id="4a517-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a517-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a517-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4a517-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a517-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="4a517-134">INPUTS</span></span>

### <span data-ttu-id="4a517-135">System.String</span><span class="sxs-lookup"><span data-stu-id="4a517-135">System.String</span></span>

## <span data-ttu-id="4a517-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4a517-136">OUTPUTS</span></span>

### <span data-ttu-id="4a517-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="4a517-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="4a517-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="4a517-138">NOTES</span></span>

## <span data-ttu-id="4a517-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4a517-139">RELATED LINKS</span></span>

<span data-ttu-id="4a517-140">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md) 
 [Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md) 
 [New-AzDataCollectionRule](./New-AzDataCollectionRule.md) 
 [Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="4a517-140">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)
[Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md)
[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)
[Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span></span>
