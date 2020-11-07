---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 064196C3-ABF3-4F3A-A4AB-EB0D27098C70
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMExtension.md
ms.openlocfilehash: 1f758f77fc7162f8110f0e2d5887eadb55d7f7c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685492"
---
# <span data-ttu-id="47c00-101">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="47c00-101">Set-AzureRmVMExtension</span></span>

## <span data-ttu-id="47c00-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="47c00-102">SYNOPSIS</span></span>
<span data-ttu-id="47c00-103">Aggiorna le proprietà delle estensioni o aggiunge un'estensione a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="47c00-103">Updates extension properties or adds an extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47c00-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="47c00-104">SYNTAX</span></span>

### <span data-ttu-id="47c00-105">Impostazioni (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="47c00-105">Settings (Default)</span></span>
```
Set-AzureRmVMExtension -Publisher <String> -ExtensionType <String> [-Settings <Hashtable>]
 [-ProtectedSettings <Hashtable>] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47c00-106">SettingString</span><span class="sxs-lookup"><span data-stu-id="47c00-106">SettingString</span></span>
```
Set-AzureRmVMExtension -Publisher <String> -ExtensionType <String> [-SettingString <String>]
 [-ProtectedSettingString <String>] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47c00-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="47c00-107">DESCRIPTION</span></span>
<span data-ttu-id="47c00-108">Il cmdlet **set-AzureRmVMExtension** aggiorna le proprietà per le estensioni esistenti della macchina virtuale o aggiunge un'estensione a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="47c00-108">The **Set-AzureRmVMExtension** cmdlet updates properties for existing Virtual Machine Extensions or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="47c00-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="47c00-109">EXAMPLES</span></span>

### <span data-ttu-id="47c00-110">Esempio 1: modificare le impostazioni usando le tabelle hash</span><span class="sxs-lookup"><span data-stu-id="47c00-110">Example 1: Modify settings by using hash tables</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};
PS C:\> Set-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "ContosoTest" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -Settings $Settings -ProtectedSettings $ProtectedSettings;
```

<span data-ttu-id="47c00-111">I primi due comandi usano la sintassi standard di Windows PowerShell per creare tabelle hash e quindi archivia le tabelle hash nelle variabili $Settings e $ProtectedSettings.</span><span class="sxs-lookup"><span data-stu-id="47c00-111">The first two commands use standard Windows PowerShell syntax to create hash tables, and then stores those hash tables in the $Settings and $ProtectedSettings variables.</span></span>
<span data-ttu-id="47c00-112">Per altre informazioni, digitare `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="47c00-112">For more information, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="47c00-113">Il secondo comando include due valori creati in precedenza e archiviati in variabili.</span><span class="sxs-lookup"><span data-stu-id="47c00-113">The second command includes two values previously created and stored in variables.</span></span>

<span data-ttu-id="47c00-114">Il comando finale modifica un'estensione della macchina virtuale denominata VirtualMachine22 in ResourceGroup11 in base al contenuto di $Settings e $ProtectedSettings.</span><span class="sxs-lookup"><span data-stu-id="47c00-114">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $Settings and $ProtectedSettings.</span></span>
<span data-ttu-id="47c00-115">Il comando specifica altre informazioni necessarie che includono l'editore e il tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="47c00-115">The command specifies other required information that includes the publisher and the extension type.</span></span>

### <span data-ttu-id="47c00-116">Esempio 2: modificare le impostazioni usando le stringhe</span><span class="sxs-lookup"><span data-stu-id="47c00-116">Example 2: Modify settings by using strings</span></span>
```
PS C:\> $SettingsString = '{"fileUris":[],"commandToExecute":""}';
PS C:\> $ProtectedSettingsString = '{"storageAccountName":"' + $stoname + '","storageAccountKey":"' + $stokey + '"}';
PS C:\> Set-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -SettingString $SettingsString -ProtectedSettingString $ProtectedSettingsString ;
```

<span data-ttu-id="47c00-117">I primi due comandi creano stringhe che contengono impostazioni e le memorizzano nelle variabili $SettingsString e $ProtectedSettingsString.</span><span class="sxs-lookup"><span data-stu-id="47c00-117">The first two commands create strings that contain settings, and then stores them in the $SettingsString and $ProtectedSettingsString variables.</span></span>

<span data-ttu-id="47c00-118">Il comando finale modifica un'estensione della macchina virtuale denominata VirtualMachine22 in ResourceGroup11 in base al contenuto di $SettingsString e $ProtectedSettingsString.</span><span class="sxs-lookup"><span data-stu-id="47c00-118">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $SettingsString and $ProtectedSettingsString.</span></span>
<span data-ttu-id="47c00-119">Il comando specifica altre informazioni necessarie che includono l'editore e il tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="47c00-119">The command specifies other required information that includes the publisher and the extension type.</span></span>

## <span data-ttu-id="47c00-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="47c00-120">PARAMETERS</span></span>

### <span data-ttu-id="47c00-121">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="47c00-121">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="47c00-122">Indica che questo cmdlet impedisce all'agente guest Azure di aggiornare automaticamente le estensioni a una versione secondaria più recente.</span><span class="sxs-lookup"><span data-stu-id="47c00-122">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extensions to a newer minor version.</span></span>
<span data-ttu-id="47c00-123">Per impostazione predefinita, questo cmdlet consente all'agente guest di aggiornare le estensioni.</span><span class="sxs-lookup"><span data-stu-id="47c00-123">By default, this cmdlet enables the guest agent to update the extensions.</span></span>

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

