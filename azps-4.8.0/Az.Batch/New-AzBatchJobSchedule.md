---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 87E7FA51-427E-4DB8-A6A2-D8638FD3DB8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJobSchedule.md
ms.openlocfilehash: ab1293bf147424bb9a7315cb541b9bf22fe4a357
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032658"
---
# <span data-ttu-id="4573f-101">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="4573f-101">New-AzBatchJobSchedule</span></span>

## <span data-ttu-id="4573f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4573f-102">SYNOPSIS</span></span>
<span data-ttu-id="4573f-103">Crea una pianificazione del processo nel servizio batch.</span><span class="sxs-lookup"><span data-stu-id="4573f-103">Creates a job schedule in the Batch service.</span></span>

## <span data-ttu-id="4573f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4573f-104">SYNTAX</span></span>

```
New-AzBatchJobSchedule [-Id] <String> [-DisplayName <String>] -Schedule <PSSchedule>
 -JobSpecification <PSJobSpecification> [-Metadata <IDictionary>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4573f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4573f-105">DESCRIPTION</span></span>
<span data-ttu-id="4573f-106">Il cmdlet **New-AzBatchJobSchedule** crea una pianificazione del processo nel servizio batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="4573f-106">The **New-AzBatchJobSchedule** cmdlet creates a job schedule in the Azure Batch service.</span></span>
<span data-ttu-id="4573f-107">Il parametro *BatchAccountContext* specifica l'account in cui questo cmdlet crea la pianificazione.</span><span class="sxs-lookup"><span data-stu-id="4573f-107">The *BatchAccountContext* parameter specifies the account in which this cmdlet creates the schedule.</span></span>

## <span data-ttu-id="4573f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4573f-108">EXAMPLES</span></span>

### <span data-ttu-id="4573f-109">Esempio 1: creare una pianificazione del processo</span><span class="sxs-lookup"><span data-stu-id="4573f-109">Example 1: Create a job schedule</span></span>
```
PS C:\>$Schedule = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSSchedule"
PS C:\> $Schedule.RecurrenceInterval = [TimeSpan]::FromDays(1)
PS C:\> $JobSpecification = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSJobSpecification"
PS C:\> $JobSpecification.PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation"
PS C:\> $JobSpecification.PoolInformation.PoolId = "ContosoPool06"
PS C:\> New-AzBatchJobSchedule -Id "JobSchedule17" -Schedule $Schedule -JobSpecification $JobSpecification -BatchContext $Context
```

<span data-ttu-id="4573f-110">Questo esempio crea una pianificazione del processo.</span><span class="sxs-lookup"><span data-stu-id="4573f-110">This example creates a job schedule.</span></span>
<span data-ttu-id="4573f-111">I primi cinque comandi creano e modificano gli oggetti **PSSchedule** , **PSJobSpecification** e **PSPoolInformation** .</span><span class="sxs-lookup"><span data-stu-id="4573f-111">The first five commands create and modify **PSSchedule** , **PSJobSpecification** , and **PSPoolInformation** objects.</span></span>
<span data-ttu-id="4573f-112">I comandi usano il cmdlet New-Object e la sintassi di PowerShell di Azure standard.</span><span class="sxs-lookup"><span data-stu-id="4573f-112">The commands use the New-Object cmdlet and standard Azure PowerShell syntax.</span></span>
<span data-ttu-id="4573f-113">I comandi archiviano questi oggetti nelle variabili $Schedule e $JobSpecification.</span><span class="sxs-lookup"><span data-stu-id="4573f-113">The commands store these objects in the $Schedule and $JobSpecification variables.</span></span>
<span data-ttu-id="4573f-114">Il comando finale crea una pianificazione del processo con ID JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="4573f-114">The final command creates a job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="4573f-115">Questa pianificazione crea processi con un intervallo di ricorrenza di un giorno.</span><span class="sxs-lookup"><span data-stu-id="4573f-115">This schedule creates jobs with a recurrence interval of one day.</span></span>
<span data-ttu-id="4573f-116">I processi vengono eseguiti nel pool che contiene l'ID ContosoPool06, come specificato nel quinto comando.</span><span class="sxs-lookup"><span data-stu-id="4573f-116">The jobs run on the pool that has the ID ContosoPool06, as specified in the fifth command.</span></span>
<span data-ttu-id="4573f-117">Usa il cmdlet **Get-AzBatchAccountKey** per assegnare un contesto alla variabile $context.</span><span class="sxs-lookup"><span data-stu-id="4573f-117">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="4573f-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4573f-118">PARAMETERS</span></span>

### <span data-ttu-id="4573f-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="4573f-119">-BatchContext</span></span>
<span data-ttu-id="4573f-120">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="4573f-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="4573f-121">Se si usa il cmdlet Get-AzBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="4573f-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="4573f-122">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="4573f-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="4573f-123">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="4573f-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="4573f-124">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="4573f-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="4573f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4573f-125">-DefaultProfile</span></span>
<span data-ttu-id="4573f-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4573f-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4573f-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4573f-127">-DisplayName</span></span>
<span data-ttu-id="4573f-128">Specifica un nome visualizzato per la pianificazione del processo.</span><span class="sxs-lookup"><span data-stu-id="4573f-128">Specifies a display name for the job schedule.</span></span>

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

### <span data-ttu-id="4573f-129">-ID</span><span class="sxs-lookup"><span data-stu-id="4573f-129">-Id</span></span>
<span data-ttu-id="4573f-130">Specifica l'ID della pianificazione del processo creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4573f-130">Specifies the ID of the job schedule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="4573f-131">-JobSpecification</span><span class="sxs-lookup"><span data-stu-id="4573f-131">-JobSpecification</span></span>
<span data-ttu-id="4573f-132">Specifica i dettagli dei processi inclusi in questo cmdlet nella pianificazione del processo.</span><span class="sxs-lookup"><span data-stu-id="4573f-132">Specifies the details of the jobs that this cmdlet includes in the job schedule.</span></span>

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

### <span data-ttu-id="4573f-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="4573f-133">-Metadata</span></span>
<span data-ttu-id="4573f-134">Specifica i metadati, come coppie chiave/valore, da aggiungere alla pianificazione del processo.</span><span class="sxs-lookup"><span data-stu-id="4573f-134">Specifies metadata, as key/value pairs, to add to the job schedule.</span></span>
<span data-ttu-id="4573f-135">La chiave è il nome dei metadati.</span><span class="sxs-lookup"><span data-stu-id="4573f-135">The key is the metadata name.</span></span>
<span data-ttu-id="4573f-136">Il valore è il valore Metadata.</span><span class="sxs-lookup"><span data-stu-id="4573f-136">The value is the metadata value.</span></span>

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

### <span data-ttu-id="4573f-137">-Programmazione</span><span class="sxs-lookup"><span data-stu-id="4573f-137">-Schedule</span></span>
<span data-ttu-id="4573f-138">Specifica la programmazione che determina quando creare processi.</span><span class="sxs-lookup"><span data-stu-id="4573f-138">Specifies the schedule that determines when to create jobs.</span></span>

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

### <span data-ttu-id="4573f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4573f-139">CommonParameters</span></span>
<span data-ttu-id="4573f-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4573f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4573f-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4573f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4573f-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4573f-142">INPUTS</span></span>

### <span data-ttu-id="4573f-143">System. String</span><span class="sxs-lookup"><span data-stu-id="4573f-143">System.String</span></span>

### <span data-ttu-id="4573f-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4573f-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="4573f-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4573f-145">OUTPUTS</span></span>

### <span data-ttu-id="4573f-146">System. void</span><span class="sxs-lookup"><span data-stu-id="4573f-146">System.Void</span></span>

## <span data-ttu-id="4573f-147">Note</span><span class="sxs-lookup"><span data-stu-id="4573f-147">NOTES</span></span>

## <span data-ttu-id="4573f-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4573f-148">RELATED LINKS</span></span>

[<span data-ttu-id="4573f-149">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="4573f-149">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="4573f-150">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="4573f-150">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="4573f-151">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="4573f-151">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="4573f-152">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="4573f-152">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="4573f-153">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="4573f-153">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="4573f-154">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="4573f-154">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="4573f-155">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="4573f-155">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
