---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/get-azurermmlopclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
ms.openlocfilehash: cdf8c04a3d3b3b9fc50e571642bc14352d976b84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519434"
---
# <span data-ttu-id="aea04-101">Get-AzureRmMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="aea04-101">Get-AzureRmMlOpClusterKey</span></span>

## <span data-ttu-id="aea04-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aea04-102">SYNOPSIS</span></span>
<span data-ttu-id="aea04-103">Ottiene i tasti di scelta associati a un cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="aea04-103">Gets the access keys associated with an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aea04-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aea04-104">SYNTAX</span></span>

### <span data-ttu-id="aea04-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="aea04-105">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmMlOpClusterKey -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="aea04-106">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="aea04-106">GetByInputObject</span></span>
```
Get-AzureRmMlOpClusterKey -InputObject <PSOperationalizationCluster> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="aea04-107">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="aea04-107">GetByResourceId</span></span>
```
Get-AzureRmMlOpClusterKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aea04-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aea04-108">DESCRIPTION</span></span>
<span data-ttu-id="aea04-109">Quando si ottengono le proprietà del cluster, le chiavi per l'account di archiviazione, il registro dei contenitori e altri servizi associati al cluster di operatività non vengono restituiti.</span><span class="sxs-lookup"><span data-stu-id="aea04-109">The keys for the storage account, container registry, and other services associated with the operationalization cluster are not returned when getting the cluster properties.</span></span> <span data-ttu-id="aea04-110">Una chiamata specifica per recuperare le chiavi deve essere eseguita perché sono informazioni riservate.</span><span class="sxs-lookup"><span data-stu-id="aea04-110">A specific call to retrieve the keys must be made since they are sensitive information.</span></span>

## <span data-ttu-id="aea04-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aea04-111">EXAMPLES</span></span>

### <span data-ttu-id="aea04-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="aea04-112">Example 1</span></span>
```
PS C:\> Get-AzureRmMlOpClusterKey -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="aea04-113">Restituisce le chiavi segrete per i servizi associati al cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="aea04-113">Returns the secret keys for the services associated with the operationalization cluster.</span></span>

## <span data-ttu-id="aea04-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aea04-114">PARAMETERS</span></span>

### <span data-ttu-id="aea04-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aea04-115">-DefaultProfile</span></span>
<span data-ttu-id="aea04-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aea04-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aea04-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aea04-117">-InputObject</span></span>
<span data-ttu-id="aea04-118">Oggetto cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="aea04-118">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: GetByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aea04-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="aea04-119">-Name</span></span>
<span data-ttu-id="aea04-120">Nome del cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="aea04-120">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aea04-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aea04-121">-ResourceGroupName</span></span>
<span data-ttu-id="aea04-122">Nome del gruppo di risorse per il cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="aea04-122">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aea04-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aea04-123">-ResourceId</span></span>
<span data-ttu-id="aea04-124">ID risorsa Azure per il cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="aea04-124">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aea04-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aea04-125">CommonParameters</span></span>
<span data-ttu-id="aea04-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aea04-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aea04-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aea04-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aea04-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aea04-128">INPUTS</span></span>

### <span data-ttu-id="aea04-129">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="aea04-129">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
<span data-ttu-id="aea04-130">System. String</span><span class="sxs-lookup"><span data-stu-id="aea04-130">System.String</span></span>

## <span data-ttu-id="aea04-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aea04-131">OUTPUTS</span></span>

### <span data-ttu-id="aea04-132">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationClusterCredentials</span><span class="sxs-lookup"><span data-stu-id="aea04-132">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationClusterCredentials</span></span>

## <span data-ttu-id="aea04-133">Note</span><span class="sxs-lookup"><span data-stu-id="aea04-133">NOTES</span></span>

## <span data-ttu-id="aea04-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aea04-134">RELATED LINKS</span></span>

