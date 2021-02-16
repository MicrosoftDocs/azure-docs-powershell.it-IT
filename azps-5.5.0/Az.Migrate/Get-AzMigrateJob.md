---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
ms.openlocfilehash: bb28550a0b23fa9032832873a78771d25d2a38bd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190190"
---
# <span data-ttu-id="0076c-101">Get-AzMigrateJob</span><span class="sxs-lookup"><span data-stu-id="0076c-101">Get-AzMigrateJob</span></span>

## <span data-ttu-id="0076c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0076c-102">SYNOPSIS</span></span>
<span data-ttu-id="0076c-103">Recupera lo stato di un processo di migrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="0076c-103">Retrieves the status of an Azure Migrate job.</span></span>

## <span data-ttu-id="0076c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0076c-104">SYNTAX</span></span>

### <span data-ttu-id="0076c-105">ListByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0076c-105">ListByName (Default)</span></span>
```
Get-AzMigrateJob -ProjectName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0076c-106">GetById</span><span class="sxs-lookup"><span data-stu-id="0076c-106">GetById</span></span>
```
Get-AzMigrateJob -JobID <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0076c-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="0076c-107">GetByInputObject</span></span>
```
Get-AzMigrateJob -InputObject <IJob> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="0076c-108">GetByName</span><span class="sxs-lookup"><span data-stu-id="0076c-108">GetByName</span></span>
```
Get-AzMigrateJob -JobName <String> -ProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0076c-109">ListById</span><span class="sxs-lookup"><span data-stu-id="0076c-109">ListById</span></span>
```
Get-AzMigrateJob -ProjectID <String> -ResourceGroupID <String> [-SubscriptionId <String>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="0076c-110">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0076c-110">DESCRIPTION</span></span>
<span data-ttu-id="0076c-111">Il Get-AzMigrateJob cmdlet recupera lo stato di un processo di azure migrate.</span><span class="sxs-lookup"><span data-stu-id="0076c-111">The Get-AzMigrateJob cmdlet retrives the status of an Azure Migrate job.</span></span>

## <span data-ttu-id="0076c-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0076c-112">EXAMPLES</span></span>

### <span data-ttu-id="0076c-113">Esempio 1: Ottenere per ID processo</span><span class="sxs-lookup"><span data-stu-id="0076c-113">Example 1: Get By Job Id</span></span>
```powershell
PS C:\> Get-AzMigrateJob -JobID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b" 

ActivityId                       : 68af14b4-46ae-48d1-b3e9-cdcffb9e8a93 ActivityId: 74d1a396-1d37-4264-8a5b-b727aaef0171
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 9/16/20 11:57:33 AM
Error                            : {}
FriendlyName                     : Associate replication policy
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b
Location                         :
Name                             : 997e2a92-5afe-49c7-a81a-89660aec9b7b
ScenarioName                     : AssociateProtectionProfile
StartTime                        : 9/16/20 11:57:32 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 42752b89-5fad-52fd-bf93-679fbdb6fed9
TargetObjectName                 : migrateAzMigratePWSHTc8d1sitepolicy
Task                             : {CloudPairingPrerequisitesCheck, CloudPairingPrepareSite}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="0076c-114">In questo modo viene recuperato un processo in base all'ID.</span><span class="sxs-lookup"><span data-stu-id="0076c-114">This retrieves a job by it's Id.</span></span>

### <span data-ttu-id="0076c-115">Esempio 2: Elencare per gruppo di risorse e progetto</span><span class="sxs-lookup"><span data-stu-id="0076c-115">Example 2: List by resource group and project</span></span>
```powershell
PS C:\> Get-AzMigrateJob -ResourceGroupName 'azmigratepwshtestasr13072020' -ProjectName 'AzMigrateTestProjectPWSH'

ActivityId                       :
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         :
EndTime                          : 9/21/20 4:13:40 PM
Error                            : {}
FriendlyName                     : Update the virtual machine
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/1c89e38e-34ec-4903-aa7c-115201bf2de1
Location                         :
Name                             : 1c89e38e-34ec-4903-aa7c-115201bf2de1
ScenarioName                     : UpdateVmProperties
StartTime                        : 9/21/20 4:13:34 PM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 593b735d-2a34-53b2-b8ed-e33da5650703
TargetObjectName                 : rb-w2k12r2-1
Task                             : {}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="0076c-116">In questo modo si ottiene tutto il lavoro in un progetto.</span><span class="sxs-lookup"><span data-stu-id="0076c-116">This gets all jobs in a project.</span></span>

### <span data-ttu-id="0076c-117">Esempio 3: Ottenere per gruppo di risorse, progetto e nome del processo</span><span class="sxs-lookup"><span data-stu-id="0076c-117">Example 3: Get by resource group, project and job name</span></span>
```powershell
PS C:\> Get-AzMigrateJob -ResourceGroupName 'azmigratepwshtestasr13072020' -ProjectName 'AzMigrateTestProjectPWSH' -JobName 7ae1ee7c-442c-499d-8b0e-81d52a42b71e

