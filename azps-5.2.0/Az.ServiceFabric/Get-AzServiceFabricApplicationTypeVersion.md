---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 7dc8ca2302b00b5eb200c30aed104f5fe5ff8642
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347827"
---
# <span data-ttu-id="59c8c-101">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="59c8c-101">Get-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="59c8c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="59c8c-102">SYNOPSIS</span></span>
<span data-ttu-id="59c8c-103">Ottenere i dettagli della versione del tipo di servizio in tessuto.</span><span class="sxs-lookup"><span data-stu-id="59c8c-103">Get Service Fabric application type version details.</span></span> <span data-ttu-id="59c8c-104">Supporta solo le versioni di tipo applicazione distribuite ARM.</span><span class="sxs-lookup"><span data-stu-id="59c8c-104">Only supports ARM deployed application type versions.</span></span>

## <span data-ttu-id="59c8c-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="59c8c-105">SYNTAX</span></span>

### <span data-ttu-id="59c8c-106">ByResourceGroupAndCluster (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="59c8c-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59c8c-107">ByVersion</span><span class="sxs-lookup"><span data-stu-id="59c8c-107">ByVersion</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59c8c-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="59c8c-108">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="59c8c-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59c8c-109">DESCRIPTION</span></span>
<span data-ttu-id="59c8c-110">Questo cmdlet consente di ottenere i dettagli della versione del tipo di applicazione nel gruppo di risorse e nel cluster specificati.</span><span class="sxs-lookup"><span data-stu-id="59c8c-110">Use this cmdlet to get the application type version details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="59c8c-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="59c8c-111">EXAMPLES</span></span>

### <span data-ttu-id="59c8c-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="59c8c-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appTypeName = "v1"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version
```

<span data-ttu-id="59c8c-113">Questo esempio ottiene il tipo di applicazione "testAppType" con la versione "V1", se non trova la risorsa che genererà un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="59c8c-113">This example gets the application type "testAppType" with version "v1", if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="59c8c-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="59c8c-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="59c8c-115">Questo esempio consente di ottenere un elenco delle versioni del tipo di applicazione definite sotto il tipo e il cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="59c8c-115">This example gets a list of the application type versions defined under the specified cluster and type.</span></span>

## <span data-ttu-id="59c8c-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="59c8c-116">PARAMETERS</span></span>

### <span data-ttu-id="59c8c-117">-Clustername</span><span class="sxs-lookup"><span data-stu-id="59c8c-117">-ClusterName</span></span>
<span data-ttu-id="59c8c-118">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="59c8c-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="59c8c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59c8c-119">-DefaultProfile</span></span>
<span data-ttu-id="59c8c-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="59c8c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59c8c-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="59c8c-121">-Name</span></span>
<span data-ttu-id="59c8c-122">Specificare il nome del tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="59c8c-122">Specify the name of the application type.</span></span>

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

### <span data-ttu-id="59c8c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59c8c-123">-ResourceGroupName</span></span>
<span data-ttu-id="59c8c-124">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="59c8c-124">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="59c8c-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59c8c-125">-ResourceId</span></span>
<span data-ttu-id="59c8c-126">ARM ResourceId della versione del tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="59c8c-126">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="59c8c-127">-Versione</span><span class="sxs-lookup"><span data-stu-id="59c8c-127">-Version</span></span>
<span data-ttu-id="59c8c-128">Specifica la versione del tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="59c8c-128">Specify the version of the application type.</span></span>

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

### <span data-ttu-id="59c8c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59c8c-129">CommonParameters</span></span>
<span data-ttu-id="59c8c-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59c8c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59c8c-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="59c8c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59c8c-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="59c8c-132">INPUTS</span></span>

### <span data-ttu-id="59c8c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="59c8c-133">System.String</span></span>

## <span data-ttu-id="59c8c-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="59c8c-134">OUTPUTS</span></span>

### <span data-ttu-id="59c8c-135">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="59c8c-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="59c8c-136">Note</span><span class="sxs-lookup"><span data-stu-id="59c8c-136">NOTES</span></span>

## <span data-ttu-id="59c8c-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="59c8c-137">RELATED LINKS</span></span>
