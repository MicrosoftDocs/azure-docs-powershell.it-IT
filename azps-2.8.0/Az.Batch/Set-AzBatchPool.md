---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 23893EAE-47F3-45AA-AEB2-354FB8316C25
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPool.md
ms.openlocfilehash: 7ab0d9f64b14f6fbdd572f69ecb081114d78891d
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2020
ms.locfileid: "93865669"
---
# <span data-ttu-id="13898-101">Set-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="13898-101">Set-AzBatchPool</span></span>

## <span data-ttu-id="13898-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="13898-102">SYNOPSIS</span></span>
<span data-ttu-id="13898-103">Aggiorna le proprietà di un pool.</span><span class="sxs-lookup"><span data-stu-id="13898-103">Updates the properties of a pool.</span></span>

## <span data-ttu-id="13898-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="13898-104">SYNTAX</span></span>

```
Set-AzBatchPool [-Pool] <PSCloudPool> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13898-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="13898-105">DESCRIPTION</span></span>
<span data-ttu-id="13898-106">Il cmdlet **set-AzBatchPool** aggiorna le proprietà di un pool nel servizio batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="13898-106">The **Set-AzBatchPool** cmdlet updates the properties of a pool in the Azure Batch service.</span></span>
<span data-ttu-id="13898-107">Usa il cmdlet Get-AzBatchPool per ottenere un oggetto **PSCloudPool** .</span><span class="sxs-lookup"><span data-stu-id="13898-107">Use the Get-AzBatchPool cmdlet to get a **PSCloudPool** object.</span></span>
<span data-ttu-id="13898-108">Modificare le proprietà di tale oggetto e quindi usare il cmdlet corrente per eseguire il commit delle modifiche apportate al servizio batch.</span><span class="sxs-lookup"><span data-stu-id="13898-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="13898-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="13898-109">EXAMPLES</span></span>

### <span data-ttu-id="13898-110">Esempio 1: aggiornare un pool</span><span class="sxs-lookup"><span data-stu-id="13898-110">Example 1: Update a pool</span></span>
```
PS C:\>$Pool = Get-AzBatchPool "ContosoPool" -BatchContext $Context
PS C:\> $StartTask = New-Object Microsoft.Azure.Commands.Batch.Models.PSStartTask
PS C:\> $StartTask.CommandLine = "cmd /c echo example"
PS C:\> $Pool.StartTask = $StartTask
PS C:\> Set-AzBatchPool -Pool $Pool -BatchContext $Context
```

<span data-ttu-id="13898-111">Il primo comando ottiene un pool utilizzando **Get-AzBatchPool** e lo archivia nella variabile $pool.</span><span class="sxs-lookup"><span data-stu-id="13898-111">The first command gets a pool by using **Get-AzBatchPool** , and then stores it in the $Pool variable.</span></span>
<span data-ttu-id="13898-112">I tre comandi successivi modificano la specifica dell'attività Start nell'oggetto $Pool.</span><span class="sxs-lookup"><span data-stu-id="13898-112">The next three commands modify the start task specification on the $Pool object.</span></span>
<span data-ttu-id="13898-113">Il comando finale aggiorna il servizio batch in base all'oggetto locale in $Pool.</span><span class="sxs-lookup"><span data-stu-id="13898-113">The final command updates the Batch service to match the local object in $Pool.</span></span>

## <span data-ttu-id="13898-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="13898-114">PARAMETERS</span></span>

### <span data-ttu-id="13898-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="13898-115">-BatchContext</span></span>
<span data-ttu-id="13898-116">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="13898-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="13898-117">Se si usa il cmdlet Get-AzBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="13898-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="13898-118">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="13898-118">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="13898-119">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="13898-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="13898-120">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="13898-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="13898-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13898-121">-DefaultProfile</span></span>
<span data-ttu-id="13898-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="13898-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13898-123">-Pool</span><span class="sxs-lookup"><span data-stu-id="13898-123">-Pool</span></span>
<span data-ttu-id="13898-124">Specifica il **PSCloudPool** a cui questo cmdlet aggiorna il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="13898-124">Specifies the **PSCloudPool** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="13898-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13898-125">CommonParameters</span></span>
<span data-ttu-id="13898-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13898-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13898-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13898-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13898-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="13898-128">INPUTS</span></span>

### <span data-ttu-id="13898-129">Microsoft.Azure.Commands.Batch. Models. PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="13898-129">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="13898-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="13898-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="13898-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="13898-131">OUTPUTS</span></span>

### <span data-ttu-id="13898-132">System. void</span><span class="sxs-lookup"><span data-stu-id="13898-132">System.Void</span></span>

## <span data-ttu-id="13898-133">Note</span><span class="sxs-lookup"><span data-stu-id="13898-133">NOTES</span></span>

## <span data-ttu-id="13898-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="13898-134">RELATED LINKS</span></span>

[<span data-ttu-id="13898-135">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="13898-135">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="13898-136">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="13898-136">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="13898-137">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="13898-137">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="13898-138">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="13898-138">Remove-AzBatchPool</span></span>](./Remove-AzBatchPool.md)

[<span data-ttu-id="13898-139">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="13898-139">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


