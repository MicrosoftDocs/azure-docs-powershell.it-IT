---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseFirewallRule.md
ms.openlocfilehash: 6df0e33ff94be7bf5e060b929206c09180d830f5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961086"
---
# <span data-ttu-id="a3d8f-101">Remove-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a3d8f-101">Remove-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="a3d8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3d8f-102">SYNOPSIS</span></span>
<span data-ttu-id="a3d8f-103">Elimina una regola del firewall di Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="a3d8f-103">Deletes a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="a3d8f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a3d8f-104">SYNTAX</span></span>

### <span data-ttu-id="a3d8f-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a3d8f-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3d8f-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3d8f-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseFirewallRule -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3d8f-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a3d8f-107">DESCRIPTION</span></span>
<span data-ttu-id="a3d8f-108">Il cmdlet **Remove-AzSynapseFirewallRule** elimina definitivamente una regola del firewall di Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="a3d8f-108">The **Remove-AzSynapseFirewallRule** cmdlet permanently deletes an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="a3d8f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a3d8f-109">EXAMPLES</span></span>

### <span data-ttu-id="a3d8f-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a3d8f-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule
```

<span data-ttu-id="a3d8f-111">Questo comando elimina la regola del firewall denominata ContosoFirewallRule nell'area di lavoro ContosoWorkspace con il nome ContosoFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="a3d8f-111">This command deletes firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="a3d8f-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a3d8f-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseFirewallRule -Name ContosoFirewallRule
```

<span data-ttu-id="a3d8f-113">Questo comando elimina la regola del firewall denominata ContosoFirewallRule in un'area di lavoro tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="a3d8f-113">This command deletes firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

## <span data-ttu-id="a3d8f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3d8f-114">PARAMETERS</span></span>

### <span data-ttu-id="a3d8f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3d8f-115">-AsJob</span></span>
<span data-ttu-id="a3d8f-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a3d8f-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a3d8f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3d8f-117">-DefaultProfile</span></span>
<span data-ttu-id="a3d8f-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a3d8f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3d8f-119">-Force</span><span class="sxs-lookup"><span data-stu-id="a3d8f-119">-Force</span></span>
<span data-ttu-id="a3d8f-120">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="a3d8f-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a3d8f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a3d8f-121">-Name</span></span>
<span data-ttu-id="a3d8f-122">Nome della regola firerwall per l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="a3d8f-122">The firerwall rule name for the workspace.</span></span>

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

### <span data-ttu-id="a3d8f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a3d8f-123">-PassThru</span></span>
<span data-ttu-id="a3d8f-124">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a3d8f-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="a3d8f-125">Se questa opzione è specificata, restituisce true se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="a3d8f-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="a3d8f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3d8f-126">-ResourceGroupName</span></span>
<span data-ttu-id="a3d8f-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a3d8f-127">Resource group name.</span></span>

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

### <span data-ttu-id="a3d8f-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a3d8f-128">-WorkspaceName</span></span>
<span data-ttu-id="a3d8f-129">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="a3d8f-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a3d8f-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a3d8f-130">-WorkspaceObject</span></span>
<span data-ttu-id="a3d8f-131">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="a3d8f-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a3d8f-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a3d8f-132">-Confirm</span></span>
<span data-ttu-id="a3d8f-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3d8f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3d8f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3d8f-134">-WhatIf</span></span>
<span data-ttu-id="a3d8f-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a3d8f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3d8f-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a3d8f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3d8f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3d8f-137">CommonParameters</span></span>
<span data-ttu-id="a3d8f-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3d8f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3d8f-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a3d8f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3d8f-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="a3d8f-140">INPUTS</span></span>

### <span data-ttu-id="a3d8f-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a3d8f-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="a3d8f-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a3d8f-142">OUTPUTS</span></span>

### <span data-ttu-id="a3d8f-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a3d8f-143">System.Boolean</span></span>

## <span data-ttu-id="a3d8f-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="a3d8f-144">NOTES</span></span>

## <span data-ttu-id="a3d8f-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a3d8f-145">RELATED LINKS</span></span>
