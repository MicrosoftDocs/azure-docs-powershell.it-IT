---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 2B4BFDDA-9721-42E6-84E1-A209CB782954
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchTask.md
ms.openlocfilehash: a081e6da07557033430033adc8ef28cb4b63da8c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511931"
---
# <span data-ttu-id="b4fa8-101">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="b4fa8-101">New-AzureBatchTask</span></span>

## <span data-ttu-id="b4fa8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b4fa8-102">SYNOPSIS</span></span>
<span data-ttu-id="b4fa8-103">Crea un'attività batch in un processo.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-103">Creates a Batch task under a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4fa8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b4fa8-104">SYNTAX</span></span>

### <span data-ttu-id="b4fa8-105">JobId_Single (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b4fa8-105">JobId_Single (Default)</span></span>
```
New-AzureBatchTask -JobId <String> -Id <String> [-DisplayName <String>] [-CommandLine <String>]
 [-ResourceFiles <IDictionary>] [-EnvironmentSettings <IDictionary>]
 [-AuthenticationTokenSettings <PSAuthenticationTokenSettings>] [-UserIdentity <PSUserIdentity>]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-OutputFile <PSOutputFile[]>]
 [-ExitConditions <PSExitConditions>] [-ContainerSettings <PSTaskContainerSettings>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4fa8-106">JobId_Bulk</span><span class="sxs-lookup"><span data-stu-id="b4fa8-106">JobId_Bulk</span></span>
```
New-AzureBatchTask -JobId <String> [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4fa8-107">JobObject_Bulk</span><span class="sxs-lookup"><span data-stu-id="b4fa8-107">JobObject_Bulk</span></span>
```
New-AzureBatchTask [-Job <PSCloudJob>] [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4fa8-108">JobObject_Single</span><span class="sxs-lookup"><span data-stu-id="b4fa8-108">JobObject_Single</span></span>
```
New-AzureBatchTask [-Job <PSCloudJob>] -Id <String> [-DisplayName <String>] [-CommandLine <String>]
 [-ResourceFiles <IDictionary>] [-EnvironmentSettings <IDictionary>]
 [-AuthenticationTokenSettings <PSAuthenticationTokenSettings>] [-UserIdentity <PSUserIdentity>]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-OutputFile <PSOutputFile[]>]
 [-ExitConditions <PSExitConditions>] [-ContainerSettings <PSTaskContainerSettings>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4fa8-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b4fa8-109">DESCRIPTION</span></span>
<span data-ttu-id="b4fa8-110">Il cmdlet **New-AzureBatchTask** crea un'attività batch di Azure sotto il processo specificato dal parametro *JobID* o dal parametro *Job* .</span><span class="sxs-lookup"><span data-stu-id="b4fa8-110">The **New-AzureBatchTask** cmdlet creates an Azure Batch task under the job specified by the *JobId* parameter or the *Job* parameter.</span></span>

## <span data-ttu-id="b4fa8-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b4fa8-111">EXAMPLES</span></span>

### <span data-ttu-id="b4fa8-112">Esempio 1: creare un'attività batch</span><span class="sxs-lookup"><span data-stu-id="b4fa8-112">Example 1: Create a Batch task</span></span>
```
PS C:\>New-AzureBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
```

<span data-ttu-id="b4fa8-113">Questo comando crea un'attività che contiene l'ID Task23 sotto il processo con ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-113">This command creates a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="b4fa8-114">L'attività esegue il comando specificato.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-114">The task runs the specified command.</span></span>
<span data-ttu-id="b4fa8-115">Usa il cmdlet **Get-AzureRmBatchAccountKeys** per assegnare un contesto alla variabile $context.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-115">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="b4fa8-116">Esempio 2: creare un'attività batch</span><span class="sxs-lookup"><span data-stu-id="b4fa8-116">Example 2: Create a Batch task</span></span>
```
PS C:\> $autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
PS C:\> $userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
PS C:\>Get-AzureBatchJob -Id "Job-000001" -BatchContext $Context | New-AzureBatchTask -Id "Task26" -CommandLine "cmd /c echo hello > newFile.txt" -UserIdentity $userIdentity -BatchContext $Context
```

<span data-ttu-id="b4fa8-117">Questo comando ottiene il processo batch con ID Job-000001 usando il cmdlet **Get-AzureBatchJob** .</span><span class="sxs-lookup"><span data-stu-id="b4fa8-117">This command gets the Batch job that has the ID Job-000001 by using the **Get-AzureBatchJob** cmdlet.</span></span>
<span data-ttu-id="b4fa8-118">Il comando passa il processo al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-118">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b4fa8-119">Il comando crea un'attività che contiene l'ID Task26 in tale processo.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-119">The command creates a task that has the ID Task26 under that job.</span></span>
<span data-ttu-id="b4fa8-120">L'attività esegue il comando specificato usando le autorizzazioni elevate.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-120">The task runs the specified command by using elevated permissions.</span></span>

### <span data-ttu-id="b4fa8-121">Esempio 3: aggiungere una raccolta di attività al processo specificato tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="b4fa8-121">Example 3: Add a collection of tasks to the specified job by using the pipeline</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> Get-AzureBatchJob -Id "Job-000001" -BatchContext $Context | New-AzureBatchTask -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="b4fa8-122">Il primo comando crea un riferimento a un oggetto alle chiavi dell'account per l'account batch denominato ContosoBatchAccount tramite **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-122">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="b4fa8-123">Il comando Archivia il riferimento all'oggetto nella variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-123">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="b4fa8-124">I due comandi successivi creano oggetti **PSCloudTask** usando il cmdlet New-Object.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-124">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="b4fa8-125">I comandi archiviano le attività nelle variabili $Task 01 e $Task 02.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-125">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>
<span data-ttu-id="b4fa8-126">Il comando finale ottiene il processo batch con ID Job-000001 tramite **Get-AzureBatchJob**.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-126">The final command gets the Batch job that has the ID Job-000001 by using **Get-AzureBatchJob**.</span></span>
<span data-ttu-id="b4fa8-127">Quindi il comando passa il processo al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-127">Then the command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b4fa8-128">Il comando aggiunge una raccolta di attività in tale processo.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-128">The command adds a collection of tasks under that job.</span></span>
<span data-ttu-id="b4fa8-129">Il comando usa il contesto archiviato in $Context.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-129">The command uses the context stored in $Context.</span></span>

### <span data-ttu-id="b4fa8-130">Esempio 4: aggiungere una raccolta di attività al processo specificato</span><span class="sxs-lookup"><span data-stu-id="b4fa8-130">Example 4: Add a collection of tasks to the specified job</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> New-AzureBatchTask -JobId "Job-000001" -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="b4fa8-131">Il primo comando crea un riferimento a un oggetto alle chiavi dell'account per l'account batch denominato ContosoBatchAccount tramite **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-131">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="b4fa8-132">Il comando Archivia il riferimento all'oggetto nella variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-132">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="b4fa8-133">I due comandi successivi creano oggetti **PSCloudTask** usando il cmdlet New-Object.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-133">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="b4fa8-134">I comandi archiviano le attività nelle variabili $Task 01 e $Task 02.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-134">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>
<span data-ttu-id="b4fa8-135">Il comando finale aggiunge le attività archiviate in $Task 01 e $Task 02 sotto il processo con ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-135">The final command adds the tasks stored in $Task01 and $Task02 under the job that has the ID Job-000001.</span></span>

### <span data-ttu-id="b4fa8-136">Esempio 5: aggiungere un'attività con i file di output</span><span class="sxs-lookup"><span data-stu-id="b4fa8-136">Example 5: Add a task with output files</span></span>
```
PS C:\>New-AzureBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
PS C:\>$blobContainerDestination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileBlobContainerDestination "https://myaccount.blob.core.windows.net/sascontainer?sv=2015-04-05&st=2015-04-29T22%3A18%3A26Z&se=2015-04-30T02%3A23%3A26Z&sr=b&sp=rw&spr=https&sig=Z%2FRHIX5Xcg0Mq2rqI3OlWTjEg2tYkboXr1P9ZUXDtkk%3D"
PS C:\>$destination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileDestination $blobContainerDestination
PS C:\>$uploadOptions = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileUploadOptions "TaskSuccess"
PS C:\>$outputFile = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFile "*.txt", $blobContainerDestination, $uploadOptions

PS C:\>New-AzureBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -OutputFile $outputFile -BatchContext $Context
```

### <span data-ttu-id="b4fa8-137">Esempio 6: aggiungere un'attività con le impostazioni del token di autenticazione</span><span class="sxs-lookup"><span data-stu-id="b4fa8-137">Example 6: Add a task with authentication token settings</span></span>
```
PS C:\>$authSettings = New-Object Microsoft.Azure.Commands.Batch.Models.PSAuthenticationTokenSettings
PS C:\>$authSettings.Access = "Job"
PS C:\>New-AzureBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -AuthenticationTokenSettings $authSettings -BatchContext $Context
```

### <span data-ttu-id="b4fa8-138">Esempio 7: aggiungere un'attività che viene eseguita in un contenitore</span><span class="sxs-lookup"><span data-stu-id="b4fa8-138">Example 7: Add a task which runs in a container</span></span>
```
PS C:\>New-AzureBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ContainerSettings New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskContainerSettings "containerImageName"
```

## <span data-ttu-id="b4fa8-139">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b4fa8-139">PARAMETERS</span></span>

### <span data-ttu-id="b4fa8-140">-AffinityInformation</span><span class="sxs-lookup"><span data-stu-id="b4fa8-140">-AffinityInformation</span></span>
<span data-ttu-id="b4fa8-141">Specifica un suggerimento per la località usato dal servizio batch per selezionare un nodo in cui eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-141">Specifies a locality hint that the Batch service uses to select a node on which to run the task.</span></span>

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

### <span data-ttu-id="b4fa8-142">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="b4fa8-142">-ApplicationPackageReferences</span></span>
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

### <span data-ttu-id="b4fa8-143">-AuthenticationTokenSettings</span><span class="sxs-lookup"><span data-stu-id="b4fa8-143">-AuthenticationTokenSettings</span></span>
<span data-ttu-id="b4fa8-144">Le impostazioni per un token di autenticazione che l'attività può usare per eseguire operazioni di servizio batch.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-144">The settings for an authentication token that the task can use to perform Batch service operations.</span></span>
<span data-ttu-id="b4fa8-145">Se è impostato, il servizio batch fornisce l'attività con un token di autenticazione che può essere usato per autenticare le operazioni del servizio batch senza richiedere un tasto di scelta dell'account.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-145">If this is set, the Batch service provides the task with an authentication token which can be used to authenticate Batch service operations without requiring an account access key.</span></span> <span data-ttu-id="b4fa8-146">Il token viene fornito tramite la variabile di ambiente AZ_BATCH_AUTHENTICATION_TOKEN.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-146">The token is provided via the AZ_BATCH_AUTHENTICATION_TOKEN environment variable.</span></span> <span data-ttu-id="b4fa8-147">Le operazioni che l'attività può eseguire usando il token dipendono dalle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-147">The operations that the task can carry out using the token depend on the settings.</span></span> <span data-ttu-id="b4fa8-148">Ad esempio, un'attività può richiedere le autorizzazioni per i processi per aggiungere altre attività al processo oppure verificare lo stato del processo o di altre attività.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-148">For example, a task can request job permissions in order to add other tasks to the job, or check the status of the job or of other tasks.</span></span>

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

### <span data-ttu-id="b4fa8-149">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b4fa8-149">-BatchContext</span></span>
<span data-ttu-id="b4fa8-150">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-150">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b4fa8-151">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-151">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b4fa8-152">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-152">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b4fa8-153">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-153">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b4fa8-154">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-154">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b4fa8-155">-Riga di comando</span><span class="sxs-lookup"><span data-stu-id="b4fa8-155">-CommandLine</span></span>
<span data-ttu-id="b4fa8-156">Specifica la riga di comando per l'attività.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-156">Specifies the command line for the task.</span></span>

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

### <span data-ttu-id="b4fa8-157">-Vincoli</span><span class="sxs-lookup"><span data-stu-id="b4fa8-157">-Constraints</span></span>
<span data-ttu-id="b4fa8-158">Specifica i vincoli di esecuzione che si applicano a questa attività.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-158">Specifies the execution constraints that apply to this task.</span></span>

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

### <span data-ttu-id="b4fa8-159">-ContainerSettings</span><span class="sxs-lookup"><span data-stu-id="b4fa8-159">-ContainerSettings</span></span>
<span data-ttu-id="b4fa8-160">Impostazioni per il contenitore in cui viene eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-160">The settings for the container under which the task runs.</span></span>
<span data-ttu-id="b4fa8-161">Se il pool che eseguirà questa attività ha containerConfiguration set, anche questo deve essere impostato.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-161">If the pool that will run this task has containerConfiguration set, this must be set as well.</span></span> <span data-ttu-id="b4fa8-162">Se il pool che eseguirà l'attività non ha un set di containerConfiguration, non deve essere impostato.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-162">If the pool that will run this task doesn't have containerConfiguration set, this must not be set.</span></span> <span data-ttu-id="b4fa8-163">Quando questa operazione viene specificata, tutte le directory ricorsivamente sotto la AZ_BATCH_NODE_ROOT_DIR (la radice delle directory batch di Azure nel nodo) sono mappate nel contenitore, tutte le variabili di ambiente delle attività sono mappate nel contenitore e la riga di comando dell'attività viene eseguita nel contenitore.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-163">When this is specified, all directories recursively below the AZ_BATCH_NODE_ROOT_DIR (the root of Azure Batch directories on the node) are mapped into the container, all task environment variables are mapped into the container, and the task command line is executed in the container.</span></span>

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

### <span data-ttu-id="b4fa8-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4fa8-164">-DefaultProfile</span></span>
<span data-ttu-id="b4fa8-165">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-165">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4fa8-166">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="b4fa8-166">-DependsOn</span></span>
<span data-ttu-id="b4fa8-167">Specifica che l'attività dipende da altre attività.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-167">Specifies that the task depends on other tasks.</span></span>
<span data-ttu-id="b4fa8-168">L'attività non verrà pianificata finché tutte le attività dipendenti non verranno completate correttamente.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-168">The task will not be scheduled until all depended-on tasks have completed successfully.</span></span>

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

### <span data-ttu-id="b4fa8-169">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b4fa8-169">-DisplayName</span></span>
<span data-ttu-id="b4fa8-170">Specifica il nome visualizzato dell'attività.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-170">Specifies the display name of the task.</span></span>

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

### <span data-ttu-id="b4fa8-171">-EnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="b4fa8-171">-EnvironmentSettings</span></span>
<span data-ttu-id="b4fa8-172">Specifica le impostazioni di ambiente, come coppie chiave/valore, che questo cmdlet aggiunge all'attività.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-172">Specifies the environment settings, as key/value pairs, that this cmdlet adds to the task.</span></span>
<span data-ttu-id="b4fa8-173">La chiave è il nome dell'impostazione dell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-173">The key is the environment setting name.</span></span>
<span data-ttu-id="b4fa8-174">Il valore è l'impostazione dell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-174">The value is the environment setting.</span></span>

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

### <span data-ttu-id="b4fa8-175">-ExitConditions</span><span class="sxs-lookup"><span data-stu-id="b4fa8-175">-ExitConditions</span></span>
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

### <span data-ttu-id="b4fa8-176">-ID</span><span class="sxs-lookup"><span data-stu-id="b4fa8-176">-Id</span></span>
<span data-ttu-id="b4fa8-177">Specifica l'ID dell'attività.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-177">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="b4fa8-178">-Job</span><span class="sxs-lookup"><span data-stu-id="b4fa8-178">-Job</span></span>
<span data-ttu-id="b4fa8-179">Specifica il processo in cui questo cmdlet crea l'attività.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-179">Specifies the job under which this cmdlet creates the task.</span></span>
<span data-ttu-id="b4fa8-180">Per ottenere un oggetto **PSCloudJob** , usa il cmdlet Get-AzureBatchJob.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-180">To obtain a **PSCloudJob** object, use the Get-AzureBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="b4fa8-181">-JobId</span><span class="sxs-lookup"><span data-stu-id="b4fa8-181">-JobId</span></span>
<span data-ttu-id="b4fa8-182">Specifica l'ID del processo in cui questo cmdlet crea l'attività.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-182">Specifies the ID of the job under which this cmdlet creates the task.</span></span>

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

### <span data-ttu-id="b4fa8-183">-MultiInstanceSettings</span><span class="sxs-lookup"><span data-stu-id="b4fa8-183">-MultiInstanceSettings</span></span>
<span data-ttu-id="b4fa8-184">Specifica informazioni su come eseguire un'attività a più istanze.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-184">Specifies information about how to run a multi-instance task.</span></span>

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

### <span data-ttu-id="b4fa8-185">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="b4fa8-185">-OutputFile</span></span>
<span data-ttu-id="b4fa8-186">Ottiene o imposta un elenco di file che il servizio batch caricherà dal nodo COMPUTE dopo l'uso della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-186">Gets or sets a list of files that the Batch service will upload from the compute node after running the command line.</span></span>
<span data-ttu-id="b4fa8-187">Per le attività a più istanze, i file verranno caricati solo dal nodo COMPUTE in cui viene eseguita l'attività principale.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-187">For multi-instance tasks, the files will only be uploaded from the compute node on which the primary task is executed.</span></span>

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

### <span data-ttu-id="b4fa8-188">-ResourceFiles</span><span class="sxs-lookup"><span data-stu-id="b4fa8-188">-ResourceFiles</span></span>
<span data-ttu-id="b4fa8-189">Specifica i file di risorse, come coppie chiave/valore, che l'attività richiede.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-189">Specifies resource files, as key/value pairs, that the task requires.</span></span>
<span data-ttu-id="b4fa8-190">La chiave è il percorso del file di risorse.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-190">The key is the resource file path.</span></span>
<span data-ttu-id="b4fa8-191">Il valore è l'origine BLOB del file di risorse.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-191">The value is the resource file blob source.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: ResourceFile

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4fa8-192">-Attività</span><span class="sxs-lookup"><span data-stu-id="b4fa8-192">-Tasks</span></span>
<span data-ttu-id="b4fa8-193">Specifica la raccolta di attività da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-193">Specifies the collection of tasks to be added.</span></span>
<span data-ttu-id="b4fa8-194">Ogni attività deve avere un ID univoco.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-194">Each task must have a unique ID.</span></span>

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

### <span data-ttu-id="b4fa8-195">-UserIdentity</span><span class="sxs-lookup"><span data-stu-id="b4fa8-195">-UserIdentity</span></span>
<span data-ttu-id="b4fa8-196">Identità utente in cui viene eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-196">The user identity under which the task runs.</span></span>

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

### <span data-ttu-id="b4fa8-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4fa8-197">CommonParameters</span></span>
<span data-ttu-id="b4fa8-198">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4fa8-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4fa8-199">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4fa8-199">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4fa8-200">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b4fa8-200">INPUTS</span></span>

### <span data-ttu-id="b4fa8-201">Microsoft.Azure.Commands.Batch. Models. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="b4fa8-201">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>
<span data-ttu-id="b4fa8-202">Parameters: Job (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b4fa8-202">Parameters: Job (ByValue)</span></span>

### <span data-ttu-id="b4fa8-203">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b4fa8-203">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="b4fa8-204">Parametri: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b4fa8-204">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="b4fa8-205">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b4fa8-205">OUTPUTS</span></span>

### <span data-ttu-id="b4fa8-206">System. void</span><span class="sxs-lookup"><span data-stu-id="b4fa8-206">System.Void</span></span>

## <span data-ttu-id="b4fa8-207">Note</span><span class="sxs-lookup"><span data-stu-id="b4fa8-207">NOTES</span></span>

## <span data-ttu-id="b4fa8-208">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b4fa8-208">RELATED LINKS</span></span>

[<span data-ttu-id="b4fa8-209">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="b4fa8-209">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="b4fa8-210">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="b4fa8-210">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="b4fa8-211">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="b4fa8-211">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="b4fa8-212">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="b4fa8-212">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="b4fa8-213">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="b4fa8-213">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="b4fa8-214">Stop-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="b4fa8-214">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="b4fa8-215">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="b4fa8-215">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


