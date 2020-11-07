---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: E655684D-9601-4A0B-BB09-EFB787EB2B1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjobstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobStatistic.md
ms.openlocfilehash: b2c62cf91410e2604875df6f82237445e153f6aa
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2020
ms.locfileid: "93865537"
---
# <span data-ttu-id="f8f18-101">Get-AzBatchJobStatistic</span><span class="sxs-lookup"><span data-stu-id="f8f18-101">Get-AzBatchJobStatistic</span></span>

## <span data-ttu-id="f8f18-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f8f18-102">SYNOPSIS</span></span>
<span data-ttu-id="f8f18-103">Ottiene le statistiche di riepilogo dei processi per un account batch.</span><span class="sxs-lookup"><span data-stu-id="f8f18-103">Gets job summary statistics for a Batch account.</span></span>

## <span data-ttu-id="f8f18-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f8f18-104">SYNTAX</span></span>

```
Get-AzBatchJobStatistic -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f8f18-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f8f18-105">DESCRIPTION</span></span>
<span data-ttu-id="f8f18-106">Il cmdlet **Get-AzBatchJobStatistic** ottiene le statistiche di riepilogo durata per tutti i processi in un account batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="f8f18-106">The **Get-AzBatchJobStatistic** cmdlet gets lifetime summary statistics for all of the jobs in an Azure Batch account.</span></span>
<span data-ttu-id="f8f18-107">Le statistiche vengono aggregate in tutti i processi mai esistiti nell'account, dalla creazione dell'account fino all'ultimo aggiornamento delle statistiche.</span><span class="sxs-lookup"><span data-stu-id="f8f18-107">Statistics are aggregated across all jobs that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="f8f18-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f8f18-108">EXAMPLES</span></span>

### <span data-ttu-id="f8f18-109">Esempio 1: ottenere statistiche di riepilogo per tutti i processi</span><span class="sxs-lookup"><span data-stu-id="f8f18-109">Example 1: Get summary statistics for all jobs</span></span>
```
PS C:\>Get-AzBatchJobStatistic -BatchContext $Context
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

<span data-ttu-id="f8f18-110">Il primo comando crea un riferimento a un oggetto alle chiavi dell'account per l'account batch denominato ContosoBatchAccount tramite **Get-AzBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="f8f18-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKeys**.</span></span>
<span data-ttu-id="f8f18-111">Il comando Archivia il riferimento all'oggetto nella variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="f8f18-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="f8f18-112">Il secondo comando consente di ottenere le statistiche di riepilogo per tutti i processi.</span><span class="sxs-lookup"><span data-stu-id="f8f18-112">The second command gets the summary statistics for all of the jobs.</span></span>
<span data-ttu-id="f8f18-113">Il comando usa il valore $Context del primo comando.</span><span class="sxs-lookup"><span data-stu-id="f8f18-113">The command uses the $Context value from the first command.</span></span>

## <span data-ttu-id="f8f18-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f8f18-114">PARAMETERS</span></span>

### <span data-ttu-id="f8f18-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f8f18-115">-BatchContext</span></span>
<span data-ttu-id="f8f18-116">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="f8f18-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f8f18-117">Se si usa il cmdlet Get-AzBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="f8f18-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f8f18-118">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="f8f18-118">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f8f18-119">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="f8f18-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f8f18-120">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="f8f18-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f8f18-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8f18-121">-DefaultProfile</span></span>
<span data-ttu-id="f8f18-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f8f18-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8f18-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8f18-123">CommonParameters</span></span>
<span data-ttu-id="f8f18-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8f18-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8f18-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8f18-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8f18-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f8f18-126">INPUTS</span></span>

### <span data-ttu-id="f8f18-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f8f18-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="f8f18-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f8f18-128">OUTPUTS</span></span>

### <span data-ttu-id="f8f18-129">Microsoft.Azure.Commands.Batch. Models. PSJobStatistics</span><span class="sxs-lookup"><span data-stu-id="f8f18-129">Microsoft.Azure.Commands.Batch.Models.PSJobStatistics</span></span>

## <span data-ttu-id="f8f18-130">Note</span><span class="sxs-lookup"><span data-stu-id="f8f18-130">NOTES</span></span>

## <span data-ttu-id="f8f18-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f8f18-131">RELATED LINKS</span></span>

[<span data-ttu-id="f8f18-132">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="f8f18-132">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="f8f18-133">Get-AzBatchPoolStatistic</span><span class="sxs-lookup"><span data-stu-id="f8f18-133">Get-AzBatchPoolStatistic</span></span>](./Get-AzBatchPoolStatistic.md)

[<span data-ttu-id="f8f18-134">Get-AzBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="f8f18-134">Get-AzBatchPoolUsageMetrics</span></span>](./Get-AzBatchPoolUsageMetric.md)


