---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 6A6D6C7D-EED7-4AD4-ACE6-BFA64404455E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchTask.md
ms.openlocfilehash: bae5f2b075f8d4f2fa579b38bdccf160cd46caad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685584"
---
# <span data-ttu-id="08c03-101">Set-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="08c03-101">Set-AzureBatchTask</span></span>

## <span data-ttu-id="08c03-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="08c03-102">SYNOPSIS</span></span>
<span data-ttu-id="08c03-103">Aggiorna le proprietà di un'attività.</span><span class="sxs-lookup"><span data-stu-id="08c03-103">Updates the properties of a task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08c03-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="08c03-104">SYNTAX</span></span>

```
Set-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08c03-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="08c03-105">DESCRIPTION</span></span>
<span data-ttu-id="08c03-106">Il cmdlet **set-AzureBatchTask** aggiorna le proprietà di un'attività nel servizio batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="08c03-106">The **Set-AzureBatchTask** cmdlet updates the properties of a task in the Azure Batch service.</span></span>
<span data-ttu-id="08c03-107">Usa il cmdlet Get-AzureBatchTask per ottenere un oggetto **PSCloudTask** .</span><span class="sxs-lookup"><span data-stu-id="08c03-107">Use the Get-AzureBatchTask cmdlet to get a **PSCloudTask** object.</span></span>
<span data-ttu-id="08c03-108">Modificare le proprietà di tale oggetto e quindi usare il cmdlet corrente per eseguire il commit delle modifiche apportate al servizio batch.</span><span class="sxs-lookup"><span data-stu-id="08c03-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="08c03-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="08c03-109">EXAMPLES</span></span>

### <span data-ttu-id="08c03-110">Esempio 1: aggiornare un'attività</span><span class="sxs-lookup"><span data-stu-id="08c03-110">Example 1: Update a task</span></span>
```
PS C:\>$Task = Get-AzureBatchTask -JobId "Job16" -Id "Task22" -BatchContext $Context
PS C:\> $Constraints = New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints -ArgumentList @([TimeSpan}::FromDays(5), [TimeSpan]::FromDays(2), 3)
PS C:\> $Task.Constraints = $Constraints
PS C:\> Set-AzureBatchTask -Task $Task -BatchContext $Context
```

<span data-ttu-id="08c03-111">Il primo comando ottiene un'attività usando **Get-AzureBatchTask** e lo archivia nella variabile $Task.</span><span class="sxs-lookup"><span data-stu-id="08c03-111">The first command gets a task by using **Get-AzureBatchTask** , and then stores it in the $Task variable.</span></span>
<span data-ttu-id="08c03-112">I due comandi successivi modificano i vincoli dell'attività in $Task.</span><span class="sxs-lookup"><span data-stu-id="08c03-112">The next two commands modify the constraints of the task in $Task.</span></span>
<span data-ttu-id="08c03-113">Il comando finale aggiorna il servizio batch in base all'oggetto locale in $Task.</span><span class="sxs-lookup"><span data-stu-id="08c03-113">The final command updates the Batch service to match the local object in $Task.</span></span>

## <span data-ttu-id="08c03-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="08c03-114">PARAMETERS</span></span>

### <span data-ttu-id="08c03-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="08c03-115">-BatchContext</span></span>
<span data-ttu-id="08c03-116">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="08c03-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="08c03-117">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="08c03-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="08c03-118">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="08c03-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="08c03-119">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="08c03-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="08c03-120">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="08c03-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="08c03-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08c03-121">-DefaultProfile</span></span>
<span data-ttu-id="08c03-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="08c03-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08c03-123">-Attività</span><span class="sxs-lookup"><span data-stu-id="08c03-123">-Task</span></span>
<span data-ttu-id="08c03-124">Specifica il **PSCloudTask** a cui questo cmdlet aggiorna il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="08c03-124">Specifies the **PSCloudTask** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="08c03-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08c03-125">CommonParameters</span></span>
<span data-ttu-id="08c03-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08c03-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08c03-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08c03-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08c03-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="08c03-128">INPUTS</span></span>

### <span data-ttu-id="08c03-129">Microsoft.Azure.Commands.Batch. Models. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="08c03-129">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>
<span data-ttu-id="08c03-130">Parametri: attività (ByValue)</span><span class="sxs-lookup"><span data-stu-id="08c03-130">Parameters: Task (ByValue)</span></span>

### <span data-ttu-id="08c03-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="08c03-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="08c03-132">Parametri: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="08c03-132">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="08c03-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="08c03-133">OUTPUTS</span></span>

### <span data-ttu-id="08c03-134">System. void</span><span class="sxs-lookup"><span data-stu-id="08c03-134">System.Void</span></span>

## <span data-ttu-id="08c03-135">Note</span><span class="sxs-lookup"><span data-stu-id="08c03-135">NOTES</span></span>

## <span data-ttu-id="08c03-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="08c03-136">RELATED LINKS</span></span>

[<span data-ttu-id="08c03-137">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="08c03-137">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="08c03-138">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="08c03-138">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="08c03-139">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="08c03-139">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="08c03-140">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="08c03-140">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="08c03-141">Stop-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="08c03-141">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="08c03-142">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="08c03-142">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


