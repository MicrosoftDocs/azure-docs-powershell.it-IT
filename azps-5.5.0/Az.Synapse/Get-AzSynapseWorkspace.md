---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseWorkspace.md
ms.openlocfilehash: d95892068b92745fa09419d83d3bdb001f0bdead
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190606"
---
# <span data-ttu-id="ea173-101">Get-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ea173-101">Get-AzSynapseWorkspace</span></span>

## <span data-ttu-id="ea173-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea173-102">SYNOPSIS</span></span>
<span data-ttu-id="ea173-103">Ottiene un'area di lavoro Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="ea173-103">Gets a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="ea173-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ea173-104">SYNTAX</span></span>

### <span data-ttu-id="ea173-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ea173-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseWorkspace [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea173-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea173-106">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseWorkspace -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea173-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ea173-107">DESCRIPTION</span></span>
<span data-ttu-id="ea173-108">Il cmdlet **Get-AzSynapseWorkspace** ottiene informazioni su un'area di lavoro di Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="ea173-108">The **Get-AzSynapseWorkspace** cmdlet gets information about an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="ea173-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ea173-109">EXAMPLES</span></span>

### <span data-ttu-id="ea173-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ea173-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace
```

<span data-ttu-id="ea173-111">Questo comando recupera tutte le aree di lavoro di Azure Synapse Analytics nella sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="ea173-111">This command gets all the Azure Synapse Analytics workspaces under the current subscription.</span></span>

### <span data-ttu-id="ea173-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ea173-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup
```

<span data-ttu-id="ea173-113">Questo comando recupera tutte le aree di lavoro di Azure Synapse Analytics nella sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="ea173-113">This command gets all the Azure Synapse Analytics workspaces under the current subscription.</span></span>

### <span data-ttu-id="ea173-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="ea173-114">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="ea173-115">Questo comando recupera l'area di lavoro Azure Synapse Analytics con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="ea173-115">This command gets the Azure Synapse Analytics workspace with the specified name.</span></span>

### <span data-ttu-id="ea173-116">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="ea173-116">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace
```

<span data-ttu-id="ea173-117">Questo comando recupera l'area di lavoro Azure Synapse Analytics con l'ID risorsa specificato.</span><span class="sxs-lookup"><span data-stu-id="ea173-117">This command gets the Azure Synapse Analytics workspace with the specified resource ID.</span></span>

## <span data-ttu-id="ea173-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea173-118">PARAMETERS</span></span>

### <span data-ttu-id="ea173-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea173-119">-DefaultProfile</span></span>
<span data-ttu-id="ea173-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ea173-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea173-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ea173-121">-Name</span></span>
<span data-ttu-id="ea173-122">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="ea173-122">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: WorkspaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea173-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea173-123">-ResourceGroupName</span></span>
<span data-ttu-id="ea173-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ea173-124">Resource group name.</span></span>

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

### <span data-ttu-id="ea173-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea173-125">-ResourceId</span></span>
<span data-ttu-id="ea173-126">Identificatore di risorsa dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="ea173-126">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea173-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea173-127">CommonParameters</span></span>
<span data-ttu-id="ea173-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea173-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea173-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ea173-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea173-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="ea173-130">INPUTS</span></span>

### <span data-ttu-id="ea173-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ea173-131">None</span></span>

## <span data-ttu-id="ea173-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ea173-132">OUTPUTS</span></span>

### <span data-ttu-id="ea173-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ea173-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="ea173-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="ea173-134">NOTES</span></span>

## <span data-ttu-id="ea173-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ea173-135">RELATED LINKS</span></span>
