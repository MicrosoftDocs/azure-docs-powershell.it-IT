---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDataCollectionRule.md
ms.openlocfilehash: 864b3c8abe2411316edf155c49757c1082a863a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190087"
---
# <span data-ttu-id="941e0-101">Set-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="941e0-101">Set-AzDataCollectionRule</span></span>

## <span data-ttu-id="941e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="941e0-102">SYNOPSIS</span></span>
<span data-ttu-id="941e0-103">Aggiorna (sostituzione completa) una regola per la raccolta dei dati.</span><span class="sxs-lookup"><span data-stu-id="941e0-103">Updates (full replacement) a data collection rule.</span></span>

## <span data-ttu-id="941e0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="941e0-104">SYNTAX</span></span>

### <span data-ttu-id="941e0-105">ByName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="941e0-105">ByName (Default)</span></span>
```
Set-AzDataCollectionRule 
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

### <span data-ttu-id="941e0-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="941e0-106">ByResourceId</span></span>
```
Set-AzDataCollectionRule 
   -Location <string>
   -RuleId <string>
   -RuleFile <string>
   [-Description <string>]
   [-Tag <hashtable>]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

### <span data-ttu-id="941e0-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="941e0-107">ByInputObject</span></span>
```
Set-AzDataCollectionRule 
   -InputObject <PSDataCollectionRuleResource> 
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="941e0-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="941e0-108">DESCRIPTION</span></span>
<span data-ttu-id="941e0-109">Il **cmdlet Set-AzDataCollectionRule** sostituisce una regola di raccolta dati esistente.</span><span class="sxs-lookup"><span data-stu-id="941e0-109">The **Set-AzDataCollectionRule** cmdlet replaces an existing data collection rule.</span></span>

<span data-ttu-id="941e0-110">Le regole di raccolta dei dati (DCR) definiscono i dati in arrivo in Azure Monitor e specificano dove devono essere inviati o archiviati i dati.</span><span class="sxs-lookup"><span data-stu-id="941e0-110">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="941e0-111">Ecco l'articolo [completo sulla panoramica di DCR.](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview)</span><span class="sxs-lookup"><span data-stu-id="941e0-111">Here is the complete [DCR overview article](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

<span data-ttu-id="941e0-112">Per usare il parametro -RuleFile, creare un file json contenente tre proprietà: dataSources, destinations, dataFlows (vedere l'esempio #1).</span><span class="sxs-lookup"><span data-stu-id="941e0-112">To use the -RuleFile parameter, construct a json file containing three properties: dataSources, destinations, dataFlows (see Example #1).</span></span>

<span data-ttu-id="941e0-113">I dettagli dello schema sono [qui.](https://docs.microsoft.com/en-us/rest/api/monitor/datacollectionrules/create)</span><span class="sxs-lookup"><span data-stu-id="941e0-113">You may find here the [schema detail](https://docs.microsoft.com/en-us/rest/api/monitor/datacollectionrules/create).</span></span>

<span data-ttu-id="941e0-114">È supportato anche l'output di un DCR serializzato con il cmdlet ConvertTo-Json (esempio #2).</span><span class="sxs-lookup"><span data-stu-id="941e0-114">The output of a DCR serialized with the cmdlet ConvertTo-Json is also supported (Example #2).</span></span>

## <span data-ttu-id="941e0-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="941e0-115">EXAMPLES</span></span>

### <span data-ttu-id="941e0-116">Esempio 1: Aggiornare la regola di raccolta dati, JSON dall'API Rest</span><span class="sxs-lookup"><span data-stu-id="941e0-116">Example 1: Update data collection rule, JSON from Rest API</span></span>
```powershell
PS C:\>Set-AzDataCollectionRule -Location 'East US 2 EUAP'
                                -ResourceGroupName 'testdcr' 
                                -RuleName 'newDcr' 
                                -RuleFile 'C:\samples\dcr1.json'
                                -Description 'Updated Description'

Description       : Updated Description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcr
Name              : newDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}

# Note: Content of C:\samples\dcr1.json
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

<span data-ttu-id="941e0-117">Questo comando sostituisce le regole di raccolta dati esistenti per la sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="941e0-117">This command replaces an existing data collection rules for the current subscription.</span></span>

