---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssExtension.md
ms.openlocfilehash: 97c8824bca395ddd8fb23ebb4750ab35931c5d51
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863865"
---
# <span data-ttu-id="19e7d-101">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="19e7d-101">Add-AzVmssExtension</span></span>

## <span data-ttu-id="19e7d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="19e7d-102">SYNOPSIS</span></span>
<span data-ttu-id="19e7d-103">Aggiunge un'estensione a VMSS.</span><span class="sxs-lookup"><span data-stu-id="19e7d-103">Adds an extension to the VMSS.</span></span>

## <span data-ttu-id="19e7d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="19e7d-104">SYNTAX</span></span>

```
Add-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-ForceUpdateTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="19e7d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="19e7d-105">DESCRIPTION</span></span>
<span data-ttu-id="19e7d-106">Il cmdlet **Add-AzVmssExtension** aggiunge un'estensione al set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="19e7d-106">The **Add-AzVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="19e7d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="19e7d-107">EXAMPLES</span></span>

### <span data-ttu-id="19e7d-108">Esempio 1: aggiungere un'estensione a VMSS</span><span class="sxs-lookup"><span data-stu-id="19e7d-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="19e7d-109">Questo comando aggiunge un'estensione a VMMS.</span><span class="sxs-lookup"><span data-stu-id="19e7d-109">This command adds an extension to the VMMS.</span></span>

## <span data-ttu-id="19e7d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="19e7d-110">PARAMETERS</span></span>

### <span data-ttu-id="19e7d-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="19e7d-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="19e7d-112">Indica se la versione dell'estensione deve essere aggiornata automaticamente a una versione secondaria più recente.</span><span class="sxs-lookup"><span data-stu-id="19e7d-112">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

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

### <span data-ttu-id="19e7d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19e7d-113">-DefaultProfile</span></span>
<span data-ttu-id="19e7d-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="19e7d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19e7d-115">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="19e7d-115">-ForceUpdateTag</span></span>
<span data-ttu-id="19e7d-116">Se viene specificato un valore ed è diverso dal valore precedente, il gestore dell'estensione verrà costretto all'aggiornamento anche se la configurazione dell'estensione non è cambiata.</span><span class="sxs-lookup"><span data-stu-id="19e7d-116">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="19e7d-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="19e7d-117">-Name</span></span>
<span data-ttu-id="19e7d-118">Specifica il nome dell'estensione aggiunta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19e7d-118">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="19e7d-119">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="19e7d-119">-ProtectedSetting</span></span>
<span data-ttu-id="19e7d-120">Specifica la configurazione privata per l'estensione, come stringa.</span><span class="sxs-lookup"><span data-stu-id="19e7d-120">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="19e7d-121">Questo cmdlet crittografa la configurazione privata.</span><span class="sxs-lookup"><span data-stu-id="19e7d-121">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="19e7d-122">-Publisher</span><span class="sxs-lookup"><span data-stu-id="19e7d-122">-Publisher</span></span>
<span data-ttu-id="19e7d-123">Specifica il nome dell'autore dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="19e7d-123">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="19e7d-124">L'editore fornisce un nome quando l'editore registra un'estensione.</span><span class="sxs-lookup"><span data-stu-id="19e7d-124">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="19e7d-125">Questo può usare il cmdlet [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) per ottenere il Publisher.</span><span class="sxs-lookup"><span data-stu-id="19e7d-125">This can use the [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="19e7d-126">-Impostazione</span><span class="sxs-lookup"><span data-stu-id="19e7d-126">-Setting</span></span>
<span data-ttu-id="19e7d-127">Specifica la configurazione pubblica, come stringa, per l'estensione.</span><span class="sxs-lookup"><span data-stu-id="19e7d-127">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="19e7d-128">Questo cmdlet non crittografa la configurazione pubblica.</span><span class="sxs-lookup"><span data-stu-id="19e7d-128">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="19e7d-129">-Digitare</span><span class="sxs-lookup"><span data-stu-id="19e7d-129">-Type</span></span>
<span data-ttu-id="19e7d-130">Specifica il tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="19e7d-130">Specifies the extension type.</span></span>
<span data-ttu-id="19e7d-131">Puoi usare il cmdlet [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) per ottenere il tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="19e7d-131">You can use the [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="19e7d-132">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="19e7d-132">-TypeHandlerVersion</span></span>
<span data-ttu-id="19e7d-133">Specifica la versione dell'estensione da usare per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="19e7d-133">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="19e7d-134">Puoi usare il cmdlet [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) per ottenere la versione dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="19e7d-134">You can use the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="19e7d-135">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="19e7d-135">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="19e7d-136">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="19e7d-136">Specify the VMSS object.</span></span>
<span data-ttu-id="19e7d-137">Puoi usare il [nuovo-AzVmssConfig](./New-AzVmssConfig.md) per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="19e7d-137">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19e7d-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="19e7d-138">-Confirm</span></span>
<span data-ttu-id="19e7d-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19e7d-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19e7d-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19e7d-140">-WhatIf</span></span>
<span data-ttu-id="19e7d-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="19e7d-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="19e7d-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="19e7d-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19e7d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19e7d-143">CommonParameters</span></span>
<span data-ttu-id="19e7d-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19e7d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19e7d-145">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19e7d-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19e7d-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="19e7d-146">INPUTS</span></span>

### <span data-ttu-id="19e7d-147">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="19e7d-147">VirtualMachineScaleSet</span></span>
<span data-ttu-id="19e7d-148">Il parametro ' VirtualMachineScaleSet ' accetta il valore di tipo ' VirtualMachineScaleSet ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="19e7d-148">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="19e7d-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="19e7d-149">OUTPUTS</span></span>

###  
<span data-ttu-id="19e7d-150">Questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="19e7d-150">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="19e7d-151">Note</span><span class="sxs-lookup"><span data-stu-id="19e7d-151">NOTES</span></span>

## <span data-ttu-id="19e7d-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="19e7d-152">RELATED LINKS</span></span>

[<span data-ttu-id="19e7d-153">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="19e7d-153">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)

[<span data-ttu-id="19e7d-154">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="19e7d-154">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="19e7d-155">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="19e7d-155">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="19e7d-156">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="19e7d-156">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="19e7d-157">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="19e7d-157">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
