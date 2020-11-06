---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssExtension.md
ms.openlocfilehash: ad87e4e556263889de23640abad391ee28d7b397
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519282"
---
# <span data-ttu-id="65a53-101">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="65a53-101">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="65a53-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="65a53-102">SYNOPSIS</span></span>
<span data-ttu-id="65a53-103">Aggiunge un'estensione a VMSS.</span><span class="sxs-lookup"><span data-stu-id="65a53-103">Adds an extension to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65a53-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="65a53-104">SYNTAX</span></span>

```
Add-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-ForceUpdateTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="65a53-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="65a53-105">DESCRIPTION</span></span>
<span data-ttu-id="65a53-106">Il cmdlet **Add-AzureRmVmssExtension** aggiunge un'estensione al set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="65a53-106">The **Add-AzureRmVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="65a53-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="65a53-107">EXAMPLES</span></span>

### <span data-ttu-id="65a53-108">Esempio 1: aggiungere un'estensione a VMSS</span><span class="sxs-lookup"><span data-stu-id="65a53-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="65a53-109">Questo comando aggiunge un'estensione a VMSS.</span><span class="sxs-lookup"><span data-stu-id="65a53-109">This command adds an extension to the VMSS.</span></span>

### <span data-ttu-id="65a53-110">Esempio 2: aggiungere un'estensione a VMSS con le impostazioni e le impostazioni protette</span><span class="sxs-lookup"><span data-stu-id="65a53-110">Example 2: Add an extension to the VMSS with settings and protected settings</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};

PS C:\> Add-AzureRmVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName -Publisher $vmssPublisher  `
  -Type $vmssExtensionType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True  `
  -Setting $Settings -ProtectedSetting $ProtectedSettings
```

<span data-ttu-id="65a53-111">Questo comando aggiunge un'estensione a VMSS con uno script bash di esempio in uno spazio di archiviazione BLOB, specifica l'URL dell'archiviazione BLOB e il comando eseguibile in impostazioni e accesso alla sicurezza nelle impostazioni protette.</span><span class="sxs-lookup"><span data-stu-id="65a53-111">This command adds an extension to the VMSS with a sample bash script on a blob storage, specify the url of blob storage and executable command in settings and security access in protected settings.</span></span> 

## <span data-ttu-id="65a53-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="65a53-112">PARAMETERS</span></span>

### <span data-ttu-id="65a53-113">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="65a53-113">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="65a53-114">Indica se la versione dell'estensione deve essere aggiornata automaticamente a una versione secondaria più recente.</span><span class="sxs-lookup"><span data-stu-id="65a53-114">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

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

### <span data-ttu-id="65a53-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65a53-115">-DefaultProfile</span></span>
<span data-ttu-id="65a53-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="65a53-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65a53-117">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="65a53-117">-ForceUpdateTag</span></span>
<span data-ttu-id="65a53-118">Se viene specificato un valore ed è diverso dal valore precedente, il gestore dell'estensione verrà costretto all'aggiornamento anche se la configurazione dell'estensione non è cambiata.</span><span class="sxs-lookup"><span data-stu-id="65a53-118">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="65a53-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="65a53-119">-Name</span></span>
<span data-ttu-id="65a53-120">Specifica il nome dell'estensione aggiunta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65a53-120">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="65a53-121">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="65a53-121">-ProtectedSetting</span></span>
<span data-ttu-id="65a53-122">Specifica la configurazione privata per l'estensione, come stringa.</span><span class="sxs-lookup"><span data-stu-id="65a53-122">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="65a53-123">Questo cmdlet crittografa la configurazione privata.</span><span class="sxs-lookup"><span data-stu-id="65a53-123">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="65a53-124">-Publisher</span><span class="sxs-lookup"><span data-stu-id="65a53-124">-Publisher</span></span>
<span data-ttu-id="65a53-125">Specifica il nome dell'autore dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="65a53-125">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="65a53-126">L'editore fornisce un nome quando l'editore registra un'estensione.</span><span class="sxs-lookup"><span data-stu-id="65a53-126">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="65a53-127">Questo può usare il cmdlet [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) per ottenere il Publisher.</span><span class="sxs-lookup"><span data-stu-id="65a53-127">This can use the [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="65a53-128">-Impostazione</span><span class="sxs-lookup"><span data-stu-id="65a53-128">-Setting</span></span>
<span data-ttu-id="65a53-129">Specifica la configurazione pubblica, come stringa, per l'estensione.</span><span class="sxs-lookup"><span data-stu-id="65a53-129">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="65a53-130">Questo cmdlet non crittografa la configurazione pubblica.</span><span class="sxs-lookup"><span data-stu-id="65a53-130">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="65a53-131">-Digitare</span><span class="sxs-lookup"><span data-stu-id="65a53-131">-Type</span></span>
<span data-ttu-id="65a53-132">Specifica il tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="65a53-132">Specifies the extension type.</span></span>
<span data-ttu-id="65a53-133">Puoi usare il cmdlet [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) per ottenere il tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="65a53-133">You can use the [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="65a53-134">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="65a53-134">-TypeHandlerVersion</span></span>
<span data-ttu-id="65a53-135">Specifica la versione dell'estensione da usare per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="65a53-135">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="65a53-136">Puoi usare il cmdlet [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) per ottenere la versione dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="65a53-136">You can use the [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="65a53-137">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="65a53-137">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="65a53-138">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="65a53-138">Specify the VMSS object.</span></span>
<span data-ttu-id="65a53-139">Puoi usare il [nuovo-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="65a53-139">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) to create the object.</span></span>

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

### <span data-ttu-id="65a53-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="65a53-140">-Confirm</span></span>
<span data-ttu-id="65a53-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65a53-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65a53-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65a53-142">-WhatIf</span></span>
<span data-ttu-id="65a53-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="65a53-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="65a53-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="65a53-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65a53-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65a53-145">CommonParameters</span></span>
<span data-ttu-id="65a53-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65a53-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65a53-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65a53-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65a53-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="65a53-148">INPUTS</span></span>

### <span data-ttu-id="65a53-149">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="65a53-149">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="65a53-150">System. String</span><span class="sxs-lookup"><span data-stu-id="65a53-150">System.String</span></span>

### <span data-ttu-id="65a53-151">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="65a53-151">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="65a53-152">System. Object</span><span class="sxs-lookup"><span data-stu-id="65a53-152">System.Object</span></span>

## <span data-ttu-id="65a53-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="65a53-153">OUTPUTS</span></span>

### <span data-ttu-id="65a53-154">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="65a53-154">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="65a53-155">Note</span><span class="sxs-lookup"><span data-stu-id="65a53-155">NOTES</span></span>

## <span data-ttu-id="65a53-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="65a53-156">RELATED LINKS</span></span>

[<span data-ttu-id="65a53-157">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="65a53-157">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)

[<span data-ttu-id="65a53-158">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="65a53-158">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="65a53-159">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="65a53-159">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="65a53-160">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="65a53-160">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="65a53-161">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="65a53-161">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
