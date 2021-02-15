---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 23893EAE-47F3-45AA-AEB2-354FB8316C25
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPool.md
ms.openlocfilehash: 423f249a7971883cbe47d8f499fdd780980362f3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197007"
---
# <span data-ttu-id="a10a3-101">Set-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="a10a3-101">Set-AzBatchPool</span></span>

## <span data-ttu-id="a10a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a10a3-102">SYNOPSIS</span></span>
<span data-ttu-id="a10a3-103">Aggiorna le proprietà di un pool.</span><span class="sxs-lookup"><span data-stu-id="a10a3-103">Updates the properties of a pool.</span></span>

## <span data-ttu-id="a10a3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a10a3-104">SYNTAX</span></span>

```
Set-AzBatchPool [-Pool] <PSCloudPool> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a10a3-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a10a3-105">DESCRIPTION</span></span>
<span data-ttu-id="a10a3-106">Il cmdlet **Set-AzBatchPool** aggiorna le proprietà di un pool nel servizio batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="a10a3-106">The **Set-AzBatchPool** cmdlet updates the properties of a pool in the Azure Batch service.</span></span>
<span data-ttu-id="a10a3-107">Usare il cmdlet Get-AzBatchPool per ottenere un **oggetto PSCloudPool.**</span><span class="sxs-lookup"><span data-stu-id="a10a3-107">Use the Get-AzBatchPool cmdlet to get a **PSCloudPool** object.</span></span>
<span data-ttu-id="a10a3-108">Modificare le proprietà dell'oggetto e quindi usare il cmdlet corrente per eseguire il commit delle modifiche al servizio batch.</span><span class="sxs-lookup"><span data-stu-id="a10a3-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="a10a3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a10a3-109">EXAMPLES</span></span>

### <span data-ttu-id="a10a3-110">Esempio 1: Aggiornare un pool</span><span class="sxs-lookup"><span data-stu-id="a10a3-110">Example 1: Update a pool</span></span>
```
PS C:\>$Pool = Get-AzBatchPool "ContosoPool" -BatchContext $Context
PS C:\> $StartTask = New-Object Microsoft.Azure.Commands.Batch.Models.PSStartTask
PS C:\> $StartTask.CommandLine = "cmd /c echo example"
PS C:\> $Pool.StartTask = $StartTask
PS C:\> Set-AzBatchPool -Pool $Pool -BatchContext $Context
```

<span data-ttu-id="a10a3-111">Il primo comando ottiene un pool con **Get-AzBatchPool** e quindi lo archivia nella variabile $Pool locale.</span><span class="sxs-lookup"><span data-stu-id="a10a3-111">The first command gets a pool by using **Get-AzBatchPool**, and then stores it in the $Pool variable.</span></span>
<span data-ttu-id="a10a3-112">I tre comandi seguenti modificano la specifica dell'attività di inizio nell$Pool o object.</span><span class="sxs-lookup"><span data-stu-id="a10a3-112">The next three commands modify the start task specification on the $Pool object.</span></span>
<span data-ttu-id="a10a3-113">Il comando finale aggiorna il servizio batch in modo che corrisponda all'oggetto locale in $Pool.</span><span class="sxs-lookup"><span data-stu-id="a10a3-113">The final command updates the Batch service to match the local object in $Pool.</span></span>

## <span data-ttu-id="a10a3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a10a3-114">PARAMETERS</span></span>

### <span data-ttu-id="a10a3-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a10a3-115">-BatchContext</span></span>
<span data-ttu-id="a10a3-116">Specifica **l'istanza BatchAccountContext** che questo cmdlet usa per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="a10a3-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a10a3-117">Se si usa il cmdlet Get-AzBatchAccount per ottenere BatchAccountContext, verrà usata l'autenticazione di Azure Active Directory quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="a10a3-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a10a3-118">Per usare invece l'autenticazione della chiave condivisa, usare il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con le relative chiavi di accesso popolate.</span><span class="sxs-lookup"><span data-stu-id="a10a3-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a10a3-119">Quando si usa l'autenticazione con chiave condivisa, per impostazione predefinita viene usata la chiave di accesso primario.</span><span class="sxs-lookup"><span data-stu-id="a10a3-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a10a3-120">Per modificare la chiave da usare, impostare la proprietà BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="a10a3-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a10a3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a10a3-121">-DefaultProfile</span></span>
<span data-ttu-id="a10a3-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a10a3-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a10a3-123">-Pool</span><span class="sxs-lookup"><span data-stu-id="a10a3-123">-Pool</span></span>
<span data-ttu-id="a10a3-124">Specifica **psCloudPool** a cui questo cmdlet aggiorna il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="a10a3-124">Specifies the **PSCloudPool** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudPool
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a10a3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a10a3-125">CommonParameters</span></span>
<span data-ttu-id="a10a3-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a10a3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a10a3-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a10a3-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a10a3-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="a10a3-128">INPUTS</span></span>

### <span data-ttu-id="a10a3-129">Microsoft.Azure.Commands.Batch. Models.PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="a10a3-129">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="a10a3-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a10a3-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="a10a3-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a10a3-131">OUTPUTS</span></span>

### <span data-ttu-id="a10a3-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="a10a3-132">System.Void</span></span>

## <span data-ttu-id="a10a3-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="a10a3-133">NOTES</span></span>

## <span data-ttu-id="a10a3-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a10a3-134">RELATED LINKS</span></span>

[<span data-ttu-id="a10a3-135">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="a10a3-135">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="a10a3-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="a10a3-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="a10a3-137">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="a10a3-137">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="a10a3-138">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="a10a3-138">Remove-AzBatchPool</span></span>](./Remove-AzBatchPool.md)

[<span data-ttu-id="a10a3-139">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="a10a3-139">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
