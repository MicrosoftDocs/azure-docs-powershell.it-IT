---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/powershell/module/az.alertsmanagement/get-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
ms.openlocfilehash: c90c4ba559bfe6e453a984546217692181f40597
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961038"
---
# <span data-ttu-id="e1bc7-101">Get-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="e1bc7-101">Get-AzActionRule</span></span>

## <span data-ttu-id="e1bc7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1bc7-102">SYNOPSIS</span></span>
<span data-ttu-id="e1bc7-103">Ottenere informazioni sulle regole di azione</span><span class="sxs-lookup"><span data-stu-id="e1bc7-103">Get Action Rules Information</span></span>

## <span data-ttu-id="e1bc7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e1bc7-104">SYNTAX</span></span>

### <span data-ttu-id="e1bc7-105">ListActionRules (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e1bc7-105">ListActionRules (Default)</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceType <String>]
 [-TargetResourceGroup <String>] [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>]
 [-AlertRuleId <String>] [-Description <String>] [-ActionGroup <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1bc7-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1bc7-106">ResourceId</span></span>
```
Get-AzActionRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1bc7-107">ActionRuleByName</span><span class="sxs-lookup"><span data-stu-id="e1bc7-107">ActionRuleByName</span></span>
```
Get-AzActionRule -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e1bc7-108">ListActionRulesByTargetResourceId</span><span class="sxs-lookup"><span data-stu-id="e1bc7-108">ListActionRulesByTargetResourceId</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceId <String>]
 [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>] [-AlertRuleId <String>]
 [-Description <String>] [-ActionGroup <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e1bc7-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e1bc7-109">DESCRIPTION</span></span>
<span data-ttu-id="e1bc7-110">Il cmdlet **Get-AzActionRule** ottiene le regole di azione configurate.</span><span class="sxs-lookup"><span data-stu-id="e1bc7-110">**Get-AzActionRule** cmdlet gets action rules configured.</span></span>

## <span data-ttu-id="e1bc7-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e1bc7-111">EXAMPLES</span></span>

### <span data-ttu-id="e1bc7-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e1bc7-112">Example 1</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Severity "Sev2" -MonitorService "Platform"
```

<span data-ttu-id="e1bc7-113">Elencare tutte le regole di azione configurate nel test-rg del gruppo di risorse filtrate in base alla gravità di Sev2 e al servizio Monitoraggio piattaforma.</span><span class="sxs-lookup"><span data-stu-id="e1bc7-113">List all action rules configured in resource group test-rg filtered on Sev2 severity and Platform Monitor Service.</span></span> <span data-ttu-id="e1bc7-114">Usare Format-List per ottenere i dettagli di ogni regola di azione nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="e1bc7-114">Use Format-List to get the details of each action rule in list.</span></span>

### <span data-ttu-id="e1bc7-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e1bc7-115">Example 2</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Name "Test-Action-Rule" | Format-List
```

<span data-ttu-id="e1bc7-116">Ottenere la regola di azione con il nome Test-Action-Rule nel gruppo di risorse test-rg.</span><span class="sxs-lookup"><span data-stu-id="e1bc7-116">Get the action rule with name Test-Action-Rule in test-rg resource group.</span></span>

## <span data-ttu-id="e1bc7-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1bc7-117">PARAMETERS</span></span>

### <span data-ttu-id="e1bc7-118">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="e1bc7-118">-ActionGroup</span></span>
<span data-ttu-id="e1bc7-119">Gruppo di azioni</span><span class="sxs-lookup"><span data-stu-id="e1bc7-119">Action group</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1bc7-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="e1bc7-120">-AlertRuleId</span></span>
<span data-ttu-id="e1bc7-121">Filtro in base all'ID regola di avviso</span><span class="sxs-lookup"><span data-stu-id="e1bc7-121">Filter on Alert Rule Id</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1bc7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1bc7-122">-DefaultProfile</span></span>
<span data-ttu-id="e1bc7-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e1bc7-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1bc7-124">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="e1bc7-124">-Description</span></span>
<span data-ttu-id="e1bc7-125">Filtrare tutti gli avvisi con l'ID gruppo smart</span><span class="sxs-lookup"><span data-stu-id="e1bc7-125">Filter all the alerts having the Smart Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1bc7-126">-ImpactedScope</span><span class="sxs-lookup"><span data-stu-id="e1bc7-126">-ImpactedScope</span></span>
<span data-ttu-id="e1bc7-127">Filtro in base all'ambito in cui è stato applicato l'impatto</span><span class="sxs-lookup"><span data-stu-id="e1bc7-127">Filter on Impacted scope</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1bc7-128">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="e1bc7-128">-MonitorService</span></span>
<span data-ttu-id="e1bc7-129">Filtro in base a servizio di messaggi</span><span class="sxs-lookup"><span data-stu-id="e1bc7-129">Filter on Moniter Service</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1bc7-130">-Name</span><span class="sxs-lookup"><span data-stu-id="e1bc7-130">-Name</span></span>
<span data-ttu-id="e1bc7-131">Nome della regola di azione.</span><span class="sxs-lookup"><span data-stu-id="e1bc7-131">Name of action rule.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ActionRuleByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1bc7-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1bc7-132">-ResourceGroupName</span></span>
<span data-ttu-id="e1bc7-133">Nome gruppo di risorse in cui si trova la regola di azione.</span><span class="sxs-lookup"><span data-stu-id="e1bc7-133">Resource Group Name in which action rule resides.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ActionRuleByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1bc7-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1bc7-134">-ResourceId</span></span>
<span data-ttu-id="e1bc7-135">Ottenere la regola Azione in base all'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="e1bc7-135">Get Action rule by resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1bc7-136">-Gravità</span><span class="sxs-lookup"><span data-stu-id="e1bc7-136">-Severity</span></span>
<span data-ttu-id="e1bc7-137">Filtrare in base alla gravità dell'avviso</span><span class="sxs-lookup"><span data-stu-id="e1bc7-137">Filter on Severity of alert</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1bc7-138">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e1bc7-138">-TargetResourceGroup</span></span>
<span data-ttu-id="e1bc7-139">Filtrare in base al nome del gruppo di risorse della risorsa di destinazione dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="e1bc7-139">Filter on Resource group name of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1bc7-140">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="e1bc7-140">-TargetResourceId</span></span>
<span data-ttu-id="e1bc7-141">Filtrare in base all'ID risorsa della risorsa di destinazione dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="e1bc7-141">Filter on Resource Id of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1bc7-142">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="e1bc7-142">-TargetResourceType</span></span>
<span data-ttu-id="e1bc7-143">Filtrare in base al tipo di risorsa della risorsa di destinazione dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="e1bc7-143">Filter on Resource type of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1bc7-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1bc7-144">CommonParameters</span></span>
<span data-ttu-id="e1bc7-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1bc7-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1bc7-146">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e1bc7-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1bc7-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="e1bc7-147">INPUTS</span></span>

### <span data-ttu-id="e1bc7-148">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e1bc7-148">None</span></span>

## <span data-ttu-id="e1bc7-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e1bc7-149">OUTPUTS</span></span>

### <span data-ttu-id="e1bc7-150">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="e1bc7-150">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="e1bc7-151">NOTE</span><span class="sxs-lookup"><span data-stu-id="e1bc7-151">NOTES</span></span>

## <span data-ttu-id="e1bc7-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e1bc7-152">RELATED LINKS</span></span>
