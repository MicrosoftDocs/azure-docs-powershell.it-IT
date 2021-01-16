---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/set-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Set-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Set-AzMigrateServerReplication.md
ms.openlocfilehash: bb7f951403fd2298a2890f0b92f756c0417e94c9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363579"
---
# <span data-ttu-id="764ca-101">Set-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="764ca-101">Set-AzMigrateServerReplication</span></span>

## <span data-ttu-id="764ca-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="764ca-102">SYNOPSIS</span></span>
<span data-ttu-id="764ca-103">Aggiorna le proprietà di destinazione per il server di replica.</span><span class="sxs-lookup"><span data-stu-id="764ca-103">Updates the target properties for the replicating server.</span></span>

## <span data-ttu-id="764ca-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="764ca-104">SYNTAX</span></span>

### <span data-ttu-id="764ca-105">ByIDVMwareCbt (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="764ca-105">ByIDVMwareCbt (Default)</span></span>
```
Set-AzMigrateServerReplication -TargetObjectID <String> [-NicToUpdate <IVMwareCbtNicInput[]>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetNetworkId <String>] [-TargetResourceGroupID <String>] [-TargetVMName <String>]
 [-TargetVMSize <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="764ca-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="764ca-106">ByInputObjectVMwareCbt</span></span>
```
Set-AzMigrateServerReplication -InputObject <IMigrationItem> [-NicToUpdate <IVMwareCbtNicInput[]>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetNetworkId <String>] [-TargetResourceGroupID <String>] [-TargetVMName <String>]
 [-TargetVMSize <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="764ca-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="764ca-107">DESCRIPTION</span></span>
<span data-ttu-id="764ca-108">Il cmdlet Set-AzMigrateServerReplication aggiorna le proprietà di destinazione per il server di replica.</span><span class="sxs-lookup"><span data-stu-id="764ca-108">The Set-AzMigrateServerReplication cmdlet updates the target properties for the replicating server.</span></span>

## <span data-ttu-id="764ca-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="764ca-109">EXAMPLES</span></span>

### <span data-ttu-id="764ca-110">Esempio 1: aggiornamento per ID</span><span class="sxs-lookup"><span data-stu-id="764ca-110">Example 1: Update by id</span></span>
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

<span data-ttu-id="764ca-111">Per ID.</span><span class="sxs-lookup"><span data-stu-id="764ca-111">By id.</span></span>

## <span data-ttu-id="764ca-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="764ca-112">PARAMETERS</span></span>

### <span data-ttu-id="764ca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="764ca-113">-DefaultProfile</span></span>
<span data-ttu-id="764ca-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="764ca-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="764ca-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="764ca-115">-InputObject</span></span>
<span data-ttu-id="764ca-116">Specifica il server di replica per cui devono essere aggiornate le proprietà.</span><span class="sxs-lookup"><span data-stu-id="764ca-116">Specifies the replicating server for which the properties need to be updated.</span></span>
<span data-ttu-id="764ca-117">L'oggetto server può essere recuperato usando il cmdlet Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="764ca-117">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="764ca-118">Per costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="764ca-118">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="764ca-119">-NicToUpdate</span><span class="sxs-lookup"><span data-stu-id="764ca-119">-NicToUpdate</span></span>
<span data-ttu-id="764ca-120">Aggiorna la scheda NIC per la VM di Azure da creare.</span><span class="sxs-lookup"><span data-stu-id="764ca-120">Updates the NIC for the Azure VM to be created.</span></span>
<span data-ttu-id="764ca-121">Per costruire, vedere la sezione Note per le proprietà di NICTOUPDATE e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="764ca-121">To construct, see NOTES section for NICTOUPDATE properties and create a hash table.</span></span>

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

### <span data-ttu-id="764ca-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="764ca-122">-SubscriptionId</span></span>
<span data-ttu-id="764ca-123">ID abbonamento.</span><span class="sxs-lookup"><span data-stu-id="764ca-123">The subscription Id.</span></span>

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

### <span data-ttu-id="764ca-124">-TargetAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="764ca-124">-TargetAvailabilitySet</span></span>
<span data-ttu-id="764ca-125">Specifica il set di disponibilità da usare per la creazione di VM.</span><span class="sxs-lookup"><span data-stu-id="764ca-125">Specifies the Availability Set to be used for VM creation.</span></span>

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

### <span data-ttu-id="764ca-126">-TargetAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="764ca-126">-TargetAvailabilityZone</span></span>
<span data-ttu-id="764ca-127">Specifica l'area di disponibilità da usare per la creazione di VM.</span><span class="sxs-lookup"><span data-stu-id="764ca-127">Specifies the Availability Zone to be used for VM creation.</span></span>

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

### <span data-ttu-id="764ca-128">-TargetNetworkId</span><span class="sxs-lookup"><span data-stu-id="764ca-128">-TargetNetworkId</span></span>
<span data-ttu-id="764ca-129">Aggiorna l'ID della rete virtuale nell'abbonamento a destinazione Azure a cui è necessario eseguire la migrazione del server.</span><span class="sxs-lookup"><span data-stu-id="764ca-129">Updates the Virtual Network id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="764ca-130">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="764ca-130">-TargetObjectID</span></span>
<span data-ttu-id="764ca-131">Specifica il server replcating per cui devono essere aggiornate le proprietà.</span><span class="sxs-lookup"><span data-stu-id="764ca-131">Specifies the replcating server for which the properties need to be updated.</span></span>
<span data-ttu-id="764ca-132">L'ID deve essere recuperato usando il cmdlet Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="764ca-132">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="764ca-133">-TargetResourceGroupID</span><span class="sxs-lookup"><span data-stu-id="764ca-133">-TargetResourceGroupID</span></span>
<span data-ttu-id="764ca-134">Aggiorna l'ID del gruppo di risorse nell'abbonamento a destinazione Azure a cui deve essere eseguita la migrazione del server.</span><span class="sxs-lookup"><span data-stu-id="764ca-134">Updates the Resource Group id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="764ca-135">-TargetVMName</span><span class="sxs-lookup"><span data-stu-id="764ca-135">-TargetVMName</span></span>
<span data-ttu-id="764ca-136">Specifica il server replcating per cui devono essere aggiornate le proprietà.</span><span class="sxs-lookup"><span data-stu-id="764ca-136">Specifies the replcating server for which the properties need to be updated.</span></span>
<span data-ttu-id="764ca-137">L'ID deve essere recuperato usando il cmdlet Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="764ca-137">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="764ca-138">-TargetVMSize</span><span class="sxs-lookup"><span data-stu-id="764ca-138">-TargetVMSize</span></span>
<span data-ttu-id="764ca-139">Aggiorna l'USK di Azure VM da creare.</span><span class="sxs-lookup"><span data-stu-id="764ca-139">Updates the SKU of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="764ca-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="764ca-140">CommonParameters</span></span>
<span data-ttu-id="764ca-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="764ca-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="764ca-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="764ca-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="764ca-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="764ca-143">INPUTS</span></span>

## <span data-ttu-id="764ca-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="764ca-144">OUTPUTS</span></span>

### <span data-ttu-id="764ca-145">Microsoft. Azure. PowerShell. Cmdlets. migrate. Models. Api20180110. IJob</span><span class="sxs-lookup"><span data-stu-id="764ca-145">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="764ca-146">Note</span><span class="sxs-lookup"><span data-stu-id="764ca-146">NOTES</span></span>

<span data-ttu-id="764ca-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="764ca-147">ALIASES</span></span>

<span data-ttu-id="764ca-148">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="764ca-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="764ca-149">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="764ca-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="764ca-150">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="764ca-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="764ca-151">INPUTOBJECT <IMigrationItem> : specifica il server di replica per cui devono essere aggiornate le proprietà.</span><span class="sxs-lookup"><span data-stu-id="764ca-151">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the properties need to be updated.</span></span> <span data-ttu-id="764ca-152">L'oggetto server può essere recuperato usando il cmdlet Get-AzMigrateServerReplication.</span><span class="sxs-lookup"><span data-stu-id="764ca-152">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="764ca-153">`[Location <String>]`: Percorso delle risorse</span><span class="sxs-lookup"><span data-stu-id="764ca-153">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="764ca-154">`[CurrentJobId <String>]`: ID ARM del processo in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="764ca-154">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="764ca-155">`[CurrentJobName <String>]`: Nome processo.</span><span class="sxs-lookup"><span data-stu-id="764ca-155">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="764ca-156">`[CurrentJobStartTime <DateTime?>]`: L'ora di inizio del processo.</span><span class="sxs-lookup"><span data-stu-id="764ca-156">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="764ca-157">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Impostazioni personalizzate del provider di migrazione.</span><span class="sxs-lookup"><span data-stu-id="764ca-157">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

<span data-ttu-id="764ca-158">NICTOUPDATE <IVMwareCbtNicInput [] >: aggiorna la scheda NIC per la VM di Azure da creare.</span><span class="sxs-lookup"><span data-stu-id="764ca-158">NICTOUPDATE <IVMwareCbtNicInput[]>: Updates the NIC for the Azure VM to be created.</span></span>
  - <span data-ttu-id="764ca-159">`IsPrimaryNic <String>`: Valore che indica se si tratta della scheda NIC primaria.</span><span class="sxs-lookup"><span data-stu-id="764ca-159">`IsPrimaryNic <String>`: A value indicating whether this is the primary NIC.</span></span>
  - <span data-ttu-id="764ca-160">`NicId <String>`: ID NIC.</span><span class="sxs-lookup"><span data-stu-id="764ca-160">`NicId <String>`: The NIC Id.</span></span>
  - <span data-ttu-id="764ca-161">`[IsSelectedForMigration <String>]`: Valore che indica se questa NIC è selezionata per la migrazione.</span><span class="sxs-lookup"><span data-stu-id="764ca-161">`[IsSelectedForMigration <String>]`: A value indicating whether this NIC is selected for migration.</span></span>
  - <span data-ttu-id="764ca-162">`[TargetStaticIPAddress <String>]`: Indirizzo IP statico.</span><span class="sxs-lookup"><span data-stu-id="764ca-162">`[TargetStaticIPAddress <String>]`: The static IP address.</span></span>
  - <span data-ttu-id="764ca-163">`[TargetSubnetName <String>]`: Nome subnet di destinazione.</span><span class="sxs-lookup"><span data-stu-id="764ca-163">`[TargetSubnetName <String>]`: Target subnet name.</span></span>

## <span data-ttu-id="764ca-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="764ca-164">RELATED LINKS</span></span>

