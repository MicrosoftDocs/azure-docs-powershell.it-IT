---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: BF0C1A2F-2703-492F-A3A7-053416A5D1EB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/test-azurebatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Test-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Test-AzureBatchAutoScale.md
ms.openlocfilehash: 4258c5d83b15c2cecb6e2cd4e3edc216efec7a97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508384"
---
# <span data-ttu-id="1bb13-101">Test-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="1bb13-101">Test-AzureBatchAutoScale</span></span>

## <span data-ttu-id="1bb13-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1bb13-102">SYNOPSIS</span></span>
<span data-ttu-id="1bb13-103">Ottiene il risultato di una formula di ridimensionamento automatico in un pool.</span><span class="sxs-lookup"><span data-stu-id="1bb13-103">Gets the result of an automatic scaling formula on a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1bb13-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1bb13-104">SYNTAX</span></span>

```
Test-AzureBatchAutoScale [-Id] <String> [-AutoScaleFormula] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1bb13-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1bb13-105">DESCRIPTION</span></span>
<span data-ttu-id="1bb13-106">Il cmdlet **test-AzureBatchAutoScale** ottiene il risultato di una formula di ridimensionamento automatico nel pool specificato.</span><span class="sxs-lookup"><span data-stu-id="1bb13-106">The **Test-AzureBatchAutoScale** cmdlet gets the result of an automatic scaling formula on the specified pool.</span></span>

## <span data-ttu-id="1bb13-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1bb13-107">EXAMPLES</span></span>

### <span data-ttu-id="1bb13-108">Esempio 1: valutare una formula di scalabilità verticale in un pool</span><span class="sxs-lookup"><span data-stu-id="1bb13-108">Example 1: Evaluate an autoscale formula on a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> $Evaluation = Test-AzureBatchAutoScale -Id "ContosoPool" -AutoScaleFormula $Formula -BatchContext $Context
PS C:\> $Evaluation.AutoScaleRun.Results
$TargetDedicated=5;$NodeDeallocationOption=requeue;totalNodes=5
```

<span data-ttu-id="1bb13-109">Il primo comando Archivia una formula nella variabile $Formula per l'uso nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="1bb13-109">The first command stores a formula in the $Formula variable for use in the example.</span></span>

<span data-ttu-id="1bb13-110">Il secondo comando valuta la formula di scalabilità verticale nel pool che contiene l'ID ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="1bb13-110">The second command evaluates the autoscale formula on the pool that has the ID ContosoPool.</span></span>

<span data-ttu-id="1bb13-111">Il comando finale Visualizza i **risultati** usando la sintassi del punto standard.</span><span class="sxs-lookup"><span data-stu-id="1bb13-111">The final command displays the **Results** by using standard dot syntax.</span></span>

## <span data-ttu-id="1bb13-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1bb13-112">PARAMETERS</span></span>

### <span data-ttu-id="1bb13-113">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="1bb13-113">-AutoScaleFormula</span></span>
<span data-ttu-id="1bb13-114">Specifica la formula per il numero desiderato di nodi compute nel pool.</span><span class="sxs-lookup"><span data-stu-id="1bb13-114">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bb13-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="1bb13-115">-BatchContext</span></span>
<span data-ttu-id="1bb13-116">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="1bb13-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="1bb13-117">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="1bb13-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="1bb13-118">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="1bb13-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="1bb13-119">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="1bb13-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="1bb13-120">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="1bb13-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="1bb13-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bb13-121">-DefaultProfile</span></span>
<span data-ttu-id="1bb13-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1bb13-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1bb13-123">-ID</span><span class="sxs-lookup"><span data-stu-id="1bb13-123">-Id</span></span>
<span data-ttu-id="1bb13-124">Specifica l'ID oggetto del pool per cui testare il ridimensionamento automatico.</span><span class="sxs-lookup"><span data-stu-id="1bb13-124">Specifies the object ID of the pool for which to test automatic scaling.</span></span>

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

### <span data-ttu-id="1bb13-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bb13-125">CommonParameters</span></span>
<span data-ttu-id="1bb13-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bb13-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bb13-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bb13-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bb13-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1bb13-128">INPUTS</span></span>

### <span data-ttu-id="1bb13-129">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="1bb13-129">BatchAccountContext</span></span>
<span data-ttu-id="1bb13-130">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="1bb13-130">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="1bb13-131">Stringa</span><span class="sxs-lookup"><span data-stu-id="1bb13-131">String</span></span>
<span data-ttu-id="1bb13-132">Il parametro "ID" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="1bb13-132">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="1bb13-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1bb13-133">OUTPUTS</span></span>

### <span data-ttu-id="1bb13-134">PSAutoScaleEvaluation</span><span class="sxs-lookup"><span data-stu-id="1bb13-134">PSAutoScaleEvaluation</span></span>

## <span data-ttu-id="1bb13-135">Note</span><span class="sxs-lookup"><span data-stu-id="1bb13-135">NOTES</span></span>

## <span data-ttu-id="1bb13-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1bb13-136">RELATED LINKS</span></span>

[<span data-ttu-id="1bb13-137">Disable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="1bb13-137">Disable-AzureBatchAutoScale</span></span>](./Disable-AzureBatchAutoScale.md)

[<span data-ttu-id="1bb13-138">Enable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="1bb13-138">Enable-AzureBatchAutoScale</span></span>](./Enable-AzureBatchAutoScale.md)

[<span data-ttu-id="1bb13-139">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="1bb13-139">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="1bb13-140">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="1bb13-140">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


