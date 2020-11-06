---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 64AB1BAE-A756-43A8-A40F-10B746EA0946
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMCustomScriptExtension.md
ms.openlocfilehash: 693809e46823cbcb8331eade7b8cd38c83238be2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512695"
---
# <span data-ttu-id="97651-101">Set-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="97651-101">Set-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="97651-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="97651-102">SYNOPSIS</span></span>
<span data-ttu-id="97651-103">Aggiunge un'estensione di script personalizzata a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="97651-103">Adds a custom script extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97651-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="97651-104">SYNTAX</span></span>

### <span data-ttu-id="97651-105">SetCustomScriptExtensionByContainerAndFileNames (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="97651-105">SetCustomScriptExtensionByContainerAndFileNames (Default)</span></span>
```
Set-AzureRmVMCustomScriptExtension -ContainerName <String> -FileName <String[]> [-StorageAccountName <String>]
 [-StorageEndpointSuffix <String>] [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97651-106">SetCustomScriptExtensionByUriLinks</span><span class="sxs-lookup"><span data-stu-id="97651-106">SetCustomScriptExtensionByUriLinks</span></span>
```
Set-AzureRmVMCustomScriptExtension [-FileUri <String[]>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97651-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="97651-107">DESCRIPTION</span></span>
<span data-ttu-id="97651-108">Il cmdlet **set-AzureRmVMCustomScriptExtension** aggiunge un'estensione di macchina virtuale script personalizzata a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="97651-108">The **Set-AzureRmVMCustomScriptExtension** cmdlet adds a custom script Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="97651-109">Questa estensione consente di eseguire script personalizzati nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="97651-109">This extension lets you run your own scripts on the virtual machine.</span></span>

## <span data-ttu-id="97651-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="97651-110">EXAMPLES</span></span>

### <span data-ttu-id="97651-111">Esempio 1: aggiungere uno script personalizzato</span><span class="sxs-lookup"><span data-stu-id="97651-111">Example 1: Add a custom script</span></span>
```
PS C:\> Set-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "1.1" -StorageAccountName "Contoso" -StorageAccountKey <StorageKey> -FileName "ContosoScript.exe" -ContainerName "Scripts"
```

<span data-ttu-id="97651-112">Questo comando aggiunge uno script personalizzato alla macchina virtuale denominata VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="97651-112">This command adds a custom script to the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="97651-113">Il file di script è contososcript.exe.</span><span class="sxs-lookup"><span data-stu-id="97651-113">The script file is contososcript.exe.</span></span>

## <span data-ttu-id="97651-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="97651-114">PARAMETERS</span></span>

### <span data-ttu-id="97651-115">-Argomento</span><span class="sxs-lookup"><span data-stu-id="97651-115">-Argument</span></span>
<span data-ttu-id="97651-116">Specifica gli argomenti che l'estensione di script passa allo script.</span><span class="sxs-lookup"><span data-stu-id="97651-116">Specifies arguments that the script extension passes to the script.</span></span>

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

### <span data-ttu-id="97651-117">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="97651-117">-ContainerName</span></span>
<span data-ttu-id="97651-118">Specifica il nome del contenitore di archiviazione di Azure in cui questo cmdlet archivia lo script.</span><span class="sxs-lookup"><span data-stu-id="97651-118">Specifies the name of the Azure storage container where this cmdlet stores the script.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97651-119">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="97651-119">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="97651-120">-Nomefile</span><span class="sxs-lookup"><span data-stu-id="97651-120">-FileName</span></span>
<span data-ttu-id="97651-121">Specifica il nome del file di script.</span><span class="sxs-lookup"><span data-stu-id="97651-121">Specifies the name of the script file.</span></span>

```yaml
Type: String[]
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97651-122">-FileUri</span><span class="sxs-lookup"><span data-stu-id="97651-122">-FileUri</span></span>
<span data-ttu-id="97651-123">Specifica l'URI del file di script.</span><span class="sxs-lookup"><span data-stu-id="97651-123">Specifies the URI of the script file.</span></span>

```yaml
Type: String[]
Parameter Sets: SetCustomScriptExtensionByUriLinks
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97651-124">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="97651-124">-ForceRerun</span></span>
<span data-ttu-id="97651-125">Indica che questo cmdlet impone la ripetizione della stessa configurazione di estensione nella macchina virtuale senza disinstallare e reinstallare l'estensione.</span><span class="sxs-lookup"><span data-stu-id="97651-125">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="97651-126">Il valore può essere qualsiasi stringa diversa dal valore corrente.</span><span class="sxs-lookup"><span data-stu-id="97651-126">The value can be any string different from the current value.</span></span>

<span data-ttu-id="97651-127">Se forceUpdateTag non viene modificato, le modifiche apportate alle impostazioni pubbliche o protette verranno ancora applicate dal gestore.</span><span class="sxs-lookup"><span data-stu-id="97651-127">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="97651-128">-Posizione</span><span class="sxs-lookup"><span data-stu-id="97651-128">-Location</span></span>
<span data-ttu-id="97651-129">Specifica la posizione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="97651-129">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="97651-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="97651-130">-Name</span></span>
<span data-ttu-id="97651-131">Specifica il nome dell'estensione di script personalizzata.</span><span class="sxs-lookup"><span data-stu-id="97651-131">Specifies the name of the custom script extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97651-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97651-132">-ResourceGroupName</span></span>
<span data-ttu-id="97651-133">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="97651-133">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="97651-134">-Run</span><span class="sxs-lookup"><span data-stu-id="97651-134">-Run</span></span>
<span data-ttu-id="97651-135">Specifica il comando da usare per eseguire lo script.</span><span class="sxs-lookup"><span data-stu-id="97651-135">Specifies the command to use that runs your script.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunFile, Command

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97651-136">-SecureExecution</span><span class="sxs-lookup"><span data-stu-id="97651-136">-SecureExecution</span></span>
<span data-ttu-id="97651-137">Indica che questo cmdlet assicura che il valore del parametro *Run* non sia connesso al server o venga restituito all'utente usando l'API di estensione Get.</span><span class="sxs-lookup"><span data-stu-id="97651-137">Indicates that this cmdlet makes sure that the value of the *Run* parameter is not logged on the server or returned to the user by using the GET extension API.</span></span>
<span data-ttu-id="97651-138">Il valore di *Run* può contenere segreti o password da passare al file di script in modo sicuro.</span><span class="sxs-lookup"><span data-stu-id="97651-138">The value of *Run* might contain secrets or passwords to be passed to the script file securely.</span></span>

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

### <span data-ttu-id="97651-139">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="97651-139">-StorageAccountKey</span></span>
<span data-ttu-id="97651-140">Specifica la chiave per il contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="97651-140">Specifies the key for the Azure storage container.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97651-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="97651-141">-StorageAccountName</span></span>
<span data-ttu-id="97651-142">Specifica il nome dell'account di archiviazione di Azure in cui questo cmdlet archivia lo script.</span><span class="sxs-lookup"><span data-stu-id="97651-142">Specifies the name of the Azure storage account where this cmdlet stores the script.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97651-143">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="97651-143">-StorageEndpointSuffix</span></span>
<span data-ttu-id="97651-144">Specifica il suffisso dell'endpoint di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="97651-144">Specifies the storage endpoint suffix.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97651-145">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="97651-145">-TypeHandlerVersion</span></span>
<span data-ttu-id="97651-146">Specifica la versione dell'estensione da usare per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="97651-146">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="97651-147">Per ottenere la versione, eseguire il cmdlet Get-AzureRmVMExtensionImage con il valore Microsoft. COMPUTE per il parametro *PublisherName* e VMAccessAgent per il parametro *Type* .</span><span class="sxs-lookup"><span data-stu-id="97651-147">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

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

### <span data-ttu-id="97651-148">-VMName</span><span class="sxs-lookup"><span data-stu-id="97651-148">-VMName</span></span>
<span data-ttu-id="97651-149">Specifica il nome di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="97651-149">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="97651-150">Questo cmdlet aggiunge l'estensione di script personalizzata per la macchina virtuale specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="97651-150">This cmdlet adds the custom script extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97651-151">-Confermare</span><span class="sxs-lookup"><span data-stu-id="97651-151">-Confirm</span></span>
<span data-ttu-id="97651-152">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97651-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97651-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97651-153">-WhatIf</span></span>
<span data-ttu-id="97651-154">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="97651-154">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="97651-155">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="97651-155">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97651-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97651-156">CommonParameters</span></span>
<span data-ttu-id="97651-157">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97651-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97651-158">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97651-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97651-159">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="97651-159">INPUTS</span></span>

### <span data-ttu-id="97651-160">Nessuno</span><span class="sxs-lookup"><span data-stu-id="97651-160">None</span></span>
<span data-ttu-id="97651-161">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="97651-161">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="97651-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="97651-162">OUTPUTS</span></span>

## <span data-ttu-id="97651-163">Note</span><span class="sxs-lookup"><span data-stu-id="97651-163">NOTES</span></span>

## <span data-ttu-id="97651-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="97651-164">RELATED LINKS</span></span>

[<span data-ttu-id="97651-165">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="97651-165">Get-AzureRmVMCustomScriptExtension</span></span>](./Get-AzureRmVMCustomScriptExtension.md)

[<span data-ttu-id="97651-166">Remove-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="97651-166">Remove-AzureRmVMCustomScriptExtension</span></span>](./Remove-AzureRmVMCustomScriptExtension.md)


