---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
ms.openlocfilehash: 73e89bcb6ffb6f8c09a0ec53f203b6ed251fd3e4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347848"
---
# <span data-ttu-id="44566-101">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="44566-101">Get-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="44566-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="44566-102">SYNOPSIS</span></span>
<span data-ttu-id="44566-103">Ottenere i dettagli del tipo di applicazione tessuto servizio.</span><span class="sxs-lookup"><span data-stu-id="44566-103">Get Service Fabric application type details.</span></span> <span data-ttu-id="44566-104">Supporta solo i tipi di applicazione distribuiti ARM.</span><span class="sxs-lookup"><span data-stu-id="44566-104">Only supports ARM deployed application types.</span></span>

## <span data-ttu-id="44566-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="44566-105">SYNTAX</span></span>

### <span data-ttu-id="44566-106">ByResourceGroupAndCluster (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="44566-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44566-107">ByName</span><span class="sxs-lookup"><span data-stu-id="44566-107">ByName</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44566-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="44566-108">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationType -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="44566-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="44566-109">DESCRIPTION</span></span>
<span data-ttu-id="44566-110">Questo cmdlet consente di ottenere i dettagli del tipo di applicazione nel gruppo di risorse e nel cluster specificati.</span><span class="sxs-lookup"><span data-stu-id="44566-110">Use this cmdlet to get the application type details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="44566-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="44566-111">EXAMPLES</span></span>

### <span data-ttu-id="44566-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="44566-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="44566-113">Questo esempio otterrà i dettagli del tipo di applicazione con i parametri specificati, se non trova la risorsa che genererà un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="44566-113">This example will get the application type details with the parameters specified, if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="44566-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="44566-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="44566-115">Questo esempio otterrà un elenco dei tipi di applicazione definiti nel cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="44566-115">This example will get a list of the application types defined under the specified cluster.</span></span>

## <span data-ttu-id="44566-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="44566-116">PARAMETERS</span></span>

### <span data-ttu-id="44566-117">-Clustername</span><span class="sxs-lookup"><span data-stu-id="44566-117">-ClusterName</span></span>
<span data-ttu-id="44566-118">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="44566-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="44566-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44566-119">-DefaultProfile</span></span>
<span data-ttu-id="44566-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="44566-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44566-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="44566-121">-Name</span></span>
<span data-ttu-id="44566-122">Specificare il nome del tipo di applicazione</span><span class="sxs-lookup"><span data-stu-id="44566-122">Specify the name of the application type</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ApplicationTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44566-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44566-123">-ResourceGroupName</span></span>
<span data-ttu-id="44566-124">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="44566-124">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="44566-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44566-125">-ResourceId</span></span>
<span data-ttu-id="44566-126">ARM ResourceId del tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="44566-126">Arm ResourceId of the application type.</span></span>

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

### <span data-ttu-id="44566-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44566-127">CommonParameters</span></span>
<span data-ttu-id="44566-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44566-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44566-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="44566-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44566-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="44566-130">INPUTS</span></span>

### <span data-ttu-id="44566-131">System. String</span><span class="sxs-lookup"><span data-stu-id="44566-131">System.String</span></span>

## <span data-ttu-id="44566-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="44566-132">OUTPUTS</span></span>

### <span data-ttu-id="44566-133">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="44566-133">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="44566-134">Note</span><span class="sxs-lookup"><span data-stu-id="44566-134">NOTES</span></span>

## <span data-ttu-id="44566-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="44566-135">RELATED LINKS</span></span>
