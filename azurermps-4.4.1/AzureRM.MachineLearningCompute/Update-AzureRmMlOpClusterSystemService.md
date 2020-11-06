---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Update-AzureRmMlOpClusterSystemService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Update-AzureRmMlOpClusterSystemService.md
ms.openlocfilehash: fc89ff40c36fc444eec23089288849aa5ffe592c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521606"
---
# <span data-ttu-id="c5756-101">Update-AzureRmMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="c5756-101">Update-AzureRmMlOpClusterSystemService</span></span>

## <span data-ttu-id="c5756-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c5756-102">SYNOPSIS</span></span>
<span data-ttu-id="c5756-103">Avvia un aggiornamento sui servizi di sistema del cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="c5756-103">Starts an update on the operationalization cluster's system services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5756-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c5756-104">SYNTAX</span></span>

### <span data-ttu-id="c5756-105">Avviare un aggiornamento dei servizi di sistema dai parametri di input del cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5756-105">Start a system services update from cmdlet input parameters.</span></span>
```
Update-AzureRmMlOpClusterSystemService -ResourceGroupName <String> -Name <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="c5756-106">Avviare un aggiornamento di servizi di sistema da una definizione di istanza di PSOperationalizationCluster.</span><span class="sxs-lookup"><span data-stu-id="c5756-106">Start a system services update from an PSOperationalizationCluster instance definition.</span></span>
```
Update-AzureRmMlOpClusterSystemService -InputObject <PSOperationalizationCluster> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="c5756-107">Avviare un aggiornamento di servizi di sistema da un ID di Azure resouce.</span><span class="sxs-lookup"><span data-stu-id="c5756-107">Start a system services update from an Azure resouce id.</span></span>
```
Update-AzureRmMlOpClusterSystemService -ResourceId <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="c5756-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c5756-108">DESCRIPTION</span></span>
<span data-ttu-id="c5756-109">I servizi di sistema possono essere aggiornati in modo indipendente dal cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="c5756-109">The system services can be updated independently from the operationalization cluster.</span></span> <span data-ttu-id="c5756-110">Per avviare un aggiornamento in servizi di sistema, usare questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5756-110">To start an update on the system services use this cmdlet.</span></span> <span data-ttu-id="c5756-111">Se non è disponibile alcun aggiornamento, l'aggiornamento verrà ancora avviato e verrà restituito correttamente.</span><span class="sxs-lookup"><span data-stu-id="c5756-111">If no update is available an update will still be started and will return successfully.</span></span> <span data-ttu-id="c5756-112">Una volta terminato l'aggiornamento, viene segnalato quando è stato avviato, terminato e se ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="c5756-112">Once the update is finished it reports when it started, finished, and if it was successful.</span></span>

## <span data-ttu-id="c5756-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c5756-113">EXAMPLES</span></span>

### <span data-ttu-id="c5756-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c5756-114">Example 1</span></span>
```
PS C:\> Update-AzureRmMlOpClusterSystemService -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="c5756-115">Avvia un aggiornamento di servizi di sistema nel cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="c5756-115">Starts a system services update on the specified cluster.</span></span> 

## <span data-ttu-id="c5756-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c5756-116">PARAMETERS</span></span>

### <span data-ttu-id="c5756-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c5756-117">-InputObject</span></span>
<span data-ttu-id="c5756-118">Oggetto cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="c5756-118">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Start a system services update from an PSOperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5756-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c5756-119">-Confirm</span></span>
<span data-ttu-id="c5756-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5756-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5756-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="c5756-121">-Name</span></span>
<span data-ttu-id="c5756-122">Nome del cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="c5756-122">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Start a system services update from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5756-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5756-123">-ResourceGroupName</span></span>
<span data-ttu-id="c5756-124">Nome del gruppo di risorse per il cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="c5756-124">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Start a system services update from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5756-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5756-125">-ResourceId</span></span>
<span data-ttu-id="c5756-126">ID risorsa Azure per il cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="c5756-126">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Start a system services update from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5756-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5756-127">-WhatIf</span></span>
<span data-ttu-id="c5756-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c5756-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5756-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c5756-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="c5756-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c5756-130">INPUTS</span></span>

### <span data-ttu-id="c5756-131">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="c5756-131">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
### <span data-ttu-id="c5756-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c5756-132">System.String</span></span>


## <span data-ttu-id="c5756-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c5756-133">OUTPUTS</span></span>

### <span data-ttu-id="c5756-134">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSUpdateSystemServicesResponse</span><span class="sxs-lookup"><span data-stu-id="c5756-134">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSUpdateSystemServicesResponse</span></span>


## <span data-ttu-id="c5756-135">Note</span><span class="sxs-lookup"><span data-stu-id="c5756-135">NOTES</span></span>

## <span data-ttu-id="c5756-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c5756-136">RELATED LINKS</span></span>

