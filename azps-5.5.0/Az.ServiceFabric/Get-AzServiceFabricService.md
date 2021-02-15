---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
ms.openlocfilehash: d927ef9a8a1c3ef97976911b122f22e1948f2996
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197831"
---
# <span data-ttu-id="8593c-101">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="8593c-101">Get-AzServiceFabricService</span></span>

## <span data-ttu-id="8593c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8593c-102">SYNOPSIS</span></span>
<span data-ttu-id="8593c-103">Ottenere i dettagli del servizio Service Fabric nell'applicazione e nel cluster specificati.</span><span class="sxs-lookup"><span data-stu-id="8593c-103">Get Service Fabric service details under the specified application and cluster.</span></span> <span data-ttu-id="8593c-104">Supporta solo i ARM distribuiti.</span><span class="sxs-lookup"><span data-stu-id="8593c-104">Only supports ARM deployed services.</span></span>

## <span data-ttu-id="8593c-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8593c-105">SYNTAX</span></span>

### <span data-ttu-id="8593c-106">ByResourceGroupAndCluster (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8593c-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8593c-107">ByName</span><span class="sxs-lookup"><span data-stu-id="8593c-107">ByName</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8593c-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8593c-108">ByResourceId</span></span>
```
Get-AzServiceFabricService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8593c-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8593c-109">DESCRIPTION</span></span>
<span data-ttu-id="8593c-110">Questo cmdlet otterrà i dettagli del servizio nell'applicazione e nel cluster specificati.</span><span class="sxs-lookup"><span data-stu-id="8593c-110">This cmdlet will get the service details in the specified application and cluster.</span></span>

## <span data-ttu-id="8593c-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8593c-111">EXAMPLES</span></span>

### <span data-ttu-id="8593c-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8593c-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService"
PS C:\> Get-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="8593c-113">Questo esempio recupera i dettagli delle risorse del servizio per il servizio "testApp~testService".</span><span class="sxs-lookup"><span data-stu-id="8593c-113">This example gets the service resource details for the service "testApp~testService".</span></span>

### <span data-ttu-id="8593c-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="8593c-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName
```

<span data-ttu-id="8593c-115">Questo esempio ottiene un elenco dei servizi nell'applicazione "testApp".</span><span class="sxs-lookup"><span data-stu-id="8593c-115">This example gets a list of the services under the application "testApp".</span></span>

## <span data-ttu-id="8593c-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8593c-116">PARAMETERS</span></span>

### <span data-ttu-id="8593c-117">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="8593c-117">-ApplicationName</span></span>
<span data-ttu-id="8593c-118">Specificare il nome dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8593c-118">Specify the name of the application.</span></span>

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

### <span data-ttu-id="8593c-119">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="8593c-119">-ClusterName</span></span>
<span data-ttu-id="8593c-120">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="8593c-120">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="8593c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8593c-121">-DefaultProfile</span></span>
<span data-ttu-id="8593c-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8593c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8593c-123">-Name</span><span class="sxs-lookup"><span data-stu-id="8593c-123">-Name</span></span>
<span data-ttu-id="8593c-124">Specificare il nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="8593c-124">Specify the name of the service.</span></span>

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

### <span data-ttu-id="8593c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8593c-125">-ResourceGroupName</span></span>
<span data-ttu-id="8593c-126">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8593c-126">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="8593c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8593c-127">-ResourceId</span></span>
<span data-ttu-id="8593c-128">Arm ResourceId del servizio.</span><span class="sxs-lookup"><span data-stu-id="8593c-128">Arm ResourceId of the service.</span></span>

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

### <span data-ttu-id="8593c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8593c-129">CommonParameters</span></span>
<span data-ttu-id="8593c-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8593c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8593c-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8593c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8593c-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="8593c-132">INPUTS</span></span>

### <span data-ttu-id="8593c-133">System.String</span><span class="sxs-lookup"><span data-stu-id="8593c-133">System.String</span></span>

## <span data-ttu-id="8593c-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8593c-134">OUTPUTS</span></span>

### <span data-ttu-id="8593c-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span><span class="sxs-lookup"><span data-stu-id="8593c-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="8593c-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="8593c-136">NOTES</span></span>

## <span data-ttu-id="8593c-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8593c-137">RELATED LINKS</span></span>
