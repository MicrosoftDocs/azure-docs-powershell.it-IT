---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/restart-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Restart-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Restart-AzMigrateServerReplication.md
ms.openlocfilehash: 35bf416249f24d7158720e2a9c28230da3f4f291
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363590"
---
# <span data-ttu-id="68dd6-101">Restart-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="68dd6-101">Restart-AzMigrateServerReplication</span></span>

## <span data-ttu-id="68dd6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="68dd6-102">SYNOPSIS</span></span>
<span data-ttu-id="68dd6-103">Riavvia la replica per il server specificato.</span><span class="sxs-lookup"><span data-stu-id="68dd6-103">Restarts the replication for specified server.</span></span>

## <span data-ttu-id="68dd6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="68dd6-104">SYNTAX</span></span>

### <span data-ttu-id="68dd6-105">ByIDVMwareCbt (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="68dd6-105">ByIDVMwareCbt (Default)</span></span>
```
Restart-AzMigrateServerReplication -TargetObjectID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="68dd6-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="68dd6-106">ByInputObjectVMwareCbt</span></span>
```
Restart-AzMigrateServerReplication -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="68dd6-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="68dd6-107">DESCRIPTION</span></span>
<span data-ttu-id="68dd6-108">Il cmdlet Restart-AzMigrateServerReplication consente di riparare la replica per il server specificato.</span><span class="sxs-lookup"><span data-stu-id="68dd6-108">The Restart-AzMigrateServerReplication cmdlet repairs the replication for the specified server.</span></span>

## <span data-ttu-id="68dd6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="68dd6-109">EXAMPLES</span></span>

### <span data-ttu-id="68dd6-110">Esempio 1: in base all'ID.</span><span class="sxs-lookup"><span data-stu-id="68dd6-110">Example 1: By id.</span></span>
```powershell
PS C:\> Restart-AzMigrateServerReplication -TargetObjectID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f"

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Restart
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Restart
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="68dd6-111">Per ID.</span><span class="sxs-lookup"><span data-stu-id="68dd6-111">By id.</span></span>

### <span data-ttu-id="68dd6-112">Esempio 2: per oggetto di input</span><span class="sxs-lookup"><span data-stu-id="68dd6-112">Example 2: By Input Object</span></span>
```powershell
PS C:\> $obj = Get-AzMigrateServerReplication -TargetObjectID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f"
PS C:\> $output = Restart-AzMigrateServerReplication -InputObject $obj
ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Restart
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Restart
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="68dd6-113">Per oggetto input.</span><span class="sxs-lookup"><span data-stu-id="68dd6-113">By Input Object.</span></span>

## <span data-ttu-id="68dd6-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="68dd6-114">PARAMETERS</span></span>

### <span data-ttu-id="68dd6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68dd6-115">-DefaultProfile</span></span>
<span data-ttu-id="68dd6-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="68dd6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68dd6-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68dd6-117">-InputObject</span></span>
<span data-ttu-id="68dd6-118">Specifica l'oggetto computer del server di replica.</span><span class="sxs-lookup"><span data-stu-id="68dd6-118">Specifies the machine object of the replicating server.</span></span>
<span data-ttu-id="68dd6-119">Per costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="68dd6-119">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="68dd6-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="68dd6-120">-SubscriptionId</span></span>
<span data-ttu-id="68dd6-121">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="68dd6-121">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="68dd6-122">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="68dd6-122">-TargetObjectID</span></span>
<span data-ttu-id="68dd6-123">Specifica il server replcating per cui deve essere avviata la risincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="68dd6-123">Specifies the replcating server for which the resync needs to be initiated.</span></span>
<span data-ttu-id="68dd6-124">L'ID deve essere recuperato usando il cmdlet Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="68dd6-124">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="68dd6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68dd6-125">CommonParameters</span></span>
<span data-ttu-id="68dd6-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68dd6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68dd6-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="68dd6-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68dd6-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="68dd6-128">INPUTS</span></span>

## <span data-ttu-id="68dd6-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="68dd6-129">OUTPUTS</span></span>

### <span data-ttu-id="68dd6-130">Microsoft. Azure. PowerShell. Cmdlets. migrate. Models. Api20180110. IJob</span><span class="sxs-lookup"><span data-stu-id="68dd6-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="68dd6-131">Note</span><span class="sxs-lookup"><span data-stu-id="68dd6-131">NOTES</span></span>

<span data-ttu-id="68dd6-132">ALIAS</span><span class="sxs-lookup"><span data-stu-id="68dd6-132">ALIASES</span></span>

<span data-ttu-id="68dd6-133">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="68dd6-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="68dd6-134">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="68dd6-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="68dd6-135">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="68dd6-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="68dd6-136">INPUTOBJECT <IMigrationItem> : specifica l'oggetto computer del server di replica.</span><span class="sxs-lookup"><span data-stu-id="68dd6-136">INPUTOBJECT <IMigrationItem>: Specifies the machine object of the replicating server.</span></span>
  - <span data-ttu-id="68dd6-137">`[Location <String>]`: Percorso delle risorse</span><span class="sxs-lookup"><span data-stu-id="68dd6-137">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="68dd6-138">`[CurrentJobId <String>]`: ID ARM del processo in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="68dd6-138">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="68dd6-139">`[CurrentJobName <String>]`: Nome processo.</span><span class="sxs-lookup"><span data-stu-id="68dd6-139">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="68dd6-140">`[CurrentJobStartTime <DateTime?>]`: L'ora di inizio del processo.</span><span class="sxs-lookup"><span data-stu-id="68dd6-140">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="68dd6-141">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Impostazioni personalizzate del provider di migrazione.</span><span class="sxs-lookup"><span data-stu-id="68dd6-141">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="68dd6-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="68dd6-142">RELATED LINKS</span></span>

