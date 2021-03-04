---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/get-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 9c9f1b3c88e49eca3be8a923324d195d3a773c1b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974317"
---
# <span data-ttu-id="4c044-101">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="4c044-101">Get-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="4c044-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c044-102">SYNOPSIS</span></span>
<span data-ttu-id="4c044-103">Ottenere i dettagli della versione del tipo di applicazione Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="4c044-103">Get Service Fabric application type version details.</span></span> <span data-ttu-id="4c044-104">Supporta solo le ARM di tipi di applicazione distribuite.</span><span class="sxs-lookup"><span data-stu-id="4c044-104">Only supports ARM deployed application type versions.</span></span>

## <span data-ttu-id="4c044-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4c044-105">SYNTAX</span></span>

### <span data-ttu-id="4c044-106">ByResourceGroupAndCluster (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4c044-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c044-107">ByVersion</span><span class="sxs-lookup"><span data-stu-id="4c044-107">ByVersion</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c044-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4c044-108">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4c044-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4c044-109">DESCRIPTION</span></span>
<span data-ttu-id="4c044-110">Usare questo cmdlet per ottenere i dettagli sulla versione del tipo di applicazione nel gruppo di risorse e nel cluster specificati.</span><span class="sxs-lookup"><span data-stu-id="4c044-110">Use this cmdlet to get the application type version details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="4c044-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4c044-111">EXAMPLES</span></span>

### <span data-ttu-id="4c044-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4c044-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appTypeName = "v1"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version
```

<span data-ttu-id="4c044-113">Questo esempio ottiene il tipo di applicazione "testAppType" con la versione "v1", se non trova la risorsa genera un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="4c044-113">This example gets the application type "testAppType" with version "v1", if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="4c044-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="4c044-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="4c044-115">Questo esempio ottiene un elenco delle versioni del tipo di applicazione definite nel tipo e nel cluster specificati.</span><span class="sxs-lookup"><span data-stu-id="4c044-115">This example gets a list of the application type versions defined under the specified cluster and type.</span></span>

## <span data-ttu-id="4c044-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c044-116">PARAMETERS</span></span>

### <span data-ttu-id="4c044-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4c044-117">-ClusterName</span></span>
<span data-ttu-id="4c044-118">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="4c044-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="4c044-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c044-119">-DefaultProfile</span></span>
<span data-ttu-id="4c044-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4c044-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c044-121">-Name</span><span class="sxs-lookup"><span data-stu-id="4c044-121">-Name</span></span>
<span data-ttu-id="4c044-122">Specificare il nome del tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="4c044-122">Specify the name of the application type.</span></span>

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

### <span data-ttu-id="4c044-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c044-123">-ResourceGroupName</span></span>
<span data-ttu-id="4c044-124">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4c044-124">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="4c044-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4c044-125">-ResourceId</span></span>
<span data-ttu-id="4c044-126">Arm ResourceId della versione del tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="4c044-126">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="4c044-127">-Version</span><span class="sxs-lookup"><span data-stu-id="4c044-127">-Version</span></span>
<span data-ttu-id="4c044-128">Specificare la versione del tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="4c044-128">Specify the version of the application type.</span></span>

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

### <span data-ttu-id="4c044-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c044-129">CommonParameters</span></span>
<span data-ttu-id="4c044-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c044-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c044-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4c044-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c044-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="4c044-132">INPUTS</span></span>

### <span data-ttu-id="4c044-133">System.String</span><span class="sxs-lookup"><span data-stu-id="4c044-133">System.String</span></span>

## <span data-ttu-id="4c044-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4c044-134">OUTPUTS</span></span>

### <span data-ttu-id="4c044-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="4c044-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="4c044-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="4c044-136">NOTES</span></span>

## <span data-ttu-id="4c044-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4c044-137">RELATED LINKS</span></span>
