---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: BF0C1A2F-2703-492F-A3A7-053416A5D1EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/test-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Test-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Test-AzBatchAutoScale.md
ms.openlocfilehash: dcac72f8ca362ea87d464e024d6e77b2b3b61425
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2020
ms.locfileid: "93685279"
---
# <span data-ttu-id="66b2c-101">Test-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="66b2c-101">Test-AzBatchAutoScale</span></span>

## <span data-ttu-id="66b2c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="66b2c-102">SYNOPSIS</span></span>
<span data-ttu-id="66b2c-103">Ottiene il risultato di una formula di ridimensionamento automatico in un pool.</span><span class="sxs-lookup"><span data-stu-id="66b2c-103">Gets the result of an automatic scaling formula on a pool.</span></span>

## <span data-ttu-id="66b2c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="66b2c-104">SYNTAX</span></span>

```
Test-AzBatchAutoScale [-Id] <String> [-AutoScaleFormula] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66b2c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="66b2c-105">DESCRIPTION</span></span>
<span data-ttu-id="66b2c-106">Il cmdlet **test-AzBatchAutoScale** ottiene il risultato di una formula di ridimensionamento automatico nel pool specificato.</span><span class="sxs-lookup"><span data-stu-id="66b2c-106">The **Test-AzBatchAutoScale** cmdlet gets the result of an automatic scaling formula on the specified pool.</span></span>

## <span data-ttu-id="66b2c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="66b2c-107">EXAMPLES</span></span>

### <span data-ttu-id="66b2c-108">Esempio 1: valutare una formula di scalabilità verticale in un pool</span><span class="sxs-lookup"><span data-stu-id="66b2c-108">Example 1: Evaluate an autoscale formula on a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> $Evaluation = Test-AzBatchAutoScale -Id "ContosoPool" -AutoScaleFormula $Formula -BatchContext $Context
PS C:\> $Evaluation.AutoScaleRun.Results
$TargetDedicated=5;$NodeDeallocationOption=requeue;totalNodes=5
```

<span data-ttu-id="66b2c-109">Il primo comando Archivia una formula nella variabile $Formula per l'uso nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="66b2c-109">The first command stores a formula in the $Formula variable for use in the example.</span></span>
<span data-ttu-id="66b2c-110">Il secondo comando valuta la formula di scalabilità verticale nel pool che contiene l'ID ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="66b2c-110">The second command evaluates the autoscale formula on the pool that has the ID ContosoPool.</span></span>
<span data-ttu-id="66b2c-111">Il comando finale Visualizza i **risultati** usando la sintassi del punto standard.</span><span class="sxs-lookup"><span data-stu-id="66b2c-111">The final command displays the **Results** by using standard dot syntax.</span></span>

## <span data-ttu-id="66b2c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="66b2c-112">PARAMETERS</span></span>

### <span data-ttu-id="66b2c-113">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="66b2c-113">-AutoScaleFormula</span></span>
<span data-ttu-id="66b2c-114">Specifica la formula per il numero desiderato di nodi compute nel pool.</span><span class="sxs-lookup"><span data-stu-id="66b2c-114">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66b2c-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="66b2c-115">-BatchContext</span></span>
<span data-ttu-id="66b2c-116">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="66b2c-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="66b2c-117">Se si usa il cmdlet Get-AzBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="66b2c-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="66b2c-118">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="66b2c-118">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="66b2c-119">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="66b2c-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="66b2c-120">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="66b2c-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="66b2c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66b2c-121">-DefaultProfile</span></span>
<span data-ttu-id="66b2c-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="66b2c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66b2c-123">-ID</span><span class="sxs-lookup"><span data-stu-id="66b2c-123">-Id</span></span>
<span data-ttu-id="66b2c-124">Specifica l'ID oggetto del pool per cui testare il ridimensionamento automatico.</span><span class="sxs-lookup"><span data-stu-id="66b2c-124">Specifies the object ID of the pool for which to test automatic scaling.</span></span>

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

### <span data-ttu-id="66b2c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66b2c-125">CommonParameters</span></span>
<span data-ttu-id="66b2c-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66b2c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66b2c-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66b2c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66b2c-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="66b2c-128">INPUTS</span></span>

### <span data-ttu-id="66b2c-129">System. String</span><span class="sxs-lookup"><span data-stu-id="66b2c-129">System.String</span></span>

### <span data-ttu-id="66b2c-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="66b2c-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="66b2c-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="66b2c-131">OUTPUTS</span></span>

### <span data-ttu-id="66b2c-132">Microsoft.Azure.Commands.Batch. Models. PSAutoScaleRun</span><span class="sxs-lookup"><span data-stu-id="66b2c-132">Microsoft.Azure.Commands.Batch.Models.PSAutoScaleRun</span></span>

## <span data-ttu-id="66b2c-133">Note</span><span class="sxs-lookup"><span data-stu-id="66b2c-133">NOTES</span></span>

## <span data-ttu-id="66b2c-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="66b2c-134">RELATED LINKS</span></span>

[<span data-ttu-id="66b2c-135">Disable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="66b2c-135">Disable-AzBatchAutoScale</span></span>](./Disable-AzBatchAutoScale.md)

[<span data-ttu-id="66b2c-136">Enable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="66b2c-136">Enable-AzBatchAutoScale</span></span>](./Enable-AzBatchAutoScale.md)

[<span data-ttu-id="66b2c-137">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="66b2c-137">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="66b2c-138">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="66b2c-138">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


