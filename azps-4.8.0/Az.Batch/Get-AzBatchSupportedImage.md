---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchsupportedimage.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSupportedImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSupportedImage.md
ms.openlocfilehash: e06b9957b8e9b58e25b52b69d4064aca1a69035a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190561"
---
# <span data-ttu-id="84298-101">Get-AzBatchSupportedImage</span><span class="sxs-lookup"><span data-stu-id="84298-101">Get-AzBatchSupportedImage</span></span>

## <span data-ttu-id="84298-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="84298-102">SYNOPSIS</span></span>
<span data-ttu-id="84298-103">Ottiene immagini supportate in batch per un account batch.</span><span class="sxs-lookup"><span data-stu-id="84298-103">Gets Batch supported images for a Batch account.</span></span>

## <span data-ttu-id="84298-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="84298-104">SYNTAX</span></span>

```
Get-AzBatchSupportedImage [-Filter <String>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84298-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84298-105">DESCRIPTION</span></span>
<span data-ttu-id="84298-106">Il cmdlet **Get-AzBatchSupportedImage** ottiene le immagini della macchina virtuale supportate disponibili in un account batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="84298-106">The **Get-AzBatchSupportedImage** cmdlet gets supported virtual machine images that are available in an Azure Batch account.</span></span>
<span data-ttu-id="84298-107">Specificare l'account usando il parametro *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="84298-107">Specify the account by using the *BatchContext* parameter.</span></span>

## <span data-ttu-id="84298-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="84298-108">EXAMPLES</span></span>

### <span data-ttu-id="84298-109">Esempio 1: ottenere tutte le immagini supportate disponibili</span><span class="sxs-lookup"><span data-stu-id="84298-109">Example 1: Get all available supported images</span></span>

```powershell
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchSupportedImage -BatchContext $Context
BatchSupportEndOfLife :
Capabilities          :
ImageReference        : canonical:ubuntuserver:16.04-lts:latest
NodeAgentSkuId        : batch.node.ubuntu 16.04
OSType                : Linux
VerificationType      : Verified

BatchSupportEndOfLife :
Capabilities          :
ImageReference        : canonical:ubuntuserver:18.04-lts:latest
NodeAgentSkuId        : batch.node.ubuntu 18.04
OSType                : Linux
VerificationType      : Verified

BatchSupportEndOfLife :
Capabilities          :
ImageReference        : credativ:debian:8:latest
NodeAgentSkuId        : batch.node.debian 8
OSType                : Linux
VerificationType      : Verified

BatchSupportEndOfLife :
Capabilities          :
ImageReference        : microsoftwindowsserver:windowsserver:2016-datacenter:latest
NodeAgentSkuId        : batch.node.windows amd64
OSType                : Windows
VerificationType      : Verified

...
```

<span data-ttu-id="84298-110">Il primo comando ottiene un contesto dell'account batch che contiene i tasti di scelta per l'abbonamento utilizzando **Get-AzBatchAccountKey**.</span><span class="sxs-lookup"><span data-stu-id="84298-110">The first command gets a Batch account context that contains access keys for your subscription by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="84298-111">Il comando Archivia il contesto nella variabile $Context da usare nel comando successivo.</span><span class="sxs-lookup"><span data-stu-id="84298-111">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="84298-112">Il secondo comando consente di ottenere tutte le immagini supportate disponibili per l'account batch.</span><span class="sxs-lookup"><span data-stu-id="84298-112">The second command gets all available supported images for that Batch account.</span></span>

## <span data-ttu-id="84298-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="84298-113">PARAMETERS</span></span>

### <span data-ttu-id="84298-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="84298-114">-BatchContext</span></span>
<span data-ttu-id="84298-115">Istanza di BatchAccountContext da usare per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="84298-115">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="84298-116">Se si usa il cmdlet Get-AzBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="84298-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="84298-117">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="84298-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="84298-118">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="84298-118">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="84298-119">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="84298-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="84298-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84298-120">-DefaultProfile</span></span>
<span data-ttu-id="84298-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="84298-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84298-122">-Filtro</span><span class="sxs-lookup"><span data-stu-id="84298-122">-Filter</span></span>
<span data-ttu-id="84298-123">Specifica una clausola di filtro OData per le immagini supportate.</span><span class="sxs-lookup"><span data-stu-id="84298-123">Specifies an OData filter clause for supported images.</span></span>
<span data-ttu-id="84298-124">Se non specifichi un filtro, questo cmdlet restituisce tutte le immagini supportate dall'account batch.</span><span class="sxs-lookup"><span data-stu-id="84298-124">If you do not specify a filter, this cmdlet returns all images the Batch account supports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84298-125">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="84298-125">-MaxCount</span></span>
<span data-ttu-id="84298-126">Specifica il numero massimo di immagini supportate da restituire.</span><span class="sxs-lookup"><span data-stu-id="84298-126">Specifies the maximum number of supported images to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84298-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84298-127">CommonParameters</span></span>
<span data-ttu-id="84298-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84298-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84298-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="84298-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84298-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="84298-130">INPUTS</span></span>

### <span data-ttu-id="84298-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="84298-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="84298-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="84298-132">OUTPUTS</span></span>

### <span data-ttu-id="84298-133">Microsoft.Azure.Commands.Batch. Models. PSImageInformation</span><span class="sxs-lookup"><span data-stu-id="84298-133">Microsoft.Azure.Commands.Batch.Models.PSImageInformation</span></span>

## <span data-ttu-id="84298-134">Note</span><span class="sxs-lookup"><span data-stu-id="84298-134">NOTES</span></span>

## <span data-ttu-id="84298-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="84298-135">RELATED LINKS</span></span>

[<span data-ttu-id="84298-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="84298-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)