---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D1C5B35C-5419-4739-9D57-6C4228E98DAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
ms.openlocfilehash: b236f163a6c5c849fcbfcea0a19dac955e15c798
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478160"
---
# <span data-ttu-id="1f99f-101">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="1f99f-101">Stop-AzBatchJobSchedule</span></span>

## <span data-ttu-id="1f99f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1f99f-102">SYNOPSIS</span></span>
<span data-ttu-id="1f99f-103">Interrompe la pianificazione di un processo batch.</span><span class="sxs-lookup"><span data-stu-id="1f99f-103">Stops a Batch job schedule.</span></span>

## <span data-ttu-id="1f99f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1f99f-104">SYNTAX</span></span>

```
Stop-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f99f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f99f-105">DESCRIPTION</span></span>
<span data-ttu-id="1f99f-106">Il cmdlet **Stop-AzBatchJobSchedule** interrompe la pianificazione di un processo batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="1f99f-106">The **Stop-AzBatchJobSchedule** cmdlet stops an Azure Batch job schedule.</span></span>

## <span data-ttu-id="1f99f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1f99f-107">EXAMPLES</span></span>

### <span data-ttu-id="1f99f-108">Esempio 1: interrompere la pianificazione di un processo</span><span class="sxs-lookup"><span data-stu-id="1f99f-108">Example 1: Stop a job schedule</span></span>
```
PS C:\>Stop-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="1f99f-109">Questo comando interrompe la pianificazione del processo che contiene l'ID JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="1f99f-109">This command stops the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="1f99f-110">Usa il cmdlet Get-AzBatchAccountKey per assegnare un contesto alla variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="1f99f-110">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="1f99f-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1f99f-111">PARAMETERS</span></span>

### <span data-ttu-id="1f99f-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="1f99f-112">-BatchContext</span></span>
<span data-ttu-id="1f99f-113">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="1f99f-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="1f99f-114">Se si usa il cmdlet Get-AzBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="1f99f-114">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="1f99f-115">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="1f99f-115">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="1f99f-116">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="1f99f-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="1f99f-117">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="1f99f-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="1f99f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f99f-118">-DefaultProfile</span></span>
<span data-ttu-id="1f99f-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1f99f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f99f-120">-ID</span><span class="sxs-lookup"><span data-stu-id="1f99f-120">-Id</span></span>
<span data-ttu-id="1f99f-121">Specifica l'ID della pianificazione del processo arrestata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f99f-121">Specifies the ID of the job schedule that this cmdlet stops.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f99f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f99f-122">CommonParameters</span></span>
<span data-ttu-id="1f99f-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f99f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f99f-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f99f-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f99f-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1f99f-125">INPUTS</span></span>

### <span data-ttu-id="1f99f-126">System. String</span><span class="sxs-lookup"><span data-stu-id="1f99f-126">System.String</span></span>

### <span data-ttu-id="1f99f-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="1f99f-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="1f99f-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1f99f-128">OUTPUTS</span></span>

### <span data-ttu-id="1f99f-129">System. void</span><span class="sxs-lookup"><span data-stu-id="1f99f-129">System.Void</span></span>

## <span data-ttu-id="1f99f-130">Note</span><span class="sxs-lookup"><span data-stu-id="1f99f-130">NOTES</span></span>

## <span data-ttu-id="1f99f-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1f99f-131">RELATED LINKS</span></span>

[<span data-ttu-id="1f99f-132">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="1f99f-132">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="1f99f-133">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="1f99f-133">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="1f99f-134">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="1f99f-134">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="1f99f-135">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="1f99f-135">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="1f99f-136">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="1f99f-136">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="1f99f-137">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="1f99f-137">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="1f99f-138">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="1f99f-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
