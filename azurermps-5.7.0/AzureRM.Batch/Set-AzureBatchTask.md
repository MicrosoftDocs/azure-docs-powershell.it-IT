---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 6A6D6C7D-EED7-4AD4-ACE6-BFA64404455E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchTask.md
ms.openlocfilehash: 6e6bb12aeb5b5d319b0997578991c87e91c81003
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515803"
---
# <span data-ttu-id="d933b-101">Set-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="d933b-101">Set-AzureBatchTask</span></span>

## <span data-ttu-id="d933b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d933b-102">SYNOPSIS</span></span>
<span data-ttu-id="d933b-103">Aggiorna le proprietà di un'attività.</span><span class="sxs-lookup"><span data-stu-id="d933b-103">Updates the properties of a task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d933b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d933b-104">SYNTAX</span></span>

```
Set-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d933b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d933b-105">DESCRIPTION</span></span>
<span data-ttu-id="d933b-106">Il cmdlet **set-AzureBatchTask** aggiorna le proprietà di un'attività nel servizio batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="d933b-106">The **Set-AzureBatchTask** cmdlet updates the properties of a task in the Azure Batch service.</span></span>
<span data-ttu-id="d933b-107">Usa il cmdlet Get-AzureBatchTask per ottenere un oggetto **PSCloudTask** .</span><span class="sxs-lookup"><span data-stu-id="d933b-107">Use the Get-AzureBatchTask cmdlet to get a **PSCloudTask** object.</span></span>
<span data-ttu-id="d933b-108">Modificare le proprietà di tale oggetto e quindi usare il cmdlet corrente per eseguire il commit delle modifiche apportate al servizio batch.</span><span class="sxs-lookup"><span data-stu-id="d933b-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="d933b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d933b-109">EXAMPLES</span></span>

### <span data-ttu-id="d933b-110">Esempio 1: aggiornare un'attività</span><span class="sxs-lookup"><span data-stu-id="d933b-110">Example 1: Update a task</span></span>
```
PS C:\>$Task = Get-AzureBatchTask -JobId "Job16" -Id "Task22" -BatchContext $Context
PS C:\> $Constraints = New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints -ArgumentList @([TimeSpan}::FromDays(5), [TimeSpan]::FromDays(2), 3)
PS C:\> $Task.Constraints = $Constraints
PS C:\> Set-AzureBatchTask -Task $Task -BatchContext $Context
```

<span data-ttu-id="d933b-111">Il primo comando ottiene un'attività usando **Get-AzureBatchTask** e lo archivia nella variabile $Task.</span><span class="sxs-lookup"><span data-stu-id="d933b-111">The first command gets a task by using **Get-AzureBatchTask** , and then stores it in the $Task variable.</span></span>

<span data-ttu-id="d933b-112">I due comandi successivi modificano i vincoli dell'attività in $Task.</span><span class="sxs-lookup"><span data-stu-id="d933b-112">The next two commands modify the constraints of the task in $Task.</span></span>

<span data-ttu-id="d933b-113">Il comando finale aggiorna il servizio batch in base all'oggetto locale in $Task.</span><span class="sxs-lookup"><span data-stu-id="d933b-113">The final command updates the Batch service to match the local object in $Task.</span></span>

## <span data-ttu-id="d933b-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d933b-114">PARAMETERS</span></span>

### <span data-ttu-id="d933b-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d933b-115">-BatchContext</span></span>
<span data-ttu-id="d933b-116">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="d933b-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d933b-117">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="d933b-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d933b-118">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="d933b-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d933b-119">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="d933b-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d933b-120">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="d933b-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d933b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d933b-121">-DefaultProfile</span></span>
<span data-ttu-id="d933b-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d933b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d933b-123">-Attività</span><span class="sxs-lookup"><span data-stu-id="d933b-123">-Task</span></span>
<span data-ttu-id="d933b-124">Specifica il **PSCloudTask** a cui questo cmdlet aggiorna il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="d933b-124">Specifies the **PSCloudTask** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: PSCloudTask
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d933b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d933b-125">CommonParameters</span></span>
<span data-ttu-id="d933b-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d933b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d933b-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d933b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d933b-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d933b-128">INPUTS</span></span>

### <span data-ttu-id="d933b-129">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d933b-129">BatchAccountContext</span></span>
<span data-ttu-id="d933b-130">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="d933b-130">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="d933b-131">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="d933b-131">PSCloudTask</span></span>
<span data-ttu-id="d933b-132">Il parametro ' Task ' accetta il valore di tipo ' PSCloudTask ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="d933b-132">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="d933b-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d933b-133">OUTPUTS</span></span>

## <span data-ttu-id="d933b-134">Note</span><span class="sxs-lookup"><span data-stu-id="d933b-134">NOTES</span></span>

## <span data-ttu-id="d933b-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d933b-135">RELATED LINKS</span></span>

[<span data-ttu-id="d933b-136">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="d933b-136">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="d933b-137">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="d933b-137">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="d933b-138">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="d933b-138">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="d933b-139">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="d933b-139">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="d933b-140">Stop-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="d933b-140">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="d933b-141">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="d933b-141">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


