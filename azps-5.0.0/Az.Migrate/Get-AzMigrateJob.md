---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
ms.openlocfilehash: bb28550a0b23fa9032832873a78771d25d2a38bd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203535"
---
# Get-AzMigrateJob

## Sinossi
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

## Descrizione
Il cmdlet Get-AzMigrateJob Retrives lo stato di un processo di migrazione di Azure.

## ESEMPI

### Esempio 1: ottenere per ID processo
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

In questo articolo viene recuperato un processo in base all'ID.

### Esempio 2: elenco per gruppo risorse e progetto
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

In questo articolo vengono ottenuti tutti i processi in un progetto.

### Esempio 3: ottenere un gruppo di risorse, un progetto e un nome di lavoro
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

Questo ottiene un processo specifico.

## PARAMETRI

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

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

### -Filtro
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
Specifica l'oggetto processo del server di replica.
Per costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.

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
Specifica l'ID processo per cui devono essere recuperati i dettagli.

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
Identificatore processo

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
Specifica il progetto di migrazione di Azure in cui vengono replicati i server.

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
Specifica il gruppo di risorse di Azure migra Project nell'abbonamento corrente.

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
Nome del gruppo di risorse in cui è presente il Vault di servizi di ripristino.

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
ID abbonamento di Azure.

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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

## OUTPUT

### Microsoft. Azure. PowerShell. Cmdlets. migrate. Models. Api20180110. IJob

## Note

ALIAS

PROPRIETÀ COMPLESSE DI PARAMETRI

Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate. Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.


INPUTOBJECT <IJob> : specifica l'oggetto processo del server di replica.
  - `[Location <String>]`: Percorso delle risorse
  - `[ActivityId <String>]`: ID attività.
  - `[AllowedAction <String[]>]`: Azione consentita per il processo.
  - `[CustomDetailAffectedObjectDetail <IJobDetailsAffectedObjectDetails>]`: Le proprietà dell'oggetto interessato, come il server di origine, il cloud di origine, il server di destinazione, la nuvola di destinazione, ecc.
    - `[(Any) <String>]`: Indica che qualsiasi proprietà può essere aggiunta a questo oggetto.
  - `[EndTime <DateTime?>]`: L'ora di fine.
  - `[Error <IJobErrorDetails[]>]`: Gli errori.
    - `[CreationTime <DateTime?>]`: L'ora di creazione dell'errore del processo.
    - `[ErrorLevel <String>]`: Errore livello di errore.
    - `[ProviderErrorDetailErrorCode <Int32?>]`: Il codice di errore.
    - `[ProviderErrorDetailErrorId <String>]`: ID errore provider.
    - `[ProviderErrorDetailErrorMessage <String>]`: Messaggio di errore.
    - `[ProviderErrorDetailPossibleCaus <String>]`: Le possibili cause dell'errore.
    - `[ProviderErrorDetailRecommendedAction <String>]`: L'azione consigliata per risolvere l'errore.
    - `[ServiceErrorDetailActivityId <String>]`: ID attività.
    - `[ServiceErrorDetailCode <String>]`: Codice di errore.
    - `[ServiceErrorDetailMessage <String>]`: Messaggio di errore.
    - `[ServiceErrorDetailPossibleCaus <String>]`: Possibili cause di errore.
    - `[ServiceErrorDetailRecommendedAction <String>]`: Azione consigliata per risolvere l'errore.
    - `[TaskId <String>]`: ID dell'attività.
  - `[FriendlyName <String>]`: DisplayName.
  - `[ScenarioName <String>]`: Lo scenario.
  - `[StartTime <DateTime?>]`: L'ora di inizio.
  - `[State <String>]`: Lo stato del processo. Si tratta di uno di questi valori: NotStarted, InProgress, Succeeded, failed, Cancelled, Suspended o other.
  - `[StateDescription <String>]`: Descrizione dello stato del processo. Ad esempio, per stato riuscito, la descrizione può essere completata, PartiallySucceeded, CompletedWithInformation o ignorata.
  - `[TargetInstanceType <String>]`: Il tipo dell'oggetto interessato che è della classe {Microsoft.Azure.SiteRecovery.V2015_11_10. AffectedObjectType}.
  - `[TargetObjectId <String>]`: ID oggetto interessato.
  - `[TargetObjectName <String>]`: Nome dell'oggetto interessato.
  - `[Task <IAsrTask[]>]`: Le attività.
    - `[AllowedAction <String[]>]`: Lo stato o le azioni valide per questa attività.
    - `[CustomDetailInstanceType <String>]`: Tipo di dettagli attività.
    - `[EndTime <DateTime?>]`: L'ora di fine.
    - `[Error <IJobErrorDetails[]>]`: Dettagli errore attività.
    - `[FriendlyName <String>]`: Nome.
    - `[GroupTaskCustomDetailChildTask <IAsrTask[]>]`: Attività figlio.
    - `[GroupTaskCustomDetailInstanceType <String>]`: Tipo di dettagli attività.
    - `[Name <String>]`: Nome dell'attività univoco.
    - `[StartTime <DateTime?>]`: L'ora di inizio.
    - `[State <String>]`: Lo stato. Si tratta di uno di questi valori: NotStarted, InProgress, Succeeded, failed, Cancelled, Suspended o other.
    - `[StateDescription <String>]`: Descrizione dello stato dell'attività. Ad esempio, per stato riuscito, la descrizione può essere completata, PartiallySucceeded, CompletedWithInformation o ignorata.
    - `[TaskId <String>]`: ID.
    - `[TaskType <String>]`: Il tipo di attività. I dettagli nella proprietà CustomDetails dipendono da questo tipo.

## COLLEGAMENTI CORRELATI

