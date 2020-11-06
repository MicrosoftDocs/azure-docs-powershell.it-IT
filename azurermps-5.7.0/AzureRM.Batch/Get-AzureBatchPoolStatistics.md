---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 8188C617-4895-4B43-8D3B-FA6FC5B868DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchpoolstatistics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolStatistics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolStatistics.md
ms.openlocfilehash: e51f10fb7d1043e7a0f9addb9c874224ce952dc3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510152"
---
# <span data-ttu-id="a7838-101">Get-AzureBatchPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="a7838-101">Get-AzureBatchPoolStatistics</span></span>

## <span data-ttu-id="a7838-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a7838-102">SYNOPSIS</span></span>
<span data-ttu-id="a7838-103">Ottiene le statistiche di riepilogo del pool per un account batch.</span><span class="sxs-lookup"><span data-stu-id="a7838-103">Gets pool summary statistics for a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7838-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a7838-104">SYNTAX</span></span>

```
Get-AzureBatchPoolStatistics -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a7838-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a7838-105">DESCRIPTION</span></span>
<span data-ttu-id="a7838-106">Il cmdlet **Get-AzureBatchPoolStatistics** ottiene le statistiche di durata per tutti i pool nell'account specificato.</span><span class="sxs-lookup"><span data-stu-id="a7838-106">The **Get-AzureBatchPoolStatistics** cmdlet gets the lifetime statistics for all of the pools in the specified account.</span></span>
<span data-ttu-id="a7838-107">Le statistiche vengono aggregate in tutti i pool mai esistiti nell'account, dalla creazione dell'account fino all'ultimo aggiornamento delle statistiche.</span><span class="sxs-lookup"><span data-stu-id="a7838-107">Statistics are aggregated across all pools that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="a7838-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a7838-108">EXAMPLES</span></span>

### <span data-ttu-id="a7838-109">Esempio 1: ottenere le statistiche delle risorse di tutti i pool di un account</span><span class="sxs-lookup"><span data-stu-id="a7838-109">Example 1: Get resource statistics of all pools in an account</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $PoolStatistics = Get-AzureBatchPoolStatistics -BatchContext $Context
PS C:\> $PoolStatistics.ResourceStatistics 
AverageCpuPercentage : 0.351232518750755
AverageDiskGiB       : 55.2569014701165
AverageMemoryGiB     : 2.87273772318252
DiskReadGiB          : 45.1326256990433
DiskReadIOps         : 878278
DiskWriteGiB         : 1230.72120628133
DiskWriteIOps        : 176832212
LastUpdateTime       : 5/16/2016 4:30:00 PM
NetworkReadGiB       : 29.3502839952707
NetworkWriteGiB      : 25.5208827350289
PeakDiskGiB          : 21.9638671875
PeakMemoryGiB        : 1.11184692382813
StartTime            : 2/10/2016 7:07:24 PM
```

<span data-ttu-id="a7838-110">Il primo comando crea un riferimento a un oggetto alle chiavi dell'account per l'account batch denominato ContosoBatchAccount tramite **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="a7838-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="a7838-111">Il comando Archivia il riferimento all'oggetto nella variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="a7838-111">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="a7838-112">Il secondo comando ottiene le statistiche di tutti i pool nell'account specificato e li archivia nel $PoolStatistics.</span><span class="sxs-lookup"><span data-stu-id="a7838-112">The second command gets the statistics of all of the pools in the specified account, and then stores them in the $PoolStatistics.</span></span>

<span data-ttu-id="a7838-113">Il comando finale Visualizza la proprietà **ResourceStatistics** di $PoolStatistics.</span><span class="sxs-lookup"><span data-stu-id="a7838-113">The final command displays the **ResourceStatistics** property of $PoolStatistics.</span></span>

## <span data-ttu-id="a7838-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a7838-114">PARAMETERS</span></span>

### <span data-ttu-id="a7838-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a7838-115">-BatchContext</span></span>
<span data-ttu-id="a7838-116">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="a7838-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a7838-117">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="a7838-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a7838-118">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="a7838-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a7838-119">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a7838-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a7838-120">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="a7838-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a7838-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7838-121">-DefaultProfile</span></span>
<span data-ttu-id="a7838-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a7838-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7838-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7838-123">CommonParameters</span></span>
<span data-ttu-id="a7838-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7838-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7838-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7838-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7838-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a7838-126">INPUTS</span></span>

### <span data-ttu-id="a7838-127">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a7838-127">BatchAccountContext</span></span>
<span data-ttu-id="a7838-128">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="a7838-128">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="a7838-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a7838-129">OUTPUTS</span></span>

### <span data-ttu-id="a7838-130">PSPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="a7838-130">PSPoolStatistics</span></span>

## <span data-ttu-id="a7838-131">Note</span><span class="sxs-lookup"><span data-stu-id="a7838-131">NOTES</span></span>

## <span data-ttu-id="a7838-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a7838-132">RELATED LINKS</span></span>

[<span data-ttu-id="a7838-133">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="a7838-133">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="a7838-134">Get-AzureBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="a7838-134">Get-AzureBatchPoolUsageMetrics</span></span>](./Get-AzureBatchPoolUsageMetrics.md)

[<span data-ttu-id="a7838-135">Get-AzureBatchJobStatistics</span><span class="sxs-lookup"><span data-stu-id="a7838-135">Get-AzureBatchJobStatistics</span></span>](./Get-AzureBatchJobStatistics.md)


