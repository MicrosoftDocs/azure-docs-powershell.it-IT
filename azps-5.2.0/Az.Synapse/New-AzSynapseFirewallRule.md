---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseFirewallRule.md
ms.openlocfilehash: b4579d01ed6dd5a7d742cbb82afb424151579772
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360891"
---
# <span data-ttu-id="e544f-101">New-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e544f-101">New-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="e544f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e544f-102">SYNOPSIS</span></span>
<span data-ttu-id="e544f-103">Crea una regola del firewall di analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="e544f-103">Creates a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="e544f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e544f-104">SYNTAX</span></span>

### <span data-ttu-id="e544f-105">CreateByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e544f-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -StartIpAddress <String> -EndIpAddress <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e544f-106">CreateByNameAllowAllIpParameterSet</span><span class="sxs-lookup"><span data-stu-id="e544f-106">CreateByNameAllowAllIpParameterSet</span></span>
```
New-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> [-AllowAllAzureIP] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e544f-107">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e544f-107">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> -Name <String> -StartIpAddress <String>
 -EndIpAddress <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e544f-108">CreateByParentObjectAllowAllIpParameterSet</span><span class="sxs-lookup"><span data-stu-id="e544f-108">CreateByParentObjectAllowAllIpParameterSet</span></span>
```
New-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> [-AllowAllAzureIP] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e544f-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e544f-109">DESCRIPTION</span></span>
<span data-ttu-id="e544f-110">Il cmdlet **New-AzSynapseFirewallRule** crea una regola del firewall di analisi di Azure sinapsi.</span><span class="sxs-lookup"><span data-stu-id="e544f-110">The **New-AzSynapseFirewallRule** cmdlet creates an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="e544f-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e544f-111">EXAMPLES</span></span>

### <span data-ttu-id="e544f-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e544f-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseFirewallRule -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAddress "255.255.255.255"
```

<span data-ttu-id="e544f-113">Questo comando crea la regola del firewall denominata ContosoFirewallRule in area di lavoro ContosoWorkspace con nome ContosoFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="e544f-113">This command creates firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="e544f-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e544f-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseFirewallRule -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAddress "255.255.255.255"
```

<span data-ttu-id="e544f-115">Questo comando crea la regola del firewall denominata ContosoFirewallRule in un'area di lavoro tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="e544f-115">This command creates firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

### <span data-ttu-id="e544f-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="e544f-116">Example 3</span></span>
```powershell
PS C:\> New-AzSynapseFirewallRule -WorkspaceName ContosoWorkspace -AllowAllAzureIP
```

<span data-ttu-id="e544f-117">Questo comando crea la regola del firewall che consente a tutti gli IPS di Azure in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="e544f-117">This command creates firewall rule that allow all azure ips under a workspace.</span></span>

## <span data-ttu-id="e544f-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e544f-118">PARAMETERS</span></span>

### <span data-ttu-id="e544f-119">-AllowAllAzureIP</span><span class="sxs-lookup"><span data-stu-id="e544f-119">-AllowAllAzureIP</span></span>
<span data-ttu-id="e544f-120">Crea una regola speciale del firewall che consente a tutti gli IP di Azure di avere accesso.</span><span class="sxs-lookup"><span data-stu-id="e544f-120">Creates a special firewall rule that permits all Azure IPs to have access.</span></span>

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

### <span data-ttu-id="e544f-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e544f-121">-AsJob</span></span>
<span data-ttu-id="e544f-122">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e544f-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e544f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e544f-123">-DefaultProfile</span></span>
<span data-ttu-id="e544f-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e544f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e544f-125">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="e544f-125">-EndIpAddress</span></span>
<span data-ttu-id="e544f-126">Indirizzo IP finale della regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="e544f-126">The end IP address of the firewall rule.</span></span>
<span data-ttu-id="e544f-127">Deve essere formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="e544f-127">Must be IPv4 format.</span></span>
<span data-ttu-id="e544f-128">Deve essere maggiore o uguale a startIpAddress.</span><span class="sxs-lookup"><span data-stu-id="e544f-128">Must be greater than or equal to startIpAddress.</span></span>

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

### <span data-ttu-id="e544f-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="e544f-129">-Name</span></span>
<span data-ttu-id="e544f-130">Il nome della regola firerwall per l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="e544f-130">The firerwall rule name for the workspace.</span></span>

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

### <span data-ttu-id="e544f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e544f-131">-ResourceGroupName</span></span>
<span data-ttu-id="e544f-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e544f-132">Resource group name.</span></span>

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

### <span data-ttu-id="e544f-133">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="e544f-133">-StartIpAddress</span></span>
<span data-ttu-id="e544f-134">Indirizzo IP iniziale della regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="e544f-134">The start IP address of the firewall rule.</span></span>
<span data-ttu-id="e544f-135">Deve essere formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="e544f-135">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="e544f-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e544f-136">-WorkspaceName</span></span>
<span data-ttu-id="e544f-137">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="e544f-137">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e544f-138">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e544f-138">-WorkspaceObject</span></span>
<span data-ttu-id="e544f-139">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="e544f-139">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e544f-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e544f-140">-Confirm</span></span>
<span data-ttu-id="e544f-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e544f-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e544f-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e544f-142">-WhatIf</span></span>
<span data-ttu-id="e544f-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e544f-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e544f-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e544f-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e544f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e544f-145">CommonParameters</span></span>
<span data-ttu-id="e544f-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e544f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e544f-147">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e544f-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e544f-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e544f-148">INPUTS</span></span>

### <span data-ttu-id="e544f-149">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e544f-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="e544f-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e544f-150">OUTPUTS</span></span>

### <span data-ttu-id="e544f-151">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e544f-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="e544f-152">Note</span><span class="sxs-lookup"><span data-stu-id="e544f-152">NOTES</span></span>

## <span data-ttu-id="e544f-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e544f-153">RELATED LINKS</span></span>
