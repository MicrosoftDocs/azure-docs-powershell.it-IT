---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/test-azurermmlopclustersystemservicesupdateavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Test-AzureRmMlOpClusterSystemServicesUpdateAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Test-AzureRmMlOpClusterSystemServicesUpdateAvailability.md
ms.openlocfilehash: 9832faaaaf1097f53aff841f8a455680b2a40a2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515143"
---
# <span data-ttu-id="fb579-101">Test-AzureRmMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="fb579-101">Test-AzureRmMlOpClusterSystemServicesUpdateAvailability</span></span>

## <span data-ttu-id="fb579-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fb579-102">SYNOPSIS</span></span>
<span data-ttu-id="fb579-103">Controlla se sono disponibili aggiornamenti per i servizi di sistema associati a un cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="fb579-103">Checks if there are updates available for the system services associated with an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb579-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fb579-104">SYNTAX</span></span>

### <span data-ttu-id="fb579-105">TestByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fb579-105">TestByNameAndResourceGroup</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb579-106">TestByInputObject</span><span class="sxs-lookup"><span data-stu-id="fb579-106">TestByInputObject</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb579-107">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="fb579-107">TestByResourceId</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb579-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fb579-108">DESCRIPTION</span></span>
<span data-ttu-id="fb579-109">I servizi di sistema ricevono gli aggiornamenti in modo indipendente dal cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="fb579-109">System services receive updates independently from the operationalization cluster.</span></span> <span data-ttu-id="fb579-110">L'uso di questo cmdlet consentirà all'utente di sapere se Invoke-AzureRmMlOpClusterSystemServicesUpdate.</span><span class="sxs-lookup"><span data-stu-id="fb579-110">Using this cmdlet will let the user know if Invoke-AzureRmMlOpClusterSystemServicesUpdate.</span></span>

## <span data-ttu-id="fb579-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fb579-111">EXAMPLES</span></span>

### <span data-ttu-id="fb579-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fb579-112">Example 1</span></span>
```
PS C:\> Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="fb579-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="fb579-113">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster | Test-AzureRmMlOpClusterSystemServicesUpdateAvailability
```

### <span data-ttu-id="fb579-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="fb579-114">Example 3</span></span>
```
PS C:\> Find-AzureRmResource -ResourceType Microsoft.MachineLearningCompute/operationalizationClusters | Test-AzureRmMlOpClusterSystemServicesUpdateAvailability
```

## <span data-ttu-id="fb579-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fb579-115">PARAMETERS</span></span>

### <span data-ttu-id="fb579-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb579-116">-DefaultProfile</span></span>
<span data-ttu-id="fb579-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fb579-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb579-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb579-118">-InputObject</span></span>
<span data-ttu-id="fb579-119">Oggetto cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="fb579-119">The operationalization cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: TestByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb579-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="fb579-120">-Name</span></span>
<span data-ttu-id="fb579-121">Nome del cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="fb579-121">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb579-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb579-122">-ResourceGroupName</span></span>
<span data-ttu-id="fb579-123">Nome del gruppo di risorse per il cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="fb579-123">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb579-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb579-124">-ResourceId</span></span>
<span data-ttu-id="fb579-125">ID risorsa Azure per il cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="fb579-125">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb579-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb579-126">CommonParameters</span></span>
<span data-ttu-id="fb579-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb579-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb579-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb579-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb579-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fb579-129">INPUTS</span></span>

### <span data-ttu-id="fb579-130">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="fb579-130">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
<span data-ttu-id="fb579-131">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fb579-131">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="fb579-132">System. String</span><span class="sxs-lookup"><span data-stu-id="fb579-132">System.String</span></span>

## <span data-ttu-id="fb579-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fb579-133">OUTPUTS</span></span>

### <span data-ttu-id="fb579-134">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSCheckSystemServicesUpdatesAvailableResponse</span><span class="sxs-lookup"><span data-stu-id="fb579-134">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSCheckSystemServicesUpdatesAvailableResponse</span></span>

## <span data-ttu-id="fb579-135">Note</span><span class="sxs-lookup"><span data-stu-id="fb579-135">NOTES</span></span>

## <span data-ttu-id="fb579-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fb579-136">RELATED LINKS</span></span>
