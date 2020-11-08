---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
ms.openlocfilehash: c282ea9e902f26d010c2421339de68bc670e2f35
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188815"
---
# <span data-ttu-id="38c46-101">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="38c46-101">Get-AzServiceFabricApplication</span></span>

## <span data-ttu-id="38c46-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="38c46-102">SYNOPSIS</span></span>
<span data-ttu-id="38c46-103">Ottenere i dettagli delle applicazioni in tessuto di servizio.</span><span class="sxs-lookup"><span data-stu-id="38c46-103">Get Service Fabric application details.</span></span>

## <span data-ttu-id="38c46-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="38c46-104">SYNTAX</span></span>

### <span data-ttu-id="38c46-105">ByResourceGroupAndCluster (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="38c46-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38c46-106">ByName</span><span class="sxs-lookup"><span data-stu-id="38c46-106">ByName</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38c46-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="38c46-107">ByResourceId</span></span>
```
Get-AzServiceFabricApplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="38c46-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="38c46-108">DESCRIPTION</span></span>
<span data-ttu-id="38c46-109">Questo cmdlet consente di ottenere i dettagli dell'applicazione nel gruppo di risorse e nel cluster specificati.</span><span class="sxs-lookup"><span data-stu-id="38c46-109">This cmdlet gets the application details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="38c46-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="38c46-110">EXAMPLES</span></span>

### <span data-ttu-id="38c46-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="38c46-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="38c46-112">Questo esempio consente di ottenere i dettagli delle risorse dell'applicazione per l'applicazione "testApp".</span><span class="sxs-lookup"><span data-stu-id="38c46-112">This example gets the application resource details for the application "testApp".</span></span>

### <span data-ttu-id="38c46-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="38c46-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="38c46-114">Questo esempio consente di ottenere un elenco delle applicazioni sotto il cluster "testCluster".</span><span class="sxs-lookup"><span data-stu-id="38c46-114">This example gets a list of the applications under the cluster "testCluster".</span></span>

## <span data-ttu-id="38c46-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="38c46-115">PARAMETERS</span></span>

### <span data-ttu-id="38c46-116">-Clustername</span><span class="sxs-lookup"><span data-stu-id="38c46-116">-ClusterName</span></span>
<span data-ttu-id="38c46-117">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="38c46-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="38c46-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38c46-118">-DefaultProfile</span></span>
<span data-ttu-id="38c46-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="38c46-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38c46-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="38c46-120">-Name</span></span>
<span data-ttu-id="38c46-121">Specificare il nome dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="38c46-121">Specify the name of the application.</span></span>

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

### <span data-ttu-id="38c46-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38c46-122">-ResourceGroupName</span></span>
<span data-ttu-id="38c46-123">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="38c46-123">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="38c46-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38c46-124">-ResourceId</span></span>
<span data-ttu-id="38c46-125">ARM ResourceId dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="38c46-125">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="38c46-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38c46-126">CommonParameters</span></span>
<span data-ttu-id="38c46-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38c46-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38c46-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38c46-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38c46-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="38c46-129">INPUTS</span></span>

### <span data-ttu-id="38c46-130">System. String</span><span class="sxs-lookup"><span data-stu-id="38c46-130">System.String</span></span>

## <span data-ttu-id="38c46-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="38c46-131">OUTPUTS</span></span>

### <span data-ttu-id="38c46-132">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="38c46-132">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="38c46-133">Note</span><span class="sxs-lookup"><span data-stu-id="38c46-133">NOTES</span></span>

## <span data-ttu-id="38c46-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="38c46-134">RELATED LINKS</span></span>