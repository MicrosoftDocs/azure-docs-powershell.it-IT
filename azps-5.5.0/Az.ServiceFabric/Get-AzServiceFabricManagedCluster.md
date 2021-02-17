---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedCluster.md
ms.openlocfilehash: c81199bb78a64ac2ed32a21e0f3822093a2b2b14
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208043"
---
# <span data-ttu-id="7cca4-101">Get-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="7cca4-101">Get-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="7cca4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cca4-102">SYNOPSIS</span></span>
<span data-ttu-id="7cca4-103">Ottenere i dettagli delle risorse del cluster gestito.</span><span class="sxs-lookup"><span data-stu-id="7cca4-103">Get the managed cluster resource details.</span></span>

## <span data-ttu-id="7cca4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7cca4-104">SYNTAX</span></span>

### <span data-ttu-id="7cca4-105">BySubscription (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7cca4-105">BySubscription (Default)</span></span>
```
Get-AzServiceFabricManagedCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7cca4-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7cca4-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7cca4-107">ByName</span><span class="sxs-lookup"><span data-stu-id="7cca4-107">ByName</span></span>
```
Get-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7cca4-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7cca4-108">DESCRIPTION</span></span>
<span data-ttu-id="7cca4-109">Ottenere i dettagli delle risorse del cluster gestito.</span><span class="sxs-lookup"><span data-stu-id="7cca4-109">Get the managed cluster resource details.</span></span>

## <span data-ttu-id="7cca4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7cca4-110">EXAMPLES</span></span>

### <span data-ttu-id="7cca4-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7cca4-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName
```

<span data-ttu-id="7cca4-112">Ottenere informazioni dettagliate sui cluster.</span><span class="sxs-lookup"><span data-stu-id="7cca4-112">Get cluster details.</span></span>

### <span data-ttu-id="7cca4-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7cca4-113">Example 2</span></span>
```powershell
$rgName = "testRG"
Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName
```

<span data-ttu-id="7cca4-114">Ottenere l'elenco dei cluster nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="7cca4-114">Get list of clusters under the specified resource group.</span></span>

### <span data-ttu-id="7cca4-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="7cca4-115">Example 3</span></span>
```powershell
Get-AzServiceFabricManagedCluster
```

<span data-ttu-id="7cca4-116">Ottenere l'elenco dei cluster nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="7cca4-116">Get list of clusters under the current subscription.</span></span>

## <span data-ttu-id="7cca4-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7cca4-117">PARAMETERS</span></span>

### <span data-ttu-id="7cca4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cca4-118">-DefaultProfile</span></span>
<span data-ttu-id="7cca4-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7cca4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7cca4-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7cca4-120">-Name</span></span>
<span data-ttu-id="7cca4-121">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="7cca4-121">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="7cca4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cca4-122">-ResourceGroupName</span></span>
<span data-ttu-id="7cca4-123">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7cca4-123">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="7cca4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cca4-124">CommonParameters</span></span>
<span data-ttu-id="7cca4-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cca4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cca4-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7cca4-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cca4-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="7cca4-127">INPUTS</span></span>

### <span data-ttu-id="7cca4-128">System.String</span><span class="sxs-lookup"><span data-stu-id="7cca4-128">System.String</span></span>

## <span data-ttu-id="7cca4-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7cca4-129">OUTPUTS</span></span>

### <span data-ttu-id="7cca4-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="7cca4-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="7cca4-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="7cca4-131">NOTES</span></span>

## <span data-ttu-id="7cca4-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7cca4-132">RELATED LINKS</span></span>
