---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchsupportedimage.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSupportedImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSupportedImage.md
ms.openlocfilehash: e5d177776e288a855c35def8d45310a6f6849c27
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990469"
---
# <span data-ttu-id="d6feb-101">Get-AzBatchSupportedImage</span><span class="sxs-lookup"><span data-stu-id="d6feb-101">Get-AzBatchSupportedImage</span></span>

## <span data-ttu-id="d6feb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6feb-102">SYNOPSIS</span></span>
<span data-ttu-id="d6feb-103">Recupera le immagini supportate da Batch per un account batch.</span><span class="sxs-lookup"><span data-stu-id="d6feb-103">Gets Batch supported images for a Batch account.</span></span>

## <span data-ttu-id="d6feb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d6feb-104">SYNTAX</span></span>

```
Get-AzBatchSupportedImage [-Filter <String>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6feb-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d6feb-105">DESCRIPTION</span></span>
<span data-ttu-id="d6feb-106">Il cmdlet **Get-AzBatchSupportedImage** ottiene le immagini delle macchine virtuali supportate disponibili in un account batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="d6feb-106">The **Get-AzBatchSupportedImage** cmdlet gets supported virtual machine images that are available in an Azure Batch account.</span></span>
<span data-ttu-id="d6feb-107">Specificare l'account usando il *parametro BatchContext.*</span><span class="sxs-lookup"><span data-stu-id="d6feb-107">Specify the account by using the *BatchContext* parameter.</span></span>

## <span data-ttu-id="d6feb-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d6feb-108">EXAMPLES</span></span>

### <span data-ttu-id="d6feb-109">Esempio 1: Ottenere tutte le immagini supportate disponibili</span><span class="sxs-lookup"><span data-stu-id="d6feb-109">Example 1: Get all available supported images</span></span>

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

<span data-ttu-id="d6feb-110">Il primo comando ottiene un contesto di account batch contenente i tasti di scelta per l'abbonamento usando **Get-AzBatchAccountKey.**</span><span class="sxs-lookup"><span data-stu-id="d6feb-110">The first command gets a Batch account context that contains access keys for your subscription by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="d6feb-111">Il comando archivia il contesto nella $Context variabile da usare nel comando successivo.</span><span class="sxs-lookup"><span data-stu-id="d6feb-111">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="d6feb-112">Il secondo comando ottiene tutte le immagini supportate disponibili per l'account batch.</span><span class="sxs-lookup"><span data-stu-id="d6feb-112">The second command gets all available supported images for that Batch account.</span></span>

## <span data-ttu-id="d6feb-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6feb-113">PARAMETERS</span></span>

### <span data-ttu-id="d6feb-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d6feb-114">-BatchContext</span></span>
<span data-ttu-id="d6feb-115">Istanza BatchAccountContext da usare quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="d6feb-115">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="d6feb-116">Se si usa il cmdlet Get-AzBatchAccount per ottenere BatchAccountContext, verrà usata l'autenticazione di Azure Active Directory quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="d6feb-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="d6feb-117">Per usare invece l'autenticazione della chiave condivisa, usare il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con le relative chiavi di accesso popolate.</span><span class="sxs-lookup"><span data-stu-id="d6feb-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="d6feb-118">Quando si usa l'autenticazione con chiave condivisa, per impostazione predefinita viene usata la chiave di accesso primario.</span><span class="sxs-lookup"><span data-stu-id="d6feb-118">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="d6feb-119">Per modificare la chiave da usare, impostare la proprietà BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="d6feb-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="d6feb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6feb-120">-DefaultProfile</span></span>
<span data-ttu-id="d6feb-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d6feb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6feb-122">-Filter</span><span class="sxs-lookup"><span data-stu-id="d6feb-122">-Filter</span></span>
<span data-ttu-id="d6feb-123">Specifica una clausola del filtro OData per le immagini supportate.</span><span class="sxs-lookup"><span data-stu-id="d6feb-123">Specifies an OData filter clause for supported images.</span></span>
<span data-ttu-id="d6feb-124">Se non si specifica un filtro, questo cmdlet restituisce tutte le immagini supportate dall'account batch.</span><span class="sxs-lookup"><span data-stu-id="d6feb-124">If you do not specify a filter, this cmdlet returns all images the Batch account supports.</span></span>

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

### <span data-ttu-id="d6feb-125">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="d6feb-125">-MaxCount</span></span>
<span data-ttu-id="d6feb-126">Specifica il numero massimo di immagini supportate da restituire.</span><span class="sxs-lookup"><span data-stu-id="d6feb-126">Specifies the maximum number of supported images to return.</span></span>

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

### <span data-ttu-id="d6feb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6feb-127">CommonParameters</span></span>
<span data-ttu-id="d6feb-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6feb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6feb-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d6feb-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6feb-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="d6feb-130">INPUTS</span></span>

### <span data-ttu-id="d6feb-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d6feb-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="d6feb-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d6feb-132">OUTPUTS</span></span>

### <span data-ttu-id="d6feb-133">Microsoft.Azure.Commands.Batch. Models.PSImageInformation</span><span class="sxs-lookup"><span data-stu-id="d6feb-133">Microsoft.Azure.Commands.Batch.Models.PSImageInformation</span></span>

## <span data-ttu-id="d6feb-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="d6feb-134">NOTES</span></span>

## <span data-ttu-id="d6feb-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d6feb-135">RELATED LINKS</span></span>

[<span data-ttu-id="d6feb-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="d6feb-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)