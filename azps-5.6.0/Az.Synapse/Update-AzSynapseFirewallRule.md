---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/update-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseFirewallRule.md
ms.openlocfilehash: 48f2ea831470482a91e9ff78dc8b70472e2f556a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011165"
---
# <span data-ttu-id="c1c83-101">Update-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c1c83-101">Update-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="c1c83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1c83-102">SYNOPSIS</span></span>
<span data-ttu-id="c1c83-103">Aggiorna una regola del firewall di Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="c1c83-103">Updates a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="c1c83-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c1c83-104">SYNTAX</span></span>

### <span data-ttu-id="c1c83-105">UpdateByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c1c83-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-StartIpAddress <String>] [-EndIpAddress <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1c83-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1c83-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-StartIpAddress <String>]
 [-EndIpAddress <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c1c83-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c1c83-107">DESCRIPTION</span></span>
<span data-ttu-id="c1c83-108">Il cmdlet **Update-AzSynapseFirewallRule** modifica una regola del firewall di Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="c1c83-108">The **Update-AzSynapseFirewallRule** cmdlet modifys an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="c1c83-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c1c83-109">EXAMPLES</span></span>

### <span data-ttu-id="c1c83-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c1c83-110">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAssdress "255.255.255.255"
```

<span data-ttu-id="c1c83-111">Questo comando aggiorna la regola del firewall denominata ContosoFirewallRule nell'area di lavoro ContosoWorkspace con il nome ContosoFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="c1c83-111">This command updates firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="c1c83-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c1c83-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseFirewallRule -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAssdress "255.255.255.255"
```

<span data-ttu-id="c1c83-113">Questo comando aggiorna la regola del firewall denominata ContosoFirewallRule in un'area di lavoro tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="c1c83-113">This command updates firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

## <span data-ttu-id="c1c83-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c1c83-114">PARAMETERS</span></span>

### <span data-ttu-id="c1c83-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c1c83-115">-AsJob</span></span>
<span data-ttu-id="c1c83-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c1c83-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c1c83-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1c83-117">-DefaultProfile</span></span>
<span data-ttu-id="c1c83-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c1c83-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1c83-119">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="c1c83-119">-EndIpAddress</span></span>
<span data-ttu-id="c1c83-120">Indirizzo IP finale della regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="c1c83-120">The end IP address of the firewall rule.</span></span>
<span data-ttu-id="c1c83-121">Deve essere in formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="c1c83-121">Must be IPv4 format.</span></span>
<span data-ttu-id="c1c83-122">Deve essere maggiore o uguale a startIpAddress.</span><span class="sxs-lookup"><span data-stu-id="c1c83-122">Must be greater than or equal to startIpAddress.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1c83-123">-Name</span><span class="sxs-lookup"><span data-stu-id="c1c83-123">-Name</span></span>
<span data-ttu-id="c1c83-124">Nome della regola firerwall per l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c1c83-124">The firerwall rule name for the workspace.</span></span>

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

### <span data-ttu-id="c1c83-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1c83-125">-ResourceGroupName</span></span>
<span data-ttu-id="c1c83-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c1c83-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1c83-127">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="c1c83-127">-StartIpAddress</span></span>
<span data-ttu-id="c1c83-128">Indirizzo IP iniziale della regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="c1c83-128">The start IP address of the firewall rule.</span></span>
<span data-ttu-id="c1c83-129">Deve essere in formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="c1c83-129">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1c83-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c1c83-130">-WorkspaceName</span></span>
<span data-ttu-id="c1c83-131">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="c1c83-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1c83-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c1c83-132">-WorkspaceObject</span></span>
<span data-ttu-id="c1c83-133">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="c1c83-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1c83-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c1c83-134">-Confirm</span></span>
<span data-ttu-id="c1c83-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1c83-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1c83-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1c83-136">-WhatIf</span></span>
<span data-ttu-id="c1c83-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c1c83-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1c83-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c1c83-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1c83-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1c83-139">CommonParameters</span></span>
<span data-ttu-id="c1c83-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1c83-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1c83-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c1c83-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1c83-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="c1c83-142">INPUTS</span></span>

### <span data-ttu-id="c1c83-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c1c83-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="c1c83-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c1c83-144">OUTPUTS</span></span>

### <span data-ttu-id="c1c83-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c1c83-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="c1c83-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="c1c83-146">NOTES</span></span>

## <span data-ttu-id="c1c83-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c1c83-147">RELATED LINKS</span></span>
