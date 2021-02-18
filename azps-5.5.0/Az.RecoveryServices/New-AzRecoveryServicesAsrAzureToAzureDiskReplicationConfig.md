---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrazuretoazurediskreplicationconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
ms.openlocfilehash: c94fbf200de5ce56cc3116b1dc7a60052f9c19f1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192895"
---
# <span data-ttu-id="22d62-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="22d62-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="22d62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22d62-102">SYNOPSIS</span></span>
<span data-ttu-id="22d62-103">Crea un oggetto di mapping del disco per i dischi delle macchine virtuali di Azure da replicare.</span><span class="sxs-lookup"><span data-stu-id="22d62-103">Creates a disk mapping object for Azure virtual machine disks to be replicated.</span></span>

## <span data-ttu-id="22d62-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="22d62-104">SYNTAX</span></span>

### <span data-ttu-id="22d62-105">AzureToAzure (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="22d62-105">AzureToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri <String> -LogStorageAccountId <String>
 -RecoveryAzureStorageAccountId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="22d62-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="22d62-106">AzureToAzureManagedDisk</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig [-ManagedDisk] -LogStorageAccountId <String>
 -DiskId <String> -RecoveryResourceGroupId <String> -RecoveryReplicaDiskAccountType <String>
 -RecoveryTargetDiskAccountType <String> [-RecoveryDiskEncryptionSetId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-FailoverDiskName <String>] [-TfoDiskName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22d62-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="22d62-107">DESCRIPTION</span></span>
<span data-ttu-id="22d62-108">Crea un oggetto di mapping del disco che esegue il mapping di un disco della macchina virtuale di Azure all'account di archiviazione cache e all'account di archiviazione di destinazione (area di ripristino) da usare per replicare il disco.</span><span class="sxs-lookup"><span data-stu-id="22d62-108">Creates a disk mapping object that maps an Azure virtual machine disk to the cache storage account and target storage account (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="22d62-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="22d62-109">EXAMPLES</span></span>

### <span data-ttu-id="22d62-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="22d62-110">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri  $vhdUri -RecoveryAzureStorageAccountId $recoveryStorageAccountId -LogStorageAccountId $logStorageAccountId
```

<span data-ttu-id="22d62-111">Creare un oggetto di mapping del disco per i dischi delle macchine virtuali di Azure da replicare. Usato durante l'operazione di abilitazione e protezione di Azure ad Azure.</span><span class="sxs-lookup"><span data-stu-id="22d62-111">Create a disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="22d62-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="22d62-112">Example 2</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType
```

<span data-ttu-id="22d62-113">Creare un oggetto mapping del disco gestito per i dischi delle macchine virtuali di Azure da replicare. Usato durante l'operazione di abilitazione e protezione di Azure ad Azure.</span><span class="sxs-lookup"><span data-stu-id="22d62-113">Create a managed disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="22d62-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="22d62-114">Example 3</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType -DiskEncryptionVaultId $keyVaultId -DiskEncryptionSecretUrl $secret `
-KeyEncryptionKeyUrl $keyUrl -KeyEncryptionVaultId $keyVaultId
```

<span data-ttu-id="22d62-115">Creare un oggetto mapping del disco gestito con un solo pass di impostazioni di crittografia per i dischi delle macchine virtuali di Azure da replicare. Usato durante l'operazione di abilitazione e protezione di Azure ad Azure.</span><span class="sxs-lookup"><span data-stu-id="22d62-115">Create a managed disk mapping object with one pass encryption settings for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="22d62-116">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="22d62-116">Example 4</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType -RecoveryDiskEncryptionSetId $RecoveryDiskEncryptionSetId
```

<span data-ttu-id="22d62-117">Creare un oggetto mapping del disco gestito con ID impostato per la crittografia del disco di destinazione per replicare i dischi delle macchine virtuali di Azure. Usato durante l'operazione di abilitazione e protezione di Azure ad Azure.</span><span class="sxs-lookup"><span data-stu-id="22d62-117">Create a managed disk mapping object with target disk encryption set Id, for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

## <span data-ttu-id="22d62-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22d62-118">PARAMETERS</span></span>

### <span data-ttu-id="22d62-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22d62-119">-DefaultProfile</span></span>
<span data-ttu-id="22d62-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="22d62-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22d62-121">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="22d62-121">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="22d62-122">Specifica l'URL segreto di crittografia del disco.</span><span class="sxs-lookup"><span data-stu-id="22d62-122">Specifies the disk encryption secret url.</span></span>

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

### <span data-ttu-id="22d62-123">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="22d62-123">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="22d62-124">Specifica il vault della chiave di crittografia disco ARM ID utente.</span><span class="sxs-lookup"><span data-stu-id="22d62-124">Specifies the disk encryption key vault ARM Id.</span></span>

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

### <span data-ttu-id="22d62-125">-DiskId</span><span class="sxs-lookup"><span data-stu-id="22d62-125">-DiskId</span></span>
<span data-ttu-id="22d62-126">Specifica l'ID disco del disco gestito.</span><span class="sxs-lookup"><span data-stu-id="22d62-126">Specifies the disk id of managed disk.</span></span>

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

### <span data-ttu-id="22d62-127">-FailoverDiskName</span><span class="sxs-lookup"><span data-stu-id="22d62-127">-FailoverDiskName</span></span>
<span data-ttu-id="22d62-128">Specifica il nome del disco creato durante il failover.</span><span class="sxs-lookup"><span data-stu-id="22d62-128">Specifies the name of the disk created during failover.</span></span>

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

### <span data-ttu-id="22d62-129">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="22d62-129">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="22d62-130">Specifica l'URL di crittografia della chiave.</span><span class="sxs-lookup"><span data-stu-id="22d62-130">Specifies the key encryption Url.</span></span>

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

### <span data-ttu-id="22d62-131">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="22d62-131">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="22d62-132">Specifica l'ID del vault della chiave ARM chiave.</span><span class="sxs-lookup"><span data-stu-id="22d62-132">Specifies the key encryption key vault ARM Id.</span></span>

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

### <span data-ttu-id="22d62-133">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="22d62-133">-LogStorageAccountId</span></span>
<span data-ttu-id="22d62-134">Specifica l'ID dell'account di archiviazione cache o del log da usare per archiviare i log di replica.</span><span class="sxs-lookup"><span data-stu-id="22d62-134">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="22d62-135">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="22d62-135">-ManagedDisk</span></span>
<span data-ttu-id="22d62-136">Specifica che l'input è per il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="22d62-136">Specifies the input is for managed disk.</span></span>

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

### <span data-ttu-id="22d62-137">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="22d62-137">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="22d62-138">Specifica l'ID dell'account di archiviazione di Azure in cui eseguire la replica.</span><span class="sxs-lookup"><span data-stu-id="22d62-138">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="22d62-139">-RecoveryDiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="22d62-139">-RecoveryDiskEncryptionSetId</span></span>
<span data-ttu-id="22d62-140">Specifica l'ID del set di crittografia disco di Azure da usare per i dischi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="22d62-140">Specifies the ID of the Azure disk encryption set to be used for recovery disks.</span></span>

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

### <span data-ttu-id="22d62-141">-RecoveryReplicaDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="22d62-141">-RecoveryReplicaDiskAccountType</span></span>
<span data-ttu-id="22d62-142">Specifica il tipo di account del disco gestito replicato.</span><span class="sxs-lookup"><span data-stu-id="22d62-142">Specifies the account type of replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:
Accepted values: Premium_LRS, Standard_LRS, StandardSSD_LRS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22d62-143">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="22d62-143">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="22d62-144">Specifica l'ID gruppo di risorse di ripristino per il disco gestito replicato.</span><span class="sxs-lookup"><span data-stu-id="22d62-144">Specifies the recovery resource group id for replicated managed disk.</span></span>

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

### <span data-ttu-id="22d62-145">-RecoveryTargetDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="22d62-145">-RecoveryTargetDiskAccountType</span></span>
<span data-ttu-id="22d62-146">Specifica il disco di destinazione di ripristino per il disco gestito replicato.</span><span class="sxs-lookup"><span data-stu-id="22d62-146">Specifies the recovery target disk for replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:
Accepted values: Premium_LRS, Standard_LRS, StandardSSD_LRS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22d62-147">-TfoDiskName</span><span class="sxs-lookup"><span data-stu-id="22d62-147">-TfoDiskName</span></span>
<span data-ttu-id="22d62-148">Specifica il nome del disco creato durante il failover di test.</span><span class="sxs-lookup"><span data-stu-id="22d62-148">Specifies the name of the disk created during test failover.</span></span>

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

### <span data-ttu-id="22d62-149">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="22d62-149">-VhdUri</span></span>
<span data-ttu-id="22d62-150">Specificare l'URI VHD del disco a cui corrisponde questo mapping.</span><span class="sxs-lookup"><span data-stu-id="22d62-150">Specify the VHD URI of the disk that this mapping corresponds to.</span></span>

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

### <span data-ttu-id="22d62-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="22d62-151">-Confirm</span></span>
<span data-ttu-id="22d62-152">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22d62-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22d62-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22d62-153">-WhatIf</span></span>
<span data-ttu-id="22d62-154">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="22d62-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22d62-155">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="22d62-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22d62-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22d62-156">CommonParameters</span></span>
<span data-ttu-id="22d62-157">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22d62-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22d62-158">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="22d62-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22d62-159">INPUT</span><span class="sxs-lookup"><span data-stu-id="22d62-159">INPUTS</span></span>

### <span data-ttu-id="22d62-160">Nessuno</span><span class="sxs-lookup"><span data-stu-id="22d62-160">None</span></span>

## <span data-ttu-id="22d62-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="22d62-161">OUTPUTS</span></span>

### <span data-ttu-id="22d62-162">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="22d62-162">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="22d62-163">NOTE</span><span class="sxs-lookup"><span data-stu-id="22d62-163">NOTES</span></span>

## <span data-ttu-id="22d62-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="22d62-164">RELATED LINKS</span></span>
