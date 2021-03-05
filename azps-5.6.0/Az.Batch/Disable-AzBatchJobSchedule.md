---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B4737AE8-F57C-4B95-B81E-74802EF8E7AE
online version: https://docs.microsoft.com/powershell/module/az.batch/disable-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJobSchedule.md
ms.openlocfilehash: 54b9f9b60c1d424e6fd62ede85e517b40df1d062
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014014"
---
# <span data-ttu-id="cec9e-101">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cec9e-101">Disable-AzBatchJobSchedule</span></span>

## <span data-ttu-id="cec9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cec9e-102">SYNOPSIS</span></span>
<span data-ttu-id="cec9e-103">Disabilita la pianificazione di un processo batch.</span><span class="sxs-lookup"><span data-stu-id="cec9e-103">Disables a Batch job schedule.</span></span>

## <span data-ttu-id="cec9e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cec9e-104">SYNTAX</span></span>

```
Disable-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cec9e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cec9e-105">DESCRIPTION</span></span>
<span data-ttu-id="cec9e-106">Il cmdlet **Disable-AzBatchJobSchedule** disabilita la pianificazione di un processo batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="cec9e-106">The **Disable-AzBatchJobSchedule** cmdlet disables an Azure Batch job schedule.</span></span>
<span data-ttu-id="cec9e-107">Se si disabilita una pianificazione, i processi non vengono creati in base a tale pianificazione.</span><span class="sxs-lookup"><span data-stu-id="cec9e-107">If you disable a schedule, jobs are not created according to that schedule.</span></span>
<span data-ttu-id="cec9e-108">È possibile abilitare una pianificazione disabilitata in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="cec9e-108">You can enable a disabled schedule later.</span></span>

## <span data-ttu-id="cec9e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cec9e-109">EXAMPLES</span></span>

### <span data-ttu-id="cec9e-110">Esempio 1: Disabilitare la pianificazione di un processo</span><span class="sxs-lookup"><span data-stu-id="cec9e-110">Example 1: Disable a job schedule</span></span>
```
PS C:\>Disable-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="cec9e-111">Questo comando disabilita la pianificazione del processo che contiene l'ID JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="cec9e-111">This command disables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="cec9e-112">Usare il cmdlet **Get-AzBatchAccountKey** per assegnare un contesto alla $Context variabile.</span><span class="sxs-lookup"><span data-stu-id="cec9e-112">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="cec9e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cec9e-113">PARAMETERS</span></span>

### <span data-ttu-id="cec9e-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="cec9e-114">-BatchContext</span></span>
<span data-ttu-id="cec9e-115">Specifica **l'istanza BatchAccountContext** che questo cmdlet usa per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="cec9e-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="cec9e-116">Se si usa il cmdlet Get-AzBatchAccount per ottenere BatchAccountContext, verrà usata l'autenticazione di Azure Active Directory quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="cec9e-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="cec9e-117">Per usare invece l'autenticazione della chiave condivisa, usare il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con le relative chiavi di accesso popolate.</span><span class="sxs-lookup"><span data-stu-id="cec9e-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="cec9e-118">Quando si usa l'autenticazione con chiave condivisa, per impostazione predefinita viene usata la chiave di accesso primario.</span><span class="sxs-lookup"><span data-stu-id="cec9e-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="cec9e-119">Per modificare la chiave da usare, impostare la proprietà BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="cec9e-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="cec9e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cec9e-120">-DefaultProfile</span></span>
<span data-ttu-id="cec9e-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cec9e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cec9e-122">-Id</span><span class="sxs-lookup"><span data-stu-id="cec9e-122">-Id</span></span>
<span data-ttu-id="cec9e-123">Specifica l'ID della pianificazione del processo disabilitata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cec9e-123">Specifies the ID of the job schedule that this cmdlet disables.</span></span>

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

### <span data-ttu-id="cec9e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cec9e-124">CommonParameters</span></span>
<span data-ttu-id="cec9e-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cec9e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cec9e-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cec9e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cec9e-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="cec9e-127">INPUTS</span></span>

### <span data-ttu-id="cec9e-128">System.String</span><span class="sxs-lookup"><span data-stu-id="cec9e-128">System.String</span></span>

### <span data-ttu-id="cec9e-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="cec9e-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="cec9e-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cec9e-130">OUTPUTS</span></span>

### <span data-ttu-id="cec9e-131">System.Void</span><span class="sxs-lookup"><span data-stu-id="cec9e-131">System.Void</span></span>

## <span data-ttu-id="cec9e-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="cec9e-132">NOTES</span></span>

## <span data-ttu-id="cec9e-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cec9e-133">RELATED LINKS</span></span>

[<span data-ttu-id="cec9e-134">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cec9e-134">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="cec9e-135">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="cec9e-135">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="cec9e-136">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cec9e-136">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="cec9e-137">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cec9e-137">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="cec9e-138">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cec9e-138">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="cec9e-139">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cec9e-139">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="cec9e-140">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="cec9e-140">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
