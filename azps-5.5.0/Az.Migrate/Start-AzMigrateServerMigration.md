---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/start-azmigrateservermigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateServerMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateServerMigration.md
ms.openlocfilehash: 6a6eb5adb947793be1faf0d1d1921941e0d54065
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185054"
---
# <span data-ttu-id="b5992-101">Start-AzMigrateServerMigration</span><span class="sxs-lookup"><span data-stu-id="b5992-101">Start-AzMigrateServerMigration</span></span>

## <span data-ttu-id="b5992-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5992-102">SYNOPSIS</span></span>
<span data-ttu-id="b5992-103">Avvia la migrazione per il server replicante.</span><span class="sxs-lookup"><span data-stu-id="b5992-103">Starts the migration for the replicating server.</span></span>

## <span data-ttu-id="b5992-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b5992-104">SYNTAX</span></span>

### <span data-ttu-id="b5992-105">ByIDVMwareCbt (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b5992-105">ByIDVMwareCbt (Default)</span></span>
```
Start-AzMigrateServerMigration -TargetObjectID <String> [-SubscriptionId <String>] [-TurnOffSourceServer]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b5992-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="b5992-106">ByInputObjectVMwareCbt</span></span>
```
Start-AzMigrateServerMigration -InputObject <IMigrationItem> [-SubscriptionId <String>] [-TurnOffSourceServer]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b5992-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b5992-107">DESCRIPTION</span></span>
<span data-ttu-id="b5992-108">Avvia la migrazione per il server replicante.</span><span class="sxs-lookup"><span data-stu-id="b5992-108">Starts the migration for the replicating server.</span></span>

## <span data-ttu-id="b5992-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b5992-109">EXAMPLES</span></span>

### <span data-ttu-id="b5992-110">Esempio 1: Per ID</span><span class="sxs-lookup"><span data-stu-id="b5992-110">Example 1: By id</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Start-AzMigrateServerMigration -TargetObjectID "/Subscriptions/7xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_52f42ee7-8eb3-1aa4-e2d5-1ae83f86b085"

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Migrate
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Migrate
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="b5992-111">Per ID</span><span class="sxs-lookup"><span data-stu-id="b5992-111">By id</span></span>

## <span data-ttu-id="b5992-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5992-112">PARAMETERS</span></span>

### <span data-ttu-id="b5992-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5992-113">-DefaultProfile</span></span>
<span data-ttu-id="b5992-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b5992-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5992-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5992-115">-InputObject</span></span>
<span data-ttu-id="b5992-116">Specifica il server di replica per cui deve essere avviata la migrazione.</span><span class="sxs-lookup"><span data-stu-id="b5992-116">Specifies the replicating server for which migration needs to be initiated.</span></span>
<span data-ttu-id="b5992-117">L'oggetto server può essere recuperato usando il cmdlet Get-AzMigrateServerReplication server.</span><span class="sxs-lookup"><span data-stu-id="b5992-117">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="b5992-118">Per creare, vedere la sezione NOTE per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="b5992-118">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b5992-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b5992-119">-SubscriptionId</span></span>
<span data-ttu-id="b5992-120">ID sottoscrizione Azure.</span><span class="sxs-lookup"><span data-stu-id="b5992-120">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="b5992-121">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="b5992-121">-TargetObjectID</span></span>
<span data-ttu-id="b5992-122">Specifica il server di replcazione per il quale deve essere avviata la migrazione.</span><span class="sxs-lookup"><span data-stu-id="b5992-122">Specifies the replcating server for which migration needs to be initiated.</span></span>
<span data-ttu-id="b5992-123">L'ID deve essere recuperato con il cmdlet Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="b5992-123">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="b5992-124">-TurnOffSourceServer</span><span class="sxs-lookup"><span data-stu-id="b5992-124">-TurnOffSourceServer</span></span>
<span data-ttu-id="b5992-125">Specifica se il server di origine deve essere disattivato dopo la migrazione.</span><span class="sxs-lookup"><span data-stu-id="b5992-125">Specifies whether the source server should be turned off post migration.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5992-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5992-126">CommonParameters</span></span>
<span data-ttu-id="b5992-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5992-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5992-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b5992-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5992-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="b5992-129">INPUTS</span></span>

## <span data-ttu-id="b5992-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b5992-130">OUTPUTS</span></span>

### <span data-ttu-id="b5992-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="b5992-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="b5992-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="b5992-132">NOTES</span></span>

<span data-ttu-id="b5992-133">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b5992-133">ALIASES</span></span>

<span data-ttu-id="b5992-134">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="b5992-134">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b5992-135">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="b5992-135">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b5992-136">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b5992-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b5992-137">INPUTOBJECT: specifica il server di replica per cui deve essere avviata <IMigrationItem> la migrazione.</span><span class="sxs-lookup"><span data-stu-id="b5992-137">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which migration needs to be initiated.</span></span> <span data-ttu-id="b5992-138">L'oggetto server può essere recuperato usando il cmdlet Get-AzMigrateServerReplication server.</span><span class="sxs-lookup"><span data-stu-id="b5992-138">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="b5992-139">`[Location <String>]`: Posizione risorsa</span><span class="sxs-lookup"><span data-stu-id="b5992-139">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="b5992-140">`[CurrentJobId <String>]`: id ARM del processo eseguito.</span><span class="sxs-lookup"><span data-stu-id="b5992-140">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="b5992-141">`[CurrentJobName <String>]`: nome del processo.</span><span class="sxs-lookup"><span data-stu-id="b5992-141">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="b5992-142">`[CurrentJobStartTime <DateTime?>]`: ora di inizio del processo.</span><span class="sxs-lookup"><span data-stu-id="b5992-142">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="b5992-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: le impostazioni personalizzate del provider di migrazione.</span><span class="sxs-lookup"><span data-stu-id="b5992-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="b5992-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b5992-144">RELATED LINKS</span></span>

