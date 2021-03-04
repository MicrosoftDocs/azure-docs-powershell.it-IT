---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: BF0C1A2F-2703-492F-A3A7-053416A5D1EB
online version: https://docs.microsoft.com/powershell/module/az.batch/test-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Test-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Test-AzBatchAutoScale.md
ms.openlocfilehash: a048e7bd2a013bd5d8526feead3b38483a1f61b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959805"
---
# <span data-ttu-id="9f112-101">Test-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="9f112-101">Test-AzBatchAutoScale</span></span>

## <span data-ttu-id="9f112-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f112-102">SYNOPSIS</span></span>
<span data-ttu-id="9f112-103">Ottiene il risultato di una formula di ridimensionamento automatico in un pool.</span><span class="sxs-lookup"><span data-stu-id="9f112-103">Gets the result of an automatic scaling formula on a pool.</span></span>

## <span data-ttu-id="9f112-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9f112-104">SYNTAX</span></span>

```
Test-AzBatchAutoScale [-Id] <String> [-AutoScaleFormula] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f112-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9f112-105">DESCRIPTION</span></span>
<span data-ttu-id="9f112-106">Il **cmdlet Test-AzBatchAutoScale** ottiene il risultato di una formula di ridimensionamento automatico nel pool specificato.</span><span class="sxs-lookup"><span data-stu-id="9f112-106">The **Test-AzBatchAutoScale** cmdlet gets the result of an automatic scaling formula on the specified pool.</span></span>

## <span data-ttu-id="9f112-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9f112-107">EXAMPLES</span></span>

### <span data-ttu-id="9f112-108">Esempio 1: Valutare una formula di scala automatica in un pool</span><span class="sxs-lookup"><span data-stu-id="9f112-108">Example 1: Evaluate an autoscale formula on a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> $Evaluation = Test-AzBatchAutoScale -Id "ContosoPool" -AutoScaleFormula $Formula -BatchContext $Context
PS C:\> $Evaluation.AutoScaleRun.Results
$TargetDedicated=5;$NodeDeallocationOption=requeue;totalNodes=5
```

<span data-ttu-id="9f112-109">Il primo comando archivia una formula nella $Formula variabile da usare nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="9f112-109">The first command stores a formula in the $Formula variable for use in the example.</span></span>
<span data-ttu-id="9f112-110">Il secondo comando valuta la formula di scala automatica nel pool che contiene l'ID ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="9f112-110">The second command evaluates the autoscale formula on the pool that has the ID ContosoPool.</span></span>
<span data-ttu-id="9f112-111">Il comando finale visualizza i **risultati usando la sintassi** standard del punto.</span><span class="sxs-lookup"><span data-stu-id="9f112-111">The final command displays the **Results** by using standard dot syntax.</span></span>

## <span data-ttu-id="9f112-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f112-112">PARAMETERS</span></span>

### <span data-ttu-id="9f112-113">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="9f112-113">-AutoScaleFormula</span></span>
<span data-ttu-id="9f112-114">Specifica la formula per il numero desiderato di nodi di calcolo nel pool.</span><span class="sxs-lookup"><span data-stu-id="9f112-114">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

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

### <span data-ttu-id="9f112-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="9f112-115">-BatchContext</span></span>
<span data-ttu-id="9f112-116">Specifica **l'istanza BatchAccountContext** che questo cmdlet usa per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="9f112-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="9f112-117">Se si usa il cmdlet Get-AzBatchAccount per ottenere BatchAccountContext, verrà usata l'autenticazione di Azure Active Directory quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="9f112-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="9f112-118">Per usare invece l'autenticazione della chiave condivisa, usare il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con le relative chiavi di accesso popolate.</span><span class="sxs-lookup"><span data-stu-id="9f112-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="9f112-119">Quando si usa l'autenticazione con chiave condivisa, per impostazione predefinita viene usata la chiave di accesso primario.</span><span class="sxs-lookup"><span data-stu-id="9f112-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="9f112-120">Per modificare la chiave da usare, impostare la proprietà BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="9f112-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="9f112-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f112-121">-DefaultProfile</span></span>
<span data-ttu-id="9f112-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9f112-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f112-123">-Id</span><span class="sxs-lookup"><span data-stu-id="9f112-123">-Id</span></span>
<span data-ttu-id="9f112-124">Specifica l'ID oggetto del pool di cui verificare le proporzioni automatiche.</span><span class="sxs-lookup"><span data-stu-id="9f112-124">Specifies the object ID of the pool for which to test automatic scaling.</span></span>

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

### <span data-ttu-id="9f112-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f112-125">CommonParameters</span></span>
<span data-ttu-id="9f112-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f112-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f112-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9f112-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f112-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="9f112-128">INPUTS</span></span>

### <span data-ttu-id="9f112-129">System.String</span><span class="sxs-lookup"><span data-stu-id="9f112-129">System.String</span></span>

### <span data-ttu-id="9f112-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="9f112-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="9f112-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9f112-131">OUTPUTS</span></span>

### <span data-ttu-id="9f112-132">Microsoft.Azure.Commands.Batch. Models.PSAutoScaleRun</span><span class="sxs-lookup"><span data-stu-id="9f112-132">Microsoft.Azure.Commands.Batch.Models.PSAutoScaleRun</span></span>

## <span data-ttu-id="9f112-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="9f112-133">NOTES</span></span>

## <span data-ttu-id="9f112-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9f112-134">RELATED LINKS</span></span>

[<span data-ttu-id="9f112-135">Disable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="9f112-135">Disable-AzBatchAutoScale</span></span>](./Disable-AzBatchAutoScale.md)

[<span data-ttu-id="9f112-136">Enable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="9f112-136">Enable-AzBatchAutoScale</span></span>](./Enable-AzBatchAutoScale.md)

[<span data-ttu-id="9f112-137">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="9f112-137">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="9f112-138">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="9f112-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
