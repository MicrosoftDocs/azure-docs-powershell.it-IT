---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseFirewallRule.md
ms.openlocfilehash: 8dd3321804afb2f7901a8acd22cfdab3dd990c41
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369207"
---
# <span data-ttu-id="f11ac-101">Remove-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f11ac-101">Remove-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="f11ac-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f11ac-102">SYNOPSIS</span></span>
<span data-ttu-id="f11ac-103">Elimina una regola del firewall di analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="f11ac-103">Deletes a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="f11ac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f11ac-104">SYNTAX</span></span>

### <span data-ttu-id="f11ac-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f11ac-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f11ac-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f11ac-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseFirewallRule -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f11ac-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f11ac-107">DESCRIPTION</span></span>
<span data-ttu-id="f11ac-108">Il cmdlet **Remove-AzSynapseFirewallRule** Elimina definitivamente una regola del firewall di analisi di Azure sinapsi.</span><span class="sxs-lookup"><span data-stu-id="f11ac-108">The **Remove-AzSynapseFirewallRule** cmdlet permanently deletes an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="f11ac-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f11ac-109">EXAMPLES</span></span>

### <span data-ttu-id="f11ac-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f11ac-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule
```

<span data-ttu-id="f11ac-111">Questo comando Elimina la regola del firewall denominata ContosoFirewallRule in area di lavoro ContosoWorkspace con nome ContosoFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="f11ac-111">This command deletes firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="f11ac-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f11ac-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseFirewallRule -Name ContosoFirewallRule
```

<span data-ttu-id="f11ac-113">Questo comando Elimina la regola del firewall denominata ContosoFirewallRule in un'area di lavoro tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="f11ac-113">This command deletes firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

## <span data-ttu-id="f11ac-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f11ac-114">PARAMETERS</span></span>

### <span data-ttu-id="f11ac-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f11ac-115">-AsJob</span></span>
<span data-ttu-id="f11ac-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f11ac-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f11ac-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f11ac-117">-DefaultProfile</span></span>
<span data-ttu-id="f11ac-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f11ac-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f11ac-119">-Force</span><span class="sxs-lookup"><span data-stu-id="f11ac-119">-Force</span></span>
<span data-ttu-id="f11ac-120">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="f11ac-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f11ac-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="f11ac-121">-Name</span></span>
<span data-ttu-id="f11ac-122">Il nome della regola firerwall per l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="f11ac-122">The firerwall rule name for the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f11ac-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f11ac-123">-PassThru</span></span>
<span data-ttu-id="f11ac-124">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="f11ac-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="f11ac-125">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="f11ac-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="f11ac-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f11ac-126">-ResourceGroupName</span></span>
<span data-ttu-id="f11ac-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f11ac-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f11ac-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f11ac-128">-WorkspaceName</span></span>
<span data-ttu-id="f11ac-129">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="f11ac-129">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f11ac-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f11ac-130">-WorkspaceObject</span></span>
<span data-ttu-id="f11ac-131">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="f11ac-131">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f11ac-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f11ac-132">-Confirm</span></span>
<span data-ttu-id="f11ac-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f11ac-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f11ac-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f11ac-134">-WhatIf</span></span>
<span data-ttu-id="f11ac-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f11ac-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f11ac-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f11ac-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f11ac-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f11ac-137">CommonParameters</span></span>
<span data-ttu-id="f11ac-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f11ac-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f11ac-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f11ac-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f11ac-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f11ac-140">INPUTS</span></span>

### <span data-ttu-id="f11ac-141">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f11ac-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="f11ac-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f11ac-142">OUTPUTS</span></span>

### <span data-ttu-id="f11ac-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f11ac-143">System.Boolean</span></span>

## <span data-ttu-id="f11ac-144">Note</span><span class="sxs-lookup"><span data-stu-id="f11ac-144">NOTES</span></span>

## <span data-ttu-id="f11ac-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f11ac-145">RELATED LINKS</span></span>
