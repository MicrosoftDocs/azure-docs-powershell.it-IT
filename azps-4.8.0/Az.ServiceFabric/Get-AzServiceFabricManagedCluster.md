---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedCluster.md
ms.openlocfilehash: c81199bb78a64ac2ed32a21e0f3822093a2b2b14
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032189"
---
# <span data-ttu-id="31b65-101">Get-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="31b65-101">Get-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="31b65-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="31b65-102">SYNOPSIS</span></span>
<span data-ttu-id="31b65-103">Ottenere i dettagli delle risorse del cluster gestito.</span><span class="sxs-lookup"><span data-stu-id="31b65-103">Get the managed cluster resource details.</span></span>

## <span data-ttu-id="31b65-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="31b65-104">SYNTAX</span></span>

### <span data-ttu-id="31b65-105">BySubscription (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="31b65-105">BySubscription (Default)</span></span>
```
Get-AzServiceFabricManagedCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31b65-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="31b65-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="31b65-107">ByName</span><span class="sxs-lookup"><span data-stu-id="31b65-107">ByName</span></span>
```
Get-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31b65-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31b65-108">DESCRIPTION</span></span>
<span data-ttu-id="31b65-109">Ottenere i dettagli delle risorse del cluster gestito.</span><span class="sxs-lookup"><span data-stu-id="31b65-109">Get the managed cluster resource details.</span></span>

## <span data-ttu-id="31b65-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="31b65-110">EXAMPLES</span></span>

### <span data-ttu-id="31b65-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="31b65-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName
```

<span data-ttu-id="31b65-112">Ottenere i dettagli del cluster.</span><span class="sxs-lookup"><span data-stu-id="31b65-112">Get cluster details.</span></span>

### <span data-ttu-id="31b65-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="31b65-113">Example 2</span></span>
```powershell
$rgName = "testRG"
Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName
```

<span data-ttu-id="31b65-114">Ottenere l'elenco dei cluster nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="31b65-114">Get list of clusters under the specified resource group.</span></span>

### <span data-ttu-id="31b65-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="31b65-115">Example 3</span></span>
```powershell
Get-AzServiceFabricManagedCluster
```

<span data-ttu-id="31b65-116">Ottenere l'elenco dei cluster sotto l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="31b65-116">Get list of clusters under the current subscription.</span></span>

## <span data-ttu-id="31b65-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="31b65-117">PARAMETERS</span></span>

### <span data-ttu-id="31b65-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31b65-118">-DefaultProfile</span></span>
<span data-ttu-id="31b65-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="31b65-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31b65-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="31b65-120">-Name</span></span>
<span data-ttu-id="31b65-121">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="31b65-121">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31b65-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31b65-122">-ResourceGroupName</span></span>
<span data-ttu-id="31b65-123">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="31b65-123">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31b65-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31b65-124">CommonParameters</span></span>
<span data-ttu-id="31b65-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31b65-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31b65-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="31b65-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31b65-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="31b65-127">INPUTS</span></span>

### <span data-ttu-id="31b65-128">System. String</span><span class="sxs-lookup"><span data-stu-id="31b65-128">System.String</span></span>

## <span data-ttu-id="31b65-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="31b65-129">OUTPUTS</span></span>

### <span data-ttu-id="31b65-130">Microsoft. Azure. Commands. ServiceFabric. Models. PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="31b65-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="31b65-131">Note</span><span class="sxs-lookup"><span data-stu-id="31b65-131">NOTES</span></span>

## <span data-ttu-id="31b65-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="31b65-132">RELATED LINKS</span></span>
