---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
ms.openlocfilehash: 8036eede968d4c5f5b183b0713094740cfe127d7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836632"
---
# <span data-ttu-id="c845c-101">Set-AzVmssDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="c845c-101">Set-AzVmssDiskEncryptionExtension</span></span>

## <span data-ttu-id="c845c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c845c-102">SYNOPSIS</span></span>
<span data-ttu-id="c845c-103">Abilita la crittografia del disco in un set di scale VM.</span><span class="sxs-lookup"><span data-stu-id="c845c-103">Enables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="c845c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c845c-104">SYNTAX</span></span>

```
Set-AzVmssDiskEncryptionExtension [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionKeyVaultId <String>] [-KeyEncryptionAlgorithm <String>] [-VolumeType <String>] [-ForceUpdate]
 [-TypeHandlerVersion <String>] [-ExtensionName <String>] [-Passphrase <String>] [-Force]
 [-DisableAutoUpgradeMinorVersion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c845c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c845c-105">DESCRIPTION</span></span>
<span data-ttu-id="c845c-106">Il cmdlet **set-AzVmssDiskEncryptionExtension** Abilita la crittografia su un set di proporzioni VM.</span><span class="sxs-lookup"><span data-stu-id="c845c-106">The **Set-AzVmssDiskEncryptionExtension** cmdlet enables encryption on a VM scale set.</span></span>
<span data-ttu-id="c845c-107">Questo cmdlet consente la crittografia installando l'estensione di crittografia disco nel set di proporzioni VM.</span><span class="sxs-lookup"><span data-stu-id="c845c-107">This cmdlet enables encryption by installing the disk encryption extension on the VM scale set.</span></span>
<span data-ttu-id="c845c-108">Se non viene specificato alcun parametro *Name* , viene installata un'estensione con il nome predefinito AzureDiskEncryption per le macchine virtuali che eseguono il sistema operativo Windows o le macchine virtuali AzureDiskEncryptionForLinux per Linux.</span><span class="sxs-lookup"><span data-stu-id="c845c-108">If no *Name* parameter is specified, an extension with the default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines are installed.</span></span>

## <span data-ttu-id="c845c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c845c-109">EXAMPLES</span></span>

### <span data-ttu-id="c845c-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c845c-110">Example 1</span></span>
```
$RGName = "MyResourceGroup"
$VmssName = "MyTestVmss"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
PS C:\> Set-AzVmssDiskEncryptionExtension -ResourceGroupName $RGName -VMScaleSetName $VmssName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="c845c-111">Questo comando consente la crittografia in tutti i dischi di tutte le VM nel set di scale VM.</span><span class="sxs-lookup"><span data-stu-id="c845c-111">This command enables encryption on all disks of all VMs in the VM scale set.</span></span>

## <span data-ttu-id="c845c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c845c-112">PARAMETERS</span></span>

### <span data-ttu-id="c845c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c845c-113">-DefaultProfile</span></span>
<span data-ttu-id="c845c-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c845c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c845c-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="c845c-115">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="c845c-116">Disabilitare l'aggiornamento automatico della versione secondaria</span><span class="sxs-lookup"><span data-stu-id="c845c-116">Disable auto-upgrade of minor version</span></span>

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

### <span data-ttu-id="c845c-117">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="c845c-117">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="c845c-118">ResourceID della chiave di crittografia generata in cui verrà inserito</span><span class="sxs-lookup"><span data-stu-id="c845c-118">ResourceID of the KeyVault where generated encryption key will be placed to</span></span>

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

### <span data-ttu-id="c845c-119">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="c845c-119">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="c845c-120">URL della chiave di crittografia generata in cui verrà posizionato</span><span class="sxs-lookup"><span data-stu-id="c845c-120">URL of the KeyVault where generated encryption key will be placed to</span></span>

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

### <span data-ttu-id="c845c-121">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="c845c-121">-ExtensionName</span></span>
<span data-ttu-id="c845c-122">Nome dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="c845c-122">The extension name.</span></span>
<span data-ttu-id="c845c-123">Se questo parametro non è specificato, i valori predefiniti usati sono AzureDiskEncryption per VM Windows e AzureDiskEncryptionForLinux per Linux VM</span><span class="sxs-lookup"><span data-stu-id="c845c-123">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs</span></span>

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

