---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 9C755BE8-0624-4CF7-AE7C-34DAF44678E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/disable-azurebatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchAutoScale.md
ms.openlocfilehash: 403e38ae72f927b4b98107161b62859aa57bacf9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685782"
---
# <span data-ttu-id="0951f-101">Disable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="0951f-101">Disable-AzureBatchAutoScale</span></span>

## <span data-ttu-id="0951f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0951f-102">SYNOPSIS</span></span>
<span data-ttu-id="0951f-103">Disabilita la scala automatica di un pool.</span><span class="sxs-lookup"><span data-stu-id="0951f-103">Disables automatic scaling of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0951f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0951f-104">SYNTAX</span></span>

```
Disable-AzureBatchAutoScale [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0951f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0951f-105">DESCRIPTION</span></span>
<span data-ttu-id="0951f-106">Il cmdlet **Disable-AzureBatchAutoScale Disabilita** la scala automatica del pool specificato.</span><span class="sxs-lookup"><span data-stu-id="0951f-106">The **Disable-AzureBatchAutoScale** cmdlet disables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="0951f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0951f-107">EXAMPLES</span></span>

### <span data-ttu-id="0951f-108">Esempio 1: disabilitare la scala automatica di un pool</span><span class="sxs-lookup"><span data-stu-id="0951f-108">Example 1: Disable automatic scaling of a pool</span></span>
```
PS C:\>Disable-AzureBatchAutoScale -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="0951f-109">Questo comando Disabilita la scala automatica per il pool denominato pool.</span><span class="sxs-lookup"><span data-stu-id="0951f-109">This command disables automatic scaling for the pool named MyPool.</span></span>

## <span data-ttu-id="0951f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0951f-110">PARAMETERS</span></span>

### <span data-ttu-id="0951f-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="0951f-111">-BatchContext</span></span>
<span data-ttu-id="0951f-112">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="0951f-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="0951f-113">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="0951f-113">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="0951f-114">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="0951f-114">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="0951f-115">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="0951f-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="0951f-116">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="0951f-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="0951f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0951f-117">-DefaultProfile</span></span>
<span data-ttu-id="0951f-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0951f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0951f-119">-ID</span><span class="sxs-lookup"><span data-stu-id="0951f-119">-Id</span></span>
<span data-ttu-id="0951f-120">Specifica l'ID oggetto del pool.</span><span class="sxs-lookup"><span data-stu-id="0951f-120">Specifies the object ID of the pool.</span></span>

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

### <span data-ttu-id="0951f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0951f-121">CommonParameters</span></span>
<span data-ttu-id="0951f-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0951f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0951f-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0951f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0951f-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0951f-124">INPUTS</span></span>

### <span data-ttu-id="0951f-125">System. String</span><span class="sxs-lookup"><span data-stu-id="0951f-125">System.String</span></span>

### <span data-ttu-id="0951f-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0951f-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="0951f-127">Parametri: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0951f-127">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="0951f-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0951f-128">OUTPUTS</span></span>

### <span data-ttu-id="0951f-129">System. void</span><span class="sxs-lookup"><span data-stu-id="0951f-129">System.Void</span></span>

## <span data-ttu-id="0951f-130">Note</span><span class="sxs-lookup"><span data-stu-id="0951f-130">NOTES</span></span>

## <span data-ttu-id="0951f-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0951f-131">RELATED LINKS</span></span>

[<span data-ttu-id="0951f-132">Enable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="0951f-132">Enable-AzureBatchAutoScale</span></span>](./Enable-AzureBatchAutoScale.md)

[<span data-ttu-id="0951f-133">Test-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="0951f-133">Test-AzureBatchAutoScale</span></span>](./Test-AzureBatchAutoScale.md)

[<span data-ttu-id="0951f-134">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="0951f-134">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


