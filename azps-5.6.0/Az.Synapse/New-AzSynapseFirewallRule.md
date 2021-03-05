---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/new-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseFirewallRule.md
ms.openlocfilehash: e630bdba87f345229ffe18e4cf2011f82f78dc73
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976093"
---
# <span data-ttu-id="3ebe0-101">New-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3ebe0-101">New-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="3ebe0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ebe0-102">SYNOPSIS</span></span>
<span data-ttu-id="3ebe0-103">Crea una regola del firewall di Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="3ebe0-103">Creates a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="3ebe0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3ebe0-104">SYNTAX</span></span>

### <span data-ttu-id="3ebe0-105">CreateByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3ebe0-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -StartIpAddress <String> -EndIpAddress <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ebe0-106">CreateByNameAllowAllIpParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ebe0-106">CreateByNameAllowAllIpParameterSet</span></span>
```
New-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> [-AllowAllAzureIP] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ebe0-107">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ebe0-107">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> -Name <String> -StartIpAddress <String>
 -EndIpAddress <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3ebe0-108">CreateByParentObjectAllowAllIpParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ebe0-108">CreateByParentObjectAllowAllIpParameterSet</span></span>
```
New-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> [-AllowAllAzureIP] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ebe0-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3ebe0-109">DESCRIPTION</span></span>
<span data-ttu-id="3ebe0-110">Il cmdlet **New-AzSynapseFirewallRule** crea una regola firewall di Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="3ebe0-110">The **New-AzSynapseFirewallRule** cmdlet creates an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="3ebe0-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3ebe0-111">EXAMPLES</span></span>

### <span data-ttu-id="3ebe0-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3ebe0-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseFirewallRule -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAddress "255.255.255.255"
```

<span data-ttu-id="3ebe0-113">Questo comando crea una regola del firewall denominata ContosoFirewallRule nell'area di lavoro ContosoWorkspace con il nome ContosoFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="3ebe0-113">This command creates firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="3ebe0-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3ebe0-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseFirewallRule -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAddress "255.255.255.255"
```

<span data-ttu-id="3ebe0-115">Questo comando crea una regola del firewall denominata ContosoFirewallRule in un'area di lavoro tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="3ebe0-115">This command creates firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

### <span data-ttu-id="3ebe0-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="3ebe0-116">Example 3</span></span>
```powershell
PS C:\> New-AzSynapseFirewallRule -WorkspaceName ContosoWorkspace -AllowAllAzureIP
```

<span data-ttu-id="3ebe0-117">Questo comando crea una regola del firewall che consente tutti gli ip azure in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="3ebe0-117">This command creates firewall rule that allow all azure ips under a workspace.</span></span>

## <span data-ttu-id="3ebe0-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ebe0-118">PARAMETERS</span></span>

### <span data-ttu-id="3ebe0-119">-AllowAllAzureIP</span><span class="sxs-lookup"><span data-stu-id="3ebe0-119">-AllowAllAzureIP</span></span>
<span data-ttu-id="3ebe0-120">Crea una regola del firewall speciale che consente l'accesso a tutti gli IP di Azure.</span><span class="sxs-lookup"><span data-stu-id="3ebe0-120">Creates a special firewall rule that permits all Azure IPs to have access.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateByNameAllowAllIpParameterSet, CreateByParentObjectAllowAllIpParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ebe0-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3ebe0-121">-AsJob</span></span>
<span data-ttu-id="3ebe0-122">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="3ebe0-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3ebe0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ebe0-123">-DefaultProfile</span></span>
<span data-ttu-id="3ebe0-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3ebe0-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ebe0-125">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="3ebe0-125">-EndIpAddress</span></span>
<span data-ttu-id="3ebe0-126">Indirizzo IP finale della regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="3ebe0-126">The end IP address of the firewall rule.</span></span>
<span data-ttu-id="3ebe0-127">Deve essere in formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="3ebe0-127">Must be IPv4 format.</span></span>
<span data-ttu-id="3ebe0-128">Deve essere maggiore o uguale a startIpAddress.</span><span class="sxs-lookup"><span data-stu-id="3ebe0-128">Must be greater than or equal to startIpAddress.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ebe0-129">-Name</span><span class="sxs-lookup"><span data-stu-id="3ebe0-129">-Name</span></span>
<span data-ttu-id="3ebe0-130">Nome della regola firerwall per l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="3ebe0-130">The firerwall rule name for the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ebe0-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ebe0-131">-ResourceGroupName</span></span>
<span data-ttu-id="3ebe0-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3ebe0-132">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByNameAllowAllIpParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ebe0-133">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="3ebe0-133">-StartIpAddress</span></span>
<span data-ttu-id="3ebe0-134">Indirizzo IP iniziale della regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="3ebe0-134">The start IP address of the firewall rule.</span></span>
<span data-ttu-id="3ebe0-135">Deve essere in formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="3ebe0-135">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ebe0-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3ebe0-136">-WorkspaceName</span></span>
<span data-ttu-id="3ebe0-137">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="3ebe0-137">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByNameAllowAllIpParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ebe0-138">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3ebe0-138">-WorkspaceObject</span></span>
<span data-ttu-id="3ebe0-139">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="3ebe0-139">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateByParentObjectParameterSet, CreateByParentObjectAllowAllIpParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ebe0-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ebe0-140">-Confirm</span></span>
<span data-ttu-id="3ebe0-141">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ebe0-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ebe0-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ebe0-142">-WhatIf</span></span>
<span data-ttu-id="3ebe0-143">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3ebe0-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ebe0-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3ebe0-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ebe0-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ebe0-145">CommonParameters</span></span>
<span data-ttu-id="3ebe0-146">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ebe0-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ebe0-147">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3ebe0-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ebe0-148">INPUT</span><span class="sxs-lookup"><span data-stu-id="3ebe0-148">INPUTS</span></span>

### <span data-ttu-id="3ebe0-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3ebe0-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="3ebe0-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3ebe0-150">OUTPUTS</span></span>

### <span data-ttu-id="3ebe0-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3ebe0-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="3ebe0-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="3ebe0-152">NOTES</span></span>

## <span data-ttu-id="3ebe0-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3ebe0-153">RELATED LINKS</span></span>
