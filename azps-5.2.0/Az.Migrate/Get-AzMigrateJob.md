---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
ms.openlocfilehash: bb28550a0b23fa9032832873a78771d25d2a38bd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330835"
---
# <span data-ttu-id="2a13a-101">Get-AzMigrateJob</span><span class="sxs-lookup"><span data-stu-id="2a13a-101">Get-AzMigrateJob</span></span>

## <span data-ttu-id="2a13a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2a13a-102">SYNOPSIS</span></span>
<span data-ttu-id="2a13a-103">Recupera lo stato di un processo di migrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="2a13a-103">Retrieves the status of an Azure Migrate job.</span></span>

## <span data-ttu-id="2a13a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2a13a-104">SYNTAX</span></span>

### <span data-ttu-id="2a13a-105">ListByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2a13a-105">ListByName (Default)</span></span>
```
Get-AzMigrateJob -ProjectName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2a13a-106">GetById</span><span class="sxs-lookup"><span data-stu-id="2a13a-106">GetById</span></span>
```
Get-AzMigrateJob -JobID <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2a13a-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="2a13a-107">GetByInputObject</span></span>
```
Get-AzMigrateJob -InputObject <IJob> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="2a13a-108">GetByName</span><span class="sxs-lookup"><span data-stu-id="2a13a-108">GetByName</span></span>
```
Get-AzMigrateJob -JobName <String> -ProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2a13a-109">ListById</span><span class="sxs-lookup"><span data-stu-id="2a13a-109">ListById</span></span>
```
Get-AzMigrateJob -ProjectID <String> -ResourceGroupID <String> [-SubscriptionId <String>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="2a13a-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2a13a-110">DESCRIPTION</span></span>
<span data-ttu-id="2a13a-111">Il cmdlet Get-AzMigrateJob Retrives lo stato di un processo di migrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="2a13a-111">The Get-AzMigrateJob cmdlet retrives the status of an Azure Migrate job.</span></span>

## <span data-ttu-id="2a13a-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2a13a-112">EXAMPLES</span></span>

### <span data-ttu-id="2a13a-113">Esempio 1: ottenere per ID processo</span><span class="sxs-lookup"><span data-stu-id="2a13a-113">Example 1: Get By Job Id</span></span>
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

<span data-ttu-id="2a13a-114">In questo articolo viene recuperato un processo in base all'ID.</span><span class="sxs-lookup"><span data-stu-id="2a13a-114">This retrieves a job by it's Id.</span></span>

### <span data-ttu-id="2a13a-115">Esempio 2: elenco per gruppo risorse e progetto</span><span class="sxs-lookup"><span data-stu-id="2a13a-115">Example 2: List by resource group and project</span></span>
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

<span data-ttu-id="2a13a-116">In questo articolo vengono ottenuti tutti i processi in un progetto.</span><span class="sxs-lookup"><span data-stu-id="2a13a-116">This gets all jobs in a project.</span></span>

### <span data-ttu-id="2a13a-117">Esempio 3: ottenere un gruppo di risorse, un progetto e un nome di lavoro</span><span class="sxs-lookup"><span data-stu-id="2a13a-117">Example 3: Get by resource group, project and job name</span></span>
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

<span data-ttu-id="2a13a-118">Questo ottiene un processo specifico.</span><span class="sxs-lookup"><span data-stu-id="2a13a-118">This gets a specific job.</span></span>

## <span data-ttu-id="2a13a-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2a13a-119">PARAMETERS</span></span>

### <span data-ttu-id="2a13a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a13a-120">-DefaultProfile</span></span>
<span data-ttu-id="2a13a-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2a13a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a13a-122">-Filtro</span><span class="sxs-lookup"><span data-stu-id="2a13a-122">-Filter</span></span>
<span data-ttu-id="2a13a-123">Opzioni di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="2a13a-123">OData filter options.</span></span>

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

### <span data-ttu-id="2a13a-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a13a-124">-InputObject</span></span>
<span data-ttu-id="2a13a-125">Specifica l'oggetto processo del server di replica.</span><span class="sxs-lookup"><span data-stu-id="2a13a-125">Specifies the job object of the replicating server.</span></span>
<span data-ttu-id="2a13a-126">Per costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="2a13a-126">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2a13a-127">-JobID</span><span class="sxs-lookup"><span data-stu-id="2a13a-127">-JobID</span></span>
<span data-ttu-id="2a13a-128">Specifica l'ID processo per cui devono essere recuperati i dettagli.</span><span class="sxs-lookup"><span data-stu-id="2a13a-128">Specifies the job id for which the details needs to be retrieved.</span></span>

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

### <span data-ttu-id="2a13a-129">-JobName</span><span class="sxs-lookup"><span data-stu-id="2a13a-129">-JobName</span></span>
<span data-ttu-id="2a13a-130">Identificatore processo</span><span class="sxs-lookup"><span data-stu-id="2a13a-130">Job identifier</span></span>

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

### <span data-ttu-id="2a13a-131">-ProjectID</span><span class="sxs-lookup"><span data-stu-id="2a13a-131">-ProjectID</span></span>
<span data-ttu-id="2a13a-132">Specifica il progetto di migrazione di Azure in cui vengono replicati i server.</span><span class="sxs-lookup"><span data-stu-id="2a13a-132">Specifies the Azure Migrate Project in which servers are replicating.</span></span>

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

### <span data-ttu-id="2a13a-133">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="2a13a-133">-ProjectName</span></span>
<span data-ttu-id="2a13a-134">Nome del progetto di migrazione.</span><span class="sxs-lookup"><span data-stu-id="2a13a-134">The name of the migrate project.</span></span>

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

### <span data-ttu-id="2a13a-135">-ResourceGroupID</span><span class="sxs-lookup"><span data-stu-id="2a13a-135">-ResourceGroupID</span></span>
<span data-ttu-id="2a13a-136">Specifica il gruppo di risorse di Azure migra Project nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="2a13a-136">Specifies the Resource Group of the Azure Migrate Project in the current subscription.</span></span>

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

### <span data-ttu-id="2a13a-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a13a-137">-ResourceGroupName</span></span>
<span data-ttu-id="2a13a-138">Nome del gruppo di risorse in cui è presente il Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="2a13a-138">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="2a13a-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2a13a-139">-SubscriptionId</span></span>
<span data-ttu-id="2a13a-140">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="2a13a-140">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="2a13a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a13a-141">CommonParameters</span></span>
<span data-ttu-id="2a13a-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a13a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a13a-143">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a13a-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a13a-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2a13a-144">INPUTS</span></span>

## <span data-ttu-id="2a13a-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2a13a-145">OUTPUTS</span></span>

### <span data-ttu-id="2a13a-146">Microsoft. Azure. PowerShell. Cmdlets. migrate. Models. Api20180110. IJob</span><span class="sxs-lookup"><span data-stu-id="2a13a-146">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="2a13a-147">Note</span><span class="sxs-lookup"><span data-stu-id="2a13a-147">NOTES</span></span>

<span data-ttu-id="2a13a-148">ALIAS</span><span class="sxs-lookup"><span data-stu-id="2a13a-148">ALIASES</span></span>

<span data-ttu-id="2a13a-149">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2a13a-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2a13a-150">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="2a13a-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2a13a-151">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2a13a-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2a13a-152">INPUTOBJECT <IJob> : specifica l'oggetto processo del server di replica.</span><span class="sxs-lookup"><span data-stu-id="2a13a-152">INPUTOBJECT <IJob>: Specifies the job object of the replicating server.</span></span>
  - <span data-ttu-id="2a13a-153">`[Location <String>]`: Percorso delle risorse</span><span class="sxs-lookup"><span data-stu-id="2a13a-153">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="2a13a-154">`[ActivityId <String>]`: ID attività.</span><span class="sxs-lookup"><span data-stu-id="2a13a-154">`[ActivityId <String>]`: The activity id.</span></span>
  - <span data-ttu-id="2a13a-155">`[AllowedAction <String[]>]`: Azione consentita per il processo.</span><span class="sxs-lookup"><span data-stu-id="2a13a-155">`[AllowedAction <String[]>]`: The Allowed action the job.</span></span>
  - <span data-ttu-id="2a13a-156">`[CustomDetailAffectedObjectDetail <IJobDetailsAffectedObjectDetails>]`: Le proprietà dell'oggetto interessato, come il server di origine, il cloud di origine, il server di destinazione, la nuvola di destinazione, ecc.</span><span class="sxs-lookup"><span data-stu-id="2a13a-156">`[CustomDetailAffectedObjectDetail <IJobDetailsAffectedObjectDetails>]`: The affected object properties like source server, source cloud, target server, target cloud etc. based on the workflow object details.</span></span>
    - <span data-ttu-id="2a13a-157">`[(Any) <String>]`: Indica che qualsiasi proprietà può essere aggiunta a questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="2a13a-157">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="2a13a-158">`[EndTime <DateTime?>]`: L'ora di fine.</span><span class="sxs-lookup"><span data-stu-id="2a13a-158">`[EndTime <DateTime?>]`: The end time.</span></span>
  - <span data-ttu-id="2a13a-159">`[Error <IJobErrorDetails[]>]`: Gli errori.</span><span class="sxs-lookup"><span data-stu-id="2a13a-159">`[Error <IJobErrorDetails[]>]`: The errors.</span></span>
    - <span data-ttu-id="2a13a-160">`[CreationTime <DateTime?>]`: L'ora di creazione dell'errore del processo.</span><span class="sxs-lookup"><span data-stu-id="2a13a-160">`[CreationTime <DateTime?>]`: The creation time of job error.</span></span>
    - <span data-ttu-id="2a13a-161">`[ErrorLevel <String>]`: Errore livello di errore.</span><span class="sxs-lookup"><span data-stu-id="2a13a-161">`[ErrorLevel <String>]`: Error level of error.</span></span>
    - <span data-ttu-id="2a13a-162">`[ProviderErrorDetailErrorCode <Int32?>]`: Il codice di errore.</span><span class="sxs-lookup"><span data-stu-id="2a13a-162">`[ProviderErrorDetailErrorCode <Int32?>]`: The Error code.</span></span>
    - <span data-ttu-id="2a13a-163">`[ProviderErrorDetailErrorId <String>]`: ID errore provider.</span><span class="sxs-lookup"><span data-stu-id="2a13a-163">`[ProviderErrorDetailErrorId <String>]`: The Provider error Id.</span></span>
    - <span data-ttu-id="2a13a-164">`[ProviderErrorDetailErrorMessage <String>]`: Messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="2a13a-164">`[ProviderErrorDetailErrorMessage <String>]`: The Error message.</span></span>
    - <span data-ttu-id="2a13a-165">`[ProviderErrorDetailPossibleCaus <String>]`: Le possibili cause dell'errore.</span><span class="sxs-lookup"><span data-stu-id="2a13a-165">`[ProviderErrorDetailPossibleCaus <String>]`: The possible causes for the error.</span></span>
    - <span data-ttu-id="2a13a-166">`[ProviderErrorDetailRecommendedAction <String>]`: L'azione consigliata per risolvere l'errore.</span><span class="sxs-lookup"><span data-stu-id="2a13a-166">`[ProviderErrorDetailRecommendedAction <String>]`: The recommended action to resolve the error.</span></span>
    - <span data-ttu-id="2a13a-167">`[ServiceErrorDetailActivityId <String>]`: ID attività.</span><span class="sxs-lookup"><span data-stu-id="2a13a-167">`[ServiceErrorDetailActivityId <String>]`: Activity Id.</span></span>
    - <span data-ttu-id="2a13a-168">`[ServiceErrorDetailCode <String>]`: Codice di errore.</span><span class="sxs-lookup"><span data-stu-id="2a13a-168">`[ServiceErrorDetailCode <String>]`: Error code.</span></span>
    - <span data-ttu-id="2a13a-169">`[ServiceErrorDetailMessage <String>]`: Messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="2a13a-169">`[ServiceErrorDetailMessage <String>]`: Error message.</span></span>
    - <span data-ttu-id="2a13a-170">`[ServiceErrorDetailPossibleCaus <String>]`: Possibili cause di errore.</span><span class="sxs-lookup"><span data-stu-id="2a13a-170">`[ServiceErrorDetailPossibleCaus <String>]`: Possible causes of error.</span></span>
    - <span data-ttu-id="2a13a-171">`[ServiceErrorDetailRecommendedAction <String>]`: Azione consigliata per risolvere l'errore.</span><span class="sxs-lookup"><span data-stu-id="2a13a-171">`[ServiceErrorDetailRecommendedAction <String>]`: Recommended action to resolve error.</span></span>
    - <span data-ttu-id="2a13a-172">`[TaskId <String>]`: ID dell'attività.</span><span class="sxs-lookup"><span data-stu-id="2a13a-172">`[TaskId <String>]`: The Id of the task.</span></span>
  - <span data-ttu-id="2a13a-173">`[FriendlyName <String>]`: DisplayName.</span><span class="sxs-lookup"><span data-stu-id="2a13a-173">`[FriendlyName <String>]`: The DisplayName.</span></span>
  - <span data-ttu-id="2a13a-174">`[ScenarioName <String>]`: Lo scenario.</span><span class="sxs-lookup"><span data-stu-id="2a13a-174">`[ScenarioName <String>]`: The ScenarioName.</span></span>
  - <span data-ttu-id="2a13a-175">`[StartTime <DateTime?>]`: L'ora di inizio.</span><span class="sxs-lookup"><span data-stu-id="2a13a-175">`[StartTime <DateTime?>]`: The start time.</span></span>
  - <span data-ttu-id="2a13a-176">`[State <String>]`: Lo stato del processo.</span><span class="sxs-lookup"><span data-stu-id="2a13a-176">`[State <String>]`: The status of the Job.</span></span> <span data-ttu-id="2a13a-177">Si tratta di uno di questi valori: NotStarted, InProgress, Succeeded, failed, Cancelled, Suspended o other.</span><span class="sxs-lookup"><span data-stu-id="2a13a-177">It is one of these values - NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended or Other.</span></span>
  - <span data-ttu-id="2a13a-178">`[StateDescription <String>]`: Descrizione dello stato del processo.</span><span class="sxs-lookup"><span data-stu-id="2a13a-178">`[StateDescription <String>]`: The description of the state of the Job.</span></span> <span data-ttu-id="2a13a-179">Ad esempio, per stato riuscito, la descrizione può essere completata, PartiallySucceeded, CompletedWithInformation o ignorata.</span><span class="sxs-lookup"><span data-stu-id="2a13a-179">For e.g. - For Succeeded state, description can be Completed, PartiallySucceeded, CompletedWithInformation or Skipped.</span></span>
  - <span data-ttu-id="2a13a-180">`[TargetInstanceType <String>]`: Il tipo dell'oggetto interessato che è della classe {Microsoft.Azure.SiteRecovery.V2015_11_10. AffectedObjectType}.</span><span class="sxs-lookup"><span data-stu-id="2a13a-180">`[TargetInstanceType <String>]`: The type of the affected object which is of {Microsoft.Azure.SiteRecovery.V2015_11_10.AffectedObjectType} class.</span></span>
  - <span data-ttu-id="2a13a-181">`[TargetObjectId <String>]`: ID oggetto interessato.</span><span class="sxs-lookup"><span data-stu-id="2a13a-181">`[TargetObjectId <String>]`: The affected Object Id.</span></span>
  - <span data-ttu-id="2a13a-182">`[TargetObjectName <String>]`: Nome dell'oggetto interessato.</span><span class="sxs-lookup"><span data-stu-id="2a13a-182">`[TargetObjectName <String>]`: The name of the affected object.</span></span>
  - <span data-ttu-id="2a13a-183">`[Task <IAsrTask[]>]`: Le attività.</span><span class="sxs-lookup"><span data-stu-id="2a13a-183">`[Task <IAsrTask[]>]`: The tasks.</span></span>
    - <span data-ttu-id="2a13a-184">`[AllowedAction <String[]>]`: Lo stato o le azioni valide per questa attività.</span><span class="sxs-lookup"><span data-stu-id="2a13a-184">`[AllowedAction <String[]>]`: The state/actions applicable on this task.</span></span>
    - <span data-ttu-id="2a13a-185">`[CustomDetailInstanceType <String>]`: Tipo di dettagli attività.</span><span class="sxs-lookup"><span data-stu-id="2a13a-185">`[CustomDetailInstanceType <String>]`: The type of task details.</span></span>
    - <span data-ttu-id="2a13a-186">`[EndTime <DateTime?>]`: L'ora di fine.</span><span class="sxs-lookup"><span data-stu-id="2a13a-186">`[EndTime <DateTime?>]`: The end time.</span></span>
    - <span data-ttu-id="2a13a-187">`[Error <IJobErrorDetails[]>]`: Dettagli errore attività.</span><span class="sxs-lookup"><span data-stu-id="2a13a-187">`[Error <IJobErrorDetails[]>]`: The task error details.</span></span>
    - <span data-ttu-id="2a13a-188">`[FriendlyName <String>]`: Nome.</span><span class="sxs-lookup"><span data-stu-id="2a13a-188">`[FriendlyName <String>]`: The name.</span></span>
    - <span data-ttu-id="2a13a-189">`[GroupTaskCustomDetailChildTask <IAsrTask[]>]`: Attività figlio.</span><span class="sxs-lookup"><span data-stu-id="2a13a-189">`[GroupTaskCustomDetailChildTask <IAsrTask[]>]`: The child tasks.</span></span>
    - <span data-ttu-id="2a13a-190">`[GroupTaskCustomDetailInstanceType <String>]`: Tipo di dettagli attività.</span><span class="sxs-lookup"><span data-stu-id="2a13a-190">`[GroupTaskCustomDetailInstanceType <String>]`: The type of task details.</span></span>
    - <span data-ttu-id="2a13a-191">`[Name <String>]`: Nome dell'attività univoco.</span><span class="sxs-lookup"><span data-stu-id="2a13a-191">`[Name <String>]`: The unique Task name.</span></span>
    - <span data-ttu-id="2a13a-192">`[StartTime <DateTime?>]`: L'ora di inizio.</span><span class="sxs-lookup"><span data-stu-id="2a13a-192">`[StartTime <DateTime?>]`: The start time.</span></span>
    - <span data-ttu-id="2a13a-193">`[State <String>]`: Lo stato.</span><span class="sxs-lookup"><span data-stu-id="2a13a-193">`[State <String>]`: The State.</span></span> <span data-ttu-id="2a13a-194">Si tratta di uno di questi valori: NotStarted, InProgress, Succeeded, failed, Cancelled, Suspended o other.</span><span class="sxs-lookup"><span data-stu-id="2a13a-194">It is one of these values - NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended or Other.</span></span>
    - <span data-ttu-id="2a13a-195">`[StateDescription <String>]`: Descrizione dello stato dell'attività.</span><span class="sxs-lookup"><span data-stu-id="2a13a-195">`[StateDescription <String>]`: The description of the task state.</span></span> <span data-ttu-id="2a13a-196">Ad esempio, per stato riuscito, la descrizione può essere completata, PartiallySucceeded, CompletedWithInformation o ignorata.</span><span class="sxs-lookup"><span data-stu-id="2a13a-196">For example - For Succeeded state, description can be Completed, PartiallySucceeded, CompletedWithInformation or Skipped.</span></span>
    - <span data-ttu-id="2a13a-197">`[TaskId <String>]`: ID.</span><span class="sxs-lookup"><span data-stu-id="2a13a-197">`[TaskId <String>]`: The Id.</span></span>
    - <span data-ttu-id="2a13a-198">`[TaskType <String>]`: Il tipo di attività.</span><span class="sxs-lookup"><span data-stu-id="2a13a-198">`[TaskType <String>]`: The type of task.</span></span> <span data-ttu-id="2a13a-199">I dettagli nella proprietà CustomDetails dipendono da questo tipo.</span><span class="sxs-lookup"><span data-stu-id="2a13a-199">Details in CustomDetails property depend on this type.</span></span>

## <span data-ttu-id="2a13a-200">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2a13a-200">RELATED LINKS</span></span>

