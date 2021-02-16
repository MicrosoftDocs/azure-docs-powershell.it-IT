---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseFirewallRule.md
ms.openlocfilehash: 22a7bb4c135a4424aa27a76f9e13ba14f21ca572
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209058"
---
# <span data-ttu-id="796e2-101">Get-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="796e2-101">Get-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="796e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="796e2-102">SYNOPSIS</span></span>
<span data-ttu-id="796e2-103">Ottiene una regola del firewall synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="796e2-103">Gets a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="796e2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="796e2-104">SYNTAX</span></span>

### <span data-ttu-id="796e2-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="796e2-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="796e2-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="796e2-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseFirewallRule -WorkSpaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="796e2-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="796e2-107">DESCRIPTION</span></span>
<span data-ttu-id="796e2-108">Il cmdlet **Get-AzSynapseFirewallRule** ottiene una regola firewall di Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="796e2-108">The **Get-AzSynapseFirewallRule** cmdlet gets a Azure Synapse Analytics Firewall Rule.</span></span>
<span data-ttu-id="796e2-109">Se non si specifica un nome di regola, questo cmdlet ottiene tutte le regole.</span><span class="sxs-lookup"><span data-stu-id="796e2-109">If you do not specify a rule name, this cmdlet gets all rules.</span></span>

## <span data-ttu-id="796e2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="796e2-110">EXAMPLES</span></span>

### <span data-ttu-id="796e2-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="796e2-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="796e2-112">Questo comando recupera tutte le regole del firewall in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="796e2-112">This command gets all firewall rules under a workspace.</span></span>

### <span data-ttu-id="796e2-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="796e2-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule
```

<span data-ttu-id="796e2-114">Questo comando recupera la regola del firewall nell'area di lavoro ContosoWorkspace con il nome ContosoFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="796e2-114">This command gets the firewall rule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="796e2-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="796e2-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseFirewallRule
```

<span data-ttu-id="796e2-116">Questo comando recupera tutte le regole del firewall in un'area di lavoro tramite una pipeline.</span><span class="sxs-lookup"><span data-stu-id="796e2-116">This command gets all firewall rules under a workspace through pipeline.</span></span>

## <span data-ttu-id="796e2-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="796e2-117">PARAMETERS</span></span>

### <span data-ttu-id="796e2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="796e2-118">-DefaultProfile</span></span>
<span data-ttu-id="796e2-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="796e2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="796e2-120">-Name</span><span class="sxs-lookup"><span data-stu-id="796e2-120">-Name</span></span>
<span data-ttu-id="796e2-121">Nome della regola firerwall per l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="796e2-121">The firerwall rule name for the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FirewallRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="796e2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="796e2-122">-ResourceGroupName</span></span>
<span data-ttu-id="796e2-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="796e2-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="796e2-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="796e2-124">-WorkspaceName</span></span>
<span data-ttu-id="796e2-125">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="796e2-125">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="796e2-126">-WorkSpaceObject</span><span class="sxs-lookup"><span data-stu-id="796e2-126">-WorkSpaceObject</span></span>
<span data-ttu-id="796e2-127">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="796e2-127">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="796e2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="796e2-128">CommonParameters</span></span>
<span data-ttu-id="796e2-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="796e2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="796e2-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="796e2-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="796e2-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="796e2-131">INPUTS</span></span>

### <span data-ttu-id="796e2-132">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="796e2-132">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="796e2-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="796e2-133">OUTPUTS</span></span>

### <span data-ttu-id="796e2-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="796e2-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="796e2-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="796e2-135">NOTES</span></span>

## <span data-ttu-id="796e2-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="796e2-136">RELATED LINKS</span></span>
