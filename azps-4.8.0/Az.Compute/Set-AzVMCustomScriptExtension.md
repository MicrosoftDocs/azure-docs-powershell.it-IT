---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 64AB1BAE-A756-43A8-A40F-10B746EA0946
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
ms.openlocfilehash: 69b6dec11f0135803320bb7b58bdb8362aaee26e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031858"
---
# <span data-ttu-id="dfe76-101">Set-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="dfe76-101">Set-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="dfe76-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dfe76-102">SYNOPSIS</span></span>
<span data-ttu-id="dfe76-103">Aggiunge un'estensione di script personalizzata a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dfe76-103">Adds a custom script extension to a virtual machine.</span></span>

## <span data-ttu-id="dfe76-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dfe76-104">SYNTAX</span></span>

### <span data-ttu-id="dfe76-105">ByNameWithContainerAndFileNamesParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dfe76-105">ByNameWithContainerAndFileNamesParameterSet (Default)</span></span>
```
Set-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 -ContainerName <String> -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfe76-106">ByNameWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="dfe76-106">ByNameWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-FileUri <String[]>] [-Run <String>] [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>]
 [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfe76-107">ByParentObjectWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="dfe76-107">ByParentObjectWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -Name <String> -VMObject <PSVirtualMachine> -ContainerName <String>
 -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfe76-108">ByParentObjectWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="dfe76-108">ByParentObjectWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -Name <String> -VMObject <PSVirtualMachine> [-FileUri <String[]>] [-Run <String>]
 [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfe76-109">ByResourceIdWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="dfe76-109">ByResourceIdWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -ResourceId <String> -ContainerName <String> -FileName <String[]>
 [-StorageAccountName <String>] [-StorageEndpointSuffix <String>] [-StorageAccountKey <String>] [-Run <String>]
 [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfe76-110">ByResourceIdWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="dfe76-110">ByResourceIdWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -ResourceId <String> [-FileUri <String[]>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dfe76-111">ByInputObjectWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="dfe76-111">ByInputObjectWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -InputObject <VirtualMachineCustomScriptExtensionContext> -ContainerName <String>
 -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfe76-112">ByInputObjectWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="dfe76-112">ByInputObjectWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -InputObject <VirtualMachineCustomScriptExtensionContext> [-FileUri <String[]>]
 [-Run <String>] [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfe76-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dfe76-113">DESCRIPTION</span></span>
<span data-ttu-id="dfe76-114">Il cmdlet **set-AzVMCustomScriptExtension** aggiunge un'estensione di macchina virtuale script personalizzata a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dfe76-114">The **Set-AzVMCustomScriptExtension** cmdlet adds a custom script Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="dfe76-115">Questa estensione consente di eseguire script personalizzati nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dfe76-115">This extension lets you run your own scripts on the virtual machine.</span></span>

## <span data-ttu-id="dfe76-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dfe76-116">EXAMPLES</span></span>

### <span data-ttu-id="dfe76-117">Esempio 1: aggiungere uno script personalizzato</span><span class="sxs-lookup"><span data-stu-id="dfe76-117">Example 1: Add a custom script</span></span>
```powershell
PS C:\> Set-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "1.1" -StorageAccountName "Contoso" -StorageAccountKey <StorageKey> -FileName "ContosoScript.exe" -ContainerName "Scripts"
```

<span data-ttu-id="dfe76-118">Questo comando aggiunge uno script personalizzato alla macchina virtuale denominata VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="dfe76-118">This command adds a custom script to the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="dfe76-119">Il file di script è contososcript.exe.</span><span class="sxs-lookup"><span data-stu-id="dfe76-119">The script file is contososcript.exe.</span></span>

### <span data-ttu-id="dfe76-120">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="dfe76-120">Example 2</span></span>

<span data-ttu-id="dfe76-121">Aggiunge un'estensione di script personalizzata a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dfe76-121">Adds a custom script extension to a virtual machine.</span></span> <span data-ttu-id="dfe76-122">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="dfe76-122">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzVMCustomScriptExtension -Argument <String> -ContainerName 'Scripts' -DefaultProfile <IAzureContextContainer> -FileName 'ContosoScript.exe' -Location 'Central US' -Name 'ContosoTest' -ResourceGroupName 'ResourceGroup11' -Run 'myScript.ps1' -SecureExecution -StorageAccountKey <String> -StorageAccountName 'Contoso' -TypeHandlerVersion '1.1' -VMName 'VirtualMachine07'
```

## <span data-ttu-id="dfe76-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dfe76-123">PARAMETERS</span></span>

