---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Remove-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Remove-AzMetricAlertRuleV2.md
ms.openlocfilehash: 7688907a2a8b4f8a11a7290fa01294538e24f29f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861082"
---
# <span data-ttu-id="490bf-101">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="490bf-101">Remove-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="490bf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="490bf-102">SYNOPSIS</span></span>
<span data-ttu-id="490bf-103">Rimuove una regola di avviso metrica V2 (non classica).</span><span class="sxs-lookup"><span data-stu-id="490bf-103">Removes a V2 (non-classic) metric alert rule.</span></span>

## <span data-ttu-id="490bf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="490bf-104">SYNTAX</span></span>

### <span data-ttu-id="490bf-105">ByMetricRuleResourceName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="490bf-105">ByMetricRuleResourceName (Default)</span></span>
```
Remove-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="490bf-106">ByMetricRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="490bf-106">ByMetricRuleResourceId</span></span>
```
Remove-AzMetricAlertRuleV2 -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="490bf-107">ByRuleObject</span><span class="sxs-lookup"><span data-stu-id="490bf-107">ByRuleObject</span></span>
```
Remove-AzMetricAlertRuleV2 -InputObject <PSMetricAlertRuleV2> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="490bf-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="490bf-108">DESCRIPTION</span></span>
<span data-ttu-id="490bf-109">Il cmdlet **Remove-AzMetricAlertRuleV2** rimuove una regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="490bf-109">The **Remove-AzMetricAlertRuleV2** cmdlet removes an alert rule.</span></span> <span data-ttu-id="490bf-110">Questo cmdlet implementa il modello ShouldProcess, vale a dire che potrebbe richiedere conferma all'utente prima di creare, modificare o rimuovere la risorsa.</span><span class="sxs-lookup"><span data-stu-id="490bf-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="490bf-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="490bf-111">EXAMPLES</span></span>

### <span data-ttu-id="490bf-112">Esempio 1: rimuovere una regola di avviso per nome</span><span class="sxs-lookup"><span data-stu-id="490bf-112">Example 1: Remove an alert rule by name</span></span>

```powershell
PS C:\> Remove-AzMetricAlertRuleV2 -ResourceGroupName xxxxRG -Name PsSdk -PassThru
True
```

<span data-ttu-id="490bf-113">Questo comando rimuove la regola di avviso denominata PsSdk</span><span class="sxs-lookup"><span data-stu-id="490bf-113">This command removes the alert rule named PsSdk</span></span>

### <span data-ttu-id="490bf-114">Esempio 2: rimuovere una regola di avviso in base all'ID</span><span class="sxs-lookup"><span data-stu-id="490bf-114">Example 2: Remove an alert rule by ID</span></span>

```powershell
PS C:\>Remove-AzMetricAlertRuleV2 -ResourceId /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule
```

<span data-ttu-id="490bf-115">Questo comando rimuove la regola di avviso con ID risorsa `/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule`</span><span class="sxs-lookup"><span data-stu-id="490bf-115">This command removes the alert rule with resource ID `/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule`</span></span>

### <span data-ttu-id="490bf-116">Esempio 3: ottenere un avviso e rimuoverlo</span><span class="sxs-lookup"><span data-stu-id="490bf-116">Example 3: Get an alert and remove it</span></span>

```powershell
PS c:\>Get-AzMetricAlertRuleV2 -ResourceGroupName alertstest -Name sampleAlertRule |Remove-AzMetricAlertRuleV2
```

<span data-ttu-id="490bf-117">Questo comando ottiene un avviso e lo rimuove.</span><span class="sxs-lookup"><span data-stu-id="490bf-117">This command gets an alert and removes it.</span></span>

## <span data-ttu-id="490bf-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="490bf-118">PARAMETERS</span></span>

### <span data-ttu-id="490bf-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="490bf-119">-AsJob</span></span>
<span data-ttu-id="490bf-120">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="490bf-120">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="490bf-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="490bf-121">-DefaultProfile</span></span>
<span data-ttu-id="490bf-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="490bf-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="490bf-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="490bf-123">-InputObject</span></span>
<span data-ttu-id="490bf-124">Oggetto regola metrica</span><span class="sxs-lookup"><span data-stu-id="490bf-124">The Metric rule object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2
Parameter Sets: ByRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="490bf-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="490bf-125">-Name</span></span>
<span data-ttu-id="490bf-126">Nome della regola di avviso metrica</span><span class="sxs-lookup"><span data-stu-id="490bf-126">The name of metric alert rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByMetricRuleResourceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="490bf-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="490bf-127">-PassThru</span></span>
<span data-ttu-id="490bf-128">Restituisce vero dopo l'eliminazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="490bf-128">Return true upon successful deletion.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="490bf-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="490bf-129">-ResourceGroupName</span></span>
<span data-ttu-id="490bf-130">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="490bf-130">The ResourceGroupName</span></span>

```yaml
Type: System.String
Parameter Sets: ByMetricRuleResourceName
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="490bf-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="490bf-131">-ResourceId</span></span>
<span data-ttu-id="490bf-132">RuleResourceId</span><span class="sxs-lookup"><span data-stu-id="490bf-132">The RuleResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByMetricRuleResourceId
Aliases: RuleResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="490bf-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="490bf-133">-Confirm</span></span>
<span data-ttu-id="490bf-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="490bf-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="490bf-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="490bf-135">-WhatIf</span></span>
<span data-ttu-id="490bf-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="490bf-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="490bf-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="490bf-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="490bf-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="490bf-138">CommonParameters</span></span>
<span data-ttu-id="490bf-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="490bf-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="490bf-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="490bf-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="490bf-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="490bf-141">INPUTS</span></span>

### <span data-ttu-id="490bf-142">System. String</span><span class="sxs-lookup"><span data-stu-id="490bf-142">System.String</span></span>

### <span data-ttu-id="490bf-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="490bf-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="490bf-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="490bf-144">OUTPUTS</span></span>

### <span data-ttu-id="490bf-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="490bf-145">System.Boolean</span></span>

## <span data-ttu-id="490bf-146">Note</span><span class="sxs-lookup"><span data-stu-id="490bf-146">NOTES</span></span>

## <span data-ttu-id="490bf-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="490bf-147">RELATED LINKS</span></span>
