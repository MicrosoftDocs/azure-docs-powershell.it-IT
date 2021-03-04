---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/test-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
ms.openlocfilehash: cb7abd3c54d263ae9516344237588ecf9a1297ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011246"
---
# <span data-ttu-id="57d93-101">Test-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="57d93-101">Test-AzSynapseSparkPool</span></span>

## <span data-ttu-id="57d93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57d93-102">SYNOPSIS</span></span>
<span data-ttu-id="57d93-103">Verifica l'esistenza di un pool Spark spark di Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="57d93-103">Checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="57d93-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="57d93-104">SYNTAX</span></span>

### <span data-ttu-id="57d93-105">TestByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="57d93-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57d93-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="57d93-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57d93-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="57d93-107">DESCRIPTION</span></span>
<span data-ttu-id="57d93-108">Il cmdlet **Test-AzSynapseSparkPool** verifica l'esistenza di un pool Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="57d93-108">The **Test-AzSynapseSparkPool** cmdlet checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="57d93-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="57d93-109">EXAMPLES</span></span>

### <span data-ttu-id="57d93-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="57d93-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="57d93-111">Questo comando verifica l'esistenza del pool spark specificato.</span><span class="sxs-lookup"><span data-stu-id="57d93-111">This command checks the existence of the specified Spark pool.</span></span>

## <span data-ttu-id="57d93-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57d93-112">PARAMETERS</span></span>

### <span data-ttu-id="57d93-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57d93-113">-DefaultProfile</span></span>
<span data-ttu-id="57d93-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="57d93-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57d93-115">-Name</span><span class="sxs-lookup"><span data-stu-id="57d93-115">-Name</span></span>
<span data-ttu-id="57d93-116">Nome del pool Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="57d93-116">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57d93-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57d93-117">-ResourceGroupName</span></span>
<span data-ttu-id="57d93-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="57d93-118">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57d93-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="57d93-119">-WorkspaceName</span></span>
<span data-ttu-id="57d93-120">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="57d93-120">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57d93-121">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="57d93-121">-WorkspaceObject</span></span>
<span data-ttu-id="57d93-122">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="57d93-122">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: TestByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57d93-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57d93-123">CommonParameters</span></span>
<span data-ttu-id="57d93-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57d93-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57d93-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="57d93-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57d93-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="57d93-126">INPUTS</span></span>

### <span data-ttu-id="57d93-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="57d93-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="57d93-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="57d93-128">OUTPUTS</span></span>

### <span data-ttu-id="57d93-129">System.Object</span><span class="sxs-lookup"><span data-stu-id="57d93-129">System.Object</span></span>
## <span data-ttu-id="57d93-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="57d93-130">NOTES</span></span>

## <span data-ttu-id="57d93-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="57d93-131">RELATED LINKS</span></span>
