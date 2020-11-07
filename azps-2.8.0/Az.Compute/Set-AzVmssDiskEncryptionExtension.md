---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
ms.openlocfilehash: 90dd1854db30ff20cd864dc04b3235cc4e34c4d2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675151"
---
# <span data-ttu-id="6a3f4-101">Set-AzVmssDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="6a3f4-101">Set-AzVmssDiskEncryptionExtension</span></span>

## <span data-ttu-id="6a3f4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6a3f4-102">SYNOPSIS</span></span>
<span data-ttu-id="6a3f4-103">Abilita la crittografia del disco in un set di scale VM.</span><span class="sxs-lookup"><span data-stu-id="6a3f4-103">Enables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="6a3f4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6a3f4-104">SYNTAX</span></span>

```
Set-AzVmssDiskEncryptionExtension [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionKeyVaultId <String>] [-KeyEncryptionAlgorithm <String>] [-VolumeType <String>] [-ForceUpdate]
 [-TypeHandlerVersion <String>] [-ExtensionName <String>] [-Passphrase <String>] [-Force]
 [-DisableAutoUpgradeMinorVersion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6a3f4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6a3f4-105">DESCRIPTION</span></span>
<span data-ttu-id="6a3f4-106">Il cmdlet **set-AzVmssDiskEncryptionExtension** Abilita la crittografia su un set di proporzioni VM.</span><span class="sxs-lookup"><span data-stu-id="6a3f4-106">The **Set-AzVmssDiskEncryptionExtension** cmdlet enables encryption on a VM scale set.</span></span> <span data-ttu-id="6a3f4-107">Questo cmdlet consente la crittografia installando l'estensione di crittografia disco nel set di proporzioni VM.</span><span class="sxs-lookup"><span data-stu-id="6a3f4-107">This cmdlet enables encryption by installing the disk encryption extension on the VM scale set.</span></span>

<span data-ttu-id="6a3f4-108">Per le macchine virtuali Linux, il parametro *VolumeType* deve essere presente e deve essere impostato su "dati"</span><span class="sxs-lookup"><span data-stu-id="6a3f4-108">For Linux virtual machines, the *VolumeType* parameter must be present and must be set to "Data"</span></span>

## <span data-ttu-id="6a3f4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6a3f4-109">EXAMPLES</span></span>

### <span data-ttu-id="6a3f4-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6a3f4-110">Example 1</span></span>
```
$RGName = "MyResourceGroup"
$VmssName = "MyTestVmss"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

PS C:\> Set-AzVmssDiskEncryptionExtension -ResourceGroupName $RGName -VMScaleSetName $VmssName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="6a3f4-111">Questo comando consente la crittografia in tutti i dischi di tutte le VM di Windows in un set di proporzioni VM.</span><span class="sxs-lookup"><span data-stu-id="6a3f4-111">This command enables encryption on all disks of all Windows VMs in a VM scale set.</span></span>

### <span data-ttu-id="6a3f4-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="6a3f4-112">Example 2</span></span>
```
$RGName = "MyResourceGroup"
$VmssName = "MyTestVmss"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "Data"

PS C:\> Set-AzVmssDiskEncryptionExtension -ResourceGroupName $RGName -VMScaleSetName $VmssName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
 -VolumeType $volumeType
```

<span data-ttu-id="6a3f4-113">Questo comando consente di crittografare i dischi di dati di tutte le VM di Linux in un set di scale VM.</span><span class="sxs-lookup"><span data-stu-id="6a3f4-113">This command enables encryption on the data disks of all Linux VMs in a VM scale set.</span></span>

## <span data-ttu-id="6a3f4-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6a3f4-114">PARAMETERS</span></span>

