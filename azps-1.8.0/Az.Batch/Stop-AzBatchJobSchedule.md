---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D1C5B35C-5419-4739-9D57-6C4228E98DAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
ms.openlocfilehash: 94c4fe3292e07045382e432377111d0849db2668
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2020
ms.locfileid: "93865558"
---
# <span data-ttu-id="c7170-101">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c7170-101">Stop-AzBatchJobSchedule</span></span>

## <span data-ttu-id="c7170-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c7170-102">SYNOPSIS</span></span>
<span data-ttu-id="c7170-103">Interrompe la pianificazione di un processo batch.</span><span class="sxs-lookup"><span data-stu-id="c7170-103">Stops a Batch job schedule.</span></span>

## <span data-ttu-id="c7170-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c7170-104">SYNTAX</span></span>

```
Stop-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7170-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c7170-105">DESCRIPTION</span></span>
<span data-ttu-id="c7170-106">Il cmdlet **Stop-AzBatchJobSchedule** interrompe la pianificazione di un processo batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="c7170-106">The **Stop-AzBatchJobSchedule** cmdlet stops an Azure Batch job schedule.</span></span>

## <span data-ttu-id="c7170-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c7170-107">EXAMPLES</span></span>

### <span data-ttu-id="c7170-108">Esempio 1: interrompere la pianificazione di un processo</span><span class="sxs-lookup"><span data-stu-id="c7170-108">Example 1: Stop a job schedule</span></span>
```
PS C:\>Stop-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="c7170-109">Questo comando interrompe la pianificazione del processo che contiene l'ID JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="c7170-109">This command stops the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="c7170-110">Usa il cmdlet Get-AzBatchAccountKeys per assegnare un contesto alla variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="c7170-110">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="c7170-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c7170-111">PARAMETERS</span></span>

### <span data-ttu-id="c7170-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c7170-112">-BatchContext</span></span>
<span data-ttu-id="c7170-113">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="c7170-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c7170-114">Se si usa il cmdlet Get-AzBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="c7170-114">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c7170-115">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="c7170-115">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c7170-116">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="c7170-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c7170-117">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="c7170-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c7170-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7170-118">-DefaultProfile</span></span>
<span data-ttu-id="c7170-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c7170-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7170-120">-ID</span><span class="sxs-lookup"><span data-stu-id="c7170-120">-Id</span></span>
<span data-ttu-id="c7170-121">Specifica l'ID della pianificazione del processo arrestata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7170-121">Specifies the ID of the job schedule that this cmdlet stops.</span></span>

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

### <span data-ttu-id="c7170-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7170-122">CommonParameters</span></span>
<span data-ttu-id="c7170-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7170-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7170-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7170-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7170-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c7170-125">INPUTS</span></span>

### <span data-ttu-id="c7170-126">System. String</span><span class="sxs-lookup"><span data-stu-id="c7170-126">System.String</span></span>

### <span data-ttu-id="c7170-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c7170-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="c7170-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c7170-128">OUTPUTS</span></span>

### <span data-ttu-id="c7170-129">System. void</span><span class="sxs-lookup"><span data-stu-id="c7170-129">System.Void</span></span>

## <span data-ttu-id="c7170-130">Note</span><span class="sxs-lookup"><span data-stu-id="c7170-130">NOTES</span></span>

## <span data-ttu-id="c7170-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c7170-131">RELATED LINKS</span></span>

[<span data-ttu-id="c7170-132">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c7170-132">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="c7170-133">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c7170-133">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="c7170-134">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c7170-134">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="c7170-135">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c7170-135">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="c7170-136">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c7170-136">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="c7170-137">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="c7170-137">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="c7170-138">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="c7170-138">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


