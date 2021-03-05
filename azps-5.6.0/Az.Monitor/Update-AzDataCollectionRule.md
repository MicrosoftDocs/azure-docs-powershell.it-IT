---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/update-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzDataCollectionRule.md
ms.openlocfilehash: 2e4aba9a2572b5612070d860dcbe20cda2366a02
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994124"
---
# <span data-ttu-id="9ae31-101">Update-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="9ae31-101">Update-AzDataCollectionRule</span></span>

## <span data-ttu-id="9ae31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ae31-102">SYNOPSIS</span></span>
<span data-ttu-id="9ae31-103">Aggiorna una proprietà dei tag delle regole per la raccolta dei dati.</span><span class="sxs-lookup"><span data-stu-id="9ae31-103">Updates a data collection rule tags property.</span></span>

## <span data-ttu-id="9ae31-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9ae31-104">SYNTAX</span></span>

### <span data-ttu-id="9ae31-105">ByName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9ae31-105">ByName (Default)</span></span>
```
Update-AzDataCollectionRule 
      -ResourceGroupName <string> 
      -RuleName <string> 
      [-Tag <hashtable>] 
      [-DefaultProfile <IAzureContextContainer>] 
      [-WhatIf] 
      [-Confirm]
      [<CommonParameters>]
```

### <span data-ttu-id="9ae31-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9ae31-106">ByResourceId</span></span>
```
Update-AzDataCollectionRule 
      -RuleId <string> 
      [-Tag <hashtable>] 
      [-DefaultProfile <IAzureContextContainer>] 
      [-WhatIf] 
      [-Confirm]
      [<CommonParameters>]
```

### <span data-ttu-id="9ae31-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9ae31-107">ByInputObject</span></span>
```
Update-AzDataCollectionRule 
      -InputObject <PSDataCollectionRuleResource> 
      [-Tag <hashtable>] 
      [-DefaultProfile <IAzureContextContainer>]
      [-WhatIf]
      [-Confirm]
      [<CommonParameters>]
```

## <span data-ttu-id="9ae31-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9ae31-108">DESCRIPTION</span></span>
<span data-ttu-id="9ae31-109">Il cmdlet **Update-AzDataCollectionRule** aggiorna una proprietà Tag delle regole per la raccolta dei dati.</span><span class="sxs-lookup"><span data-stu-id="9ae31-109">The **Update-AzDataCollectionRule** cmdlet updates a data collection rule Tags property.</span></span>

<span data-ttu-id="9ae31-110">Le regole di raccolta dei dati (DCR) definiscono i dati in arrivo in Azure Monitor e specificano dove devono essere inviati o archiviati i dati.</span><span class="sxs-lookup"><span data-stu-id="9ae31-110">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="9ae31-111">Ecco l'articolo [completo sulla panoramica di DCR.](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview)</span><span class="sxs-lookup"><span data-stu-id="9ae31-111">Here is the complete [DCR overview article](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

## <span data-ttu-id="9ae31-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9ae31-112">EXAMPLES</span></span>

### <span data-ttu-id="9ae31-113">Esempio 1: Aggiornare i tag delle regole per la raccolta dei dati</span><span class="sxs-lookup"><span data-stu-id="9ae31-113">Example 1: Update data collection rule tags</span></span>
```
PS C:\>Update-AzDataCollectionRule -RuleName 'newDcr'
                                   -ResourceGroupName 'testdcr'
                                   -Tag @{"tag1"="value1"; "tag2"="value2"}

Description       : 
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
```

<span data-ttu-id="9ae31-114">Questo comando aggiorna la proprietà tag per la regola di raccolta dati specificata.</span><span class="sxs-lookup"><span data-stu-id="9ae31-114">This command updates the tags property for the given data collection rule.</span></span>

### <span data-ttu-id="9ae31-115">Esempio 2: Aggiornare i tag delle regole per la raccolta dei dati</span><span class="sxs-lookup"><span data-stu-id="9ae31-115">Example 2: Update data collection rule tags</span></span>
```
PS C:\>Update-AzDataCollectionRule -RuleId '/subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcr'
                                   -Tag @{"tag1"="value1"; "tag2"="value2"}

Description       : 
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
```

