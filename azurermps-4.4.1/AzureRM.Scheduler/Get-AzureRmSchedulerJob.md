---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: DC151161-72C0-40F7-B2F0-45FA01142AE1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJob.md
ms.openlocfilehash: 3357eb154f21bc57de6ef60b243571e05bc0c22a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687086"
---
# <span data-ttu-id="81ce8-101">Get-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="81ce8-101">Get-AzureRmSchedulerJob</span></span>

## <span data-ttu-id="81ce8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="81ce8-102">SYNOPSIS</span></span>
<span data-ttu-id="81ce8-103">Ottiene i processi dell'utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="81ce8-103">Gets Scheduler jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81ce8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="81ce8-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJob -ResourceGroupName <String> -JobCollectionName <String> [-JobName <String>]
 [-JobState <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81ce8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="81ce8-105">DESCRIPTION</span></span>
<span data-ttu-id="81ce8-106">Il cmdlet **Get-AzureRmSchedulerJob** ottiene i processi di pianificazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="81ce8-106">The **Get-AzureRmSchedulerJob** cmdlet gets Azure Scheduler jobs.</span></span>

## <span data-ttu-id="81ce8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="81ce8-107">EXAMPLES</span></span>

## <span data-ttu-id="81ce8-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="81ce8-108">PARAMETERS</span></span>

### <span data-ttu-id="81ce8-109">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="81ce8-109">-JobCollectionName</span></span>
<span data-ttu-id="81ce8-110">Specifica il nome di una raccolta processo che contiene i processi da ottenere.</span><span class="sxs-lookup"><span data-stu-id="81ce8-110">Specifies the name of a job collection that contains jobs to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81ce8-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="81ce8-111">-JobName</span></span>
<span data-ttu-id="81ce8-112">Specifica il nome di un processo da ottenere.</span><span class="sxs-lookup"><span data-stu-id="81ce8-112">Specifies the name of a job to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81ce8-113">-JobState</span><span class="sxs-lookup"><span data-stu-id="81ce8-113">-JobState</span></span>
<span data-ttu-id="81ce8-114">Specifica uno stato di lavoro per ottenere i processi.</span><span class="sxs-lookup"><span data-stu-id="81ce8-114">Specifies a job state of jobs to get.</span></span>
<span data-ttu-id="81ce8-115">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="81ce8-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="81ce8-116">Abilitato</span><span class="sxs-lookup"><span data-stu-id="81ce8-116">Enabled</span></span> 
- <span data-ttu-id="81ce8-117">Disabilitato</span><span class="sxs-lookup"><span data-stu-id="81ce8-117">Disabled</span></span> 
- <span data-ttu-id="81ce8-118">Faulted</span><span class="sxs-lookup"><span data-stu-id="81ce8-118">Faulted</span></span> 
- <span data-ttu-id="81ce8-119">Completato</span><span class="sxs-lookup"><span data-stu-id="81ce8-119">Completed</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled, Faulted, Completed

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81ce8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81ce8-120">-ResourceGroupName</span></span>
<span data-ttu-id="81ce8-121">Specifica il gruppo di risorse dei processi da ottenere.</span><span class="sxs-lookup"><span data-stu-id="81ce8-121">Specifies the resource group of the jobs to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81ce8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81ce8-122">-DefaultProfile</span></span>
<span data-ttu-id="81ce8-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="81ce8-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81ce8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81ce8-124">CommonParameters</span></span>
<span data-ttu-id="81ce8-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81ce8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81ce8-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81ce8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81ce8-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="81ce8-127">INPUTS</span></span>

## <span data-ttu-id="81ce8-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="81ce8-128">OUTPUTS</span></span>

### <span data-ttu-id="81ce8-129">Microsoft. Azure. Commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="81ce8-129">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="81ce8-130">Note</span><span class="sxs-lookup"><span data-stu-id="81ce8-130">NOTES</span></span>

## <span data-ttu-id="81ce8-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="81ce8-131">RELATED LINKS</span></span>

[<span data-ttu-id="81ce8-132">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="81ce8-132">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="81ce8-133">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="81ce8-133">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="81ce8-134">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="81ce8-134">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="81ce8-135">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="81ce8-135">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="81ce8-136">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="81ce8-136">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="81ce8-137">Remove-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="81ce8-137">Remove-AzureRmSchedulerJob</span></span>](./Remove-AzureRmSchedulerJob.md)

[<span data-ttu-id="81ce8-138">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="81ce8-138">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="81ce8-139">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="81ce8-139">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="81ce8-140">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="81ce8-140">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="81ce8-141">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="81ce8-141">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


