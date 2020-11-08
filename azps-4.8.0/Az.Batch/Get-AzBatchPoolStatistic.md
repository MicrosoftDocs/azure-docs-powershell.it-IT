---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 8188C617-4895-4B43-8D3B-FA6FC5B868DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchpoolstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolStatistic.md
ms.openlocfilehash: 49aa971dcc9d46f5a063042cbcdf8ca449c41e94
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190573"
---
# <span data-ttu-id="c49c2-101">Get-AzBatchPoolStatistic</span><span class="sxs-lookup"><span data-stu-id="c49c2-101">Get-AzBatchPoolStatistic</span></span>

## <span data-ttu-id="c49c2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c49c2-102">SYNOPSIS</span></span>
<span data-ttu-id="c49c2-103">Ottiene le statistiche di riepilogo del pool per un account batch.</span><span class="sxs-lookup"><span data-stu-id="c49c2-103">Gets pool summary statistics for a Batch account.</span></span>

## <span data-ttu-id="c49c2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c49c2-104">SYNTAX</span></span>

```
Get-AzBatchPoolStatistic -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c49c2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c49c2-105">DESCRIPTION</span></span>
<span data-ttu-id="c49c2-106">Il cmdlet **Get-AzBatchPoolStatistic** ottiene le statistiche di durata per tutti i pool nell'account specificato.</span><span class="sxs-lookup"><span data-stu-id="c49c2-106">The **Get-AzBatchPoolStatistic** cmdlet gets the lifetime statistics for all of the pools in the specified account.</span></span>
<span data-ttu-id="c49c2-107">Le statistiche vengono aggregate in tutti i pool mai esistiti nell'account, dalla creazione dell'account fino all'ultimo aggiornamento delle statistiche.</span><span class="sxs-lookup"><span data-stu-id="c49c2-107">Statistics are aggregated across all pools that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="c49c2-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c49c2-108">EXAMPLES</span></span>

### <span data-ttu-id="c49c2-109">Esempio 1: ottenere le statistiche delle risorse di tutti i pool di un account</span><span class="sxs-lookup"><span data-stu-id="c49c2-109">Example 1: Get resource statistics of all pools in an account</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> $PoolStatistics = Get-AzBatchPoolStatistic -BatchContext $Context
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

<span data-ttu-id="c49c2-110">Il primo comando crea un riferimento a un oggetto alle chiavi dell'account per l'account batch denominato ContosoBatchAccount tramite **Get-AzBatchAccountKey**.</span><span class="sxs-lookup"><span data-stu-id="c49c2-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="c49c2-111">Il comando Archivia il riferimento all'oggetto nella variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="c49c2-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="c49c2-112">Il secondo comando ottiene le statistiche di tutti i pool nell'account specificato e li archivia nel $PoolStatistics.</span><span class="sxs-lookup"><span data-stu-id="c49c2-112">The second command gets the statistics of all of the pools in the specified account, and then stores them in the $PoolStatistics.</span></span>
<span data-ttu-id="c49c2-113">Il comando finale Visualizza la proprietà **ResourceStatistics** di $PoolStatistics.</span><span class="sxs-lookup"><span data-stu-id="c49c2-113">The final command displays the **ResourceStatistics** property of $PoolStatistics.</span></span>

## <span data-ttu-id="c49c2-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c49c2-114">PARAMETERS</span></span>

### <span data-ttu-id="c49c2-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c49c2-115">-BatchContext</span></span>
<span data-ttu-id="c49c2-116">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="c49c2-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c49c2-117">Se si usa il cmdlet Get-AzBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="c49c2-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c49c2-118">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="c49c2-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c49c2-119">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="c49c2-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c49c2-120">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="c49c2-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c49c2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c49c2-121">-DefaultProfile</span></span>
<span data-ttu-id="c49c2-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c49c2-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c49c2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c49c2-123">CommonParameters</span></span>
<span data-ttu-id="c49c2-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c49c2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c49c2-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c49c2-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c49c2-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c49c2-126">INPUTS</span></span>

### <span data-ttu-id="c49c2-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c49c2-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="c49c2-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c49c2-128">OUTPUTS</span></span>

### <span data-ttu-id="c49c2-129">Microsoft.Azure.Commands.Batch. Models. PSPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="c49c2-129">Microsoft.Azure.Commands.Batch.Models.PSPoolStatistics</span></span>

## <span data-ttu-id="c49c2-130">Note</span><span class="sxs-lookup"><span data-stu-id="c49c2-130">NOTES</span></span>

## <span data-ttu-id="c49c2-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c49c2-131">RELATED LINKS</span></span>

[<span data-ttu-id="c49c2-132">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="c49c2-132">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="c49c2-133">Get-AzBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="c49c2-133">Get-AzBatchPoolUsageMetrics</span></span>](./Get-AzBatchPoolUsageMetric.md)

[<span data-ttu-id="c49c2-134">Get-AzBatchJobStatistic</span><span class="sxs-lookup"><span data-stu-id="c49c2-134">Get-AzBatchJobStatistic</span></span>](./Get-AzBatchJobStatistic.md)