### <span data-ttu-id="dfe76-124">-Argomento</span><span class="sxs-lookup"><span data-stu-id="dfe76-124">-Argument</span></span>
<span data-ttu-id="dfe76-125">Specifica gli argomenti che l'estensione di script passa allo script.</span><span class="sxs-lookup"><span data-stu-id="dfe76-125">Specifies arguments that the script extension passes to the script.</span></span>

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

### <span data-ttu-id="dfe76-126">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="dfe76-126">-ContainerName</span></span>
<span data-ttu-id="dfe76-127">Specifica il nome del contenitore di archiviazione di Azure in cui questo cmdlet archivia lo script.</span><span class="sxs-lookup"><span data-stu-id="dfe76-127">Specifies the name of the Azure storage container where this cmdlet stores the script.</span></span>

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

### <span data-ttu-id="dfe76-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfe76-128">-DefaultProfile</span></span>
<span data-ttu-id="dfe76-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dfe76-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfe76-130">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="dfe76-130">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="dfe76-131">-Nomefile</span><span class="sxs-lookup"><span data-stu-id="dfe76-131">-FileName</span></span>
<span data-ttu-id="dfe76-132">Specifica il nome del file di script.</span><span class="sxs-lookup"><span data-stu-id="dfe76-132">Specifies the name of the script file.</span></span> <span data-ttu-id="dfe76-133">Se il file è archiviato in archiviazione BLOB di Azure, il valore del nome del file è distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="dfe76-133">If the file is stored in Azure Blob storage, the file name value is case-sensitive.</span></span> <span data-ttu-id="dfe76-134">I nomi di file dei file archiviati nell'archiviazione di file di Azure non fanno distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="dfe76-134">File names of files stored in Azure File storage are not case-sensitive.</span></span>

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

### <span data-ttu-id="dfe76-135">-FileUri</span><span class="sxs-lookup"><span data-stu-id="dfe76-135">-FileUri</span></span>
<span data-ttu-id="dfe76-136">Specifica l'URI del file di script.</span><span class="sxs-lookup"><span data-stu-id="dfe76-136">Specifies the URI of the script file.</span></span>

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

### <span data-ttu-id="dfe76-137">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="dfe76-137">-ForceRerun</span></span>
<span data-ttu-id="dfe76-138">Indica che questo cmdlet impone la ripetizione della stessa configurazione di estensione nella macchina virtuale senza disinstallare e reinstallare l'estensione.</span><span class="sxs-lookup"><span data-stu-id="dfe76-138">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="dfe76-139">Il valore può essere qualsiasi stringa diversa dal valore corrente.</span><span class="sxs-lookup"><span data-stu-id="dfe76-139">The value can be any string different from the current value.</span></span>
<span data-ttu-id="dfe76-140">Se forceUpdateTag non viene modificato, le modifiche apportate alle impostazioni pubbliche o protette verranno ancora applicate dal gestore.</span><span class="sxs-lookup"><span data-stu-id="dfe76-140">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="dfe76-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dfe76-141">-InputObject</span></span>
<span data-ttu-id="dfe76-142">Oggetto estensione VM.</span><span class="sxs-lookup"><span data-stu-id="dfe76-142">VM extension object.</span></span>

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

### <span data-ttu-id="dfe76-143">-Posizione</span><span class="sxs-lookup"><span data-stu-id="dfe76-143">-Location</span></span>
<span data-ttu-id="dfe76-144">Specifica la posizione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dfe76-144">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="dfe76-145">-Nome</span><span class="sxs-lookup"><span data-stu-id="dfe76-145">-Name</span></span>
<span data-ttu-id="dfe76-146">Specifica il nome dell'estensione di script personalizzata.</span><span class="sxs-lookup"><span data-stu-id="dfe76-146">Specifies the name of the custom script extension.</span></span>

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

### <span data-ttu-id="dfe76-147">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="dfe76-147">-NoWait</span></span>
<span data-ttu-id="dfe76-148">Avvia l'operazione e restituisce immediatamente, prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="dfe76-148">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="dfe76-149">Per determinare se l'operazione è stata completata correttamente, usare un altro meccanismo.</span><span class="sxs-lookup"><span data-stu-id="dfe76-149">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="dfe76-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfe76-150">-ResourceGroupName</span></span>
<span data-ttu-id="dfe76-151">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dfe76-151">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="dfe76-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dfe76-152">-ResourceId</span></span>
<span data-ttu-id="dfe76-153">Estensione della VM ResourceID.</span><span class="sxs-lookup"><span data-stu-id="dfe76-153">VM extension ResourceID.</span></span>

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

### <span data-ttu-id="dfe76-154">-Run</span><span class="sxs-lookup"><span data-stu-id="dfe76-154">-Run</span></span>
<span data-ttu-id="dfe76-155">Specifica il comando da usare per eseguire lo script.</span><span class="sxs-lookup"><span data-stu-id="dfe76-155">Specifies the command to use that runs your script.</span></span>

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

