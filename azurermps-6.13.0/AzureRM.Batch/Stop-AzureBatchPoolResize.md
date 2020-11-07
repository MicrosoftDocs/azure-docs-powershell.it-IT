---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3E736E85-0488-4D10-BEA1-4F9B8DA54C4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchPoolResize.md
ms.openlocfilehash: 8db1f11cfd434beb52eb32e4b175b2dab67ecbdb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686637"
---
# <span data-ttu-id="7e489-101">Stop-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="7e489-101">Stop-AzureBatchPoolResize</span></span>

## <span data-ttu-id="7e489-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7e489-102">SYNOPSIS</span></span>
<span data-ttu-id="7e489-103">Interrompe un'operazione di ridimensionamento del pool.</span><span class="sxs-lookup"><span data-stu-id="7e489-103">Stops a pool resize operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e489-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7e489-104">SYNTAX</span></span>

```
Stop-AzureBatchPoolResize [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e489-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e489-105">DESCRIPTION</span></span>
<span data-ttu-id="7e489-106">Il cmdlet **Stop-AzureBatchPoolResize** interrompe un'operazione di ridimensionamento batch di Azure in un pool.</span><span class="sxs-lookup"><span data-stu-id="7e489-106">The **Stop-AzureBatchPoolResize** cmdlet stops an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="7e489-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7e489-107">EXAMPLES</span></span>

### <span data-ttu-id="7e489-108">Esempio 1: interrompere il ridimensionamento di un pool</span><span class="sxs-lookup"><span data-stu-id="7e489-108">Example 1: Stop resizing a pool</span></span>
```
PS C:\>Stop-AzureBatchPoolResize -Id "ContosoPool06" -BatchContext $Context
```

<span data-ttu-id="7e489-109">Questo comando interrompe un'operazione di ridimensionamento nel pool che contiene l'ID ContosoPool06.</span><span class="sxs-lookup"><span data-stu-id="7e489-109">This command stops a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="7e489-110">Usa il cmdlet Get-AzureRmBatchAccountKeys per assegnare un contesto alla variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="7e489-110">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="7e489-111">Esempio 2: interrompere il ridimensionamento di un pool tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="7e489-111">Example 2: Stop resizing a pool by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchPool -Id "ContosoPool06" -BatchContext $Context | Stop-AzureBatchPoolResize -BatchContext $Context
```

<span data-ttu-id="7e489-112">Questo comando interrompe il ridimensionamento di un pool usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="7e489-112">This command stops resizing a pool by using the pipeline operator.</span></span>
<span data-ttu-id="7e489-113">Il comando ottiene il pool con ID ContosoPool06 usando il cmdlet Get-AzureBatchPool.</span><span class="sxs-lookup"><span data-stu-id="7e489-113">The command gets the pool that has the ID ContosoPool06 by using the Get-AzureBatchPool cmdlet.</span></span>
<span data-ttu-id="7e489-114">Il comando passa l'oggetto pool al cmdlet Current.</span><span class="sxs-lookup"><span data-stu-id="7e489-114">The command passes that pool object to the current cmdlet.</span></span>
<span data-ttu-id="7e489-115">Il comando interrompe l'operazione di ridimensionamento su tale pool.</span><span class="sxs-lookup"><span data-stu-id="7e489-115">The command stops the resize operation on that pool.</span></span>

## <span data-ttu-id="7e489-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7e489-116">PARAMETERS</span></span>

### <span data-ttu-id="7e489-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="7e489-117">-BatchContext</span></span>
<span data-ttu-id="7e489-118">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="7e489-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="7e489-119">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="7e489-119">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="7e489-120">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="7e489-120">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="7e489-121">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="7e489-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="7e489-122">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="7e489-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="7e489-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e489-123">-DefaultProfile</span></span>
<span data-ttu-id="7e489-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7e489-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e489-125">-ID</span><span class="sxs-lookup"><span data-stu-id="7e489-125">-Id</span></span>
<span data-ttu-id="7e489-126">Specifica l'ID del pool per il quale questo cmdlet interrompe un'operazione di ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="7e489-126">Specifies the ID of the pool for which this cmdlet stops a resizing operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e489-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e489-127">CommonParameters</span></span>
<span data-ttu-id="7e489-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e489-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e489-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e489-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e489-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7e489-130">INPUTS</span></span>

### <span data-ttu-id="7e489-131">System. String</span><span class="sxs-lookup"><span data-stu-id="7e489-131">System.String</span></span>

### <span data-ttu-id="7e489-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="7e489-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="7e489-133">Parametri: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7e489-133">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="7e489-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7e489-134">OUTPUTS</span></span>

### <span data-ttu-id="7e489-135">System. void</span><span class="sxs-lookup"><span data-stu-id="7e489-135">System.Void</span></span>

## <span data-ttu-id="7e489-136">Note</span><span class="sxs-lookup"><span data-stu-id="7e489-136">NOTES</span></span>

## <span data-ttu-id="7e489-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7e489-137">RELATED LINKS</span></span>

[<span data-ttu-id="7e489-138">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="7e489-138">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="7e489-139">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="7e489-139">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="7e489-140">Start-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="7e489-140">Start-AzureBatchPoolResize</span></span>](./Start-AzureBatchPoolResize.md)

[<span data-ttu-id="7e489-141">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="7e489-141">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


