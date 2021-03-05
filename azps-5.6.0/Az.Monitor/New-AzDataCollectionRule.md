---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDataCollectionRule.md
ms.openlocfilehash: b14d834e005f8a81666fd98b40d276825f04c0e8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984575"
---
# <span data-ttu-id="62cd7-101">New-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="62cd7-101">New-AzDataCollectionRule</span></span>

## <span data-ttu-id="62cd7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62cd7-102">SYNOPSIS</span></span>
<span data-ttu-id="62cd7-103">Creare una regola per la raccolta dei dati.</span><span class="sxs-lookup"><span data-stu-id="62cd7-103">Create a data collection rule.</span></span>

## <span data-ttu-id="62cd7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="62cd7-104">SYNTAX</span></span>

### <span data-ttu-id="62cd7-105">ByFile (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="62cd7-105">ByFile (Default)</span></span>
```
New-AzDataCollectionRule
   -Location <string>
   -ResourceGroupName <string>
   -RuleName <string>
   -RuleFile <string>
   [-Description <string>]
   [-Tag <hashtable>]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="62cd7-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="62cd7-106">DESCRIPTION</span></span>
<span data-ttu-id="62cd7-107">Il cmdlet **New-AzDataCollectionRule** crea una regola per la raccolta dei dati.</span><span class="sxs-lookup"><span data-stu-id="62cd7-107">The **New-AzDataCollectionRule** cmdlet creates a data collection rule.</span></span>

<span data-ttu-id="62cd7-108">Le regole di raccolta dei dati (DCR) definiscono i dati in arrivo in Azure Monitor e specificano dove devono essere inviati o archiviati i dati.</span><span class="sxs-lookup"><span data-stu-id="62cd7-108">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="62cd7-109">Ecco l'articolo [completo sulla panoramica di DCR.](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview)</span><span class="sxs-lookup"><span data-stu-id="62cd7-109">Here is the complete [DCR overview article](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

<span data-ttu-id="62cd7-110">Per usare il parametro -RuleFile, creare un file json contenente tre proprietà: dataSources, destinations, dataFlows (vedere esempio #1)</span><span class="sxs-lookup"><span data-stu-id="62cd7-110">To use the -RuleFile parameter, construct a json file containing three properties: dataSources, destinations, dataFlows (see Example #1)</span></span>

<span data-ttu-id="62cd7-111">I dettagli dello schema sono [qui.](https://docs.microsoft.com/rest/api/monitor/datacollectionrules/create)</span><span class="sxs-lookup"><span data-stu-id="62cd7-111">You may find here the [schema detail](https://docs.microsoft.com/rest/api/monitor/datacollectionrules/create).</span></span>

<span data-ttu-id="62cd7-112">È supportato anche l'output di un DCR serializzato con il cmdlet ConvertTo-Json (vedere l'esempio #2).</span><span class="sxs-lookup"><span data-stu-id="62cd7-112">The output of a DCR serialized with the cmdlet ConvertTo-Json is also supported (see Example #2).</span></span>

## <span data-ttu-id="62cd7-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="62cd7-113">EXAMPLES</span></span>

### <span data-ttu-id="62cd7-114">Esempio 1: Creare una regola di raccolta dati, JSON dall'API Rest</span><span class="sxs-lookup"><span data-stu-id="62cd7-114">Example 1: Create data collection rule, JSON from Rest API</span></span>
```powershell
PS C:\>New-AzDataCollectionRule -Location 'East US 2 EUAP' -ResourceGroupName 'testdcr'
                                -RuleName 'newDcrEx1' -RuleFile 'C:\samples\dcrEx1.json'
                                -Description 'Dcr description'
                                -Tag @{"tag1"="value1"; "tag2"="value2"}

Description       : Dcr description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcrEx1
Name              : newDcrEx1
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}

# Note: Content of C:\samples\dcrEx1.json
{
  "properties": {
    "dataSources": {
      "performanceCounters": [
        {
          "streams": [
            "Microsoft-InsightsMetrics"
          ],
          "scheduledTransferPeriod": "PT1M",
          "samplingFrequencyInSeconds": 10,
          "counterSpecifiers": [
            "\\Processor Information(_Total)\\% Processor Time"
          ],
          "name": "perfCounter01"
        }
      ]
    },
    "destinations": {
      "azureMonitorMetrics": {
        "name": "azureMonitorMetrics-default"
      }
    },
    "dataFlows": [
      {
        "streams": [
          "Microsoft-InsightsMetrics"
        ],
        "destinations": [
          "azureMonitorMetrics-default"
        ]
      }
    ]
  }
}
```

<span data-ttu-id="62cd7-115">Questo comando crea regole di raccolta dati per la sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="62cd7-115">This command creates a data collection rules for the current subscription.</span></span>

### <span data-ttu-id="62cd7-116">Esempio 2: Creare una regola per la raccolta dei dati, JSON da PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="62cd7-116">Example 2: Create data collection rule, JSON from PSDataCollectionRuleResource</span></span>
```powershell
PS C:\>New-AzDataCollectionRule -Location 'East US 2 EUAP' -ResourceGroupName 'testdcr'
                                -RuleName 'newDcrEx2' -RuleFile 'C:\samples\dcrEx2.json'
                                -Description 'Dcr description'
                                -Tag @{"tag1"="value1"; "tag2"="value2"}