### <span data-ttu-id="dfe76-156">-SecureExecution</span><span class="sxs-lookup"><span data-stu-id="dfe76-156">-SecureExecution</span></span>
<span data-ttu-id="dfe76-157">Indica che questo cmdlet assicura che il valore del parametro *Run* non sia connesso al server o venga restituito all'utente usando l'API di estensione Get.</span><span class="sxs-lookup"><span data-stu-id="dfe76-157">Indicates that this cmdlet makes sure that the value of the *Run* parameter is not logged on the server or returned to the user by using the GET extension API.</span></span>
<span data-ttu-id="dfe76-158">Il valore di *Run* può contenere segreti o password da passare al file di script in modo sicuro.</span><span class="sxs-lookup"><span data-stu-id="dfe76-158">The value of *Run* might contain secrets or passwords to be passed to the script file securely.</span></span>

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

### <span data-ttu-id="dfe76-159">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="dfe76-159">-StorageAccountKey</span></span>
<span data-ttu-id="dfe76-160">Specifica la chiave per il contenitore di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="dfe76-160">Specifies the key for the Azure storage container.</span></span>

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

### <span data-ttu-id="dfe76-161">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="dfe76-161">-StorageAccountName</span></span>
<span data-ttu-id="dfe76-162">Specifica il nome dell'account di archiviazione di Azure in cui questo cmdlet archivia lo script.</span><span class="sxs-lookup"><span data-stu-id="dfe76-162">Specifies the name of the Azure storage account where this cmdlet stores the script.</span></span>

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

### <span data-ttu-id="dfe76-163">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="dfe76-163">-StorageEndpointSuffix</span></span>
<span data-ttu-id="dfe76-164">Specifica il suffisso dell'endpoint di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="dfe76-164">Specifies the storage endpoint suffix.</span></span>

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

### <span data-ttu-id="dfe76-165">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="dfe76-165">-TypeHandlerVersion</span></span>
<span data-ttu-id="dfe76-166">Specifica la versione dell'estensione da usare per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dfe76-166">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="dfe76-167">Per ottenere la versione, eseguire il cmdlet Get-AzVMExtensionImage con il valore Microsoft. COMPUTE per il parametro *PublisherName* e CustomScriptExtension per il parametro *Type* .</span><span class="sxs-lookup"><span data-stu-id="dfe76-167">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and CustomScriptExtension for the *Type* parameter.</span></span>

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

### <span data-ttu-id="dfe76-168">-VMName</span><span class="sxs-lookup"><span data-stu-id="dfe76-168">-VMName</span></span>
<span data-ttu-id="dfe76-169">Specifica il nome di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dfe76-169">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="dfe76-170">Questo cmdlet aggiunge l'estensione di script personalizzata per la macchina virtuale specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="dfe76-170">This cmdlet adds the custom script extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="dfe76-171">-VMObject</span><span class="sxs-lookup"><span data-stu-id="dfe76-171">-VMObject</span></span>
<span data-ttu-id="dfe76-172">Oggetto VM.</span><span class="sxs-lookup"><span data-stu-id="dfe76-172">VM object.</span></span>

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

### <span data-ttu-id="dfe76-173">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dfe76-173">-Confirm</span></span>
<span data-ttu-id="dfe76-174">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfe76-174">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfe76-175">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfe76-175">-WhatIf</span></span>
<span data-ttu-id="dfe76-176">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dfe76-176">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfe76-177">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dfe76-177">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfe76-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfe76-178">CommonParameters</span></span>
<span data-ttu-id="dfe76-179">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfe76-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfe76-180">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dfe76-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfe76-181">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dfe76-181">INPUTS</span></span>

### <span data-ttu-id="dfe76-182">System. String</span><span class="sxs-lookup"><span data-stu-id="dfe76-182">System.String</span></span>

### <span data-ttu-id="dfe76-183">System. String []</span><span class="sxs-lookup"><span data-stu-id="dfe76-183">System.String[]</span></span>

### <span data-ttu-id="dfe76-184">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="dfe76-184">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="dfe76-185">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dfe76-185">OUTPUTS</span></span>

### <span data-ttu-id="dfe76-186">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="dfe76-186">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="dfe76-187">Note</span><span class="sxs-lookup"><span data-stu-id="dfe76-187">NOTES</span></span>

## <span data-ttu-id="dfe76-188">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dfe76-188">RELATED LINKS</span></span>

[<span data-ttu-id="dfe76-189">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="dfe76-189">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="dfe76-190">Remove-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="dfe76-190">Remove-AzVMCustomScriptExtension</span></span>](./Remove-AzVMCustomScriptExtension.md)


