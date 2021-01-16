---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksNodePool.md
ms.openlocfilehash: 5c690b377d658e3ebc4eddaf49d546efd503a01c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354235"
---
# <span data-ttu-id="b67ff-101">Get-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="b67ff-101">Get-AzAksNodePool</span></span>

## <span data-ttu-id="b67ff-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b67ff-102">SYNOPSIS</span></span>
<span data-ttu-id="b67ff-103">Creare un pool di note nel cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="b67ff-103">Create note pool in specified cluster.</span></span>

## <span data-ttu-id="b67ff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b67ff-104">SYNTAX</span></span>

### <span data-ttu-id="b67ff-105">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b67ff-105">NameParameterSet (Default)</span></span>
```
Get-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b67ff-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b67ff-106">IdParameterSet</span></span>
```
Get-AzAksNodePool -Id <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b67ff-107">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b67ff-107">ParentObjectParameterSet</span></span>
```
Get-AzAksNodePool -ClusterObject <PSKubernetesCluster> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b67ff-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b67ff-108">DESCRIPTION</span></span>
<span data-ttu-id="b67ff-109">Creare un pool di note nel cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="b67ff-109">Create note pool in specified cluster.</span></span>

## <span data-ttu-id="b67ff-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b67ff-110">EXAMPLES</span></span>

### <span data-ttu-id="b67ff-111">Ottenere tutti i pool di nodi all'interno di un cluster specificato</span><span class="sxs-lookup"><span data-stu-id="b67ff-111">Get all node pools within specified cluster</span></span>
```powershell
PS C:\> Get-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster
```

## <span data-ttu-id="b67ff-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b67ff-112">PARAMETERS</span></span>

### <span data-ttu-id="b67ff-113">-Clustername</span><span class="sxs-lookup"><span data-stu-id="b67ff-113">-ClusterName</span></span>
<span data-ttu-id="b67ff-114">Nome della risorsa del cluster gestito.</span><span class="sxs-lookup"><span data-stu-id="b67ff-114">The name of the managed cluster resource.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b67ff-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="b67ff-115">-ClusterObject</span></span>
<span data-ttu-id="b67ff-116">Oggetto cluster.</span><span class="sxs-lookup"><span data-stu-id="b67ff-116">The cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b67ff-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b67ff-117">-DefaultProfile</span></span>
<span data-ttu-id="b67ff-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b67ff-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b67ff-119">-ID</span><span class="sxs-lookup"><span data-stu-id="b67ff-119">-Id</span></span>
<span data-ttu-id="b67ff-120">ID di un pool di nodi nel cluster managed Kubernetes</span><span class="sxs-lookup"><span data-stu-id="b67ff-120">Id of an node pool in managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b67ff-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="b67ff-121">-Name</span></span>
<span data-ttu-id="b67ff-122">Nome del pool di nodi.</span><span class="sxs-lookup"><span data-stu-id="b67ff-122">The name of the node pool.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b67ff-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b67ff-123">-ResourceGroupName</span></span>
<span data-ttu-id="b67ff-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b67ff-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b67ff-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b67ff-125">CommonParameters</span></span>
<span data-ttu-id="b67ff-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b67ff-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b67ff-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b67ff-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b67ff-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b67ff-128">INPUTS</span></span>

### <span data-ttu-id="b67ff-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b67ff-129">System.String</span></span>

## <span data-ttu-id="b67ff-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b67ff-130">OUTPUTS</span></span>

### <span data-ttu-id="b67ff-131">Microsoft. Azure. Commands. AKS. Models. PSNodePool</span><span class="sxs-lookup"><span data-stu-id="b67ff-131">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="b67ff-132">Note</span><span class="sxs-lookup"><span data-stu-id="b67ff-132">NOTES</span></span>

## <span data-ttu-id="b67ff-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b67ff-133">RELATED LINKS</span></span>
