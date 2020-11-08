---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 7a47f6b7ee5200b8e4409d7fa25ba63244fb2ae6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021030"
---
# <span data-ttu-id="4d1e1-101">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="4d1e1-101">Get-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="4d1e1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4d1e1-102">SYNOPSIS</span></span>
<span data-ttu-id="4d1e1-103">Ottenere i dettagli della versione del tipo di servizio in tessuto.</span><span class="sxs-lookup"><span data-stu-id="4d1e1-103">Get Service Fabric application type version details.</span></span>

## <span data-ttu-id="4d1e1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4d1e1-104">SYNTAX</span></span>

### <span data-ttu-id="4d1e1-105">ByResourceGroupAndCluster (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4d1e1-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d1e1-106">ByVersion</span><span class="sxs-lookup"><span data-stu-id="4d1e1-106">ByVersion</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d1e1-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4d1e1-107">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4d1e1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4d1e1-108">DESCRIPTION</span></span>
<span data-ttu-id="4d1e1-109">Questo cmdlet consente di ottenere i dettagli della versione del tipo di applicazione nel gruppo di risorse e nel cluster specificati.</span><span class="sxs-lookup"><span data-stu-id="4d1e1-109">Use this cmdlet to get the application type version details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="4d1e1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4d1e1-110">EXAMPLES</span></span>

### <span data-ttu-id="4d1e1-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4d1e1-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appTypeName = "v1"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version
```

<span data-ttu-id="4d1e1-112">Questo esempio ottiene il tipo di applicazione "testAppType" con la versione "V1", se non trova la risorsa che genererà un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="4d1e1-112">This example gets the application type "testAppType" with version "v1", if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="4d1e1-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="4d1e1-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="4d1e1-114">Questo esempio consente di ottenere un elenco delle versioni del tipo di applicazione definite sotto il tipo e il cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="4d1e1-114">This example gets a list of the application type versions defined under the specified cluster and type.</span></span>

## <span data-ttu-id="4d1e1-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4d1e1-115">PARAMETERS</span></span>

### <span data-ttu-id="4d1e1-116">-Clustername</span><span class="sxs-lookup"><span data-stu-id="4d1e1-116">-ClusterName</span></span>
<span data-ttu-id="4d1e1-117">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="4d1e1-117">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByVersion
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d1e1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d1e1-118">-DefaultProfile</span></span>
<span data-ttu-id="4d1e1-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4d1e1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d1e1-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="4d1e1-120">-Name</span></span>
<span data-ttu-id="4d1e1-121">Specificare il nome del tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="4d1e1-121">Specify the name of the application type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByVersion
Aliases: ApplicationTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d1e1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d1e1-122">-ResourceGroupName</span></span>
<span data-ttu-id="4d1e1-123">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4d1e1-123">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByVersion
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d1e1-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d1e1-124">-ResourceId</span></span>
<span data-ttu-id="4d1e1-125">ARM ResourceId della versione del tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="4d1e1-125">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="4d1e1-126">-Versione</span><span class="sxs-lookup"><span data-stu-id="4d1e1-126">-Version</span></span>
<span data-ttu-id="4d1e1-127">Specifica la versione del tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="4d1e1-127">Specify the version of the application type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVersion
Aliases: ApplicationTypeVersion

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d1e1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d1e1-128">CommonParameters</span></span>
<span data-ttu-id="4d1e1-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d1e1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d1e1-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d1e1-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d1e1-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4d1e1-131">INPUTS</span></span>

### <span data-ttu-id="4d1e1-132">System. String</span><span class="sxs-lookup"><span data-stu-id="4d1e1-132">System.String</span></span>

## <span data-ttu-id="4d1e1-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4d1e1-133">OUTPUTS</span></span>

### <span data-ttu-id="4d1e1-134">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="4d1e1-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="4d1e1-135">Note</span><span class="sxs-lookup"><span data-stu-id="4d1e1-135">NOTES</span></span>

## <span data-ttu-id="4d1e1-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4d1e1-136">RELATED LINKS</span></span>
