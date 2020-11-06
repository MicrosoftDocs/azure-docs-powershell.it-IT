---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B3C8A2DB-6571-418D-8C4B-3BE3FDA42F89
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchCertificateDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchCertificateDeletion.md
ms.openlocfilehash: 820e94b75c19d49f4e49ee8419f7807a839f925b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518352"
---
# <span data-ttu-id="841b2-101">Stop-AzureBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="841b2-101">Stop-AzureBatchCertificateDeletion</span></span>

## <span data-ttu-id="841b2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="841b2-102">SYNOPSIS</span></span>
<span data-ttu-id="841b2-103">Annulla l'eliminazione di un certificato non riuscito.</span><span class="sxs-lookup"><span data-stu-id="841b2-103">Cancels a failed deletion of a certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="841b2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="841b2-104">SYNTAX</span></span>

```
Stop-AzureBatchCertificateDeletion [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="841b2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="841b2-105">DESCRIPTION</span></span>
<span data-ttu-id="841b2-106">Il cmdlet **Stop-AzureBatchCertificateDeletion** Annulla l'eliminazione non riuscita di un certificato nel servizio batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="841b2-106">The **Stop-AzureBatchCertificateDeletion** cmdlet cancels a failed deletion of a certificate in the Azure Batch service.</span></span>
<span data-ttu-id="841b2-107">È possibile interrompere un'eliminazione solo se il certificato si trova nello stato **DeleteFailed** .</span><span class="sxs-lookup"><span data-stu-id="841b2-107">You can stop a deletion only if the certificate is in the **DeleteFailed** state.</span></span>
<span data-ttu-id="841b2-108">Questo cmldet ripristina lo stato **attivo** del certificato.</span><span class="sxs-lookup"><span data-stu-id="841b2-108">This cmldet restores the certificate to the **Active** state.</span></span>

## <span data-ttu-id="841b2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="841b2-109">EXAMPLES</span></span>

### <span data-ttu-id="841b2-110">Esempio 1: annullare un'eliminazione</span><span class="sxs-lookup"><span data-stu-id="841b2-110">Example 1: Cancel a deletion</span></span>
```
PS C:\>Stop-AzureBatchCertificateDeletion -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="841b2-111">Questo comando Annulla l'eliminazione del certificato con l'identificazione personale specificata.</span><span class="sxs-lookup"><span data-stu-id="841b2-111">This command cancels the deletion of the certificate that has the specified thumbprint.</span></span>

## <span data-ttu-id="841b2-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="841b2-112">PARAMETERS</span></span>

### <span data-ttu-id="841b2-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="841b2-113">-BatchContext</span></span>
<span data-ttu-id="841b2-114">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="841b2-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="841b2-115">Per ottenere un oggetto **BatchAccountContext** che contiene i tasti di scelta per l'abbonamento, usare il cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="841b2-115">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="841b2-116">-Identificazione personale</span><span class="sxs-lookup"><span data-stu-id="841b2-116">-Thumbprint</span></span>
<span data-ttu-id="841b2-117">Specifica l'identificazione personale del certificato che questo cmdlet Ripristina nello stato **attivo** .</span><span class="sxs-lookup"><span data-stu-id="841b2-117">Specifies the thumbprint of the certificate that this cmdlet restores to the **Active** state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="841b2-118">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="841b2-118">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="841b2-119">Specifica l'algoritmo usato per derivare il parametro *identificazione personale* .</span><span class="sxs-lookup"><span data-stu-id="841b2-119">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="841b2-120">Attualmente, l'unico valore valido è SHA1.</span><span class="sxs-lookup"><span data-stu-id="841b2-120">Currently, the only valid value is sha1.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="841b2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="841b2-121">-DefaultProfile</span></span>
<span data-ttu-id="841b2-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="841b2-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="841b2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="841b2-123">CommonParameters</span></span>
<span data-ttu-id="841b2-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="841b2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="841b2-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="841b2-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="841b2-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="841b2-126">INPUTS</span></span>

### <span data-ttu-id="841b2-127">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="841b2-127">BatchAccountContext</span></span>
<span data-ttu-id="841b2-128">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="841b2-128">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="841b2-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="841b2-129">OUTPUTS</span></span>

## <span data-ttu-id="841b2-130">Note</span><span class="sxs-lookup"><span data-stu-id="841b2-130">NOTES</span></span>

## <span data-ttu-id="841b2-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="841b2-131">RELATED LINKS</span></span>

[<span data-ttu-id="841b2-132">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="841b2-132">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="841b2-133">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="841b2-133">Remove-AzureBatchCertificate</span></span>](./Remove-AzureBatchCertificate.md)

[<span data-ttu-id="841b2-134">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="841b2-134">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


