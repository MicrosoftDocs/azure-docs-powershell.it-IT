---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssExtension.md
ms.openlocfilehash: fbf9d8c38c10465c565e40a284171b3232ba2949
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520125"
---
# <span data-ttu-id="3e358-101">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="3e358-101">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="3e358-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3e358-102">SYNOPSIS</span></span>
<span data-ttu-id="3e358-103">Aggiunge un'estensione a VMSS.</span><span class="sxs-lookup"><span data-stu-id="3e358-103">Adds an extension to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e358-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3e358-104">SYNTAX</span></span>

```
Add-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-ForceUpdateTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3e358-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e358-105">DESCRIPTION</span></span>
<span data-ttu-id="3e358-106">Il cmdlet **Add-AzureRmVmssExtension** aggiunge un'estensione al set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="3e358-106">The **Add-AzureRmVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="3e358-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3e358-107">EXAMPLES</span></span>

### <span data-ttu-id="3e358-108">Esempio 1: aggiungere un'estensione a VMSS</span><span class="sxs-lookup"><span data-stu-id="3e358-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="3e358-109">Questo comando aggiunge un'estensione a VMMS.</span><span class="sxs-lookup"><span data-stu-id="3e358-109">This command adds an extension to the VMMS.</span></span>

## <span data-ttu-id="3e358-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3e358-110">PARAMETERS</span></span>

### <span data-ttu-id="3e358-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="3e358-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="3e358-112">Indica se la versione dell'estensione deve essere aggiornata automaticamente a una versione secondaria più recente.</span><span class="sxs-lookup"><span data-stu-id="3e358-112">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

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

### <span data-ttu-id="3e358-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e358-113">-DefaultProfile</span></span>
<span data-ttu-id="3e358-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3e358-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e358-115">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="3e358-115">-ForceUpdateTag</span></span>
<span data-ttu-id="3e358-116">Se viene specificato un valore ed è diverso dal valore precedente, il gestore dell'estensione verrà costretto all'aggiornamento anche se la configurazione dell'estensione non è cambiata.</span><span class="sxs-lookup"><span data-stu-id="3e358-116">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="3e358-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="3e358-117">-Name</span></span>
<span data-ttu-id="3e358-118">Specifica il nome dell'estensione aggiunta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e358-118">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="3e358-119">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="3e358-119">-ProtectedSetting</span></span>
<span data-ttu-id="3e358-120">Specifica la configurazione privata per l'estensione, come stringa.</span><span class="sxs-lookup"><span data-stu-id="3e358-120">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="3e358-121">Questo cmdlet crittografa la configurazione privata.</span><span class="sxs-lookup"><span data-stu-id="3e358-121">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="3e358-122">-Publisher</span><span class="sxs-lookup"><span data-stu-id="3e358-122">-Publisher</span></span>
<span data-ttu-id="3e358-123">Specifica il nome dell'autore dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="3e358-123">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="3e358-124">L'editore fornisce un nome quando l'editore registra un'estensione.</span><span class="sxs-lookup"><span data-stu-id="3e358-124">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="3e358-125">Questo può usare il cmdlet [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) per ottenere il Publisher.</span><span class="sxs-lookup"><span data-stu-id="3e358-125">This can use the [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="3e358-126">-Impostazione</span><span class="sxs-lookup"><span data-stu-id="3e358-126">-Setting</span></span>
<span data-ttu-id="3e358-127">Specifica la configurazione pubblica, come stringa, per l'estensione.</span><span class="sxs-lookup"><span data-stu-id="3e358-127">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="3e358-128">Questo cmdlet non crittografa la configurazione pubblica.</span><span class="sxs-lookup"><span data-stu-id="3e358-128">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="3e358-129">-Digitare</span><span class="sxs-lookup"><span data-stu-id="3e358-129">-Type</span></span>
<span data-ttu-id="3e358-130">Specifica il tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="3e358-130">Specifies the extension type.</span></span>
<span data-ttu-id="3e358-131">Puoi usare il cmdlet [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) per ottenere il tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="3e358-131">You can use the [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="3e358-132">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="3e358-132">-TypeHandlerVersion</span></span>
<span data-ttu-id="3e358-133">Specifica la versione dell'estensione da usare per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3e358-133">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="3e358-134">Puoi usare il cmdlet [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) per ottenere la versione dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="3e358-134">You can use the [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="3e358-135">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3e358-135">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="3e358-136">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="3e358-136">Specify the VMSS object.</span></span>
<span data-ttu-id="3e358-137">Puoi usare il [nuovo-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3e358-137">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) to create the object.</span></span>

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

### <span data-ttu-id="3e358-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3e358-138">-Confirm</span></span>
<span data-ttu-id="3e358-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e358-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e358-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e358-140">-WhatIf</span></span>
<span data-ttu-id="3e358-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3e358-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3e358-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3e358-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e358-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e358-143">CommonParameters</span></span>
<span data-ttu-id="3e358-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e358-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e358-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e358-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e358-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3e358-146">INPUTS</span></span>

## <span data-ttu-id="3e358-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3e358-147">OUTPUTS</span></span>

###  
<span data-ttu-id="3e358-148">Questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="3e358-148">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="3e358-149">Note</span><span class="sxs-lookup"><span data-stu-id="3e358-149">NOTES</span></span>

## <span data-ttu-id="3e358-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3e358-150">RELATED LINKS</span></span>

[<span data-ttu-id="3e358-151">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="3e358-151">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)

[<span data-ttu-id="3e358-152">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="3e358-152">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="3e358-153">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="3e358-153">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="3e358-154">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="3e358-154">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="3e358-155">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="3e358-155">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
