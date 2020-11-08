---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
ms.openlocfilehash: 59ce466233e4997f54ed8f29835e7e64d455fb86
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200405"
---
# <span data-ttu-id="4bdce-101">Get-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="4bdce-101">Get-AzActionRule</span></span>

## <span data-ttu-id="4bdce-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4bdce-102">SYNOPSIS</span></span>
<span data-ttu-id="4bdce-103">Ottenere informazioni sulle regole di azione</span><span class="sxs-lookup"><span data-stu-id="4bdce-103">Get Action Rules Information</span></span>

## <span data-ttu-id="4bdce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4bdce-104">SYNTAX</span></span>

### <span data-ttu-id="4bdce-105">ListActionRules (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4bdce-105">ListActionRules (Default)</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceType <String>]
 [-TargetResourceGroup <String>] [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>]
 [-AlertRuleId <String>] [-Description <String>] [-ActionGroup <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bdce-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4bdce-106">ResourceId</span></span>
```
Get-AzActionRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bdce-107">ActionRuleByName</span><span class="sxs-lookup"><span data-stu-id="4bdce-107">ActionRuleByName</span></span>
```
Get-AzActionRule -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4bdce-108">ListActionRulesByTargetResourceId</span><span class="sxs-lookup"><span data-stu-id="4bdce-108">ListActionRulesByTargetResourceId</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceId <String>]
 [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>] [-AlertRuleId <String>]
 [-Description <String>] [-ActionGroup <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4bdce-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4bdce-109">DESCRIPTION</span></span>
<span data-ttu-id="4bdce-110">Il cmdlet **Get-AzActionRule** ottiene le regole di azione configurate.</span><span class="sxs-lookup"><span data-stu-id="4bdce-110">**Get-AzActionRule** cmdlet gets action rules configured.</span></span>

## <span data-ttu-id="4bdce-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4bdce-111">EXAMPLES</span></span>

### <span data-ttu-id="4bdce-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4bdce-112">Example 1</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Severity "Sev2" -MonitorService "Platform"
```

<span data-ttu-id="4bdce-113">Elenca tutte le regole di azione configurate nel gruppo di risorse test-RG filtrato in base alla gravità Sev2 e al servizio Platform monitor.</span><span class="sxs-lookup"><span data-stu-id="4bdce-113">List all action rules configured in resource group test-rg filtered on Sev2 severity and Platform Monitor Service.</span></span> <span data-ttu-id="4bdce-114">Usare Format-List per ottenere i dettagli di ogni regola di azione nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="4bdce-114">Use Format-List to get the details of each action rule in list.</span></span>

### <span data-ttu-id="4bdce-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="4bdce-115">Example 2</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Name "Test-Action-Rule" | Format-List
```

<span data-ttu-id="4bdce-116">Ottenere la regola di azione con nome test-azione-regola nel gruppo di risorse test-RG.</span><span class="sxs-lookup"><span data-stu-id="4bdce-116">Get the action rule with name Test-Action-Rule in test-rg resource group.</span></span>

## <span data-ttu-id="4bdce-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4bdce-117">PARAMETERS</span></span>

### <span data-ttu-id="4bdce-118">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="4bdce-118">-ActionGroup</span></span>
<span data-ttu-id="4bdce-119">Gruppo azioni</span><span class="sxs-lookup"><span data-stu-id="4bdce-119">Action group</span></span>

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

### <span data-ttu-id="4bdce-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="4bdce-120">-AlertRuleId</span></span>
<span data-ttu-id="4bdce-121">Filtrare l'ID della regola di avviso</span><span class="sxs-lookup"><span data-stu-id="4bdce-121">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="4bdce-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bdce-122">-DefaultProfile</span></span>
<span data-ttu-id="4bdce-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4bdce-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bdce-124">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="4bdce-124">-Description</span></span>
<span data-ttu-id="4bdce-125">Filtrare tutti gli avvisi con l'ID gruppo smart</span><span class="sxs-lookup"><span data-stu-id="4bdce-125">Filter all the alerts having the Smart Group Id</span></span>

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

### <span data-ttu-id="4bdce-126">-ImpactedScope</span><span class="sxs-lookup"><span data-stu-id="4bdce-126">-ImpactedScope</span></span>
<span data-ttu-id="4bdce-127">Filtro per l'ambito con impatto</span><span class="sxs-lookup"><span data-stu-id="4bdce-127">Filter on Impacted scope</span></span>

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

### <span data-ttu-id="4bdce-128">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="4bdce-128">-MonitorService</span></span>
<span data-ttu-id="4bdce-129">Filtrare il servizio moniter</span><span class="sxs-lookup"><span data-stu-id="4bdce-129">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="4bdce-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="4bdce-130">-Name</span></span>
<span data-ttu-id="4bdce-131">Nome della regola di azione.</span><span class="sxs-lookup"><span data-stu-id="4bdce-131">Name of action rule.</span></span>

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

### <span data-ttu-id="4bdce-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bdce-132">-ResourceGroupName</span></span>
<span data-ttu-id="4bdce-133">Nome del gruppo di risorse in cui si trova la regola di azione.</span><span class="sxs-lookup"><span data-stu-id="4bdce-133">Resource Group Name in which action rule resides.</span></span>

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

### <span data-ttu-id="4bdce-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4bdce-134">-ResourceId</span></span>
<span data-ttu-id="4bdce-135">Ottenere la regola dell'azione in base all'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="4bdce-135">Get Action rule by resource id.</span></span>

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

### <span data-ttu-id="4bdce-136">-Gravità</span><span class="sxs-lookup"><span data-stu-id="4bdce-136">-Severity</span></span>
<span data-ttu-id="4bdce-137">Filtrare la gravità dell'avviso</span><span class="sxs-lookup"><span data-stu-id="4bdce-137">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="4bdce-138">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4bdce-138">-TargetResourceGroup</span></span>
<span data-ttu-id="4bdce-139">Filtrare il nome del gruppo di risorse della risorsa di destinazione di Alert.</span><span class="sxs-lookup"><span data-stu-id="4bdce-139">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="4bdce-140">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="4bdce-140">-TargetResourceId</span></span>
<span data-ttu-id="4bdce-141">Filtrare l'ID risorsa della risorsa di destinazione di Alert.</span><span class="sxs-lookup"><span data-stu-id="4bdce-141">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="4bdce-142">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="4bdce-142">-TargetResourceType</span></span>
<span data-ttu-id="4bdce-143">Filtrare il tipo di risorsa della risorsa di destinazione di Alert.</span><span class="sxs-lookup"><span data-stu-id="4bdce-143">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="4bdce-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bdce-144">CommonParameters</span></span>
<span data-ttu-id="4bdce-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bdce-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bdce-146">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4bdce-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bdce-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4bdce-147">INPUTS</span></span>

### <span data-ttu-id="4bdce-148">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4bdce-148">None</span></span>

## <span data-ttu-id="4bdce-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4bdce-149">OUTPUTS</span></span>

### <span data-ttu-id="4bdce-150">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="4bdce-150">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="4bdce-151">Note</span><span class="sxs-lookup"><span data-stu-id="4bdce-151">NOTES</span></span>

## <span data-ttu-id="4bdce-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4bdce-152">RELATED LINKS</span></span>