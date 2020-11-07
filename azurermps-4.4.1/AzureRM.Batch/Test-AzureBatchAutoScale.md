---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: BF0C1A2F-2703-492F-A3A7-053416A5D1EB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Test-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Test-AzureBatchAutoScale.md
ms.openlocfilehash: 2ab8ca197c1d78980e1683f9572f6d3f6d4d55fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685536"
---
# <span data-ttu-id="ec15b-101">Test-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="ec15b-101">Test-AzureBatchAutoScale</span></span>

## <span data-ttu-id="ec15b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ec15b-102">SYNOPSIS</span></span>
<span data-ttu-id="ec15b-103">Ottiene il risultato di una formula di ridimensionamento automatico in un pool.</span><span class="sxs-lookup"><span data-stu-id="ec15b-103">Gets the result of an automatic scaling formula on a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec15b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ec15b-104">SYNTAX</span></span>

```
Test-AzureBatchAutoScale [-Id] <String> [-AutoScaleFormula] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec15b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ec15b-105">DESCRIPTION</span></span>
<span data-ttu-id="ec15b-106">Il cmdlet **test-AzureBatchAutoScale** ottiene il risultato di una formula di ridimensionamento automatico nel pool specificato.</span><span class="sxs-lookup"><span data-stu-id="ec15b-106">The **Test-AzureBatchAutoScale** cmdlet gets the result of an automatic scaling formula on the specified pool.</span></span>

## <span data-ttu-id="ec15b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ec15b-107">EXAMPLES</span></span>

### <span data-ttu-id="ec15b-108">Esempio 1: valutare una formula di scalabilità verticale in un pool</span><span class="sxs-lookup"><span data-stu-id="ec15b-108">Example 1: Evaluate an autoscale formula on a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> $Evaluation = Test-AzureBatchAutoScale -Id "ContosoPool" -AutoScaleFormula $Formula -BatchContext $Context
PS C:\> $Evaluation.AutoScaleRun.Results
$TargetDedicated=5;$NodeDeallocationOption=requeue;totalNodes=5
```

<span data-ttu-id="ec15b-109">Il primo comando Archivia una formula nella variabile $Formula per l'uso nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="ec15b-109">The first command stores a formula in the $Formula variable for use in the example.</span></span>

<span data-ttu-id="ec15b-110">Il secondo comando valuta la formula di scalabilità verticale nel pool che contiene l'ID ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="ec15b-110">The second command evaluates the autoscale formula on the pool that has the ID ContosoPool.</span></span>

<span data-ttu-id="ec15b-111">Il comando finale Visualizza i **risultati** usando la sintassi del punto standard.</span><span class="sxs-lookup"><span data-stu-id="ec15b-111">The final command displays the **Results** by using standard dot syntax.</span></span>

## <span data-ttu-id="ec15b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ec15b-112">PARAMETERS</span></span>

### <span data-ttu-id="ec15b-113">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="ec15b-113">-AutoScaleFormula</span></span>
<span data-ttu-id="ec15b-114">Specifica la formula per il numero desiderato di nodi compute nel pool.</span><span class="sxs-lookup"><span data-stu-id="ec15b-114">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

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

### <span data-ttu-id="ec15b-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ec15b-115">-BatchContext</span></span>
<span data-ttu-id="ec15b-116">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="ec15b-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ec15b-117">Per ottenere un oggetto **BatchAccountContext** che contiene i tasti di scelta per l'abbonamento, usare il cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="ec15b-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="ec15b-118">-ID</span><span class="sxs-lookup"><span data-stu-id="ec15b-118">-Id</span></span>
<span data-ttu-id="ec15b-119">Specifica l'ID oggetto del pool per cui testare il ridimensionamento automatico.</span><span class="sxs-lookup"><span data-stu-id="ec15b-119">Specifies the object ID of the pool for which to test automatic scaling.</span></span>

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

### <span data-ttu-id="ec15b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec15b-120">-DefaultProfile</span></span>
<span data-ttu-id="ec15b-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ec15b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec15b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec15b-122">CommonParameters</span></span>
<span data-ttu-id="ec15b-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec15b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec15b-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec15b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec15b-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ec15b-125">INPUTS</span></span>

### <span data-ttu-id="ec15b-126">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ec15b-126">BatchAccountContext</span></span>
<span data-ttu-id="ec15b-127">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="ec15b-127">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="ec15b-128">Stringa</span><span class="sxs-lookup"><span data-stu-id="ec15b-128">String</span></span>
<span data-ttu-id="ec15b-129">Il parametro "ID" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="ec15b-129">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="ec15b-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ec15b-130">OUTPUTS</span></span>

### <span data-ttu-id="ec15b-131">PSAutoScaleEvaluation</span><span class="sxs-lookup"><span data-stu-id="ec15b-131">PSAutoScaleEvaluation</span></span>

## <span data-ttu-id="ec15b-132">Note</span><span class="sxs-lookup"><span data-stu-id="ec15b-132">NOTES</span></span>

## <span data-ttu-id="ec15b-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ec15b-133">RELATED LINKS</span></span>

[<span data-ttu-id="ec15b-134">Disable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="ec15b-134">Disable-AzureBatchAutoScale</span></span>](./Disable-AzureBatchAutoScale.md)

[<span data-ttu-id="ec15b-135">Enable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="ec15b-135">Enable-AzureBatchAutoScale</span></span>](./Enable-AzureBatchAutoScale.md)

[<span data-ttu-id="ec15b-136">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="ec15b-136">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="ec15b-137">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="ec15b-137">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


