---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 9C755BE8-0624-4CF7-AE7C-34DAF44678E8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchAutoScale.md
ms.openlocfilehash: 124000fdf11b3fa5b90253fc3b9a75c040725ba8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518375"
---
# <span data-ttu-id="60026-101">Disable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="60026-101">Disable-AzureBatchAutoScale</span></span>

## <span data-ttu-id="60026-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="60026-102">SYNOPSIS</span></span>
<span data-ttu-id="60026-103">Disabilita la scala automatica di un pool.</span><span class="sxs-lookup"><span data-stu-id="60026-103">Disables automatic scaling of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60026-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="60026-104">SYNTAX</span></span>

```
Disable-AzureBatchAutoScale [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60026-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60026-105">DESCRIPTION</span></span>
<span data-ttu-id="60026-106">Il cmdlet **Disable-AzureBatchAutoScale Disabilita** la scala automatica del pool specificato.</span><span class="sxs-lookup"><span data-stu-id="60026-106">The **Disable-AzureBatchAutoScale** cmdlet disables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="60026-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="60026-107">EXAMPLES</span></span>

### <span data-ttu-id="60026-108">Esempio 1: disabilitare la scala automatica di un pool</span><span class="sxs-lookup"><span data-stu-id="60026-108">Example 1: Disable automatic scaling of a pool</span></span>
```
PS C:\>Disable-AzureBatchAutoScale -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="60026-109">Questo comando Disabilita la scala automatica per il pool denominato pool.</span><span class="sxs-lookup"><span data-stu-id="60026-109">This command disables automatic scaling for the pool named MyPool.</span></span>

## <span data-ttu-id="60026-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="60026-110">PARAMETERS</span></span>

### <span data-ttu-id="60026-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="60026-111">-BatchContext</span></span>
<span data-ttu-id="60026-112">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="60026-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="60026-113">Per ottenere un oggetto **BatchAccountContext** che contiene i tasti di scelta per l'abbonamento, usare il cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="60026-113">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="60026-114">-ID</span><span class="sxs-lookup"><span data-stu-id="60026-114">-Id</span></span>
<span data-ttu-id="60026-115">Specifica l'ID oggetto del pool.</span><span class="sxs-lookup"><span data-stu-id="60026-115">Specifies the object ID of the pool.</span></span>

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

### <span data-ttu-id="60026-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60026-116">-DefaultProfile</span></span>
<span data-ttu-id="60026-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="60026-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60026-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60026-118">CommonParameters</span></span>
<span data-ttu-id="60026-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60026-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60026-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60026-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60026-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="60026-121">INPUTS</span></span>

### <span data-ttu-id="60026-122">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="60026-122">BatchAccountContext</span></span>
<span data-ttu-id="60026-123">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="60026-123">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="60026-124">Stringa</span><span class="sxs-lookup"><span data-stu-id="60026-124">String</span></span>
<span data-ttu-id="60026-125">Il parametro "ID" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="60026-125">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="60026-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="60026-126">OUTPUTS</span></span>

## <span data-ttu-id="60026-127">Note</span><span class="sxs-lookup"><span data-stu-id="60026-127">NOTES</span></span>

## <span data-ttu-id="60026-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="60026-128">RELATED LINKS</span></span>

[<span data-ttu-id="60026-129">Enable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="60026-129">Enable-AzureBatchAutoScale</span></span>](./Enable-AzureBatchAutoScale.md)

[<span data-ttu-id="60026-130">Test-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="60026-130">Test-AzureBatchAutoScale</span></span>](./Test-AzureBatchAutoScale.md)

[<span data-ttu-id="60026-131">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="60026-131">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


