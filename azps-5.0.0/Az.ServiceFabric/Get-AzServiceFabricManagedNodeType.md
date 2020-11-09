---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 6cca65a061e54bbd08327fc054a0c6b55d8c98f6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300138"
---
# <span data-ttu-id="1b207-101">Get-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="1b207-101">Get-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="1b207-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1b207-102">SYNOPSIS</span></span>
<span data-ttu-id="1b207-103">Ottenere i dettagli delle risorse del tipo di nodo gestito.</span><span class="sxs-lookup"><span data-stu-id="1b207-103">Get the managed node type resource details.</span></span>

## <span data-ttu-id="1b207-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1b207-104">SYNTAX</span></span>

### <span data-ttu-id="1b207-105">ByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1b207-105">ByName (Default)</span></span>
```
Get-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b207-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1b207-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b207-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b207-107">DESCRIPTION</span></span>
<span data-ttu-id="1b207-108">Ottenere i dettagli delle risorse del tipo di nodo gestito.</span><span class="sxs-lookup"><span data-stu-id="1b207-108">Get the managed node type resource details.</span></span>

## <span data-ttu-id="1b207-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1b207-109">EXAMPLES</span></span>

### <span data-ttu-id="1b207-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1b207-110">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName
```

<span data-ttu-id="1b207-111">Ottenere i dettagli del tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="1b207-111">Get node type details.</span></span>

### <span data-ttu-id="1b207-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="1b207-112">Example 2</span></span>
```powershell
$rgName = "testRG"
Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName
```

<span data-ttu-id="1b207-113">Ottenere l'elenco dei tipi di nodo sotto il cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="1b207-113">Get list of node types under the specified cluster.</span></span>

## <span data-ttu-id="1b207-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1b207-114">PARAMETERS</span></span>

### <span data-ttu-id="1b207-115">-Clustername</span><span class="sxs-lookup"><span data-stu-id="1b207-115">-ClusterName</span></span>
<span data-ttu-id="1b207-116">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="1b207-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="1b207-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b207-117">-DefaultProfile</span></span>
<span data-ttu-id="1b207-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1b207-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b207-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="1b207-119">-Name</span></span>
<span data-ttu-id="1b207-120">Specificare il nome del tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="1b207-120">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="1b207-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b207-121">-ResourceGroupName</span></span>
<span data-ttu-id="1b207-122">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1b207-122">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="1b207-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b207-123">CommonParameters</span></span>
<span data-ttu-id="1b207-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b207-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b207-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1b207-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b207-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1b207-126">INPUTS</span></span>

### <span data-ttu-id="1b207-127">System. String</span><span class="sxs-lookup"><span data-stu-id="1b207-127">System.String</span></span>

## <span data-ttu-id="1b207-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1b207-128">OUTPUTS</span></span>

### <span data-ttu-id="1b207-129">Microsoft. Azure. Commands. ServiceFabric. Models. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="1b207-129">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="1b207-130">Note</span><span class="sxs-lookup"><span data-stu-id="1b207-130">NOTES</span></span>

## <span data-ttu-id="1b207-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1b207-131">RELATED LINKS</span></span>
