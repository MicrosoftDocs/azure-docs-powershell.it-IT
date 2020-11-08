---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
ms.openlocfilehash: 6304e730e6b3b0a4f8edc0f42fc024852acbfc12
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193106"
---
# <span data-ttu-id="f1874-101">Test-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="f1874-101">Test-AzSynapseSparkPool</span></span>

## <span data-ttu-id="f1874-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f1874-102">SYNOPSIS</span></span>
<span data-ttu-id="f1874-103">Verifica l'esistenza di un pool di scintille di analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="f1874-103">Checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="f1874-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f1874-104">SYNTAX</span></span>

### <span data-ttu-id="f1874-105">TestByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f1874-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1874-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1874-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1874-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1874-107">DESCRIPTION</span></span>
<span data-ttu-id="f1874-108">Il cmdlet **test-AzSynapseSparkPool** controlla l'esistenza di un pool di Spark di analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="f1874-108">The **Test-AzSynapseSparkPool** cmdlet checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="f1874-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f1874-109">EXAMPLES</span></span>

### <span data-ttu-id="f1874-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f1874-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="f1874-111">Questo comando controlla l'esistenza del pool di scintille specificato.</span><span class="sxs-lookup"><span data-stu-id="f1874-111">This command checks the existence of the specified Spark pool.</span></span>

## <span data-ttu-id="f1874-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f1874-112">PARAMETERS</span></span>

### <span data-ttu-id="f1874-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1874-113">-DefaultProfile</span></span>
<span data-ttu-id="f1874-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f1874-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1874-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="f1874-115">-Name</span></span>
<span data-ttu-id="f1874-116">Nome del pool di scintille sinapsi.</span><span class="sxs-lookup"><span data-stu-id="f1874-116">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="f1874-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1874-117">-ResourceGroupName</span></span>
<span data-ttu-id="f1874-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f1874-118">Resource group name.</span></span>

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

### <span data-ttu-id="f1874-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f1874-119">-WorkspaceName</span></span>
<span data-ttu-id="f1874-120">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="f1874-120">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="f1874-121">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f1874-121">-WorkspaceObject</span></span>
<span data-ttu-id="f1874-122">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="f1874-122">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f1874-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1874-123">CommonParameters</span></span>
<span data-ttu-id="f1874-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1874-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1874-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1874-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1874-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f1874-126">INPUTS</span></span>

### <span data-ttu-id="f1874-127">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f1874-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="f1874-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f1874-128">OUTPUTS</span></span>

### <span data-ttu-id="f1874-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="f1874-129">System.Object</span></span>
## <span data-ttu-id="f1874-130">Note</span><span class="sxs-lookup"><span data-stu-id="f1874-130">NOTES</span></span>

## <span data-ttu-id="f1874-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f1874-131">RELATED LINKS</span></span>
