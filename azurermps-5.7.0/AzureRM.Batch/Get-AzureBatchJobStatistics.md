---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: E655684D-9601-4A0B-BB09-EFB787EB2B1B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchjobstatistics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobStatistics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobStatistics.md
ms.openlocfilehash: 80ee6f881731f61b045e448e8a231ae9c971552d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518219"
---
# <span data-ttu-id="f4f5e-101">Get-AzureBatchJobStatistics</span><span class="sxs-lookup"><span data-stu-id="f4f5e-101">Get-AzureBatchJobStatistics</span></span>

## <span data-ttu-id="f4f5e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f4f5e-102">SYNOPSIS</span></span>
<span data-ttu-id="f4f5e-103">Ottiene le statistiche di riepilogo dei processi per un account batch.</span><span class="sxs-lookup"><span data-stu-id="f4f5e-103">Gets job summary statistics for a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4f5e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f4f5e-104">SYNTAX</span></span>

```
Get-AzureBatchJobStatistics -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f4f5e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4f5e-105">DESCRIPTION</span></span>
<span data-ttu-id="f4f5e-106">Il cmdlet **Get-AzureBatchJobStatistics** ottiene le statistiche di riepilogo durata per tutti i processi in un account batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="f4f5e-106">The **Get-AzureBatchJobStatistics** cmdlet gets lifetime summary statistics for all of the jobs in an Azure Batch account.</span></span>
<span data-ttu-id="f4f5e-107">Le statistiche vengono aggregate in tutti i processi mai esistiti nell'account, dalla creazione dell'account fino all'ultimo aggiornamento delle statistiche.</span><span class="sxs-lookup"><span data-stu-id="f4f5e-107">Statistics are aggregated across all jobs that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="f4f5e-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f4f5e-108">EXAMPLES</span></span>

### <span data-ttu-id="f4f5e-109">Esempio 1: ottenere statistiche di riepilogo per tutti i processi</span><span class="sxs-lookup"><span data-stu-id="f4f5e-109">Example 1: Get summary statistics for all jobs</span></span>
```
PS C:\>Get-AzureBatchJobStatistics -BatchContext $Context
FailedTaskCount    : 330
KernelCpuTime      : 00:24:31.8440000
LastUpdateTime     : 5/16/2016 6:00:00 PM
ReadIOGiB          : 38.1271341182292
ReadIOps           : 26546054
StartTime          : 11/3/2015 9:47:14 PM
SucceededTaskCount : 766
TaskRetryCount     : 0
Url                : https://accountname.westus.batch.azure.com/lifetimejobstats
UserCpuTime        : 20:55:50.3200000
WaitTime           : 03:54:49.8530000
WallClockTime      : 20:55:50.3200000
WriteIOGiB         : 0.159623090177774
WriteIOps          : 146946
```

<span data-ttu-id="f4f5e-110">Il primo comando crea un riferimento a un oggetto alle chiavi dell'account per l'account batch denominato ContosoBatchAccount tramite **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="f4f5e-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="f4f5e-111">Il comando Archivia il riferimento all'oggetto nella variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="f4f5e-111">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="f4f5e-112">Il secondo comando consente di ottenere le statistiche di riepilogo per tutti i processi.</span><span class="sxs-lookup"><span data-stu-id="f4f5e-112">The second command gets the summary statistics for all of the jobs.</span></span>
<span data-ttu-id="f4f5e-113">Il comando usa il valore $Context del primo comando.</span><span class="sxs-lookup"><span data-stu-id="f4f5e-113">The command uses the $Context value from the first command.</span></span>

## <span data-ttu-id="f4f5e-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f4f5e-114">PARAMETERS</span></span>

### <span data-ttu-id="f4f5e-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f4f5e-115">-BatchContext</span></span>
<span data-ttu-id="f4f5e-116">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="f4f5e-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f4f5e-117">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="f4f5e-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f4f5e-118">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="f4f5e-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f4f5e-119">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="f4f5e-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f4f5e-120">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="f4f5e-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f4f5e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4f5e-121">-DefaultProfile</span></span>
<span data-ttu-id="f4f5e-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f4f5e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4f5e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4f5e-123">CommonParameters</span></span>
<span data-ttu-id="f4f5e-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4f5e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4f5e-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4f5e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4f5e-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f4f5e-126">INPUTS</span></span>

### <span data-ttu-id="f4f5e-127">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f4f5e-127">BatchAccountContext</span></span>
<span data-ttu-id="f4f5e-128">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="f4f5e-128">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="f4f5e-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f4f5e-129">OUTPUTS</span></span>

### <span data-ttu-id="f4f5e-130">PSJobStatistics</span><span class="sxs-lookup"><span data-stu-id="f4f5e-130">PSJobStatistics</span></span>

## <span data-ttu-id="f4f5e-131">Note</span><span class="sxs-lookup"><span data-stu-id="f4f5e-131">NOTES</span></span>

## <span data-ttu-id="f4f5e-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f4f5e-132">RELATED LINKS</span></span>

[<span data-ttu-id="f4f5e-133">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="f4f5e-133">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="f4f5e-134">Get-AzureBatchPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="f4f5e-134">Get-AzureBatchPoolStatistics</span></span>](./Get-AzureBatchPoolStatistics.md)

[<span data-ttu-id="f4f5e-135">Get-AzureBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="f4f5e-135">Get-AzureBatchPoolUsageMetrics</span></span>](./Get-AzureBatchPoolUsageMetrics.md)


