---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: 7b52c6064f7dd692b732558b682290e8612f383c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93865178"
---
# <span data-ttu-id="d5b4d-101">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="d5b4d-101">Enable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="d5b4d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d5b4d-102">SYNOPSIS</span></span>
<span data-ttu-id="d5b4d-103">Consente di eseguire il backup di un elemento con un criterio di protezione del backup specificato.</span><span class="sxs-lookup"><span data-stu-id="d5b4d-103">Enables backup for an item with a specified Backup protection policy.</span></span>

## <span data-ttu-id="d5b4d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d5b4d-104">SYNTAX</span></span>

### <span data-ttu-id="d5b4d-105">AzureVMComputeEnableProtection (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d5b4d-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-ResourceGroupName] <String> [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d5b4d-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="d5b4d-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String> [-ServiceName] <String>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ExcludeAllDataDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5b4d-107">AzureFileShareEnableProtection</span><span class="sxs-lookup"><span data-stu-id="d5b4d-107">AzureFileShareEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-StorageAccountName] <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5b4d-108">AzureWorkloadEnableProtection</span><span class="sxs-lookup"><span data-stu-id="d5b4d-108">AzureWorkloadEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-ProtectableItem] <ProtectableItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5b4d-109">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="d5b4d-109">ModifyProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Item] <ItemBase>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ResetExclusionSettings]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d5b4d-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d5b4d-110">DESCRIPTION</span></span>
<span data-ttu-id="d5b4d-111">Il cmdlet **Enable-AzRecoveryServicesBackupProtection** imposta i criteri di protezione di Azure Backup su un elemento.</span><span class="sxs-lookup"><span data-stu-id="d5b4d-111">The **Enable-AzRecoveryServicesBackupProtection** cmdlet sets Azure Backup protection policy on an item.</span></span>
<span data-ttu-id="d5b4d-112">Impostare il contesto del Vault usando il cmdlet Set-AzRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="d5b4d-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="d5b4d-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d5b4d-113">EXAMPLES</span></span>

### <span data-ttu-id="d5b4d-114">Esempio 1: abilitare la protezione del backup per un elemento</span><span class="sxs-lookup"><span data-stu-id="d5b4d-114">Example 1: Enable Backup protection for an item</span></span>
```
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> $inclusionDiskLUNS = ("1", "2")
PS C:\> Enable-AzRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1" -InclusionDisksList $inclusionDiskLUNS
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="d5b4d-115">Il primo cmdlet ottiene un oggetto criteri predefinito e lo archivia nella variabile $Pol.</span><span class="sxs-lookup"><span data-stu-id="d5b4d-115">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="d5b4d-116">Il secondo cmdlet specifica i LUN del disco di cui eseguire il backup e lo archivia in $inclusionDiskLUNS variabile.</span><span class="sxs-lookup"><span data-stu-id="d5b4d-116">The second cmdlet specifies the disk LUNs which are to be backed up and stores it in $inclusionDiskLUNS variable.</span></span>
<span data-ttu-id="d5b4d-117">Il terzo cmdlet imposta i criteri di protezione del backup per la macchina virtuale ARM denominata V2VM usando i criteri in $Pol.</span><span class="sxs-lookup"><span data-stu-id="d5b4d-117">The third cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

## <span data-ttu-id="d5b4d-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d5b4d-118">PARAMETERS</span></span>

### <span data-ttu-id="d5b4d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5b4d-119">-DefaultProfile</span></span>
<span data-ttu-id="d5b4d-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d5b4d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5b4d-121">-ExcludeAllDataDisks</span><span class="sxs-lookup"><span data-stu-id="d5b4d-121">-ExcludeAllDataDisks</span></span>
<span data-ttu-id="d5b4d-122">Opzione per specificare solo i dischi del sistema operativo di backup</span><span class="sxs-lookup"><span data-stu-id="d5b4d-122">Option to specify to backup OS disks only</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection, ModifyProtection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5b4d-123">-ExclusionDisksList</span><span class="sxs-lookup"><span data-stu-id="d5b4d-123">-ExclusionDisksList</span></span>
<span data-ttu-id="d5b4d-124">Elenco dei LUN del disco da escludere nel backup</span><span class="sxs-lookup"><span data-stu-id="d5b4d-124">List of Disk LUNs to exclude in backup</span></span>

```yaml
Type: System.String[]
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection, ModifyProtection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5b4d-125">-InclusionDisksList</span><span class="sxs-lookup"><span data-stu-id="d5b4d-125">-InclusionDisksList</span></span>
<span data-ttu-id="d5b4d-126">Elenco dei LUN del disco da includere nel backup</span><span class="sxs-lookup"><span data-stu-id="d5b4d-126">List of Disk LUNs to include in backup</span></span>

