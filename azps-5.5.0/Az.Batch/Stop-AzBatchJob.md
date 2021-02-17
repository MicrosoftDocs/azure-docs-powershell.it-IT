---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 975B707C-5001-43ED-81AB-9BB6665135BA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJob.md
ms.openlocfilehash: ffaac0bdd4a144cc3979da052c0c40cb824862f4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205179"
---
# <span data-ttu-id="a4240-101">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a4240-101">Stop-AzBatchJob</span></span>

## <span data-ttu-id="a4240-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4240-102">SYNOPSIS</span></span>
<span data-ttu-id="a4240-103">Interrompe un processo batch.</span><span class="sxs-lookup"><span data-stu-id="a4240-103">Stops a Batch job.</span></span>

## <span data-ttu-id="a4240-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a4240-104">SYNTAX</span></span>

```
Stop-AzBatchJob [-Id] <String> [[-TerminateReason] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4240-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a4240-105">DESCRIPTION</span></span>
<span data-ttu-id="a4240-106">Il cmdlet **Stop-AzBatchJob** interrompe un processo batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="a4240-106">The **Stop-AzBatchJob** cmdlet stops an Azure Batch job.</span></span>
<span data-ttu-id="a4240-107">Questo comando contrassegna il processo come completato.</span><span class="sxs-lookup"><span data-stu-id="a4240-107">This command marks the job as completed.</span></span>

## <span data-ttu-id="a4240-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a4240-108">EXAMPLES</span></span>

### <span data-ttu-id="a4240-109">Esempio 1: Interrompere un processo batch</span><span class="sxs-lookup"><span data-stu-id="a4240-109">Example 1: Stop a Batch job</span></span>
```
PS C:\>Stop-AzBatchJob -Id "Job-000001" -TerminateReason "No more tasks to run" -BatchContext $Context
```

<span data-ttu-id="a4240-110">Questo comando interrompe il processo con ID Processo-000001.</span><span class="sxs-lookup"><span data-stu-id="a4240-110">This command stops the job that has the ID Job-000001.</span></span>
<span data-ttu-id="a4240-111">Il comando specifica un motivo per cui si è scelto di interrompere il processo.</span><span class="sxs-lookup"><span data-stu-id="a4240-111">The command specifies a reason that you chose to stop the job.</span></span>
<span data-ttu-id="a4240-112">Usare il cmdlet Get-AzBatchAccountKey per assegnare un contesto alla $Context variabile.</span><span class="sxs-lookup"><span data-stu-id="a4240-112">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="a4240-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4240-113">PARAMETERS</span></span>

### <span data-ttu-id="a4240-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a4240-114">-BatchContext</span></span>
<span data-ttu-id="a4240-115">Specifica **l'istanza BatchAccountContext** che questo cmdlet usa per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="a4240-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a4240-116">Se si usa il cmdlet Get-AzBatchAccount per ottenere BatchAccountContext, verrà usata l'autenticazione di Azure Active Directory quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="a4240-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a4240-117">Per usare invece l'autenticazione della chiave condivisa, usare il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con le relative chiavi di accesso popolate.</span><span class="sxs-lookup"><span data-stu-id="a4240-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a4240-118">Quando si usa l'autenticazione con chiave condivisa, per impostazione predefinita viene usata la chiave di accesso primario.</span><span class="sxs-lookup"><span data-stu-id="a4240-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a4240-119">Per modificare la chiave da usare, impostare la proprietà BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="a4240-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a4240-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4240-120">-DefaultProfile</span></span>
<span data-ttu-id="a4240-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a4240-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4240-122">-Id</span><span class="sxs-lookup"><span data-stu-id="a4240-122">-Id</span></span>
<span data-ttu-id="a4240-123">Specifica l'ID del processo interrotto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4240-123">Specifies the ID of the job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="a4240-124">-Terminate Terminate Unidirezione</span><span class="sxs-lookup"><span data-stu-id="a4240-124">-TerminateReason</span></span>
<span data-ttu-id="a4240-125">Specifica il motivo per cui si è deciso di interrompere il processo.</span><span class="sxs-lookup"><span data-stu-id="a4240-125">Specifies the reason that you decided to stop the job.</span></span>
<span data-ttu-id="a4240-126">Questo cmdlet archivia questo testo come **proprietà Terminate Rtf** del processo.</span><span class="sxs-lookup"><span data-stu-id="a4240-126">This cmdlet stores this text as the **TerminateReason** property of the job.</span></span>

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

### <span data-ttu-id="a4240-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4240-127">CommonParameters</span></span>
<span data-ttu-id="a4240-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4240-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4240-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a4240-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4240-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="a4240-130">INPUTS</span></span>

### <span data-ttu-id="a4240-131">System.String</span><span class="sxs-lookup"><span data-stu-id="a4240-131">System.String</span></span>

### <span data-ttu-id="a4240-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a4240-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="a4240-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a4240-133">OUTPUTS</span></span>

### <span data-ttu-id="a4240-134">System.Void</span><span class="sxs-lookup"><span data-stu-id="a4240-134">System.Void</span></span>

## <span data-ttu-id="a4240-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="a4240-135">NOTES</span></span>

## <span data-ttu-id="a4240-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a4240-136">RELATED LINKS</span></span>

[<span data-ttu-id="a4240-137">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a4240-137">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="a4240-138">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a4240-138">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="a4240-139">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="a4240-139">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="a4240-140">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a4240-140">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="a4240-141">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a4240-141">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="a4240-142">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a4240-142">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="a4240-143">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="a4240-143">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
