---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 7C79BFF1-41E1-472D-AF67-1C3B39AB7548
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJob.md
ms.openlocfilehash: 81ace9fd18b916f8f4788cf5878af1a620a61882
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687500"
---
# <span data-ttu-id="a4e69-101">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a4e69-101">Enable-AzureBatchJob</span></span>

## <span data-ttu-id="a4e69-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a4e69-102">SYNOPSIS</span></span>
<span data-ttu-id="a4e69-103">Abilita un processo batch.</span><span class="sxs-lookup"><span data-stu-id="a4e69-103">Enables a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4e69-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a4e69-104">SYNTAX</span></span>

```
Enable-AzureBatchJob [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4e69-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a4e69-105">DESCRIPTION</span></span>
<span data-ttu-id="a4e69-106">Il cmdlet **Enable-AzureBatchJob** Abilita un processo batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="a4e69-106">The **Enable-AzureBatchJob** cmdlet enables an Azure Batch job.</span></span>
<span data-ttu-id="a4e69-107">Dopo l'abilitazione di un processo, le nuove attività possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="a4e69-107">After you enable a job, new tasks can run.</span></span>

## <span data-ttu-id="a4e69-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a4e69-108">EXAMPLES</span></span>

### <span data-ttu-id="a4e69-109">Esempio 1: abilitare un processo batch</span><span class="sxs-lookup"><span data-stu-id="a4e69-109">Example 1: Enable a Batch job</span></span>
```
PS C:\>Enable-AzureBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="a4e69-110">Questo comando consente di abilitare il processo con ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="a4e69-110">This command enables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="a4e69-111">Usa il cmdlet Get-AzureRmBatchAccountKeys per assegnare un contesto alla variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="a4e69-111">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="a4e69-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a4e69-112">PARAMETERS</span></span>

### <span data-ttu-id="a4e69-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a4e69-113">-BatchContext</span></span>
<span data-ttu-id="a4e69-114">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="a4e69-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a4e69-115">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="a4e69-115">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a4e69-116">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="a4e69-116">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a4e69-117">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a4e69-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a4e69-118">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="a4e69-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4e69-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4e69-119">-DefaultProfile</span></span>
<span data-ttu-id="a4e69-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a4e69-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4e69-121">-ID</span><span class="sxs-lookup"><span data-stu-id="a4e69-121">-Id</span></span>
<span data-ttu-id="a4e69-122">Specifica l'ID del processo abilitato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4e69-122">Specifies the ID of the job that this cmdlet enables.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4e69-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4e69-123">CommonParameters</span></span>
<span data-ttu-id="a4e69-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4e69-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4e69-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4e69-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4e69-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a4e69-126">INPUTS</span></span>

### <span data-ttu-id="a4e69-127">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a4e69-127">BatchAccountContext</span></span>
<span data-ttu-id="a4e69-128">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="a4e69-128">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="a4e69-129">Stringa</span><span class="sxs-lookup"><span data-stu-id="a4e69-129">String</span></span>
<span data-ttu-id="a4e69-130">Il parametro "ID" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="a4e69-130">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="a4e69-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a4e69-131">OUTPUTS</span></span>

## <span data-ttu-id="a4e69-132">Note</span><span class="sxs-lookup"><span data-stu-id="a4e69-132">NOTES</span></span>

## <span data-ttu-id="a4e69-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a4e69-133">RELATED LINKS</span></span>

[<span data-ttu-id="a4e69-134">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a4e69-134">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="a4e69-135">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a4e69-135">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="a4e69-136">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a4e69-136">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="a4e69-137">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a4e69-137">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="a4e69-138">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a4e69-138">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="a4e69-139">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="a4e69-139">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


