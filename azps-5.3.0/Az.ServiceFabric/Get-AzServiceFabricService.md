---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
ms.openlocfilehash: d927ef9a8a1c3ef97976911b122f22e1948f2996
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98485888"
---
# <span data-ttu-id="bb643-101">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="bb643-101">Get-AzServiceFabricService</span></span>

## <span data-ttu-id="bb643-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bb643-102">SYNOPSIS</span></span>
<span data-ttu-id="bb643-103">Ottenere i dettagli del servizio Fabric servizio nell'applicazione e nel cluster specificati.</span><span class="sxs-lookup"><span data-stu-id="bb643-103">Get Service Fabric service details under the specified application and cluster.</span></span> <span data-ttu-id="bb643-104">Supporta solo i servizi distribuiti con ARM.</span><span class="sxs-lookup"><span data-stu-id="bb643-104">Only supports ARM deployed services.</span></span>

## <span data-ttu-id="bb643-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bb643-105">SYNTAX</span></span>

### <span data-ttu-id="bb643-106">ByResourceGroupAndCluster (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bb643-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb643-107">ByName</span><span class="sxs-lookup"><span data-stu-id="bb643-107">ByName</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb643-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="bb643-108">ByResourceId</span></span>
```
Get-AzServiceFabricService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb643-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb643-109">DESCRIPTION</span></span>
<span data-ttu-id="bb643-110">Questo cmdlet otterrà i dettagli del servizio nell'applicazione e nel cluster specificati.</span><span class="sxs-lookup"><span data-stu-id="bb643-110">This cmdlet will get the service details in the specified application and cluster.</span></span>

## <span data-ttu-id="bb643-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bb643-111">EXAMPLES</span></span>

### <span data-ttu-id="bb643-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bb643-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService"
PS C:\> Get-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="bb643-113">Questo esempio consente di ottenere i dettagli delle risorse del servizio per il servizio "testApp ~ testService".</span><span class="sxs-lookup"><span data-stu-id="bb643-113">This example gets the service resource details for the service "testApp~testService".</span></span>

### <span data-ttu-id="bb643-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="bb643-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName
```

<span data-ttu-id="bb643-115">Questo esempio consente di ottenere un elenco dei servizi sotto l'applicazione "testApp".</span><span class="sxs-lookup"><span data-stu-id="bb643-115">This example gets a list of the services under the application "testApp".</span></span>

## <span data-ttu-id="bb643-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bb643-116">PARAMETERS</span></span>

### <span data-ttu-id="bb643-117">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="bb643-117">-ApplicationName</span></span>
<span data-ttu-id="bb643-118">Specificare il nome dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bb643-118">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb643-119">-Clustername</span><span class="sxs-lookup"><span data-stu-id="bb643-119">-ClusterName</span></span>
<span data-ttu-id="bb643-120">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="bb643-120">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="bb643-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb643-121">-DefaultProfile</span></span>
<span data-ttu-id="bb643-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bb643-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb643-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="bb643-123">-Name</span></span>
<span data-ttu-id="bb643-124">Specificare il nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="bb643-124">Specify the name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ServiceName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb643-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb643-125">-ResourceGroupName</span></span>
<span data-ttu-id="bb643-126">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bb643-126">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="bb643-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb643-127">-ResourceId</span></span>
<span data-ttu-id="bb643-128">ARM ResourceId del servizio.</span><span class="sxs-lookup"><span data-stu-id="bb643-128">Arm ResourceId of the service.</span></span>

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

### <span data-ttu-id="bb643-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb643-129">CommonParameters</span></span>
<span data-ttu-id="bb643-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb643-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb643-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bb643-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb643-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bb643-132">INPUTS</span></span>

### <span data-ttu-id="bb643-133">System. String</span><span class="sxs-lookup"><span data-stu-id="bb643-133">System.String</span></span>

## <span data-ttu-id="bb643-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bb643-134">OUTPUTS</span></span>

### <span data-ttu-id="bb643-135">Microsoft. Azure. Commands. ServiceFabric. Models. PSService</span><span class="sxs-lookup"><span data-stu-id="bb643-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="bb643-136">Note</span><span class="sxs-lookup"><span data-stu-id="bb643-136">NOTES</span></span>

## <span data-ttu-id="bb643-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bb643-137">RELATED LINKS</span></span>
