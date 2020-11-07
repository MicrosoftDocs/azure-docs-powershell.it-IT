---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssDiskEncryptionExtension.md
ms.openlocfilehash: 541e9df84fb0142ba6bcb43b429b77f64d685dd2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516847"
---
# <span data-ttu-id="169c4-101">Set-AzureRmVmssDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="169c4-101">Set-AzureRmVmssDiskEncryptionExtension</span></span>

## <span data-ttu-id="169c4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="169c4-102">SYNOPSIS</span></span>
<span data-ttu-id="169c4-103">Abilita la crittografia del disco in un set di scale VM.</span><span class="sxs-lookup"><span data-stu-id="169c4-103">Enables disk encryption on a VM scale set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="169c4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="169c4-104">SYNTAX</span></span>

```
Set-AzureRmVmssDiskEncryptionExtension [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionKeyVaultId <String>] [-KeyEncryptionAlgorithm <String>] [-VolumeType <String>] [-ForceUpdate]
 [-TypeHandlerVersion <String>] [-ExtensionName <String>] [-Passphrase <String>] [-Force]
 [-DisableAutoUpgradeMinorVersion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="169c4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="169c4-105">DESCRIPTION</span></span>
<span data-ttu-id="169c4-106">Il cmdlet **set-AzureRmVmssDiskEncryptionExtension** Abilita la crittografia su un set di proporzioni VM.</span><span class="sxs-lookup"><span data-stu-id="169c4-106">The **Set-AzureRmVmssDiskEncryptionExtension** cmdlet enables encryption on a VM scale set.</span></span>
<span data-ttu-id="169c4-107">Questo cmdlet consente la crittografia installando l'estensione di crittografia disco nel set di proporzioni VM.</span><span class="sxs-lookup"><span data-stu-id="169c4-107">This cmdlet enables encryption by installing the disk encryption extension on the VM scale set.</span></span>
<span data-ttu-id="169c4-108">Se non viene specificato alcun parametro *Name* , viene installata un'estensione con il nome predefinito AzureDiskEncryption per le macchine virtuali che eseguono il sistema operativo Windows o le macchine virtuali AzureDiskEncryptionForLinux per Linux.</span><span class="sxs-lookup"><span data-stu-id="169c4-108">If no *Name* parameter is specified, an extension with the default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines are installed.</span></span>

## <span data-ttu-id="169c4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="169c4-109">EXAMPLES</span></span>

### <span data-ttu-id="169c4-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="169c4-110">Example 1</span></span>
```
$RGName = "MyResourceGroup"
$VmssName = "MyTestVmss"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
PS C:\> Set-AzureRmVmssDiskEncryptionExtension -ResourceGroupName $RGName -VMScaleSetName $VmssName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="169c4-111">Questo comando consente la crittografia in tutti i dischi di tutte le VM nel set di scale VM.</span><span class="sxs-lookup"><span data-stu-id="169c4-111">This command enables encryption on all disks of all VMs in the VM scale set.</span></span>

## <span data-ttu-id="169c4-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="169c4-112">PARAMETERS</span></span>

