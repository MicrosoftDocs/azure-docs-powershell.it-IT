---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: ea86fb4a110d355a848b9fe58969d30ccb96e2da
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300150"
---
# <span data-ttu-id="ff034-101">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="ff034-101">Get-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="ff034-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ff034-102">SYNOPSIS</span></span>
<span data-ttu-id="ff034-103">Ottenere i dettagli della versione del tipo di servizio in tessuto.</span><span class="sxs-lookup"><span data-stu-id="ff034-103">Get Service Fabric application type version details.</span></span>

## <span data-ttu-id="ff034-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ff034-104">SYNTAX</span></span>

### <span data-ttu-id="ff034-105">ByResourceGroupAndCluster (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ff034-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff034-106">ByVersion</span><span class="sxs-lookup"><span data-stu-id="ff034-106">ByVersion</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff034-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ff034-107">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ff034-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ff034-108">DESCRIPTION</span></span>
<span data-ttu-id="ff034-109">Questo cmdlet consente di ottenere i dettagli della versione del tipo di applicazione nel gruppo di risorse e nel cluster specificati.</span><span class="sxs-lookup"><span data-stu-id="ff034-109">Use this cmdlet to get the application type version details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="ff034-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ff034-110">EXAMPLES</span></span>

### <span data-ttu-id="ff034-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ff034-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appTypeName = "v1"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version
```

<span data-ttu-id="ff034-112">Questo esempio ottiene il tipo di applicazione "testAppType" con la versione "V1", se non trova la risorsa che genererà un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="ff034-112">This example gets the application type "testAppType" with version "v1", if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="ff034-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ff034-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="ff034-114">Questo esempio consente di ottenere un elenco delle versioni del tipo di applicazione definite sotto il tipo e il cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="ff034-114">This example gets a list of the application type versions defined under the specified cluster and type.</span></span>

## <span data-ttu-id="ff034-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ff034-115">PARAMETERS</span></span>

### <span data-ttu-id="ff034-116">-Clustername</span><span class="sxs-lookup"><span data-stu-id="ff034-116">-ClusterName</span></span>
<span data-ttu-id="ff034-117">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="ff034-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="ff034-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff034-118">-DefaultProfile</span></span>
<span data-ttu-id="ff034-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ff034-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff034-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="ff034-120">-Name</span></span>
<span data-ttu-id="ff034-121">Specificare il nome del tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="ff034-121">Specify the name of the application type.</span></span>

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

### <span data-ttu-id="ff034-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff034-122">-ResourceGroupName</span></span>
<span data-ttu-id="ff034-123">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ff034-123">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="ff034-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ff034-124">-ResourceId</span></span>
<span data-ttu-id="ff034-125">ARM ResourceId della versione del tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="ff034-125">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="ff034-126">-Versione</span><span class="sxs-lookup"><span data-stu-id="ff034-126">-Version</span></span>
<span data-ttu-id="ff034-127">Specifica la versione del tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="ff034-127">Specify the version of the application type.</span></span>

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

### <span data-ttu-id="ff034-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff034-128">CommonParameters</span></span>
<span data-ttu-id="ff034-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff034-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff034-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ff034-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff034-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ff034-131">INPUTS</span></span>

### <span data-ttu-id="ff034-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ff034-132">System.String</span></span>

## <span data-ttu-id="ff034-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ff034-133">OUTPUTS</span></span>

### <span data-ttu-id="ff034-134">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="ff034-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="ff034-135">Note</span><span class="sxs-lookup"><span data-stu-id="ff034-135">NOTES</span></span>

## <span data-ttu-id="ff034-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ff034-136">RELATED LINKS</span></span>
