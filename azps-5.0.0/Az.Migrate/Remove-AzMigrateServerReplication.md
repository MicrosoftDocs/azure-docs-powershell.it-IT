---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/remove-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateServerReplication.md
ms.openlocfilehash: e9e6d3f9c045b9ff9cc2d5a4860b2c7fc5559f14
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202089"
---
# <span data-ttu-id="333a4-101">Remove-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="333a4-101">Remove-AzMigrateServerReplication</span></span>

## <span data-ttu-id="333a4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="333a4-102">SYNOPSIS</span></span>
<span data-ttu-id="333a4-103">Interrompe la replica per il server migrato.</span><span class="sxs-lookup"><span data-stu-id="333a4-103">Stops replication for the migrated server.</span></span>

## <span data-ttu-id="333a4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="333a4-104">SYNTAX</span></span>

### <span data-ttu-id="333a4-105">ByIDVMwareCbt (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="333a4-105">ByIDVMwareCbt (Default)</span></span>
```
Remove-AzMigrateServerReplication -TargetObjectID <String> [-SubscriptionId <String>] [-ForceRemove <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="333a4-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="333a4-106">ByInputObjectVMwareCbt</span></span>
```
Remove-AzMigrateServerReplication -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-ForceRemove <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="333a4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="333a4-107">DESCRIPTION</span></span>
<span data-ttu-id="333a4-108">Il cmdlet Remove-AzMigrateServerReplication interrompe la replica per un server migrato.</span><span class="sxs-lookup"><span data-stu-id="333a4-108">The Remove-AzMigrateServerReplication cmdlet stops the replication for a migrated server.</span></span>

## <span data-ttu-id="333a4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="333a4-109">EXAMPLES</span></span>

### <span data-ttu-id="333a4-110">Esempio 1: Rimuovi per ID.</span><span class="sxs-lookup"><span data-stu-id="333a4-110">Example 1: Remove by id.</span></span>
```powershell
PS C:\> Remove-AzMigrateServerReplication -TargetObjectID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f"

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Disable
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Disable
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs

```

<span data-ttu-id="333a4-111">Risincronizzare in base all'ID.</span><span class="sxs-lookup"><span data-stu-id="333a4-111">Resync by id.</span></span>

### <span data-ttu-id="333a4-112">Esempio 2: Rimuovi per oggetto di input</span><span class="sxs-lookup"><span data-stu-id="333a4-112">Example 2: Remove by Input Object</span></span>
```powershell
PS C:\> $obj = Get-AzMigrateServerReplication -TargetObjectID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f"
PS C:\> Remove-AzMigrateServerReplication -InputObject $obj


ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Disable
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Disable
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="333a4-113">Per nome.</span><span class="sxs-lookup"><span data-stu-id="333a4-113">By name.</span></span>

## <span data-ttu-id="333a4-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="333a4-114">PARAMETERS</span></span>

### <span data-ttu-id="333a4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="333a4-115">-DefaultProfile</span></span>
<span data-ttu-id="333a4-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="333a4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="333a4-117">-ForceRemove</span><span class="sxs-lookup"><span data-stu-id="333a4-117">-ForceRemove</span></span>
<span data-ttu-id="333a4-118">Specifica se la replica deve essere forzata.</span><span class="sxs-lookup"><span data-stu-id="333a4-118">Specifies whether the replication needs to be force removed.</span></span>

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

### <span data-ttu-id="333a4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="333a4-119">-InputObject</span></span>
<span data-ttu-id="333a4-120">Specifica l'oggetto computer del server di replica.</span><span class="sxs-lookup"><span data-stu-id="333a4-120">Specifies the machine object of the replicating server.</span></span>
<span data-ttu-id="333a4-121">Per costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="333a4-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="333a4-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="333a4-122">-SubscriptionId</span></span>
<span data-ttu-id="333a4-123">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="333a4-123">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="333a4-124">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="333a4-124">-TargetObjectID</span></span>
<span data-ttu-id="333a4-125">Specifica il server replcating per cui deve essere disabilitato replicatio.</span><span class="sxs-lookup"><span data-stu-id="333a4-125">Specifies the replcating server for which the replicatio needs to be disabled.</span></span>
<span data-ttu-id="333a4-126">L'ID deve essere recuperato usando il cmdlet Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="333a4-126">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="333a4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="333a4-127">CommonParameters</span></span>
<span data-ttu-id="333a4-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="333a4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="333a4-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="333a4-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="333a4-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="333a4-130">INPUTS</span></span>

## <span data-ttu-id="333a4-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="333a4-131">OUTPUTS</span></span>

### <span data-ttu-id="333a4-132">Microsoft. Azure. PowerShell. Cmdlets. migrate. Models. Api20180110. IJob</span><span class="sxs-lookup"><span data-stu-id="333a4-132">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="333a4-133">Note</span><span class="sxs-lookup"><span data-stu-id="333a4-133">NOTES</span></span>

<span data-ttu-id="333a4-134">ALIAS</span><span class="sxs-lookup"><span data-stu-id="333a4-134">ALIASES</span></span>

<span data-ttu-id="333a4-135">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="333a4-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="333a4-136">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="333a4-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="333a4-137">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="333a4-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="333a4-138">INPUTOBJECT <IMigrationItem> : specifica l'oggetto computer del server di replica.</span><span class="sxs-lookup"><span data-stu-id="333a4-138">INPUTOBJECT <IMigrationItem>: Specifies the machine object of the replicating server.</span></span>
  - <span data-ttu-id="333a4-139">`[Location <String>]`: Percorso delle risorse</span><span class="sxs-lookup"><span data-stu-id="333a4-139">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="333a4-140">`[CurrentJobId <String>]`: ID ARM del processo in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="333a4-140">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="333a4-141">`[CurrentJobName <String>]`: Nome processo.</span><span class="sxs-lookup"><span data-stu-id="333a4-141">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="333a4-142">`[CurrentJobStartTime <DateTime?>]`: L'ora di inizio del processo.</span><span class="sxs-lookup"><span data-stu-id="333a4-142">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="333a4-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Impostazioni personalizzate del provider di migrazione.</span><span class="sxs-lookup"><span data-stu-id="333a4-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="333a4-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="333a4-144">RELATED LINKS</span></span>

