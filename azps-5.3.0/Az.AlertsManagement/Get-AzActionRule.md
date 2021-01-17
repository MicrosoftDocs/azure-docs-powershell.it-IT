---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
ms.openlocfilehash: 59ce466233e4997f54ed8f29835e7e64d455fb86
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475961"
---
# <span data-ttu-id="22e4b-101">Get-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="22e4b-101">Get-AzActionRule</span></span>

## <span data-ttu-id="22e4b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="22e4b-102">SYNOPSIS</span></span>
<span data-ttu-id="22e4b-103">Ottenere informazioni sulle regole di azione</span><span class="sxs-lookup"><span data-stu-id="22e4b-103">Get Action Rules Information</span></span>

## <span data-ttu-id="22e4b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="22e4b-104">SYNTAX</span></span>

### <span data-ttu-id="22e4b-105">ListActionRules (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="22e4b-105">ListActionRules (Default)</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceType <String>]
 [-TargetResourceGroup <String>] [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>]
 [-AlertRuleId <String>] [-Description <String>] [-ActionGroup <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22e4b-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="22e4b-106">ResourceId</span></span>
```
Get-AzActionRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22e4b-107">ActionRuleByName</span><span class="sxs-lookup"><span data-stu-id="22e4b-107">ActionRuleByName</span></span>
```
Get-AzActionRule -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="22e4b-108">ListActionRulesByTargetResourceId</span><span class="sxs-lookup"><span data-stu-id="22e4b-108">ListActionRulesByTargetResourceId</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceId <String>]
 [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>] [-AlertRuleId <String>]
 [-Description <String>] [-ActionGroup <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="22e4b-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="22e4b-109">DESCRIPTION</span></span>
<span data-ttu-id="22e4b-110">Il cmdlet **Get-AzActionRule** ottiene le regole di azione configurate.</span><span class="sxs-lookup"><span data-stu-id="22e4b-110">**Get-AzActionRule** cmdlet gets action rules configured.</span></span>

## <span data-ttu-id="22e4b-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="22e4b-111">EXAMPLES</span></span>

### <span data-ttu-id="22e4b-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="22e4b-112">Example 1</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Severity "Sev2" -MonitorService "Platform"
```

<span data-ttu-id="22e4b-113">Elenca tutte le regole di azione configurate nel gruppo di risorse test-RG filtrato in base alla gravità Sev2 e al servizio Platform monitor.</span><span class="sxs-lookup"><span data-stu-id="22e4b-113">List all action rules configured in resource group test-rg filtered on Sev2 severity and Platform Monitor Service.</span></span> <span data-ttu-id="22e4b-114">Usare Format-List per ottenere i dettagli di ogni regola di azione nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="22e4b-114">Use Format-List to get the details of each action rule in list.</span></span>

### <span data-ttu-id="22e4b-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="22e4b-115">Example 2</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Name "Test-Action-Rule" | Format-List
```

<span data-ttu-id="22e4b-116">Ottenere la regola di azione con nome test-azione-regola nel gruppo di risorse test-RG.</span><span class="sxs-lookup"><span data-stu-id="22e4b-116">Get the action rule with name Test-Action-Rule in test-rg resource group.</span></span>

## <span data-ttu-id="22e4b-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="22e4b-117">PARAMETERS</span></span>

### <span data-ttu-id="22e4b-118">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="22e4b-118">-ActionGroup</span></span>
<span data-ttu-id="22e4b-119">Gruppo azioni</span><span class="sxs-lookup"><span data-stu-id="22e4b-119">Action group</span></span>

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

### <span data-ttu-id="22e4b-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="22e4b-120">-AlertRuleId</span></span>
<span data-ttu-id="22e4b-121">Filtrare l'ID della regola di avviso</span><span class="sxs-lookup"><span data-stu-id="22e4b-121">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="22e4b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22e4b-122">-DefaultProfile</span></span>
<span data-ttu-id="22e4b-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="22e4b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22e4b-124">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="22e4b-124">-Description</span></span>
<span data-ttu-id="22e4b-125">Filtrare tutti gli avvisi con l'ID gruppo smart</span><span class="sxs-lookup"><span data-stu-id="22e4b-125">Filter all the alerts having the Smart Group Id</span></span>

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

### <span data-ttu-id="22e4b-126">-ImpactedScope</span><span class="sxs-lookup"><span data-stu-id="22e4b-126">-ImpactedScope</span></span>
<span data-ttu-id="22e4b-127">Filtro per l'ambito con impatto</span><span class="sxs-lookup"><span data-stu-id="22e4b-127">Filter on Impacted scope</span></span>

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

### <span data-ttu-id="22e4b-128">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="22e4b-128">-MonitorService</span></span>
<span data-ttu-id="22e4b-129">Filtrare il servizio moniter</span><span class="sxs-lookup"><span data-stu-id="22e4b-129">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="22e4b-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="22e4b-130">-Name</span></span>
<span data-ttu-id="22e4b-131">Nome della regola di azione.</span><span class="sxs-lookup"><span data-stu-id="22e4b-131">Name of action rule.</span></span>

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

### <span data-ttu-id="22e4b-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22e4b-132">-ResourceGroupName</span></span>
<span data-ttu-id="22e4b-133">Nome del gruppo di risorse in cui si trova la regola di azione.</span><span class="sxs-lookup"><span data-stu-id="22e4b-133">Resource Group Name in which action rule resides.</span></span>

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

### <span data-ttu-id="22e4b-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22e4b-134">-ResourceId</span></span>
<span data-ttu-id="22e4b-135">Ottenere la regola dell'azione in base all'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="22e4b-135">Get Action rule by resource id.</span></span>

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

### <span data-ttu-id="22e4b-136">-Gravità</span><span class="sxs-lookup"><span data-stu-id="22e4b-136">-Severity</span></span>
<span data-ttu-id="22e4b-137">Filtrare la gravità dell'avviso</span><span class="sxs-lookup"><span data-stu-id="22e4b-137">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="22e4b-138">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="22e4b-138">-TargetResourceGroup</span></span>
<span data-ttu-id="22e4b-139">Filtrare il nome del gruppo di risorse della risorsa di destinazione di Alert.</span><span class="sxs-lookup"><span data-stu-id="22e4b-139">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="22e4b-140">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="22e4b-140">-TargetResourceId</span></span>
<span data-ttu-id="22e4b-141">Filtrare l'ID risorsa della risorsa di destinazione di Alert.</span><span class="sxs-lookup"><span data-stu-id="22e4b-141">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="22e4b-142">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="22e4b-142">-TargetResourceType</span></span>
<span data-ttu-id="22e4b-143">Filtrare il tipo di risorsa della risorsa di destinazione di Alert.</span><span class="sxs-lookup"><span data-stu-id="22e4b-143">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="22e4b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22e4b-144">CommonParameters</span></span>
<span data-ttu-id="22e4b-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22e4b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22e4b-146">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22e4b-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22e4b-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="22e4b-147">INPUTS</span></span>

### <span data-ttu-id="22e4b-148">Nessuno</span><span class="sxs-lookup"><span data-stu-id="22e4b-148">None</span></span>

## <span data-ttu-id="22e4b-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="22e4b-149">OUTPUTS</span></span>

### <span data-ttu-id="22e4b-150">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="22e4b-150">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="22e4b-151">Note</span><span class="sxs-lookup"><span data-stu-id="22e4b-151">NOTES</span></span>

## <span data-ttu-id="22e4b-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="22e4b-152">RELATED LINKS</span></span>