Description       : Dcr description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcrEx2
Name              : newDcrEx2
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}

# Note: Content of C:\samples\dcrEx2.json
{
  "DataSources": {
    "PerformanceCounters": [
      {
        "Streams": [
          "Microsoft-InsightsMetrics"
        ],
        "ScheduledTransferPeriod": "PT1M",
        "SamplingFrequencyInSeconds": 10,
        "CounterSpecifiers": [
          "\\Processor Information(_Total)\\% Processor Time"
        ],
        "Name": "perfCounter01"
      }
    ]
  },
  "Destinations": {
    "AzureMonitorMetrics": {
      "Name": "azureMonitorMetrics-default"
    }
  },
  "DataFlows": [
    {
      "Streams": [
        "Microsoft-InsightsMetrics"
      ],
      "Destinations": [
        "azureMonitorMetrics-default"
      ]
    }
  ]
}
```

<span data-ttu-id="62cd7-117">Questo comando crea regole di raccolta dati per la sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="62cd7-117">This command creates a data collection rules for the current subscription.</span></span>

## <span data-ttu-id="62cd7-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62cd7-118">PARAMETERS</span></span>

### <span data-ttu-id="62cd7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62cd7-119">-DefaultProfile</span></span>
<span data-ttu-id="62cd7-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="62cd7-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62cd7-121">-Location</span><span class="sxs-lookup"><span data-stu-id="62cd7-121">-Location</span></span>
<span data-ttu-id="62cd7-122">Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="62cd7-122">The resource location</span></span>

```yaml
Type: System.String
Parameter Sets: ByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62cd7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62cd7-123">-ResourceGroupName</span></span>
<span data-ttu-id="62cd7-124">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="62cd7-124">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62cd7-125">-RuleName</span><span class="sxs-lookup"><span data-stu-id="62cd7-125">-RuleName</span></span>
<span data-ttu-id="62cd7-126">Nome della risorsa</span><span class="sxs-lookup"><span data-stu-id="62cd7-126">The resource name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFile
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62cd7-127">-RuleFile</span><span class="sxs-lookup"><span data-stu-id="62cd7-127">-RuleFile</span></span>
<span data-ttu-id="62cd7-128">Percorso del file JSON</span><span class="sxs-lookup"><span data-stu-id="62cd7-128">The JSON file path</span></span>

```yaml
Type: System.String
Parameter Sets: ByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62cd7-129">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="62cd7-129">-Description</span></span>
<span data-ttu-id="62cd7-130">Descrizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="62cd7-130">The resource description</span></span>

```yaml
Type: System.String
Parameter Sets: ByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62cd7-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="62cd7-131">-Tag</span></span>
<span data-ttu-id="62cd7-132">I tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="62cd7-132">The resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62cd7-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="62cd7-133">-Confirm</span></span>
<span data-ttu-id="62cd7-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62cd7-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62cd7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62cd7-135">-WhatIf</span></span>
<span data-ttu-id="62cd7-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="62cd7-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="62cd7-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="62cd7-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62cd7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62cd7-138">CommonParameters</span></span>
<span data-ttu-id="62cd7-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62cd7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62cd7-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="62cd7-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62cd7-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="62cd7-141">INPUTS</span></span>

### <span data-ttu-id="62cd7-142">System.String</span><span class="sxs-lookup"><span data-stu-id="62cd7-142">System.String</span></span>

## <span data-ttu-id="62cd7-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="62cd7-143">OUTPUTS</span></span>

### <span data-ttu-id="62cd7-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="62cd7-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="62cd7-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="62cd7-145">NOTES</span></span>

## <span data-ttu-id="62cd7-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="62cd7-146">RELATED LINKS</span></span>

<span data-ttu-id="62cd7-147">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md) 
 [Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md) 
 [Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
 [Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="62cd7-147">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)
[Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md)
[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span></span>