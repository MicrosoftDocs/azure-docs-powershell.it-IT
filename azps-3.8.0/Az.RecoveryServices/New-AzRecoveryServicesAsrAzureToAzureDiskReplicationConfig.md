---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrazuretoazurediskreplicationconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
ms.openlocfilehash: b5d369a4f67888d6b7035e81d3462e10586ca3ee
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022661"
---
# <span data-ttu-id="7f03b-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="7f03b-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="7f03b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7f03b-102">SYNOPSIS</span></span>
<span data-ttu-id="7f03b-103">Crea un oggetto di mapping del disco per i dischi di una macchina virtuale Azure da replicare.</span><span class="sxs-lookup"><span data-stu-id="7f03b-103">Creates a disk mapping object for Azure virtual machine disks to be replicated.</span></span>

## <span data-ttu-id="7f03b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7f03b-104">SYNTAX</span></span>

### <span data-ttu-id="7f03b-105">AzureToAzure (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7f03b-105">AzureToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri <String> -LogStorageAccountId <String>
 -RecoveryAzureStorageAccountId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7f03b-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="7f03b-106">AzureToAzureManagedDisk</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig [-ManagedDisk] -LogStorageAccountId <String>
 -DiskId <String> -RecoveryResourceGroupId <String> -RecoveryReplicaDiskAccountType <String>
 -RecoveryTargetDiskAccountType <String> [-RecoveryDiskEncryptionSetId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-FailoverDiskName <String>] [-TfoDiskName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f03b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f03b-107">DESCRIPTION</span></span>
<span data-ttu-id="7f03b-108">Crea un oggetto di mapping del disco che esegue il mapping di un disco di una macchina virtuale di Azure all'account di archiviazione della cache e dell'account di archiviazione di destinazione (area di ripristino) da usare per replicare il disco.</span><span class="sxs-lookup"><span data-stu-id="7f03b-108">Creates a disk mapping object that maps an Azure virtual machine disk to the cache storage account and target storage account (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="7f03b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7f03b-109">EXAMPLES</span></span>

### <span data-ttu-id="7f03b-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7f03b-110">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri  $vhdUri -RecoveryAzureStorageAccountId $recoveryStorageAccountId -LogStorageAccountId $logStorageAccountId
```

<span data-ttu-id="7f03b-111">Creare un oggetto di mapping del disco per i dischi di una macchina virtuale di Azure da replicare. Usato durante Azure in Azure per abilitare e riproteggere l'operazione.</span><span class="sxs-lookup"><span data-stu-id="7f03b-111">Create a disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="7f03b-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7f03b-112">Example 2</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType
```

<span data-ttu-id="7f03b-113">Creare un oggetto mapping del disco gestito per i dischi di una macchina virtuale di Azure da replicare. Usato durante Azure in Azure per abilitare e riproteggere l'operazione.</span><span class="sxs-lookup"><span data-stu-id="7f03b-113">Create a managed disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="7f03b-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="7f03b-114">Example 3</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType -DiskEncryptionVaultId $keyVaultId -DiskEncryptionSecretUrl $secret `
-KeyEncryptionKeyUrl $keyUrl -KeyEncryptionVaultId $keyVaultId
```

<span data-ttu-id="7f03b-115">Creare un oggetto mapping del disco gestito con le impostazioni di crittografia di una sessione per i dischi di una macchina virtuale di Azure da replicare. Usato durante Azure in Azure per abilitare e riproteggere l'operazione.</span><span class="sxs-lookup"><span data-stu-id="7f03b-115">Create a managed disk mapping object with one pass encryption settings for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="7f03b-116">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="7f03b-116">Example 4</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType -RecoveryDiskEncryptionSetId $RecoveryDiskEncryptionSetId
```

<span data-ttu-id="7f03b-117">Creare un oggetto mapping del disco gestito con ID set di crittografia disco di destinazione per i dischi di una macchina virtuale Azure da replicare. Usato durante Azure in Azure per abilitare e riproteggere l'operazione.</span><span class="sxs-lookup"><span data-stu-id="7f03b-117">Create a managed disk mapping object with target disk encryption set Id, for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

## <span data-ttu-id="7f03b-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7f03b-118">PARAMETERS</span></span>

### <span data-ttu-id="7f03b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f03b-119">-DefaultProfile</span></span>
<span data-ttu-id="7f03b-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7f03b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f03b-121">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="7f03b-121">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="7f03b-122">Specifica l'URL segreto della crittografia disco.</span><span class="sxs-lookup"><span data-stu-id="7f03b-122">Specifies the disk encryption secret url.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f03b-123">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="7f03b-123">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="7f03b-124">Specifica l'ID del braccio di volta della chiave di crittografia disco.</span><span class="sxs-lookup"><span data-stu-id="7f03b-124">Specifies the disk encryption key vault ARM Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f03b-125">-DiskID</span><span class="sxs-lookup"><span data-stu-id="7f03b-125">-DiskId</span></span>
<span data-ttu-id="7f03b-126">Specifica l'ID disco del disco gestito.</span><span class="sxs-lookup"><span data-stu-id="7f03b-126">Specifies the disk id of managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f03b-127">-FailoverDiskName</span><span class="sxs-lookup"><span data-stu-id="7f03b-127">-FailoverDiskName</span></span>
<span data-ttu-id="7f03b-128">Specifica il nome del disco creato durante il failover.</span><span class="sxs-lookup"><span data-stu-id="7f03b-128">Specifies the name of the disk created during failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f03b-129">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="7f03b-129">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="7f03b-130">Specifica l'URL di crittografia della chiave.</span><span class="sxs-lookup"><span data-stu-id="7f03b-130">Specifies the key encryption Url.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f03b-131">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="7f03b-131">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="7f03b-132">Specifica l'ID del braccio della chiave di crittografia chiave.</span><span class="sxs-lookup"><span data-stu-id="7f03b-132">Specifies the key encryption key vault ARM Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f03b-133">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="7f03b-133">-LogStorageAccountId</span></span>
<span data-ttu-id="7f03b-134">Specifica l'ID dell'account di archiviazione del log o della cache da usare per archiviare i registri di replica.</span><span class="sxs-lookup"><span data-stu-id="7f03b-134">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="7f03b-135">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="7f03b-135">-ManagedDisk</span></span>
<span data-ttu-id="7f03b-136">Specifica che l'input è per il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="7f03b-136">Specifies the input is for managed disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f03b-137">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="7f03b-137">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="7f03b-138">Specifica l'ID dell'account di archiviazione di Azure a cui eseguire la replica.</span><span class="sxs-lookup"><span data-stu-id="7f03b-138">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f03b-139">-RecoveryDiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="7f03b-139">-RecoveryDiskEncryptionSetId</span></span>
<span data-ttu-id="7f03b-140">Specifica l'ID del set di crittografia del disco di Azure da usare per i dischi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="7f03b-140">Specifies the ID of the Azure disk encryption set to be used for recovery disks.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f03b-141">-RecoveryReplicaDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="7f03b-141">-RecoveryReplicaDiskAccountType</span></span>
<span data-ttu-id="7f03b-142">Specifica il tipo di account del disco gestito replicato.</span><span class="sxs-lookup"><span data-stu-id="7f03b-142">Specifies the account type of replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:
Accepted values: Premium_LRS, Standard_LRS, Standard_SSD

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f03b-143">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="7f03b-143">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="7f03b-144">Specifica l'ID del gruppo di risorse di recupero per il disco gestito replicato.</span><span class="sxs-lookup"><span data-stu-id="7f03b-144">Specifies the recovery resource group id for replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f03b-145">-RecoveryTargetDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="7f03b-145">-RecoveryTargetDiskAccountType</span></span>
<span data-ttu-id="7f03b-146">Specifica il disco di destinazione del ripristino per il disco gestito replicato.</span><span class="sxs-lookup"><span data-stu-id="7f03b-146">Specifies the recovery target disk for replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:
Accepted values: Premium_LRS, Standard_LRS, Standard_SSD

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f03b-147">-TfoDiskName</span><span class="sxs-lookup"><span data-stu-id="7f03b-147">-TfoDiskName</span></span>
<span data-ttu-id="7f03b-148">Specifica il nome del disco creato durante il failover del test.</span><span class="sxs-lookup"><span data-stu-id="7f03b-148">Specifies the name of the disk created during test failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f03b-149">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="7f03b-149">-VhdUri</span></span>
<span data-ttu-id="7f03b-150">Specifica l'URI VHD del disco a cui corrisponde il mapping.</span><span class="sxs-lookup"><span data-stu-id="7f03b-150">Specify the VHD URI of the disk that this mapping corresponds to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f03b-151">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7f03b-151">-Confirm</span></span>
<span data-ttu-id="7f03b-152">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f03b-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f03b-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f03b-153">-WhatIf</span></span>
<span data-ttu-id="7f03b-154">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7f03b-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f03b-155">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7f03b-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f03b-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f03b-156">CommonParameters</span></span>
<span data-ttu-id="7f03b-157">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f03b-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f03b-158">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f03b-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f03b-159">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7f03b-159">INPUTS</span></span>

### <span data-ttu-id="7f03b-160">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7f03b-160">None</span></span>

## <span data-ttu-id="7f03b-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7f03b-161">OUTPUTS</span></span>

### <span data-ttu-id="7f03b-162">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAzuretoAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="7f03b-162">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="7f03b-163">Note</span><span class="sxs-lookup"><span data-stu-id="7f03b-163">NOTES</span></span>

## <span data-ttu-id="7f03b-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7f03b-164">RELATED LINKS</span></span>
