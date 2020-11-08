---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 02F91510-F14F-4401-BC5F-06B0874AEB4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJobSchedule.md
ms.openlocfilehash: 03decd5b1d32defb25692220c63ffe768445697e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199730"
---
# <span data-ttu-id="e7218-101">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e7218-101">Enable-AzBatchJobSchedule</span></span>

## <span data-ttu-id="e7218-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e7218-102">SYNOPSIS</span></span>
<span data-ttu-id="e7218-103">Abilita una pianificazione processo batch.</span><span class="sxs-lookup"><span data-stu-id="e7218-103">Enables a Batch job schedule.</span></span>

## <span data-ttu-id="e7218-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e7218-104">SYNTAX</span></span>

```
Enable-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7218-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e7218-105">DESCRIPTION</span></span>
<span data-ttu-id="e7218-106">Il cmdlet **Enable-AzBatchJobSchedule** Abilita una pianificazione del processo batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="e7218-106">The **Enable-AzBatchJobSchedule** cmdlet enables an Azure Batch job schedule.</span></span>
<span data-ttu-id="e7218-107">Dopo l'abilitazione di una pianificazione processo, i processi possono essere creati in base a tale programmazione.</span><span class="sxs-lookup"><span data-stu-id="e7218-107">After you enable a job schedule, jobs can be created according to that schedule.</span></span>

## <span data-ttu-id="e7218-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e7218-108">EXAMPLES</span></span>

### <span data-ttu-id="e7218-109">Esempio 1: abilitare una pianificazione del processo</span><span class="sxs-lookup"><span data-stu-id="e7218-109">Example 1: Enable a job schedule</span></span>
```
PS C:\>Enable-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="e7218-110">Questo comando Abilita la pianificazione del processo con ID JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="e7218-110">This command enables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="e7218-111">Usa il cmdlet **Get-AzBatchAccountKey** per assegnare un contesto alla variabile $context.</span><span class="sxs-lookup"><span data-stu-id="e7218-111">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="e7218-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e7218-112">PARAMETERS</span></span>

### <span data-ttu-id="e7218-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e7218-113">-BatchContext</span></span>
<span data-ttu-id="e7218-114">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="e7218-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e7218-115">Se si usa il cmdlet Get-AzBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="e7218-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e7218-116">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="e7218-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e7218-117">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="e7218-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e7218-118">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="e7218-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e7218-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7218-119">-DefaultProfile</span></span>
<span data-ttu-id="e7218-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e7218-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7218-121">-ID</span><span class="sxs-lookup"><span data-stu-id="e7218-121">-Id</span></span>
<span data-ttu-id="e7218-122">Specifica l'ID della pianificazione del processo abilitata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7218-122">Specifies the ID of the job schedule that this cmdlet enables.</span></span>

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

### <span data-ttu-id="e7218-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7218-123">CommonParameters</span></span>
<span data-ttu-id="e7218-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7218-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7218-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7218-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7218-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e7218-126">INPUTS</span></span>

### <span data-ttu-id="e7218-127">System. String</span><span class="sxs-lookup"><span data-stu-id="e7218-127">System.String</span></span>

### <span data-ttu-id="e7218-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e7218-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e7218-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e7218-129">OUTPUTS</span></span>

### <span data-ttu-id="e7218-130">System. void</span><span class="sxs-lookup"><span data-stu-id="e7218-130">System.Void</span></span>

## <span data-ttu-id="e7218-131">Note</span><span class="sxs-lookup"><span data-stu-id="e7218-131">NOTES</span></span>

## <span data-ttu-id="e7218-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e7218-132">RELATED LINKS</span></span>

[<span data-ttu-id="e7218-133">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e7218-133">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="e7218-134">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="e7218-134">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="e7218-135">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e7218-135">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="e7218-136">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e7218-136">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="e7218-137">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e7218-137">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="e7218-138">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e7218-138">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="e7218-139">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="e7218-139">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
