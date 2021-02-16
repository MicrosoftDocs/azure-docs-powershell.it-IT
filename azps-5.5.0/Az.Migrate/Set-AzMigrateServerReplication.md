---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/set-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Set-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Set-AzMigrateServerReplication.md
ms.openlocfilehash: 4c2afa4922d6e33493379739753856731020f321
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185046"
---
# <span data-ttu-id="cff24-101">Set-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="cff24-101">Set-AzMigrateServerReplication</span></span>

## <span data-ttu-id="cff24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cff24-102">SYNOPSIS</span></span>
<span data-ttu-id="cff24-103">Aggiorna le proprietà di destinazione per il server di replica.</span><span class="sxs-lookup"><span data-stu-id="cff24-103">Updates the target properties for the replicating server.</span></span>

## <span data-ttu-id="cff24-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cff24-104">SYNTAX</span></span>

### <span data-ttu-id="cff24-105">ByIDVMwareCbt (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cff24-105">ByIDVMwareCbt (Default)</span></span>
```
Set-AzMigrateServerReplication -TargetObjectID <String> [-NicToUpdate <IVMwareCbtNicInput[]>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetNetworkId <String>] [-TargetResourceGroupID <String>]
 [-TargetVMName <String>] [-TargetVMSize <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cff24-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="cff24-106">ByInputObjectVMwareCbt</span></span>
```
Set-AzMigrateServerReplication -InputObject <IMigrationItem> [-NicToUpdate <IVMwareCbtNicInput[]>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetNetworkId <String>] [-TargetResourceGroupID <String>]
 [-TargetVMName <String>] [-TargetVMSize <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="cff24-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cff24-107">DESCRIPTION</span></span>
<span data-ttu-id="cff24-108">Il Set-AzMigrateServerReplication cmdlet aggiorna le proprietà di destinazione per il server di replica.</span><span class="sxs-lookup"><span data-stu-id="cff24-108">The Set-AzMigrateServerReplication cmdlet updates the target properties for the replicating server.</span></span>

## <span data-ttu-id="cff24-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cff24-109">EXAMPLES</span></span>

### <span data-ttu-id="cff24-110">Esempio 1: Aggiornamento in base all'ID</span><span class="sxs-lookup"><span data-stu-id="cff24-110">Example 1: Update by id</span></span>
```powershell
PS C:\> Set-AzMigrateServerReplication -TargetObjectID '/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_500f44f8-2aa3-587b-8958-ead358639629' -TargetVMName 'rb-w2k12r2-1'

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Update
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Update
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="cff24-111">Per ID.</span><span class="sxs-lookup"><span data-stu-id="cff24-111">By id.</span></span>

## <span data-ttu-id="cff24-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cff24-112">PARAMETERS</span></span>

### <span data-ttu-id="cff24-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cff24-113">-DefaultProfile</span></span>
<span data-ttu-id="cff24-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cff24-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cff24-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cff24-115">-InputObject</span></span>
<span data-ttu-id="cff24-116">Specifica il server di replica per cui è necessario aggiornare le proprietà.</span><span class="sxs-lookup"><span data-stu-id="cff24-116">Specifies the replicating server for which the properties need to be updated.</span></span>
<span data-ttu-id="cff24-117">L'oggetto server può essere recuperato usando il cmdlet Get-AzMigrateServerReplication server.</span><span class="sxs-lookup"><span data-stu-id="cff24-117">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="cff24-118">Per creare, vedere la sezione NOTE per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="cff24-118">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cff24-119">-NicToUpdate</span><span class="sxs-lookup"><span data-stu-id="cff24-119">-NicToUpdate</span></span>
<span data-ttu-id="cff24-120">Aggiorna la scheda NIC per la macchina virtuale di Azure da creare.</span><span class="sxs-lookup"><span data-stu-id="cff24-120">Updates the NIC for the Azure VM to be created.</span></span>
<span data-ttu-id="cff24-121">Per creare, vedere la sezione NOTE per le proprietà NICTOUPDATE e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="cff24-121">To construct, see NOTES section for NICTOUPDATE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtNicInput[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cff24-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cff24-122">-SubscriptionId</span></span>
<span data-ttu-id="cff24-123">ID sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="cff24-123">The subscription Id.</span></span>

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

### <span data-ttu-id="cff24-124">-TargetAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="cff24-124">-TargetAvailabilitySet</span></span>
<span data-ttu-id="cff24-125">Specifica il set di disponibilità da usare per la creazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="cff24-125">Specifies the Availability Set to be used for VM creation.</span></span>

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

### <span data-ttu-id="cff24-126">-TargetAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="cff24-126">-TargetAvailabilityZone</span></span>
<span data-ttu-id="cff24-127">Specifica l'area di disponibilità da usare per la creazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="cff24-127">Specifies the Availability Zone to be used for VM creation.</span></span>

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

### <span data-ttu-id="cff24-128">-TargetBootDiagnosticsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cff24-128">-TargetBootDiagnosticsStorageAccount</span></span>
<span data-ttu-id="cff24-129">Specifica l'account di archiviazione da usare per la diagnostica di avvio.</span><span class="sxs-lookup"><span data-stu-id="cff24-129">Specifies the storage account to be used for boot diagnostics.</span></span>

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

### <span data-ttu-id="cff24-130">-TargetNetworkId</span><span class="sxs-lookup"><span data-stu-id="cff24-130">-TargetNetworkId</span></span>
<span data-ttu-id="cff24-131">Aggiorna l'ID rete virtuale all'interno della sottoscrizione di Destinazione di Azure in cui deve essere eseguita la migrazione del server.</span><span class="sxs-lookup"><span data-stu-id="cff24-131">Updates the Virtual Network id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="cff24-132">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="cff24-132">-TargetObjectID</span></span>
<span data-ttu-id="cff24-133">Specifica il server di replcating per cui è necessario aggiornare le proprietà.</span><span class="sxs-lookup"><span data-stu-id="cff24-133">Specifies the replcating server for which the properties need to be updated.</span></span>
<span data-ttu-id="cff24-134">L'ID deve essere recuperato con il cmdlet Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="cff24-134">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="cff24-135">-TargetResourceGroupID</span><span class="sxs-lookup"><span data-stu-id="cff24-135">-TargetResourceGroupID</span></span>
<span data-ttu-id="cff24-136">Aggiorna l'ID gruppo di risorse all'interno della sottoscrizione di Azure di destinazione in cui deve essere eseguita la migrazione del server.</span><span class="sxs-lookup"><span data-stu-id="cff24-136">Updates the Resource Group id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="cff24-137">-TargetVMName</span><span class="sxs-lookup"><span data-stu-id="cff24-137">-TargetVMName</span></span>
<span data-ttu-id="cff24-138">Specifica il server di replcating per cui è necessario aggiornare le proprietà.</span><span class="sxs-lookup"><span data-stu-id="cff24-138">Specifies the replcating server for which the properties need to be updated.</span></span>
<span data-ttu-id="cff24-139">L'ID deve essere recuperato con il cmdlet Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="cff24-139">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="cff24-140">-TargetVMSize</span><span class="sxs-lookup"><span data-stu-id="cff24-140">-TargetVMSize</span></span>
<span data-ttu-id="cff24-141">Aggiorna lo SKU della macchina virtuale di Azure da creare.</span><span class="sxs-lookup"><span data-stu-id="cff24-141">Updates the SKU of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="cff24-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cff24-142">CommonParameters</span></span>
<span data-ttu-id="cff24-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cff24-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cff24-144">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cff24-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cff24-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="cff24-145">INPUTS</span></span>

## <span data-ttu-id="cff24-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cff24-146">OUTPUTS</span></span>

### <span data-ttu-id="cff24-147">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="cff24-147">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="cff24-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="cff24-148">NOTES</span></span>

<span data-ttu-id="cff24-149">ALIAS</span><span class="sxs-lookup"><span data-stu-id="cff24-149">ALIASES</span></span>

<span data-ttu-id="cff24-150">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="cff24-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cff24-151">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="cff24-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cff24-152">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cff24-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cff24-153">INPUTOBJECT: specifica il server di replica per cui è necessario aggiornare <IMigrationItem> le proprietà.</span><span class="sxs-lookup"><span data-stu-id="cff24-153">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the properties need to be updated.</span></span> <span data-ttu-id="cff24-154">L'oggetto server può essere recuperato usando il cmdlet Get-AzMigrateServerReplication server.</span><span class="sxs-lookup"><span data-stu-id="cff24-154">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="cff24-155">`[Location <String>]`: Posizione risorsa</span><span class="sxs-lookup"><span data-stu-id="cff24-155">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="cff24-156">`[CurrentJobId <String>]`: id ARM del processo eseguito.</span><span class="sxs-lookup"><span data-stu-id="cff24-156">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="cff24-157">`[CurrentJobName <String>]`: nome del processo.</span><span class="sxs-lookup"><span data-stu-id="cff24-157">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="cff24-158">`[CurrentJobStartTime <DateTime?>]`: ora di inizio del processo.</span><span class="sxs-lookup"><span data-stu-id="cff24-158">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="cff24-159">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: le impostazioni personalizzate del provider di migrazione.</span><span class="sxs-lookup"><span data-stu-id="cff24-159">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

<span data-ttu-id="cff24-160">NICTOUPDATE <IVMwareCbtNicInput[]>: aggiorna il nic per la macchina virtuale di Azure da creare.</span><span class="sxs-lookup"><span data-stu-id="cff24-160">NICTOUPDATE <IVMwareCbtNicInput[]>: Updates the NIC for the Azure VM to be created.</span></span>
  - <span data-ttu-id="cff24-161">`IsPrimaryNic <String>`: valore che indica se si tratta della scheda NIC principale.</span><span class="sxs-lookup"><span data-stu-id="cff24-161">`IsPrimaryNic <String>`: A value indicating whether this is the primary NIC.</span></span>
  - <span data-ttu-id="cff24-162">`NicId <String>`: ID NIC.</span><span class="sxs-lookup"><span data-stu-id="cff24-162">`NicId <String>`: The NIC Id.</span></span>
  - <span data-ttu-id="cff24-163">`[IsSelectedForMigration <String>]`: valore che indica se questa scheda di rete è selezionata per la migrazione.</span><span class="sxs-lookup"><span data-stu-id="cff24-163">`[IsSelectedForMigration <String>]`: A value indicating whether this NIC is selected for migration.</span></span>
  - <span data-ttu-id="cff24-164">`[TargetStaticIPAddress <String>]`: l'indirizzo IP statico.</span><span class="sxs-lookup"><span data-stu-id="cff24-164">`[TargetStaticIPAddress <String>]`: The static IP address.</span></span>
  - <span data-ttu-id="cff24-165">`[TargetSubnetName <String>]`: nome subnet di destinazione.</span><span class="sxs-lookup"><span data-stu-id="cff24-165">`[TargetSubnetName <String>]`: Target subnet name.</span></span>

## <span data-ttu-id="cff24-166">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cff24-166">RELATED LINKS</span></span>