### <span data-ttu-id="6a3f4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a3f4-115">-DefaultProfile</span></span>
<span data-ttu-id="6a3f4-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6a3f4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a3f4-117">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="6a3f4-117">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="6a3f4-118">Disabilitare l'aggiornamento automatico della versione secondaria</span><span class="sxs-lookup"><span data-stu-id="6a3f4-118">Disable auto-upgrade of minor version</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a3f4-119">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="6a3f4-119">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="6a3f4-120">ResourceID della chiave di crittografia generata in cui verrà inserito</span><span class="sxs-lookup"><span data-stu-id="6a3f4-120">ResourceID of the KeyVault where generated encryption key will be placed to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a3f4-121">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="6a3f4-121">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="6a3f4-122">URL della chiave di crittografia generata in cui verrà posizionato</span><span class="sxs-lookup"><span data-stu-id="6a3f4-122">URL of the KeyVault where generated encryption key will be placed to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a3f4-123">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="6a3f4-123">-ExtensionName</span></span>
<span data-ttu-id="6a3f4-124">Nome dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="6a3f4-124">The extension name.</span></span>
<span data-ttu-id="6a3f4-125">Se questo parametro non è specificato, i valori predefiniti usati sono AzureDiskEncryption per VM Windows e AzureDiskEncryptionForLinux per Linux VM</span><span class="sxs-lookup"><span data-stu-id="6a3f4-125">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a3f4-126">-Force</span><span class="sxs-lookup"><span data-stu-id="6a3f4-126">-Force</span></span>
<span data-ttu-id="6a3f4-127">Per forzare l'abilitazione della crittografia nel set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6a3f4-127">To force enabling encryption on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="6a3f4-128">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="6a3f4-128">-ForceUpdate</span></span>
<span data-ttu-id="6a3f4-129">Genera un contrassegno per Force Update.</span><span class="sxs-lookup"><span data-stu-id="6a3f4-129">Generate a tag for force update.</span></span>  <span data-ttu-id="6a3f4-130">Questa operazione deve essere concessa per eseguire ripetute operazioni di crittografia nella stessa VM.</span><span class="sxs-lookup"><span data-stu-id="6a3f4-130">This should be given to perform repeated encryption operations on the same VM.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a3f4-131">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="6a3f4-131">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="6a3f4-132">Algoritmo di crittografia dei tasti usato per crittografare la chiave di crittografia del volume</span><span class="sxs-lookup"><span data-stu-id="6a3f4-132">KeyEncryption Algorithm used to encrypt the volume encryption key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA-OAEP, RSA1_5

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a3f4-133">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="6a3f4-133">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="6a3f4-134">URL del Vault con versione di KeyEncryptionKey usato per crittografare la chiave di crittografia del disco</span><span class="sxs-lookup"><span data-stu-id="6a3f4-134">Versioned KeyVault URL of the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a3f4-135">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="6a3f4-135">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="6a3f4-136">ResourceID del Vault contenente il KeyEncryptionKey usato per crittografare la chiave di crittografia del disco</span><span class="sxs-lookup"><span data-stu-id="6a3f4-136">ResourceID of the KeyVault containing the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a3f4-137">-Passphrase</span><span class="sxs-lookup"><span data-stu-id="6a3f4-137">-Passphrase</span></span>
<span data-ttu-id="6a3f4-138">Passphrase specificata in Parameters.</span><span class="sxs-lookup"><span data-stu-id="6a3f4-138">The passphrase specified in parameters.</span></span>
<span data-ttu-id="6a3f4-139">Questo parametro funziona solo per Linux VM.</span><span class="sxs-lookup"><span data-stu-id="6a3f4-139">This parameter only works for Linux VM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a3f4-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a3f4-140">-ResourceGroupName</span></span>
<span data-ttu-id="6a3f4-141">Nome del gruppo di risorse a cui appartiene il set di scale VM</span><span class="sxs-lookup"><span data-stu-id="6a3f4-141">The resource group name to which the VM Scale Set belongs to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a3f4-142">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="6a3f4-142">-TypeHandlerVersion</span></span>
<span data-ttu-id="6a3f4-143">Versione del gestore del tipo.</span><span class="sxs-lookup"><span data-stu-id="6a3f4-143">The type handler version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a3f4-144">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="6a3f4-144">-VMScaleSetName</span></span>
<span data-ttu-id="6a3f4-145">Nome del set di scale della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="6a3f4-145">Name of the virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a3f4-146">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="6a3f4-146">-VolumeType</span></span>
<span data-ttu-id="6a3f4-147">Specifica il tipo di volumi della macchina virtuale su cui eseguire l'operazione di crittografia: OS, dati o tutti.</span><span class="sxs-lookup"><span data-stu-id="6a3f4-147">Specifies the type of virtual machine volumes on which to perform encryption operation: OS, Data, or All.</span></span> 

<span data-ttu-id="6a3f4-148">Linux: il parametro **VolumeType** deve essere presente e deve essere impostato su Data.</span><span class="sxs-lookup"><span data-stu-id="6a3f4-148">Linux: The **VolumeType** parameter must be present and must be set to Data.</span></span> 

<span data-ttu-id="6a3f4-149">Windows: il parametro **VolumeType** , se presente, deve essere impostato su All o OS.</span><span class="sxs-lookup"><span data-stu-id="6a3f4-149">Windows: The **VolumeType** parameter, if present, must be set to either All or OS.</span></span> <span data-ttu-id="6a3f4-150">Se il parametro **VolumeType** viene omesso, il valore predefinito è "All".</span><span class="sxs-lookup"><span data-stu-id="6a3f4-150">If the **VolumeType** parameter is omitted it defaults to "All".</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OS, Data, All

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a3f4-151">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6a3f4-151">-Confirm</span></span>
<span data-ttu-id="6a3f4-152">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a3f4-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a3f4-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a3f4-153">-WhatIf</span></span>
<span data-ttu-id="6a3f4-154">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6a3f4-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a3f4-155">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6a3f4-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a3f4-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a3f4-156">CommonParameters</span></span>
<span data-ttu-id="6a3f4-157">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a3f4-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a3f4-158">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a3f4-158">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a3f4-159">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6a3f4-159">INPUTS</span></span>

### <span data-ttu-id="6a3f4-160">System. String</span><span class="sxs-lookup"><span data-stu-id="6a3f4-160">System.String</span></span>

### <span data-ttu-id="6a3f4-161">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6a3f4-161">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6a3f4-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6a3f4-162">OUTPUTS</span></span>

### <span data-ttu-id="6a3f4-163">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineScaleSetExtension</span><span class="sxs-lookup"><span data-stu-id="6a3f4-163">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineScaleSetExtension</span></span>

## <span data-ttu-id="6a3f4-164">Note</span><span class="sxs-lookup"><span data-stu-id="6a3f4-164">NOTES</span></span>

## <span data-ttu-id="6a3f4-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6a3f4-165">RELATED LINKS</span></span>