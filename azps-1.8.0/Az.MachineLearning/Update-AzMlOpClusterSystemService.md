---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/update-azmlopclustersystemservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlOpClusterSystemService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlOpClusterSystemService.md
ms.openlocfilehash: 0e673cd74d87cee990130c1fd58b9049eec9ff15
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835259"
---
# <span data-ttu-id="077fc-101">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="077fc-101">Update-AzMlOpClusterSystemService</span></span>

## <span data-ttu-id="077fc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="077fc-102">SYNOPSIS</span></span>
<span data-ttu-id="077fc-103">Avvia un aggiornamento sui servizi di sistema del cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="077fc-103">Starts an update on the operationalization cluster's system services.</span></span>

## <span data-ttu-id="077fc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="077fc-104">SYNTAX</span></span>

### <span data-ttu-id="077fc-105">StartUpdateWithNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="077fc-105">StartUpdateWithNameAndResourceGroup</span></span>
```
Update-AzMlOpClusterSystemService -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="077fc-106">StartUpdateWithInputObject</span><span class="sxs-lookup"><span data-stu-id="077fc-106">StartUpdateWithInputObject</span></span>
```
Update-AzMlOpClusterSystemService -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="077fc-107">StartUpdateWithResourceId</span><span class="sxs-lookup"><span data-stu-id="077fc-107">StartUpdateWithResourceId</span></span>
```
Update-AzMlOpClusterSystemService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="077fc-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="077fc-108">DESCRIPTION</span></span>
<span data-ttu-id="077fc-109">I servizi di sistema possono essere aggiornati in modo indipendente dal cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="077fc-109">The system services can be updated independently from the operationalization cluster.</span></span> <span data-ttu-id="077fc-110">Per avviare un aggiornamento in servizi di sistema, usare questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="077fc-110">To start an update on the system services use this cmdlet.</span></span> <span data-ttu-id="077fc-111">Se non è disponibile alcun aggiornamento, l'aggiornamento verrà ancora avviato e verrà restituito correttamente.</span><span class="sxs-lookup"><span data-stu-id="077fc-111">If no update is available an update will still be started and will return successfully.</span></span> <span data-ttu-id="077fc-112">Una volta terminato l'aggiornamento, viene segnalato quando è stato avviato, terminato e se ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="077fc-112">Once the update is finished it reports when it started, finished, and if it was successful.</span></span>

## <span data-ttu-id="077fc-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="077fc-113">EXAMPLES</span></span>

### <span data-ttu-id="077fc-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="077fc-114">Example 1</span></span>
```
PS C:\> Update-AzMlOpClusterSystemService -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="077fc-115">Avvia un aggiornamento di servizi di sistema nel cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="077fc-115">Starts a system services update on the specified cluster.</span></span> 

## <span data-ttu-id="077fc-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="077fc-116">PARAMETERS</span></span>

### <span data-ttu-id="077fc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="077fc-117">-DefaultProfile</span></span>
<span data-ttu-id="077fc-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="077fc-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="077fc-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="077fc-119">-InputObject</span></span>
<span data-ttu-id="077fc-120">Oggetto cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="077fc-120">The operationalization cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: StartUpdateWithInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="077fc-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="077fc-121">-Name</span></span>
<span data-ttu-id="077fc-122">Nome del cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="077fc-122">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: StartUpdateWithNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="077fc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="077fc-123">-ResourceGroupName</span></span>
<span data-ttu-id="077fc-124">Nome del gruppo di risorse per il cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="077fc-124">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: StartUpdateWithNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="077fc-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="077fc-125">-ResourceId</span></span>
<span data-ttu-id="077fc-126">ID risorsa Azure per il cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="077fc-126">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: StartUpdateWithResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="077fc-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="077fc-127">-Confirm</span></span>
<span data-ttu-id="077fc-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="077fc-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="077fc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="077fc-129">-WhatIf</span></span>
<span data-ttu-id="077fc-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="077fc-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="077fc-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="077fc-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="077fc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="077fc-132">CommonParameters</span></span>
<span data-ttu-id="077fc-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="077fc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="077fc-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="077fc-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="077fc-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="077fc-135">INPUTS</span></span>

### <span data-ttu-id="077fc-136">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="077fc-136">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="077fc-137">System. String</span><span class="sxs-lookup"><span data-stu-id="077fc-137">System.String</span></span>

## <span data-ttu-id="077fc-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="077fc-138">OUTPUTS</span></span>

### <span data-ttu-id="077fc-139">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSUpdateSystemServicesResponse</span><span class="sxs-lookup"><span data-stu-id="077fc-139">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSUpdateSystemServicesResponse</span></span>

## <span data-ttu-id="077fc-140">Note</span><span class="sxs-lookup"><span data-stu-id="077fc-140">NOTES</span></span>

## <span data-ttu-id="077fc-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="077fc-141">RELATED LINKS</span></span>