### <span data-ttu-id="169c4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="169c4-113">-DefaultProfile</span></span>
<span data-ttu-id="169c4-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="169c4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="169c4-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="169c4-115">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="169c4-116">Disabilitare l'aggiornamento automatico della versione secondaria</span><span class="sxs-lookup"><span data-stu-id="169c4-116">Disable auto-upgrade of minor version</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="169c4-117">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="169c4-117">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="169c4-118">ResourceID della chiave di crittografia generata in cui verrà inserito</span><span class="sxs-lookup"><span data-stu-id="169c4-118">ResourceID of the KeyVault where generated encryption key will be placed to</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="169c4-119">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="169c4-119">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="169c4-120">URL della chiave di crittografia generata in cui verrà posizionato</span><span class="sxs-lookup"><span data-stu-id="169c4-120">URL of the KeyVault where generated encryption key will be placed to</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="169c4-121">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="169c4-121">-ExtensionName</span></span>
<span data-ttu-id="169c4-122">Nome dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="169c4-122">The extension name.</span></span>
<span data-ttu-id="169c4-123">Se questo parametro non è specificato, i valori predefiniti usati sono AzureDiskEncryption per VM Windows e AzureDiskEncryptionForLinux per Linux VM</span><span class="sxs-lookup"><span data-stu-id="169c4-123">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="169c4-124">-Force</span><span class="sxs-lookup"><span data-stu-id="169c4-124">-Force</span></span>
<span data-ttu-id="169c4-125">Per forzare l'abilitazione della crittografia nel set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="169c4-125">To force enabling encryption on the virtual machine scale set.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="169c4-126">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="169c4-126">-ForceUpdate</span></span>
<span data-ttu-id="169c4-127">Genera un contrassegno per Force Update.</span><span class="sxs-lookup"><span data-stu-id="169c4-127">Generate a tag for force update.</span></span>  <span data-ttu-id="169c4-128">Questa operazione deve essere concessa per eseguire ripetute operazioni di crittografia nella stessa VM.</span><span class="sxs-lookup"><span data-stu-id="169c4-128">This should be given to perform repeated encryption operations on the same VM.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="169c4-129">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="169c4-129">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="169c4-130">Algoritmo di crittografia dei tasti usato per crittografare la chiave di crittografia del volume</span><span class="sxs-lookup"><span data-stu-id="169c4-130">KeyEncryption Algorithm used to encrypt the volume encryption key</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: RSA-OAEP, RSA1_5

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="169c4-131">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="169c4-131">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="169c4-132">URL del Vault con versione di KeyEncryptionKey usato per crittografare la chiave di crittografia del disco</span><span class="sxs-lookup"><span data-stu-id="169c4-132">Versioned KeyVault URL of the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="169c4-133">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="169c4-133">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="169c4-134">ResourceID del Vault contenente il KeyEncryptionKey usato per crittografare la chiave di crittografia del disco</span><span class="sxs-lookup"><span data-stu-id="169c4-134">ResourceID of the KeyVault containing the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="169c4-135">-Passphrase</span><span class="sxs-lookup"><span data-stu-id="169c4-135">-Passphrase</span></span>
<span data-ttu-id="169c4-136">Passphrase specificata in Parameters.</span><span class="sxs-lookup"><span data-stu-id="169c4-136">The passphrase specified in parameters.</span></span>
<span data-ttu-id="169c4-137">Questo parametro funziona solo per Linux VM.</span><span class="sxs-lookup"><span data-stu-id="169c4-137">This parameter only works for Linux VM.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="169c4-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="169c4-138">-ResourceGroupName</span></span>
<span data-ttu-id="169c4-139">Nome del gruppo di risorse a cui appartiene il set di scale VM</span><span class="sxs-lookup"><span data-stu-id="169c4-139">The resource group name to which the VM Scale Set belongs to</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="169c4-140">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="169c4-140">-TypeHandlerVersion</span></span>
<span data-ttu-id="169c4-141">Versione del gestore del tipo.</span><span class="sxs-lookup"><span data-stu-id="169c4-141">The type handler version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="169c4-142">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="169c4-142">-VMScaleSetName</span></span>
<span data-ttu-id="169c4-143">Nome del set di scale della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="169c4-143">Name of the virtual machine scale set</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="169c4-144">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="169c4-144">-VolumeType</span></span>
<span data-ttu-id="169c4-145">Tipo di volume (OS o dati) per eseguire l'operazione di crittografia</span><span class="sxs-lookup"><span data-stu-id="169c4-145">Type of the volume (OS or Data) to perform encryption operation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: OS, Data, All

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="169c4-146">-Confermare</span><span class="sxs-lookup"><span data-stu-id="169c4-146">-Confirm</span></span>
<span data-ttu-id="169c4-147">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="169c4-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="169c4-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="169c4-148">-WhatIf</span></span>
<span data-ttu-id="169c4-149">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="169c4-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="169c4-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="169c4-150">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="169c4-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="169c4-151">CommonParameters</span></span>
<span data-ttu-id="169c4-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="169c4-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="169c4-153">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="169c4-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="169c4-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="169c4-154">INPUTS</span></span>

### <span data-ttu-id="169c4-155">System. String</span><span class="sxs-lookup"><span data-stu-id="169c4-155">System.String</span></span>
<span data-ttu-id="169c4-156">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="169c4-156">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="169c4-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="169c4-157">OUTPUTS</span></span>

### <span data-ttu-id="169c4-158">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineScaleSetExtension</span><span class="sxs-lookup"><span data-stu-id="169c4-158">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineScaleSetExtension</span></span>

## <span data-ttu-id="169c4-159">Note</span><span class="sxs-lookup"><span data-stu-id="169c4-159">NOTES</span></span>

## <span data-ttu-id="169c4-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="169c4-160">RELATED LINKS</span></span>