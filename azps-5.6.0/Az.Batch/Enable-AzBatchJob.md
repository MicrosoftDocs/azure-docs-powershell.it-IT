---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 7C79BFF1-41E1-472D-AF67-1C3B39AB7548
online version: https://docs.microsoft.com/powershell/module/az.batch/enable-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJob.md
ms.openlocfilehash: 1470f02570462a3a7bb922c88504e3c8a20eb8fb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971565"
---
# <span data-ttu-id="627ad-101">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="627ad-101">Enable-AzBatchJob</span></span>

## <span data-ttu-id="627ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="627ad-102">SYNOPSIS</span></span>
<span data-ttu-id="627ad-103">Abilita un processo batch.</span><span class="sxs-lookup"><span data-stu-id="627ad-103">Enables a Batch job.</span></span>

## <span data-ttu-id="627ad-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="627ad-104">SYNTAX</span></span>

```
Enable-AzBatchJob [-Id] <String> -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="627ad-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="627ad-105">DESCRIPTION</span></span>
<span data-ttu-id="627ad-106">Il cmdlet **Enable-AzBatchJob** abilita un processo batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="627ad-106">The **Enable-AzBatchJob** cmdlet enables an Azure Batch job.</span></span>
<span data-ttu-id="627ad-107">Dopo aver abilitato un processo, è possibile eseguire nuove attività.</span><span class="sxs-lookup"><span data-stu-id="627ad-107">After you enable a job, new tasks can run.</span></span>

## <span data-ttu-id="627ad-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="627ad-108">EXAMPLES</span></span>

### <span data-ttu-id="627ad-109">Esempio 1: Abilitare un processo batch</span><span class="sxs-lookup"><span data-stu-id="627ad-109">Example 1: Enable a Batch job</span></span>
```
PS C:\>Enable-AzBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="627ad-110">Questo comando abilita il processo con ID Processo-000001.</span><span class="sxs-lookup"><span data-stu-id="627ad-110">This command enables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="627ad-111">Usare il cmdlet Get-AzBatchAccountKey per assegnare un contesto alla $Context variabile.</span><span class="sxs-lookup"><span data-stu-id="627ad-111">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="627ad-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="627ad-112">PARAMETERS</span></span>

### <span data-ttu-id="627ad-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="627ad-113">-BatchContext</span></span>
<span data-ttu-id="627ad-114">Specifica **l'istanza BatchAccountContext** che questo cmdlet usa per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="627ad-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="627ad-115">Se si usa il cmdlet Get-AzBatchAccount per ottenere BatchAccountContext, verrà usata l'autenticazione di Azure Active Directory quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="627ad-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="627ad-116">Per usare invece l'autenticazione della chiave condivisa, usare il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con le relative chiavi di accesso popolate.</span><span class="sxs-lookup"><span data-stu-id="627ad-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="627ad-117">Quando si usa l'autenticazione con chiave condivisa, per impostazione predefinita viene usata la chiave di accesso primario.</span><span class="sxs-lookup"><span data-stu-id="627ad-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="627ad-118">Per modificare la chiave da usare, impostare la proprietà BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="627ad-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="627ad-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="627ad-119">-DefaultProfile</span></span>
<span data-ttu-id="627ad-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="627ad-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="627ad-121">-Id</span><span class="sxs-lookup"><span data-stu-id="627ad-121">-Id</span></span>
<span data-ttu-id="627ad-122">Specifica l'ID del processo che questo cmdlet abilita.</span><span class="sxs-lookup"><span data-stu-id="627ad-122">Specifies the ID of the job that this cmdlet enables.</span></span>

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

### <span data-ttu-id="627ad-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="627ad-123">CommonParameters</span></span>
<span data-ttu-id="627ad-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="627ad-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="627ad-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="627ad-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="627ad-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="627ad-126">INPUTS</span></span>

### <span data-ttu-id="627ad-127">System.String</span><span class="sxs-lookup"><span data-stu-id="627ad-127">System.String</span></span>

### <span data-ttu-id="627ad-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="627ad-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="627ad-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="627ad-129">OUTPUTS</span></span>

### <span data-ttu-id="627ad-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="627ad-130">System.Void</span></span>

## <span data-ttu-id="627ad-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="627ad-131">NOTES</span></span>

## <span data-ttu-id="627ad-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="627ad-132">RELATED LINKS</span></span>

[<span data-ttu-id="627ad-133">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="627ad-133">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="627ad-134">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="627ad-134">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="627ad-135">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="627ad-135">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="627ad-136">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="627ad-136">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="627ad-137">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="627ad-137">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="627ad-138">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="627ad-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
