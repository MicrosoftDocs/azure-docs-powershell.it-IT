---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
ms.openlocfilehash: 87ea9af1980948f28477a9f483b3c6429df98d12
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370775"
---
# <span data-ttu-id="0ef5f-101">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="0ef5f-101">Add-AzVmssExtension</span></span>

## <span data-ttu-id="0ef5f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0ef5f-102">SYNOPSIS</span></span>
<span data-ttu-id="0ef5f-103">Aggiunge un'estensione a VMSS.</span><span class="sxs-lookup"><span data-stu-id="0ef5f-103">Adds an extension to the VMSS.</span></span>

## <span data-ttu-id="0ef5f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0ef5f-104">SYNTAX</span></span>

```
Add-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-ForceUpdateTag <String>] [-ProvisionAfterExtension <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ef5f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0ef5f-105">DESCRIPTION</span></span>
<span data-ttu-id="0ef5f-106">Il cmdlet **Add-AzVmssExtension** aggiunge un'estensione al set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="0ef5f-106">The **Add-AzVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="0ef5f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0ef5f-107">EXAMPLES</span></span>

### <span data-ttu-id="0ef5f-108">Esempio 1: aggiungere un'estensione a VMSS</span><span class="sxs-lookup"><span data-stu-id="0ef5f-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="0ef5f-109">Questo comando aggiunge un'estensione a VMSS.</span><span class="sxs-lookup"><span data-stu-id="0ef5f-109">This command adds an extension to the VMSS.</span></span>

### <span data-ttu-id="0ef5f-110">Esempio 2: aggiungere un'estensione a VMSS con le impostazioni e le impostazioni protette</span><span class="sxs-lookup"><span data-stu-id="0ef5f-110">Example 2: Add an extension to the VMSS with settings and protected settings</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};

PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName -Publisher $vmssPublisher  `
  -Type $vmssExtensionType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True  `
  -Setting $Settings -ProtectedSetting $ProtectedSettings
```

<span data-ttu-id="0ef5f-111">Questo comando aggiunge un'estensione a VMSS con uno script bash di esempio in uno spazio di archiviazione BLOB, specifica l'URL dell'archiviazione BLOB e il comando eseguibile in impostazioni e accesso alla sicurezza nelle impostazioni protette.</span><span class="sxs-lookup"><span data-stu-id="0ef5f-111">This command adds an extension to the VMSS with a sample bash script on a blob storage, specify the url of blob storage and executable command in settings and security access in protected settings.</span></span> 

## <span data-ttu-id="0ef5f-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0ef5f-112">PARAMETERS</span></span>

### <span data-ttu-id="0ef5f-113">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="0ef5f-113">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="0ef5f-114">Indica se la versione dell'estensione deve essere aggiornata automaticamente a una versione secondaria più recente.</span><span class="sxs-lookup"><span data-stu-id="0ef5f-114">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

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

### <span data-ttu-id="0ef5f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ef5f-115">-DefaultProfile</span></span>
<span data-ttu-id="0ef5f-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0ef5f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ef5f-117">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="0ef5f-117">-ForceUpdateTag</span></span>
<span data-ttu-id="0ef5f-118">Se viene specificato un valore ed è diverso dal valore precedente, il gestore dell'estensione verrà costretto all'aggiornamento anche se la configurazione dell'estensione non è cambiata.</span><span class="sxs-lookup"><span data-stu-id="0ef5f-118">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="0ef5f-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="0ef5f-119">-Name</span></span>
<span data-ttu-id="0ef5f-120">Specifica il nome dell'estensione aggiunta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ef5f-120">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="0ef5f-121">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="0ef5f-121">-ProtectedSetting</span></span>
<span data-ttu-id="0ef5f-122">Specifica la configurazione privata per l'estensione, come stringa.</span><span class="sxs-lookup"><span data-stu-id="0ef5f-122">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="0ef5f-123">Questo cmdlet crittografa la configurazione privata.</span><span class="sxs-lookup"><span data-stu-id="0ef5f-123">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="0ef5f-124">-ProvisionAfterExtension</span><span class="sxs-lookup"><span data-stu-id="0ef5f-124">-ProvisionAfterExtension</span></span>
<span data-ttu-id="0ef5f-125">Raccolta di nomi di estensione dopo cui deve essere effettuato il provisioning di questa estensione.</span><span class="sxs-lookup"><span data-stu-id="0ef5f-125">Collection of extension names after which this extension needs to be provisioned.</span></span>

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

