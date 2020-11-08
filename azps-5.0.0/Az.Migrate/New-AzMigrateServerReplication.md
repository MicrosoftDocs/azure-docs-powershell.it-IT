---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateServerReplication.md
ms.openlocfilehash: 0ef21777f5a7f22fff5d9352f667d8968ff843f3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200776"
---
# <span data-ttu-id="236fe-101">New-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="236fe-101">New-AzMigrateServerReplication</span></span>

## <span data-ttu-id="236fe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="236fe-102">SYNOPSIS</span></span>
<span data-ttu-id="236fe-103">Avvia la replica per il server specificato.</span><span class="sxs-lookup"><span data-stu-id="236fe-103">Starts replication for the specified server.</span></span>

## <span data-ttu-id="236fe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="236fe-104">SYNTAX</span></span>

### <span data-ttu-id="236fe-105">ByIdDefaultUser (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="236fe-105">ByIdDefaultUser (Default)</span></span>
```
New-AzMigrateServerReplication -DiskType <DiskAccountType> -LicenseType <LicenseType> -MachineId <String>
 -OSDiskID <String> -TargetNetworkId <String> -TargetResourceGroupId <String> -TargetSubnetName <String>
 -TargetVMName <String> [-DiskEncryptionSetID <String>] [-PerformAutoResync <String>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="236fe-106">ByIdPowerUser</span><span class="sxs-lookup"><span data-stu-id="236fe-106">ByIdPowerUser</span></span>
```
New-AzMigrateServerReplication -DiskToInclude <IVMwareCbtDiskInput[]> -LicenseType <LicenseType>
 -MachineId <String> -TargetNetworkId <String> -TargetResourceGroupId <String> -TargetSubnetName <String>
 -TargetVMName <String> [-PerformAutoResync <String>] [-SubscriptionId <String>]
 [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="236fe-107">ByInputObjectDefaultUser</span><span class="sxs-lookup"><span data-stu-id="236fe-107">ByInputObjectDefaultUser</span></span>
```
New-AzMigrateServerReplication -DiskType <DiskAccountType> -InputObject <IVMwareMachine>
 -LicenseType <LicenseType> -OSDiskID <String> -TargetNetworkId <String> -TargetResourceGroupId <String>
 -TargetSubnetName <String> -TargetVMName <String> [-DiskEncryptionSetID <String>]
 [-PerformAutoResync <String>] [-SubscriptionId <String>] [-TargetAvailabilitySet <String>]
 [-TargetAvailabilityZone <String>] [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>]
 [-VMWarerunasaccountID <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="236fe-108">ByInputObjectPowerUser</span><span class="sxs-lookup"><span data-stu-id="236fe-108">ByInputObjectPowerUser</span></span>
```
New-AzMigrateServerReplication -DiskToInclude <IVMwareCbtDiskInput[]> -InputObject <IVMwareMachine>
 -LicenseType <LicenseType> -TargetNetworkId <String> -TargetResourceGroupId <String>
 -TargetSubnetName <String> -TargetVMName <String> [-PerformAutoResync <String>] [-SubscriptionId <String>]
 [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="236fe-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="236fe-109">DESCRIPTION</span></span>
<span data-ttu-id="236fe-110">Il cmdlet New-AzMigrateServerReplication avvia la replica per un determinato server individuato nel progetto di migrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="236fe-110">The New-AzMigrateServerReplication cmdlet starts the replication for a particular discovered server in the Azure Migrate project.</span></span>

## <span data-ttu-id="236fe-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="236fe-111">EXAMPLES</span></span>

### <span data-ttu-id="236fe-112">Esempio 1: quando esiste solo il disco del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="236fe-112">Example 1: When there is only OS disk</span></span>
```powershell
PS C:\> New-AzMigrateServerReplication -MachineId "/subscriptions/xxx-xxx-xxx4/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.OffAzure/VMwareSites/AzMigratePWSHTc8d1site/machines/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f" -LicenseType NoLicenseType -TargetResourceGroupId "/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG" -TargetNetworkId  "/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG/providers/Microsoft.Network/virtualNetworks/AzMigrateTargetNetwork" -TargetSubnetName default -TargetVMName "prsadhu-TestVM" -DiskType "Standard_LRS" -OSDiskID "6000C299-343d-7bcd-c05e-a94bd63316dd"

ActivityId                       : 68af14b4-46ae-48d1-b3e9-cdcffb9e8a93 ActivityId: 74d1a396-1d37-4264-8a5b-b727aaef0171
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 9/16/20 11:57:33 AM
Error                            : {}
FriendlyName                     : Enable
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b
Location                         :
Name                             : 997e2a92-5afe-49c7-a81a-89660aec9b7b
ScenarioName                     : Enable
StartTime                        : 9/16/20 11:57:32 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 42752b89-5fad-52fd-bf93-679fbdb6fed9
TargetObjectName                 : migrateAzMigratePWSHTc8d1sitepolicy
Task                             : {CloudPairingPrerequisitesCheck, CloudPairingPrepareSite}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="236fe-113">Questo è lo scenario in cui è presente un solo disco che deve essere protetto.</span><span class="sxs-lookup"><span data-stu-id="236fe-113">This is for the scenario, when there is only one single disk that has to be protected.</span></span>

### <span data-ttu-id="236fe-114">Esempio 2: quando sono presenti più dischi</span><span class="sxs-lookup"><span data-stu-id="236fe-114">Example 2: When there are multiple disks</span></span>
```powershell
PS C:\> $OSDisk = New-AzMigrateDiskMapping -DiskID '6000C299-343d-7bcd-c05e-a94bd63316dd' -DiskType 'Standard_LRS' -IsOSDisk 'true'
PS C:\> $DataDisk = New-AzMigrateDiskMapping -DiskID '7000C299-343d-7bcd-c05e-a94bd63316dd' -DiskType 'Standard_LRS' -IsOSDisk 'false'
PS C:\> $DisksToInclude += $OSDisk
PS C:\> $DisksToInclude += $DataDisk
PS C:\> New-AzMigrateServerReplication -MachineId "/subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.OffAzure/VMwareSites/AzMigratePWSHTc8d1site/machines/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f" -LicenseType NoLicenseType -TargetResourceGroupId "/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG" -TargetNetworkId  "/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG/providers/Microsoft.Network/virtualNetworks/AzMigrateTargetNetwork" -TargetSubnetName default -TargetVMName "prsadhu-TestVM" -DiskToInclude $DisksToInclude -PerformAutoResync true

ActivityId                       : 68af14b4-46ae-48d1-b3e9-cdcffb9e8a93 ActivityId: 74d1a396-1d37-4264-8a5b-b727aaef0171
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 9/16/20 11:57:33 AM
Error                            : {}
FriendlyName                     : Enable
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b
Location                         :
Name                             : 997e2a92-5afe-49c7-a81a-89660aec9b7b
ScenarioName                     : Enable
StartTime                        : 9/16/20 11:57:32 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 42752b89-5fad-52fd-bf93-679fbdb6fed9
TargetObjectName                 : migrateAzMigratePWSHTc8d1sitepolicy
Task                             : {CloudPairingPrerequisitesCheck, CloudPairingPrepareSite}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="236fe-115">Questo è lo scenario in cui sono presenti più dischi che devono essere protetti.</span><span class="sxs-lookup"><span data-stu-id="236fe-115">This is for the scenario, when there are multiple disks that has to be protected.</span></span>

## <span data-ttu-id="236fe-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="236fe-116">PARAMETERS</span></span>

### <span data-ttu-id="236fe-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="236fe-117">-DefaultProfile</span></span>
<span data-ttu-id="236fe-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="236fe-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="236fe-119">-DiskEncryptionSetID</span><span class="sxs-lookup"><span data-stu-id="236fe-119">-DiskEncryptionSetID</span></span>
<span data-ttu-id="236fe-120">Specifica il set di Encyption del disco da usare.</span><span class="sxs-lookup"><span data-stu-id="236fe-120">Specifies the disk encyption set to be used.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIdDefaultUser, ByInputObjectDefaultUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="236fe-121">-DiskToInclude</span><span class="sxs-lookup"><span data-stu-id="236fe-121">-DiskToInclude</span></span>
<span data-ttu-id="236fe-122">Specifica i dischi nel server di origine da includere per la replica.</span><span class="sxs-lookup"><span data-stu-id="236fe-122">Specifies the disks on the source server to be included for replication.</span></span>
<span data-ttu-id="236fe-123">Per costruire, vedere la sezione Note per le proprietà di DISKTOINCLUDE e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="236fe-123">To construct, see NOTES section for DISKTOINCLUDE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtDiskInput[]
Parameter Sets: ByIdPowerUser, ByInputObjectPowerUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="236fe-124">-DiskType</span><span class="sxs-lookup"><span data-stu-id="236fe-124">-DiskType</span></span>
<span data-ttu-id="236fe-125">Specifica il tipo di dischi da usare per la VM di Azure.</span><span class="sxs-lookup"><span data-stu-id="236fe-125">Specifies the type of disks to be used for the Azure VM.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Support.DiskAccountType
Parameter Sets: ByIdDefaultUser, ByInputObjectDefaultUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="236fe-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="236fe-126">-InputObject</span></span>
<span data-ttu-id="236fe-127">Specifica il server individuato di cui eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="236fe-127">Specifies the discovered server to be migrated.</span></span>
<span data-ttu-id="236fe-128">L'oggetto server può essere recuperato usando il cmdlet Get-AzMigrateServer.</span><span class="sxs-lookup"><span data-stu-id="236fe-128">The server object can be retrieved using the Get-AzMigrateServer cmdlet.</span></span>
<span data-ttu-id="236fe-129">Per costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="236fe-129">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareMachine
Parameter Sets: ByInputObjectDefaultUser, ByInputObjectPowerUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="236fe-130">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="236fe-130">-LicenseType</span></span>
<span data-ttu-id="236fe-131">Specifica se l'utilità ibrida di Azure è applicabile per il server di origine di cui eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="236fe-131">Specifies if Azure Hybrid benefit is applicable for the source server to be migrated.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Support.LicenseType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="236fe-132">-MachineId</span><span class="sxs-lookup"><span data-stu-id="236fe-132">-MachineId</span></span>
<span data-ttu-id="236fe-133">Specifica l'ID computer del server individuato di cui eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="236fe-133">Specifies the machine ID of the discovered server to be migrated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIdDefaultUser, ByIdPowerUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="236fe-134">-OSDiskID</span><span class="sxs-lookup"><span data-stu-id="236fe-134">-OSDiskID</span></span>
<span data-ttu-id="236fe-135">Specifica il disco di sistema operativo per il server di origine di cui eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="236fe-135">Specifies the Operating System disk for the source server to be migrated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIdDefaultUser, ByInputObjectDefaultUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="236fe-136">-PerformAutoResync</span><span class="sxs-lookup"><span data-stu-id="236fe-136">-PerformAutoResync</span></span>
<span data-ttu-id="236fe-137">Specifica se la replica viene riparata automaticamente in caso di perdita del rilevamento delle modifiche per il server di origine in replica.</span><span class="sxs-lookup"><span data-stu-id="236fe-137">Specifies if replication be auto-repaired in case change tracking is lost for the source server under replication.</span></span>

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

### <span data-ttu-id="236fe-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="236fe-138">-SubscriptionId</span></span>
<span data-ttu-id="236fe-139">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="236fe-139">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="236fe-140">-TargetAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="236fe-140">-TargetAvailabilitySet</span></span>
<span data-ttu-id="236fe-141">Specifica il set di disponibilità da usare per VM creationSpecifies il set di disponibilità da usare per la creazione di VM.</span><span class="sxs-lookup"><span data-stu-id="236fe-141">Specifies the Availability Set to be used for VM creationSpecifies the Availability Set to be used for VM creation.</span></span>

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

### <span data-ttu-id="236fe-142">-TargetAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="236fe-142">-TargetAvailabilityZone</span></span>
<span data-ttu-id="236fe-143">Specifica l'area di disponibilità da usare per la creazione di VM.</span><span class="sxs-lookup"><span data-stu-id="236fe-143">Specifies the Availability Zone to be used for VM creation.</span></span>

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

### <span data-ttu-id="236fe-144">-TargetBootDiagnosticsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="236fe-144">-TargetBootDiagnosticsStorageAccount</span></span>
<span data-ttu-id="236fe-145">Specifica l'account di archiviazione da usare per la diagnostica di avvio.</span><span class="sxs-lookup"><span data-stu-id="236fe-145">Specifies the storage account to be used for boot diagnostics.</span></span>

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

### <span data-ttu-id="236fe-146">-TargetNetworkId</span><span class="sxs-lookup"><span data-stu-id="236fe-146">-TargetNetworkId</span></span>
<span data-ttu-id="236fe-147">Specifica l'ID della rete virtuale nell'abbonamento a Azure di destinazione a cui deve essere eseguita la migrazione del server.</span><span class="sxs-lookup"><span data-stu-id="236fe-147">Specifies the Virtual Network id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="236fe-148">-TargetResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="236fe-148">-TargetResourceGroupId</span></span>
<span data-ttu-id="236fe-149">Specifica l'ID del gruppo di risorse nell'abbonamento Azure di destinazione a cui deve essere eseguita la migrazione del server.</span><span class="sxs-lookup"><span data-stu-id="236fe-149">Specifies the Resource Group id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="236fe-150">-TargetSubnetName</span><span class="sxs-lookup"><span data-stu-id="236fe-150">-TargetSubnetName</span></span>
<span data-ttu-id="236fe-151">Specifica il nome della subnet all'interno del netowk virtuale di destinazione a cui deve essere eseguita la migrazione del server.</span><span class="sxs-lookup"><span data-stu-id="236fe-151">Specifies the Subnet name within the destination Virtual Netowk to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="236fe-152">-TargetVMName</span><span class="sxs-lookup"><span data-stu-id="236fe-152">-TargetVMName</span></span>
<span data-ttu-id="236fe-153">Specifica il nome della VM di Azure da creare.</span><span class="sxs-lookup"><span data-stu-id="236fe-153">Specifies the name of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="236fe-154">-TargetVMSize</span><span class="sxs-lookup"><span data-stu-id="236fe-154">-TargetVMSize</span></span>
<span data-ttu-id="236fe-155">Specifica l'USK della VM di Azure da creare.</span><span class="sxs-lookup"><span data-stu-id="236fe-155">Specifies the SKU of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="236fe-156">-VMWarerunasaccountID</span><span class="sxs-lookup"><span data-stu-id="236fe-156">-VMWarerunasaccountID</span></span>
<span data-ttu-id="236fe-157">ID account.</span><span class="sxs-lookup"><span data-stu-id="236fe-157">Account id.</span></span>

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

### <span data-ttu-id="236fe-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="236fe-158">CommonParameters</span></span>
<span data-ttu-id="236fe-159">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="236fe-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="236fe-160">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="236fe-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="236fe-161">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="236fe-161">INPUTS</span></span>

## <span data-ttu-id="236fe-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="236fe-162">OUTPUTS</span></span>

### <span data-ttu-id="236fe-163">Microsoft. Azure. PowerShell. Cmdlets. migrate. Models. Api20180110. IJob</span><span class="sxs-lookup"><span data-stu-id="236fe-163">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="236fe-164">Note</span><span class="sxs-lookup"><span data-stu-id="236fe-164">NOTES</span></span>

<span data-ttu-id="236fe-165">ALIAS</span><span class="sxs-lookup"><span data-stu-id="236fe-165">ALIASES</span></span>

<span data-ttu-id="236fe-166">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="236fe-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="236fe-167">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="236fe-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="236fe-168">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="236fe-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="236fe-169">DISKTOINCLUDE <IVMwareCbtDiskInput [] >: specifica i dischi nel server di origine da includere per la replica.</span><span class="sxs-lookup"><span data-stu-id="236fe-169">DISKTOINCLUDE <IVMwareCbtDiskInput[]>: Specifies the disks on the source server to be included for replication.</span></span>
  - <span data-ttu-id="236fe-170">`DiskId <String>`: ID disco.</span><span class="sxs-lookup"><span data-stu-id="236fe-170">`DiskId <String>`: The disk Id.</span></span>
  - <span data-ttu-id="236fe-171">`IsOSDisk <String>`: Valore che indica se il disco è il disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="236fe-171">`IsOSDisk <String>`: A value indicating whether the disk is the OS disk.</span></span>
  - <span data-ttu-id="236fe-172">`LogStorageAccountId <String>`: ID ARM dell'account di archiviazione dei log.</span><span class="sxs-lookup"><span data-stu-id="236fe-172">`LogStorageAccountId <String>`: The log storage account ARM Id.</span></span>
  - <span data-ttu-id="236fe-173">`LogStorageAccountSasSecretName <String>`: Nome segreto del Vault chiave dell'account di archiviazione del log.</span><span class="sxs-lookup"><span data-stu-id="236fe-173">`LogStorageAccountSasSecretName <String>`: The key vault secret name of the log storage account.</span></span>
  - <span data-ttu-id="236fe-174">`[DiskEncryptionSetId <String>]`: ID ARM di DiskEncryptionSet.</span><span class="sxs-lookup"><span data-stu-id="236fe-174">`[DiskEncryptionSetId <String>]`: The DiskEncryptionSet ARM Id.</span></span>
  - <span data-ttu-id="236fe-175">`[DiskType <DiskAccountType?>]`: Il tipo di disco.</span><span class="sxs-lookup"><span data-stu-id="236fe-175">`[DiskType <DiskAccountType?>]`: The disk type.</span></span>

<span data-ttu-id="236fe-176">INPUTOBJECT <IVMwareMachine> : specifica il server individuato di cui eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="236fe-176">INPUTOBJECT <IVMwareMachine>: Specifies the discovered server to be migrated.</span></span> <span data-ttu-id="236fe-177">L'oggetto server può essere recuperato usando il cmdlet Get-AzMigrateServer.</span><span class="sxs-lookup"><span data-stu-id="236fe-177">The server object can be retrieved using the Get-AzMigrateServer cmdlet.</span></span>
  - <span data-ttu-id="236fe-178">`[GuestOSDetailOstype <String>]`: Tipo di sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="236fe-178">`[GuestOSDetailOstype <String>]`: Type of the operating system.</span></span>

## <span data-ttu-id="236fe-179">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="236fe-179">RELATED LINKS</span></span>

