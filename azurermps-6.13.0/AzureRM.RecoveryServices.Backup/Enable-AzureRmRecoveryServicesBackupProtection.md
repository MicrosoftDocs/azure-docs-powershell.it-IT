---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/enable-azurermrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
ms.openlocfilehash: 357256d1c1a754915cbebc978e5c4ccf4440ccf4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687280"
---
# <span data-ttu-id="4fd77-101">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="4fd77-101">Enable-AzureRmRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="4fd77-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4fd77-102">SYNOPSIS</span></span>
<span data-ttu-id="4fd77-103">Consente di eseguire il backup di un elemento con un criterio di protezione del backup specificato.</span><span class="sxs-lookup"><span data-stu-id="4fd77-103">Enables backup for an item with a specified Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4fd77-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4fd77-104">SYNTAX</span></span>

### <span data-ttu-id="4fd77-105">AzureVMComputeEnableProtection (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4fd77-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String>
 [-ResourceGroupName] <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fd77-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="4fd77-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String> [-ServiceName] <String>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fd77-107">AzureFileShareEnableProtection</span><span class="sxs-lookup"><span data-stu-id="4fd77-107">AzureFileShareEnableProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String>
 -StorageAccountName <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fd77-108">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="4fd77-108">ModifyProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fd77-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4fd77-109">DESCRIPTION</span></span>
<span data-ttu-id="4fd77-110">Il cmdlet **Enable-AzureRmRecoveryServicesBackupProtection** imposta i criteri di protezione di Azure Backup su un elemento.</span><span class="sxs-lookup"><span data-stu-id="4fd77-110">The **Enable-AzureRmRecoveryServicesBackupProtection** cmdlet sets Azure Backup protection policy on an item.</span></span>
<span data-ttu-id="4fd77-111">Impostare il contesto del Vault usando il cmdlet Set-AzureRmRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="4fd77-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="4fd77-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4fd77-112">EXAMPLES</span></span>

### <span data-ttu-id="4fd77-113">Esempio 1: abilitare la protezione del backup per un elemento</span><span class="sxs-lookup"><span data-stu-id="4fd77-113">Example 1: Enable Backup protection for an item</span></span>
```
PS C:\> $Pol = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> Enable-AzureRmRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1"
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="4fd77-114">Il primo cmdlet ottiene un oggetto criteri predefinito e lo archivia nella variabile $Pol.</span><span class="sxs-lookup"><span data-stu-id="4fd77-114">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="4fd77-115">Il secondo cmdlet imposta i criteri di protezione del backup per la macchina virtuale ARM denominata V2VM usando i criteri in $Pol.</span><span class="sxs-lookup"><span data-stu-id="4fd77-115">The second cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

## <span data-ttu-id="4fd77-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4fd77-116">PARAMETERS</span></span>

### <span data-ttu-id="4fd77-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fd77-117">-DefaultProfile</span></span>
<span data-ttu-id="4fd77-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4fd77-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fd77-119">-Elemento</span><span class="sxs-lookup"><span data-stu-id="4fd77-119">-Item</span></span>
<span data-ttu-id="4fd77-120">Specifica l'elemento di backup per cui questo cmdlet Abilita la protezione.</span><span class="sxs-lookup"><span data-stu-id="4fd77-120">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="4fd77-121">Per ottenere un **AzureRmRecoveryServicesBackupItem** , usare il cmdlet Get-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="4fd77-121">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="4fd77-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="4fd77-122">-Name</span></span>
<span data-ttu-id="4fd77-123">Specifica il nome dell'elemento di backup.</span><span class="sxs-lookup"><span data-stu-id="4fd77-123">Specifies the name of the Backup item.</span></span>

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

### <span data-ttu-id="4fd77-124">-Policy</span><span class="sxs-lookup"><span data-stu-id="4fd77-124">-Policy</span></span>
<span data-ttu-id="4fd77-125">Specifica i criteri di protezione che il cmdlet associa a un elemento.</span><span class="sxs-lookup"><span data-stu-id="4fd77-125">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="4fd77-126">Per ottenere un oggetto **AzureRmRecoveryServicesBackupProtectionPolicy** , usa il cmdlet Get-AzureRmRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="4fd77-126">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="4fd77-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fd77-127">-ResourceGroupName</span></span>
<span data-ttu-id="4fd77-128">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4fd77-128">Specifies the name of the resource group.</span></span>
<span data-ttu-id="4fd77-129">Specificare questo parametro solo per le macchine virtuali ARM.</span><span class="sxs-lookup"><span data-stu-id="4fd77-129">Specify this parameter only for ARM virtual machines.</span></span>

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

### <span data-ttu-id="4fd77-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="4fd77-130">-ServiceName</span></span>
<span data-ttu-id="4fd77-131">Specifica il nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="4fd77-131">Specifies the service name.</span></span>
<span data-ttu-id="4fd77-132">Specifica questo parametro solo per le macchine virtuali ASM.</span><span class="sxs-lookup"><span data-stu-id="4fd77-132">Specify this parameter only for ASM virtual machines.</span></span>

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

### <span data-ttu-id="4fd77-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4fd77-133">-StorageAccountName</span></span>
<span data-ttu-id="4fd77-134">Nome dell'account di archiviazione condivisione file di Azure</span><span class="sxs-lookup"><span data-stu-id="4fd77-134">Azure file share storage account name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileShareEnableProtection
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fd77-135">-VaultId</span><span class="sxs-lookup"><span data-stu-id="4fd77-135">-VaultId</span></span>
<span data-ttu-id="4fd77-136">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="4fd77-136">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="4fd77-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4fd77-137">-Confirm</span></span>
<span data-ttu-id="4fd77-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4fd77-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fd77-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fd77-139">-WhatIf</span></span>
<span data-ttu-id="4fd77-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4fd77-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4fd77-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4fd77-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fd77-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fd77-142">CommonParameters</span></span>
<span data-ttu-id="4fd77-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fd77-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fd77-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fd77-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fd77-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4fd77-145">INPUTS</span></span>

### <span data-ttu-id="4fd77-146">System. String</span><span class="sxs-lookup"><span data-stu-id="4fd77-146">System.String</span></span>
<span data-ttu-id="4fd77-147">Parametri: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4fd77-147">Parameters: VaultId (ByValue)</span></span>

### <span data-ttu-id="4fd77-148">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="4fd77-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="4fd77-149">Parameters: Item (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4fd77-149">Parameters: Item (ByValue)</span></span>

## <span data-ttu-id="4fd77-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4fd77-150">OUTPUTS</span></span>

### <span data-ttu-id="4fd77-151">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="4fd77-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="4fd77-152">Note</span><span class="sxs-lookup"><span data-stu-id="4fd77-152">NOTES</span></span>

## <span data-ttu-id="4fd77-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4fd77-153">RELATED LINKS</span></span>

[<span data-ttu-id="4fd77-154">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="4fd77-154">Disable-AzureRmRecoveryServicesBackupProtection</span></span>](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="4fd77-155">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="4fd77-155">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)


