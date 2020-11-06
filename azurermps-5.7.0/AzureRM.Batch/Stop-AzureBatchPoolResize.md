---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3E736E85-0488-4D10-BEA1-4F9B8DA54C4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchPoolResize.md
ms.openlocfilehash: 153e566df3e2ab6f758d139719af1e812e0476ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510099"
---
# <span data-ttu-id="bdcb5-101">Stop-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="bdcb5-101">Stop-AzureBatchPoolResize</span></span>

## <span data-ttu-id="bdcb5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bdcb5-102">SYNOPSIS</span></span>
<span data-ttu-id="bdcb5-103">Interrompe un'operazione di ridimensionamento del pool.</span><span class="sxs-lookup"><span data-stu-id="bdcb5-103">Stops a pool resize operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bdcb5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bdcb5-104">SYNTAX</span></span>

```
Stop-AzureBatchPoolResize [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bdcb5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bdcb5-105">DESCRIPTION</span></span>
<span data-ttu-id="bdcb5-106">Il cmdlet **Stop-AzureBatchPoolResize** interrompe un'operazione di ridimensionamento batch di Azure in un pool.</span><span class="sxs-lookup"><span data-stu-id="bdcb5-106">The **Stop-AzureBatchPoolResize** cmdlet stops an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="bdcb5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bdcb5-107">EXAMPLES</span></span>

### <span data-ttu-id="bdcb5-108">Esempio 1: interrompere il ridimensionamento di un pool</span><span class="sxs-lookup"><span data-stu-id="bdcb5-108">Example 1: Stop resizing a pool</span></span>
```
PS C:\>Stop-AzureBatchPoolResize -Id "ContosoPool06" -BatchContext $Context
```

<span data-ttu-id="bdcb5-109">Questo comando interrompe un'operazione di ridimensionamento nel pool che contiene l'ID ContosoPool06.</span><span class="sxs-lookup"><span data-stu-id="bdcb5-109">This command stops a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="bdcb5-110">Usa il cmdlet Get-AzureRmBatchAccountKeys per assegnare un contesto alla variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="bdcb5-110">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="bdcb5-111">Esempio 2: interrompere il ridimensionamento di un pool tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="bdcb5-111">Example 2: Stop resizing a pool by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchPool -Id "ContosoPool06" -BatchContext $Context | Stop-AzureBatchPoolResize -BatchContext $Context
```

<span data-ttu-id="bdcb5-112">Questo comando interrompe il ridimensionamento di un pool usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="bdcb5-112">This command stops resizing a pool by using the pipeline operator.</span></span>
<span data-ttu-id="bdcb5-113">Il comando ottiene il pool con ID ContosoPool06 usando il cmdlet Get-AzureBatchPool.</span><span class="sxs-lookup"><span data-stu-id="bdcb5-113">The command gets the pool that has the ID ContosoPool06 by using the Get-AzureBatchPool cmdlet.</span></span>
<span data-ttu-id="bdcb5-114">Il comando passa l'oggetto pool al cmdlet Current.</span><span class="sxs-lookup"><span data-stu-id="bdcb5-114">The command passes that pool object to the current cmdlet.</span></span>
<span data-ttu-id="bdcb5-115">Il comando interrompe l'operazione di ridimensionamento su tale pool.</span><span class="sxs-lookup"><span data-stu-id="bdcb5-115">The command stops the resize operation on that pool.</span></span>

## <span data-ttu-id="bdcb5-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bdcb5-116">PARAMETERS</span></span>

### <span data-ttu-id="bdcb5-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="bdcb5-117">-BatchContext</span></span>
<span data-ttu-id="bdcb5-118">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="bdcb5-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="bdcb5-119">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="bdcb5-119">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="bdcb5-120">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="bdcb5-120">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="bdcb5-121">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="bdcb5-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="bdcb5-122">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="bdcb5-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="bdcb5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdcb5-123">-DefaultProfile</span></span>
<span data-ttu-id="bdcb5-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bdcb5-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bdcb5-125">-ID</span><span class="sxs-lookup"><span data-stu-id="bdcb5-125">-Id</span></span>
<span data-ttu-id="bdcb5-126">Specifica l'ID del pool per il quale questo cmdlet interrompe un'operazione di ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="bdcb5-126">Specifies the ID of the pool for which this cmdlet stops a resizing operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bdcb5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdcb5-127">CommonParameters</span></span>
<span data-ttu-id="bdcb5-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdcb5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdcb5-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdcb5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdcb5-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bdcb5-130">INPUTS</span></span>

### <span data-ttu-id="bdcb5-131">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="bdcb5-131">BatchAccountContext</span></span>
<span data-ttu-id="bdcb5-132">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="bdcb5-132">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="bdcb5-133">Stringa</span><span class="sxs-lookup"><span data-stu-id="bdcb5-133">String</span></span>
<span data-ttu-id="bdcb5-134">Il parametro "ID" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="bdcb5-134">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="bdcb5-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bdcb5-135">OUTPUTS</span></span>

## <span data-ttu-id="bdcb5-136">Note</span><span class="sxs-lookup"><span data-stu-id="bdcb5-136">NOTES</span></span>

## <span data-ttu-id="bdcb5-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bdcb5-137">RELATED LINKS</span></span>

[<span data-ttu-id="bdcb5-138">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="bdcb5-138">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="bdcb5-139">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="bdcb5-139">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="bdcb5-140">Start-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="bdcb5-140">Start-AzureBatchPoolResize</span></span>](./Start-AzureBatchPoolResize.md)

[<span data-ttu-id="bdcb5-141">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="bdcb5-141">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


