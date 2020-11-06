---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 64AB1BAE-A756-43A8-A40F-10B746EA0946
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMCustomScriptExtension.md
ms.openlocfilehash: 926a33040421acbcb6424c89ec10da89ad87e5ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515467"
---
# <span data-ttu-id="7e10c-101">Set-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="7e10c-101">Set-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="7e10c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7e10c-102">SYNOPSIS</span></span>
<span data-ttu-id="7e10c-103">Aggiunge un'estensione di script personalizzata a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7e10c-103">Adds a custom script extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e10c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7e10c-104">SYNTAX</span></span>

### <span data-ttu-id="7e10c-105">SetCustomScriptExtensionByContainerAndFileNames (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7e10c-105">SetCustomScriptExtensionByContainerAndFileNames (Default)</span></span>
```
Set-AzureRmVMCustomScriptExtension -ContainerName <String> -FileName <String[]> [-StorageAccountName <String>]
 [-StorageEndpointSuffix <String>] [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e10c-106">SetCustomScriptExtensionByUriLinks</span><span class="sxs-lookup"><span data-stu-id="7e10c-106">SetCustomScriptExtensionByUriLinks</span></span>
```
Set-AzureRmVMCustomScriptExtension [-FileUri <String[]>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e10c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e10c-107">DESCRIPTION</span></span>
<span data-ttu-id="7e10c-108">Il cmdlet **set-AzureRmVMCustomScriptExtension** aggiunge un'estensione di macchina virtuale script personalizzata a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7e10c-108">The **Set-AzureRmVMCustomScriptExtension** cmdlet adds a custom script Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="7e10c-109">Questa estensione consente di eseguire script personalizzati nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7e10c-109">This extension lets you run your own scripts on the virtual machine.</span></span>

## <span data-ttu-id="7e10c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7e10c-110">EXAMPLES</span></span>

### <span data-ttu-id="7e10c-111">Esempio 1: aggiungere uno script personalizzato</span><span class="sxs-lookup"><span data-stu-id="7e10c-111">Example 1: Add a custom script</span></span>
```
PS C:\> Set-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "1.1" -StorageAccountName "Contoso" -StorageAccountKey <StorageKey> -FileName "ContosoScript.exe" -ContainerName "Scripts"
```

<span data-ttu-id="7e10c-112">Questo comando aggiunge uno script personalizzato alla macchina virtuale denominata VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="7e10c-112">This command adds a custom script to the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="7e10c-113">Il file di script è contososcript.exe.</span><span class="sxs-lookup"><span data-stu-id="7e10c-113">The script file is contososcript.exe.</span></span>

## <span data-ttu-id="7e10c-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7e10c-114">PARAMETERS</span></span>

### <span data-ttu-id="7e10c-115">-Argomento</span><span class="sxs-lookup"><span data-stu-id="7e10c-115">-Argument</span></span>
<span data-ttu-id="7e10c-116">Specifica gli argomenti che l'estensione di script passa allo script.</span><span class="sxs-lookup"><span data-stu-id="7e10c-116">Specifies arguments that the script extension passes to the script.</span></span>

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

### <span data-ttu-id="7e10c-117">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="7e10c-117">-ContainerName</span></span>
<span data-ttu-id="7e10c-118">Specifica il nome del contenitore di archiviazione di Azure in cui questo cmdlet archivia lo script.</span><span class="sxs-lookup"><span data-stu-id="7e10c-118">Specifies the name of the Azure storage container where this cmdlet stores the script.</span></span>

```yaml
Type: System.String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e10c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e10c-119">-DefaultProfile</span></span>
<span data-ttu-id="7e10c-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7e10c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e10c-121">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="7e10c-121">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="7e10c-122">-Nomefile</span><span class="sxs-lookup"><span data-stu-id="7e10c-122">-FileName</span></span>
<span data-ttu-id="7e10c-123">Specifica il nome del file di script.</span><span class="sxs-lookup"><span data-stu-id="7e10c-123">Specifies the name of the script file.</span></span> <span data-ttu-id="7e10c-124">Se il file è archiviato in archiviazione BLOB di Azure, il valore del nome file è case-senstive.</span><span class="sxs-lookup"><span data-stu-id="7e10c-124">If the file is stored in Azure Blob storage, the file name value is case-senstive.</span></span> <span data-ttu-id="7e10c-125">I nomi dei file archiviati nell'archiviazione di file di Azure non sono case-senstive.</span><span class="sxs-lookup"><span data-stu-id="7e10c-125">File names of files stored in Azure File storage are not case-senstive.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e10c-126">-FileUri</span><span class="sxs-lookup"><span data-stu-id="7e10c-126">-FileUri</span></span>
<span data-ttu-id="7e10c-127">Specifica l'URI del file di script.</span><span class="sxs-lookup"><span data-stu-id="7e10c-127">Specifies the URI of the script file.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetCustomScriptExtensionByUriLinks
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e10c-128">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="7e10c-128">-ForceRerun</span></span>
<span data-ttu-id="7e10c-129">Indica che questo cmdlet impone la ripetizione della stessa configurazione di estensione nella macchina virtuale senza disinstallare e reinstallare l'estensione.</span><span class="sxs-lookup"><span data-stu-id="7e10c-129">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="7e10c-130">Il valore può essere qualsiasi stringa diversa dal valore corrente.</span><span class="sxs-lookup"><span data-stu-id="7e10c-130">The value can be any string different from the current value.</span></span>
<span data-ttu-id="7e10c-131">Se forceUpdateTag non viene modificato, le modifiche apportate alle impostazioni pubbliche o protette verranno ancora applicate dal gestore.</span><span class="sxs-lookup"><span data-stu-id="7e10c-131">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="7e10c-132">-Posizione</span><span class="sxs-lookup"><span data-stu-id="7e10c-132">-Location</span></span>
<span data-ttu-id="7e10c-133">Specifica la posizione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7e10c-133">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="7e10c-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="7e10c-134">-Name</span></span>
<span data-ttu-id="7e10c-135">Specifica il nome dell'estensione di script personalizzata.</span><span class="sxs-lookup"><span data-stu-id="7e10c-135">Specifies the name of the custom script extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e10c-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e10c-136">-ResourceGroupName</span></span>
<span data-ttu-id="7e10c-137">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7e10c-137">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="7e10c-138">-Run</span><span class="sxs-lookup"><span data-stu-id="7e10c-138">-Run</span></span>
<span data-ttu-id="7e10c-139">Specifica il comando da usare per eseguire lo script.</span><span class="sxs-lookup"><span data-stu-id="7e10c-139">Specifies the command to use that runs your script.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunFile, Command

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e10c-140">-SecureExecution</span><span class="sxs-lookup"><span data-stu-id="7e10c-140">-SecureExecution</span></span>
<span data-ttu-id="7e10c-141">Indica che questo cmdlet assicura che il valore del parametro *Run* non sia connesso al server o venga restituito all'utente usando l'API di estensione Get.</span><span class="sxs-lookup"><span data-stu-id="7e10c-141">Indicates that this cmdlet makes sure that the value of the *Run* parameter is not logged on the server or returned to the user by using the GET extension API.</span></span>
<span data-ttu-id="7e10c-142">Il valore di *Run* può contenere segreti o password da passare al file di script in modo sicuro.</span><span class="sxs-lookup"><span data-stu-id="7e10c-142">The value of *Run* might contain secrets or passwords to be passed to the script file securely.</span></span>

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

### <span data-ttu-id="7e10c-143">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="7e10c-143">-StorageAccountKey</span></span>
<span data-ttu-id="7e10c-144">Specifica la chiave per il contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="7e10c-144">Specifies the key for the Azure storage container.</span></span>

```yaml
Type: System.String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e10c-145">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7e10c-145">-StorageAccountName</span></span>
<span data-ttu-id="7e10c-146">Specifica il nome dell'account di archiviazione di Azure in cui questo cmdlet archivia lo script.</span><span class="sxs-lookup"><span data-stu-id="7e10c-146">Specifies the name of the Azure storage account where this cmdlet stores the script.</span></span>

```yaml
Type: System.String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e10c-147">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="7e10c-147">-StorageEndpointSuffix</span></span>
<span data-ttu-id="7e10c-148">Specifica il suffisso dell'endpoint di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7e10c-148">Specifies the storage endpoint suffix.</span></span>

```yaml
Type: System.String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e10c-149">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="7e10c-149">-TypeHandlerVersion</span></span>
<span data-ttu-id="7e10c-150">Specifica la versione dell'estensione da usare per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7e10c-150">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="7e10c-151">Per ottenere la versione, eseguire il cmdlet Get-AzureRmVMExtensionImage con il valore Microsoft. COMPUTE per il parametro *PublisherName* e VMAccessAgent per il parametro *Type* .</span><span class="sxs-lookup"><span data-stu-id="7e10c-151">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

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

### <span data-ttu-id="7e10c-152">-VMName</span><span class="sxs-lookup"><span data-stu-id="7e10c-152">-VMName</span></span>
<span data-ttu-id="7e10c-153">Specifica il nome di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7e10c-153">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="7e10c-154">Questo cmdlet aggiunge l'estensione di script personalizzata per la macchina virtuale specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="7e10c-154">This cmdlet adds the custom script extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e10c-155">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7e10c-155">-Confirm</span></span>
<span data-ttu-id="7e10c-156">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e10c-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e10c-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e10c-157">-WhatIf</span></span>
<span data-ttu-id="7e10c-158">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7e10c-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e10c-159">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7e10c-159">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e10c-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e10c-160">CommonParameters</span></span>
<span data-ttu-id="7e10c-161">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e10c-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e10c-162">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e10c-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e10c-163">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7e10c-163">INPUTS</span></span>

### <span data-ttu-id="7e10c-164">System. String</span><span class="sxs-lookup"><span data-stu-id="7e10c-164">System.String</span></span>

### <span data-ttu-id="7e10c-165">System. String []</span><span class="sxs-lookup"><span data-stu-id="7e10c-165">System.String[]</span></span>

### <span data-ttu-id="7e10c-166">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7e10c-166">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7e10c-167">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7e10c-167">OUTPUTS</span></span>

### <span data-ttu-id="7e10c-168">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="7e10c-168">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="7e10c-169">Note</span><span class="sxs-lookup"><span data-stu-id="7e10c-169">NOTES</span></span>

## <span data-ttu-id="7e10c-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7e10c-170">RELATED LINKS</span></span>

[<span data-ttu-id="7e10c-171">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="7e10c-171">Get-AzureRmVMCustomScriptExtension</span></span>](./Get-AzureRmVMCustomScriptExtension.md)

[<span data-ttu-id="7e10c-172">Remove-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="7e10c-172">Remove-AzureRmVMCustomScriptExtension</span></span>](./Remove-AzureRmVMCustomScriptExtension.md)