### <span data-ttu-id="47c00-124">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="47c00-124">-ExtensionType</span></span>
<span data-ttu-id="47c00-125">Specifica il tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="47c00-125">Specifies the extension type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Type

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47c00-126">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="47c00-126">-ForceRerun</span></span>
<span data-ttu-id="47c00-127">Indica che questo cmdlet impone la ripetizione della stessa configurazione di estensione nella macchina virtuale senza disinstallare e reinstallare l'estensione.</span><span class="sxs-lookup"><span data-stu-id="47c00-127">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="47c00-128">Il valore può essere qualsiasi stringa diversa dal valore corrente.</span><span class="sxs-lookup"><span data-stu-id="47c00-128">The value can be any string different from the current value.</span></span>

<span data-ttu-id="47c00-129">Se forceUpdateTag non viene modificato, le modifiche apportate alle impostazioni pubbliche o protette verranno ancora applicate dal gestore.</span><span class="sxs-lookup"><span data-stu-id="47c00-129">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="47c00-130">-Posizione</span><span class="sxs-lookup"><span data-stu-id="47c00-130">-Location</span></span>
<span data-ttu-id="47c00-131">Specifica la posizione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="47c00-131">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="47c00-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="47c00-132">-Name</span></span>
<span data-ttu-id="47c00-133">Specifica il nome di un'estensione.</span><span class="sxs-lookup"><span data-stu-id="47c00-133">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="47c00-134">-ProtectedSettings</span><span class="sxs-lookup"><span data-stu-id="47c00-134">-ProtectedSettings</span></span>
<span data-ttu-id="47c00-135">Specifica la configurazione privata per l'estensione, come tabella hash.</span><span class="sxs-lookup"><span data-stu-id="47c00-135">Specifies private configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="47c00-136">Questo cmdlet crittografa la configurazione privata.</span><span class="sxs-lookup"><span data-stu-id="47c00-136">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: Hashtable
Parameter Sets: Settings
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47c00-137">-ProtectedSettingString</span><span class="sxs-lookup"><span data-stu-id="47c00-137">-ProtectedSettingString</span></span>
<span data-ttu-id="47c00-138">Specifica la configurazione privata per l'estensione, come stringa.</span><span class="sxs-lookup"><span data-stu-id="47c00-138">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="47c00-139">Questo cmdlet crittografa la configurazione privata.</span><span class="sxs-lookup"><span data-stu-id="47c00-139">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: String
Parameter Sets: SettingString
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47c00-140">-Publisher</span><span class="sxs-lookup"><span data-stu-id="47c00-140">-Publisher</span></span>
<span data-ttu-id="47c00-141">Specifica il nome dell'autore dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="47c00-141">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="47c00-142">L'editore fornisce un nome quando l'editore registra un'estensione.</span><span class="sxs-lookup"><span data-stu-id="47c00-142">The publisher provides a name when the publisher registers an extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47c00-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47c00-143">-ResourceGroupName</span></span>
<span data-ttu-id="47c00-144">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="47c00-144">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="47c00-145">-Impostazioni</span><span class="sxs-lookup"><span data-stu-id="47c00-145">-Settings</span></span>
<span data-ttu-id="47c00-146">Specifica la configurazione pubblica per l'estensione, come tabella hash.</span><span class="sxs-lookup"><span data-stu-id="47c00-146">Specifies public configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="47c00-147">Questo cmdlet non crittografa la configurazione pubblica.</span><span class="sxs-lookup"><span data-stu-id="47c00-147">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: Hashtable
Parameter Sets: Settings
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47c00-148">-SettingString</span><span class="sxs-lookup"><span data-stu-id="47c00-148">-SettingString</span></span>
<span data-ttu-id="47c00-149">Specifica la configurazione pubblica per l'estensione, come stringa.</span><span class="sxs-lookup"><span data-stu-id="47c00-149">Specifies public configuration for the extension, as a string.</span></span>
<span data-ttu-id="47c00-150">Questo cmdlet non crittografa la configurazione pubblica.</span><span class="sxs-lookup"><span data-stu-id="47c00-150">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: String
Parameter Sets: SettingString
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47c00-151">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="47c00-151">-TypeHandlerVersion</span></span>
<span data-ttu-id="47c00-152">Specifica la versione dell'estensione da usare per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="47c00-152">Specifies the version of the extension to use for this virtual machine.</span></span>

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

### <span data-ttu-id="47c00-153">-VMName</span><span class="sxs-lookup"><span data-stu-id="47c00-153">-VMName</span></span>
<span data-ttu-id="47c00-154">Specifica il nome di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="47c00-154">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="47c00-155">Questo cmdlet modifica le estensioni per la macchina virtuale specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="47c00-155">This cmdlet modifies extensions for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="47c00-156">-Confermare</span><span class="sxs-lookup"><span data-stu-id="47c00-156">-Confirm</span></span>
<span data-ttu-id="47c00-157">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47c00-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47c00-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47c00-158">-WhatIf</span></span>
<span data-ttu-id="47c00-159">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="47c00-159">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="47c00-160">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="47c00-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47c00-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47c00-161">CommonParameters</span></span>
<span data-ttu-id="47c00-162">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47c00-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47c00-163">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47c00-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47c00-164">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="47c00-164">INPUTS</span></span>

### <span data-ttu-id="47c00-165">Nessuno</span><span class="sxs-lookup"><span data-stu-id="47c00-165">None</span></span>
<span data-ttu-id="47c00-166">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="47c00-166">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="47c00-167">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="47c00-167">OUTPUTS</span></span>

## <span data-ttu-id="47c00-168">Note</span><span class="sxs-lookup"><span data-stu-id="47c00-168">NOTES</span></span>

## <span data-ttu-id="47c00-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="47c00-169">RELATED LINKS</span></span>

[<span data-ttu-id="47c00-170">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="47c00-170">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="47c00-171">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="47c00-171">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)


