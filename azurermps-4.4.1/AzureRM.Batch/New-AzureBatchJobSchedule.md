---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 87E7FA51-427E-4DB8-A6A2-D8638FD3DB8B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJobSchedule.md
ms.openlocfilehash: 0a31b787b1be6d45caca74d01ee5d15d00071641
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517055"
---
# <span data-ttu-id="7d9e7-101">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="7d9e7-101">New-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="7d9e7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7d9e7-102">SYNOPSIS</span></span>
<span data-ttu-id="7d9e7-103">Crea una pianificazione del processo nel servizio batch.</span><span class="sxs-lookup"><span data-stu-id="7d9e7-103">Creates a job schedule in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d9e7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7d9e7-104">SYNTAX</span></span>

```
New-AzureBatchJobSchedule [-Id] <String> [-DisplayName <String>] -Schedule <PSSchedule>
 -JobSpecification <PSJobSpecification> [-Metadata <IDictionary>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d9e7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7d9e7-105">DESCRIPTION</span></span>
<span data-ttu-id="7d9e7-106">Il cmdlet **New-AzureBatchJobSchedule** crea una pianificazione del processo nel servizio batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="7d9e7-106">The **New-AzureBatchJobSchedule** cmdlet creates a job schedule in the Azure Batch service.</span></span>
<span data-ttu-id="7d9e7-107">Il parametro *BatchAccountContext* specifica l'account in cui questo cmdlet crea la pianificazione.</span><span class="sxs-lookup"><span data-stu-id="7d9e7-107">The *BatchAccountContext* parameter specifies the account in which this cmdlet creates the schedule.</span></span>

## <span data-ttu-id="7d9e7-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7d9e7-108">EXAMPLES</span></span>

### <span data-ttu-id="7d9e7-109">Esempio 1: creare una pianificazione del processo</span><span class="sxs-lookup"><span data-stu-id="7d9e7-109">Example 1: Create a job schedule</span></span>
```
PS C:\>$Schedule = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSSchedule"
PS C:\> $Schedule.RecurrenceInterval = [TimeSpan]::FromDays(1)
PS C:\> $JobSpecification = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSJobSpecification"
PS C:\> $JobSpecification.PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation"
PS C:\> $JobSpecification.PoolInformation.PoolId = "ContosoPool06"
PS C:\> New-AzureBatchJobSchedule -Id "JobSchedule17" -Schedule $Schedule -JobSpecification $JobSpecification -BatchContext $Context
```

<span data-ttu-id="7d9e7-110">Questo esempio crea una pianificazione del processo.</span><span class="sxs-lookup"><span data-stu-id="7d9e7-110">This example creates a job schedule.</span></span>

<span data-ttu-id="7d9e7-111">I primi cinque comandi creano e modificano gli oggetti **PSSchedule** , **PSJobSpecification** e **PSPoolInformation** .</span><span class="sxs-lookup"><span data-stu-id="7d9e7-111">The first five commands create and modify **PSSchedule** , **PSJobSpecification** , and **PSPoolInformation** objects.</span></span>
<span data-ttu-id="7d9e7-112">I comandi usano il cmdlet New-Object e la sintassi di PowerShell di Azure standard.</span><span class="sxs-lookup"><span data-stu-id="7d9e7-112">The commands use the New-Object cmdlet and standard Azure PowerShell syntax.</span></span>
<span data-ttu-id="7d9e7-113">I comandi archiviano questi oggetti nelle variabili $Schedule e $JobSpecification.</span><span class="sxs-lookup"><span data-stu-id="7d9e7-113">The commands store these objects in the $Schedule and $JobSpecification variables.</span></span>

<span data-ttu-id="7d9e7-114">Il comando finale crea una pianificazione del processo con ID JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="7d9e7-114">The final command creates a job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="7d9e7-115">Questa pianificazione crea processi con un intervallo di ricorrenza di un giorno.</span><span class="sxs-lookup"><span data-stu-id="7d9e7-115">This schedule creates jobs with a recurrence interval of one day.</span></span>
<span data-ttu-id="7d9e7-116">I processi vengono eseguiti nel pool che contiene l'ID ContosoPool06, come specificato nel quinto comando.</span><span class="sxs-lookup"><span data-stu-id="7d9e7-116">The jobs run on the pool that has the ID ContosoPool06, as specified in the fifth command.</span></span>
<span data-ttu-id="7d9e7-117">Usa il cmdlet **Get-AzureRmBatchAccountKeys** per assegnare un contesto alla variabile $context.</span><span class="sxs-lookup"><span data-stu-id="7d9e7-117">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="7d9e7-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7d9e7-118">PARAMETERS</span></span>

### <span data-ttu-id="7d9e7-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="7d9e7-119">-BatchContext</span></span>
<span data-ttu-id="7d9e7-120">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="7d9e7-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="7d9e7-121">Per ottenere un oggetto **BatchAccountContext** che contiene i tasti di scelta per l'abbonamento, usare il cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="7d9e7-121">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="7d9e7-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7d9e7-122">-DisplayName</span></span>
<span data-ttu-id="7d9e7-123">Specifica un nome visualizzato per la pianificazione del processo.</span><span class="sxs-lookup"><span data-stu-id="7d9e7-123">Specifies a display name for the job schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d9e7-124">-ID</span><span class="sxs-lookup"><span data-stu-id="7d9e7-124">-Id</span></span>
<span data-ttu-id="7d9e7-125">Specifica l'ID della pianificazione del processo creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d9e7-125">Specifies the ID of the job schedule that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d9e7-126">-JobSpecification</span><span class="sxs-lookup"><span data-stu-id="7d9e7-126">-JobSpecification</span></span>
<span data-ttu-id="7d9e7-127">Specifica i dettagli dei processi inclusi in questo cmdlet nella pianificazione del processo.</span><span class="sxs-lookup"><span data-stu-id="7d9e7-127">Specifies the details of the jobs that this cmdlet includes in the job schedule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d9e7-128">-Metadata</span><span class="sxs-lookup"><span data-stu-id="7d9e7-128">-Metadata</span></span>
<span data-ttu-id="7d9e7-129">Specifica i metadati, come coppie chiave/valore, da aggiungere alla pianificazione del processo.</span><span class="sxs-lookup"><span data-stu-id="7d9e7-129">Specifies metadata, as key/value pairs, to add to the job schedule.</span></span>
<span data-ttu-id="7d9e7-130">La chiave è il nome dei metadati.</span><span class="sxs-lookup"><span data-stu-id="7d9e7-130">The key is the metadata name.</span></span>
<span data-ttu-id="7d9e7-131">Il valore è il valore Metadata.</span><span class="sxs-lookup"><span data-stu-id="7d9e7-131">The value is the metadata value.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d9e7-132">-Programmazione</span><span class="sxs-lookup"><span data-stu-id="7d9e7-132">-Schedule</span></span>
<span data-ttu-id="7d9e7-133">Specifica la programmazione che determina quando creare processi.</span><span class="sxs-lookup"><span data-stu-id="7d9e7-133">Specifies the schedule that determines when to create jobs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSSchedule
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d9e7-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d9e7-134">-DefaultProfile</span></span>
<span data-ttu-id="7d9e7-135">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7d9e7-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d9e7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d9e7-136">CommonParameters</span></span>
<span data-ttu-id="7d9e7-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d9e7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d9e7-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d9e7-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d9e7-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7d9e7-139">INPUTS</span></span>

### <span data-ttu-id="7d9e7-140">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="7d9e7-140">BatchAccountContext</span></span>
<span data-ttu-id="7d9e7-141">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="7d9e7-141">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="7d9e7-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7d9e7-142">OUTPUTS</span></span>

## <span data-ttu-id="7d9e7-143">Note</span><span class="sxs-lookup"><span data-stu-id="7d9e7-143">NOTES</span></span>

## <span data-ttu-id="7d9e7-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7d9e7-144">RELATED LINKS</span></span>

[<span data-ttu-id="7d9e7-145">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="7d9e7-145">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="7d9e7-146">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="7d9e7-146">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="7d9e7-147">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="7d9e7-147">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="7d9e7-148">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="7d9e7-148">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="7d9e7-149">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="7d9e7-149">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="7d9e7-150">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="7d9e7-150">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="7d9e7-151">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="7d9e7-151">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


