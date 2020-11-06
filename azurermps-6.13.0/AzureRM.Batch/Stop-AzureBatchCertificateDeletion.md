---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B3C8A2DB-6571-418D-8C4B-3BE3FDA42F89
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchcertificatedeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchCertificateDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchCertificateDeletion.md
ms.openlocfilehash: d43754e1b04dadc447de3d727769902f5454f79a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517552"
---
# <span data-ttu-id="e7810-101">Stop-AzureBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="e7810-101">Stop-AzureBatchCertificateDeletion</span></span>

## <span data-ttu-id="e7810-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e7810-102">SYNOPSIS</span></span>
<span data-ttu-id="e7810-103">Annulla l'eliminazione di un certificato non riuscito.</span><span class="sxs-lookup"><span data-stu-id="e7810-103">Cancels a failed deletion of a certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7810-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e7810-104">SYNTAX</span></span>

```
Stop-AzureBatchCertificateDeletion [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7810-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e7810-105">DESCRIPTION</span></span>
<span data-ttu-id="e7810-106">Il cmdlet **Stop-AzureBatchCertificateDeletion** Annulla l'eliminazione non riuscita di un certificato nel servizio batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="e7810-106">The **Stop-AzureBatchCertificateDeletion** cmdlet cancels a failed deletion of a certificate in the Azure Batch service.</span></span>
<span data-ttu-id="e7810-107">È possibile interrompere un'eliminazione solo se il certificato si trova nello stato **DeleteFailed** .</span><span class="sxs-lookup"><span data-stu-id="e7810-107">You can stop a deletion only if the certificate is in the **DeleteFailed** state.</span></span>
<span data-ttu-id="e7810-108">Questo cmldet ripristina lo stato **attivo** del certificato.</span><span class="sxs-lookup"><span data-stu-id="e7810-108">This cmldet restores the certificate to the **Active** state.</span></span>

## <span data-ttu-id="e7810-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e7810-109">EXAMPLES</span></span>

### <span data-ttu-id="e7810-110">Esempio 1: annullare un'eliminazione</span><span class="sxs-lookup"><span data-stu-id="e7810-110">Example 1: Cancel a deletion</span></span>
```
PS C:\>Stop-AzureBatchCertificateDeletion -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="e7810-111">Questo comando Annulla l'eliminazione del certificato con l'identificazione personale specificata.</span><span class="sxs-lookup"><span data-stu-id="e7810-111">This command cancels the deletion of the certificate that has the specified thumbprint.</span></span>

## <span data-ttu-id="e7810-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e7810-112">PARAMETERS</span></span>

### <span data-ttu-id="e7810-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e7810-113">-BatchContext</span></span>
<span data-ttu-id="e7810-114">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="e7810-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e7810-115">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="e7810-115">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e7810-116">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="e7810-116">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e7810-117">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="e7810-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e7810-118">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="e7810-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e7810-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7810-119">-DefaultProfile</span></span>
<span data-ttu-id="e7810-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e7810-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7810-121">-Identificazione personale</span><span class="sxs-lookup"><span data-stu-id="e7810-121">-Thumbprint</span></span>
<span data-ttu-id="e7810-122">Specifica l'identificazione personale del certificato che questo cmdlet Ripristina nello stato **attivo** .</span><span class="sxs-lookup"><span data-stu-id="e7810-122">Specifies the thumbprint of the certificate that this cmdlet restores to the **Active** state.</span></span>

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

### <span data-ttu-id="e7810-123">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="e7810-123">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="e7810-124">Specifica l'algoritmo usato per derivare il parametro *identificazione personale* .</span><span class="sxs-lookup"><span data-stu-id="e7810-124">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="e7810-125">Attualmente, l'unico valore valido è SHA1.</span><span class="sxs-lookup"><span data-stu-id="e7810-125">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="e7810-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7810-126">CommonParameters</span></span>
<span data-ttu-id="e7810-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7810-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7810-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7810-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7810-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e7810-129">INPUTS</span></span>

### <span data-ttu-id="e7810-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e7810-130">System.String</span></span>

### <span data-ttu-id="e7810-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e7810-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="e7810-132">Parametri: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e7810-132">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="e7810-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e7810-133">OUTPUTS</span></span>

### <span data-ttu-id="e7810-134">System. void</span><span class="sxs-lookup"><span data-stu-id="e7810-134">System.Void</span></span>

## <span data-ttu-id="e7810-135">Note</span><span class="sxs-lookup"><span data-stu-id="e7810-135">NOTES</span></span>

## <span data-ttu-id="e7810-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e7810-136">RELATED LINKS</span></span>

[<span data-ttu-id="e7810-137">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="e7810-137">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="e7810-138">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="e7810-138">Remove-AzureBatchCertificate</span></span>](./Remove-AzureBatchCertificate.md)

[<span data-ttu-id="e7810-139">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="e7810-139">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


