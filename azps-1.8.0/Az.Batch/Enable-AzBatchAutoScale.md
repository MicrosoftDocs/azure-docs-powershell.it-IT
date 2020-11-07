---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3107D061-7F25-45D0-8029-C99120A156DA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchAutoScale.md
ms.openlocfilehash: 72ba9a2d78ab343b44267c09a7c1524cab7278a9
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2020
ms.locfileid: "93685370"
---
# <span data-ttu-id="f55a8-101">Enable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="f55a8-101">Enable-AzBatchAutoScale</span></span>

## <span data-ttu-id="f55a8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f55a8-102">SYNOPSIS</span></span>
<span data-ttu-id="f55a8-103">Consente la scala automatica di un pool.</span><span class="sxs-lookup"><span data-stu-id="f55a8-103">Enables automatic scaling of a pool.</span></span>

## <span data-ttu-id="f55a8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f55a8-104">SYNTAX</span></span>

```
Enable-AzBatchAutoScale [-Id] <String> [[-AutoScaleFormula] <String>]
 [[-AutoScaleEvaluationInterval] <TimeSpan>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f55a8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f55a8-105">DESCRIPTION</span></span>
<span data-ttu-id="f55a8-106">Il cmdlet **Enable-AzBatchAutoScale** Abilita la scala automatica del pool specificato.</span><span class="sxs-lookup"><span data-stu-id="f55a8-106">The **Enable-AzBatchAutoScale** cmdlet enables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="f55a8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f55a8-107">EXAMPLES</span></span>

### <span data-ttu-id="f55a8-108">Esempio 1: abilitare la scala automatica per un pool</span><span class="sxs-lookup"><span data-stu-id="f55a8-108">Example 1: Enable automatic scaling for a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> Enable-AzBatchAutoScale -Id "MyPool" -AutoScaleFormula $Formula -BatchContext $Context
```

<span data-ttu-id="f55a8-109">Il primo comando definisce una formula e quindi la Salva nella variabile $Formula.</span><span class="sxs-lookup"><span data-stu-id="f55a8-109">The first command defines a formula, and then saves it to the $Formula variable.</span></span>
<span data-ttu-id="f55a8-110">Il secondo comando consente la scala automatica nel pool denominato pool usando la formula in $Formula.</span><span class="sxs-lookup"><span data-stu-id="f55a8-110">The second command enables automatic scaling on the pool named MyPool using the formula in $Formula.</span></span>

## <span data-ttu-id="f55a8-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f55a8-111">PARAMETERS</span></span>

### <span data-ttu-id="f55a8-112">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="f55a8-112">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="f55a8-113">Specifica la quantità di tempo (in minuti) che trascorre prima che le dimensioni del pool vengano regolate automaticamente in base alla formula di scala automatica.</span><span class="sxs-lookup"><span data-stu-id="f55a8-113">Specifies the amount of time (in minutes) that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="f55a8-114">Il valore predefinito è 15 minuti e il valore minimo è di 5 minuti.</span><span class="sxs-lookup"><span data-stu-id="f55a8-114">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="f55a8-115">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="f55a8-115">-AutoScaleFormula</span></span>
<span data-ttu-id="f55a8-116">Specifica la formula per il numero desiderato di nodi compute nel pool.</span><span class="sxs-lookup"><span data-stu-id="f55a8-116">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

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

### <span data-ttu-id="f55a8-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f55a8-117">-BatchContext</span></span>
<span data-ttu-id="f55a8-118">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="f55a8-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f55a8-119">Se si usa il cmdlet Get-AzBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="f55a8-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f55a8-120">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="f55a8-120">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f55a8-121">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="f55a8-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f55a8-122">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="f55a8-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f55a8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f55a8-123">-DefaultProfile</span></span>
<span data-ttu-id="f55a8-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f55a8-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f55a8-125">-ID</span><span class="sxs-lookup"><span data-stu-id="f55a8-125">-Id</span></span>
<span data-ttu-id="f55a8-126">Specifica l'ID oggetto del pool per cui abilitare il ridimensionamento automatico.</span><span class="sxs-lookup"><span data-stu-id="f55a8-126">Specifies the object ID of the pool for which to enable automatic scaling.</span></span>

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

### <span data-ttu-id="f55a8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f55a8-127">CommonParameters</span></span>
<span data-ttu-id="f55a8-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f55a8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f55a8-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f55a8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f55a8-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f55a8-130">INPUTS</span></span>

### <span data-ttu-id="f55a8-131">System. String</span><span class="sxs-lookup"><span data-stu-id="f55a8-131">System.String</span></span>

### <span data-ttu-id="f55a8-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f55a8-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="f55a8-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f55a8-133">OUTPUTS</span></span>

### <span data-ttu-id="f55a8-134">System. void</span><span class="sxs-lookup"><span data-stu-id="f55a8-134">System.Void</span></span>

## <span data-ttu-id="f55a8-135">Note</span><span class="sxs-lookup"><span data-stu-id="f55a8-135">NOTES</span></span>

## <span data-ttu-id="f55a8-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f55a8-136">RELATED LINKS</span></span>

[<span data-ttu-id="f55a8-137">Disable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="f55a8-137">Disable-AzBatchAutoScale</span></span>](./Disable-AzBatchAutoScale.md)

[<span data-ttu-id="f55a8-138">Test-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="f55a8-138">Test-AzBatchAutoScale</span></span>](./Test-AzBatchAutoScale.md)

[<span data-ttu-id="f55a8-139">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="f55a8-139">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


