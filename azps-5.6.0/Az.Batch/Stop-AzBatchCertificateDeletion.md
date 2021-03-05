---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B3C8A2DB-6571-418D-8C4B-3BE3FDA42F89
online version: https://docs.microsoft.com/powershell/module/az.batch/stop-azbatchcertificatedeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchCertificateDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchCertificateDeletion.md
ms.openlocfilehash: 099f6a1ea19e9810745715dbc90ea0e0b1962285
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994502"
---
# <span data-ttu-id="83a1c-101">Stop-AzBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="83a1c-101">Stop-AzBatchCertificateDeletion</span></span>

## <span data-ttu-id="83a1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83a1c-102">SYNOPSIS</span></span>
<span data-ttu-id="83a1c-103">Annulla l'eliminazione non riuscita di un certificato.</span><span class="sxs-lookup"><span data-stu-id="83a1c-103">Cancels a failed deletion of a certificate.</span></span>

## <span data-ttu-id="83a1c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="83a1c-104">SYNTAX</span></span>

```
Stop-AzBatchCertificateDeletion [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83a1c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="83a1c-105">DESCRIPTION</span></span>
<span data-ttu-id="83a1c-106">Il cmdlet **Stop-AzBatchCertificateDeletion** annulla l'eliminazione non riuscita di un certificato nel servizio batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="83a1c-106">The **Stop-AzBatchCertificateDeletion** cmdlet cancels a failed deletion of a certificate in the Azure Batch service.</span></span>
<span data-ttu-id="83a1c-107">È possibile interrompere un'eliminazione solo se il certificato è in **stato DeleteFailed.**</span><span class="sxs-lookup"><span data-stu-id="83a1c-107">You can stop a deletion only if the certificate is in the **DeleteFailed** state.</span></span>
<span data-ttu-id="83a1c-108">Questo cmdlet ripristina lo stato Attivo **del** certificato.</span><span class="sxs-lookup"><span data-stu-id="83a1c-108">This cmdlet restores the certificate to the **Active** state.</span></span>

## <span data-ttu-id="83a1c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="83a1c-109">EXAMPLES</span></span>

### <span data-ttu-id="83a1c-110">Esempio 1: Annullare un'eliminazione</span><span class="sxs-lookup"><span data-stu-id="83a1c-110">Example 1: Cancel a deletion</span></span>
```
PS C:\>Stop-AzBatchCertificateDeletion -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="83a1c-111">Questo comando annulla l'eliminazione del certificato con l'immagine thumbprint specificata.</span><span class="sxs-lookup"><span data-stu-id="83a1c-111">This command cancels the deletion of the certificate that has the specified thumbprint.</span></span>

## <span data-ttu-id="83a1c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83a1c-112">PARAMETERS</span></span>

### <span data-ttu-id="83a1c-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="83a1c-113">-BatchContext</span></span>
<span data-ttu-id="83a1c-114">Specifica **l'istanza BatchAccountContext** che questo cmdlet usa per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="83a1c-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="83a1c-115">Se si usa il cmdlet Get-AzBatchAccount per ottenere BatchAccountContext, verrà usata l'autenticazione di Azure Active Directory quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="83a1c-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="83a1c-116">Per usare invece l'autenticazione della chiave condivisa, usare il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con le relative chiavi di accesso popolate.</span><span class="sxs-lookup"><span data-stu-id="83a1c-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="83a1c-117">Quando si usa l'autenticazione con chiave condivisa, per impostazione predefinita viene usata la chiave di accesso primario.</span><span class="sxs-lookup"><span data-stu-id="83a1c-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="83a1c-118">Per modificare la chiave da usare, impostare la proprietà BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="83a1c-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="83a1c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83a1c-119">-DefaultProfile</span></span>
<span data-ttu-id="83a1c-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="83a1c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83a1c-121">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="83a1c-121">-Thumbprint</span></span>
<span data-ttu-id="83a1c-122">Specifica l'immagine thumbprint del certificato ripristinato da questo cmdlet sullo **stato** Attivo.</span><span class="sxs-lookup"><span data-stu-id="83a1c-122">Specifies the thumbprint of the certificate that this cmdlet restores to the **Active** state.</span></span>

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

### <span data-ttu-id="83a1c-123">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="83a1c-123">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="83a1c-124">Specifica l'algoritmo usato per ricavare *il parametro Thumbprint.*</span><span class="sxs-lookup"><span data-stu-id="83a1c-124">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="83a1c-125">Attualmente l'unico valore valido è sha1.</span><span class="sxs-lookup"><span data-stu-id="83a1c-125">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="83a1c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83a1c-126">CommonParameters</span></span>
<span data-ttu-id="83a1c-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83a1c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83a1c-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="83a1c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83a1c-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="83a1c-129">INPUTS</span></span>

### <span data-ttu-id="83a1c-130">System.String</span><span class="sxs-lookup"><span data-stu-id="83a1c-130">System.String</span></span>

### <span data-ttu-id="83a1c-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="83a1c-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="83a1c-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="83a1c-132">OUTPUTS</span></span>

### <span data-ttu-id="83a1c-133">System.Void</span><span class="sxs-lookup"><span data-stu-id="83a1c-133">System.Void</span></span>

## <span data-ttu-id="83a1c-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="83a1c-134">NOTES</span></span>

## <span data-ttu-id="83a1c-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="83a1c-135">RELATED LINKS</span></span>

[<span data-ttu-id="83a1c-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="83a1c-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="83a1c-137">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="83a1c-137">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="83a1c-138">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="83a1c-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
