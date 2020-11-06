---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3DFFD0F2-6CD8-4FBE-B15C-8505CBF8F44E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchCertificate.md
ms.openlocfilehash: e62aebd6a03f7d5a162f141eae55e3df6c9a0a88
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520708"
---
# <span data-ttu-id="a1bc5-101">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="a1bc5-101">Remove-AzureBatchCertificate</span></span>

## <span data-ttu-id="a1bc5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a1bc5-102">SYNOPSIS</span></span>
<span data-ttu-id="a1bc5-103">Elimina un certificato da un account.</span><span class="sxs-lookup"><span data-stu-id="a1bc5-103">Deletes a certificate from an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1bc5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a1bc5-104">SYNTAX</span></span>

```
Remove-AzureBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a1bc5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a1bc5-105">DESCRIPTION</span></span>
<span data-ttu-id="a1bc5-106">Il cmdlet **Remove-AzureBatchCertificate** rimuove un certificato dall'account batch di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="a1bc5-106">The **Remove-AzureBatchCertificate** cmdlet removes a certificate from the specified Azure Batch account.</span></span>

## <span data-ttu-id="a1bc5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a1bc5-107">EXAMPLES</span></span>

### <span data-ttu-id="a1bc5-108">Esempio 1: rimuovere un certificato</span><span class="sxs-lookup"><span data-stu-id="a1bc5-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureBatchCertificate -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="a1bc5-109">Questo comando rimuove il certificato con l'identificazione personale specificata.</span><span class="sxs-lookup"><span data-stu-id="a1bc5-109">This command removes the certificate that has the specified thumbprint.</span></span>

### <span data-ttu-id="a1bc5-110">Esempio 2: rimuovere tutti i certificati attivi</span><span class="sxs-lookup"><span data-stu-id="a1bc5-110">Example 2:Remove all active certificates</span></span>
```
PS C:\>Get-AzureBatchCertificate -Filter "state eq 'active'" -BatchContext $Context | Remove-AzureBatchCertificate -Force -BatchContext $Context
```

<span data-ttu-id="a1bc5-111">Questo comando ottiene tutti i certificati attivi tramite il cmdlet Get-AzureBatchCertificate.</span><span class="sxs-lookup"><span data-stu-id="a1bc5-111">This command gets all certificates that are active by using the Get-AzureBatchCertificate cmdlet.</span></span>
<span data-ttu-id="a1bc5-112">Il comando passa i certificati attivi al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="a1bc5-112">The command passes the active certificates to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a1bc5-113">Questo cmdlet rimuove ogni certificato.</span><span class="sxs-lookup"><span data-stu-id="a1bc5-113">That cmdlet removes each certificate.</span></span>
<span data-ttu-id="a1bc5-114">Il comando specifica il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="a1bc5-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="a1bc5-115">Di conseguenza, il comando non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="a1bc5-115">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="a1bc5-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a1bc5-116">PARAMETERS</span></span>

### <span data-ttu-id="a1bc5-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a1bc5-117">-BatchContext</span></span>
<span data-ttu-id="a1bc5-118">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="a1bc5-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a1bc5-119">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="a1bc5-119">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a1bc5-120">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="a1bc5-120">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a1bc5-121">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a1bc5-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a1bc5-122">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="a1bc5-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a1bc5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1bc5-123">-DefaultProfile</span></span>
<span data-ttu-id="a1bc5-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a1bc5-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1bc5-125">-Identificazione personale</span><span class="sxs-lookup"><span data-stu-id="a1bc5-125">-Thumbprint</span></span>
<span data-ttu-id="a1bc5-126">Specifica l'identificazione personale del certificato eliminato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1bc5-126">Specifies the thumbprint of the certificate that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="a1bc5-127">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="a1bc5-127">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="a1bc5-128">Specifica l'algoritmo usato per derivare il parametro *identificazione personale* .</span><span class="sxs-lookup"><span data-stu-id="a1bc5-128">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="a1bc5-129">Attualmente, l'unico valore valido è SHA1.</span><span class="sxs-lookup"><span data-stu-id="a1bc5-129">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="a1bc5-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a1bc5-130">-Confirm</span></span>
<span data-ttu-id="a1bc5-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1bc5-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1bc5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1bc5-132">-WhatIf</span></span>
<span data-ttu-id="a1bc5-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a1bc5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1bc5-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a1bc5-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1bc5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1bc5-135">CommonParameters</span></span>
<span data-ttu-id="a1bc5-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1bc5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1bc5-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1bc5-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1bc5-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a1bc5-138">INPUTS</span></span>

### <span data-ttu-id="a1bc5-139">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a1bc5-139">BatchAccountContext</span></span>
<span data-ttu-id="a1bc5-140">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="a1bc5-140">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="a1bc5-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a1bc5-141">OUTPUTS</span></span>

## <span data-ttu-id="a1bc5-142">Note</span><span class="sxs-lookup"><span data-stu-id="a1bc5-142">NOTES</span></span>

## <span data-ttu-id="a1bc5-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a1bc5-143">RELATED LINKS</span></span>

[<span data-ttu-id="a1bc5-144">Get-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="a1bc5-144">Get-AzureBatchCertificate</span></span>](./Get-AzureBatchCertificate.md)

[<span data-ttu-id="a1bc5-145">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="a1bc5-145">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="a1bc5-146">New-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="a1bc5-146">New-AzureBatchCertificate</span></span>](./New-AzureBatchCertificate.md)

[<span data-ttu-id="a1bc5-147">Stop-AzureBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="a1bc5-147">Stop-AzureBatchCertificateDeletion</span></span>](./Stop-AzureBatchCertificateDeletion.md)

[<span data-ttu-id="a1bc5-148">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="a1bc5-148">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


