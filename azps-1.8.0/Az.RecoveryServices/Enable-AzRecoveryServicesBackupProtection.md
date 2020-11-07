---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: 7f29c0bef53d75be4f5b253e3a15bf78cbacd04b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677708"
---
# <span data-ttu-id="faa27-101">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="faa27-101">Enable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="faa27-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="faa27-102">SYNOPSIS</span></span>
<span data-ttu-id="faa27-103">Consente di eseguire il backup di un elemento con un criterio di protezione del backup specificato.</span><span class="sxs-lookup"><span data-stu-id="faa27-103">Enables backup for an item with a specified Backup protection policy.</span></span>

## <span data-ttu-id="faa27-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="faa27-104">SYNTAX</span></span>

### <span data-ttu-id="faa27-105">AzureVMComputeEnableProtection (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="faa27-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String> [-ResourceGroupName] <String>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="faa27-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="faa27-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String> [-ServiceName] <String>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="faa27-107">AzureFileShareEnableProtection</span><span class="sxs-lookup"><span data-stu-id="faa27-107">AzureFileShareEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String>
 [-StorageAccountName] <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="faa27-108">AzureWorkloadEnableProtection</span><span class="sxs-lookup"><span data-stu-id="faa27-108">AzureWorkloadEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-ProtectableItem] <ProtectableItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="faa27-109">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="faa27-109">ModifyProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="faa27-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="faa27-110">DESCRIPTION</span></span>
<span data-ttu-id="faa27-111">Il cmdlet **Enable-AzRecoveryServicesBackupProtection** imposta i criteri di protezione di Azure Backup su un elemento.</span><span class="sxs-lookup"><span data-stu-id="faa27-111">The **Enable-AzRecoveryServicesBackupProtection** cmdlet sets Azure Backup protection policy on an item.</span></span>
<span data-ttu-id="faa27-112">Impostare il contesto del Vault usando il cmdlet Set-AzRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="faa27-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="faa27-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="faa27-113">EXAMPLES</span></span>

### <span data-ttu-id="faa27-114">Esempio 1: abilitare la protezione del backup per un elemento</span><span class="sxs-lookup"><span data-stu-id="faa27-114">Example 1: Enable Backup protection for an item</span></span>
```
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> Enable-AzRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1"
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="faa27-115">Il primo cmdlet ottiene un oggetto criteri predefinito e lo archivia nella variabile $Pol.</span><span class="sxs-lookup"><span data-stu-id="faa27-115">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="faa27-116">Il secondo cmdlet imposta i criteri di protezione del backup per la macchina virtuale ARM denominata V2VM usando i criteri in $Pol.</span><span class="sxs-lookup"><span data-stu-id="faa27-116">The second cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

## <span data-ttu-id="faa27-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="faa27-117">PARAMETERS</span></span>

### <span data-ttu-id="faa27-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faa27-118">-DefaultProfile</span></span>
<span data-ttu-id="faa27-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="faa27-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="faa27-120">-Elemento</span><span class="sxs-lookup"><span data-stu-id="faa27-120">-Item</span></span>
<span data-ttu-id="faa27-121">Specifica l'elemento di backup per cui questo cmdlet Abilita la protezione.</span><span class="sxs-lookup"><span data-stu-id="faa27-121">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="faa27-122">Per ottenere un **AzureRmRecoveryServicesBackupItem** , usare il cmdlet Get-AzRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="faa27-122">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="faa27-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="faa27-123">-Name</span></span>
<span data-ttu-id="faa27-124">Specifica il nome dell'elemento di backup.</span><span class="sxs-lookup"><span data-stu-id="faa27-124">Specifies the name of the Backup item.</span></span>

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

### <span data-ttu-id="faa27-125">-Policy</span><span class="sxs-lookup"><span data-stu-id="faa27-125">-Policy</span></span>
<span data-ttu-id="faa27-126">Specifica i criteri di protezione che il cmdlet associa a un elemento.</span><span class="sxs-lookup"><span data-stu-id="faa27-126">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="faa27-127">Per ottenere un oggetto **AzureRmRecoveryServicesBackupProtectionPolicy** , usa il cmdlet Get-AzRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="faa27-127">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faa27-128">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="faa27-128">-ProtectableItem</span></span>
<span data-ttu-id="faa27-129">Valore di filtro per lo stato di job.</span><span class="sxs-lookup"><span data-stu-id="faa27-129">Filter value for status of job.</span></span>

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

### <span data-ttu-id="faa27-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="faa27-130">-ResourceGroupName</span></span>
<span data-ttu-id="faa27-131">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="faa27-131">Specifies the name of the resource group.</span></span>
<span data-ttu-id="faa27-132">Specificare questo parametro solo per le macchine virtuali ARM.</span><span class="sxs-lookup"><span data-stu-id="faa27-132">Specify this parameter only for ARM virtual machines.</span></span>

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

### <span data-ttu-id="faa27-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="faa27-133">-ServiceName</span></span>
<span data-ttu-id="faa27-134">Specifica il nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="faa27-134">Specifies the service name.</span></span>
<span data-ttu-id="faa27-135">Specifica questo parametro solo per le macchine virtuali ASM.</span><span class="sxs-lookup"><span data-stu-id="faa27-135">Specify this parameter only for ASM virtual machines.</span></span>

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

### <span data-ttu-id="faa27-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="faa27-136">-StorageAccountName</span></span>
<span data-ttu-id="faa27-137">Nome dell'account di archiviazione condivisione file di Azure</span><span class="sxs-lookup"><span data-stu-id="faa27-137">Azure file share storage account name</span></span>

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

### <span data-ttu-id="faa27-138">-VaultId</span><span class="sxs-lookup"><span data-stu-id="faa27-138">-VaultId</span></span>
<span data-ttu-id="faa27-139">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="faa27-139">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="faa27-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="faa27-140">-Confirm</span></span>
<span data-ttu-id="faa27-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="faa27-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="faa27-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="faa27-142">-WhatIf</span></span>
<span data-ttu-id="faa27-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="faa27-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="faa27-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="faa27-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="faa27-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faa27-145">CommonParameters</span></span>
<span data-ttu-id="faa27-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="faa27-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faa27-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="faa27-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faa27-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="faa27-148">INPUTS</span></span>

### <span data-ttu-id="faa27-149">System. String</span><span class="sxs-lookup"><span data-stu-id="faa27-149">System.String</span></span>

### <span data-ttu-id="faa27-150">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="faa27-150">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="faa27-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="faa27-151">OUTPUTS</span></span>

### <span data-ttu-id="faa27-152">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="faa27-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="faa27-153">Note</span><span class="sxs-lookup"><span data-stu-id="faa27-153">NOTES</span></span>

## <span data-ttu-id="faa27-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="faa27-154">RELATED LINKS</span></span>

[<span data-ttu-id="faa27-155">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="faa27-155">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="faa27-156">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="faa27-156">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)


