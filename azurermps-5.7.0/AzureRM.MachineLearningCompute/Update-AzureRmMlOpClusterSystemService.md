---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/update-azurermmlopclustersystemservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Update-AzureRmMlOpClusterSystemService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Update-AzureRmMlOpClusterSystemService.md
ms.openlocfilehash: 01f826746b92dd5aa82416e8207305b945ddb711
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686509"
---
# <span data-ttu-id="61f8e-101">Update-AzureRmMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="61f8e-101">Update-AzureRmMlOpClusterSystemService</span></span>

## <span data-ttu-id="61f8e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="61f8e-102">SYNOPSIS</span></span>
<span data-ttu-id="61f8e-103">Avvia un aggiornamento sui servizi di sistema del cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="61f8e-103">Starts an update on the operationalization cluster's system services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61f8e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="61f8e-104">SYNTAX</span></span>

### <span data-ttu-id="61f8e-105">StartUpdateWithNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="61f8e-105">StartUpdateWithNameAndResourceGroup</span></span>
```
Update-AzureRmMlOpClusterSystemService -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61f8e-106">StartUpdateWithInputObject</span><span class="sxs-lookup"><span data-stu-id="61f8e-106">StartUpdateWithInputObject</span></span>
```
Update-AzureRmMlOpClusterSystemService -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61f8e-107">StartUpdateWithResourceId</span><span class="sxs-lookup"><span data-stu-id="61f8e-107">StartUpdateWithResourceId</span></span>
```
Update-AzureRmMlOpClusterSystemService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61f8e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61f8e-108">DESCRIPTION</span></span>
<span data-ttu-id="61f8e-109">I servizi di sistema possono essere aggiornati in modo indipendente dal cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="61f8e-109">The system services can be updated independently from the operationalization cluster.</span></span> <span data-ttu-id="61f8e-110">Per avviare un aggiornamento in servizi di sistema, usare questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61f8e-110">To start an update on the system services use this cmdlet.</span></span> <span data-ttu-id="61f8e-111">Se non è disponibile alcun aggiornamento, l'aggiornamento verrà ancora avviato e verrà restituito correttamente.</span><span class="sxs-lookup"><span data-stu-id="61f8e-111">If no update is available an update will still be started and will return successfully.</span></span> <span data-ttu-id="61f8e-112">Una volta terminato l'aggiornamento, viene segnalato quando è stato avviato, terminato e se ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="61f8e-112">Once the update is finished it reports when it started, finished, and if it was successful.</span></span>

## <span data-ttu-id="61f8e-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="61f8e-113">EXAMPLES</span></span>

### <span data-ttu-id="61f8e-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="61f8e-114">Example 1</span></span>
```
PS C:\> Update-AzureRmMlOpClusterSystemService -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="61f8e-115">Avvia un aggiornamento di servizi di sistema nel cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="61f8e-115">Starts a system services update on the specified cluster.</span></span> 

## <span data-ttu-id="61f8e-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="61f8e-116">PARAMETERS</span></span>

### <span data-ttu-id="61f8e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61f8e-117">-DefaultProfile</span></span>
<span data-ttu-id="61f8e-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="61f8e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61f8e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61f8e-119">-InputObject</span></span>
<span data-ttu-id="61f8e-120">Oggetto cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="61f8e-120">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: StartUpdateWithInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61f8e-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="61f8e-121">-Name</span></span>
<span data-ttu-id="61f8e-122">Nome del cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="61f8e-122">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: StartUpdateWithNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61f8e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61f8e-123">-ResourceGroupName</span></span>
<span data-ttu-id="61f8e-124">Nome del gruppo di risorse per il cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="61f8e-124">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: StartUpdateWithNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61f8e-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="61f8e-125">-ResourceId</span></span>
<span data-ttu-id="61f8e-126">ID risorsa Azure per il cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="61f8e-126">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: StartUpdateWithResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f8e-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="61f8e-127">-Confirm</span></span>
<span data-ttu-id="61f8e-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61f8e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61f8e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61f8e-129">-WhatIf</span></span>
<span data-ttu-id="61f8e-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="61f8e-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61f8e-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="61f8e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61f8e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61f8e-132">CommonParameters</span></span>
<span data-ttu-id="61f8e-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61f8e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61f8e-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61f8e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61f8e-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="61f8e-135">INPUTS</span></span>

### <span data-ttu-id="61f8e-136">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="61f8e-136">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="61f8e-137">System. String</span><span class="sxs-lookup"><span data-stu-id="61f8e-137">System.String</span></span>

## <span data-ttu-id="61f8e-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="61f8e-138">OUTPUTS</span></span>

### <span data-ttu-id="61f8e-139">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSUpdateSystemServicesResponse</span><span class="sxs-lookup"><span data-stu-id="61f8e-139">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSUpdateSystemServicesResponse</span></span>

## <span data-ttu-id="61f8e-140">Note</span><span class="sxs-lookup"><span data-stu-id="61f8e-140">NOTES</span></span>

## <span data-ttu-id="61f8e-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="61f8e-141">RELATED LINKS</span></span>

