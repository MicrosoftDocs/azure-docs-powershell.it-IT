---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3107D061-7F25-45D0-8029-C99120A156DA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchAutoScale.md
ms.openlocfilehash: 1a85ac52622bb752b2e3437eb096f229c4d8e762
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521794"
---
# <span data-ttu-id="c4776-101">Enable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="c4776-101">Enable-AzureBatchAutoScale</span></span>

## <span data-ttu-id="c4776-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c4776-102">SYNOPSIS</span></span>
<span data-ttu-id="c4776-103">Consente la scala automatica di un pool.</span><span class="sxs-lookup"><span data-stu-id="c4776-103">Enables automatic scaling of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4776-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c4776-104">SYNTAX</span></span>

```
Enable-AzureBatchAutoScale [-Id] <String> [[-AutoScaleFormula] <String>]
 [[-AutoScaleEvaluationInterval] <TimeSpan>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4776-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c4776-105">DESCRIPTION</span></span>
<span data-ttu-id="c4776-106">Il cmdlet **Enable-AzureBatchAutoScale** Abilita la scala automatica del pool specificato.</span><span class="sxs-lookup"><span data-stu-id="c4776-106">The **Enable-AzureBatchAutoScale** cmdlet enables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="c4776-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c4776-107">EXAMPLES</span></span>

### <span data-ttu-id="c4776-108">Esempio 1: abilitare la scala automatica per un pool</span><span class="sxs-lookup"><span data-stu-id="c4776-108">Example 1: Enable automatic scaling for a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> Enable-AzureBatchAutoScale -Id "MyPool" -AutoScaleFormula $Formula -BatchContext $Context
```

<span data-ttu-id="c4776-109">Il primo comando definisce una formula e quindi la Salva nella variabile $Formula.</span><span class="sxs-lookup"><span data-stu-id="c4776-109">The first command defines a formula, and then saves it to the $Formula variable.</span></span>

<span data-ttu-id="c4776-110">Il secondo comando consente la scala automatica nel pool denominato pool usando la formula in $Formula.</span><span class="sxs-lookup"><span data-stu-id="c4776-110">The second command enables automatic scaling on the pool named MyPool using the formula in $Formula.</span></span>

## <span data-ttu-id="c4776-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c4776-111">PARAMETERS</span></span>

### <span data-ttu-id="c4776-112">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="c4776-112">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="c4776-113">Specifica la quantità di tempo (in minuti) che trascorre prima che le dimensioni del pool vengano regolate automaticamente in base alla formula di scala automatica.</span><span class="sxs-lookup"><span data-stu-id="c4776-113">Specifies the amount of time (in minutes) that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="c4776-114">Il valore predefinito è 15 minuti e il valore minimo è di 5 minuti.</span><span class="sxs-lookup"><span data-stu-id="c4776-114">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4776-115">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="c4776-115">-AutoScaleFormula</span></span>
<span data-ttu-id="c4776-116">Specifica la formula per il numero desiderato di nodi compute nel pool.</span><span class="sxs-lookup"><span data-stu-id="c4776-116">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4776-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c4776-117">-BatchContext</span></span>
<span data-ttu-id="c4776-118">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="c4776-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c4776-119">Per ottenere un oggetto **BatchAccountContext** che contiene i tasti di scelta per l'abbonamento, usare il cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="c4776-119">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="c4776-120">-ID</span><span class="sxs-lookup"><span data-stu-id="c4776-120">-Id</span></span>
<span data-ttu-id="c4776-121">Specifica l'ID oggetto del pool per cui abilitare il ridimensionamento automatico.</span><span class="sxs-lookup"><span data-stu-id="c4776-121">Specifies the object ID of the pool for which to enable automatic scaling.</span></span>

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

### <span data-ttu-id="c4776-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4776-122">-DefaultProfile</span></span>
<span data-ttu-id="c4776-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c4776-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4776-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4776-124">CommonParameters</span></span>
<span data-ttu-id="c4776-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4776-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4776-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4776-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4776-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c4776-127">INPUTS</span></span>

### <span data-ttu-id="c4776-128">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c4776-128">BatchAccountContext</span></span>
<span data-ttu-id="c4776-129">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="c4776-129">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="c4776-130">Stringa</span><span class="sxs-lookup"><span data-stu-id="c4776-130">String</span></span>
<span data-ttu-id="c4776-131">Il parametro "ID" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="c4776-131">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="c4776-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c4776-132">OUTPUTS</span></span>

## <span data-ttu-id="c4776-133">Note</span><span class="sxs-lookup"><span data-stu-id="c4776-133">NOTES</span></span>

## <span data-ttu-id="c4776-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c4776-134">RELATED LINKS</span></span>

[<span data-ttu-id="c4776-135">Disable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="c4776-135">Disable-AzureBatchAutoScale</span></span>](./Disable-AzureBatchAutoScale.md)

[<span data-ttu-id="c4776-136">Test-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="c4776-136">Test-AzureBatchAutoScale</span></span>](./Test-AzureBatchAutoScale.md)

[<span data-ttu-id="c4776-137">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="c4776-137">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


