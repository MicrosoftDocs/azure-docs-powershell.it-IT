---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 7C79BFF1-41E1-472D-AF67-1C3B39AB7548
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJob.md
ms.openlocfilehash: be73b757bf20a2f688d7f7293ac4022e7bc8f4aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517600"
---
# <span data-ttu-id="68fc3-101">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="68fc3-101">Enable-AzureBatchJob</span></span>

## <span data-ttu-id="68fc3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="68fc3-102">SYNOPSIS</span></span>
<span data-ttu-id="68fc3-103">Abilita un processo batch.</span><span class="sxs-lookup"><span data-stu-id="68fc3-103">Enables a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68fc3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="68fc3-104">SYNTAX</span></span>

```
Enable-AzureBatchJob [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68fc3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="68fc3-105">DESCRIPTION</span></span>
<span data-ttu-id="68fc3-106">Il cmdlet **Enable-AzureBatchJob** Abilita un processo batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="68fc3-106">The **Enable-AzureBatchJob** cmdlet enables an Azure Batch job.</span></span>
<span data-ttu-id="68fc3-107">Dopo l'abilitazione di un processo, le nuove attività possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="68fc3-107">After you enable a job, new tasks can run.</span></span>

## <span data-ttu-id="68fc3-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="68fc3-108">EXAMPLES</span></span>

### <span data-ttu-id="68fc3-109">Esempio 1: abilitare un processo batch</span><span class="sxs-lookup"><span data-stu-id="68fc3-109">Example 1: Enable a Batch job</span></span>
```
PS C:\>Enable-AzureBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="68fc3-110">Questo comando consente di abilitare il processo con ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="68fc3-110">This command enables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="68fc3-111">Usa il cmdlet Get-AzureRmBatchAccountKeys per assegnare un contesto alla variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="68fc3-111">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="68fc3-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="68fc3-112">PARAMETERS</span></span>

### <span data-ttu-id="68fc3-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="68fc3-113">-BatchContext</span></span>
<span data-ttu-id="68fc3-114">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="68fc3-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="68fc3-115">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="68fc3-115">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="68fc3-116">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="68fc3-116">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="68fc3-117">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="68fc3-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="68fc3-118">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="68fc3-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="68fc3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68fc3-119">-DefaultProfile</span></span>
<span data-ttu-id="68fc3-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="68fc3-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68fc3-121">-ID</span><span class="sxs-lookup"><span data-stu-id="68fc3-121">-Id</span></span>
<span data-ttu-id="68fc3-122">Specifica l'ID del processo abilitato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68fc3-122">Specifies the ID of the job that this cmdlet enables.</span></span>

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

### <span data-ttu-id="68fc3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68fc3-123">CommonParameters</span></span>
<span data-ttu-id="68fc3-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68fc3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68fc3-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68fc3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68fc3-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="68fc3-126">INPUTS</span></span>

### <span data-ttu-id="68fc3-127">System. String</span><span class="sxs-lookup"><span data-stu-id="68fc3-127">System.String</span></span>

### <span data-ttu-id="68fc3-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="68fc3-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="68fc3-129">Parametri: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="68fc3-129">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="68fc3-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="68fc3-130">OUTPUTS</span></span>

### <span data-ttu-id="68fc3-131">System. void</span><span class="sxs-lookup"><span data-stu-id="68fc3-131">System.Void</span></span>

## <span data-ttu-id="68fc3-132">Note</span><span class="sxs-lookup"><span data-stu-id="68fc3-132">NOTES</span></span>

## <span data-ttu-id="68fc3-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="68fc3-133">RELATED LINKS</span></span>

[<span data-ttu-id="68fc3-134">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="68fc3-134">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="68fc3-135">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="68fc3-135">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="68fc3-136">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="68fc3-136">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="68fc3-137">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="68fc3-137">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="68fc3-138">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="68fc3-138">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="68fc3-139">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="68fc3-139">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


