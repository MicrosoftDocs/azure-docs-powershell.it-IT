---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 2B4BFDDA-9721-42E6-84E1-A209CB782954
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchTask.md
ms.openlocfilehash: dd8825be6491b0a0c8c8589f77180b38f9f230d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517052"
---
# <span data-ttu-id="820fc-101">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="820fc-101">New-AzureBatchTask</span></span>

## <span data-ttu-id="820fc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="820fc-102">SYNOPSIS</span></span>
<span data-ttu-id="820fc-103">Crea un'attività batch in un processo.</span><span class="sxs-lookup"><span data-stu-id="820fc-103">Creates a Batch task under a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="820fc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="820fc-104">SYNTAX</span></span>

### <span data-ttu-id="820fc-105">JobId_Single (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="820fc-105">JobId_Single (Default)</span></span>
```
New-AzureBatchTask -JobId <String> -Id <String> [-DisplayName <String>] [-CommandLine <String>]
 [-ResourceFiles <IDictionary>] [-EnvironmentSettings <IDictionary>] [-RunElevated]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-ExitConditions <PSExitConditions>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="820fc-106">JobId_Bulk</span><span class="sxs-lookup"><span data-stu-id="820fc-106">JobId_Bulk</span></span>
```
New-AzureBatchTask -JobId <String> [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="820fc-107">JobObject_Bulk</span><span class="sxs-lookup"><span data-stu-id="820fc-107">JobObject_Bulk</span></span>
```
New-AzureBatchTask [-Job <PSCloudJob>] [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="820fc-108">JobObject_Single</span><span class="sxs-lookup"><span data-stu-id="820fc-108">JobObject_Single</span></span>
```
New-AzureBatchTask [-Job <PSCloudJob>] -Id <String> [-DisplayName <String>] [-CommandLine <String>]
 [-ResourceFiles <IDictionary>] [-EnvironmentSettings <IDictionary>] [-RunElevated]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-ExitConditions <PSExitConditions>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="820fc-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="820fc-109">DESCRIPTION</span></span>
<span data-ttu-id="820fc-110">Il cmdlet **New-AzureBatchTask** crea un'attività batch di Azure sotto il processo specificato dal parametro *JobID* o dal parametro *Job* .</span><span class="sxs-lookup"><span data-stu-id="820fc-110">The **New-AzureBatchTask** cmdlet creates an Azure Batch task under the job specified by the *JobId* parameter or the *Job* parameter.</span></span>

## <span data-ttu-id="820fc-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="820fc-111">EXAMPLES</span></span>

### <span data-ttu-id="820fc-112">Esempio 1: creare un'attività batch</span><span class="sxs-lookup"><span data-stu-id="820fc-112">Example 1: Create a Batch task</span></span>
```
PS C:\>New-AzureBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
```

<span data-ttu-id="820fc-113">Questo comando crea un'attività che contiene l'ID Task23 sotto il processo con ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="820fc-113">This command creates a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="820fc-114">L'attività esegue il comando specificato.</span><span class="sxs-lookup"><span data-stu-id="820fc-114">The task runs the specified command.</span></span>
<span data-ttu-id="820fc-115">Usa il cmdlet **Get-AzureRmBatchAccountKeys** per assegnare un contesto alla variabile $context.</span><span class="sxs-lookup"><span data-stu-id="820fc-115">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="820fc-116">Esempio 2: creare un'attività batch</span><span class="sxs-lookup"><span data-stu-id="820fc-116">Example 2: Create a Batch task</span></span>
```
PS C:\>Get-AzureBatchJob -Id "Job-000001" -BatchContext $Context | New-AzureBatchTask -Id "Task26" -CommandLine "cmd /c echo hello > newFile.txt" -RunElevated -BatchContext $Context
```

<span data-ttu-id="820fc-117">Questo comando ottiene il processo batch con ID Job-000001 usando il cmdlet **Get-AzureBatchJob** .</span><span class="sxs-lookup"><span data-stu-id="820fc-117">This command gets the Batch job that has the ID Job-000001 by using the **Get-AzureBatchJob** cmdlet.</span></span>
<span data-ttu-id="820fc-118">Il comando passa il processo al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="820fc-118">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="820fc-119">Il comando crea un'attività che contiene l'ID Task26 in tale processo.</span><span class="sxs-lookup"><span data-stu-id="820fc-119">The command creates a task that has the ID Task26 under that job.</span></span>
<span data-ttu-id="820fc-120">L'attività esegue il comando specificato usando le autorizzazioni elevate.</span><span class="sxs-lookup"><span data-stu-id="820fc-120">The task runs the specified command by using elevated permissions.</span></span>

### <span data-ttu-id="820fc-121">Esempio 3: aggiungere una raccolta di attività al processo specificato tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="820fc-121">Example 3: Add a collection of tasks to the specified job by using the pipeline</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> Get-AzureBatchJob -Id "Job-000001" -BatchContext $Context | New-AzureBatchTask -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="820fc-122">Il primo comando crea un riferimento a un oggetto alle chiavi dell'account per l'account batch denominato ContosoBatchAccount tramite **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="820fc-122">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="820fc-123">Il comando Archivia il riferimento all'oggetto nella variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="820fc-123">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="820fc-124">I due comandi successivi creano oggetti **PSCloudTask** usando il cmdlet New-Object.</span><span class="sxs-lookup"><span data-stu-id="820fc-124">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="820fc-125">I comandi archiviano le attività nelle variabili $Task 01 e $Task 02.</span><span class="sxs-lookup"><span data-stu-id="820fc-125">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>

<span data-ttu-id="820fc-126">Il comando finale ottiene il processo batch con ID Job-000001 tramite **Get-AzureBatchJob**.</span><span class="sxs-lookup"><span data-stu-id="820fc-126">The final command gets the Batch job that has the ID Job-000001 by using **Get-AzureBatchJob**.</span></span>
<span data-ttu-id="820fc-127">Quindi il comando passa il processo al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="820fc-127">Then the command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="820fc-128">Il comando aggiunge una raccolta di attività in tale processo.</span><span class="sxs-lookup"><span data-stu-id="820fc-128">The command adds a collection of tasks under that job.</span></span>
<span data-ttu-id="820fc-129">Il comando usa il contesto archiviato in $Context.</span><span class="sxs-lookup"><span data-stu-id="820fc-129">The command uses the context stored in $Context.</span></span>

### <span data-ttu-id="820fc-130">Esempio 4: aggiungere una raccolta di attività al processo specificato</span><span class="sxs-lookup"><span data-stu-id="820fc-130">Example 4: Add a collection of tasks to the specified job</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> New-AzureBatchTask -JobId "Job-000001" -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="820fc-131">Il primo comando crea un riferimento a un oggetto alle chiavi dell'account per l'account batch denominato ContosoBatchAccount tramite **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="820fc-131">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="820fc-132">Il comando Archivia il riferimento all'oggetto nella variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="820fc-132">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="820fc-133">I due comandi successivi creano oggetti **PSCloudTask** usando il cmdlet New-Object.</span><span class="sxs-lookup"><span data-stu-id="820fc-133">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="820fc-134">I comandi archiviano le attività nelle variabili $Task 01 e $Task 02.</span><span class="sxs-lookup"><span data-stu-id="820fc-134">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>

<span data-ttu-id="820fc-135">Il comando finale aggiunge le attività archiviate in $Task 01 e $Task 02 sotto il processo con ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="820fc-135">The final command adds the tasks stored in $Task01 and $Task02 under the job that has the ID Job-000001.</span></span>

## <span data-ttu-id="820fc-136">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="820fc-136">PARAMETERS</span></span>

### <span data-ttu-id="820fc-137">-AffinityInformation</span><span class="sxs-lookup"><span data-stu-id="820fc-137">-AffinityInformation</span></span>
<span data-ttu-id="820fc-138">Specifica un suggerimento per la località usato dal servizio batch per selezionare un nodo in cui eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="820fc-138">Specifies a locality hint that the Batch service uses to select a node on which to run the task.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSAffinityInformation
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="820fc-139">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="820fc-139">-ApplicationPackageReferences</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSApplicationPackageReference[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="820fc-140">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="820fc-140">-BatchContext</span></span>
<span data-ttu-id="820fc-141">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="820fc-141">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="820fc-142">Per ottenere un oggetto **BatchAccountContext** che contiene i tasti di scelta per l'abbonamento, usare il cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="820fc-142">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="820fc-143">-Riga di comando</span><span class="sxs-lookup"><span data-stu-id="820fc-143">-CommandLine</span></span>
<span data-ttu-id="820fc-144">Specifica la riga di comando per l'attività.</span><span class="sxs-lookup"><span data-stu-id="820fc-144">Specifies the command line for the task.</span></span>

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="820fc-145">-Vincoli</span><span class="sxs-lookup"><span data-stu-id="820fc-145">-Constraints</span></span>
<span data-ttu-id="820fc-146">Specifica i vincoli di esecuzione che si applicano a questa attività.</span><span class="sxs-lookup"><span data-stu-id="820fc-146">Specifies the execution constraints that apply to this task.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="820fc-147">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="820fc-147">-DependsOn</span></span>
<span data-ttu-id="820fc-148">Specifica che l'attività dipende da altre attività.</span><span class="sxs-lookup"><span data-stu-id="820fc-148">Specifies that the task depends on other tasks.</span></span>
<span data-ttu-id="820fc-149">L'attività non verrà pianificata finché tutte le attività dipendenti non verranno completate correttamente.</span><span class="sxs-lookup"><span data-stu-id="820fc-149">The task will not be scheduled until all depended-on tasks have completed successfully.</span></span>

```yaml
Type: Microsoft.Azure.Batch.TaskDependencies
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="820fc-150">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="820fc-150">-DisplayName</span></span>
<span data-ttu-id="820fc-151">Specifica il nome visualizzato dell'attività.</span><span class="sxs-lookup"><span data-stu-id="820fc-151">Specifies the display name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="820fc-152">-EnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="820fc-152">-EnvironmentSettings</span></span>
<span data-ttu-id="820fc-153">Specifica le impostazioni di ambiente, come coppie chiave/valore, che questo cmdlet aggiunge all'attività.</span><span class="sxs-lookup"><span data-stu-id="820fc-153">Specifies the environment settings, as key/value pairs, that this cmdlet adds to the task.</span></span>
<span data-ttu-id="820fc-154">La chiave è il nome dell'impostazione dell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="820fc-154">The key is the environment setting name.</span></span>
<span data-ttu-id="820fc-155">Il valore è l'impostazione dell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="820fc-155">The value is the environment setting.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="820fc-156">-ExitConditions</span><span class="sxs-lookup"><span data-stu-id="820fc-156">-ExitConditions</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSExitConditions
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="820fc-157">-ID</span><span class="sxs-lookup"><span data-stu-id="820fc-157">-Id</span></span>
<span data-ttu-id="820fc-158">Specifica l'ID dell'attività.</span><span class="sxs-lookup"><span data-stu-id="820fc-158">Specifies the ID of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="820fc-159">-Job</span><span class="sxs-lookup"><span data-stu-id="820fc-159">-Job</span></span>
<span data-ttu-id="820fc-160">Specifica il processo in cui questo cmdlet crea l'attività.</span><span class="sxs-lookup"><span data-stu-id="820fc-160">Specifies the job under which this cmdlet creates the task.</span></span>
<span data-ttu-id="820fc-161">Per ottenere un oggetto **PSCloudJob** , usa il cmdlet Get-AzureBatchJob.</span><span class="sxs-lookup"><span data-stu-id="820fc-161">To obtain a **PSCloudJob** object, use the Get-AzureBatchJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: JobObject_Bulk, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="820fc-162">-JobId</span><span class="sxs-lookup"><span data-stu-id="820fc-162">-JobId</span></span>
<span data-ttu-id="820fc-163">Specifica l'ID del processo in cui questo cmdlet crea l'attività.</span><span class="sxs-lookup"><span data-stu-id="820fc-163">Specifies the ID of the job under which this cmdlet creates the task.</span></span>

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobId_Bulk
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="820fc-164">-MultiInstanceSettings</span><span class="sxs-lookup"><span data-stu-id="820fc-164">-MultiInstanceSettings</span></span>
<span data-ttu-id="820fc-165">Specifica informazioni su come eseguire un'attività a più istanze.</span><span class="sxs-lookup"><span data-stu-id="820fc-165">Specifies information about how to run a multi-instance task.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="820fc-166">-ResourceFiles</span><span class="sxs-lookup"><span data-stu-id="820fc-166">-ResourceFiles</span></span>
<span data-ttu-id="820fc-167">Specifica i file di risorse, come coppie chiave/valore, che l'attività richiede.</span><span class="sxs-lookup"><span data-stu-id="820fc-167">Specifies resource files, as key/value pairs, that the task requires.</span></span>
<span data-ttu-id="820fc-168">La chiave è il percorso del file di risorse.</span><span class="sxs-lookup"><span data-stu-id="820fc-168">The key is the resource file path.</span></span>
<span data-ttu-id="820fc-169">Il valore è l'origine BLOB del file di risorse.</span><span class="sxs-lookup"><span data-stu-id="820fc-169">The value is the resource file blob source.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="820fc-170">-RunElevated</span><span class="sxs-lookup"><span data-stu-id="820fc-170">-RunElevated</span></span>
<span data-ttu-id="820fc-171">Indica che il processo dell'attività viene eseguito con privilegi di amministratore.</span><span class="sxs-lookup"><span data-stu-id="820fc-171">Indicates that the task process runs with administrator privileges.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="820fc-172">-Attività</span><span class="sxs-lookup"><span data-stu-id="820fc-172">-Tasks</span></span>
<span data-ttu-id="820fc-173">Specifica la raccolta di attività da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="820fc-173">Specifies the collection of tasks to be added.</span></span>
<span data-ttu-id="820fc-174">Ogni attività deve avere un ID univoco.</span><span class="sxs-lookup"><span data-stu-id="820fc-174">Each task must have a unique ID.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask[]
Parameter Sets: JobId_Bulk, JobObject_Bulk
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="820fc-175">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="820fc-175">-DefaultProfile</span></span>
<span data-ttu-id="820fc-176">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="820fc-176">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="820fc-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="820fc-177">CommonParameters</span></span>
<span data-ttu-id="820fc-178">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="820fc-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="820fc-179">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="820fc-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="820fc-180">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="820fc-180">INPUTS</span></span>

### <span data-ttu-id="820fc-181">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="820fc-181">BatchAccountContext</span></span>
<span data-ttu-id="820fc-182">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="820fc-182">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="820fc-183">PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="820fc-183">PSCloudJob</span></span>
<span data-ttu-id="820fc-184">Il parametro "Job" accetta il valore di tipo "PSCloudJob" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="820fc-184">Parameter 'Job' accepts value of type 'PSCloudJob' from the pipeline</span></span>

## <span data-ttu-id="820fc-185">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="820fc-185">OUTPUTS</span></span>

## <span data-ttu-id="820fc-186">Note</span><span class="sxs-lookup"><span data-stu-id="820fc-186">NOTES</span></span>

## <span data-ttu-id="820fc-187">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="820fc-187">RELATED LINKS</span></span>

[<span data-ttu-id="820fc-188">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="820fc-188">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="820fc-189">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="820fc-189">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="820fc-190">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="820fc-190">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="820fc-191">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="820fc-191">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="820fc-192">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="820fc-192">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="820fc-193">Stop-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="820fc-193">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="820fc-194">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="820fc-194">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


