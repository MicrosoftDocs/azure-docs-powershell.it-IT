---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
ms.openlocfilehash: 774fb61f2394c5634c8415a7a18ce63f4e696a3f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991548"
---
# <span data-ttu-id="e98c8-101">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="e98c8-101">Add-AzVmssExtension</span></span>

## <span data-ttu-id="e98c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e98c8-102">SYNOPSIS</span></span>
<span data-ttu-id="e98c8-103">Aggiunge un'estensione al sistema VMSS.</span><span class="sxs-lookup"><span data-stu-id="e98c8-103">Adds an extension to the VMSS.</span></span>

## <span data-ttu-id="e98c8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e98c8-104">SYNTAX</span></span>

```
Add-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-EnableAutomaticUpgrade <Boolean>] [-ForceUpdateTag <String>] [-ProvisionAfterExtension <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e98c8-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e98c8-105">DESCRIPTION</span></span>
<span data-ttu-id="e98c8-106">Il cmdlet **Add-AzVmssExtension** aggiunge un'estensione al set di scalabilità delle macchine virtuali (VMSS).</span><span class="sxs-lookup"><span data-stu-id="e98c8-106">The **Add-AzVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="e98c8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e98c8-107">EXAMPLES</span></span>

### <span data-ttu-id="e98c8-108">Esempio 1: Aggiungere un'estensione al sistema VMSS</span><span class="sxs-lookup"><span data-stu-id="e98c8-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="e98c8-109">Questo comando aggiunge un'estensione al sistema VMSS.</span><span class="sxs-lookup"><span data-stu-id="e98c8-109">This command adds an extension to the VMSS.</span></span>

### <span data-ttu-id="e98c8-110">Esempio 2: Aggiungere un'estensione al sistema VMSS con impostazioni e impostazioni protette</span><span class="sxs-lookup"><span data-stu-id="e98c8-110">Example 2: Add an extension to the VMSS with settings and protected settings</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};

PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName -Publisher $vmssPublisher  `
  -Type $vmssExtensionType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True  `
  -Setting $Settings -ProtectedSetting $ProtectedSettings
```

<span data-ttu-id="e98c8-111">Questo comando aggiunge un'estensione al sistema VMSS con uno script bash di esempio in un archivio BLOB, specifica l'URL di archiviazione BLOB e il comando eseguibile nelle impostazioni e nell'accesso di sicurezza nelle impostazioni protette.</span><span class="sxs-lookup"><span data-stu-id="e98c8-111">This command adds an extension to the VMSS with a sample bash script on a blob storage, specify the url of blob storage and executable command in settings and security access in protected settings.</span></span> 

## <span data-ttu-id="e98c8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e98c8-112">PARAMETERS</span></span>

