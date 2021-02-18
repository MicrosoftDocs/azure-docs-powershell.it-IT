---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: 41ee67359d4545a5b69ec1f9c44ff8e37302837e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193054"
---
# <span data-ttu-id="92272-101">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="92272-101">Enable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="92272-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92272-102">SYNOPSIS</span></span>
<span data-ttu-id="92272-103">Abilita il backup di un elemento con un criterio di protezione del backup specificato.</span><span class="sxs-lookup"><span data-stu-id="92272-103">Enables backup for an item with a specified Backup protection policy.</span></span>

## <span data-ttu-id="92272-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="92272-104">SYNTAX</span></span>

### <span data-ttu-id="92272-105">AzureVMComputeEnableProtection (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="92272-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-ResourceGroupName] <String> [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="92272-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="92272-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String> [-ServiceName] <String>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ExcludeAllDataDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92272-107">AzureFileShareEnableProtection</span><span class="sxs-lookup"><span data-stu-id="92272-107">AzureFileShareEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-StorageAccountName] <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92272-108">AzureWorkloadEnableProtection</span><span class="sxs-lookup"><span data-stu-id="92272-108">AzureWorkloadEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-ProtectableItem] <ProtectableItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92272-109">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="92272-109">ModifyProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Item] <ItemBase>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ResetExclusionSettings]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="92272-110">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="92272-110">DESCRIPTION</span></span>
<span data-ttu-id="92272-111">Il cmdlet **Enable-AzRecoveryServicesBackupProtection** abilita il backup associando un criterio di protezione all'elemento.</span><span class="sxs-lookup"><span data-stu-id="92272-111">The **Enable-AzRecoveryServicesBackupProtection** cmdlet enables the backup by associating a protection policy with the item.</span></span>
<span data-ttu-id="92272-112">Se l'ID criterio non è presente o l'elemento di backup non è associato ad alcun criterio, questo comando prevede un ID criterio.</span><span class="sxs-lookup"><span data-stu-id="92272-112">If policy ID is not present or the backup item is not associated with any policy, then this command will expect a policyID.</span></span>
<span data-ttu-id="92272-113">Impostare il contesto del vault usando il cmdlet Set-AzRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="92272-113">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="92272-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="92272-114">EXAMPLES</span></span>

### <span data-ttu-id="92272-115">Esempio 1: Abilitare la protezione di backup per un elemento</span><span class="sxs-lookup"><span data-stu-id="92272-115">Example 1: Enable Backup protection for an item</span></span>
```powershell
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> $inclusionDiskLUNS = ("1", "2")
PS C:\> Enable-AzRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1" -InclusionDisksList $inclusionDiskLUNS
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="92272-116">Il primo cmdlet ottiene un oggetto criterio predefinito, quindi lo archivia nella variabile $Pol predefinita.</span><span class="sxs-lookup"><span data-stu-id="92272-116">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="92272-117">Il secondo cmdlet specifica i LUN del disco di cui eseguire il backup e li archivia in $inclusionDiskLUNS variabile.</span><span class="sxs-lookup"><span data-stu-id="92272-117">The second cmdlet specifies the disk LUNs which are to be backed up and stores it in $inclusionDiskLUNS variable.</span></span>
<span data-ttu-id="92272-118">Il terzo cmdlet imposta i criteri di protezione del backup per la macchina virtuale ARM V2VM usando i criteri di $Pol.</span><span class="sxs-lookup"><span data-stu-id="92272-118">The third cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

### <span data-ttu-id="92272-119">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="92272-119">Example 2</span></span>

<span data-ttu-id="92272-120">Abilita il backup di un elemento con un criterio di protezione del backup specificato.</span><span class="sxs-lookup"><span data-stu-id="92272-120">Enables backup for an item with a specified Backup protection policy.</span></span> <span data-ttu-id="92272-121">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="92272-121">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Enable-AzRecoveryServicesBackupProtection -Item $Item -Policy $Pol -VaultId $vault
```

## <span data-ttu-id="92272-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92272-122">PARAMETERS</span></span>

### <span data-ttu-id="92272-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92272-123">-DefaultProfile</span></span>
<span data-ttu-id="92272-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="92272-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92272-125">-ExcludeAllDataDisks</span><span class="sxs-lookup"><span data-stu-id="92272-125">-ExcludeAllDataDisks</span></span>
<span data-ttu-id="92272-126">Opzione per specificare di eseguire il backup solo dei dischi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="92272-126">Option to specify to backup OS disks only</span></span>

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

### <span data-ttu-id="92272-127">-ExclusionDisksList</span><span class="sxs-lookup"><span data-stu-id="92272-127">-ExclusionDisksList</span></span>
<span data-ttu-id="92272-128">Elenco dei PIN del disco da escludere dal backup e il resto viene incluso automaticamente.</span><span class="sxs-lookup"><span data-stu-id="92272-128">List of Disk LUNs to be excluded in backup and the rest are automatically included.</span></span>

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

