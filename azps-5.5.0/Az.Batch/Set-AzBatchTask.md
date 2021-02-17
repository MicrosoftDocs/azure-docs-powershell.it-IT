---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 6A6D6C7D-EED7-4AD4-ACE6-BFA64404455E
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchTask.md
ms.openlocfilehash: 7c3e976e85e6754702f8288f5bb257086837fc36
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205187"
---
# <span data-ttu-id="8c78b-101">Set-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="8c78b-101">Set-AzBatchTask</span></span>

## <span data-ttu-id="8c78b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c78b-102">SYNOPSIS</span></span>
<span data-ttu-id="8c78b-103">Aggiorna le proprietà di un'attività.</span><span class="sxs-lookup"><span data-stu-id="8c78b-103">Updates the properties of a task.</span></span>

## <span data-ttu-id="8c78b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8c78b-104">SYNTAX</span></span>

```
Set-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c78b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8c78b-105">DESCRIPTION</span></span>
<span data-ttu-id="8c78b-106">Il **cmdlet Set-AzBatchTask** aggiorna le proprietà di un'attività nel servizio batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="8c78b-106">The **Set-AzBatchTask** cmdlet updates the properties of a task in the Azure Batch service.</span></span>
<span data-ttu-id="8c78b-107">Usare il cmdlet Get-AzBatchTask per ottenere un **oggetto PSCloudTask.**</span><span class="sxs-lookup"><span data-stu-id="8c78b-107">Use the Get-AzBatchTask cmdlet to get a **PSCloudTask** object.</span></span>
<span data-ttu-id="8c78b-108">Modificare le proprietà dell'oggetto e quindi usare il cmdlet corrente per eseguire il commit delle modifiche al servizio batch.</span><span class="sxs-lookup"><span data-stu-id="8c78b-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="8c78b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8c78b-109">EXAMPLES</span></span>

### <span data-ttu-id="8c78b-110">Esempio 1: Aggiornare un'attività</span><span class="sxs-lookup"><span data-stu-id="8c78b-110">Example 1: Update a task</span></span>
```
PS C:\>$Task = Get-AzBatchTask -JobId "Job16" -Id "Task22" -BatchContext $Context
PS C:\> $Constraints = New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints -ArgumentList @([TimeSpan}::FromDays(5), [TimeSpan]::FromDays(2), 3)
PS C:\> $Task.Constraints = $Constraints
PS C:\> Set-AzBatchTask -Task $Task -BatchContext $Context
```

<span data-ttu-id="8c78b-111">Il primo comando ottiene un'attività usando **Get-AzBatchTask** e quindi la archivia nella $Task variabile.</span><span class="sxs-lookup"><span data-stu-id="8c78b-111">The first command gets a task by using **Get-AzBatchTask**, and then stores it in the $Task variable.</span></span>
<span data-ttu-id="8c78b-112">I due comandi seguenti modificano i vincoli dell'attività in $Task.</span><span class="sxs-lookup"><span data-stu-id="8c78b-112">The next two commands modify the constraints of the task in $Task.</span></span>
<span data-ttu-id="8c78b-113">Il comando finale aggiorna il servizio batch in modo che corrisponda all'oggetto locale in $Task.</span><span class="sxs-lookup"><span data-stu-id="8c78b-113">The final command updates the Batch service to match the local object in $Task.</span></span>

## <span data-ttu-id="8c78b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c78b-114">PARAMETERS</span></span>

### <span data-ttu-id="8c78b-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="8c78b-115">-BatchContext</span></span>
<span data-ttu-id="8c78b-116">Specifica **l'istanza BatchAccountContext** che questo cmdlet usa per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="8c78b-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8c78b-117">Se si usa il cmdlet Get-AzBatchAccount per ottenere BatchAccountContext, verrà usata l'autenticazione di Azure Active Directory quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="8c78b-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="8c78b-118">Per usare invece l'autenticazione della chiave condivisa, usare il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con le relative chiavi di accesso popolate.</span><span class="sxs-lookup"><span data-stu-id="8c78b-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="8c78b-119">Quando si usa l'autenticazione con chiave condivisa, per impostazione predefinita viene usata la chiave di accesso primario.</span><span class="sxs-lookup"><span data-stu-id="8c78b-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="8c78b-120">Per modificare la chiave da usare, impostare la proprietà BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="8c78b-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="8c78b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c78b-121">-DefaultProfile</span></span>
<span data-ttu-id="8c78b-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8c78b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c78b-123">-Attività</span><span class="sxs-lookup"><span data-stu-id="8c78b-123">-Task</span></span>
<span data-ttu-id="8c78b-124">Specifica **l'attività PSCloudTask** a cui questo cmdlet aggiorna il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="8c78b-124">Specifies the **PSCloudTask** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c78b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c78b-125">CommonParameters</span></span>
<span data-ttu-id="8c78b-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c78b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c78b-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8c78b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c78b-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="8c78b-128">INPUTS</span></span>

### <span data-ttu-id="8c78b-129">Microsoft.Azure.Commands.Batch. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="8c78b-129">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="8c78b-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8c78b-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="8c78b-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8c78b-131">OUTPUTS</span></span>

### <span data-ttu-id="8c78b-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="8c78b-132">System.Void</span></span>

## <span data-ttu-id="8c78b-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="8c78b-133">NOTES</span></span>

## <span data-ttu-id="8c78b-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8c78b-134">RELATED LINKS</span></span>

[<span data-ttu-id="8c78b-135">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="8c78b-135">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="8c78b-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="8c78b-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="8c78b-137">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="8c78b-137">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="8c78b-138">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="8c78b-138">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="8c78b-139">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="8c78b-139">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="8c78b-140">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="8c78b-140">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
