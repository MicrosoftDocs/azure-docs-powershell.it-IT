---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Test-AzureRmMlOpClusterSystemServicesUpdateAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Test-AzureRmMlOpClusterSystemServicesUpdateAvailability.md
ms.openlocfilehash: 067fdf88b7a7b29007f81ab26590ffaa542ac7e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686822"
---
# <span data-ttu-id="f09e4-101">Test-AzureRmMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="f09e4-101">Test-AzureRmMlOpClusterSystemServicesUpdateAvailability</span></span>

## <span data-ttu-id="f09e4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f09e4-102">SYNOPSIS</span></span>
<span data-ttu-id="f09e4-103">Controlla se sono disponibili aggiornamenti per i servizi di sistema associati a un cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="f09e4-103">Checks if there are updates available for the system services associated with an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f09e4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f09e4-104">SYNTAX</span></span>

### <span data-ttu-id="f09e4-105">Verificare la disponibilità degli aggiornamenti dai parametri di input dei cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f09e4-105">Test for update availability from cmdlet input parameters.</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName <String> -Name <String>
```

### <span data-ttu-id="f09e4-106">Verificare la disponibilità degli aggiornamenti da una definizione di istanza di OperationalizationCluster.</span><span class="sxs-lookup"><span data-stu-id="f09e4-106">Test for update availability from an OperationalizationCluster instance definition.</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -InputObject <PSOperationalizationCluster>
```

### <span data-ttu-id="f09e4-107">Verificare la disponibilità degli aggiornamenti da un ID di Azure resouce.</span><span class="sxs-lookup"><span data-stu-id="f09e4-107">Test for update availability from an Azure resouce id.</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceId <String>
```

## <span data-ttu-id="f09e4-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f09e4-108">DESCRIPTION</span></span>
<span data-ttu-id="f09e4-109">I servizi di sistema ricevono gli aggiornamenti in modo indipendente dal cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="f09e4-109">System services receive updates independently from the operationalization cluster.</span></span> <span data-ttu-id="f09e4-110">L'uso di questo cmdlet consentirà all'utente di sapere se Invoke-AzureRmMlOpClusterSystemServicesUpdate.</span><span class="sxs-lookup"><span data-stu-id="f09e4-110">Using this cmdlet will let the user know if Invoke-AzureRmMlOpClusterSystemServicesUpdate.</span></span>

## <span data-ttu-id="f09e4-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f09e4-111">EXAMPLES</span></span>

### <span data-ttu-id="f09e4-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f09e4-112">Example 1</span></span>
```
PS C:\> Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="f09e4-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f09e4-113">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster | Test-AzureRmMlOpClusterSystemServicesUpdateAvailability
```

### <span data-ttu-id="f09e4-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="f09e4-114">Example 3</span></span>
```
PS C:\> Find-AzureRmResource -ResourceType Microsoft.MachineLearningCompute/operationalizationClusters | Test-AzureRmMlOpClusterSystemServicesUpdateAvailability
```

## <span data-ttu-id="f09e4-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f09e4-115">PARAMETERS</span></span>

### <span data-ttu-id="f09e4-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f09e4-116">-InputObject</span></span>
<span data-ttu-id="f09e4-117">Oggetto cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="f09e4-117">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Test for update availability from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f09e4-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="f09e4-118">-Name</span></span>
<span data-ttu-id="f09e4-119">Nome del cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="f09e4-119">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Test for update availability from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f09e4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f09e4-120">-ResourceGroupName</span></span>
<span data-ttu-id="f09e4-121">Nome del gruppo di risorse per il cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="f09e4-121">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Test for update availability from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f09e4-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f09e4-122">-ResourceId</span></span>
<span data-ttu-id="f09e4-123">ID risorsa Azure per il cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="f09e4-123">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Test for update availability from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="f09e4-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f09e4-124">INPUTS</span></span>

### <span data-ttu-id="f09e4-125">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="f09e4-125">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
### <span data-ttu-id="f09e4-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f09e4-126">System.String</span></span>


## <span data-ttu-id="f09e4-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f09e4-127">OUTPUTS</span></span>

### <span data-ttu-id="f09e4-128">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSCheckSystemServicesUpdatesAvailableResponse</span><span class="sxs-lookup"><span data-stu-id="f09e4-128">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSCheckSystemServicesUpdatesAvailableResponse</span></span>


## <span data-ttu-id="f09e4-129">Note</span><span class="sxs-lookup"><span data-stu-id="f09e4-129">NOTES</span></span>

## <span data-ttu-id="f09e4-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f09e4-130">RELATED LINKS</span></span>

