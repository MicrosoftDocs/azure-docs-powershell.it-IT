---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 1EA57372-6FA5-45C9-94A1-50D53830FC10
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchTask.md
ms.openlocfilehash: 979c136f1bdbd216cebe367060ebdc5d8360ea24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510096"
---
# <span data-ttu-id="29e27-101">Stop-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="29e27-101">Stop-AzureBatchTask</span></span>

## <span data-ttu-id="29e27-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="29e27-102">SYNOPSIS</span></span>
<span data-ttu-id="29e27-103">Interrompe un'attività batch.</span><span class="sxs-lookup"><span data-stu-id="29e27-103">Stops a Batch task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29e27-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="29e27-104">SYNTAX</span></span>

### <span data-ttu-id="29e27-105">ID</span><span class="sxs-lookup"><span data-stu-id="29e27-105">Id</span></span>
```
Stop-AzureBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29e27-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="29e27-106">InputObject</span></span>
```
Stop-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29e27-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="29e27-107">DESCRIPTION</span></span>
<span data-ttu-id="29e27-108">Il cmdlet **Stop-AzureBatchTask** interrompe un'attività batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="29e27-108">The **Stop-AzureBatchTask** cmdlet stops an Azure Batch task.</span></span>

## <span data-ttu-id="29e27-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="29e27-109">EXAMPLES</span></span>

### <span data-ttu-id="29e27-110">Esempio 1: eliminare un'attività batch in base all'ID</span><span class="sxs-lookup"><span data-stu-id="29e27-110">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Stop-AzureBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="29e27-111">Questo comando Arresta un'attività con ID Task23 sotto il processo con ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="29e27-111">This command stops a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="29e27-112">Il comando richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="29e27-112">The command prompts you for confirmation.</span></span>
<span data-ttu-id="29e27-113">Usa il cmdlet Get-AzureRmBatchAccountKeys per assegnare un contesto alla variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="29e27-113">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="29e27-114">Esempio 2: arrestare un'attività batch usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="29e27-114">Example 2: Stop a Batch task by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Stop-AzureBatchTask -BatchContext $Context
```

<span data-ttu-id="29e27-115">Questo comando ottiene l'attività batch che contiene l'ID Task26 nel processo con l'ID Job-000001 usando il cmdlet Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="29e27-115">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the Get-AzureBatchTask cmdlet.</span></span>
<span data-ttu-id="29e27-116">Il comando passa l'attività al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="29e27-116">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="29e27-117">Il comando interrompe l'attività.</span><span class="sxs-lookup"><span data-stu-id="29e27-117">The command stops that task.</span></span>

## <span data-ttu-id="29e27-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="29e27-118">PARAMETERS</span></span>

### <span data-ttu-id="29e27-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="29e27-119">-BatchContext</span></span>
<span data-ttu-id="29e27-120">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="29e27-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="29e27-121">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="29e27-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="29e27-122">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="29e27-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="29e27-123">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="29e27-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="29e27-124">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="29e27-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="29e27-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29e27-125">-DefaultProfile</span></span>
<span data-ttu-id="29e27-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="29e27-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29e27-127">-ID</span><span class="sxs-lookup"><span data-stu-id="29e27-127">-Id</span></span>
<span data-ttu-id="29e27-128">Specifica l'ID dell'attività arrestata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29e27-128">Specifies the ID of the task that this cmdlet stops.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29e27-129">-JobId</span><span class="sxs-lookup"><span data-stu-id="29e27-129">-JobId</span></span>
<span data-ttu-id="29e27-130">Specifica l'ID del processo che contiene l'attività.</span><span class="sxs-lookup"><span data-stu-id="29e27-130">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29e27-131">-Attività</span><span class="sxs-lookup"><span data-stu-id="29e27-131">-Task</span></span>
<span data-ttu-id="29e27-132">Specifica l'attività arrestata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29e27-132">Specifies the task that this cmdlet stops.</span></span>
<span data-ttu-id="29e27-133">Per ottenere un oggetto **PSCloudTask** , usa il cmdlet Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="29e27-133">To obtain a **PSCloudTask** object, use the Get-AzureBatchTask cmdlet.</span></span>

```yaml
Type: PSCloudTask
Parameter Sets: InputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29e27-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29e27-134">CommonParameters</span></span>
<span data-ttu-id="29e27-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29e27-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29e27-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29e27-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29e27-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="29e27-137">INPUTS</span></span>

### <span data-ttu-id="29e27-138">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="29e27-138">BatchAccountContext</span></span>
<span data-ttu-id="29e27-139">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="29e27-139">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="29e27-140">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="29e27-140">PSCloudTask</span></span>
<span data-ttu-id="29e27-141">Il parametro ' Task ' accetta il valore di tipo ' PSCloudTask ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="29e27-141">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="29e27-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="29e27-142">OUTPUTS</span></span>

## <span data-ttu-id="29e27-143">Note</span><span class="sxs-lookup"><span data-stu-id="29e27-143">NOTES</span></span>

## <span data-ttu-id="29e27-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="29e27-144">RELATED LINKS</span></span>

[<span data-ttu-id="29e27-145">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="29e27-145">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="29e27-146">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="29e27-146">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="29e27-147">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="29e27-147">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="29e27-148">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="29e27-148">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


