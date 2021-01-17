---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
ms.openlocfilehash: d6a17588b5718f9a6d735521a7a136cba472ead0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478188"
---
# <span data-ttu-id="303fe-101">Set-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="303fe-101">Set-AzBatchJobSchedule</span></span>

## <span data-ttu-id="303fe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="303fe-102">SYNOPSIS</span></span>
<span data-ttu-id="303fe-103">Imposta una pianificazione del processo.</span><span class="sxs-lookup"><span data-stu-id="303fe-103">Sets a job schedule.</span></span>

## <span data-ttu-id="303fe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="303fe-104">SYNTAX</span></span>

```
Set-AzBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="303fe-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="303fe-105">DESCRIPTION</span></span>
<span data-ttu-id="303fe-106">Il cmdlet **set-AzBatchJobSchedule** imposta una pianificazione dei processi nel servizio batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="303fe-106">The **Set-AzBatchJobSchedule** cmdlet sets a job schedule in the Azure Batch service.</span></span>

## <span data-ttu-id="303fe-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="303fe-107">EXAMPLES</span></span>

### <span data-ttu-id="303fe-108">Esempio 1: aggiornare una pianificazione del processo</span><span class="sxs-lookup"><span data-stu-id="303fe-108">Example 1: Update a job schedule</span></span>
```
PS C:\> $JobSchedule = Get-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context
PS C:\> $JobSchedule.Schedule.RecurrenceInterval = New-TimeSpan -Days 2
PS C:\> Set-AzBatchJobSchedule -JobSchedule $Job -BatchContext $Context
```

<span data-ttu-id="303fe-109">Il primo comando ottiene un processo utilizzando **Get-AzBatchJobSchedule** e lo archivia nella variabile $JobSchedule.</span><span class="sxs-lookup"><span data-stu-id="303fe-109">The first command gets a job by using **Get-AzBatchJobSchedule**, and then stores it in the $JobSchedule variable.</span></span>
<span data-ttu-id="303fe-110">Il secondo comando modifica l'intervallo di ricorrenza nell' `$JobSchedule.Schedule` oggetto.</span><span class="sxs-lookup"><span data-stu-id="303fe-110">The second command modifies the recurrence interval on the `$JobSchedule.Schedule` object.</span></span>
<span data-ttu-id="303fe-111">Il comando finale aggiorna il servizio batch in base all'oggetto locale in $JobSchedule.</span><span class="sxs-lookup"><span data-stu-id="303fe-111">The final command updates the Batch service to match the local object in $JobSchedule.</span></span>

## <span data-ttu-id="303fe-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="303fe-112">PARAMETERS</span></span>

### <span data-ttu-id="303fe-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="303fe-113">-BatchContext</span></span>
<span data-ttu-id="303fe-114">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="303fe-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="303fe-115">Se si usa il cmdlet Get-AzBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="303fe-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="303fe-116">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="303fe-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="303fe-117">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="303fe-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="303fe-118">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="303fe-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="303fe-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="303fe-119">-DefaultProfile</span></span>
<span data-ttu-id="303fe-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="303fe-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="303fe-121">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="303fe-121">-JobSchedule</span></span>
<span data-ttu-id="303fe-122">Specifica un oggetto **PSCloudJobSchedule** che rappresenta una pianificazione del processo.</span><span class="sxs-lookup"><span data-stu-id="303fe-122">Specifies a **PSCloudJobSchedule** object that represents a job schedule.</span></span>
<span data-ttu-id="303fe-123">Per ottenere un oggetto **PSCloudJobSchedule** , usa il cmdlet Get-AzBatchJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="303fe-123">To obtain a **PSCloudJobSchedule** object, use the Get-AzBatchJobSchedule cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="303fe-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="303fe-124">CommonParameters</span></span>
<span data-ttu-id="303fe-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="303fe-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="303fe-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="303fe-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="303fe-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="303fe-127">INPUTS</span></span>

### <span data-ttu-id="303fe-128">Microsoft.Azure.Commands.Batch. Models. PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="303fe-128">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

### <span data-ttu-id="303fe-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="303fe-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="303fe-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="303fe-130">OUTPUTS</span></span>

### <span data-ttu-id="303fe-131">System. void</span><span class="sxs-lookup"><span data-stu-id="303fe-131">System.Void</span></span>

## <span data-ttu-id="303fe-132">Note</span><span class="sxs-lookup"><span data-stu-id="303fe-132">NOTES</span></span>

## <span data-ttu-id="303fe-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="303fe-133">RELATED LINKS</span></span>

[<span data-ttu-id="303fe-134">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="303fe-134">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="303fe-135">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="303fe-135">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="303fe-136">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="303fe-136">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="303fe-137">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="303fe-137">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="303fe-138">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="303fe-138">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="303fe-139">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="303fe-139">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)


