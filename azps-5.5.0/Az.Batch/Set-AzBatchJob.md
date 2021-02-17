---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 75483BC7-440A-437B-9EDE-D270D87CF3C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
ms.openlocfilehash: 1104eed4d60405226cdc6dad351ae418b84142e2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210170"
---
# <span data-ttu-id="50b9f-101">Set-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="50b9f-101">Set-AzBatchJob</span></span>

## <span data-ttu-id="50b9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50b9f-102">SYNOPSIS</span></span>
<span data-ttu-id="50b9f-103">Aggiorna un processo batch.</span><span class="sxs-lookup"><span data-stu-id="50b9f-103">Updates a Batch job.</span></span>

## <span data-ttu-id="50b9f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="50b9f-104">SYNTAX</span></span>

```
Set-AzBatchJob [-Job] <PSCloudJob> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50b9f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="50b9f-105">DESCRIPTION</span></span>
<span data-ttu-id="50b9f-106">Il **cmdlet Set-AzBatchJob** aggiorna un processo batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="50b9f-106">The **Set-AzBatchJob** cmdlet updates an Azure Batch job.</span></span>
<span data-ttu-id="50b9f-107">Usare il cmdlet Get-AzBatchJob per ottenere un **oggetto PSCloudJob.**</span><span class="sxs-lookup"><span data-stu-id="50b9f-107">Use the Get-AzBatchJob cmdlet to get a **PSCloudJob** object.</span></span>
<span data-ttu-id="50b9f-108">Modificare le proprietà dell'oggetto e quindi usare il cmdlet corrente per eseguire il commit delle modifiche al servizio batch.</span><span class="sxs-lookup"><span data-stu-id="50b9f-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="50b9f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="50b9f-109">EXAMPLES</span></span>

### <span data-ttu-id="50b9f-110">Esempio 1: Aggiornare un processo</span><span class="sxs-lookup"><span data-stu-id="50b9f-110">Example 1: Update a job</span></span>
```
PS C:\>$Job = Get-AzBatchJob -Id "Job17" -BatchContext $Context
PS C:\> $Job.Priority = 1
PS C:\> Set-AzBatchJob -Job $Job -BatchContext $Context
```

<span data-ttu-id="50b9f-111">Il primo comando ottiene un processo con **Get-AzBatchJob** e quindi lo archivia nella $Job variabile.</span><span class="sxs-lookup"><span data-stu-id="50b9f-111">The first command gets a job by using **Get-AzBatchJob**, and then stores it in the $Job variable.</span></span>
<span data-ttu-id="50b9f-112">Il secondo comando modifica la specifica della priorità per l$Job o object.</span><span class="sxs-lookup"><span data-stu-id="50b9f-112">The second command modifies the priority specification on the $Job object.</span></span>
<span data-ttu-id="50b9f-113">Il comando finale aggiorna il servizio batch in modo che corrisponda all'oggetto locale in $Job.</span><span class="sxs-lookup"><span data-stu-id="50b9f-113">The final command updates the Batch service to match the local object in $Job.</span></span>

## <span data-ttu-id="50b9f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50b9f-114">PARAMETERS</span></span>

### <span data-ttu-id="50b9f-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="50b9f-115">-BatchContext</span></span>
<span data-ttu-id="50b9f-116">Specifica **l'istanza BatchAccountContext** che questo cmdlet usa per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="50b9f-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="50b9f-117">Se si usa il cmdlet Get-AzBatchAccount per ottenere BatchAccountContext, verrà usata l'autenticazione di Azure Active Directory quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="50b9f-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="50b9f-118">Per usare invece l'autenticazione della chiave condivisa, usare il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con le relative chiavi di accesso popolate.</span><span class="sxs-lookup"><span data-stu-id="50b9f-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="50b9f-119">Quando si usa l'autenticazione con chiave condivisa, per impostazione predefinita viene usata la chiave di accesso primario.</span><span class="sxs-lookup"><span data-stu-id="50b9f-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="50b9f-120">Per modificare la chiave da usare, impostare la proprietà BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="50b9f-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="50b9f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50b9f-121">-DefaultProfile</span></span>
<span data-ttu-id="50b9f-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="50b9f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50b9f-123">-Job</span><span class="sxs-lookup"><span data-stu-id="50b9f-123">-Job</span></span>
<span data-ttu-id="50b9f-124">Specifica un **psCloudJob** a cui questo cmdlet aggiorna il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="50b9f-124">Specifies a **PSCloudJob** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50b9f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50b9f-125">CommonParameters</span></span>
<span data-ttu-id="50b9f-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50b9f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50b9f-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="50b9f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50b9f-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="50b9f-128">INPUTS</span></span>

### <span data-ttu-id="50b9f-129">Microsoft.Azure.Commands.Batch. Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="50b9f-129">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="50b9f-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="50b9f-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="50b9f-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="50b9f-131">OUTPUTS</span></span>

### <span data-ttu-id="50b9f-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="50b9f-132">System.Void</span></span>

## <span data-ttu-id="50b9f-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="50b9f-133">NOTES</span></span>

## <span data-ttu-id="50b9f-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="50b9f-134">RELATED LINKS</span></span>

[<span data-ttu-id="50b9f-135">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="50b9f-135">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="50b9f-136">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="50b9f-136">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="50b9f-137">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="50b9f-137">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="50b9f-138">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="50b9f-138">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="50b9f-139">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="50b9f-139">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="50b9f-140">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="50b9f-140">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="50b9f-141">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="50b9f-141">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="50b9f-142">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="50b9f-142">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
