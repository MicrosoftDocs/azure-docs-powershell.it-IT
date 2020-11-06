---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B3C8A2DB-6571-418D-8C4B-3BE3FDA42F89
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchcertificatedeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchCertificateDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchCertificateDeletion.md
ms.openlocfilehash: 51fca07847ca5bf0c73a5f2c88a41d3de166053c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510107"
---
# <span data-ttu-id="fe3e1-101">Stop-AzureBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="fe3e1-101">Stop-AzureBatchCertificateDeletion</span></span>

## <span data-ttu-id="fe3e1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fe3e1-102">SYNOPSIS</span></span>
<span data-ttu-id="fe3e1-103">Annulla l'eliminazione di un certificato non riuscito.</span><span class="sxs-lookup"><span data-stu-id="fe3e1-103">Cancels a failed deletion of a certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe3e1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fe3e1-104">SYNTAX</span></span>

```
Stop-AzureBatchCertificateDeletion [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe3e1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fe3e1-105">DESCRIPTION</span></span>
<span data-ttu-id="fe3e1-106">Il cmdlet **Stop-AzureBatchCertificateDeletion** Annulla l'eliminazione non riuscita di un certificato nel servizio batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="fe3e1-106">The **Stop-AzureBatchCertificateDeletion** cmdlet cancels a failed deletion of a certificate in the Azure Batch service.</span></span>
<span data-ttu-id="fe3e1-107">È possibile interrompere un'eliminazione solo se il certificato si trova nello stato **DeleteFailed** .</span><span class="sxs-lookup"><span data-stu-id="fe3e1-107">You can stop a deletion only if the certificate is in the **DeleteFailed** state.</span></span>
<span data-ttu-id="fe3e1-108">Questo cmldet ripristina lo stato **attivo** del certificato.</span><span class="sxs-lookup"><span data-stu-id="fe3e1-108">This cmldet restores the certificate to the **Active** state.</span></span>

## <span data-ttu-id="fe3e1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fe3e1-109">EXAMPLES</span></span>

### <span data-ttu-id="fe3e1-110">Esempio 1: annullare un'eliminazione</span><span class="sxs-lookup"><span data-stu-id="fe3e1-110">Example 1: Cancel a deletion</span></span>
```
PS C:\>Stop-AzureBatchCertificateDeletion -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="fe3e1-111">Questo comando Annulla l'eliminazione del certificato con l'identificazione personale specificata.</span><span class="sxs-lookup"><span data-stu-id="fe3e1-111">This command cancels the deletion of the certificate that has the specified thumbprint.</span></span>

## <span data-ttu-id="fe3e1-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fe3e1-112">PARAMETERS</span></span>

### <span data-ttu-id="fe3e1-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="fe3e1-113">-BatchContext</span></span>
<span data-ttu-id="fe3e1-114">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="fe3e1-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="fe3e1-115">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="fe3e1-115">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="fe3e1-116">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="fe3e1-116">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="fe3e1-117">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="fe3e1-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="fe3e1-118">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="fe3e1-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="fe3e1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe3e1-119">-DefaultProfile</span></span>
<span data-ttu-id="fe3e1-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fe3e1-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe3e1-121">-Identificazione personale</span><span class="sxs-lookup"><span data-stu-id="fe3e1-121">-Thumbprint</span></span>
<span data-ttu-id="fe3e1-122">Specifica l'identificazione personale del certificato che questo cmdlet Ripristina nello stato **attivo** .</span><span class="sxs-lookup"><span data-stu-id="fe3e1-122">Specifies the thumbprint of the certificate that this cmdlet restores to the **Active** state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe3e1-123">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="fe3e1-123">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="fe3e1-124">Specifica l'algoritmo usato per derivare il parametro *identificazione personale* .</span><span class="sxs-lookup"><span data-stu-id="fe3e1-124">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="fe3e1-125">Attualmente, l'unico valore valido è SHA1.</span><span class="sxs-lookup"><span data-stu-id="fe3e1-125">Currently, the only valid value is sha1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe3e1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe3e1-126">CommonParameters</span></span>
<span data-ttu-id="fe3e1-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe3e1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe3e1-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe3e1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe3e1-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fe3e1-129">INPUTS</span></span>

### <span data-ttu-id="fe3e1-130">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="fe3e1-130">BatchAccountContext</span></span>
<span data-ttu-id="fe3e1-131">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="fe3e1-131">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="fe3e1-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fe3e1-132">OUTPUTS</span></span>

## <span data-ttu-id="fe3e1-133">Note</span><span class="sxs-lookup"><span data-stu-id="fe3e1-133">NOTES</span></span>

## <span data-ttu-id="fe3e1-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fe3e1-134">RELATED LINKS</span></span>

[<span data-ttu-id="fe3e1-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="fe3e1-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="fe3e1-136">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="fe3e1-136">Remove-AzureBatchCertificate</span></span>](./Remove-AzureBatchCertificate.md)

[<span data-ttu-id="fe3e1-137">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="fe3e1-137">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


