---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/start-azmigratetestmigrationcleanup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigrationCleanup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigrationCleanup.md
ms.openlocfilehash: df4eac2c6380c36dcd07c906ccbbee4d2a93f27b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476095"
---
# <span data-ttu-id="d6a2f-101">Start-AzMigrateTestMigrationCleanup</span><span class="sxs-lookup"><span data-stu-id="d6a2f-101">Start-AzMigrateTestMigrationCleanup</span></span>

## <span data-ttu-id="d6a2f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d6a2f-102">SYNOPSIS</span></span>
<span data-ttu-id="d6a2f-103">Pulisce la migrazione dei test per il server di replica.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-103">Cleans up the test migration for the replicating server.</span></span>

## <span data-ttu-id="d6a2f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d6a2f-104">SYNTAX</span></span>

### <span data-ttu-id="d6a2f-105">ByIDVMwareCbt (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d6a2f-105">ByIDVMwareCbt (Default)</span></span>
```
Start-AzMigrateTestMigrationCleanup -TargetObjectID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d6a2f-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="d6a2f-106">ByInputObjectVMwareCbt</span></span>
```
Start-AzMigrateTestMigrationCleanup -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d6a2f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d6a2f-107">DESCRIPTION</span></span>
<span data-ttu-id="d6a2f-108">Il cmdlet Start-AzMigrateTestMigrationCleanup avvia la pulizia della migrazione di test per il server di replica.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-108">The Start-AzMigrateTestMigrationCleanup cmdlet initiates the clean up of the test migration for the replicating server.</span></span>

## <span data-ttu-id="d6a2f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d6a2f-109">EXAMPLES</span></span>

### <span data-ttu-id="d6a2f-110">Esempio 1: per ID macchina.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-110">Example 1: By machine id.</span></span>
```powershell
PS C:\> Start-AzMigrateTestMigrationCleanup -TargetObjectID '/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f'


ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Test Migrate Cleanup
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : TestMigrateCleanup
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs

```

<span data-ttu-id="d6a2f-111">Per ID macchina.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-111">By machine id.</span></span>

### <span data-ttu-id="d6a2f-112">Esempio 2: per oggetto di input</span><span class="sxs-lookup"><span data-stu-id="d6a2f-112">Example 2: By input object</span></span>
```powershell
PS C:\> $obj = Get-AzMigrateServerReplication -TargetObjectID $env.srsMachineId -SubscriptionId $env.srsSubscriptionId
PS C:\> Start-AzMigrateTestMigrationCleanup -InputObject $ob


AllowedOperation            : {DisableMigration, TestMigrate, Migrate}

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Test Migrate Cleanup
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : TestMigrateCleanup
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs

```

<span data-ttu-id="d6a2f-113">Per oggetto input.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-113">By input object.</span></span>

## <span data-ttu-id="d6a2f-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d6a2f-114">PARAMETERS</span></span>

### <span data-ttu-id="d6a2f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6a2f-115">-DefaultProfile</span></span>
<span data-ttu-id="d6a2f-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6a2f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6a2f-117">-InputObject</span></span>
<span data-ttu-id="d6a2f-118">Specifica il server di replica per cui deve essere avviata la pulizia della migrazione di test.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-118">Specifies the replicating server for which the test migration cleanup needs to be initiated.</span></span>
<span data-ttu-id="d6a2f-119">L'oggetto server può essere recuperato usando il cmdlet Get-AzMigrateServerReplication per creare, vedi la sezione Note per le proprietà di INPUTOBJECT e crea una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-119">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IMigrationItem
Parameter Sets: ByInputObjectVMwareCbt
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6a2f-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d6a2f-120">-SubscriptionId</span></span>
<span data-ttu-id="d6a2f-121">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-121">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="d6a2f-122">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="d6a2f-122">-TargetObjectID</span></span>
<span data-ttu-id="d6a2f-123">Specifica il server di replica per cui deve essere avviata la pulizia della migrazione di test.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-123">Specifies the replicating server for which the test migration cleanup needs to be initiated.</span></span>
<span data-ttu-id="d6a2f-124">L'ID deve essere recuperato usando il cmdlet Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-124">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIDVMwareCbt
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6a2f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6a2f-125">CommonParameters</span></span>
<span data-ttu-id="d6a2f-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6a2f-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d6a2f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6a2f-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d6a2f-128">INPUTS</span></span>

## <span data-ttu-id="d6a2f-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d6a2f-129">OUTPUTS</span></span>

### <span data-ttu-id="d6a2f-130">Microsoft. Azure. PowerShell. Cmdlets. migrate. Models. Api20180110. IJob</span><span class="sxs-lookup"><span data-stu-id="d6a2f-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="d6a2f-131">Note</span><span class="sxs-lookup"><span data-stu-id="d6a2f-131">NOTES</span></span>

<span data-ttu-id="d6a2f-132">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d6a2f-132">ALIASES</span></span>

<span data-ttu-id="d6a2f-133">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d6a2f-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d6a2f-134">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d6a2f-135">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d6a2f-136">INPUTOBJECT <IMigrationItem> : specifica il server di replica per cui deve essere avviata la pulizia della migrazione di test.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-136">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the test migration cleanup needs to be initiated.</span></span> <span data-ttu-id="d6a2f-137">L'oggetto server può essere recuperato usando il cmdlet Get-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="d6a2f-137">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet</span></span>
  - <span data-ttu-id="d6a2f-138">`[Location <String>]`: Percorso delle risorse</span><span class="sxs-lookup"><span data-stu-id="d6a2f-138">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="d6a2f-139">`[CurrentJobId <String>]`: ID ARM del processo in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-139">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="d6a2f-140">`[CurrentJobName <String>]`: Nome processo.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-140">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="d6a2f-141">`[CurrentJobStartTime <DateTime?>]`: L'ora di inizio del processo.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-141">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="d6a2f-142">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Impostazioni personalizzate del provider di migrazione.</span><span class="sxs-lookup"><span data-stu-id="d6a2f-142">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="d6a2f-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d6a2f-143">RELATED LINKS</span></span>