### <span data-ttu-id="941e0-118">Esempio 2: Aggiornare la regola di raccolta dati, JSON da PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="941e0-118">Example 2: Update data collection rule, JSON from PSDataCollectionRuleResource</span></span>
```powershell
PS C:\>Set-AzDataCollectionRule -Location 'East US 2 EUAP'
                                -RuleId '/subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcr' 
                                -RuleFile 'C:\samples\dcr2.json'
                                -Description 'Updated Description'

Description       : Updated Description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcr
Name              : newDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}

# Note: Content of C:\samples\dcr2.json
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

<span data-ttu-id="941e0-119">Questo comando sostituisce le regole di raccolta dati esistenti per la sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="941e0-119">This command replaces an existing data collection rules for the current subscription.</span></span>

### <span data-ttu-id="941e0-120">Esempio 3: Aggiornare la regola di raccolta dati dall'oggetto</span><span class="sxs-lookup"><span data-stu-id="941e0-120">Example 3: Update data collection rule from object</span></span>
```powershell
PS C:\>$dcr = Get-AzDataCollectionRule -ResourceGroupName "testdcr" -Name "newDcr"
PS C:\>$dcr.Description = 'This is a test'
PS C:\>$dcr | Set-AzDataCollectionRule

Description       : This is a test
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : {provState}
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcr
Name              : newDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}
```

## <span data-ttu-id="941e0-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="941e0-121">PARAMETERS</span></span>

### <span data-ttu-id="941e0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="941e0-122">-DefaultProfile</span></span>
<span data-ttu-id="941e0-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="941e0-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="941e0-124">-Location</span><span class="sxs-lookup"><span data-stu-id="941e0-124">-Location</span></span>
<span data-ttu-id="941e0-125">Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="941e0-125">The resource location</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="941e0-126">-RuleFile</span><span class="sxs-lookup"><span data-stu-id="941e0-126">-RuleFile</span></span>
<span data-ttu-id="941e0-127">Percorso del file JSON</span><span class="sxs-lookup"><span data-stu-id="941e0-127">The JSON file path</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="941e0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="941e0-128">-ResourceGroupName</span></span>
<span data-ttu-id="941e0-129">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="941e0-129">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="941e0-130">-RuleName</span><span class="sxs-lookup"><span data-stu-id="941e0-130">-RuleName</span></span>
<span data-ttu-id="941e0-131">Nome della risorsa</span><span class="sxs-lookup"><span data-stu-id="941e0-131">The resource name</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="941e0-132">-RuleId</span><span class="sxs-lookup"><span data-stu-id="941e0-132">-RuleId</span></span>
<span data-ttu-id="941e0-133">ID risorsa</span><span class="sxs-lookup"><span data-stu-id="941e0-133">The resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="941e0-134">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="941e0-134">-Description</span></span>
<span data-ttu-id="941e0-135">Descrizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="941e0-135">The resource description</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="941e0-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="941e0-136">-Tag</span></span>
<span data-ttu-id="941e0-137">I tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="941e0-137">The resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="941e0-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="941e0-138">-InputObject</span></span>
<span data-ttu-id="941e0-139">Oggetto PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="941e0-139">PSDataCollectionRuleResource Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### <span data-ttu-id="941e0-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="941e0-140">-Confirm</span></span>
<span data-ttu-id="941e0-141">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="941e0-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="941e0-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="941e0-142">-WhatIf</span></span>
<span data-ttu-id="941e0-143">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="941e0-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="941e0-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="941e0-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="941e0-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="941e0-145">CommonParameters</span></span>
<span data-ttu-id="941e0-146">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="941e0-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="941e0-147">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="941e0-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="941e0-148">INPUT</span><span class="sxs-lookup"><span data-stu-id="941e0-148">INPUTS</span></span>

### <span data-ttu-id="941e0-149">System.String</span><span class="sxs-lookup"><span data-stu-id="941e0-149">System.String</span></span>

## <span data-ttu-id="941e0-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="941e0-150">OUTPUTS</span></span>

### <span data-ttu-id="941e0-151">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="941e0-151">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="941e0-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="941e0-152">NOTES</span></span>

## <span data-ttu-id="941e0-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="941e0-153">RELATED LINKS</span></span>

<span data-ttu-id="941e0-154">[New-AzDataCollectionRule](./New-AzDataCollectionRule.md) 
 [Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md) 
 [Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
 [Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="941e0-154">[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)
[Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md)
[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span></span>