---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
ms.openlocfilehash: a18e91a147e60ddc54caacccd8c63f3568bfe2eb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204691"
---
# <span data-ttu-id="8d002-101">Set-AzVmssDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="8d002-101">Set-AzVmssDiskEncryptionExtension</span></span>

## <span data-ttu-id="8d002-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d002-102">SYNOPSIS</span></span>
<span data-ttu-id="8d002-103">Abilita la crittografia del disco su un set di scalabilità della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8d002-103">Enables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="8d002-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8d002-104">SYNTAX</span></span>

```
Set-AzVmssDiskEncryptionExtension [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionKeyVaultId <String>] [-KeyEncryptionAlgorithm <String>] [-VolumeType <String>] [-ForceUpdate]
 [-TypeHandlerVersion <String>] [-ExtensionName <String>] [-Passphrase <String>] [-Force]
 [-DisableAutoUpgradeMinorVersion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8d002-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8d002-105">DESCRIPTION</span></span>
<span data-ttu-id="8d002-106">Il cmdlet **Set-AzVmssDiskEncryptionExtension** abilita la crittografia su un set di scalabilità della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8d002-106">The **Set-AzVmssDiskEncryptionExtension** cmdlet enables encryption on a VM scale set.</span></span> <span data-ttu-id="8d002-107">Questo cmdlet abilita la crittografia installando l'estensione di crittografia del disco nel set di scalabilità della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8d002-107">This cmdlet enables encryption by installing the disk encryption extension on the VM scale set.</span></span>

<span data-ttu-id="8d002-108">Per le macchine virtuali Linux, il *parametro VolumeType* deve essere presente e deve essere impostato su "Data"</span><span class="sxs-lookup"><span data-stu-id="8d002-108">For Linux virtual machines, the *VolumeType* parameter must be present and must be set to "Data"</span></span>

## <span data-ttu-id="8d002-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8d002-109">EXAMPLES</span></span>

### <span data-ttu-id="8d002-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8d002-110">Example 1</span></span>
```
$RGName = "MyResourceGroup"
$VmssName = "MyTestVmss"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

PS C:\> Set-AzVmssDiskEncryptionExtension -ResourceGroupName $RGName -VMScaleSetName $VmssName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="8d002-111">Questo comando abilita la crittografia in tutti i dischi di tutte le vm Windows in un set di scalabilità della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8d002-111">This command enables encryption on all disks of all Windows VMs in a VM scale set.</span></span>

### <span data-ttu-id="8d002-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="8d002-112">Example 2</span></span>
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

<span data-ttu-id="8d002-113">Questo comando abilita la crittografia sui dischi dati di tutte le macchine virtuali Linux in un set di scalabilità della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8d002-113">This command enables encryption on the data disks of all Linux VMs in a VM scale set.</span></span>

## <span data-ttu-id="8d002-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d002-114">PARAMETERS</span></span>

### <span data-ttu-id="8d002-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d002-115">-DefaultProfile</span></span>
<span data-ttu-id="8d002-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8d002-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d002-117">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="8d002-117">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="8d002-118">Disabilitare l'aggiornamento automatico della versione secondaria</span><span class="sxs-lookup"><span data-stu-id="8d002-118">Disable auto-upgrade of minor version</span></span>

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

### <span data-ttu-id="8d002-119">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="8d002-119">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="8d002-120">ResourceID della chiave KeyVault in cui verrà inserita la chiave di crittografia generata</span><span class="sxs-lookup"><span data-stu-id="8d002-120">ResourceID of the KeyVault where generated encryption key will be placed to</span></span>

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

### <span data-ttu-id="8d002-121">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="8d002-121">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="8d002-122">URL della chiave KeyVault in cui verrà inserita la chiave di crittografia generata</span><span class="sxs-lookup"><span data-stu-id="8d002-122">URL of the KeyVault where generated encryption key will be placed to</span></span>

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

### <span data-ttu-id="8d002-123">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="8d002-123">-ExtensionName</span></span>
<span data-ttu-id="8d002-124">Nome dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="8d002-124">The extension name.</span></span>
<span data-ttu-id="8d002-125">Se questo parametro non è specificato, i valori predefiniti usati sono AzureDiskEncryption per le macchine virtuali Windows e AzureDiskEncryptionForLinux per le macchine virtuali Linux</span><span class="sxs-lookup"><span data-stu-id="8d002-125">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs</span></span>

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

### <span data-ttu-id="8d002-126">-Force</span><span class="sxs-lookup"><span data-stu-id="8d002-126">-Force</span></span>
<span data-ttu-id="8d002-127">Per forzare l'abilitazione della crittografia nel set di scalabilità della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8d002-127">To force enabling encryption on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="8d002-128">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="8d002-128">-ForceUpdate</span></span>
<span data-ttu-id="8d002-129">Generare un tag per forzare l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="8d002-129">Generate a tag for force update.</span></span>  <span data-ttu-id="8d002-130">Questa operazione deve essere eseguita per eseguire operazioni di crittografia ripetute nella stessa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8d002-130">This should be given to perform repeated encryption operations on the same VM.</span></span>

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

