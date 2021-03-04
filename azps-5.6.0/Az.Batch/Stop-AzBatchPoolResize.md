---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3E736E85-0488-4D10-BEA1-4F9B8DA54C4B
online version: https://docs.microsoft.com/powershell/module/az.batch/stop-azbatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchPoolResize.md
ms.openlocfilehash: 339c3a537e84ff63a6eac0a6f1f63669ce4567ae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959822"
---
# <span data-ttu-id="d4950-101">Stop-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="d4950-101">Stop-AzBatchPoolResize</span></span>

## <span data-ttu-id="d4950-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4950-102">SYNOPSIS</span></span>
<span data-ttu-id="d4950-103">Interrompe un'operazione di ridimensionamento del pool.</span><span class="sxs-lookup"><span data-stu-id="d4950-103">Stops a pool resize operation.</span></span>

## <span data-ttu-id="d4950-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d4950-104">SYNTAX</span></span>

```
Stop-AzBatchPoolResize [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4950-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d4950-105">DESCRIPTION</span></span>
<span data-ttu-id="d4950-106">Il cmdlet **Stop-AzBatchPoolResize interrompe** un'operazione di ridimensionamento batch di Azure in un pool.</span><span class="sxs-lookup"><span data-stu-id="d4950-106">The **Stop-AzBatchPoolResize** cmdlet stops an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="d4950-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d4950-107">EXAMPLES</span></span>

### <span data-ttu-id="d4950-108">Esempio 1: Interrompere il ridimensionamento di un pool</span><span class="sxs-lookup"><span data-stu-id="d4950-108">Example 1: Stop resizing a pool</span></span>
```
PS C:\>Stop-AzBatchPoolResize -Id "ContosoPool06" -BatchContext $Context
```

<span data-ttu-id="d4950-109">Questo comando interrompe un'operazione di ridimensionamento nel pool con l'ID ContosoPool06.</span><span class="sxs-lookup"><span data-stu-id="d4950-109">This command stops a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="d4950-110">Usare il cmdlet Get-AzBatchAccountKey per assegnare un contesto alla $Context variabile.</span><span class="sxs-lookup"><span data-stu-id="d4950-110">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="d4950-111">Esempio 2: Interrompere il ridimensionamento di un pool tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="d4950-111">Example 2: Stop resizing a pool by using the pipeline</span></span>
```
PS C:\>Get-AzBatchPool -Id "ContosoPool06" -BatchContext $Context | Stop-AzBatchPoolResize -BatchContext $Context
```

<span data-ttu-id="d4950-112">Questo comando interrompe il ridimensionamento di un pool con l'operatore della pipeline.</span><span class="sxs-lookup"><span data-stu-id="d4950-112">This command stops resizing a pool by using the pipeline operator.</span></span>
<span data-ttu-id="d4950-113">Il comando ottiene il pool con l'ID ContosoPool06 usando il cmdlet Get-AzBatchPool></span><span class="sxs-lookup"><span data-stu-id="d4950-113">The command gets the pool that has the ID ContosoPool06 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="d4950-114">Il comando passa l'oggetto pool al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="d4950-114">The command passes that pool object to the current cmdlet.</span></span>
<span data-ttu-id="d4950-115">Il comando interrompe l'operazione di ridimensionamento nel pool.</span><span class="sxs-lookup"><span data-stu-id="d4950-115">The command stops the resize operation on that pool.</span></span>

## <span data-ttu-id="d4950-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4950-116">PARAMETERS</span></span>

### <span data-ttu-id="d4950-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d4950-117">-BatchContext</span></span>
<span data-ttu-id="d4950-118">Specifica **l'istanza BatchAccountContext** che questo cmdlet usa per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="d4950-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d4950-119">Se si usa il cmdlet Get-AzBatchAccount per ottenere BatchAccountContext, verrà usata l'autenticazione di Azure Active Directory quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="d4950-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d4950-120">Per usare invece l'autenticazione della chiave condivisa, usare il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con le relative chiavi di accesso popolate.</span><span class="sxs-lookup"><span data-stu-id="d4950-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d4950-121">Quando si usa l'autenticazione con chiave condivisa, per impostazione predefinita viene usata la chiave di accesso primario.</span><span class="sxs-lookup"><span data-stu-id="d4950-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d4950-122">Per modificare la chiave da usare, impostare la proprietà BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="d4950-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="d4950-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4950-123">-DefaultProfile</span></span>
<span data-ttu-id="d4950-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d4950-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4950-125">-Id</span><span class="sxs-lookup"><span data-stu-id="d4950-125">-Id</span></span>
<span data-ttu-id="d4950-126">Specifica l'ID del pool per cui questo cmdlet interrompe un'operazione di ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="d4950-126">Specifies the ID of the pool for which this cmdlet stops a resizing operation.</span></span>

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

### <span data-ttu-id="d4950-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4950-127">CommonParameters</span></span>
<span data-ttu-id="d4950-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4950-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4950-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d4950-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4950-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="d4950-130">INPUTS</span></span>

### <span data-ttu-id="d4950-131">System.String</span><span class="sxs-lookup"><span data-stu-id="d4950-131">System.String</span></span>

### <span data-ttu-id="d4950-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d4950-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="d4950-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d4950-133">OUTPUTS</span></span>

### <span data-ttu-id="d4950-134">System.Void</span><span class="sxs-lookup"><span data-stu-id="d4950-134">System.Void</span></span>

## <span data-ttu-id="d4950-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="d4950-135">NOTES</span></span>

## <span data-ttu-id="d4950-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d4950-136">RELATED LINKS</span></span>

[<span data-ttu-id="d4950-137">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="d4950-137">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="d4950-138">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="d4950-138">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="d4950-139">Start-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="d4950-139">Start-AzBatchPoolResize</span></span>](./Start-AzBatchPoolResize.md)

[<span data-ttu-id="d4950-140">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="d4950-140">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
