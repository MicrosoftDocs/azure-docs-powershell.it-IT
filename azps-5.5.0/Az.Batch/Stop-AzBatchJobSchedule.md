---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D1C5B35C-5419-4739-9D57-6C4228E98DAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
ms.openlocfilehash: b236f163a6c5c849fcbfcea0a19dac955e15c798
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195222"
---
# <span data-ttu-id="e2be8-101">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e2be8-101">Stop-AzBatchJobSchedule</span></span>

## <span data-ttu-id="e2be8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2be8-102">SYNOPSIS</span></span>
<span data-ttu-id="e2be8-103">Interrompe la pianificazione di un processo batch.</span><span class="sxs-lookup"><span data-stu-id="e2be8-103">Stops a Batch job schedule.</span></span>

## <span data-ttu-id="e2be8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e2be8-104">SYNTAX</span></span>

```
Stop-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2be8-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e2be8-105">DESCRIPTION</span></span>
<span data-ttu-id="e2be8-106">Il cmdlet **Stop-AzBatchJobSchedule** interrompe la pianificazione di un processo batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="e2be8-106">The **Stop-AzBatchJobSchedule** cmdlet stops an Azure Batch job schedule.</span></span>

## <span data-ttu-id="e2be8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e2be8-107">EXAMPLES</span></span>

### <span data-ttu-id="e2be8-108">Esempio 1: Interrompere la pianificazione di un processo</span><span class="sxs-lookup"><span data-stu-id="e2be8-108">Example 1: Stop a job schedule</span></span>
```
PS C:\>Stop-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="e2be8-109">Questo comando interrompe la pianificazione del processo con ID JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="e2be8-109">This command stops the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="e2be8-110">Usare il cmdlet Get-AzBatchAccountKey per assegnare un contesto alla $Context variabile.</span><span class="sxs-lookup"><span data-stu-id="e2be8-110">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="e2be8-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2be8-111">PARAMETERS</span></span>

### <span data-ttu-id="e2be8-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e2be8-112">-BatchContext</span></span>
<span data-ttu-id="e2be8-113">Specifica **l'istanza BatchAccountContext** che questo cmdlet usa per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="e2be8-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e2be8-114">Se si usa il cmdlet Get-AzBatchAccount per ottenere BatchAccountContext, verrà usata l'autenticazione di Azure Active Directory quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="e2be8-114">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e2be8-115">Per usare invece l'autenticazione della chiave condivisa, usare il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con le relative chiavi di accesso popolate.</span><span class="sxs-lookup"><span data-stu-id="e2be8-115">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e2be8-116">Quando si usa l'autenticazione con chiave condivisa, per impostazione predefinita viene usata la chiave di accesso primario.</span><span class="sxs-lookup"><span data-stu-id="e2be8-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e2be8-117">Per modificare la chiave da usare, impostare la proprietà BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="e2be8-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e2be8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2be8-118">-DefaultProfile</span></span>
<span data-ttu-id="e2be8-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e2be8-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2be8-120">-Id</span><span class="sxs-lookup"><span data-stu-id="e2be8-120">-Id</span></span>
<span data-ttu-id="e2be8-121">Specifica l'ID della pianificazione del processo interrotta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2be8-121">Specifies the ID of the job schedule that this cmdlet stops.</span></span>

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

### <span data-ttu-id="e2be8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2be8-122">CommonParameters</span></span>
<span data-ttu-id="e2be8-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2be8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2be8-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e2be8-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2be8-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="e2be8-125">INPUTS</span></span>

### <span data-ttu-id="e2be8-126">System.String</span><span class="sxs-lookup"><span data-stu-id="e2be8-126">System.String</span></span>

### <span data-ttu-id="e2be8-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e2be8-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e2be8-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e2be8-128">OUTPUTS</span></span>

### <span data-ttu-id="e2be8-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="e2be8-129">System.Void</span></span>

## <span data-ttu-id="e2be8-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="e2be8-130">NOTES</span></span>

## <span data-ttu-id="e2be8-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e2be8-131">RELATED LINKS</span></span>

[<span data-ttu-id="e2be8-132">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e2be8-132">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="e2be8-133">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e2be8-133">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="e2be8-134">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="e2be8-134">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="e2be8-135">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e2be8-135">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="e2be8-136">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e2be8-136">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="e2be8-137">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e2be8-137">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="e2be8-138">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="e2be8-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
