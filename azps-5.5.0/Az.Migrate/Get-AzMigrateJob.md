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
# Get-AzMigrateJob

## SYNOPSIS
Recupera lo stato di un processo di migrazione di Azure.

## SINTASSI

### ListByName (impostazione predefinita)
```
Get-AzMigrateJob -ProjectName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetById
```
Get-AzMigrateJob -JobID <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetByInputObject
```
Get-AzMigrateJob -InputObject <IJob> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### GetByName
```
Get-AzMigrateJob -JobName <String> -ProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### ListById
```
Get-AzMigrateJob -ProjectID <String> -ResourceGroupID <String> [-SubscriptionId <String>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## DESCRIZIONE
Il Get-AzMigrateJob cmdlet recupera lo stato di un processo di azure migrate.

## ESEMPI

### Esempio 1: Ottenere per ID processo
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

In questo modo viene recuperato un processo in base all'ID.

### Esempio 2: Elencare per gruppo di risorse e progetto
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

In questo modo si ottiene tutto il lavoro in un progetto.

### Esempio 3: Ottenere per gruppo di risorse, progetto e nome del processo
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

Si ottiene un lavoro specifico.

## PARAMETERS

### -DefaultProfile
Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.

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

### -Filter
Opzioni di filtro OData.

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

### -InputObject
Specifica l'oggetto processo del server che replica.
Per creare, vedere la sezione NOTE per le proprietà INPUTOBJECT e creare una tabella hash.

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

### -JobID
Specifica l'ID processo per cui recuperare i dettagli.

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

### -JobName
Identificatore di processo

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

### -ProjectID
Specifica il progetto di Azure Migrate in cui vengono replicati i server.

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

### -ProjectName
Nome del progetto di migrazione.

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

### -ResourceGroupID
Specifica il gruppo di risorse del progetto Azure Migrate nella sottoscrizione corrente.

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

### -ResourceGroupName
Nome del gruppo di risorse in cui è presente la vault dei servizi di ripristino.

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

### -SubscriptionId
ID sottoscrizione Azure.

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

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

## OUTPUT

### Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob

## NOTE

ALIAS

PROPRIETÀ DEI PARAMETRI COMPLESSE

Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate. Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.


<IJob>INPUTOBJECT: specifica l'oggetto processo del server di replica.
  - `[Location <String>]`: Posizione risorsa
  - `[ActivityId <String>]`: l'ID attività.
  - `[AllowedAction <String[]>]`: azione consentita per il processo.
  - `[CustomDetailAffectedObjectDetail <IJobDetailsAffectedObjectDetails>]`: le proprietà degli oggetti interessati, come il server di origine, il cloud di origine, il server di destinazione, il cloud di destinazione e così via, in base ai dettagli dell'oggetto flusso di lavoro.
    - `[(Any) <String>]`: indica che è possibile aggiungere qualsiasi proprietà all'oggetto.
  - `[EndTime <DateTime?>]`: ora di fine.
  - `[Error <IJobErrorDetails[]>]`: gli errori.
    - `[CreationTime <DateTime?>]`: ora di creazione dell'errore di processo.
    - `[ErrorLevel <String>]`: livello di errore.
    - `[ProviderErrorDetailErrorCode <Int32?>]`: codice di errore.
    - `[ProviderErrorDetailErrorId <String>]`: ID errore del provider.
    - `[ProviderErrorDetailErrorMessage <String>]`: messaggio di errore.
    - `[ProviderErrorDetailPossibleCaus <String>]`: le possibili cause dell'errore.
    - `[ProviderErrorDetailRecommendedAction <String>]`: l'azione consigliata per risolvere l'errore.
    - `[ServiceErrorDetailActivityId <String>]`: ID attività.
    - `[ServiceErrorDetailCode <String>]`: codice di errore.
    - `[ServiceErrorDetailMessage <String>]`: messaggio di errore.
    - `[ServiceErrorDetailPossibleCaus <String>]`: le possibili cause dell'errore.
    - `[ServiceErrorDetailRecommendedAction <String>]`: azione consigliata per risolvere l'errore.
    - `[TaskId <String>]`: ID dell'attività.
  - `[FriendlyName <String>]`: il valore displayName.
  - `[ScenarioName <String>]`: ScenarioName.
  - `[StartTime <DateTime?>]`: l'ora di inizio.
  - `[State <String>]`: stato del processo. Si tratta di uno di questi valori: NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended o Other.
  - `[StateDescription <String>]`: Descrizione dello stato del processo. Ad esempio, per lo stato Succeeded, la descrizione può essere Completed, PartiallySucceeded, CompletedWithInformation o Skipped.
  - `[TargetInstanceType <String>]`: il tipo dell'oggetto interessato, che è della classe {Microsoft.Azure.SiteRecovery.V2015_11_10.AffectedObjectType}.
  - `[TargetObjectId <String>]`: l'ID oggetto interessato.
  - `[TargetObjectName <String>]`: nome dell'oggetto interessato.
  - `[Task <IAsrTask[]>]`: le attività.
    - `[AllowedAction <String[]>]`: stato/azioni applicabili all'attività.
    - `[CustomDetailInstanceType <String>]`: il tipo di dettagli dell'attività.
    - `[EndTime <DateTime?>]`: ora di fine.
    - `[Error <IJobErrorDetails[]>]`: dettagli dell'errore dell'attività.
    - `[FriendlyName <String>]`: il nome.
    - `[GroupTaskCustomDetailChildTask <IAsrTask[]>]`: le attività figlio.
    - `[GroupTaskCustomDetailInstanceType <String>]`: il tipo di dettagli dell'attività.
    - `[Name <String>]`: nome univoco dell'attività.
    - `[StartTime <DateTime?>]`: l'ora di inizio.
    - `[State <String>]`: lo stato. Si tratta di uno di questi valori: NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended o Other.
    - `[StateDescription <String>]`: Descrizione dello stato dell'attività. Ad esempio: per lo stato Succeeded, la descrizione può essere Completed, PartiallySucceeded, CompletedWithInformation o Skipped.
    - `[TaskId <String>]`: l'ID.
    - `[TaskType <String>]`: il tipo di attività. I dettagli della proprietà Dettagli personalizzati dipendono da questo tipo.

## COLLEGAMENTI CORRELATI

