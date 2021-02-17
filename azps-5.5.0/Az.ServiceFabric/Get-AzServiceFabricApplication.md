---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
ms.openlocfilehash: 5946be075e2b97283546614543d5a0d4544bfa0f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208067"
---
# <span data-ttu-id="56274-101">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="56274-101">Get-AzServiceFabricApplication</span></span>

## <span data-ttu-id="56274-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56274-102">SYNOPSIS</span></span>
<span data-ttu-id="56274-103">Ottenere i dettagli dell'applicazione Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="56274-103">Get Service Fabric application details.</span></span> <span data-ttu-id="56274-104">Supporta solo ARM applicazioni distribuite.</span><span class="sxs-lookup"><span data-stu-id="56274-104">Only supports ARM deployed applications.</span></span>

## <span data-ttu-id="56274-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="56274-105">SYNTAX</span></span>

### <span data-ttu-id="56274-106">ByResourceGroupAndCluster (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="56274-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56274-107">ByName</span><span class="sxs-lookup"><span data-stu-id="56274-107">ByName</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56274-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="56274-108">ByResourceId</span></span>
```
Get-AzServiceFabricApplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="56274-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="56274-109">DESCRIPTION</span></span>
<span data-ttu-id="56274-110">Questo cmdlet recupera i dettagli dell'applicazione nel gruppo di risorse e nel cluster specificati.</span><span class="sxs-lookup"><span data-stu-id="56274-110">This cmdlet gets the application details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="56274-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="56274-111">EXAMPLES</span></span>

### <span data-ttu-id="56274-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="56274-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="56274-113">Questo esempio recupera i dettagli delle risorse dell'applicazione per l'applicazione "testApp".</span><span class="sxs-lookup"><span data-stu-id="56274-113">This example gets the application resource details for the application "testApp".</span></span>

### <span data-ttu-id="56274-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="56274-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="56274-115">Questo esempio ottiene un elenco delle applicazioni nel cluster "testCluster".</span><span class="sxs-lookup"><span data-stu-id="56274-115">This example gets a list of the applications under the cluster "testCluster".</span></span>

## <span data-ttu-id="56274-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56274-116">PARAMETERS</span></span>

### <span data-ttu-id="56274-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="56274-117">-ClusterName</span></span>
<span data-ttu-id="56274-118">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="56274-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="56274-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56274-119">-DefaultProfile</span></span>
<span data-ttu-id="56274-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="56274-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56274-121">-Name</span><span class="sxs-lookup"><span data-stu-id="56274-121">-Name</span></span>
<span data-ttu-id="56274-122">Specificare il nome dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="56274-122">Specify the name of the application.</span></span>

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

### <span data-ttu-id="56274-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56274-123">-ResourceGroupName</span></span>
<span data-ttu-id="56274-124">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="56274-124">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="56274-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="56274-125">-ResourceId</span></span>
<span data-ttu-id="56274-126">Arm ResourceId dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="56274-126">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="56274-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56274-127">CommonParameters</span></span>
<span data-ttu-id="56274-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56274-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56274-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="56274-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56274-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="56274-130">INPUTS</span></span>

### <span data-ttu-id="56274-131">System.String</span><span class="sxs-lookup"><span data-stu-id="56274-131">System.String</span></span>

## <span data-ttu-id="56274-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="56274-132">OUTPUTS</span></span>

### <span data-ttu-id="56274-133">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="56274-133">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="56274-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="56274-134">NOTES</span></span>

## <span data-ttu-id="56274-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="56274-135">RELATED LINKS</span></span>