### <span data-ttu-id="8d002-131">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="8d002-131">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="8d002-132">Algoritmo di crittografia KeyEncryption usato per crittografare la chiave di crittografia del volume</span><span class="sxs-lookup"><span data-stu-id="8d002-132">KeyEncryption Algorithm used to encrypt the volume encryption key</span></span>

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

### <span data-ttu-id="8d002-133">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="8d002-133">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="8d002-134">URL KeyVault con versione di KeyEncryptionKey usato per crittografare la chiave di crittografia del disco</span><span class="sxs-lookup"><span data-stu-id="8d002-134">Versioned KeyVault URL of the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="8d002-135">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="8d002-135">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="8d002-136">ResourceID di KeyVault che contiene KeyEncryptionKey usata per crittografare la chiave di crittografia del disco</span><span class="sxs-lookup"><span data-stu-id="8d002-136">ResourceID of the KeyVault containing the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="8d002-137">-Passphrase</span><span class="sxs-lookup"><span data-stu-id="8d002-137">-Passphrase</span></span>
<span data-ttu-id="8d002-138">Passphrase specificata nei parametri.</span><span class="sxs-lookup"><span data-stu-id="8d002-138">The passphrase specified in parameters.</span></span>
<span data-ttu-id="8d002-139">Questo parametro funziona solo per Linux VM.</span><span class="sxs-lookup"><span data-stu-id="8d002-139">This parameter only works for Linux VM.</span></span>

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

### <span data-ttu-id="8d002-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d002-140">-ResourceGroupName</span></span>
<span data-ttu-id="8d002-141">Nome del gruppo di risorse a cui appartiene il set di scale della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="8d002-141">The resource group name to which the VM Scale Set belongs to</span></span>

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

### <span data-ttu-id="8d002-142">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="8d002-142">-TypeHandlerVersion</span></span>
<span data-ttu-id="8d002-143">Versione del gestore tipi.</span><span class="sxs-lookup"><span data-stu-id="8d002-143">The type handler version.</span></span>

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

### <span data-ttu-id="8d002-144">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="8d002-144">-VMScaleSetName</span></span>
<span data-ttu-id="8d002-145">Nome del set di scalabilità della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="8d002-145">Name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="8d002-146">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="8d002-146">-VolumeType</span></span>
<span data-ttu-id="8d002-147">Specifica il tipo di volumi della macchina virtuale in cui eseguire l'operazione di crittografia: sistema operativo, dati o tutti.</span><span class="sxs-lookup"><span data-stu-id="8d002-147">Specifies the type of virtual machine volumes on which to perform encryption operation: OS, Data, or All.</span></span> 

<span data-ttu-id="8d002-148">Linux: il **parametro VolumeType** deve essere presente e deve essere impostato su Data.</span><span class="sxs-lookup"><span data-stu-id="8d002-148">Linux: The **VolumeType** parameter must be present and must be set to Data.</span></span> 

<span data-ttu-id="8d002-149">Windows: il **parametro VolumeType,** se presente, deve essere impostato su Tutti o su Sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8d002-149">Windows: The **VolumeType** parameter, if present, must be set to either All or OS.</span></span> <span data-ttu-id="8d002-150">Se il **parametro VolumeType** viene omesso, per impostazione predefinita viene utilizzato "Tutti".</span><span class="sxs-lookup"><span data-stu-id="8d002-150">If the **VolumeType** parameter is omitted it defaults to "All".</span></span>


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

### <span data-ttu-id="8d002-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8d002-151">-Confirm</span></span>
<span data-ttu-id="8d002-152">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d002-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d002-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d002-153">-WhatIf</span></span>
<span data-ttu-id="8d002-154">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8d002-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d002-155">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8d002-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d002-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d002-156">CommonParameters</span></span>
<span data-ttu-id="8d002-157">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d002-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d002-158">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8d002-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d002-159">INPUT</span><span class="sxs-lookup"><span data-stu-id="8d002-159">INPUTS</span></span>

### <span data-ttu-id="8d002-160">System.String</span><span class="sxs-lookup"><span data-stu-id="8d002-160">System.String</span></span>

### <span data-ttu-id="8d002-161">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8d002-161">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8d002-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8d002-162">OUTPUTS</span></span>

### <span data-ttu-id="8d002-163">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineScaleSetExtension</span><span class="sxs-lookup"><span data-stu-id="8d002-163">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineScaleSetExtension</span></span>

## <span data-ttu-id="8d002-164">NOTE</span><span class="sxs-lookup"><span data-stu-id="8d002-164">NOTES</span></span>

## <span data-ttu-id="8d002-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8d002-165">RELATED LINKS</span></span>
