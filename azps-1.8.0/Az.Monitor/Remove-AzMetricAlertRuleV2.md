---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzMetricAlertRuleV2.md
ms.openlocfilehash: 698f05840df6578d8595e2ca8e31c9f0a11bc722
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678749"
---
# <span data-ttu-id="ae55a-101">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="ae55a-101">Remove-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="ae55a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ae55a-102">SYNOPSIS</span></span>
<span data-ttu-id="ae55a-103">Rimuove una regola di avviso metrica V2 (non classica).</span><span class="sxs-lookup"><span data-stu-id="ae55a-103">Removes a V2 (non-classic) metric alert rule.</span></span>

## <span data-ttu-id="ae55a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ae55a-104">SYNTAX</span></span>

### <span data-ttu-id="ae55a-105">ByMetricRuleResourceName</span><span class="sxs-lookup"><span data-stu-id="ae55a-105">ByMetricRuleResourceName</span></span>
```
Remove-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae55a-106">ByMetricRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="ae55a-106">ByMetricRuleResourceId</span></span>
```
Remove-AzMetricAlertRuleV2 -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae55a-107">ByRuleObject</span><span class="sxs-lookup"><span data-stu-id="ae55a-107">ByRuleObject</span></span>
```
Remove-AzMetricAlertRuleV2 -InputObject <PSMetricAlertRuleV2> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae55a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ae55a-108">DESCRIPTION</span></span>
<span data-ttu-id="ae55a-109">Il cmdlet **Remove-AzMetricAlertRuleV2** rimuove una regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="ae55a-109">The **Remove-AzMetricAlertRuleV2** cmdlet removes an alert rule.</span></span> <span data-ttu-id="ae55a-110">Questo cmdlet implementa il modello ShouldProcess, vale a dire che potrebbe richiedere conferma all'utente prima di creare, modificare o rimuovere la risorsa.</span><span class="sxs-lookup"><span data-stu-id="ae55a-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="ae55a-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ae55a-111">EXAMPLES</span></span>

### <span data-ttu-id="ae55a-112">Esempio 1: rimuovere una regola di avviso per nome</span><span class="sxs-lookup"><span data-stu-id="ae55a-112">Example 1: Remove an alert rule by name</span></span>

```powershell
PS C:\> Remove-AzMetricAlertRuleV2 -ResourceGroupName xxxxRG -Name PsSdk -PassThru
True
```

<span data-ttu-id="ae55a-113">Questo comando rimuove la regola di avviso denominata PsSdk</span><span class="sxs-lookup"><span data-stu-id="ae55a-113">This command removes the alert rule named PsSdk</span></span>

### <span data-ttu-id="ae55a-114">Esempio 2: rimuovere una regola di avviso in base all'ID</span><span class="sxs-lookup"><span data-stu-id="ae55a-114">Example 2: Remove an alert rule by ID</span></span>

```powershell
PS C:\>Remove-AzMetricAlertRuleV2 -ResourceId /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule
```

<span data-ttu-id="ae55a-115">Questo comando rimuove la regola di avviso con ID risorsa `/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule`</span><span class="sxs-lookup"><span data-stu-id="ae55a-115">This command removes the alert rule with resource ID `/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule`</span></span>
### <span data-ttu-id="ae55a-116">Esempio 3: ottenere un avviso e rimuoverlo</span><span class="sxs-lookup"><span data-stu-id="ae55a-116">Example 3: Get an alert and remove it</span></span>

```powershell
PS c:\>Get-AzMetricAlertRuleV2 -ResourceGroupName alertstest -Name sampleAlertRule |Remove-AzMetricAlertRuleV2
```

<span data-ttu-id="ae55a-117">Questo comando ottiene un avviso e lo rimuove.</span><span class="sxs-lookup"><span data-stu-id="ae55a-117">This command gets an alert and removes it.</span></span>

## <span data-ttu-id="ae55a-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ae55a-118">PARAMETERS</span></span>

### <span data-ttu-id="ae55a-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ae55a-119">-AsJob</span></span>
<span data-ttu-id="ae55a-120">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ae55a-120">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae55a-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ae55a-121">-Confirm</span></span>
<span data-ttu-id="ae55a-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae55a-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae55a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae55a-123">-DefaultProfile</span></span>
<span data-ttu-id="ae55a-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ae55a-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae55a-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae55a-125">-InputObject</span></span>
<span data-ttu-id="ae55a-126">Oggetto regola metrica</span><span class="sxs-lookup"><span data-stu-id="ae55a-126">The Metric rule object</span></span>

```yaml
Type: PSMetricAlertRuleV2
Parameter Sets: ByRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae55a-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="ae55a-127">-Name</span></span>
<span data-ttu-id="ae55a-128">Nome della regola di avviso metrica</span><span class="sxs-lookup"><span data-stu-id="ae55a-128">The name of metric alert rule</span></span>

```yaml
Type: String
Parameter Sets: ByMetricRuleResourceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae55a-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ae55a-129">-PassThru</span></span>
<span data-ttu-id="ae55a-130">Restituisce vero dopo l'eliminazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="ae55a-130">Return true upon successful deletion.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae55a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae55a-131">-ResourceGroupName</span></span>
<span data-ttu-id="ae55a-132">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae55a-132">The ResourceGroupName</span></span>

```yaml
Type: String
Parameter Sets: ByMetricRuleResourceName
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae55a-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae55a-133">-ResourceId</span></span>
<span data-ttu-id="ae55a-134">RuleResourceId</span><span class="sxs-lookup"><span data-stu-id="ae55a-134">The RuleResourceId</span></span>

```yaml
Type: String
Parameter Sets: ByMetricRuleResourceId
Aliases: RuleResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae55a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae55a-135">-WhatIf</span></span>
<span data-ttu-id="ae55a-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ae55a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae55a-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ae55a-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae55a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae55a-138">CommonParameters</span></span>
<span data-ttu-id="ae55a-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae55a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ae55a-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae55a-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae55a-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ae55a-141">INPUTS</span></span>

### <span data-ttu-id="ae55a-142">System. String</span><span class="sxs-lookup"><span data-stu-id="ae55a-142">System.String</span></span>

### <span data-ttu-id="ae55a-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="ae55a-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="ae55a-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ae55a-144">OUTPUTS</span></span>

### <span data-ttu-id="ae55a-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ae55a-145">System.Boolean</span></span>

## <span data-ttu-id="ae55a-146">Note</span><span class="sxs-lookup"><span data-stu-id="ae55a-146">NOTES</span></span>

## <span data-ttu-id="ae55a-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ae55a-147">RELATED LINKS</span></span>
