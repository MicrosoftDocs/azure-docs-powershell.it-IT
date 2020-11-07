---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlopclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlOpClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlOpClusterKey.md
ms.openlocfilehash: d8b8a333b4d009ee1b40a8b4ddc6ed49850f1a11
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835311"
---
# <span data-ttu-id="43dac-101">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="43dac-101">Get-AzMlOpClusterKey</span></span>

## <span data-ttu-id="43dac-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="43dac-102">SYNOPSIS</span></span>
<span data-ttu-id="43dac-103">Ottiene i tasti di scelta associati a un cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="43dac-103">Gets the access keys associated with an operationalization cluster.</span></span>

## <span data-ttu-id="43dac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="43dac-104">SYNTAX</span></span>

### <span data-ttu-id="43dac-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="43dac-105">GetByNameAndResourceGroup</span></span>
```
Get-AzMlOpClusterKey -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="43dac-106">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="43dac-106">GetByInputObject</span></span>
```
Get-AzMlOpClusterKey -InputObject <PSOperationalizationCluster> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="43dac-107">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="43dac-107">GetByResourceId</span></span>
```
Get-AzMlOpClusterKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43dac-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43dac-108">DESCRIPTION</span></span>
<span data-ttu-id="43dac-109">Quando si ottengono le proprietà del cluster, le chiavi per l'account di archiviazione, il registro dei contenitori e altri servizi associati al cluster di operatività non vengono restituiti.</span><span class="sxs-lookup"><span data-stu-id="43dac-109">The keys for the storage account, container registry, and other services associated with the operationalization cluster are not returned when getting the cluster properties.</span></span> <span data-ttu-id="43dac-110">Una chiamata specifica per recuperare le chiavi deve essere eseguita perché sono informazioni riservate.</span><span class="sxs-lookup"><span data-stu-id="43dac-110">A specific call to retrieve the keys must be made since they are sensitive information.</span></span>

## <span data-ttu-id="43dac-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="43dac-111">EXAMPLES</span></span>

### <span data-ttu-id="43dac-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="43dac-112">Example 1</span></span>
```
PS C:\> Get-AzMlOpClusterKey -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="43dac-113">Restituisce le chiavi segrete per i servizi associati al cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="43dac-113">Returns the secret keys for the services associated with the operationalization cluster.</span></span>

## <span data-ttu-id="43dac-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="43dac-114">PARAMETERS</span></span>

### <span data-ttu-id="43dac-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43dac-115">-DefaultProfile</span></span>
<span data-ttu-id="43dac-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="43dac-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43dac-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43dac-117">-InputObject</span></span>
<span data-ttu-id="43dac-118">Oggetto cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="43dac-118">The operationalization cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: GetByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43dac-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="43dac-119">-Name</span></span>
<span data-ttu-id="43dac-120">Nome del cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="43dac-120">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43dac-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43dac-121">-ResourceGroupName</span></span>
<span data-ttu-id="43dac-122">Nome del gruppo di risorse per il cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="43dac-122">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43dac-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43dac-123">-ResourceId</span></span>
<span data-ttu-id="43dac-124">ID risorsa Azure per il cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="43dac-124">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43dac-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43dac-125">CommonParameters</span></span>
<span data-ttu-id="43dac-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43dac-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43dac-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43dac-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43dac-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="43dac-128">INPUTS</span></span>

### <span data-ttu-id="43dac-129">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="43dac-129">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="43dac-130">System. String</span><span class="sxs-lookup"><span data-stu-id="43dac-130">System.String</span></span>

## <span data-ttu-id="43dac-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="43dac-131">OUTPUTS</span></span>

### <span data-ttu-id="43dac-132">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationClusterCredentials</span><span class="sxs-lookup"><span data-stu-id="43dac-132">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationClusterCredentials</span></span>

## <span data-ttu-id="43dac-133">Note</span><span class="sxs-lookup"><span data-stu-id="43dac-133">NOTES</span></span>

## <span data-ttu-id="43dac-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="43dac-134">RELATED LINKS</span></span>
