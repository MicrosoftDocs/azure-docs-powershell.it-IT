---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3107D061-7F25-45D0-8029-C99120A156DA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchAutoScale.md
ms.openlocfilehash: 73e7e9e0e4020f284b26e720e0f34ec7f11fd04f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205386"
---
# <span data-ttu-id="65a07-101">Enable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="65a07-101">Enable-AzBatchAutoScale</span></span>

## <span data-ttu-id="65a07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65a07-102">SYNOPSIS</span></span>
<span data-ttu-id="65a07-103">Abilita il ridimensionamento automatico di una pool.</span><span class="sxs-lookup"><span data-stu-id="65a07-103">Enables automatic scaling of a pool.</span></span>

## <span data-ttu-id="65a07-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="65a07-104">SYNTAX</span></span>

```
Enable-AzBatchAutoScale [-Id] <String> [[-AutoScaleFormula] <String>]
 [[-AutoScaleEvaluationInterval] <TimeSpan>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65a07-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="65a07-105">DESCRIPTION</span></span>
<span data-ttu-id="65a07-106">Il cmdlet **Enable-AzBatchAutoScale** abilita il ridimensionamento automatico del pool specificato.</span><span class="sxs-lookup"><span data-stu-id="65a07-106">The **Enable-AzBatchAutoScale** cmdlet enables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="65a07-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="65a07-107">EXAMPLES</span></span>

### <span data-ttu-id="65a07-108">Esempio 1: Abilitare il ridimensionamento automatico per un pool</span><span class="sxs-lookup"><span data-stu-id="65a07-108">Example 1: Enable automatic scaling for a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> Enable-AzBatchAutoScale -Id "MyPool" -AutoScaleFormula $Formula -BatchContext $Context
```

<span data-ttu-id="65a07-109">Il primo comando definisce una formula e quindi la salva nella $Formula variabile.</span><span class="sxs-lookup"><span data-stu-id="65a07-109">The first command defines a formula, and then saves it to the $Formula variable.</span></span>
<span data-ttu-id="65a07-110">Il secondo comando abilita il ridimensionamento automatico nel pool denominato MyPool usando la formula in $Formula.</span><span class="sxs-lookup"><span data-stu-id="65a07-110">The second command enables automatic scaling on the pool named MyPool using the formula in $Formula.</span></span>

## <span data-ttu-id="65a07-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65a07-111">PARAMETERS</span></span>

### <span data-ttu-id="65a07-112">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="65a07-112">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="65a07-113">Specifica la quantità di tempo (in minuti) che deve trascorrere prima che le dimensioni del pool vengono regolate automaticamente in base alla formula Di scala automatica.</span><span class="sxs-lookup"><span data-stu-id="65a07-113">Specifies the amount of time (in minutes) that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="65a07-114">Il valore predefinito è 15 minuti e il valore minimo è 5 minuti.</span><span class="sxs-lookup"><span data-stu-id="65a07-114">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="65a07-115">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="65a07-115">-AutoScaleFormula</span></span>
<span data-ttu-id="65a07-116">Specifica la formula per il numero desiderato di nodi di calcolo nel pool.</span><span class="sxs-lookup"><span data-stu-id="65a07-116">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

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

### <span data-ttu-id="65a07-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="65a07-117">-BatchContext</span></span>
<span data-ttu-id="65a07-118">Specifica **l'istanza BatchAccountContext** che questo cmdlet usa per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="65a07-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="65a07-119">Se si usa il cmdlet Get-AzBatchAccount per ottenere BatchAccountContext, verrà usata l'autenticazione di Azure Active Directory quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="65a07-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="65a07-120">Per usare invece l'autenticazione della chiave condivisa, usare il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con le relative chiavi di accesso popolate.</span><span class="sxs-lookup"><span data-stu-id="65a07-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="65a07-121">Quando si usa l'autenticazione con chiave condivisa, per impostazione predefinita viene usata la chiave di accesso primario.</span><span class="sxs-lookup"><span data-stu-id="65a07-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="65a07-122">Per modificare la chiave da usare, impostare la proprietà BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="65a07-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="65a07-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65a07-123">-DefaultProfile</span></span>
<span data-ttu-id="65a07-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="65a07-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65a07-125">-Id</span><span class="sxs-lookup"><span data-stu-id="65a07-125">-Id</span></span>
<span data-ttu-id="65a07-126">Specifica l'ID oggetto del pool per cui abilitare il ridimensionamento automatico.</span><span class="sxs-lookup"><span data-stu-id="65a07-126">Specifies the object ID of the pool for which to enable automatic scaling.</span></span>

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

### <span data-ttu-id="65a07-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65a07-127">CommonParameters</span></span>
<span data-ttu-id="65a07-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65a07-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65a07-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="65a07-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65a07-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="65a07-130">INPUTS</span></span>

### <span data-ttu-id="65a07-131">System.String</span><span class="sxs-lookup"><span data-stu-id="65a07-131">System.String</span></span>

### <span data-ttu-id="65a07-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="65a07-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="65a07-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="65a07-133">OUTPUTS</span></span>

### <span data-ttu-id="65a07-134">System.Void</span><span class="sxs-lookup"><span data-stu-id="65a07-134">System.Void</span></span>

## <span data-ttu-id="65a07-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="65a07-135">NOTES</span></span>

## <span data-ttu-id="65a07-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="65a07-136">RELATED LINKS</span></span>

[<span data-ttu-id="65a07-137">Disable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="65a07-137">Disable-AzBatchAutoScale</span></span>](./Disable-AzBatchAutoScale.md)

[<span data-ttu-id="65a07-138">Test-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="65a07-138">Test-AzBatchAutoScale</span></span>](./Test-AzBatchAutoScale.md)

[<span data-ttu-id="65a07-139">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="65a07-139">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
