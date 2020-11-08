---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseFirewallRule.md
ms.openlocfilehash: 22a7bb4c135a4424aa27a76f9e13ba14f21ca572
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199960"
---
# <span data-ttu-id="8832d-101">Get-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8832d-101">Get-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="8832d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8832d-102">SYNOPSIS</span></span>
<span data-ttu-id="8832d-103">Ottiene una regola del firewall di analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="8832d-103">Gets a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="8832d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8832d-104">SYNTAX</span></span>

### <span data-ttu-id="8832d-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8832d-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8832d-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8832d-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseFirewallRule -WorkSpaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8832d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8832d-107">DESCRIPTION</span></span>
<span data-ttu-id="8832d-108">Il cmdlet **Get-AzSynapseFirewallRule** ottiene una regola del firewall di analisi di Azure sinapsi.</span><span class="sxs-lookup"><span data-stu-id="8832d-108">The **Get-AzSynapseFirewallRule** cmdlet gets a Azure Synapse Analytics Firewall Rule.</span></span>
<span data-ttu-id="8832d-109">Se non specifichi un nome di regola, questo cmdlet ottiene tutte le regole.</span><span class="sxs-lookup"><span data-stu-id="8832d-109">If you do not specify a rule name, this cmdlet gets all rules.</span></span>

## <span data-ttu-id="8832d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8832d-110">EXAMPLES</span></span>

### <span data-ttu-id="8832d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8832d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="8832d-112">Questo comando consente di ottenere tutte le regole del firewall in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="8832d-112">This command gets all firewall rules under a workspace.</span></span>

### <span data-ttu-id="8832d-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="8832d-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule
```

<span data-ttu-id="8832d-114">Questo comando consente di ottenere la regola del firewall in area di lavoro ContosoWorkspace con nome ContosoFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="8832d-114">This command gets the firewall rule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="8832d-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="8832d-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseFirewallRule
```

<span data-ttu-id="8832d-116">Questo comando consente di ottenere tutte le regole del firewall in un'area di lavoro tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="8832d-116">This command gets all firewall rules under a workspace through pipeline.</span></span>

## <span data-ttu-id="8832d-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8832d-117">PARAMETERS</span></span>

### <span data-ttu-id="8832d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8832d-118">-DefaultProfile</span></span>
<span data-ttu-id="8832d-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8832d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8832d-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="8832d-120">-Name</span></span>
<span data-ttu-id="8832d-121">Il nome della regola firerwall per l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="8832d-121">The firerwall rule name for the workspace.</span></span>

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

### <span data-ttu-id="8832d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8832d-122">-ResourceGroupName</span></span>
<span data-ttu-id="8832d-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8832d-123">Resource group name.</span></span>

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

### <span data-ttu-id="8832d-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8832d-124">-WorkspaceName</span></span>
<span data-ttu-id="8832d-125">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="8832d-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="8832d-126">-WorkSpaceObject</span><span class="sxs-lookup"><span data-stu-id="8832d-126">-WorkSpaceObject</span></span>
<span data-ttu-id="8832d-127">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="8832d-127">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="8832d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8832d-128">CommonParameters</span></span>
<span data-ttu-id="8832d-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8832d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8832d-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8832d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8832d-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8832d-131">INPUTS</span></span>

### <span data-ttu-id="8832d-132">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="8832d-132">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="8832d-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8832d-133">OUTPUTS</span></span>

### <span data-ttu-id="8832d-134">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8832d-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="8832d-135">Note</span><span class="sxs-lookup"><span data-stu-id="8832d-135">NOTES</span></span>

## <span data-ttu-id="8832d-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8832d-136">RELATED LINKS</span></span>