### <span data-ttu-id="e98c8-113">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="e98c8-113">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="e98c8-114">Indica se la versione dell'estensione deve essere aggiornata automaticamente a una versione secondaria più recente.</span><span class="sxs-lookup"><span data-stu-id="e98c8-114">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e98c8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e98c8-115">-DefaultProfile</span></span>
<span data-ttu-id="e98c8-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e98c8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e98c8-117">-EnableAutomaticUpgrade</span><span class="sxs-lookup"><span data-stu-id="e98c8-117">-EnableAutomaticUpgrade</span></span>
<span data-ttu-id="e98c8-118">Indica se l'estensione deve essere aggiornata automaticamente dalla piattaforma se è disponibile una versione più recente dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="e98c8-118">Indicates whether the extension should be automatically upgraded by the platform if there is a newer version of the extension available.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e98c8-119">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="e98c8-119">-ForceUpdateTag</span></span>
<span data-ttu-id="e98c8-120">Se viene fornito un valore diverso dal valore precedente, il gestore dell'estensione sarà forzato ad aggiornarsi anche se la configurazione dell'estensione non è stata modificata.</span><span class="sxs-lookup"><span data-stu-id="e98c8-120">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="e98c8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e98c8-121">-Name</span></span>
<span data-ttu-id="e98c8-122">Specifica il nome dell'estensione aggiunta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e98c8-122">Specifies the name of the extension that this cmdlet adds.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e98c8-123">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="e98c8-123">-ProtectedSetting</span></span>
<span data-ttu-id="e98c8-124">Specifica la configurazione privata per l'estensione, come stringa.</span><span class="sxs-lookup"><span data-stu-id="e98c8-124">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="e98c8-125">Questo cmdlet crittografa la configurazione privata.</span><span class="sxs-lookup"><span data-stu-id="e98c8-125">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e98c8-126">-ProvisionAfterExtension</span><span class="sxs-lookup"><span data-stu-id="e98c8-126">-ProvisionAfterExtension</span></span>
<span data-ttu-id="e98c8-127">Raccolta di nomi di estensione dopo i quali è necessario eseguire il provisioning di questa estensione.</span><span class="sxs-lookup"><span data-stu-id="e98c8-127">Collection of extension names after which this extension needs to be provisioned.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e98c8-128">-Publisher</span><span class="sxs-lookup"><span data-stu-id="e98c8-128">-Publisher</span></span>
<span data-ttu-id="e98c8-129">Specifica il nome dell'autore dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="e98c8-129">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="e98c8-130">L'editore fornisce un nome quando registra un'estensione.</span><span class="sxs-lookup"><span data-stu-id="e98c8-130">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="e98c8-131">In questo modo è possibile usare il cmdlet [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) per ottenere l'autore.</span><span class="sxs-lookup"><span data-stu-id="e98c8-131">This can use the [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) cmdlet to get the publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e98c8-132">-Setting</span><span class="sxs-lookup"><span data-stu-id="e98c8-132">-Setting</span></span>
<span data-ttu-id="e98c8-133">Specifica la configurazione pubblica, come stringa, per l'estensione.</span><span class="sxs-lookup"><span data-stu-id="e98c8-133">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="e98c8-134">Questo cmdlet non crittografa la configurazione pubblica.</span><span class="sxs-lookup"><span data-stu-id="e98c8-134">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e98c8-135">-Type</span><span class="sxs-lookup"><span data-stu-id="e98c8-135">-Type</span></span>
<span data-ttu-id="e98c8-136">Specifica il tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="e98c8-136">Specifies the extension type.</span></span>
<span data-ttu-id="e98c8-137">È possibile usare il cmdlet [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) per ottenere il tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="e98c8-137">You can use the [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e98c8-138">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="e98c8-138">-TypeHandlerVersion</span></span>
<span data-ttu-id="e98c8-139">Specifica la versione dell'estensione da usare per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e98c8-139">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="e98c8-140">È possibile usare il cmdlet [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) per ottenere la versione dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="e98c8-140">You can use the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e98c8-141">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e98c8-141">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="e98c8-142">Specificare l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="e98c8-142">Specify the VMSS object.</span></span>
<span data-ttu-id="e98c8-143">È possibile usare [New-AzVmssConfig](./New-AzVmssConfig.md) per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e98c8-143">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e98c8-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e98c8-144">-Confirm</span></span>
<span data-ttu-id="e98c8-145">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e98c8-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e98c8-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e98c8-146">-WhatIf</span></span>
<span data-ttu-id="e98c8-147">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e98c8-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e98c8-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e98c8-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e98c8-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e98c8-149">CommonParameters</span></span>
<span data-ttu-id="e98c8-150">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e98c8-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e98c8-151">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e98c8-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e98c8-152">INPUT</span><span class="sxs-lookup"><span data-stu-id="e98c8-152">INPUTS</span></span>

### <span data-ttu-id="e98c8-153">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e98c8-153">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="e98c8-154">System.String</span><span class="sxs-lookup"><span data-stu-id="e98c8-154">System.String</span></span>

### <span data-ttu-id="e98c8-155">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e98c8-155">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="e98c8-156">System.Object</span><span class="sxs-lookup"><span data-stu-id="e98c8-156">System.Object</span></span>

## <span data-ttu-id="e98c8-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e98c8-157">OUTPUTS</span></span>

### <span data-ttu-id="e98c8-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e98c8-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="e98c8-159">NOTE</span><span class="sxs-lookup"><span data-stu-id="e98c8-159">NOTES</span></span>

## <span data-ttu-id="e98c8-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e98c8-160">RELATED LINKS</span></span>

[<span data-ttu-id="e98c8-161">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="e98c8-161">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)

[<span data-ttu-id="e98c8-162">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="e98c8-162">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="e98c8-163">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="e98c8-163">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="e98c8-164">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="e98c8-164">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="e98c8-165">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="e98c8-165">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
