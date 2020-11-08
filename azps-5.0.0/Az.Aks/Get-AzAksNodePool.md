---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksNodePool.md
ms.openlocfilehash: 5c690b377d658e3ebc4eddaf49d546efd503a01c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200579"
---
# <span data-ttu-id="db795-101">Get-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="db795-101">Get-AzAksNodePool</span></span>

## <span data-ttu-id="db795-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="db795-102">SYNOPSIS</span></span>
<span data-ttu-id="db795-103">Creare un pool di note nel cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="db795-103">Create note pool in specified cluster.</span></span>

## <span data-ttu-id="db795-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db795-104">SYNTAX</span></span>

### <span data-ttu-id="db795-105">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="db795-105">NameParameterSet (Default)</span></span>
```
Get-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db795-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="db795-106">IdParameterSet</span></span>
```
Get-AzAksNodePool -Id <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db795-107">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="db795-107">ParentObjectParameterSet</span></span>
```
Get-AzAksNodePool -ClusterObject <PSKubernetesCluster> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db795-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db795-108">DESCRIPTION</span></span>
<span data-ttu-id="db795-109">Creare un pool di note nel cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="db795-109">Create note pool in specified cluster.</span></span>

## <span data-ttu-id="db795-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db795-110">EXAMPLES</span></span>

### <span data-ttu-id="db795-111">Ottenere tutti i pool di nodi all'interno di un cluster specificato</span><span class="sxs-lookup"><span data-stu-id="db795-111">Get all node pools within specified cluster</span></span>
```powershell
PS C:\> Get-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster
```

## <span data-ttu-id="db795-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="db795-112">PARAMETERS</span></span>

### <span data-ttu-id="db795-113">-Clustername</span><span class="sxs-lookup"><span data-stu-id="db795-113">-ClusterName</span></span>
<span data-ttu-id="db795-114">Nome della risorsa del cluster gestito.</span><span class="sxs-lookup"><span data-stu-id="db795-114">The name of the managed cluster resource.</span></span>

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

### <span data-ttu-id="db795-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="db795-115">-ClusterObject</span></span>
<span data-ttu-id="db795-116">Oggetto cluster.</span><span class="sxs-lookup"><span data-stu-id="db795-116">The cluster object.</span></span>

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

### <span data-ttu-id="db795-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db795-117">-DefaultProfile</span></span>
<span data-ttu-id="db795-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="db795-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db795-119">-ID</span><span class="sxs-lookup"><span data-stu-id="db795-119">-Id</span></span>
<span data-ttu-id="db795-120">ID di un pool di nodi nel cluster managed Kubernetes</span><span class="sxs-lookup"><span data-stu-id="db795-120">Id of an node pool in managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="db795-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="db795-121">-Name</span></span>
<span data-ttu-id="db795-122">Nome del pool di nodi.</span><span class="sxs-lookup"><span data-stu-id="db795-122">The name of the node pool.</span></span>

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

### <span data-ttu-id="db795-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db795-123">-ResourceGroupName</span></span>
<span data-ttu-id="db795-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="db795-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="db795-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db795-125">CommonParameters</span></span>
<span data-ttu-id="db795-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db795-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db795-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db795-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db795-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="db795-128">INPUTS</span></span>

### <span data-ttu-id="db795-129">System. String</span><span class="sxs-lookup"><span data-stu-id="db795-129">System.String</span></span>

## <span data-ttu-id="db795-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db795-130">OUTPUTS</span></span>

### <span data-ttu-id="db795-131">Microsoft. Azure. Commands. AKS. Models. PSNodePool</span><span class="sxs-lookup"><span data-stu-id="db795-131">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="db795-132">Note</span><span class="sxs-lookup"><span data-stu-id="db795-132">NOTES</span></span>

## <span data-ttu-id="db795-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db795-133">RELATED LINKS</span></span>