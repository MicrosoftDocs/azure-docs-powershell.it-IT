---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
ms.openlocfilehash: e78580f98ae0569a2104a4d39123070e7383fa6f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022249"
---
# <span data-ttu-id="f6a86-101">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="f6a86-101">Get-AzServiceFabricApplication</span></span>

## <span data-ttu-id="f6a86-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f6a86-102">SYNOPSIS</span></span>
<span data-ttu-id="f6a86-103">Ottenere i dettagli delle applicazioni in tessuto di servizio.</span><span class="sxs-lookup"><span data-stu-id="f6a86-103">Get Service Fabric application details.</span></span>

## <span data-ttu-id="f6a86-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f6a86-104">SYNTAX</span></span>

### <span data-ttu-id="f6a86-105">ByResourceGroupAndCluster (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f6a86-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6a86-106">ByName</span><span class="sxs-lookup"><span data-stu-id="f6a86-106">ByName</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6a86-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f6a86-107">ByResourceId</span></span>
```
Get-AzServiceFabricApplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f6a86-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f6a86-108">DESCRIPTION</span></span>
<span data-ttu-id="f6a86-109">Questo cmdlet consente di ottenere i dettagli dell'applicazione nel gruppo di risorse e nel cluster specificati.</span><span class="sxs-lookup"><span data-stu-id="f6a86-109">This cmdlet gets the application details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="f6a86-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f6a86-110">EXAMPLES</span></span>

### <span data-ttu-id="f6a86-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f6a86-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="f6a86-112">Questo esempio consente di ottenere i dettagli delle risorse dell'applicazione per l'applicazione "testApp".</span><span class="sxs-lookup"><span data-stu-id="f6a86-112">This example gets the application resource details for the application "testApp".</span></span>

### <span data-ttu-id="f6a86-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f6a86-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="f6a86-114">Questo esempio consente di ottenere un elenco delle applicazioni sotto il cluster "testCluster".</span><span class="sxs-lookup"><span data-stu-id="f6a86-114">This example gets a list of the applications under the cluster "testCluster".</span></span>

## <span data-ttu-id="f6a86-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f6a86-115">PARAMETERS</span></span>

### <span data-ttu-id="f6a86-116">-Clustername</span><span class="sxs-lookup"><span data-stu-id="f6a86-116">-ClusterName</span></span>
<span data-ttu-id="f6a86-117">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="f6a86-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="f6a86-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6a86-118">-DefaultProfile</span></span>
<span data-ttu-id="f6a86-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f6a86-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6a86-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="f6a86-120">-Name</span></span>
<span data-ttu-id="f6a86-121">Specificare il nome dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f6a86-121">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ApplicationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6a86-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6a86-122">-ResourceGroupName</span></span>
<span data-ttu-id="f6a86-123">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f6a86-123">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="f6a86-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f6a86-124">-ResourceId</span></span>
<span data-ttu-id="f6a86-125">ARM ResourceId dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f6a86-125">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="f6a86-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6a86-126">CommonParameters</span></span>
<span data-ttu-id="f6a86-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6a86-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6a86-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6a86-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6a86-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f6a86-129">INPUTS</span></span>

### <span data-ttu-id="f6a86-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f6a86-130">System.String</span></span>

## <span data-ttu-id="f6a86-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f6a86-131">OUTPUTS</span></span>

### <span data-ttu-id="f6a86-132">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="f6a86-132">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="f6a86-133">Note</span><span class="sxs-lookup"><span data-stu-id="f6a86-133">NOTES</span></span>

## <span data-ttu-id="f6a86-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f6a86-134">RELATED LINKS</span></span>
