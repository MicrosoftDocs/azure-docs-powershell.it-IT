---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/test-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlPool.md
ms.openlocfilehash: d932a875957f1649976966a9f2e115e93dfea351
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011230"
---
# <span data-ttu-id="e975b-101">Test-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="e975b-101">Test-AzSynapseSqlPool</span></span>

## <span data-ttu-id="e975b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e975b-102">SYNOPSIS</span></span>
<span data-ttu-id="e975b-103">Verifica la presenza di un pool di SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="e975b-103">Checks for the existence of a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="e975b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e975b-104">SYNTAX</span></span>

### <span data-ttu-id="e975b-105">TestByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e975b-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e975b-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e975b-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e975b-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e975b-107">DESCRIPTION</span></span>
<span data-ttu-id="e975b-108">Il cmdlet **Test-AzSynapseSqlPool** verifica l'esistenza di un SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="e975b-108">The **Test-AzSynapseSqlPool** cmdlet checks for the existence of a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="e975b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e975b-109">EXAMPLES</span></span>

### <span data-ttu-id="e975b-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e975b-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="e975b-111">Questo comando verifica l'esistenza del pool SQL specificato.</span><span class="sxs-lookup"><span data-stu-id="e975b-111">This command checks the existence of the specified SQL pool.</span></span>

## <span data-ttu-id="e975b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e975b-112">PARAMETERS</span></span>

### <span data-ttu-id="e975b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e975b-113">-DefaultProfile</span></span>
<span data-ttu-id="e975b-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e975b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e975b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e975b-115">-Name</span></span>
<span data-ttu-id="e975b-116">Nome del pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="e975b-116">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e975b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e975b-117">-ResourceGroupName</span></span>
<span data-ttu-id="e975b-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e975b-118">Resource group name.</span></span>

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

### <span data-ttu-id="e975b-119">-Version</span><span class="sxs-lookup"><span data-stu-id="e975b-119">-Version</span></span>
<span data-ttu-id="e975b-120">Versione di Synapse SQL pool.</span><span class="sxs-lookup"><span data-stu-id="e975b-120">Version of Synapse SQL pool.</span></span> <span data-ttu-id="e975b-121">Ad esempio, 2 o 3.</span><span class="sxs-lookup"><span data-stu-id="e975b-121">For example, 2 or 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e975b-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e975b-122">-WorkspaceName</span></span>
<span data-ttu-id="e975b-123">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="e975b-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e975b-124">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e975b-124">-WorkspaceObject</span></span>
<span data-ttu-id="e975b-125">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="e975b-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e975b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e975b-126">CommonParameters</span></span>
<span data-ttu-id="e975b-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e975b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e975b-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e975b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e975b-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="e975b-129">INPUTS</span></span>

### <span data-ttu-id="e975b-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e975b-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="e975b-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e975b-131">OUTPUTS</span></span>

### <span data-ttu-id="e975b-132">System.Object</span><span class="sxs-lookup"><span data-stu-id="e975b-132">System.Object</span></span>
## <span data-ttu-id="e975b-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="e975b-133">NOTES</span></span>

## <span data-ttu-id="e975b-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e975b-134">RELATED LINKS</span></span>
