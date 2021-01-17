---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: bde840903c53dae9ba47b9eb30634ce90f80ee9e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359561"
---
# New-AzRecoveryServicesAsrReplicationProtectedItem

## Sinossi
Abilita la replica per un elemento protettivo ASR creando un elemento protetto da replica.

## SINTASSI

### EnterpriseToEnterprise (impostazione predefinita)
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VmmToVmm] -ProtectableItem <ASRProtectableItem>
 -Name <String> -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### VMwareToAzureWithDiskType
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -Account <ASRRunAsAccount> [-LogStorageAccountId <String>] -ProcessServer <ASRProcessServer>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-WaitForCompletion] -DiskType <String> [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### VMwareToAzure
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -Account <ASRRunAsAccount> [-LogStorageAccountId <String>]
 [-InMageAzureV2DiskInput <AsrInMageAzureV2DiskInput[]>] -ProcessServer <ASRProcessServer>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-WaitForCompletion] [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### EnterpriseToAzure
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -RecoveryResourceGroupId <String> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HyperVSiteToAzure
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>]
 -RecoveryResourceGroupId <String> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### AzureToAzure
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure]
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> -AzureVmId <String>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilityZone <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-DiskEncryptionVaultId <String>]
 [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>] [-KeyEncryptionVaultId <String>]
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AzureToAzureWithoutDiskDetails
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure] -AzureVmId <String> -Name <String>
 [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 [-RecoveryAzureStorageAccountId <String>] -LogStorageAccountId <String> [-RecoveryAzureNetworkId <String>]
 [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String> [-ReplicationGroupName <String>]
 [-RecoveryAvailabilityZone <String>] [-RecoveryProximityPlacementGroupId <String>]
 [-RecoveryAvailabilitySetId <String>] [-RecoveryBootDiagStorageAccountId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzRecoveryServicesAsrReplicationProtectedItem** crea un nuovo elemento protetto da replica.
Usa questo cmdlet per abilitare la replica per un elemento protetto da ASR.

## ESEMPI

### Esempio 1
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $VM -Name $VM.Name -ProtectionContainerMapping $ProtectionContainerMapping
```

Avvia l'operazione di creazione di elementi protetti da replica per l'elemento protetto ASR specificato e restituisce il processo ASR usato per tenere traccia dell'operazione.

### Esempio 2
```
PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] `
-RecoveryResourceGroupId $RecoveryResourceGroupId -RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name `
-ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem -ProtectionContainerMapping $pcm `
-RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName -LogStorageAccountId $LogStorageAccountId
```

Avvia l'operazione di creazione di elementi protetti da replica per l'elemento protetto ASR specificato e restituisce il processo ASR usato per tenere traccia dell'operazione (scenario vmWare-Azure).

### Esempio 3
```
PS C:>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup
```

Avvia l'operazione di creazione di elementi protetti da replica per l'elemento protetto ASR specificato e restituisce il processo ASR usato per tenere traccia dell'operazione (scenario di Azure in Azure).

### Esempio 4
```
PS C:\> $disk1 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -RecoveryAzureNetworkId $RecoveryAzureNetworkId -RecoveryAzureSubnetName $RecoveryAzureSubnetName
```

Avvia l'operazione di creazione di elementi protetta dalla replica per l'oggetto VmId specificato e restituisce il processo ASR usato per tenere traccia dell'operazione (scenario di Azure in Azure).

### Esempio 5
```
PS C:\>$disk1 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
PS C:\>$disk2 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId2 -LogStorageAccountId $logStorageAccountId -DiskType $diskType2

PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem  `
-ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName `
-LogStorageAccountId $LogStorageAccountId -InMageAzureV2DiskInput $disk1,$disk2
```

Avvia l'operazione di creazione di elementi protetti da replica per l'elemento protetto ASR specificato, inclusi i dischi selettivi e restituisce il processo ASR usato per tenere traccia dell'operazione (scenario vmWare in Azure) con i dischi selezionati.

### Esempio 6
```
PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem  `
-ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName `
-LogStorageAccountId $LogStorageAccountId -DiskType Standard_LRS

Starts the replication protected item creation operation for the specified ASR protectable item with default disk type and returns the ASR job used to track the operation(vmWare to Azure scenario).
```

### Esempio 7
```
PS C:\> $disk1 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = new-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -DiskEncryptionVaultId  $DiskEncryptionVaultId -DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
 -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

Avvia l'operazione di creazione di elementi protetta dalla replica per l'oggetto VmId specificato e restituisce il processo ASR usato per tenere traccia dell'operazione (scenario di Azure in Azure). Per i dettagli di failover VM passati in cmdlet per la crittografia verrà usato.

### Esempio 8
```
PS C:>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup -RecoveryProximityPlacementGroupId $ppg
```

Avvia l'operazione di creazione di elementi protetti da replica per una macchina virtuale all'interno del gruppo di posizionamento di prossimità e restituisce il processo ASR usato per tenere traccia dell'operazione (scenario di Azure in Azure).

## PARAMETRI

### -Account
L'account RunAs da usare per spingere l'installazione del servizio di mobilità, se necessario. Deve essere uno dall'elenco di account RunAs nel tessuto ASR.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AzureToAzure
Parametro switch specifica la creazione dell'elemento replicato in uno scenario di Azure in Azure.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AzureToAzureDiskReplicationConfiguration
Specifica la configurazione del disco in uno scenario di ripristino di emergenza di VM per Azure in Azure.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AzureVmId
Specifica l'ID VM di Azure per la protezione dal ripristino di emergenza nell'area di ripristino.

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskEncryptionSecretUrl
Specifica l'URL segreto di crittografia disco con la versione (Azure Disk Encryption) da usare come ripristino VM dopo il failover.

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskEncryptionSetId
Specifica l'ID risorsa del set di crittografia disco da usare per la crittografia dei dischi gestiti.

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskEncryptionVaultId
Specifica l'ID del Vault segreto del disco (crittografia disco Azure) da usare come ripristino VM dopo il failover.

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskType
Specifica il tipo di disco gestito VM di ripristino.

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HyperVToAzure
Parametro switch per specificare che l'elemento replicato è una macchina virtuale Hyper-V che viene replicata in Azure.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeDiskId
Elenco di dischi da includere per la replica. Per impostazione predefinita, tutti i dischi sono inclusi.

```yaml
Type: System.String[]
Parameter Sets: HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InMageAzureV2DiskInput
Specifica l'input di configurazione del disco per vMWare disk ID per la protezione da un elemento protetto specificato.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.AsrInMageAzureV2DiskInput[]
Parameter Sets: VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyEncryptionKeyUrl
Specifica l'URL della chiave di crittografia del disco con la versione (Azure Disk Encryption) da usare come ripristino VM dopo il failover.

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyEncryptionVaultId
Specifica la chiave della chiave di crittografia del disco-ID Vault (crittografia disco Azure) da usare come VM di ripristino dopo il failover.

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LogStorageAccountId
Specifica l'ID dell'account di archiviazione del log o della cache da usare per archiviare i registri di replica.

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Specifica un nome per l'elemento protetto da replica ASR. Il nome deve essere univoco all'interno del Vault.

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

### -OS
Specifica la famiglia di sistemi operativi.
I valori accettabili per questo parametro sono: Windows o Linux.

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases:
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OSDiskName
Specifica il nome del disco del sistema operativo.

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProcessServer
Il server dei processi da usare per replicare il computer. Usare l'elenco dei server di processo nel tessuto ASR che corrispondono al server di configurazione per specificarne uno.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProtectableItem
Specifica l'oggetto elemento protetto ASR per cui viene abilitata la replica.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, VMwareToAzureWithDiskType, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ProtectionContainerMapping
Specifica l'oggetto mapping del contenitore di protezione ASR che corrisponde ai criteri di replica da usare per la replica.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryAvailabilitySetId
ID della AvailabilitySet in cui ripristinare il computer in caso di failover.

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryAvailabilityZone
Specifica l'area di disponibilità di ripristino VM dopo il failover.


```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryAzureNetworkId
ID della rete virtuale di Azure in cui ripristinare il computer in caso di failover.

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryAzureStorageAccountId
Specifica l'ID dell'account di archiviazione di Azure a cui eseguire la replica.

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryAzureSubnetName
La subnet all'interno della rete virtuale di Azure recupero a cui deve essere associata la macchina virtuale fallita in caso di failover.

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryBootDiagStorageAccountId
Specifica l'account di archiviazione per la diagnostica di avvio per ripristino di Azure VM.

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryCloudServiceId
Specifica l'ID risorsa del servizio cloud di ripristino a cui eseguire il failover della macchina virtuale.

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryProximityPlacementGroupId
Specifica l'ID del gruppo di posizionamento di prossimità usato dalla VM di failover nell'area di recupero di destinazione.

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryResourceGroupId
Specifica l'identificatore ARM del gruppo di risorse in cui verrà creata la macchina virtuale in caso di failover.

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryVmName
Nome della VM di ripristino creata dopo il failover.

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplicationGroupName
Specifica il nome del gruppo di replica da usare per creare punti di ripristino coerenti con più VM. Per impostazione predefinita, ogni elemento protetto da replica viene creato in un gruppo di punti di ripristino coerenti e con più VM non vengono generati. Usare questa opzione solo se è necessario creare punti di ripristino coerenti con più VM in un gruppo di computer, proteggendo tutti i computer nello stesso gruppo di replica. 

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VmmToVmm
Parametro switch per specificare che l'elemento replicato è una macchina virtuale Hyper-V che viene replicata tra i siti Hyper-V gestiti da VMM.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMwareToAzure
Parametro switch per specificare che l'elemento replicato è una macchina virtuale VMware o un server fisico che verrà replicato in Azure.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WaitForCompletion
Specifica che il cmdlet deve attendere il completamento dell'operazione prima della restituzione.

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

### -Confermare
Richiede la conferma prima di avviare l'operazione.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa succede se il cmdlet viene eseguito.
Il cmdlet non viene eseguito.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectableItem

## OUTPUT

### Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob

## Note

## COLLEGAMENTI CORRELATI

[Get-AzRecoveryServicesAsrReplicationProtectedItem](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[Remove-AzRecoveryServicesAsrReplicationProtectedItem](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)

[Set-AzRecoveryServicesAsrReplicationProtectedItem](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)