### <span data-ttu-id="c845c-124">-Force</span><span class="sxs-lookup"><span data-stu-id="c845c-124">-Force</span></span>
<span data-ttu-id="c845c-125">Per forzare l'abilitazione della crittografia nel set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c845c-125">To force enabling encryption on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="c845c-126">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="c845c-126">-ForceUpdate</span></span>
<span data-ttu-id="c845c-127">Genera un contrassegno per Force Update.</span><span class="sxs-lookup"><span data-stu-id="c845c-127">Generate a tag for force update.</span></span>  <span data-ttu-id="c845c-128">Questa operazione deve essere concessa per eseguire ripetute operazioni di crittografia nella stessa VM.</span><span class="sxs-lookup"><span data-stu-id="c845c-128">This should be given to perform repeated encryption operations on the same VM.</span></span>

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

### <span data-ttu-id="c845c-129">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="c845c-129">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="c845c-130">Algoritmo di crittografia dei tasti usato per crittografare la chiave di crittografia del volume</span><span class="sxs-lookup"><span data-stu-id="c845c-130">KeyEncryption Algorithm used to encrypt the volume encryption key</span></span>

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

### <span data-ttu-id="c845c-131">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="c845c-131">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="c845c-132">URL del Vault con versione di KeyEncryptionKey usato per crittografare la chiave di crittografia del disco</span><span class="sxs-lookup"><span data-stu-id="c845c-132">Versioned KeyVault URL of the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="c845c-133">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="c845c-133">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="c845c-134">ResourceID del Vault contenente il KeyEncryptionKey usato per crittografare la chiave di crittografia del disco</span><span class="sxs-lookup"><span data-stu-id="c845c-134">ResourceID of the KeyVault containing the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="c845c-135">-Passphrase</span><span class="sxs-lookup"><span data-stu-id="c845c-135">-Passphrase</span></span>
<span data-ttu-id="c845c-136">Passphrase specificata in Parameters.</span><span class="sxs-lookup"><span data-stu-id="c845c-136">The passphrase specified in parameters.</span></span>
<span data-ttu-id="c845c-137">Questo parametro funziona solo per Linux VM.</span><span class="sxs-lookup"><span data-stu-id="c845c-137">This parameter only works for Linux VM.</span></span>

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

### <span data-ttu-id="c845c-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c845c-138">-ResourceGroupName</span></span>
<span data-ttu-id="c845c-139">Nome del gruppo di risorse a cui appartiene il set di scale VM</span><span class="sxs-lookup"><span data-stu-id="c845c-139">The resource group name to which the VM Scale Set belongs to</span></span>

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

### <span data-ttu-id="c845c-140">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="c845c-140">-TypeHandlerVersion</span></span>
<span data-ttu-id="c845c-141">Versione del gestore del tipo.</span><span class="sxs-lookup"><span data-stu-id="c845c-141">The type handler version.</span></span>

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

### <span data-ttu-id="c845c-142">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="c845c-142">-VMScaleSetName</span></span>
<span data-ttu-id="c845c-143">Nome del set di scale della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="c845c-143">Name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="c845c-144">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="c845c-144">-VolumeType</span></span>
<span data-ttu-id="c845c-145">Tipo di volume (OS o dati) per eseguire l'operazione di crittografia</span><span class="sxs-lookup"><span data-stu-id="c845c-145">Type of the volume (OS or Data) to perform encryption operation</span></span>

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

### <span data-ttu-id="c845c-146">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c845c-146">-Confirm</span></span>
<span data-ttu-id="c845c-147">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c845c-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c845c-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c845c-148">-WhatIf</span></span>
<span data-ttu-id="c845c-149">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c845c-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c845c-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c845c-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c845c-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c845c-151">CommonParameters</span></span>
<span data-ttu-id="c845c-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c845c-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c845c-153">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c845c-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c845c-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c845c-154">INPUTS</span></span>

### <span data-ttu-id="c845c-155">System. String</span><span class="sxs-lookup"><span data-stu-id="c845c-155">System.String</span></span>

### <span data-ttu-id="c845c-156">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c845c-156">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c845c-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c845c-157">OUTPUTS</span></span>

### <span data-ttu-id="c845c-158">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineScaleSetExtension</span><span class="sxs-lookup"><span data-stu-id="c845c-158">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineScaleSetExtension</span></span>

## <span data-ttu-id="c845c-159">Note</span><span class="sxs-lookup"><span data-stu-id="c845c-159">NOTES</span></span>

## <span data-ttu-id="c845c-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c845c-160">RELATED LINKS</span></span>
