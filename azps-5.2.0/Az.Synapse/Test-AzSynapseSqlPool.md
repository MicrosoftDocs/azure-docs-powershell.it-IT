---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlPool.md
ms.openlocfilehash: d07ec757fd5ab589de6234caac23992d6ff320fe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344791"
---
# <span data-ttu-id="8e97f-101">Test-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="8e97f-101">Test-AzSynapseSqlPool</span></span>

## <span data-ttu-id="8e97f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8e97f-102">SYNOPSIS</span></span>
<span data-ttu-id="8e97f-103">Verifica l'esistenza di un pool SQL di analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="8e97f-103">Checks for the existence of a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="8e97f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8e97f-104">SYNTAX</span></span>

### <span data-ttu-id="8e97f-105">TestByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8e97f-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e97f-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e97f-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e97f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8e97f-107">DESCRIPTION</span></span>
<span data-ttu-id="8e97f-108">Il cmdlet **test-AzSynapseSqlPool** controlla l'esistenza di un pool di analisi delle sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="8e97f-108">The **Test-AzSynapseSqlPool** cmdlet checks for the existence of a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="8e97f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8e97f-109">EXAMPLES</span></span>

### <span data-ttu-id="8e97f-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8e97f-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="8e97f-111">Questo comando controlla l'esistenza del pool SQL specificato.</span><span class="sxs-lookup"><span data-stu-id="8e97f-111">This command checks the existence of the specified SQL pool.</span></span>

## <span data-ttu-id="8e97f-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8e97f-112">PARAMETERS</span></span>

### <span data-ttu-id="8e97f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e97f-113">-DefaultProfile</span></span>
<span data-ttu-id="8e97f-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8e97f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e97f-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="8e97f-115">-Name</span></span>
<span data-ttu-id="8e97f-116">Nome del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="8e97f-116">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="8e97f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e97f-117">-ResourceGroupName</span></span>
<span data-ttu-id="8e97f-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8e97f-118">Resource group name.</span></span>

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

### <span data-ttu-id="8e97f-119">-Versione</span><span class="sxs-lookup"><span data-stu-id="8e97f-119">-Version</span></span>
<span data-ttu-id="8e97f-120">Versione del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="8e97f-120">Version of Synapse SQL pool.</span></span> <span data-ttu-id="8e97f-121">Ad esempio, 2 o 3.</span><span class="sxs-lookup"><span data-stu-id="8e97f-121">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="8e97f-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8e97f-122">-WorkspaceName</span></span>
<span data-ttu-id="8e97f-123">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="8e97f-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="8e97f-124">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="8e97f-124">-WorkspaceObject</span></span>
<span data-ttu-id="8e97f-125">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="8e97f-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="8e97f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e97f-126">CommonParameters</span></span>
<span data-ttu-id="8e97f-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e97f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e97f-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e97f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e97f-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8e97f-129">INPUTS</span></span>

### <span data-ttu-id="8e97f-130">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="8e97f-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="8e97f-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8e97f-131">OUTPUTS</span></span>

### <span data-ttu-id="8e97f-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="8e97f-132">System.Object</span></span>
## <span data-ttu-id="8e97f-133">Note</span><span class="sxs-lookup"><span data-stu-id="8e97f-133">NOTES</span></span>

## <span data-ttu-id="8e97f-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8e97f-134">RELATED LINKS</span></span>