### <span data-ttu-id="92272-129">-InclusionDisksList</span><span class="sxs-lookup"><span data-stu-id="92272-129">-InclusionDisksList</span></span>
<span data-ttu-id="92272-130">L'elenco dei LUN da includere nel backup, e il resto viene automaticamente escluso ad eccezione del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="92272-130">List of Disk LUNs to be included in backup and the rest are automatically excluded except OS disk.</span></span>

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

### <span data-ttu-id="92272-131">-Item</span><span class="sxs-lookup"><span data-stu-id="92272-131">-Item</span></span>
<span data-ttu-id="92272-132">Specifica l'elemento di backup per cui questo cmdlet abilita la protezione.</span><span class="sxs-lookup"><span data-stu-id="92272-132">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="92272-133">Per ottenere un **elemento AzureRmRecoveryServicesBackupItem,** usare il cmdlet Get-AzRecoveryServicesBackupItem AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="92272-133">To obtain an **AzureRmRecoveryServicesBackupItem**, use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="92272-134">-Name</span><span class="sxs-lookup"><span data-stu-id="92272-134">-Name</span></span>
<span data-ttu-id="92272-135">Specifica il nome dell'elemento di backup.</span><span class="sxs-lookup"><span data-stu-id="92272-135">Specifies the name of the Backup item.</span></span>

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

### <span data-ttu-id="92272-136">-Policy</span><span class="sxs-lookup"><span data-stu-id="92272-136">-Policy</span></span>
<span data-ttu-id="92272-137">Specifica i criteri di protezione associati da questo cmdlet a un elemento.</span><span class="sxs-lookup"><span data-stu-id="92272-137">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="92272-138">Per ottenere un **oggetto AzureRmRecoveryServicesBackupProtectionPolicy, usare il cmdlet Get-AzRecoveryServicesBackupProtectionPolicy AzureRmRecoveryServicesBackupProtectionPolicy.**</span><span class="sxs-lookup"><span data-stu-id="92272-138">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="92272-139">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="92272-139">-ProtectableItem</span></span>
<span data-ttu-id="92272-140">Specifica l'elemento da proteggere con il criterio specificato.</span><span class="sxs-lookup"><span data-stu-id="92272-140">Specifies the item to be protected with the given policy.</span></span>

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

### <span data-ttu-id="92272-141">-ResetExsettingsSettings</span><span class="sxs-lookup"><span data-stu-id="92272-141">-ResetExclusionSettings</span></span>
<span data-ttu-id="92272-142">Specifica di reimpostare l'impostazione di esclusione disco associata all'elemento</span><span class="sxs-lookup"><span data-stu-id="92272-142">Specifies to reset disk exclusion setting associated with the item</span></span>

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

### <span data-ttu-id="92272-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92272-143">-ResourceGroupName</span></span>
<span data-ttu-id="92272-144">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="92272-144">Specifies the name of the resource group.</span></span>
<span data-ttu-id="92272-145">Specificare questo parametro solo per le ARM virtuali virtuali.</span><span class="sxs-lookup"><span data-stu-id="92272-145">Specify this parameter only for ARM virtual machines.</span></span>

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

### <span data-ttu-id="92272-146">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="92272-146">-StorageAccountName</span></span>
<span data-ttu-id="92272-147">Nome account di archiviazione condivisione file di Azure</span><span class="sxs-lookup"><span data-stu-id="92272-147">Azure file share storage account name</span></span>

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

### <span data-ttu-id="92272-148">-VaultId</span><span class="sxs-lookup"><span data-stu-id="92272-148">-VaultId</span></span>
<span data-ttu-id="92272-149">ARM ID del Vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="92272-149">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="92272-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="92272-150">-Confirm</span></span>
<span data-ttu-id="92272-151">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92272-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92272-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92272-152">-WhatIf</span></span>
<span data-ttu-id="92272-153">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="92272-153">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="92272-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92272-154">CommonParameters</span></span>
<span data-ttu-id="92272-155">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92272-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92272-156">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="92272-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92272-157">INPUT</span><span class="sxs-lookup"><span data-stu-id="92272-157">INPUTS</span></span>

### <span data-ttu-id="92272-158">System.String</span><span class="sxs-lookup"><span data-stu-id="92272-158">System.String</span></span>

### <span data-ttu-id="92272-159">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="92272-159">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="92272-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="92272-160">OUTPUTS</span></span>

### <span data-ttu-id="92272-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="92272-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="92272-162">NOTE</span><span class="sxs-lookup"><span data-stu-id="92272-162">NOTES</span></span>

## <span data-ttu-id="92272-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="92272-163">RELATED LINKS</span></span>

[<span data-ttu-id="92272-164">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="92272-164">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="92272-165">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="92272-165">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)


