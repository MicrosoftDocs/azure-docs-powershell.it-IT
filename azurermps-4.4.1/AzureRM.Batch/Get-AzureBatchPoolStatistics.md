---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 8188C617-4895-4B43-8D3B-FA6FC5B868DD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolStatistics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolStatistics.md
ms.openlocfilehash: 25fe1f4e89b7ea569899fc980a55c3a30acbf77a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521781"
---
# <span data-ttu-id="9cecd-101">Get-AzureBatchPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="9cecd-101">Get-AzureBatchPoolStatistics</span></span>

## <span data-ttu-id="9cecd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9cecd-102">SYNOPSIS</span></span>
<span data-ttu-id="9cecd-103">Ottiene le statistiche di riepilogo del pool per un account batch.</span><span class="sxs-lookup"><span data-stu-id="9cecd-103">Gets pool summary statistics for a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9cecd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9cecd-104">SYNTAX</span></span>

```
Get-AzureBatchPoolStatistics -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9cecd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9cecd-105">DESCRIPTION</span></span>
<span data-ttu-id="9cecd-106">Il cmdlet **Get-AzureBatchPoolStatistics** ottiene le statistiche di durata per tutti i pool nell'account specificato.</span><span class="sxs-lookup"><span data-stu-id="9cecd-106">The **Get-AzureBatchPoolStatistics** cmdlet gets the lifetime statistics for all of the pools in the specified account.</span></span>
<span data-ttu-id="9cecd-107">Le statistiche vengono aggregate in tutti i pool mai esistiti nell'account, dalla creazione dell'account fino all'ultimo aggiornamento delle statistiche.</span><span class="sxs-lookup"><span data-stu-id="9cecd-107">Statistics are aggregated across all pools that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="9cecd-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9cecd-108">EXAMPLES</span></span>

### <span data-ttu-id="9cecd-109">Esempio 1: ottenere le statistiche delle risorse di tutti i pool di un account</span><span class="sxs-lookup"><span data-stu-id="9cecd-109">Example 1: Get resource statistics of all pools in an account</span></span>
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

<span data-ttu-id="9cecd-110">Il primo comando crea un riferimento a un oggetto alle chiavi dell'account per l'account batch denominato ContosoBatchAccount tramite **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="9cecd-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="9cecd-111">Il comando Archivia il riferimento all'oggetto nella variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="9cecd-111">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="9cecd-112">Il secondo comando ottiene le statistiche di tutti i pool nell'account specificato e li archivia nel $PoolStatistics.</span><span class="sxs-lookup"><span data-stu-id="9cecd-112">The second command gets the statistics of all of the pools in the specified account, and then stores them in the $PoolStatistics.</span></span>

<span data-ttu-id="9cecd-113">Il comando finale Visualizza la proprietà **ResourceStatistics** di $PoolStatistics.</span><span class="sxs-lookup"><span data-stu-id="9cecd-113">The final command displays the **ResourceStatistics** property of $PoolStatistics.</span></span>

## <span data-ttu-id="9cecd-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9cecd-114">PARAMETERS</span></span>

### <span data-ttu-id="9cecd-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="9cecd-115">-BatchContext</span></span>
<span data-ttu-id="9cecd-116">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="9cecd-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="9cecd-117">Per ottenere un oggetto **BatchAccountContext** che contiene i tasti di scelta per l'abbonamento, usare il cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="9cecd-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="9cecd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cecd-118">-DefaultProfile</span></span>
<span data-ttu-id="9cecd-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9cecd-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9cecd-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cecd-120">CommonParameters</span></span>
<span data-ttu-id="9cecd-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cecd-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cecd-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cecd-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cecd-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9cecd-123">INPUTS</span></span>

### <span data-ttu-id="9cecd-124">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="9cecd-124">BatchAccountContext</span></span>
<span data-ttu-id="9cecd-125">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="9cecd-125">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="9cecd-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9cecd-126">OUTPUTS</span></span>

### <span data-ttu-id="9cecd-127">PSPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="9cecd-127">PSPoolStatistics</span></span>

## <span data-ttu-id="9cecd-128">Note</span><span class="sxs-lookup"><span data-stu-id="9cecd-128">NOTES</span></span>

## <span data-ttu-id="9cecd-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9cecd-129">RELATED LINKS</span></span>

[<span data-ttu-id="9cecd-130">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="9cecd-130">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="9cecd-131">Get-AzureBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="9cecd-131">Get-AzureBatchPoolUsageMetrics</span></span>](./Get-AzureBatchPoolUsageMetrics.md)

[<span data-ttu-id="9cecd-132">Get-AzureBatchJobStatistics</span><span class="sxs-lookup"><span data-stu-id="9cecd-132">Get-AzureBatchJobStatistics</span></span>](./Get-AzureBatchJobStatistics.md)