ActivityId                       : 6986b7e5-0f1f-49d8-8b4b-77e6f66bcb92 ActivityId: eb73c6a1-7c66-469f-a853-d896aa38cc0f
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 8/21/20 6:41:48 AM
Error                            : {}
FriendlyName                     : Create replication policy
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/7ae1ee7c-442c-499d-8b0e-81d52a42b71e
Location                         :
Name                             : 7ae1ee7c-442c-499d-8b0e-81d52a42b71e
ScenarioName                     : AddProtectionProfile
StartTime                        : 8/21/20 6:41:48 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 18b2ccec-e39a-517b-ae5d-dd395e9f4f96
TargetObjectName                 : samplePolicy3
Task                             : {AddProtectionProfilePreflightsCheckTask, AddProtectionProfileTask}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="0076c-118">Si ottiene un lavoro specifico.</span><span class="sxs-lookup"><span data-stu-id="0076c-118">This gets a specific job.</span></span>

## <span data-ttu-id="0076c-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0076c-119">PARAMETERS</span></span>

### <span data-ttu-id="0076c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0076c-120">-DefaultProfile</span></span>
<span data-ttu-id="0076c-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0076c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0076c-122">-Filter</span><span class="sxs-lookup"><span data-stu-id="0076c-122">-Filter</span></span>
<span data-ttu-id="0076c-123">Opzioni di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="0076c-123">OData filter options.</span></span>

```yaml
Type: System.String
Parameter Sets: ListById, ListByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0076c-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0076c-124">-InputObject</span></span>
<span data-ttu-id="0076c-125">Specifica l'oggetto processo del server che replica.</span><span class="sxs-lookup"><span data-stu-id="0076c-125">Specifies the job object of the replicating server.</span></span>
<span data-ttu-id="0076c-126">Per creare, vedere la sezione NOTE per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="0076c-126">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob
Parameter Sets: GetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0076c-127">-JobID</span><span class="sxs-lookup"><span data-stu-id="0076c-127">-JobID</span></span>
<span data-ttu-id="0076c-128">Specifica l'ID processo per cui recuperare i dettagli.</span><span class="sxs-lookup"><span data-stu-id="0076c-128">Specifies the job id for which the details needs to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: GetById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0076c-129">-JobName</span><span class="sxs-lookup"><span data-stu-id="0076c-129">-JobName</span></span>
<span data-ttu-id="0076c-130">Identificatore di processo</span><span class="sxs-lookup"><span data-stu-id="0076c-130">Job identifier</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0076c-131">-ProjectID</span><span class="sxs-lookup"><span data-stu-id="0076c-131">-ProjectID</span></span>
<span data-ttu-id="0076c-132">Specifica il progetto di Azure Migrate in cui vengono replicati i server.</span><span class="sxs-lookup"><span data-stu-id="0076c-132">Specifies the Azure Migrate Project in which servers are replicating.</span></span>

```yaml
Type: System.String
Parameter Sets: ListById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0076c-133">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="0076c-133">-ProjectName</span></span>
<span data-ttu-id="0076c-134">Nome del progetto di migrazione.</span><span class="sxs-lookup"><span data-stu-id="0076c-134">The name of the migrate project.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName, ListByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0076c-135">-ResourceGroupID</span><span class="sxs-lookup"><span data-stu-id="0076c-135">-ResourceGroupID</span></span>
<span data-ttu-id="0076c-136">Specifica il gruppo di risorse del progetto Azure Migrate nella sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="0076c-136">Specifies the Resource Group of the Azure Migrate Project in the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ListById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0076c-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0076c-137">-ResourceGroupName</span></span>
<span data-ttu-id="0076c-138">Nome del gruppo di risorse in cui è presente la vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="0076c-138">The name of the resource group where the recovery services vault is present.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName, ListByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0076c-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0076c-139">-SubscriptionId</span></span>
<span data-ttu-id="0076c-140">ID sottoscrizione Azure.</span><span class="sxs-lookup"><span data-stu-id="0076c-140">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0076c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0076c-141">CommonParameters</span></span>
<span data-ttu-id="0076c-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0076c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0076c-143">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0076c-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0076c-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="0076c-144">INPUTS</span></span>

