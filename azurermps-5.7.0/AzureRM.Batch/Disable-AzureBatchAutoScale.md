---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 9C755BE8-0624-4CF7-AE7C-34DAF44678E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/disable-azurebatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchAutoScale.md
ms.openlocfilehash: 1a53e72cd31d3ca43cf5c9a4e6a66de4bc2bd59d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93522063"
---
# <span data-ttu-id="f54da-101">Disable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="f54da-101">Disable-AzureBatchAutoScale</span></span>

## <span data-ttu-id="f54da-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f54da-102">SYNOPSIS</span></span>
<span data-ttu-id="f54da-103">Disabilita la scala automatica di un pool.</span><span class="sxs-lookup"><span data-stu-id="f54da-103">Disables automatic scaling of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f54da-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f54da-104">SYNTAX</span></span>

```
Disable-AzureBatchAutoScale [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f54da-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f54da-105">DESCRIPTION</span></span>
<span data-ttu-id="f54da-106">Il cmdlet **Disable-AzureBatchAutoScale Disabilita** la scala automatica del pool specificato.</span><span class="sxs-lookup"><span data-stu-id="f54da-106">The **Disable-AzureBatchAutoScale** cmdlet disables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="f54da-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f54da-107">EXAMPLES</span></span>

### <span data-ttu-id="f54da-108">Esempio 1: disabilitare la scala automatica di un pool</span><span class="sxs-lookup"><span data-stu-id="f54da-108">Example 1: Disable automatic scaling of a pool</span></span>
```
PS C:\>Disable-AzureBatchAutoScale -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="f54da-109">Questo comando Disabilita la scala automatica per il pool denominato pool.</span><span class="sxs-lookup"><span data-stu-id="f54da-109">This command disables automatic scaling for the pool named MyPool.</span></span>

## <span data-ttu-id="f54da-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f54da-110">PARAMETERS</span></span>

### <span data-ttu-id="f54da-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f54da-111">-BatchContext</span></span>
<span data-ttu-id="f54da-112">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="f54da-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f54da-113">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="f54da-113">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f54da-114">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="f54da-114">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f54da-115">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="f54da-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f54da-116">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="f54da-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f54da-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f54da-117">-DefaultProfile</span></span>
<span data-ttu-id="f54da-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f54da-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f54da-119">-ID</span><span class="sxs-lookup"><span data-stu-id="f54da-119">-Id</span></span>
<span data-ttu-id="f54da-120">Specifica l'ID oggetto del pool.</span><span class="sxs-lookup"><span data-stu-id="f54da-120">Specifies the object ID of the pool.</span></span>

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

### <span data-ttu-id="f54da-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f54da-121">CommonParameters</span></span>
<span data-ttu-id="f54da-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f54da-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f54da-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f54da-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f54da-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f54da-124">INPUTS</span></span>

### <span data-ttu-id="f54da-125">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f54da-125">BatchAccountContext</span></span>
<span data-ttu-id="f54da-126">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="f54da-126">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="f54da-127">Stringa</span><span class="sxs-lookup"><span data-stu-id="f54da-127">String</span></span>
<span data-ttu-id="f54da-128">Il parametro "ID" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="f54da-128">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="f54da-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f54da-129">OUTPUTS</span></span>

## <span data-ttu-id="f54da-130">Note</span><span class="sxs-lookup"><span data-stu-id="f54da-130">NOTES</span></span>

## <span data-ttu-id="f54da-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f54da-131">RELATED LINKS</span></span>

[<span data-ttu-id="f54da-132">Enable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="f54da-132">Enable-AzureBatchAutoScale</span></span>](./Enable-AzureBatchAutoScale.md)

[<span data-ttu-id="f54da-133">Test-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="f54da-133">Test-AzureBatchAutoScale</span></span>](./Test-AzureBatchAutoScale.md)

[<span data-ttu-id="f54da-134">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="f54da-134">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