<span data-ttu-id="9ae31-116">Questo comando aggiorna la proprietà tag per la regola di raccolta dati specificata.</span><span class="sxs-lookup"><span data-stu-id="9ae31-116">This command updates the tags property for the given data collection rule.</span></span>

### <span data-ttu-id="9ae31-117">Esempio 3: Aggiornare i tag delle regole per la raccolta dei dati</span><span class="sxs-lookup"><span data-stu-id="9ae31-117">Example 3: Update data collection rule tags</span></span>
```
PS C:\>$dcr = Get-AzDataCollectionRule -ResourceGroupName "testdcr" -Name "newDcr"
PS C:\>$dcr | Update-AzDataCollectionRule -Tag @{"tag1"="value1"; "tag2"="value2"}

Description       : 
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

<span data-ttu-id="9ae31-118">Questo comando aggiorna la proprietà tag per la regola di raccolta dati specificata.</span><span class="sxs-lookup"><span data-stu-id="9ae31-118">This command updates the tags property for the given data collection rule.</span></span>

## <span data-ttu-id="9ae31-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ae31-119">PARAMETERS</span></span>

### <span data-ttu-id="9ae31-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ae31-120">-DefaultProfile</span></span>
<span data-ttu-id="9ae31-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9ae31-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9ae31-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ae31-122">-ResourceGroupName</span></span>
<span data-ttu-id="9ae31-123">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="9ae31-123">The resource group name</span></span>

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

### <span data-ttu-id="9ae31-124">-RuleName</span><span class="sxs-lookup"><span data-stu-id="9ae31-124">-RuleName</span></span>
<span data-ttu-id="9ae31-125">Nome della risorsa</span><span class="sxs-lookup"><span data-stu-id="9ae31-125">The resource name</span></span>

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

### <span data-ttu-id="9ae31-126">-RuleId</span><span class="sxs-lookup"><span data-stu-id="9ae31-126">-RuleId</span></span>
<span data-ttu-id="9ae31-127">ID risorsa della regola di raccolta dati</span><span class="sxs-lookup"><span data-stu-id="9ae31-127">The resource ID of the data collection rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### <span data-ttu-id="9ae31-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ae31-128">-InputObject</span></span>
<span data-ttu-id="9ae31-129">Oggetto PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="9ae31-129">PSDataCollectionRuleResource Object</span></span>

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

### <span data-ttu-id="9ae31-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="9ae31-130">-Tag</span></span>
<span data-ttu-id="9ae31-131">Proprietà tag della regola di raccolta dati</span><span class="sxs-lookup"><span data-stu-id="9ae31-131">The tags property of the data collection rule</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: Falose
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ae31-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9ae31-132">-Confirm</span></span>
<span data-ttu-id="9ae31-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ae31-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ae31-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ae31-134">-WhatIf</span></span>
<span data-ttu-id="9ae31-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9ae31-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9ae31-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9ae31-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ae31-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ae31-137">CommonParameters</span></span>
<span data-ttu-id="9ae31-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ae31-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ae31-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9ae31-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ae31-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="9ae31-140">INPUTS</span></span>

### <span data-ttu-id="9ae31-141">System.String</span><span class="sxs-lookup"><span data-stu-id="9ae31-141">System.String</span></span>

## <span data-ttu-id="9ae31-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9ae31-142">OUTPUTS</span></span>

### <span data-ttu-id="9ae31-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="9ae31-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="9ae31-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="9ae31-144">NOTES</span></span>

## <span data-ttu-id="9ae31-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9ae31-145">RELATED LINKS</span></span>

<span data-ttu-id="9ae31-146">[New-AzDataCollectionRule](./New-AzDataCollectionRule.md) 
 [Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md) 
 [Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
 [Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="9ae31-146">[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)
[Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md)
[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)</span></span>