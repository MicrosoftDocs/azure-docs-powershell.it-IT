---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/start-azmigratetestmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigration.md
ms.openlocfilehash: 2c0582f8e91218679b9fbaeb3192e15f2848fd1e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009566"
---
# <span data-ttu-id="3711b-101">Start-AzMigrateTestMigration</span><span class="sxs-lookup"><span data-stu-id="3711b-101">Start-AzMigrateTestMigration</span></span>

## <span data-ttu-id="3711b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3711b-102">SYNOPSIS</span></span>
<span data-ttu-id="3711b-103">Avvia la migrazione di test per il server che replica.</span><span class="sxs-lookup"><span data-stu-id="3711b-103">Starts the test migration for the replicating server.</span></span>

## <span data-ttu-id="3711b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3711b-104">SYNTAX</span></span>

### <span data-ttu-id="3711b-105">ByIDVMwareCbt (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3711b-105">ByIDVMwareCbt (Default)</span></span>
```
Start-AzMigrateTestMigration -TargetObjectID <String> -TestNetworkID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3711b-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="3711b-106">ByInputObjectVMwareCbt</span></span>
```
Start-AzMigrateTestMigration -InputObject <IMigrationItem> -TestNetworkID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="3711b-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3711b-107">DESCRIPTION</span></span>
<span data-ttu-id="3711b-108">Il cmdlet Start-AzMigrateTestMigration avvia la migrazione di test per il server di replica.</span><span class="sxs-lookup"><span data-stu-id="3711b-108">The Start-AzMigrateTestMigration cmdlet initiates the test migration for the replicating server.</span></span>

## <span data-ttu-id="3711b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3711b-109">EXAMPLES</span></span>

### <span data-ttu-id="3711b-110">Esempio 1: Per ID computer.</span><span class="sxs-lookup"><span data-stu-id="3711b-110">Example 1: By machine id.</span></span>
```powershell
PS C:\> Start-AzMigrateTestMigration -TargetObjectID '/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f' -TestNetworkId '/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG/providers/Microsoft.Network/virtualNetworks/AzMigrateTargetNetwork


ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Test Migrate
Id                               : /Subscriptions/xxx-xxx-xxxresourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : TestMigrate
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs

```

<span data-ttu-id="3711b-111">Per ID computer.</span><span class="sxs-lookup"><span data-stu-id="3711b-111">By machine id.</span></span>

### <span data-ttu-id="3711b-112">Esempio 2: Per oggetto di input</span><span class="sxs-lookup"><span data-stu-id="3711b-112">Example 2: By input object</span></span>
```powershell
PS C:\> $obj = Get-AzMigrateServerReplication -TargetObjectID $env.srsMachineId -SubscriptionId $env.srsSubscriptionId
PS C:\> Start-AzMigrateTestMigration -InputObject $obj -TestNetworkId '/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG/providers/Microsoft.Network/virtualNetworks/AzMigrateTargetNetwork


ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Test Migrate
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : TestMigrate
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs

```

<span data-ttu-id="3711b-113">Per oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="3711b-113">By input object.</span></span>

## <span data-ttu-id="3711b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3711b-114">PARAMETERS</span></span>

### <span data-ttu-id="3711b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3711b-115">-DefaultProfile</span></span>
<span data-ttu-id="3711b-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3711b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3711b-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3711b-117">-InputObject</span></span>
<span data-ttu-id="3711b-118">Specifica il server di replica per cui deve essere avviata la migrazione di test.</span><span class="sxs-lookup"><span data-stu-id="3711b-118">Specifies the replicating server for which the test migration needs to be initiated.</span></span>
<span data-ttu-id="3711b-119">L'oggetto server può essere recuperato usando il cmdlet Get-AzMigrateServerReplication server.</span><span class="sxs-lookup"><span data-stu-id="3711b-119">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="3711b-120">Per creare, vedere la sezione NOTE per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="3711b-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3711b-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3711b-121">-SubscriptionId</span></span>
<span data-ttu-id="3711b-122">ID sottoscrizione Azure.</span><span class="sxs-lookup"><span data-stu-id="3711b-122">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="3711b-123">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="3711b-123">-TargetObjectID</span></span>
<span data-ttu-id="3711b-124">Specifica il server di replica per cui deve essere avviata la migrazione di test.</span><span class="sxs-lookup"><span data-stu-id="3711b-124">Specifies the replicating server for which the test migration needs to be initiated.</span></span>
<span data-ttu-id="3711b-125">L'ID deve essere recuperato con il cmdlet Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="3711b-125">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="3711b-126">-TestNetworkID</span><span class="sxs-lookup"><span data-stu-id="3711b-126">-TestNetworkID</span></span>
<span data-ttu-id="3711b-127">Aggiorna l'ID rete virtuale all'interno della sottoscrizione di Azure di destinazione da usare per la migrazione di test.</span><span class="sxs-lookup"><span data-stu-id="3711b-127">Updates the Virtual Network id within the destination Azure subscription to be used for test migration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3711b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3711b-128">CommonParameters</span></span>
<span data-ttu-id="3711b-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3711b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3711b-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3711b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3711b-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="3711b-131">INPUTS</span></span>

## <span data-ttu-id="3711b-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3711b-132">OUTPUTS</span></span>

### <span data-ttu-id="3711b-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="3711b-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="3711b-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="3711b-134">NOTES</span></span>

<span data-ttu-id="3711b-135">ALIAS</span><span class="sxs-lookup"><span data-stu-id="3711b-135">ALIASES</span></span>

<span data-ttu-id="3711b-136">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="3711b-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3711b-137">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="3711b-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3711b-138">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3711b-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3711b-139">INPUTOBJECT: specifica il server di replica per cui deve essere avviata la migrazione <IMigrationItem> di test.</span><span class="sxs-lookup"><span data-stu-id="3711b-139">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the test migration needs to be initiated.</span></span> <span data-ttu-id="3711b-140">L'oggetto server può essere recuperato usando il cmdlet Get-AzMigrateServerReplication server.</span><span class="sxs-lookup"><span data-stu-id="3711b-140">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="3711b-141">`[Location <String>]`: Posizione risorsa</span><span class="sxs-lookup"><span data-stu-id="3711b-141">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="3711b-142">`[CurrentJobId <String>]`: id ARM del processo eseguito.</span><span class="sxs-lookup"><span data-stu-id="3711b-142">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="3711b-143">`[CurrentJobName <String>]`: nome del processo.</span><span class="sxs-lookup"><span data-stu-id="3711b-143">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="3711b-144">`[CurrentJobStartTime <DateTime?>]`: ora di inizio del processo.</span><span class="sxs-lookup"><span data-stu-id="3711b-144">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="3711b-145">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: le impostazioni personalizzate del provider di migrazione.</span><span class="sxs-lookup"><span data-stu-id="3711b-145">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="3711b-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3711b-146">RELATED LINKS</span></span>

