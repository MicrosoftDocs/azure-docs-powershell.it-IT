---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/get-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 15ba499908a4a631a22f9064b1938d3b32fdafd5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955629"
---
# <span data-ttu-id="21387-101">Get-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="21387-101">Get-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="21387-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21387-102">SYNOPSIS</span></span>
<span data-ttu-id="21387-103">Ottenere i dettagli delle risorse per il tipo di nodo gestito.</span><span class="sxs-lookup"><span data-stu-id="21387-103">Get the managed node type resource details.</span></span>

## <span data-ttu-id="21387-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="21387-104">SYNTAX</span></span>

### <span data-ttu-id="21387-105">ByName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="21387-105">ByName (Default)</span></span>
```
Get-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21387-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="21387-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21387-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="21387-107">DESCRIPTION</span></span>
<span data-ttu-id="21387-108">Ottenere i dettagli delle risorse per il tipo di nodo gestito.</span><span class="sxs-lookup"><span data-stu-id="21387-108">Get the managed node type resource details.</span></span>

## <span data-ttu-id="21387-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="21387-109">EXAMPLES</span></span>

### <span data-ttu-id="21387-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="21387-110">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName
```

<span data-ttu-id="21387-111">Ottenere i dettagli sul tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="21387-111">Get node type details.</span></span>

### <span data-ttu-id="21387-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="21387-112">Example 2</span></span>
```powershell
$rgName = "testRG"
Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName
```

<span data-ttu-id="21387-113">Ottenere l'elenco dei tipi di nodo nel cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="21387-113">Get list of node types under the specified cluster.</span></span>

## <span data-ttu-id="21387-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21387-114">PARAMETERS</span></span>

### <span data-ttu-id="21387-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="21387-115">-ClusterName</span></span>
<span data-ttu-id="21387-116">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="21387-116">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21387-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21387-117">-DefaultProfile</span></span>
<span data-ttu-id="21387-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="21387-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21387-119">-Name</span><span class="sxs-lookup"><span data-stu-id="21387-119">-Name</span></span>
<span data-ttu-id="21387-120">Specificare il nome del tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="21387-120">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: NodeTypeName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21387-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21387-121">-ResourceGroupName</span></span>
<span data-ttu-id="21387-122">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="21387-122">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21387-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21387-123">CommonParameters</span></span>
<span data-ttu-id="21387-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21387-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21387-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="21387-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21387-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="21387-126">INPUTS</span></span>

### <span data-ttu-id="21387-127">System.String</span><span class="sxs-lookup"><span data-stu-id="21387-127">System.String</span></span>

## <span data-ttu-id="21387-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="21387-128">OUTPUTS</span></span>

### <span data-ttu-id="21387-129">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="21387-129">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="21387-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="21387-130">NOTES</span></span>

## <span data-ttu-id="21387-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="21387-131">RELATED LINKS</span></span>