### <span data-ttu-id="0ef5f-126">-Publisher</span><span class="sxs-lookup"><span data-stu-id="0ef5f-126">-Publisher</span></span>
<span data-ttu-id="0ef5f-127">Specifica il nome dell'autore dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="0ef5f-127">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="0ef5f-128">L'editore fornisce un nome quando l'editore registra un'estensione.</span><span class="sxs-lookup"><span data-stu-id="0ef5f-128">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="0ef5f-129">Questo può usare il cmdlet [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) per ottenere il Publisher.</span><span class="sxs-lookup"><span data-stu-id="0ef5f-129">This can use the [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="0ef5f-130">-Impostazione</span><span class="sxs-lookup"><span data-stu-id="0ef5f-130">-Setting</span></span>
<span data-ttu-id="0ef5f-131">Specifica la configurazione pubblica, come stringa, per l'estensione.</span><span class="sxs-lookup"><span data-stu-id="0ef5f-131">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="0ef5f-132">Questo cmdlet non crittografa la configurazione pubblica.</span><span class="sxs-lookup"><span data-stu-id="0ef5f-132">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="0ef5f-133">-Digitare</span><span class="sxs-lookup"><span data-stu-id="0ef5f-133">-Type</span></span>
<span data-ttu-id="0ef5f-134">Specifica il tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="0ef5f-134">Specifies the extension type.</span></span>
<span data-ttu-id="0ef5f-135">Puoi usare il cmdlet [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) per ottenere il tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="0ef5f-135">You can use the [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="0ef5f-136">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="0ef5f-136">-TypeHandlerVersion</span></span>
<span data-ttu-id="0ef5f-137">Specifica la versione dell'estensione da usare per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0ef5f-137">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="0ef5f-138">Puoi usare il cmdlet [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) per ottenere la versione dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="0ef5f-138">You can use the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="0ef5f-139">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0ef5f-139">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="0ef5f-140">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="0ef5f-140">Specify the VMSS object.</span></span>
<span data-ttu-id="0ef5f-141">Puoi usare il [nuovo-AzVmssConfig](./New-AzVmssConfig.md) per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0ef5f-141">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) to create the object.</span></span>

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

### <span data-ttu-id="0ef5f-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0ef5f-142">-Confirm</span></span>
<span data-ttu-id="0ef5f-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ef5f-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ef5f-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ef5f-144">-WhatIf</span></span>
<span data-ttu-id="0ef5f-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0ef5f-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0ef5f-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0ef5f-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ef5f-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ef5f-147">CommonParameters</span></span>
<span data-ttu-id="0ef5f-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ef5f-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ef5f-149">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0ef5f-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ef5f-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0ef5f-150">INPUTS</span></span>

### <span data-ttu-id="0ef5f-151">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0ef5f-151">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="0ef5f-152">System. String</span><span class="sxs-lookup"><span data-stu-id="0ef5f-152">System.String</span></span>

### <span data-ttu-id="0ef5f-153">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0ef5f-153">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="0ef5f-154">System. Object</span><span class="sxs-lookup"><span data-stu-id="0ef5f-154">System.Object</span></span>

## <span data-ttu-id="0ef5f-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0ef5f-155">OUTPUTS</span></span>

### <span data-ttu-id="0ef5f-156">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0ef5f-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="0ef5f-157">Note</span><span class="sxs-lookup"><span data-stu-id="0ef5f-157">NOTES</span></span>

## <span data-ttu-id="0ef5f-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0ef5f-158">RELATED LINKS</span></span>

[<span data-ttu-id="0ef5f-159">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="0ef5f-159">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)

[<span data-ttu-id="0ef5f-160">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="0ef5f-160">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="0ef5f-161">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="0ef5f-161">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="0ef5f-162">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="0ef5f-162">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="0ef5f-163">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="0ef5f-163">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
