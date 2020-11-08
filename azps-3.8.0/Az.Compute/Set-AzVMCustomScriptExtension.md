---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 64AB1BAE-A756-43A8-A40F-10B746EA0946
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
ms.openlocfilehash: 4ed63b1afa2f72e8f557cc95381883973ae7feb4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022596"
---
# <span data-ttu-id="a678c-101">Set-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="a678c-101">Set-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="a678c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a678c-102">SYNOPSIS</span></span>
<span data-ttu-id="a678c-103">Aggiunge un'estensione di script personalizzata a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a678c-103">Adds a custom script extension to a virtual machine.</span></span>

## <span data-ttu-id="a678c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a678c-104">SYNTAX</span></span>

### <span data-ttu-id="a678c-105">ByNameWithContainerAndFileNamesParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a678c-105">ByNameWithContainerAndFileNamesParameterSet (Default)</span></span>
```
Set-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 -ContainerName <String> -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a678c-106">ByNameWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="a678c-106">ByNameWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-FileUri <String[]>] [-Run <String>] [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>]
 [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a678c-107">ByParentObjectWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="a678c-107">ByParentObjectWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -Name <String> -VMObject <PSVirtualMachine> -ContainerName <String>
 -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a678c-108">ByParentObjectWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="a678c-108">ByParentObjectWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -Name <String> -VMObject <PSVirtualMachine> [-FileUri <String[]>] [-Run <String>]
 [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a678c-109">ByResourceIdWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="a678c-109">ByResourceIdWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -ResourceId <String> -ContainerName <String> -FileName <String[]>
 [-StorageAccountName <String>] [-StorageEndpointSuffix <String>] [-StorageAccountKey <String>] [-Run <String>]
 [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a678c-110">ByResourceIdWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="a678c-110">ByResourceIdWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -ResourceId <String> [-FileUri <String[]>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a678c-111">ByInputObjectWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="a678c-111">ByInputObjectWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -InputObject <VirtualMachineCustomScriptExtensionContext> -ContainerName <String>
 -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a678c-112">ByInputObjectWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="a678c-112">ByInputObjectWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -InputObject <VirtualMachineCustomScriptExtensionContext> [-FileUri <String[]>]
 [-Run <String>] [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a678c-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a678c-113">DESCRIPTION</span></span>
<span data-ttu-id="a678c-114">Il cmdlet **set-AzVMCustomScriptExtension** aggiunge un'estensione di macchina virtuale script personalizzata a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a678c-114">The **Set-AzVMCustomScriptExtension** cmdlet adds a custom script Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="a678c-115">Questa estensione consente di eseguire script personalizzati nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a678c-115">This extension lets you run your own scripts on the virtual machine.</span></span>

## <span data-ttu-id="a678c-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a678c-116">EXAMPLES</span></span>

### <span data-ttu-id="a678c-117">Esempio 1: aggiungere uno script personalizzato</span><span class="sxs-lookup"><span data-stu-id="a678c-117">Example 1: Add a custom script</span></span>
```
PS C:\> Set-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "1.1" -StorageAccountName "Contoso" -StorageAccountKey <StorageKey> -FileName "ContosoScript.exe" -ContainerName "Scripts"
```

<span data-ttu-id="a678c-118">Questo comando aggiunge uno script personalizzato alla macchina virtuale denominata VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="a678c-118">This command adds a custom script to the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="a678c-119">Il file di script è contososcript.exe.</span><span class="sxs-lookup"><span data-stu-id="a678c-119">The script file is contososcript.exe.</span></span>

## <span data-ttu-id="a678c-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a678c-120">PARAMETERS</span></span>

### <span data-ttu-id="a678c-121">-Argomento</span><span class="sxs-lookup"><span data-stu-id="a678c-121">-Argument</span></span>
<span data-ttu-id="a678c-122">Specifica gli argomenti che l'estensione di script passa allo script.</span><span class="sxs-lookup"><span data-stu-id="a678c-122">Specifies arguments that the script extension passes to the script.</span></span>

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

### <span data-ttu-id="a678c-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="a678c-123">-ContainerName</span></span>
<span data-ttu-id="a678c-124">Specifica il nome del contenitore di archiviazione di Azure in cui questo cmdlet archivia lo script.</span><span class="sxs-lookup"><span data-stu-id="a678c-124">Specifies the name of the Azure storage container where this cmdlet stores the script.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a678c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a678c-125">-DefaultProfile</span></span>
<span data-ttu-id="a678c-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a678c-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a678c-127">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="a678c-127">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="a678c-128">-Nomefile</span><span class="sxs-lookup"><span data-stu-id="a678c-128">-FileName</span></span>
<span data-ttu-id="a678c-129">Specifica il nome del file di script.</span><span class="sxs-lookup"><span data-stu-id="a678c-129">Specifies the name of the script file.</span></span> <span data-ttu-id="a678c-130">Se il file è archiviato in archiviazione BLOB di Azure, il valore del nome del file è distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="a678c-130">If the file is stored in Azure Blob storage, the file name value is case-sensitive.</span></span> <span data-ttu-id="a678c-131">I nomi di file dei file archiviati nell'archiviazione di file di Azure non fanno distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="a678c-131">File names of files stored in Azure File storage are not case-sensitive.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a678c-132">-FileUri</span><span class="sxs-lookup"><span data-stu-id="a678c-132">-FileUri</span></span>
<span data-ttu-id="a678c-133">Specifica l'URI del file di script.</span><span class="sxs-lookup"><span data-stu-id="a678c-133">Specifies the URI of the script file.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByNameWithFileUriParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: ByParentObjectWithFileUriParameterSet, ByResourceIdWithFileUriParameterSet, ByInputObjectWithFileUriParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a678c-134">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="a678c-134">-ForceRerun</span></span>
<span data-ttu-id="a678c-135">Indica che questo cmdlet impone la ripetizione della stessa configurazione di estensione nella macchina virtuale senza disinstallare e reinstallare l'estensione.</span><span class="sxs-lookup"><span data-stu-id="a678c-135">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="a678c-136">Il valore può essere qualsiasi stringa diversa dal valore corrente.</span><span class="sxs-lookup"><span data-stu-id="a678c-136">The value can be any string different from the current value.</span></span>
<span data-ttu-id="a678c-137">Se forceUpdateTag non viene modificato, le modifiche apportate alle impostazioni pubbliche o protette verranno ancora applicate dal gestore.</span><span class="sxs-lookup"><span data-stu-id="a678c-137">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="a678c-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a678c-138">-InputObject</span></span>
<span data-ttu-id="a678c-139">Oggetto estensione VM.</span><span class="sxs-lookup"><span data-stu-id="a678c-139">VM extension object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.VirtualMachineCustomScriptExtensionContext
Parameter Sets: ByInputObjectWithContainerAndFileNamesParameterSet, ByInputObjectWithFileUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a678c-140">-Posizione</span><span class="sxs-lookup"><span data-stu-id="a678c-140">-Location</span></span>
<span data-ttu-id="a678c-141">Specifica la posizione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a678c-141">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="a678c-142">-Nome</span><span class="sxs-lookup"><span data-stu-id="a678c-142">-Name</span></span>
<span data-ttu-id="a678c-143">Specifica il nome dell'estensione di script personalizzata.</span><span class="sxs-lookup"><span data-stu-id="a678c-143">Specifies the name of the custom script extension.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet, ByNameWithFileUriParameterSet
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByParentObjectWithFileUriParameterSet
Aliases: ExtensionName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a678c-144">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="a678c-144">-NoWait</span></span>
<span data-ttu-id="a678c-145">Avvia l'operazione e restituisce immediatamente, prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="a678c-145">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="a678c-146">Per determinare se l'operazione è stata completata correttamente, usare un altro meccanismo.</span><span class="sxs-lookup"><span data-stu-id="a678c-146">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="a678c-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a678c-147">-ResourceGroupName</span></span>
<span data-ttu-id="a678c-148">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a678c-148">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet, ByNameWithFileUriParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a678c-149">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a678c-149">-ResourceId</span></span>
<span data-ttu-id="a678c-150">Estensione della VM ResourceID.</span><span class="sxs-lookup"><span data-stu-id="a678c-150">VM extension ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdWithContainerAndFileNamesParameterSet, ByResourceIdWithFileUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a678c-151">-Run</span><span class="sxs-lookup"><span data-stu-id="a678c-151">-Run</span></span>
<span data-ttu-id="a678c-152">Specifica il comando da usare per eseguire lo script.</span><span class="sxs-lookup"><span data-stu-id="a678c-152">Specifies the command to use that runs your script.</span></span>

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

### <span data-ttu-id="a678c-153">-SecureExecution</span><span class="sxs-lookup"><span data-stu-id="a678c-153">-SecureExecution</span></span>
<span data-ttu-id="a678c-154">Indica che questo cmdlet assicura che il valore del parametro *Run* non sia connesso al server o venga restituito all'utente usando l'API di estensione Get.</span><span class="sxs-lookup"><span data-stu-id="a678c-154">Indicates that this cmdlet makes sure that the value of the *Run* parameter is not logged on the server or returned to the user by using the GET extension API.</span></span>
<span data-ttu-id="a678c-155">Il valore di *Run* può contenere segreti o password da passare al file di script in modo sicuro.</span><span class="sxs-lookup"><span data-stu-id="a678c-155">The value of *Run* might contain secrets or passwords to be passed to the script file securely.</span></span>

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

### <span data-ttu-id="a678c-156">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="a678c-156">-StorageAccountKey</span></span>
<span data-ttu-id="a678c-157">Specifica la chiave per il contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="a678c-157">Specifies the key for the Azure storage container.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a678c-158">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a678c-158">-StorageAccountName</span></span>
<span data-ttu-id="a678c-159">Specifica il nome dell'account di archiviazione di Azure in cui questo cmdlet archivia lo script.</span><span class="sxs-lookup"><span data-stu-id="a678c-159">Specifies the name of the Azure storage account where this cmdlet stores the script.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a678c-160">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="a678c-160">-StorageEndpointSuffix</span></span>
<span data-ttu-id="a678c-161">Specifica il suffisso dell'endpoint di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a678c-161">Specifies the storage endpoint suffix.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a678c-162">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="a678c-162">-TypeHandlerVersion</span></span>
<span data-ttu-id="a678c-163">Specifica la versione dell'estensione da usare per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a678c-163">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="a678c-164">Per ottenere la versione, eseguire il cmdlet Get-AzVMExtensionImage con il valore Microsoft. COMPUTE per il parametro *PublisherName* e CustomScriptExtension per il parametro *Type* .</span><span class="sxs-lookup"><span data-stu-id="a678c-164">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and CustomScriptExtension for the *Type* parameter.</span></span>

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

### <span data-ttu-id="a678c-165">-VMName</span><span class="sxs-lookup"><span data-stu-id="a678c-165">-VMName</span></span>
<span data-ttu-id="a678c-166">Specifica il nome di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a678c-166">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="a678c-167">Questo cmdlet aggiunge l'estensione di script personalizzata per la macchina virtuale specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="a678c-167">This cmdlet adds the custom script extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet, ByNameWithFileUriParameterSet
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a678c-168">-VMObject</span><span class="sxs-lookup"><span data-stu-id="a678c-168">-VMObject</span></span>
<span data-ttu-id="a678c-169">Oggetto VM.</span><span class="sxs-lookup"><span data-stu-id="a678c-169">VM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByParentObjectWithFileUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a678c-170">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a678c-170">-Confirm</span></span>
<span data-ttu-id="a678c-171">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a678c-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a678c-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a678c-172">-WhatIf</span></span>
<span data-ttu-id="a678c-173">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a678c-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a678c-174">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a678c-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a678c-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a678c-175">CommonParameters</span></span>
<span data-ttu-id="a678c-176">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a678c-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a678c-177">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a678c-177">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a678c-178">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a678c-178">INPUTS</span></span>

### <span data-ttu-id="a678c-179">System. String</span><span class="sxs-lookup"><span data-stu-id="a678c-179">System.String</span></span>

### <span data-ttu-id="a678c-180">System. String []</span><span class="sxs-lookup"><span data-stu-id="a678c-180">System.String[]</span></span>

### <span data-ttu-id="a678c-181">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a678c-181">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a678c-182">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a678c-182">OUTPUTS</span></span>

### <span data-ttu-id="a678c-183">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="a678c-183">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="a678c-184">Note</span><span class="sxs-lookup"><span data-stu-id="a678c-184">NOTES</span></span>

## <span data-ttu-id="a678c-185">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a678c-185">RELATED LINKS</span></span>

[<span data-ttu-id="a678c-186">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="a678c-186">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="a678c-187">Remove-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="a678c-187">Remove-AzVMCustomScriptExtension</span></span>](./Remove-AzVMCustomScriptExtension.md)


