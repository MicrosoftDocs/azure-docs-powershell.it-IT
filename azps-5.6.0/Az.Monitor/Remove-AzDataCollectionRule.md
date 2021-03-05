---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/remove-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRule.md
ms.openlocfilehash: 4dfa9417b2bce7473b3d2986f503c163cb6bf42f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974798"
---
# <span data-ttu-id="4cb56-101">Remove-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="4cb56-101">Remove-AzDataCollectionRule</span></span>

## <span data-ttu-id="4cb56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cb56-102">SYNOPSIS</span></span>
<span data-ttu-id="4cb56-103">Eliminare una regola per la raccolta dei dati.</span><span class="sxs-lookup"><span data-stu-id="4cb56-103">Delete a data collection rule.</span></span>

## <span data-ttu-id="4cb56-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4cb56-104">SYNTAX</span></span>

### <span data-ttu-id="4cb56-105">ByName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4cb56-105">ByName (Default)</span></span>
```
Remove-AzDataCollectionRule
   -ResourceGroupName <string> 
   -RuleName <string> 
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

### <span data-ttu-id="4cb56-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4cb56-106">ByInputObject</span></span>
```
Remove-AzDataCollectionRule
   -InputObject <PSDataCollectionRuleResource>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

### <span data-ttu-id="4cb56-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4cb56-107">ByResourceId</span></span>
```
Remove-AzDataCollectionRule
   -RuleId <string>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="4cb56-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4cb56-108">DESCRIPTION</span></span>
<span data-ttu-id="4cb56-109">Il cmdlet **Remove-AzDataCollectionRule** elimina una regola di raccolta dati.</span><span class="sxs-lookup"><span data-stu-id="4cb56-109">The **Remove-AzDataCollectionRule** cmdlet delete a data collection rule.</span></span>

<span data-ttu-id="4cb56-110">Le regole di raccolta dei dati (DCR) definiscono i dati in arrivo in Azure Monitor e specificano dove devono essere inviati o archiviati i dati.</span><span class="sxs-lookup"><span data-stu-id="4cb56-110">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="4cb56-111">Ecco l'articolo [completo sulla panoramica di DCR.](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview)</span><span class="sxs-lookup"><span data-stu-id="4cb56-111">Here is the complete [DCR overview article](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

## <span data-ttu-id="4cb56-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4cb56-112">EXAMPLES</span></span>

### <span data-ttu-id="4cb56-113">Esempio 1: Eliminare una regola di raccolta dati con i parametri del nome e del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="4cb56-113">Example 1: Delete data collection rule with name and resource group parameters</span></span>
```
PS C:\>Remove-AzDataCollectionRule -ResourceGroupName "testgroup" -RuleName "testDcr"             
```

### <span data-ttu-id="4cb56-114">Esempio 2: Eliminare una regola di raccolta dati con il nome e il gruppo di risorse Return bool</span><span class="sxs-lookup"><span data-stu-id="4cb56-114">Example 2: Delete data collection rule with name and resource group return bool</span></span>
```
PS C:\>Remove-AzDataCollectionRule -ResourceGroupName "testgroup" -RuleName "testDcr" -PassThru

True
```

### <span data-ttu-id="4cb56-115">Esempio 3: Eliminare una regola di raccolta dati da InputObject</span><span class="sxs-lookup"><span data-stu-id="4cb56-115">Example 3: Delete data collection rule from InputObject</span></span>
```
PS C:\>Get-AzDataCollectionRule -ResourceGroupName "testdcr" -RuleName "dcrFromPipe95" | Remove-AzDataCollectionRule
```

### <span data-ttu-id="4cb56-116">Esempio 4: Eliminare una regola di raccolta dati dall'ID risorsa</span><span class="sxs-lookup"><span data-stu-id="4cb56-116">Example 4: Delete data collection rule from resource id</span></span>
```
PS C:\>Remove-AzDataCollectionRule -RuleId "/subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/{dcrName}"
```

## <span data-ttu-id="4cb56-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4cb56-117">PARAMETERS</span></span>

### <span data-ttu-id="4cb56-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cb56-118">-DefaultProfile</span></span>
<span data-ttu-id="4cb56-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4cb56-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4cb56-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cb56-120">-ResourceGroupName</span></span>
<span data-ttu-id="4cb56-121">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="4cb56-121">The resource group name</span></span>

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

### <span data-ttu-id="4cb56-122">-RuleName</span><span class="sxs-lookup"><span data-stu-id="4cb56-122">-RuleName</span></span>
<span data-ttu-id="4cb56-123">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="4cb56-123">The resource name.</span></span>

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

### <span data-ttu-id="4cb56-124">-RuleId</span><span class="sxs-lookup"><span data-stu-id="4cb56-124">-RuleId</span></span>
<span data-ttu-id="4cb56-125">L'identificatore di risorsa.</span><span class="sxs-lookup"><span data-stu-id="4cb56-125">The resource identifier.</span></span>

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

### <span data-ttu-id="4cb56-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4cb56-126">-Confirm</span></span>
<span data-ttu-id="4cb56-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cb56-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cb56-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cb56-128">-WhatIf</span></span>
<span data-ttu-id="4cb56-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4cb56-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4cb56-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4cb56-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cb56-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cb56-131">CommonParameters</span></span>
<span data-ttu-id="4cb56-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cb56-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cb56-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4cb56-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cb56-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="4cb56-134">INPUTS</span></span>

### <span data-ttu-id="4cb56-135">System.String</span><span class="sxs-lookup"><span data-stu-id="4cb56-135">System.String</span></span>

## <span data-ttu-id="4cb56-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4cb56-136">OUTPUTS</span></span>

### <span data-ttu-id="4cb56-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="4cb56-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="4cb56-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="4cb56-138">NOTES</span></span>

## <span data-ttu-id="4cb56-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4cb56-139">RELATED LINKS</span></span>

<span data-ttu-id="4cb56-140">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md) 
 [Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
 [New-AzDataCollectionRule](./New-AzDataCollectionRule.md) 
 [Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="4cb56-140">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)
[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)
[Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span></span>