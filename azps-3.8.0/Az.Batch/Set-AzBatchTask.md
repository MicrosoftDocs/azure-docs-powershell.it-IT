---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 6A6D6C7D-EED7-4AD4-ACE6-BFA64404455E
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchTask.md
ms.openlocfilehash: 80cfa0453bf521ee8b29fb6a330ec194ada84383
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2020
ms.locfileid: "94030706"
---
# <span data-ttu-id="570a2-101">Set-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="570a2-101">Set-AzBatchTask</span></span>

## <span data-ttu-id="570a2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="570a2-102">SYNOPSIS</span></span>
<span data-ttu-id="570a2-103">Aggiorna le proprietà di un'attività.</span><span class="sxs-lookup"><span data-stu-id="570a2-103">Updates the properties of a task.</span></span>

## <span data-ttu-id="570a2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="570a2-104">SYNTAX</span></span>

```
Set-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="570a2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="570a2-105">DESCRIPTION</span></span>
<span data-ttu-id="570a2-106">Il cmdlet **set-AzBatchTask** aggiorna le proprietà di un'attività nel servizio batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="570a2-106">The **Set-AzBatchTask** cmdlet updates the properties of a task in the Azure Batch service.</span></span>
<span data-ttu-id="570a2-107">Usa il cmdlet Get-AzBatchTask per ottenere un oggetto **PSCloudTask** .</span><span class="sxs-lookup"><span data-stu-id="570a2-107">Use the Get-AzBatchTask cmdlet to get a **PSCloudTask** object.</span></span>
<span data-ttu-id="570a2-108">Modificare le proprietà di tale oggetto e quindi usare il cmdlet corrente per eseguire il commit delle modifiche apportate al servizio batch.</span><span class="sxs-lookup"><span data-stu-id="570a2-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="570a2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="570a2-109">EXAMPLES</span></span>

### <span data-ttu-id="570a2-110">Esempio 1: aggiornare un'attività</span><span class="sxs-lookup"><span data-stu-id="570a2-110">Example 1: Update a task</span></span>
```
PS C:\>$Task = Get-AzBatchTask -JobId "Job16" -Id "Task22" -BatchContext $Context
PS C:\> $Constraints = New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints -ArgumentList @([TimeSpan}::FromDays(5), [TimeSpan]::FromDays(2), 3)
PS C:\> $Task.Constraints = $Constraints
PS C:\> Set-AzBatchTask -Task $Task -BatchContext $Context
```

<span data-ttu-id="570a2-111">Il primo comando ottiene un'attività usando **Get-AzBatchTask** e lo archivia nella variabile $Task.</span><span class="sxs-lookup"><span data-stu-id="570a2-111">The first command gets a task by using **Get-AzBatchTask** , and then stores it in the $Task variable.</span></span>
<span data-ttu-id="570a2-112">I due comandi successivi modificano i vincoli dell'attività in $Task.</span><span class="sxs-lookup"><span data-stu-id="570a2-112">The next two commands modify the constraints of the task in $Task.</span></span>
<span data-ttu-id="570a2-113">Il comando finale aggiorna il servizio batch in base all'oggetto locale in $Task.</span><span class="sxs-lookup"><span data-stu-id="570a2-113">The final command updates the Batch service to match the local object in $Task.</span></span>

## <span data-ttu-id="570a2-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="570a2-114">PARAMETERS</span></span>

### <span data-ttu-id="570a2-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="570a2-115">-BatchContext</span></span>
<span data-ttu-id="570a2-116">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="570a2-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="570a2-117">Se si usa il cmdlet Get-AzBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="570a2-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="570a2-118">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="570a2-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="570a2-119">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="570a2-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="570a2-120">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="570a2-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="570a2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="570a2-121">-DefaultProfile</span></span>
<span data-ttu-id="570a2-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="570a2-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="570a2-123">-Attività</span><span class="sxs-lookup"><span data-stu-id="570a2-123">-Task</span></span>
<span data-ttu-id="570a2-124">Specifica il **PSCloudTask** a cui questo cmdlet aggiorna il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="570a2-124">Specifies the **PSCloudTask** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="570a2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="570a2-125">CommonParameters</span></span>
<span data-ttu-id="570a2-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="570a2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="570a2-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="570a2-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="570a2-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="570a2-128">INPUTS</span></span>

### <span data-ttu-id="570a2-129">Microsoft.Azure.Commands.Batch. Models. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="570a2-129">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="570a2-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="570a2-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="570a2-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="570a2-131">OUTPUTS</span></span>

### <span data-ttu-id="570a2-132">System. void</span><span class="sxs-lookup"><span data-stu-id="570a2-132">System.Void</span></span>

## <span data-ttu-id="570a2-133">Note</span><span class="sxs-lookup"><span data-stu-id="570a2-133">NOTES</span></span>

## <span data-ttu-id="570a2-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="570a2-134">RELATED LINKS</span></span>

[<span data-ttu-id="570a2-135">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="570a2-135">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="570a2-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="570a2-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="570a2-137">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="570a2-137">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="570a2-138">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="570a2-138">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="570a2-139">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="570a2-139">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="570a2-140">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="570a2-140">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