```yaml
Type: System.String[]
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection, ModifyProtection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5b4d-127">-Elemento</span><span class="sxs-lookup"><span data-stu-id="d5b4d-127">-Item</span></span>
<span data-ttu-id="d5b4d-128">Specifica l'elemento di backup per cui questo cmdlet Abilita la protezione.</span><span class="sxs-lookup"><span data-stu-id="d5b4d-128">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="d5b4d-129">Per ottenere un **AzureRmRecoveryServicesBackupItem** , usare il cmdlet Get-AzRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="d5b4d-129">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: ModifyProtection
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5b4d-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="d5b4d-130">-Name</span></span>
<span data-ttu-id="d5b4d-131">Specifica il nome dell'elemento di backup.</span><span class="sxs-lookup"><span data-stu-id="d5b4d-131">Specifies the name of the Backup item.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection, AzureFileShareEnableProtection
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5b4d-132">-Policy</span><span class="sxs-lookup"><span data-stu-id="d5b4d-132">-Policy</span></span>
<span data-ttu-id="d5b4d-133">Specifica i criteri di protezione che il cmdlet associa a un elemento.</span><span class="sxs-lookup"><span data-stu-id="d5b4d-133">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="d5b4d-134">Per ottenere un oggetto **AzureRmRecoveryServicesBackupProtectionPolicy** , usa il cmdlet Get-AzRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="d5b4d-134">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5b4d-135">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="d5b4d-135">-ProtectableItem</span></span>
<span data-ttu-id="d5b4d-136">Valore di filtro per lo stato di job.</span><span class="sxs-lookup"><span data-stu-id="d5b4d-136">Filter value for status of job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase
Parameter Sets: AzureWorkloadEnableProtection
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5b4d-137">-ResetExclusionSettings</span><span class="sxs-lookup"><span data-stu-id="d5b4d-137">-ResetExclusionSettings</span></span>
<span data-ttu-id="d5b4d-138">Specifica di reimpostare l'impostazione di esclusione del disco associata all'elemento</span><span class="sxs-lookup"><span data-stu-id="d5b4d-138">Specifies to reset disk exclusion setting associated with the item</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ModifyProtection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5b4d-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5b4d-139">-ResourceGroupName</span></span>
<span data-ttu-id="d5b4d-140">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d5b4d-140">Specifies the name of the resource group.</span></span>
<span data-ttu-id="d5b4d-141">Specificare questo parametro solo per le macchine virtuali ARM.</span><span class="sxs-lookup"><span data-stu-id="d5b4d-141">Specify this parameter only for ARM virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMComputeEnableProtection
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5b4d-142">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d5b4d-142">-ServiceName</span></span>
<span data-ttu-id="d5b4d-143">Specifica il nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="d5b4d-143">Specifies the service name.</span></span>
<span data-ttu-id="d5b4d-144">Specifica questo parametro solo per le macchine virtuali ASM.</span><span class="sxs-lookup"><span data-stu-id="d5b4d-144">Specify this parameter only for ASM virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMClassicComputeEnableProtection
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5b4d-145">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d5b4d-145">-StorageAccountName</span></span>
<span data-ttu-id="d5b4d-146">Nome dell'account di archiviazione condivisione file di Azure</span><span class="sxs-lookup"><span data-stu-id="d5b4d-146">Azure file share storage account name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileShareEnableProtection
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5b4d-147">-VaultId</span><span class="sxs-lookup"><span data-stu-id="d5b4d-147">-VaultId</span></span>
<span data-ttu-id="d5b4d-148">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="d5b4d-148">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5b4d-149">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d5b4d-149">-Confirm</span></span>
<span data-ttu-id="d5b4d-150">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5b4d-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5b4d-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5b4d-151">-WhatIf</span></span>
<span data-ttu-id="d5b4d-152">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d5b4d-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d5b4d-153">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d5b4d-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5b4d-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5b4d-154">CommonParameters</span></span>
<span data-ttu-id="d5b4d-155">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5b4d-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5b4d-156">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d5b4d-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5b4d-157">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d5b4d-157">INPUTS</span></span>

### <span data-ttu-id="d5b4d-158">System. String</span><span class="sxs-lookup"><span data-stu-id="d5b4d-158">System.String</span></span>

### <span data-ttu-id="d5b4d-159">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="d5b4d-159">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="d5b4d-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d5b4d-160">OUTPUTS</span></span>

### <span data-ttu-id="d5b4d-161">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="d5b4d-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="d5b4d-162">Note</span><span class="sxs-lookup"><span data-stu-id="d5b4d-162">NOTES</span></span>

## <span data-ttu-id="d5b4d-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d5b4d-163">RELATED LINKS</span></span>

[<span data-ttu-id="d5b4d-164">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="d5b4d-164">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="d5b4d-165">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d5b4d-165">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)


