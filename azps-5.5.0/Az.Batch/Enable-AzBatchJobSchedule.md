---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 02F91510-F14F-4401-BC5F-06B0874AEB4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJobSchedule.md
ms.openlocfilehash: 03decd5b1d32defb25692220c63ffe768445697e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205362"
---
# <span data-ttu-id="4340e-101">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="4340e-101">Enable-AzBatchJobSchedule</span></span>

## <span data-ttu-id="4340e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4340e-102">SYNOPSIS</span></span>
<span data-ttu-id="4340e-103">Abilita la pianificazione di un processo batch.</span><span class="sxs-lookup"><span data-stu-id="4340e-103">Enables a Batch job schedule.</span></span>

## <span data-ttu-id="4340e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4340e-104">SYNTAX</span></span>

```
Enable-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4340e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4340e-105">DESCRIPTION</span></span>
<span data-ttu-id="4340e-106">Il cmdlet **Enable-AzBatchJobSchedule** abilita la pianificazione di un processo batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="4340e-106">The **Enable-AzBatchJobSchedule** cmdlet enables an Azure Batch job schedule.</span></span>
<span data-ttu-id="4340e-107">Dopo aver abilitato la pianificazione di un processo, i processi possono essere creati in base a tale pianificazione.</span><span class="sxs-lookup"><span data-stu-id="4340e-107">After you enable a job schedule, jobs can be created according to that schedule.</span></span>

## <span data-ttu-id="4340e-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4340e-108">EXAMPLES</span></span>

### <span data-ttu-id="4340e-109">Esempio 1: Abilitare la pianificazione di un processo</span><span class="sxs-lookup"><span data-stu-id="4340e-109">Example 1: Enable a job schedule</span></span>
```
PS C:\>Enable-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="4340e-110">Questo comando abilita la pianificazione del processo con ID JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="4340e-110">This command enables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="4340e-111">Usare il cmdlet **Get-AzBatchAccountKey** per assegnare un contesto alla $Context variabile.</span><span class="sxs-lookup"><span data-stu-id="4340e-111">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="4340e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4340e-112">PARAMETERS</span></span>

### <span data-ttu-id="4340e-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="4340e-113">-BatchContext</span></span>
<span data-ttu-id="4340e-114">Specifica **l'istanza BatchAccountContext** che questo cmdlet usa per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="4340e-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="4340e-115">Se si usa il cmdlet Get-AzBatchAccount per ottenere BatchAccountContext, verrà usata l'autenticazione di Azure Active Directory quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="4340e-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="4340e-116">Per usare invece l'autenticazione della chiave condivisa, usare il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con le relative chiavi di accesso popolate.</span><span class="sxs-lookup"><span data-stu-id="4340e-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="4340e-117">Quando si usa l'autenticazione con chiave condivisa, per impostazione predefinita viene usata la chiave di accesso primario.</span><span class="sxs-lookup"><span data-stu-id="4340e-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="4340e-118">Per modificare la chiave da usare, impostare la proprietà BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="4340e-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="4340e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4340e-119">-DefaultProfile</span></span>
<span data-ttu-id="4340e-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4340e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4340e-121">-Id</span><span class="sxs-lookup"><span data-stu-id="4340e-121">-Id</span></span>
<span data-ttu-id="4340e-122">Specifica l'ID della pianificazione del processo abilitata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4340e-122">Specifies the ID of the job schedule that this cmdlet enables.</span></span>

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

### <span data-ttu-id="4340e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4340e-123">CommonParameters</span></span>
<span data-ttu-id="4340e-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4340e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4340e-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4340e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4340e-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="4340e-126">INPUTS</span></span>

### <span data-ttu-id="4340e-127">System.String</span><span class="sxs-lookup"><span data-stu-id="4340e-127">System.String</span></span>

### <span data-ttu-id="4340e-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4340e-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="4340e-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4340e-129">OUTPUTS</span></span>

### <span data-ttu-id="4340e-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="4340e-130">System.Void</span></span>

## <span data-ttu-id="4340e-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="4340e-131">NOTES</span></span>

## <span data-ttu-id="4340e-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4340e-132">RELATED LINKS</span></span>

[<span data-ttu-id="4340e-133">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="4340e-133">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="4340e-134">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="4340e-134">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="4340e-135">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="4340e-135">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="4340e-136">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="4340e-136">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="4340e-137">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="4340e-137">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="4340e-138">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="4340e-138">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="4340e-139">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="4340e-139">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
