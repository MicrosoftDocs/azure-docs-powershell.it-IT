---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
ms.openlocfilehash: 1dfd9e0aa2bc6b7c5d52ccfed756f2a96a3f307c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191272"
---
# <span data-ttu-id="c3625-101">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="c3625-101">Get-AzServiceFabricService</span></span>

## <span data-ttu-id="c3625-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c3625-102">SYNOPSIS</span></span>
<span data-ttu-id="c3625-103">Ottenere i dettagli del servizio Fabric servizio nell'applicazione e nel cluster specificati.</span><span class="sxs-lookup"><span data-stu-id="c3625-103">Get Service Fabric service details under the specified application and cluster.</span></span>

## <span data-ttu-id="c3625-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c3625-104">SYNTAX</span></span>

### <span data-ttu-id="c3625-105">ByResourceGroupAndCluster (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c3625-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3625-106">ByName</span><span class="sxs-lookup"><span data-stu-id="c3625-106">ByName</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3625-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c3625-107">ByResourceId</span></span>
```
Get-AzServiceFabricService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3625-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c3625-108">DESCRIPTION</span></span>
<span data-ttu-id="c3625-109">Questo cmdlet otterrà i dettagli del servizio nell'applicazione e nel cluster specificati.</span><span class="sxs-lookup"><span data-stu-id="c3625-109">This cmdlet will get the service details in the specified application and cluster.</span></span>

## <span data-ttu-id="c3625-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c3625-110">EXAMPLES</span></span>

### <span data-ttu-id="c3625-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c3625-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService"
PS C:\> Get-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="c3625-112">Questo esempio consente di ottenere i dettagli delle risorse del servizio per il servizio "testApp ~ testService".</span><span class="sxs-lookup"><span data-stu-id="c3625-112">This example gets the service resource details for the service "testApp~testService".</span></span>

### <span data-ttu-id="c3625-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c3625-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName
```

<span data-ttu-id="c3625-114">Questo esempio consente di ottenere un elenco dei servizi sotto l'applicazione "testApp".</span><span class="sxs-lookup"><span data-stu-id="c3625-114">This example gets a list of the services under the application "testApp".</span></span>

## <span data-ttu-id="c3625-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c3625-115">PARAMETERS</span></span>

### <span data-ttu-id="c3625-116">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="c3625-116">-ApplicationName</span></span>
<span data-ttu-id="c3625-117">Specificare il nome dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c3625-117">Specify the name of the application.</span></span>

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

### <span data-ttu-id="c3625-118">-Clustername</span><span class="sxs-lookup"><span data-stu-id="c3625-118">-ClusterName</span></span>
<span data-ttu-id="c3625-119">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="c3625-119">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="c3625-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3625-120">-DefaultProfile</span></span>
<span data-ttu-id="c3625-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c3625-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3625-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="c3625-122">-Name</span></span>
<span data-ttu-id="c3625-123">Specificare il nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="c3625-123">Specify the name of the service.</span></span>

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

### <span data-ttu-id="c3625-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3625-124">-ResourceGroupName</span></span>
<span data-ttu-id="c3625-125">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c3625-125">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="c3625-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3625-126">-ResourceId</span></span>
<span data-ttu-id="c3625-127">ARM ResourceId del servizio.</span><span class="sxs-lookup"><span data-stu-id="c3625-127">Arm ResourceId of the service.</span></span>

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

### <span data-ttu-id="c3625-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3625-128">CommonParameters</span></span>
<span data-ttu-id="c3625-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3625-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3625-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c3625-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3625-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c3625-131">INPUTS</span></span>

### <span data-ttu-id="c3625-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c3625-132">System.String</span></span>

## <span data-ttu-id="c3625-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c3625-133">OUTPUTS</span></span>

### <span data-ttu-id="c3625-134">Microsoft. Azure. Commands. ServiceFabric. Models. PSService</span><span class="sxs-lookup"><span data-stu-id="c3625-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="c3625-135">Note</span><span class="sxs-lookup"><span data-stu-id="c3625-135">NOTES</span></span>

## <span data-ttu-id="c3625-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c3625-136">RELATED LINKS</span></span>