---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksNodePool.md
ms.openlocfilehash: 5c690b377d658e3ebc4eddaf49d546efd503a01c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191371"
---
# <span data-ttu-id="c7429-101">Get-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="c7429-101">Get-AzAksNodePool</span></span>

## <span data-ttu-id="c7429-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c7429-102">SYNOPSIS</span></span>
<span data-ttu-id="c7429-103">Creare un pool di note nel cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="c7429-103">Create note pool in specified cluster.</span></span>

## <span data-ttu-id="c7429-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c7429-104">SYNTAX</span></span>

### <span data-ttu-id="c7429-105">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c7429-105">NameParameterSet (Default)</span></span>
```
Get-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7429-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7429-106">IdParameterSet</span></span>
```
Get-AzAksNodePool -Id <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7429-107">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7429-107">ParentObjectParameterSet</span></span>
```
Get-AzAksNodePool -ClusterObject <PSKubernetesCluster> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7429-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c7429-108">DESCRIPTION</span></span>
<span data-ttu-id="c7429-109">Creare un pool di note nel cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="c7429-109">Create note pool in specified cluster.</span></span>

## <span data-ttu-id="c7429-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c7429-110">EXAMPLES</span></span>

### <span data-ttu-id="c7429-111">Ottenere tutti i pool di nodi all'interno di un cluster specificato</span><span class="sxs-lookup"><span data-stu-id="c7429-111">Get all node pools within specified cluster</span></span>
```powershell
PS C:\> Get-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster
```

## <span data-ttu-id="c7429-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c7429-112">PARAMETERS</span></span>

### <span data-ttu-id="c7429-113">-Clustername</span><span class="sxs-lookup"><span data-stu-id="c7429-113">-ClusterName</span></span>
<span data-ttu-id="c7429-114">Nome della risorsa del cluster gestito.</span><span class="sxs-lookup"><span data-stu-id="c7429-114">The name of the managed cluster resource.</span></span>

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

### <span data-ttu-id="c7429-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="c7429-115">-ClusterObject</span></span>
<span data-ttu-id="c7429-116">Oggetto cluster.</span><span class="sxs-lookup"><span data-stu-id="c7429-116">The cluster object.</span></span>

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

### <span data-ttu-id="c7429-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7429-117">-DefaultProfile</span></span>
<span data-ttu-id="c7429-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c7429-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7429-119">-ID</span><span class="sxs-lookup"><span data-stu-id="c7429-119">-Id</span></span>
<span data-ttu-id="c7429-120">ID di un pool di nodi nel cluster managed Kubernetes</span><span class="sxs-lookup"><span data-stu-id="c7429-120">Id of an node pool in managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="c7429-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="c7429-121">-Name</span></span>
<span data-ttu-id="c7429-122">Nome del pool di nodi.</span><span class="sxs-lookup"><span data-stu-id="c7429-122">The name of the node pool.</span></span>

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

### <span data-ttu-id="c7429-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7429-123">-ResourceGroupName</span></span>
<span data-ttu-id="c7429-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c7429-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="c7429-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7429-125">CommonParameters</span></span>
<span data-ttu-id="c7429-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7429-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7429-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c7429-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7429-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c7429-128">INPUTS</span></span>

### <span data-ttu-id="c7429-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c7429-129">System.String</span></span>

## <span data-ttu-id="c7429-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c7429-130">OUTPUTS</span></span>

### <span data-ttu-id="c7429-131">Microsoft. Azure. Commands. AKS. Models. PSNodePool</span><span class="sxs-lookup"><span data-stu-id="c7429-131">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="c7429-132">Note</span><span class="sxs-lookup"><span data-stu-id="c7429-132">NOTES</span></span>

## <span data-ttu-id="c7429-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c7429-133">RELATED LINKS</span></span>
