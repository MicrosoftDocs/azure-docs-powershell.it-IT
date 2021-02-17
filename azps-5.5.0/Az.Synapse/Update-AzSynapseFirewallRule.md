---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseFirewallRule.md
ms.openlocfilehash: 9188a1cc8dde39db4d755fb2059f3633fc85ead8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190567"
---
# <span data-ttu-id="04154-101">Update-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="04154-101">Update-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="04154-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04154-102">SYNOPSIS</span></span>
<span data-ttu-id="04154-103">Aggiorna una regola del firewall di Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="04154-103">Updates a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="04154-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="04154-104">SYNTAX</span></span>

### <span data-ttu-id="04154-105">UpdateByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="04154-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-StartIpAddress <String>] [-EndIpAddress <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04154-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="04154-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-StartIpAddress <String>]
 [-EndIpAddress <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="04154-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="04154-107">DESCRIPTION</span></span>
<span data-ttu-id="04154-108">Il cmdlet **Update-AzSynapseFirewallRule** modifica una regola del firewall di Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="04154-108">The **Update-AzSynapseFirewallRule** cmdlet modifys an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="04154-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="04154-109">EXAMPLES</span></span>

### <span data-ttu-id="04154-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="04154-110">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAssdress "255.255.255.255"
```

<span data-ttu-id="04154-111">Questo comando aggiorna la regola del firewall denominata ContosoFirewallRule nell'area di lavoro ContosoWorkspace con il nome ContosoFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="04154-111">This command updates firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="04154-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="04154-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseFirewallRule -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAssdress "255.255.255.255"
```

<span data-ttu-id="04154-113">Questo comando aggiorna la regola del firewall denominata ContosoFirewallRule in un'area di lavoro tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="04154-113">This command updates firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

## <span data-ttu-id="04154-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04154-114">PARAMETERS</span></span>

### <span data-ttu-id="04154-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04154-115">-AsJob</span></span>
<span data-ttu-id="04154-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="04154-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="04154-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04154-117">-DefaultProfile</span></span>
<span data-ttu-id="04154-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="04154-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04154-119">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="04154-119">-EndIpAddress</span></span>
<span data-ttu-id="04154-120">Indirizzo IP finale della regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="04154-120">The end IP address of the firewall rule.</span></span>
<span data-ttu-id="04154-121">Deve essere in formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="04154-121">Must be IPv4 format.</span></span>
<span data-ttu-id="04154-122">Deve essere maggiore o uguale a startIpAddress.</span><span class="sxs-lookup"><span data-stu-id="04154-122">Must be greater than or equal to startIpAddress.</span></span>

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

### <span data-ttu-id="04154-123">-Name</span><span class="sxs-lookup"><span data-stu-id="04154-123">-Name</span></span>
<span data-ttu-id="04154-124">Nome della regola firerwall per l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="04154-124">The firerwall rule name for the workspace.</span></span>

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

### <span data-ttu-id="04154-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04154-125">-ResourceGroupName</span></span>
<span data-ttu-id="04154-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="04154-126">Resource group name.</span></span>

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

### <span data-ttu-id="04154-127">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="04154-127">-StartIpAddress</span></span>
<span data-ttu-id="04154-128">Indirizzo IP iniziale della regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="04154-128">The start IP address of the firewall rule.</span></span>
<span data-ttu-id="04154-129">Deve essere in formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="04154-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="04154-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="04154-130">-WorkspaceName</span></span>
<span data-ttu-id="04154-131">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="04154-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="04154-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="04154-132">-WorkspaceObject</span></span>
<span data-ttu-id="04154-133">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="04154-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="04154-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="04154-134">-Confirm</span></span>
<span data-ttu-id="04154-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04154-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04154-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04154-136">-WhatIf</span></span>
<span data-ttu-id="04154-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="04154-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04154-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="04154-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04154-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04154-139">CommonParameters</span></span>
<span data-ttu-id="04154-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04154-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04154-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="04154-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04154-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="04154-142">INPUTS</span></span>

### <span data-ttu-id="04154-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="04154-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="04154-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="04154-144">OUTPUTS</span></span>

### <span data-ttu-id="04154-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="04154-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="04154-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="04154-146">NOTES</span></span>

## <span data-ttu-id="04154-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="04154-147">RELATED LINKS</span></span>
