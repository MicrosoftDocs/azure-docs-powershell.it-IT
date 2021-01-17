---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2B4BFDDA-9721-42E6-84E1-A209CB782954
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchTask.md
ms.openlocfilehash: 043e7bf24ce994edd0ce5621d2de8b17616d43f0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361294"
---
# <span data-ttu-id="cd9b2-101">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="cd9b2-101">New-AzBatchTask</span></span>

## <span data-ttu-id="cd9b2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cd9b2-102">SYNOPSIS</span></span>
<span data-ttu-id="cd9b2-103">Crea un'attività batch in un processo.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-103">Creates a Batch task under a job.</span></span>

## <span data-ttu-id="cd9b2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cd9b2-104">SYNTAX</span></span>

### <span data-ttu-id="cd9b2-105">JobId_Single (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cd9b2-105">JobId_Single (Default)</span></span>
```
New-AzBatchTask -JobId <String> -Id <String> [-DisplayName <String>] -CommandLine <String>
 [-ResourceFiles <PSResourceFile[]>] [-EnvironmentSettings <IDictionary>]
 [-AuthenticationTokenSettings <PSAuthenticationTokenSettings>] [-UserIdentity <PSUserIdentity>]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-OutputFile <PSOutputFile[]>]
 [-ExitConditions <PSExitConditions>] [-ContainerSettings <PSTaskContainerSettings>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd9b2-106">JobId_Bulk</span><span class="sxs-lookup"><span data-stu-id="cd9b2-106">JobId_Bulk</span></span>
```
New-AzBatchTask -JobId <String> [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd9b2-107">JobObject_Bulk</span><span class="sxs-lookup"><span data-stu-id="cd9b2-107">JobObject_Bulk</span></span>
```
New-AzBatchTask [-Job <PSCloudJob>] [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd9b2-108">JobObject_Single</span><span class="sxs-lookup"><span data-stu-id="cd9b2-108">JobObject_Single</span></span>
```
New-AzBatchTask [-Job <PSCloudJob>] -Id <String> [-DisplayName <String>] -CommandLine <String>
 [-ResourceFiles <PSResourceFile[]>] [-EnvironmentSettings <IDictionary>]
 [-AuthenticationTokenSettings <PSAuthenticationTokenSettings>] [-UserIdentity <PSUserIdentity>]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-OutputFile <PSOutputFile[]>]
 [-ExitConditions <PSExitConditions>] [-ContainerSettings <PSTaskContainerSettings>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd9b2-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd9b2-109">DESCRIPTION</span></span>
<span data-ttu-id="cd9b2-110">Il cmdlet **New-AzBatchTask** crea un'attività batch di Azure sotto il processo specificato dal parametro *JobID* o dal parametro *Job* .</span><span class="sxs-lookup"><span data-stu-id="cd9b2-110">The **New-AzBatchTask** cmdlet creates an Azure Batch task under the job specified by the *JobId* parameter or the *Job* parameter.</span></span>

## <span data-ttu-id="cd9b2-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cd9b2-111">EXAMPLES</span></span>

### <span data-ttu-id="cd9b2-112">Esempio 1: creare un'attività batch</span><span class="sxs-lookup"><span data-stu-id="cd9b2-112">Example 1: Create a Batch task</span></span>
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
```

<span data-ttu-id="cd9b2-113">Questo comando crea un'attività che contiene l'ID Task23 sotto il processo con ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-113">This command creates a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="cd9b2-114">L'attività esegue il comando specificato.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-114">The task runs the specified command.</span></span>
<span data-ttu-id="cd9b2-115">Usa il cmdlet **Get-AzBatchAccountKey** per assegnare un contesto alla variabile $context.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-115">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="cd9b2-116">Esempio 2: creare un'attività batch</span><span class="sxs-lookup"><span data-stu-id="cd9b2-116">Example 2: Create a Batch task</span></span>
```
PS C:\> $autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
PS C:\> $userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
PS C:\>Get-AzBatchJob -Id "Job-000001" -BatchContext $Context | New-AzBatchTask -Id "Task26" -CommandLine "cmd /c echo hello > newFile.txt" -UserIdentity $userIdentity -BatchContext $Context
```

<span data-ttu-id="cd9b2-117">Questo comando ottiene il processo batch con ID Job-000001 usando il cmdlet **Get-AzBatchJob** .</span><span class="sxs-lookup"><span data-stu-id="cd9b2-117">This command gets the Batch job that has the ID Job-000001 by using the **Get-AzBatchJob** cmdlet.</span></span>
<span data-ttu-id="cd9b2-118">Il comando passa il processo al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-118">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="cd9b2-119">Il comando crea un'attività che contiene l'ID Task26 in tale processo.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-119">The command creates a task that has the ID Task26 under that job.</span></span>
<span data-ttu-id="cd9b2-120">L'attività esegue il comando specificato usando le autorizzazioni elevate.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-120">The task runs the specified command by using elevated permissions.</span></span>

### <span data-ttu-id="cd9b2-121">Esempio 3: aggiungere una raccolta di attività al processo specificato tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="cd9b2-121">Example 3: Add a collection of tasks to the specified job by using the pipeline</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> Get-AzBatchJob -Id "Job-000001" -BatchContext $Context | New-AzBatchTask -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="cd9b2-122">Il primo comando crea un riferimento a un oggetto alle chiavi dell'account per l'account batch denominato ContosoBatchAccount tramite **Get-AzBatchAccountKey**.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-122">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="cd9b2-123">Il comando Archivia il riferimento all'oggetto nella variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-123">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="cd9b2-124">I due comandi successivi creano oggetti **PSCloudTask** usando il cmdlet New-Object.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-124">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="cd9b2-125">I comandi archiviano le attività nelle variabili $Task 01 e $Task 02.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-125">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>
<span data-ttu-id="cd9b2-126">Il comando finale ottiene il processo batch con ID Job-000001 tramite **Get-AzBatchJob**.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-126">The final command gets the Batch job that has the ID Job-000001 by using **Get-AzBatchJob**.</span></span>
<span data-ttu-id="cd9b2-127">Quindi il comando passa il processo al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-127">Then the command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="cd9b2-128">Il comando aggiunge una raccolta di attività in tale processo.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-128">The command adds a collection of tasks under that job.</span></span>
<span data-ttu-id="cd9b2-129">Il comando usa il contesto archiviato in $Context.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-129">The command uses the context stored in $Context.</span></span>

### <span data-ttu-id="cd9b2-130">Esempio 4: aggiungere una raccolta di attività al processo specificato</span><span class="sxs-lookup"><span data-stu-id="cd9b2-130">Example 4: Add a collection of tasks to the specified job</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> New-AzBatchTask -JobId "Job-000001" -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="cd9b2-131">Il primo comando crea un riferimento a un oggetto alle chiavi dell'account per l'account batch denominato ContosoBatchAccount tramite **Get-AzBatchAccountKey**.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-131">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="cd9b2-132">Il comando Archivia il riferimento all'oggetto nella variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-132">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="cd9b2-133">I due comandi successivi creano oggetti **PSCloudTask** usando il cmdlet New-Object.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-133">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="cd9b2-134">I comandi archiviano le attività nelle variabili $Task 01 e $Task 02.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-134">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>
<span data-ttu-id="cd9b2-135">Il comando finale aggiunge le attività archiviate in $Task 01 e $Task 02 sotto il processo con ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-135">The final command adds the tasks stored in $Task01 and $Task02 under the job that has the ID Job-000001.</span></span>

### <span data-ttu-id="cd9b2-136">Esempio 5: aggiungere un'attività con i file di output</span><span class="sxs-lookup"><span data-stu-id="cd9b2-136">Example 5: Add a task with output files</span></span>
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
PS C:\>$blobContainerDestination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileBlobContainerDestination "https://myaccount.blob.core.windows.net/sascontainer?sv=2015-04-05&st=2015-04-29T22%3A18%3A26Z&se=2015-04-30T02%3A23%3A26Z&sr=b&sp=rw&spr=https&sig=Z%2FRHIX5Xcg0Mq2rqI3OlWTjEg2tYkboXr1P9ZUXDtkk%3D"
PS C:\>$destination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileDestination $blobContainerDestination
PS C:\>$uploadOptions = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileUploadOptions "TaskSuccess"
PS C:\>$outputFile = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFile "*.txt", $blobContainerDestination, $uploadOptions

PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -OutputFile $outputFile -BatchContext $Context
```

### <span data-ttu-id="cd9b2-137">Esempio 6: aggiungere un'attività con le impostazioni del token di autenticazione</span><span class="sxs-lookup"><span data-stu-id="cd9b2-137">Example 6: Add a task with authentication token settings</span></span>
```
PS C:\>$authSettings = New-Object Microsoft.Azure.Commands.Batch.Models.PSAuthenticationTokenSettings
PS C:\>$authSettings.Access = "Job"
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -AuthenticationTokenSettings $authSettings -BatchContext $Context
```

### <span data-ttu-id="cd9b2-138">Esempio 7: aggiungere un'attività che viene eseguita in un contenitore</span><span class="sxs-lookup"><span data-stu-id="cd9b2-138">Example 7: Add a task which runs in a container</span></span>
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ContainerSettings New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskContainerSettings "containerImageName"
```

## <span data-ttu-id="cd9b2-139">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cd9b2-139">PARAMETERS</span></span>

### <span data-ttu-id="cd9b2-140">-AffinityInformation</span><span class="sxs-lookup"><span data-stu-id="cd9b2-140">-AffinityInformation</span></span>
<span data-ttu-id="cd9b2-141">Specifica un suggerimento per la località usato dal servizio batch per selezionare un nodo in cui eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-141">Specifies a locality hint that the Batch service uses to select a node on which to run the task.</span></span>

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

### <span data-ttu-id="cd9b2-142">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="cd9b2-142">-ApplicationPackageReferences</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSApplicationPackageReference[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases: ApplicationPackageReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd9b2-143">-AuthenticationTokenSettings</span><span class="sxs-lookup"><span data-stu-id="cd9b2-143">-AuthenticationTokenSettings</span></span>
<span data-ttu-id="cd9b2-144">Le impostazioni per un token di autenticazione che l'attività può usare per eseguire operazioni di servizio batch.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-144">The settings for an authentication token that the task can use to perform Batch service operations.</span></span>
<span data-ttu-id="cd9b2-145">Se è impostato, il servizio batch fornisce l'attività con un token di autenticazione che può essere usato per autenticare le operazioni del servizio batch senza richiedere un tasto di scelta dell'account.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-145">If this is set, the Batch service provides the task with an authentication token which can be used to authenticate Batch service operations without requiring an account access key.</span></span> <span data-ttu-id="cd9b2-146">Il token viene fornito tramite la variabile di ambiente AZ_BATCH_AUTHENTICATION_TOKEN.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-146">The token is provided via the AZ_BATCH_AUTHENTICATION_TOKEN environment variable.</span></span> <span data-ttu-id="cd9b2-147">Le operazioni che l'attività può eseguire usando il token dipendono dalle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-147">The operations that the task can carry out using the token depend on the settings.</span></span> <span data-ttu-id="cd9b2-148">Ad esempio, un'attività può richiedere le autorizzazioni per i processi per aggiungere altre attività al processo oppure verificare lo stato del processo o di altre attività.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-148">For example, a task can request job permissions in order to add other tasks to the job, or check the status of the job or of other tasks.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSAuthenticationTokenSettings
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd9b2-149">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="cd9b2-149">-BatchContext</span></span>
<span data-ttu-id="cd9b2-150">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-150">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="cd9b2-151">Se si usa il cmdlet Get-AzBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-151">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="cd9b2-152">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-152">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="cd9b2-153">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-153">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="cd9b2-154">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-154">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="cd9b2-155">-Riga di comando</span><span class="sxs-lookup"><span data-stu-id="cd9b2-155">-CommandLine</span></span>
<span data-ttu-id="cd9b2-156">Specifica la riga di comando per l'attività.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-156">Specifies the command line for the task.</span></span>

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

### <span data-ttu-id="cd9b2-157">-Vincoli</span><span class="sxs-lookup"><span data-stu-id="cd9b2-157">-Constraints</span></span>
<span data-ttu-id="cd9b2-158">Specifica i vincoli di esecuzione che si applicano a questa attività.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-158">Specifies the execution constraints that apply to this task.</span></span>

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

### <span data-ttu-id="cd9b2-159">-ContainerSettings</span><span class="sxs-lookup"><span data-stu-id="cd9b2-159">-ContainerSettings</span></span>
<span data-ttu-id="cd9b2-160">Impostazioni per il contenitore in cui viene eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-160">The settings for the container under which the task runs.</span></span>
<span data-ttu-id="cd9b2-161">Se il pool che eseguirà questa attività ha containerConfiguration set, anche questo deve essere impostato.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-161">If the pool that will run this task has containerConfiguration set, this must be set as well.</span></span> <span data-ttu-id="cd9b2-162">Se il pool che eseguirà l'attività non ha un set di containerConfiguration, non deve essere impostato.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-162">If the pool that will run this task doesn't have containerConfiguration set, this must not be set.</span></span> <span data-ttu-id="cd9b2-163">Quando questa operazione viene specificata, tutte le directory ricorsivamente sotto la AZ_BATCH_NODE_ROOT_DIR (la radice delle directory batch di Azure nel nodo) sono mappate nel contenitore, tutte le variabili di ambiente delle attività sono mappate nel contenitore e la riga di comando dell'attività viene eseguita nel contenitore.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-163">When this is specified, all directories recursively below the AZ_BATCH_NODE_ROOT_DIR (the root of Azure Batch directories on the node) are mapped into the container, all task environment variables are mapped into the container, and the task command line is executed in the container.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSTaskContainerSettings
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd9b2-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd9b2-164">-DefaultProfile</span></span>
<span data-ttu-id="cd9b2-165">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-165">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd9b2-166">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="cd9b2-166">-DependsOn</span></span>
<span data-ttu-id="cd9b2-167">Specifica che l'attività dipende da altre attività.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-167">Specifies that the task depends on other tasks.</span></span>
<span data-ttu-id="cd9b2-168">L'attività non verrà pianificata finché tutte le attività dipendenti non verranno completate correttamente.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-168">The task will not be scheduled until all depended-on tasks have completed successfully.</span></span>

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

### <span data-ttu-id="cd9b2-169">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="cd9b2-169">-DisplayName</span></span>
<span data-ttu-id="cd9b2-170">Specifica il nome visualizzato dell'attività.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-170">Specifies the display name of the task.</span></span>

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

### <span data-ttu-id="cd9b2-171">-EnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="cd9b2-171">-EnvironmentSettings</span></span>
<span data-ttu-id="cd9b2-172">Specifica le impostazioni di ambiente, come coppie chiave/valore, che questo cmdlet aggiunge all'attività.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-172">Specifies the environment settings, as key/value pairs, that this cmdlet adds to the task.</span></span>
<span data-ttu-id="cd9b2-173">La chiave è il nome dell'impostazione dell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-173">The key is the environment setting name.</span></span>
<span data-ttu-id="cd9b2-174">Il valore è l'impostazione dell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-174">The value is the environment setting.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: EnvironmentSetting

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd9b2-175">-ExitConditions</span><span class="sxs-lookup"><span data-stu-id="cd9b2-175">-ExitConditions</span></span>
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

### <span data-ttu-id="cd9b2-176">-ID</span><span class="sxs-lookup"><span data-stu-id="cd9b2-176">-Id</span></span>
<span data-ttu-id="cd9b2-177">Specifica l'ID dell'attività.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-177">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="cd9b2-178">-Job</span><span class="sxs-lookup"><span data-stu-id="cd9b2-178">-Job</span></span>
<span data-ttu-id="cd9b2-179">Specifica il processo in cui questo cmdlet crea l'attività.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-179">Specifies the job under which this cmdlet creates the task.</span></span>
<span data-ttu-id="cd9b2-180">Per ottenere un oggetto **PSCloudJob** , usa il cmdlet Get-AzBatchJob.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-180">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="cd9b2-181">-JobId</span><span class="sxs-lookup"><span data-stu-id="cd9b2-181">-JobId</span></span>
<span data-ttu-id="cd9b2-182">Specifica l'ID del processo in cui questo cmdlet crea l'attività.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-182">Specifies the ID of the job under which this cmdlet creates the task.</span></span>

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

### <span data-ttu-id="cd9b2-183">-MultiInstanceSettings</span><span class="sxs-lookup"><span data-stu-id="cd9b2-183">-MultiInstanceSettings</span></span>
<span data-ttu-id="cd9b2-184">Specifica informazioni su come eseguire un'attività a più istanze.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-184">Specifies information about how to run a multi-instance task.</span></span>

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

### <span data-ttu-id="cd9b2-185">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="cd9b2-185">-OutputFile</span></span>
<span data-ttu-id="cd9b2-186">Ottiene o imposta un elenco di file che il servizio batch caricherà dal nodo COMPUTE dopo l'uso della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-186">Gets or sets a list of files that the Batch service will upload from the compute node after running the command line.</span></span>
<span data-ttu-id="cd9b2-187">Per le attività a più istanze, i file verranno caricati solo dal nodo COMPUTE in cui viene eseguita l'attività principale.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-187">For multi-instance tasks, the files will only be uploaded from the compute node on which the primary task is executed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSOutputFile[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd9b2-188">-ResourceFiles</span><span class="sxs-lookup"><span data-stu-id="cd9b2-188">-ResourceFiles</span></span>
<span data-ttu-id="cd9b2-189">Specifica i file di risorse, come coppie chiave/valore, che l'attività richiede.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-189">Specifies resource files, as key/value pairs, that the task requires.</span></span>
<span data-ttu-id="cd9b2-190">La chiave è il percorso del file di risorse.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-190">The key is the resource file path.</span></span>
<span data-ttu-id="cd9b2-191">Il valore è l'origine BLOB del file di risorse.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-191">The value is the resource file blob source.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSResourceFile[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases: ResourceFile

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd9b2-192">-Attività</span><span class="sxs-lookup"><span data-stu-id="cd9b2-192">-Tasks</span></span>
<span data-ttu-id="cd9b2-193">Specifica la raccolta di attività da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-193">Specifies the collection of tasks to be added.</span></span>
<span data-ttu-id="cd9b2-194">Ogni attività deve avere un ID univoco.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-194">Each task must have a unique ID.</span></span>

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

### <span data-ttu-id="cd9b2-195">-UserIdentity</span><span class="sxs-lookup"><span data-stu-id="cd9b2-195">-UserIdentity</span></span>
<span data-ttu-id="cd9b2-196">Identità utente in cui viene eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-196">The user identity under which the task runs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSUserIdentity
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd9b2-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd9b2-197">CommonParameters</span></span>
<span data-ttu-id="cd9b2-198">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd9b2-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd9b2-199">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd9b2-199">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd9b2-200">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cd9b2-200">INPUTS</span></span>

### <span data-ttu-id="cd9b2-201">Microsoft.Azure.Commands.Batch. Models. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="cd9b2-201">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="cd9b2-202">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="cd9b2-202">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="cd9b2-203">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cd9b2-203">OUTPUTS</span></span>

### <span data-ttu-id="cd9b2-204">System. void</span><span class="sxs-lookup"><span data-stu-id="cd9b2-204">System.Void</span></span>

## <span data-ttu-id="cd9b2-205">Note</span><span class="sxs-lookup"><span data-stu-id="cd9b2-205">NOTES</span></span>

## <span data-ttu-id="cd9b2-206">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cd9b2-206">RELATED LINKS</span></span>

[<span data-ttu-id="cd9b2-207">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="cd9b2-207">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="cd9b2-208">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="cd9b2-208">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="cd9b2-209">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="cd9b2-209">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="cd9b2-210">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="cd9b2-210">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="cd9b2-211">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="cd9b2-211">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="cd9b2-212">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="cd9b2-212">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="cd9b2-213">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="cd9b2-213">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