## <span data-ttu-id="0076c-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0076c-145">OUTPUTS</span></span>

### <span data-ttu-id="0076c-146">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="0076c-146">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="0076c-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="0076c-147">NOTES</span></span>

<span data-ttu-id="0076c-148">ALIAS</span><span class="sxs-lookup"><span data-stu-id="0076c-148">ALIASES</span></span>

<span data-ttu-id="0076c-149">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="0076c-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0076c-150">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="0076c-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0076c-151">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0076c-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0076c-152"><IJob>INPUTOBJECT: specifica l'oggetto processo del server di replica.</span><span class="sxs-lookup"><span data-stu-id="0076c-152">INPUTOBJECT <IJob>: Specifies the job object of the replicating server.</span></span>
  - <span data-ttu-id="0076c-153">`[Location <String>]`: Posizione risorsa</span><span class="sxs-lookup"><span data-stu-id="0076c-153">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="0076c-154">`[ActivityId <String>]`: l'ID attività.</span><span class="sxs-lookup"><span data-stu-id="0076c-154">`[ActivityId <String>]`: The activity id.</span></span>
  - <span data-ttu-id="0076c-155">`[AllowedAction <String[]>]`: azione consentita per il processo.</span><span class="sxs-lookup"><span data-stu-id="0076c-155">`[AllowedAction <String[]>]`: The Allowed action the job.</span></span>
  - <span data-ttu-id="0076c-156">`[CustomDetailAffectedObjectDetail <IJobDetailsAffectedObjectDetails>]`: le proprietà degli oggetti interessati, come il server di origine, il cloud di origine, il server di destinazione, il cloud di destinazione e così via, in base ai dettagli dell'oggetto flusso di lavoro.</span><span class="sxs-lookup"><span data-stu-id="0076c-156">`[CustomDetailAffectedObjectDetail <IJobDetailsAffectedObjectDetails>]`: The affected object properties like source server, source cloud, target server, target cloud etc. based on the workflow object details.</span></span>
    - <span data-ttu-id="0076c-157">`[(Any) <String>]`: indica che è possibile aggiungere qualsiasi proprietà all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0076c-157">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="0076c-158">`[EndTime <DateTime?>]`: ora di fine.</span><span class="sxs-lookup"><span data-stu-id="0076c-158">`[EndTime <DateTime?>]`: The end time.</span></span>
  - <span data-ttu-id="0076c-159">`[Error <IJobErrorDetails[]>]`: gli errori.</span><span class="sxs-lookup"><span data-stu-id="0076c-159">`[Error <IJobErrorDetails[]>]`: The errors.</span></span>
    - <span data-ttu-id="0076c-160">`[CreationTime <DateTime?>]`: ora di creazione dell'errore di processo.</span><span class="sxs-lookup"><span data-stu-id="0076c-160">`[CreationTime <DateTime?>]`: The creation time of job error.</span></span>
    - <span data-ttu-id="0076c-161">`[ErrorLevel <String>]`: livello di errore.</span><span class="sxs-lookup"><span data-stu-id="0076c-161">`[ErrorLevel <String>]`: Error level of error.</span></span>
    - <span data-ttu-id="0076c-162">`[ProviderErrorDetailErrorCode <Int32?>]`: codice di errore.</span><span class="sxs-lookup"><span data-stu-id="0076c-162">`[ProviderErrorDetailErrorCode <Int32?>]`: The Error code.</span></span>
    - <span data-ttu-id="0076c-163">`[ProviderErrorDetailErrorId <String>]`: ID errore del provider.</span><span class="sxs-lookup"><span data-stu-id="0076c-163">`[ProviderErrorDetailErrorId <String>]`: The Provider error Id.</span></span>
    - <span data-ttu-id="0076c-164">`[ProviderErrorDetailErrorMessage <String>]`: messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="0076c-164">`[ProviderErrorDetailErrorMessage <String>]`: The Error message.</span></span>
    - <span data-ttu-id="0076c-165">`[ProviderErrorDetailPossibleCaus <String>]`: le possibili cause dell'errore.</span><span class="sxs-lookup"><span data-stu-id="0076c-165">`[ProviderErrorDetailPossibleCaus <String>]`: The possible causes for the error.</span></span>
    - <span data-ttu-id="0076c-166">`[ProviderErrorDetailRecommendedAction <String>]`: l'azione consigliata per risolvere l'errore.</span><span class="sxs-lookup"><span data-stu-id="0076c-166">`[ProviderErrorDetailRecommendedAction <String>]`: The recommended action to resolve the error.</span></span>
    - <span data-ttu-id="0076c-167">`[ServiceErrorDetailActivityId <String>]`: ID attività.</span><span class="sxs-lookup"><span data-stu-id="0076c-167">`[ServiceErrorDetailActivityId <String>]`: Activity Id.</span></span>
    - <span data-ttu-id="0076c-168">`[ServiceErrorDetailCode <String>]`: codice di errore.</span><span class="sxs-lookup"><span data-stu-id="0076c-168">`[ServiceErrorDetailCode <String>]`: Error code.</span></span>
    - <span data-ttu-id="0076c-169">`[ServiceErrorDetailMessage <String>]`: messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="0076c-169">`[ServiceErrorDetailMessage <String>]`: Error message.</span></span>
    - <span data-ttu-id="0076c-170">`[ServiceErrorDetailPossibleCaus <String>]`: le possibili cause dell'errore.</span><span class="sxs-lookup"><span data-stu-id="0076c-170">`[ServiceErrorDetailPossibleCaus <String>]`: Possible causes of error.</span></span>
    - <span data-ttu-id="0076c-171">`[ServiceErrorDetailRecommendedAction <String>]`: azione consigliata per risolvere l'errore.</span><span class="sxs-lookup"><span data-stu-id="0076c-171">`[ServiceErrorDetailRecommendedAction <String>]`: Recommended action to resolve error.</span></span>
    - <span data-ttu-id="0076c-172">`[TaskId <String>]`: ID dell'attività.</span><span class="sxs-lookup"><span data-stu-id="0076c-172">`[TaskId <String>]`: The Id of the task.</span></span>
  - <span data-ttu-id="0076c-173">`[FriendlyName <String>]`: il valore displayName.</span><span class="sxs-lookup"><span data-stu-id="0076c-173">`[FriendlyName <String>]`: The DisplayName.</span></span>
  - <span data-ttu-id="0076c-174">`[ScenarioName <String>]`: ScenarioName.</span><span class="sxs-lookup"><span data-stu-id="0076c-174">`[ScenarioName <String>]`: The ScenarioName.</span></span>
  - <span data-ttu-id="0076c-175">`[StartTime <DateTime?>]`: l'ora di inizio.</span><span class="sxs-lookup"><span data-stu-id="0076c-175">`[StartTime <DateTime?>]`: The start time.</span></span>
  - <span data-ttu-id="0076c-176">`[State <String>]`: stato del processo.</span><span class="sxs-lookup"><span data-stu-id="0076c-176">`[State <String>]`: The status of the Job.</span></span> <span data-ttu-id="0076c-177">Si tratta di uno di questi valori: NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended o Other.</span><span class="sxs-lookup"><span data-stu-id="0076c-177">It is one of these values - NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended or Other.</span></span>
  - <span data-ttu-id="0076c-178">`[StateDescription <String>]`: Descrizione dello stato del processo.</span><span class="sxs-lookup"><span data-stu-id="0076c-178">`[StateDescription <String>]`: The description of the state of the Job.</span></span> <span data-ttu-id="0076c-179">Ad esempio, per lo stato Succeeded, la descrizione può essere Completed, PartiallySucceeded, CompletedWithInformation o Skipped.</span><span class="sxs-lookup"><span data-stu-id="0076c-179">For e.g. - For Succeeded state, description can be Completed, PartiallySucceeded, CompletedWithInformation or Skipped.</span></span>
  - <span data-ttu-id="0076c-180">`[TargetInstanceType <String>]`: il tipo dell'oggetto interessato, che è della classe {Microsoft.Azure.SiteRecovery.V2015_11_10.AffectedObjectType}.</span><span class="sxs-lookup"><span data-stu-id="0076c-180">`[TargetInstanceType <String>]`: The type of the affected object which is of {Microsoft.Azure.SiteRecovery.V2015_11_10.AffectedObjectType} class.</span></span>
  - <span data-ttu-id="0076c-181">`[TargetObjectId <String>]`: l'ID oggetto interessato.</span><span class="sxs-lookup"><span data-stu-id="0076c-181">`[TargetObjectId <String>]`: The affected Object Id.</span></span>
  - <span data-ttu-id="0076c-182">`[TargetObjectName <String>]`: nome dell'oggetto interessato.</span><span class="sxs-lookup"><span data-stu-id="0076c-182">`[TargetObjectName <String>]`: The name of the affected object.</span></span>
  - <span data-ttu-id="0076c-183">`[Task <IAsrTask[]>]`: le attività.</span><span class="sxs-lookup"><span data-stu-id="0076c-183">`[Task <IAsrTask[]>]`: The tasks.</span></span>
    - <span data-ttu-id="0076c-184">`[AllowedAction <String[]>]`: stato/azioni applicabili all'attività.</span><span class="sxs-lookup"><span data-stu-id="0076c-184">`[AllowedAction <String[]>]`: The state/actions applicable on this task.</span></span>
    - <span data-ttu-id="0076c-185">`[CustomDetailInstanceType <String>]`: il tipo di dettagli dell'attività.</span><span class="sxs-lookup"><span data-stu-id="0076c-185">`[CustomDetailInstanceType <String>]`: The type of task details.</span></span>
    - <span data-ttu-id="0076c-186">`[EndTime <DateTime?>]`: ora di fine.</span><span class="sxs-lookup"><span data-stu-id="0076c-186">`[EndTime <DateTime?>]`: The end time.</span></span>
    - <span data-ttu-id="0076c-187">`[Error <IJobErrorDetails[]>]`: dettagli dell'errore dell'attività.</span><span class="sxs-lookup"><span data-stu-id="0076c-187">`[Error <IJobErrorDetails[]>]`: The task error details.</span></span>
    - <span data-ttu-id="0076c-188">`[FriendlyName <String>]`: il nome.</span><span class="sxs-lookup"><span data-stu-id="0076c-188">`[FriendlyName <String>]`: The name.</span></span>
    - <span data-ttu-id="0076c-189">`[GroupTaskCustomDetailChildTask <IAsrTask[]>]`: le attività figlio.</span><span class="sxs-lookup"><span data-stu-id="0076c-189">`[GroupTaskCustomDetailChildTask <IAsrTask[]>]`: The child tasks.</span></span>
    - <span data-ttu-id="0076c-190">`[GroupTaskCustomDetailInstanceType <String>]`: il tipo di dettagli dell'attività.</span><span class="sxs-lookup"><span data-stu-id="0076c-190">`[GroupTaskCustomDetailInstanceType <String>]`: The type of task details.</span></span>
    - <span data-ttu-id="0076c-191">`[Name <String>]`: nome univoco dell'attività.</span><span class="sxs-lookup"><span data-stu-id="0076c-191">`[Name <String>]`: The unique Task name.</span></span>
    - <span data-ttu-id="0076c-192">`[StartTime <DateTime?>]`: l'ora di inizio.</span><span class="sxs-lookup"><span data-stu-id="0076c-192">`[StartTime <DateTime?>]`: The start time.</span></span>
    - <span data-ttu-id="0076c-193">`[State <String>]`: lo stato.</span><span class="sxs-lookup"><span data-stu-id="0076c-193">`[State <String>]`: The State.</span></span> <span data-ttu-id="0076c-194">Si tratta di uno di questi valori: NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended o Other.</span><span class="sxs-lookup"><span data-stu-id="0076c-194">It is one of these values - NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended or Other.</span></span>
    - <span data-ttu-id="0076c-195">`[StateDescription <String>]`: Descrizione dello stato dell'attività.</span><span class="sxs-lookup"><span data-stu-id="0076c-195">`[StateDescription <String>]`: The description of the task state.</span></span> <span data-ttu-id="0076c-196">Ad esempio: per lo stato Succeeded, la descrizione può essere Completed, PartiallySucceeded, CompletedWithInformation o Skipped.</span><span class="sxs-lookup"><span data-stu-id="0076c-196">For example - For Succeeded state, description can be Completed, PartiallySucceeded, CompletedWithInformation or Skipped.</span></span>
    - <span data-ttu-id="0076c-197">`[TaskId <String>]`: l'ID.</span><span class="sxs-lookup"><span data-stu-id="0076c-197">`[TaskId <String>]`: The Id.</span></span>
    - <span data-ttu-id="0076c-198">`[TaskType <String>]`: il tipo di attività.</span><span class="sxs-lookup"><span data-stu-id="0076c-198">`[TaskType <String>]`: The type of task.</span></span> <span data-ttu-id="0076c-199">I dettagli della proprietà Dettagli personalizzati dipendono da questo tipo.</span><span class="sxs-lookup"><span data-stu-id="0076c-199">Details in CustomDetails property depend on this type.</span></span>

## <span data-ttu-id="0076c-200">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0076c-200">RELATED LINKS</span></span>

