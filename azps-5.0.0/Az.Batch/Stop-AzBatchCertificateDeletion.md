---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B3C8A2DB-6571-418D-8C4B-3BE3FDA42F89
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchcertificatedeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchCertificateDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchCertificateDeletion.md
ms.openlocfilehash: 53c4f4c24e0a5b1c868facd0fed8d3754fda7a41
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302142"
---
# <span data-ttu-id="662fb-101">Stop-AzBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="662fb-101">Stop-AzBatchCertificateDeletion</span></span>

## <span data-ttu-id="662fb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="662fb-102">SYNOPSIS</span></span>
<span data-ttu-id="662fb-103">Annulla l'eliminazione di un certificato non riuscito.</span><span class="sxs-lookup"><span data-stu-id="662fb-103">Cancels a failed deletion of a certificate.</span></span>

## <span data-ttu-id="662fb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="662fb-104">SYNTAX</span></span>

```
Stop-AzBatchCertificateDeletion [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="662fb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="662fb-105">DESCRIPTION</span></span>
<span data-ttu-id="662fb-106">Il cmdlet **Stop-AzBatchCertificateDeletion** Annulla l'eliminazione non riuscita di un certificato nel servizio batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="662fb-106">The **Stop-AzBatchCertificateDeletion** cmdlet cancels a failed deletion of a certificate in the Azure Batch service.</span></span>
<span data-ttu-id="662fb-107">È possibile interrompere un'eliminazione solo se il certificato si trova nello stato **DeleteFailed** .</span><span class="sxs-lookup"><span data-stu-id="662fb-107">You can stop a deletion only if the certificate is in the **DeleteFailed** state.</span></span>
<span data-ttu-id="662fb-108">Questo cmdlet consente di ripristinare lo stato **attivo** del certificato.</span><span class="sxs-lookup"><span data-stu-id="662fb-108">This cmdlet restores the certificate to the **Active** state.</span></span>

## <span data-ttu-id="662fb-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="662fb-109">EXAMPLES</span></span>

### <span data-ttu-id="662fb-110">Esempio 1: annullare un'eliminazione</span><span class="sxs-lookup"><span data-stu-id="662fb-110">Example 1: Cancel a deletion</span></span>
```
PS C:\>Stop-AzBatchCertificateDeletion -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="662fb-111">Questo comando Annulla l'eliminazione del certificato con l'identificazione personale specificata.</span><span class="sxs-lookup"><span data-stu-id="662fb-111">This command cancels the deletion of the certificate that has the specified thumbprint.</span></span>

## <span data-ttu-id="662fb-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="662fb-112">PARAMETERS</span></span>

### <span data-ttu-id="662fb-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="662fb-113">-BatchContext</span></span>
<span data-ttu-id="662fb-114">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="662fb-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="662fb-115">Se si usa il cmdlet Get-AzBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="662fb-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="662fb-116">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="662fb-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="662fb-117">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="662fb-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="662fb-118">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="662fb-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="662fb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="662fb-119">-DefaultProfile</span></span>
<span data-ttu-id="662fb-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="662fb-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="662fb-121">-Identificazione personale</span><span class="sxs-lookup"><span data-stu-id="662fb-121">-Thumbprint</span></span>
<span data-ttu-id="662fb-122">Specifica l'identificazione personale del certificato che questo cmdlet Ripristina nello stato **attivo** .</span><span class="sxs-lookup"><span data-stu-id="662fb-122">Specifies the thumbprint of the certificate that this cmdlet restores to the **Active** state.</span></span>

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

### <span data-ttu-id="662fb-123">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="662fb-123">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="662fb-124">Specifica l'algoritmo usato per derivare il parametro *identificazione personale* .</span><span class="sxs-lookup"><span data-stu-id="662fb-124">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="662fb-125">Attualmente, l'unico valore valido è SHA1.</span><span class="sxs-lookup"><span data-stu-id="662fb-125">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="662fb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="662fb-126">CommonParameters</span></span>
<span data-ttu-id="662fb-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="662fb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="662fb-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="662fb-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="662fb-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="662fb-129">INPUTS</span></span>

### <span data-ttu-id="662fb-130">System. String</span><span class="sxs-lookup"><span data-stu-id="662fb-130">System.String</span></span>

### <span data-ttu-id="662fb-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="662fb-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="662fb-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="662fb-132">OUTPUTS</span></span>

### <span data-ttu-id="662fb-133">System. void</span><span class="sxs-lookup"><span data-stu-id="662fb-133">System.Void</span></span>

## <span data-ttu-id="662fb-134">Note</span><span class="sxs-lookup"><span data-stu-id="662fb-134">NOTES</span></span>

## <span data-ttu-id="662fb-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="662fb-135">RELATED LINKS</span></span>

[<span data-ttu-id="662fb-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="662fb-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="662fb-137">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="662fb-137">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="662fb-138">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="662fb-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
