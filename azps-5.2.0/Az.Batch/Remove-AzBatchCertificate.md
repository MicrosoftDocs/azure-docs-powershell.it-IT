---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3DFFD0F2-6CD8-4FBE-B15C-8505CBF8F44E
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchCertificate.md
ms.openlocfilehash: 2f751a6efcf4b798c69bb0dfd9ecd38c33a65d01
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361241"
---
# <span data-ttu-id="f0c71-101">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="f0c71-101">Remove-AzBatchCertificate</span></span>

## <span data-ttu-id="f0c71-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f0c71-102">SYNOPSIS</span></span>
<span data-ttu-id="f0c71-103">Elimina un certificato da un account.</span><span class="sxs-lookup"><span data-stu-id="f0c71-103">Deletes a certificate from an account.</span></span>

## <span data-ttu-id="f0c71-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f0c71-104">SYNTAX</span></span>

```
Remove-AzBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f0c71-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f0c71-105">DESCRIPTION</span></span>
<span data-ttu-id="f0c71-106">Il cmdlet **Remove-AzBatchCertificate** rimuove un certificato dall'account batch di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="f0c71-106">The **Remove-AzBatchCertificate** cmdlet removes a certificate from the specified Azure Batch account.</span></span>

## <span data-ttu-id="f0c71-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f0c71-107">EXAMPLES</span></span>

### <span data-ttu-id="f0c71-108">Esempio 1: rimuovere un certificato</span><span class="sxs-lookup"><span data-stu-id="f0c71-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzBatchCertificate -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="f0c71-109">Questo comando rimuove il certificato con l'identificazione personale specificata.</span><span class="sxs-lookup"><span data-stu-id="f0c71-109">This command removes the certificate that has the specified thumbprint.</span></span>

### <span data-ttu-id="f0c71-110">Esempio 2: rimuovere tutti i certificati attivi</span><span class="sxs-lookup"><span data-stu-id="f0c71-110">Example 2:Remove all active certificates</span></span>
```
PS C:\>Get-AzBatchCertificate -Filter "state eq 'active'" -BatchContext $Context | Remove-AzBatchCertificate -Force -BatchContext $Context
```

<span data-ttu-id="f0c71-111">Questo comando ottiene tutti i certificati attivi tramite il cmdlet Get-AzBatchCertificate.</span><span class="sxs-lookup"><span data-stu-id="f0c71-111">This command gets all certificates that are active by using the Get-AzBatchCertificate cmdlet.</span></span>
<span data-ttu-id="f0c71-112">Il comando passa i certificati attivi al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="f0c71-112">The command passes the active certificates to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f0c71-113">Questo cmdlet rimuove ogni certificato.</span><span class="sxs-lookup"><span data-stu-id="f0c71-113">That cmdlet removes each certificate.</span></span>
<span data-ttu-id="f0c71-114">Il comando specifica il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="f0c71-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="f0c71-115">Di conseguenza, il comando non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="f0c71-115">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="f0c71-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f0c71-116">PARAMETERS</span></span>

### <span data-ttu-id="f0c71-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f0c71-117">-BatchContext</span></span>
<span data-ttu-id="f0c71-118">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="f0c71-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f0c71-119">Se si usa il cmdlet Get-AzBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="f0c71-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f0c71-120">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="f0c71-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f0c71-121">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="f0c71-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f0c71-122">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="f0c71-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f0c71-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0c71-123">-DefaultProfile</span></span>
<span data-ttu-id="f0c71-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f0c71-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0c71-125">-Identificazione personale</span><span class="sxs-lookup"><span data-stu-id="f0c71-125">-Thumbprint</span></span>
<span data-ttu-id="f0c71-126">Specifica l'identificazione personale del certificato eliminato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0c71-126">Specifies the thumbprint of the certificate that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="f0c71-127">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="f0c71-127">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="f0c71-128">Specifica l'algoritmo usato per derivare il parametro *identificazione personale* .</span><span class="sxs-lookup"><span data-stu-id="f0c71-128">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="f0c71-129">Attualmente, l'unico valore valido è SHA1.</span><span class="sxs-lookup"><span data-stu-id="f0c71-129">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="f0c71-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f0c71-130">-Confirm</span></span>
<span data-ttu-id="f0c71-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0c71-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c71-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0c71-132">-WhatIf</span></span>
<span data-ttu-id="f0c71-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f0c71-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0c71-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f0c71-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c71-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0c71-135">CommonParameters</span></span>
<span data-ttu-id="f0c71-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0c71-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0c71-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f0c71-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0c71-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f0c71-138">INPUTS</span></span>

### <span data-ttu-id="f0c71-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f0c71-139">System.String</span></span>

### <span data-ttu-id="f0c71-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f0c71-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="f0c71-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f0c71-141">OUTPUTS</span></span>

### <span data-ttu-id="f0c71-142">System. void</span><span class="sxs-lookup"><span data-stu-id="f0c71-142">System.Void</span></span>

## <span data-ttu-id="f0c71-143">Note</span><span class="sxs-lookup"><span data-stu-id="f0c71-143">NOTES</span></span>

## <span data-ttu-id="f0c71-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f0c71-144">RELATED LINKS</span></span>

[<span data-ttu-id="f0c71-145">Get-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="f0c71-145">Get-AzBatchCertificate</span></span>](./Get-AzBatchCertificate.md)

[<span data-ttu-id="f0c71-146">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="f0c71-146">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="f0c71-147">New-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="f0c71-147">New-AzBatchCertificate</span></span>](./New-AzBatchCertificate.md)

[<span data-ttu-id="f0c71-148">Stop-AzBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="f0c71-148">Stop-AzBatchCertificateDeletion</span></span>](./Stop-AzBatchCertificateDeletion.md)

[<span data-ttu-id="f0c71-149">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="f0c71-149">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
