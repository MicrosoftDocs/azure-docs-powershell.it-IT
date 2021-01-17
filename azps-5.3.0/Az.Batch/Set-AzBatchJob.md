---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 75483BC7-440A-437B-9EDE-D270D87CF3C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
ms.openlocfilehash: 1104eed4d60405226cdc6dad351ae418b84142e2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478191"
---
# <span data-ttu-id="96bbc-101">Set-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="96bbc-101">Set-AzBatchJob</span></span>

## <span data-ttu-id="96bbc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="96bbc-102">SYNOPSIS</span></span>
<span data-ttu-id="96bbc-103">Aggiorna un processo batch.</span><span class="sxs-lookup"><span data-stu-id="96bbc-103">Updates a Batch job.</span></span>

## <span data-ttu-id="96bbc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="96bbc-104">SYNTAX</span></span>

```
Set-AzBatchJob [-Job] <PSCloudJob> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96bbc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="96bbc-105">DESCRIPTION</span></span>
<span data-ttu-id="96bbc-106">Il cmdlet **set-AzBatchJob** aggiorna un processo batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="96bbc-106">The **Set-AzBatchJob** cmdlet updates an Azure Batch job.</span></span>
<span data-ttu-id="96bbc-107">Usa il cmdlet Get-AzBatchJob per ottenere un oggetto **PSCloudJob** .</span><span class="sxs-lookup"><span data-stu-id="96bbc-107">Use the Get-AzBatchJob cmdlet to get a **PSCloudJob** object.</span></span>
<span data-ttu-id="96bbc-108">Modificare le proprietà di tale oggetto e quindi usare il cmdlet corrente per eseguire il commit delle modifiche apportate al servizio batch.</span><span class="sxs-lookup"><span data-stu-id="96bbc-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="96bbc-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="96bbc-109">EXAMPLES</span></span>

### <span data-ttu-id="96bbc-110">Esempio 1: aggiornare un processo</span><span class="sxs-lookup"><span data-stu-id="96bbc-110">Example 1: Update a job</span></span>
```
PS C:\>$Job = Get-AzBatchJob -Id "Job17" -BatchContext $Context
PS C:\> $Job.Priority = 1
PS C:\> Set-AzBatchJob -Job $Job -BatchContext $Context
```

<span data-ttu-id="96bbc-111">Il primo comando ottiene un processo utilizzando **Get-AzBatchJob** e lo archivia nella variabile $job.</span><span class="sxs-lookup"><span data-stu-id="96bbc-111">The first command gets a job by using **Get-AzBatchJob**, and then stores it in the $Job variable.</span></span>
<span data-ttu-id="96bbc-112">Il secondo comando modifica la specifica della priorità nell'oggetto $Job.</span><span class="sxs-lookup"><span data-stu-id="96bbc-112">The second command modifies the priority specification on the $Job object.</span></span>
<span data-ttu-id="96bbc-113">Il comando finale aggiorna il servizio batch in base all'oggetto locale in $Job.</span><span class="sxs-lookup"><span data-stu-id="96bbc-113">The final command updates the Batch service to match the local object in $Job.</span></span>

## <span data-ttu-id="96bbc-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="96bbc-114">PARAMETERS</span></span>

### <span data-ttu-id="96bbc-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="96bbc-115">-BatchContext</span></span>
<span data-ttu-id="96bbc-116">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="96bbc-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="96bbc-117">Se si usa il cmdlet Get-AzBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="96bbc-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="96bbc-118">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="96bbc-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="96bbc-119">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="96bbc-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="96bbc-120">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="96bbc-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="96bbc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96bbc-121">-DefaultProfile</span></span>
<span data-ttu-id="96bbc-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="96bbc-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96bbc-123">-Job</span><span class="sxs-lookup"><span data-stu-id="96bbc-123">-Job</span></span>
<span data-ttu-id="96bbc-124">Specifica un **PSCloudJob** a cui questo cmdlet aggiorna il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="96bbc-124">Specifies a **PSCloudJob** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96bbc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96bbc-125">CommonParameters</span></span>
<span data-ttu-id="96bbc-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96bbc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96bbc-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96bbc-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96bbc-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="96bbc-128">INPUTS</span></span>

### <span data-ttu-id="96bbc-129">Microsoft.Azure.Commands.Batch. Models. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="96bbc-129">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="96bbc-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="96bbc-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="96bbc-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="96bbc-131">OUTPUTS</span></span>

### <span data-ttu-id="96bbc-132">System. void</span><span class="sxs-lookup"><span data-stu-id="96bbc-132">System.Void</span></span>

## <span data-ttu-id="96bbc-133">Note</span><span class="sxs-lookup"><span data-stu-id="96bbc-133">NOTES</span></span>

## <span data-ttu-id="96bbc-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="96bbc-134">RELATED LINKS</span></span>

[<span data-ttu-id="96bbc-135">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="96bbc-135">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="96bbc-136">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="96bbc-136">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="96bbc-137">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="96bbc-137">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="96bbc-138">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="96bbc-138">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="96bbc-139">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="96bbc-139">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="96bbc-140">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="96bbc-140">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="96bbc-141">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="96bbc-141">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="96bbc-142">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="96bbc-142">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
