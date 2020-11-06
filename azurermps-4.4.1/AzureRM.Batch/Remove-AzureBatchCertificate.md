---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3DFFD0F2-6CD8-4FBE-B15C-8505CBF8F44E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchCertificate.md
ms.openlocfilehash: c63caed99a10851d6172e0db5dcc33e3404be215
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511308"
---
# <span data-ttu-id="8ec33-101">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="8ec33-101">Remove-AzureBatchCertificate</span></span>

## <span data-ttu-id="8ec33-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8ec33-102">SYNOPSIS</span></span>
<span data-ttu-id="8ec33-103">Elimina un certificato da un account.</span><span class="sxs-lookup"><span data-stu-id="8ec33-103">Deletes a certificate from an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ec33-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8ec33-104">SYNTAX</span></span>

```
Remove-AzureBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8ec33-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8ec33-105">DESCRIPTION</span></span>
<span data-ttu-id="8ec33-106">Il cmdlet **Remove-AzureBatchCertificate** rimuove un certificato dall'account batch di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="8ec33-106">The **Remove-AzureBatchCertificate** cmdlet removes a certificate from the specified Azure Batch account.</span></span>

## <span data-ttu-id="8ec33-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8ec33-107">EXAMPLES</span></span>

### <span data-ttu-id="8ec33-108">Esempio 1: rimuovere un certificato</span><span class="sxs-lookup"><span data-stu-id="8ec33-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureBatchCertificate -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="8ec33-109">Questo comando rimuove il certificato con l'identificazione personale specificata.</span><span class="sxs-lookup"><span data-stu-id="8ec33-109">This command removes the certificate that has the specified thumbprint.</span></span>

### <span data-ttu-id="8ec33-110">Esempio 2: rimuovere tutti i certificati attivi</span><span class="sxs-lookup"><span data-stu-id="8ec33-110">Example 2:Remove all active certificates</span></span>
```
PS C:\>Get-AzureBatchCertificate -Filter "state eq 'active'" -BatchContext $Context | Remove-AzureBatchCertificate -Force -BatchContext $Context
```

<span data-ttu-id="8ec33-111">Questo comando ottiene tutti i certificati attivi tramite il cmdlet Get-AzureBatchCertificate.</span><span class="sxs-lookup"><span data-stu-id="8ec33-111">This command gets all certificates that are active by using the Get-AzureBatchCertificate cmdlet.</span></span>
<span data-ttu-id="8ec33-112">Il comando passa i certificati attivi al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="8ec33-112">The command passes the active certificates to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8ec33-113">Questo cmdlet rimuove ogni certificato.</span><span class="sxs-lookup"><span data-stu-id="8ec33-113">That cmdlet removes each certificate.</span></span>
<span data-ttu-id="8ec33-114">Il comando specifica il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="8ec33-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="8ec33-115">Di conseguenza, il comando non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="8ec33-115">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="8ec33-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8ec33-116">PARAMETERS</span></span>

### <span data-ttu-id="8ec33-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="8ec33-117">-BatchContext</span></span>
<span data-ttu-id="8ec33-118">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="8ec33-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8ec33-119">Per ottenere un oggetto **BatchAccountContext** che contiene i tasti di scelta per l'abbonamento, usare il cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="8ec33-119">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="8ec33-120">-Identificazione personale</span><span class="sxs-lookup"><span data-stu-id="8ec33-120">-Thumbprint</span></span>
<span data-ttu-id="8ec33-121">Specifica l'identificazione personale del certificato eliminato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ec33-121">Specifies the thumbprint of the certificate that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="8ec33-122">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="8ec33-122">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="8ec33-123">Specifica l'algoritmo usato per derivare il parametro *identificazione personale* .</span><span class="sxs-lookup"><span data-stu-id="8ec33-123">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="8ec33-124">Attualmente, l'unico valore valido è SHA1.</span><span class="sxs-lookup"><span data-stu-id="8ec33-124">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="8ec33-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8ec33-125">-Confirm</span></span>
<span data-ttu-id="8ec33-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ec33-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ec33-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ec33-127">-WhatIf</span></span>
<span data-ttu-id="8ec33-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8ec33-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ec33-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8ec33-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ec33-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ec33-130">-DefaultProfile</span></span>
<span data-ttu-id="8ec33-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8ec33-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ec33-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ec33-132">CommonParameters</span></span>
<span data-ttu-id="8ec33-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ec33-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ec33-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ec33-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ec33-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8ec33-135">INPUTS</span></span>

### <span data-ttu-id="8ec33-136">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8ec33-136">BatchAccountContext</span></span>
<span data-ttu-id="8ec33-137">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="8ec33-137">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="8ec33-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8ec33-138">OUTPUTS</span></span>

## <span data-ttu-id="8ec33-139">Note</span><span class="sxs-lookup"><span data-stu-id="8ec33-139">NOTES</span></span>

## <span data-ttu-id="8ec33-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8ec33-140">RELATED LINKS</span></span>

[<span data-ttu-id="8ec33-141">Get-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="8ec33-141">Get-AzureBatchCertificate</span></span>](./Get-AzureBatchCertificate.md)

[<span data-ttu-id="8ec33-142">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="8ec33-142">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="8ec33-143">New-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="8ec33-143">New-AzureBatchCertificate</span></span>](./New-AzureBatchCertificate.md)

[<span data-ttu-id="8ec33-144">Stop-AzureBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="8ec33-144">Stop-AzureBatchCertificateDeletion</span></span>](./Stop-AzureBatchCertificateDeletion.md)

[<span data-ttu-id="8ec33-145">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="8ec33-145">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


