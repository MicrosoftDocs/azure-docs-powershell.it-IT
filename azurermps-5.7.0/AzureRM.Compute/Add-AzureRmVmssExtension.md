---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssExtension.md
ms.openlocfilehash: 20446fc7c93000b29680689001d9e3c40c4862e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508383"
---
# <span data-ttu-id="264a5-101">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="264a5-101">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="264a5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="264a5-102">SYNOPSIS</span></span>
<span data-ttu-id="264a5-103">Aggiunge un'estensione a VMSS.</span><span class="sxs-lookup"><span data-stu-id="264a5-103">Adds an extension to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="264a5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="264a5-104">SYNTAX</span></span>

```
Add-AzureRmVmssExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="264a5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="264a5-105">DESCRIPTION</span></span>
<span data-ttu-id="264a5-106">Il cmdlet **Add-AzureRmVmssExtension** aggiunge un'estensione al set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="264a5-106">The **Add-AzureRmVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="264a5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="264a5-107">EXAMPLES</span></span>

### <span data-ttu-id="264a5-108">Esempio 1: aggiungere un'estensione a VMSS</span><span class="sxs-lookup"><span data-stu-id="264a5-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="264a5-109">Questo comando aggiunge un'estensione a VMMS.</span><span class="sxs-lookup"><span data-stu-id="264a5-109">This command adds an extension to the VMMS.</span></span>

## <span data-ttu-id="264a5-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="264a5-110">PARAMETERS</span></span>

### <span data-ttu-id="264a5-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="264a5-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="264a5-112">Indica se la versione dell'estensione deve essere aggiornata automaticamente a una versione secondaria più recente.</span><span class="sxs-lookup"><span data-stu-id="264a5-112">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="264a5-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="264a5-113">-Name</span></span>
<span data-ttu-id="264a5-114">Specifica il nome dell'estensione aggiunta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="264a5-114">Specifies the name of the extension that this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="264a5-115">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="264a5-115">-ProtectedSetting</span></span>
<span data-ttu-id="264a5-116">Specifica la configurazione privata per l'estensione, come stringa.</span><span class="sxs-lookup"><span data-stu-id="264a5-116">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="264a5-117">Questo cmdlet crittografa la configurazione privata.</span><span class="sxs-lookup"><span data-stu-id="264a5-117">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="264a5-118">-Publisher</span><span class="sxs-lookup"><span data-stu-id="264a5-118">-Publisher</span></span>
<span data-ttu-id="264a5-119">Specifica il nome dell'autore dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="264a5-119">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="264a5-120">L'editore fornisce un nome quando l'editore registra un'estensione.</span><span class="sxs-lookup"><span data-stu-id="264a5-120">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="264a5-121">Questo può usare il cmdlet [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) per ottenere il Publisher.</span><span class="sxs-lookup"><span data-stu-id="264a5-121">This can use the [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) cmdlet to get the publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="264a5-122">-Impostazione</span><span class="sxs-lookup"><span data-stu-id="264a5-122">-Setting</span></span>
<span data-ttu-id="264a5-123">Specifica la configurazione pubblica, come stringa, per l'estensione.</span><span class="sxs-lookup"><span data-stu-id="264a5-123">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="264a5-124">Questo cmdlet non crittografa la configurazione pubblica.</span><span class="sxs-lookup"><span data-stu-id="264a5-124">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="264a5-125">-Digitare</span><span class="sxs-lookup"><span data-stu-id="264a5-125">-Type</span></span>
<span data-ttu-id="264a5-126">Specifica il tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="264a5-126">Specifies the extension type.</span></span>
<span data-ttu-id="264a5-127">Puoi usare il cmdlet [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) per ottenere il tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="264a5-127">You can use the [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="264a5-128">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="264a5-128">-TypeHandlerVersion</span></span>
<span data-ttu-id="264a5-129">Specifica la versione dell'estensione da usare per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="264a5-129">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="264a5-130">Puoi usare il cmdlet [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) per ottenere la versione dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="264a5-130">You can use the [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="264a5-131">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="264a5-131">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="264a5-132">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="264a5-132">Specify the VMSS object.</span></span>
<span data-ttu-id="264a5-133">Puoi usare il [nuovo-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="264a5-133">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="264a5-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="264a5-134">-Confirm</span></span>
<span data-ttu-id="264a5-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="264a5-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="264a5-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="264a5-136">-WhatIf</span></span>
<span data-ttu-id="264a5-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="264a5-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="264a5-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="264a5-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="264a5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="264a5-139">CommonParameters</span></span>
<span data-ttu-id="264a5-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="264a5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="264a5-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="264a5-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="264a5-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="264a5-142">INPUTS</span></span>

### <span data-ttu-id="264a5-143">Nessuno</span><span class="sxs-lookup"><span data-stu-id="264a5-143">None</span></span>
<span data-ttu-id="264a5-144">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="264a5-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="264a5-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="264a5-145">OUTPUTS</span></span>

###  
<span data-ttu-id="264a5-146">Questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="264a5-146">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="264a5-147">Note</span><span class="sxs-lookup"><span data-stu-id="264a5-147">NOTES</span></span>

## <span data-ttu-id="264a5-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="264a5-148">RELATED LINKS</span></span>

[<span data-ttu-id="264a5-149">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="264a5-149">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)

[<span data-ttu-id="264a5-150">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="264a5-150">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="264a5-151">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="264a5-151">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="264a5-152">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="264a5-152">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="264a5-153">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="264a5-153">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
