---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9C755BE8-0624-4CF7-AE7C-34DAF44678E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchAutoScale.md
ms.openlocfilehash: c0a0f0a11b4caf18b12c21d37dd18ef153220a97
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478427"
---
# <span data-ttu-id="860e0-101">Disable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="860e0-101">Disable-AzBatchAutoScale</span></span>

## <span data-ttu-id="860e0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="860e0-102">SYNOPSIS</span></span>
<span data-ttu-id="860e0-103">Disabilita la scala automatica di un pool.</span><span class="sxs-lookup"><span data-stu-id="860e0-103">Disables automatic scaling of a pool.</span></span>

## <span data-ttu-id="860e0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="860e0-104">SYNTAX</span></span>

```
Disable-AzBatchAutoScale [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="860e0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="860e0-105">DESCRIPTION</span></span>
<span data-ttu-id="860e0-106">Il cmdlet **Disable-AzBatchAutoScale Disabilita** la scala automatica del pool specificato.</span><span class="sxs-lookup"><span data-stu-id="860e0-106">The **Disable-AzBatchAutoScale** cmdlet disables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="860e0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="860e0-107">EXAMPLES</span></span>

### <span data-ttu-id="860e0-108">Esempio 1: disabilitare la scala automatica di un pool</span><span class="sxs-lookup"><span data-stu-id="860e0-108">Example 1: Disable automatic scaling of a pool</span></span>
```
PS C:\>Disable-AzBatchAutoScale -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="860e0-109">Questo comando Disabilita la scala automatica per il pool denominato pool.</span><span class="sxs-lookup"><span data-stu-id="860e0-109">This command disables automatic scaling for the pool named MyPool.</span></span>

## <span data-ttu-id="860e0-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="860e0-110">PARAMETERS</span></span>

### <span data-ttu-id="860e0-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="860e0-111">-BatchContext</span></span>
<span data-ttu-id="860e0-112">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="860e0-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="860e0-113">Se si usa il cmdlet Get-AzBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="860e0-113">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="860e0-114">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="860e0-114">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="860e0-115">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="860e0-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="860e0-116">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="860e0-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="860e0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="860e0-117">-DefaultProfile</span></span>
<span data-ttu-id="860e0-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="860e0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="860e0-119">-ID</span><span class="sxs-lookup"><span data-stu-id="860e0-119">-Id</span></span>
<span data-ttu-id="860e0-120">Specifica l'ID oggetto del pool.</span><span class="sxs-lookup"><span data-stu-id="860e0-120">Specifies the object ID of the pool.</span></span>

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

### <span data-ttu-id="860e0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="860e0-121">CommonParameters</span></span>
<span data-ttu-id="860e0-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="860e0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="860e0-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="860e0-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="860e0-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="860e0-124">INPUTS</span></span>

### <span data-ttu-id="860e0-125">System. String</span><span class="sxs-lookup"><span data-stu-id="860e0-125">System.String</span></span>

### <span data-ttu-id="860e0-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="860e0-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="860e0-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="860e0-127">OUTPUTS</span></span>

### <span data-ttu-id="860e0-128">System. void</span><span class="sxs-lookup"><span data-stu-id="860e0-128">System.Void</span></span>

## <span data-ttu-id="860e0-129">Note</span><span class="sxs-lookup"><span data-stu-id="860e0-129">NOTES</span></span>

## <span data-ttu-id="860e0-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="860e0-130">RELATED LINKS</span></span>

[<span data-ttu-id="860e0-131">Enable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="860e0-131">Enable-AzBatchAutoScale</span></span>](./Enable-AzBatchAutoScale.md)

[<span data-ttu-id="860e0-132">Test-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="860e0-132">Test-AzBatchAutoScale</span></span>](./Test-AzBatchAutoScale.md)

[<span data-ttu-id="860e0-133">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="860e0-133">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)


