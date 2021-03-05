---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: E655684D-9601-4A0B-BB09-EFB787EB2B1B
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchjobstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobStatistic.md
ms.openlocfilehash: ec52f8b48433e52e86551a8346f4ec9a61b5727d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987025"
---
# <span data-ttu-id="7ec8d-101">Get-AzBatchJobStatistic</span><span class="sxs-lookup"><span data-stu-id="7ec8d-101">Get-AzBatchJobStatistic</span></span>

## <span data-ttu-id="7ec8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ec8d-102">SYNOPSIS</span></span>
<span data-ttu-id="7ec8d-103">Recupera le statistiche di riepilogo del processo per un account batch.</span><span class="sxs-lookup"><span data-stu-id="7ec8d-103">Gets job summary statistics for a Batch account.</span></span>

## <span data-ttu-id="7ec8d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7ec8d-104">SYNTAX</span></span>

```
Get-AzBatchJobStatistic -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7ec8d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7ec8d-105">DESCRIPTION</span></span>
<span data-ttu-id="7ec8d-106">Il cmdlet **Get-AzBatchJobStatistic** ottiene le statistiche di riepilogo della durata per tutti i processi in un account batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="7ec8d-106">The **Get-AzBatchJobStatistic** cmdlet gets lifetime summary statistics for all of the jobs in an Azure Batch account.</span></span>
<span data-ttu-id="7ec8d-107">Le statistiche vengono aggregate per tutti i processi che sono mai stati esistiti nell'account, dalla creazione dell'account all'ultima ora di aggiornamento delle statistiche.</span><span class="sxs-lookup"><span data-stu-id="7ec8d-107">Statistics are aggregated across all jobs that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="7ec8d-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7ec8d-108">EXAMPLES</span></span>

### <span data-ttu-id="7ec8d-109">Esempio 1: Ottenere statistiche di riepilogo per tutti i processi</span><span class="sxs-lookup"><span data-stu-id="7ec8d-109">Example 1: Get summary statistics for all jobs</span></span>
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

<span data-ttu-id="7ec8d-110">Il primo comando crea un riferimento a un oggetto alle chiavi dell'account batch denominato ContosoBatchAccount usando **Get-AzBatchAccountKey.**</span><span class="sxs-lookup"><span data-stu-id="7ec8d-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="7ec8d-111">Il comando archivia questo riferimento all'oggetto nella $Context variabile.</span><span class="sxs-lookup"><span data-stu-id="7ec8d-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="7ec8d-112">Il secondo comando recupera le statistiche di riepilogo per tutti i processi.</span><span class="sxs-lookup"><span data-stu-id="7ec8d-112">The second command gets the summary statistics for all of the jobs.</span></span>
<span data-ttu-id="7ec8d-113">Il comando usa il $Context del primo comando.</span><span class="sxs-lookup"><span data-stu-id="7ec8d-113">The command uses the $Context value from the first command.</span></span>

## <span data-ttu-id="7ec8d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ec8d-114">PARAMETERS</span></span>

### <span data-ttu-id="7ec8d-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="7ec8d-115">-BatchContext</span></span>
<span data-ttu-id="7ec8d-116">Specifica **l'istanza BatchAccountContext** che questo cmdlet usa per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="7ec8d-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="7ec8d-117">Se si usa il cmdlet Get-AzBatchAccount per ottenere BatchAccountContext, verrà usata l'autenticazione di Azure Active Directory quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="7ec8d-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="7ec8d-118">Per usare invece l'autenticazione della chiave condivisa, usare il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con le relative chiavi di accesso popolate.</span><span class="sxs-lookup"><span data-stu-id="7ec8d-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="7ec8d-119">Quando si usa l'autenticazione con chiave condivisa, per impostazione predefinita viene usata la chiave di accesso primario.</span><span class="sxs-lookup"><span data-stu-id="7ec8d-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="7ec8d-120">Per modificare la chiave da usare, impostare la proprietà BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="7ec8d-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="7ec8d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ec8d-121">-DefaultProfile</span></span>
<span data-ttu-id="7ec8d-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7ec8d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ec8d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ec8d-123">CommonParameters</span></span>
<span data-ttu-id="7ec8d-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ec8d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ec8d-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7ec8d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ec8d-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="7ec8d-126">INPUTS</span></span>

### <span data-ttu-id="7ec8d-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="7ec8d-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="7ec8d-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7ec8d-128">OUTPUTS</span></span>

### <span data-ttu-id="7ec8d-129">Microsoft.Azure.Commands.Batch. Models.PSJobStatistics</span><span class="sxs-lookup"><span data-stu-id="7ec8d-129">Microsoft.Azure.Commands.Batch.Models.PSJobStatistics</span></span>

## <span data-ttu-id="7ec8d-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="7ec8d-130">NOTES</span></span>

## <span data-ttu-id="7ec8d-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7ec8d-131">RELATED LINKS</span></span>

[<span data-ttu-id="7ec8d-132">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="7ec8d-132">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="7ec8d-133">Get-AzBatchPoolStatistic</span><span class="sxs-lookup"><span data-stu-id="7ec8d-133">Get-AzBatchPoolStatistic</span></span>](./Get-AzBatchPoolStatistic.md)

[<span data-ttu-id="7ec8d-134">Get-AzBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="7ec8d-134">Get-AzBatchPoolUsageMetrics</span></span>](./Get-AzBatchPoolUsageMetric.md)
