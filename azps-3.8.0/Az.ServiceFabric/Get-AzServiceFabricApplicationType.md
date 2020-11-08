---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
ms.openlocfilehash: dcbb85e9c7b8f1a98acec094043ec03b562e33d8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022252"
---
# <span data-ttu-id="63856-101">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="63856-101">Get-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="63856-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="63856-102">SYNOPSIS</span></span>
<span data-ttu-id="63856-103">Ottenere i dettagli del tipo di applicazione tessuto servizio.</span><span class="sxs-lookup"><span data-stu-id="63856-103">Get Service Fabric application type details.</span></span>

## <span data-ttu-id="63856-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="63856-104">SYNTAX</span></span>

### <span data-ttu-id="63856-105">ByResourceGroupAndCluster (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="63856-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63856-106">ByName</span><span class="sxs-lookup"><span data-stu-id="63856-106">ByName</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63856-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="63856-107">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationType -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="63856-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="63856-108">DESCRIPTION</span></span>
<span data-ttu-id="63856-109">Questo cmdlet consente di ottenere i dettagli del tipo di applicazione nel gruppo di risorse e nel cluster specificati.</span><span class="sxs-lookup"><span data-stu-id="63856-109">Use this cmdlet to get the application type details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="63856-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="63856-110">EXAMPLES</span></span>

### <span data-ttu-id="63856-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="63856-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="63856-112">Questo esempio otterrà i dettagli del tipo di applicazione con i parametri specificati, se non trova la risorsa che genererà un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="63856-112">This example will get the application type details with the parameters specified, if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="63856-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="63856-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="63856-114">Questo esempio otterrà un elenco dei tipi di applicazione definiti nel cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="63856-114">This example will get a list of the application types defined under the specified cluster.</span></span>

## <span data-ttu-id="63856-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="63856-115">PARAMETERS</span></span>

### <span data-ttu-id="63856-116">-Clustername</span><span class="sxs-lookup"><span data-stu-id="63856-116">-ClusterName</span></span>
<span data-ttu-id="63856-117">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="63856-117">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63856-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63856-118">-DefaultProfile</span></span>
<span data-ttu-id="63856-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="63856-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63856-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="63856-120">-Name</span></span>
<span data-ttu-id="63856-121">Specificare il nome del tipo di applicazione</span><span class="sxs-lookup"><span data-stu-id="63856-121">Specify the name of the application type</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ApplicationTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63856-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63856-122">-ResourceGroupName</span></span>
<span data-ttu-id="63856-123">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="63856-123">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63856-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="63856-124">-ResourceId</span></span>
<span data-ttu-id="63856-125">ARM ResourceId del tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="63856-125">Arm ResourceId of the application type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63856-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63856-126">CommonParameters</span></span>
<span data-ttu-id="63856-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63856-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63856-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63856-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63856-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="63856-129">INPUTS</span></span>

### <span data-ttu-id="63856-130">System. String</span><span class="sxs-lookup"><span data-stu-id="63856-130">System.String</span></span>

## <span data-ttu-id="63856-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="63856-131">OUTPUTS</span></span>

### <span data-ttu-id="63856-132">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="63856-132">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="63856-133">Note</span><span class="sxs-lookup"><span data-stu-id="63856-133">NOTES</span></span>

## <span data-ttu-id="63856-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="63856-134">RELATED LINKS</span></span>
