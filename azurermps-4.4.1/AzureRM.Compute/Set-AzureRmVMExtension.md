---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 064196C3-ABF3-4F3A-A4AB-EB0D27098C70
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMExtension.md
ms.openlocfilehash: da46aa0e6518c9a9eb9ebea58962f3da593ad264
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516264"
---
# <span data-ttu-id="f9a2c-101">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="f9a2c-101">Set-AzureRmVMExtension</span></span>

## <span data-ttu-id="f9a2c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f9a2c-102">SYNOPSIS</span></span>
<span data-ttu-id="f9a2c-103">Aggiorna le proprietà delle estensioni o aggiunge un'estensione a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-103">Updates extension properties or adds an extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9a2c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f9a2c-104">SYNTAX</span></span>

### <span data-ttu-id="f9a2c-105">Impostazioni (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f9a2c-105">Settings (Default)</span></span>
```
Set-AzureRmVMExtension -Publisher <String> -ExtensionType <String> [-Settings <Hashtable>]
 [-ProtectedSettings <Hashtable>] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9a2c-106">SettingString</span><span class="sxs-lookup"><span data-stu-id="f9a2c-106">SettingString</span></span>
```
Set-AzureRmVMExtension -Publisher <String> -ExtensionType <String> [-SettingString <String>]
 [-ProtectedSettingString <String>] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9a2c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f9a2c-107">DESCRIPTION</span></span>
<span data-ttu-id="f9a2c-108">Il cmdlet **set-AzureRmVMExtension** aggiorna le proprietà per le estensioni esistenti della macchina virtuale o aggiunge un'estensione a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-108">The **Set-AzureRmVMExtension** cmdlet updates properties for existing Virtual Machine Extensions or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="f9a2c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f9a2c-109">EXAMPLES</span></span>

### <span data-ttu-id="f9a2c-110">Esempio 1: modificare le impostazioni usando le tabelle hash</span><span class="sxs-lookup"><span data-stu-id="f9a2c-110">Example 1: Modify settings by using hash tables</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};
PS C:\> Set-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "ContosoTest" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -Settings $Settings -ProtectedSettings $ProtectedSettings;
```

<span data-ttu-id="f9a2c-111">I primi due comandi usano la sintassi standard di Windows PowerShell per creare tabelle hash e quindi archivia le tabelle hash nelle variabili $Settings e $ProtectedSettings.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-111">The first two commands use standard Windows PowerShell syntax to create hash tables, and then stores those hash tables in the $Settings and $ProtectedSettings variables.</span></span>
<span data-ttu-id="f9a2c-112">Per altre informazioni, digitare `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="f9a2c-112">For more information, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="f9a2c-113">Il secondo comando include due valori creati in precedenza e archiviati in variabili.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-113">The second command includes two values previously created and stored in variables.</span></span>

<span data-ttu-id="f9a2c-114">Il comando finale modifica un'estensione della macchina virtuale denominata VirtualMachine22 in ResourceGroup11 in base al contenuto di $Settings e $ProtectedSettings.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-114">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $Settings and $ProtectedSettings.</span></span>
<span data-ttu-id="f9a2c-115">Il comando specifica altre informazioni necessarie che includono l'editore e il tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-115">The command specifies other required information that includes the publisher and the extension type.</span></span>

### <span data-ttu-id="f9a2c-116">Esempio 2: modificare le impostazioni usando le stringhe</span><span class="sxs-lookup"><span data-stu-id="f9a2c-116">Example 2: Modify settings by using strings</span></span>
```
PS C:\> $SettingsString = '{"fileUris":[],"commandToExecute":""}';
PS C:\> $ProtectedSettingsString = '{"storageAccountName":"' + $stoname + '","storageAccountKey":"' + $stokey + '"}';
PS C:\> Set-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -SettingString $SettingsString -ProtectedSettingString $ProtectedSettingsString ;
```

<span data-ttu-id="f9a2c-117">I primi due comandi creano stringhe che contengono impostazioni e le memorizzano nelle variabili $SettingsString e $ProtectedSettingsString.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-117">The first two commands create strings that contain settings, and then stores them in the $SettingsString and $ProtectedSettingsString variables.</span></span>

<span data-ttu-id="f9a2c-118">Il comando finale modifica un'estensione della macchina virtuale denominata VirtualMachine22 in ResourceGroup11 in base al contenuto di $SettingsString e $ProtectedSettingsString.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-118">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $SettingsString and $ProtectedSettingsString.</span></span>
<span data-ttu-id="f9a2c-119">Il comando specifica altre informazioni necessarie che includono l'editore e il tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-119">The command specifies other required information that includes the publisher and the extension type.</span></span>

## <span data-ttu-id="f9a2c-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f9a2c-120">PARAMETERS</span></span>

### <span data-ttu-id="f9a2c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9a2c-121">-DefaultProfile</span></span>
<span data-ttu-id="f9a2c-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9a2c-123">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="f9a2c-123">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="f9a2c-124">Indica che questo cmdlet impedisce all'agente guest Azure di aggiornare automaticamente le estensioni a una versione secondaria più recente.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-124">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extensions to a newer minor version.</span></span>
<span data-ttu-id="f9a2c-125">Per impostazione predefinita, questo cmdlet consente all'agente guest di aggiornare le estensioni.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-125">By default, this cmdlet enables the guest agent to update the extensions.</span></span>

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

### <span data-ttu-id="f9a2c-126">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="f9a2c-126">-ExtensionType</span></span>
<span data-ttu-id="f9a2c-127">Specifica il tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-127">Specifies the extension type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Type

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9a2c-128">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="f9a2c-128">-ForceRerun</span></span>
<span data-ttu-id="f9a2c-129">Indica che questo cmdlet impone la ripetizione della stessa configurazione di estensione nella macchina virtuale senza disinstallare e reinstallare l'estensione.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-129">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="f9a2c-130">Il valore può essere qualsiasi stringa diversa dal valore corrente.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-130">The value can be any string different from the current value.</span></span>

<span data-ttu-id="f9a2c-131">Se forceUpdateTag non viene modificato, le modifiche apportate alle impostazioni pubbliche o protette verranno ancora applicate dal gestore.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-131">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="f9a2c-132">-Posizione</span><span class="sxs-lookup"><span data-stu-id="f9a2c-132">-Location</span></span>
<span data-ttu-id="f9a2c-133">Specifica la posizione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-133">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="f9a2c-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="f9a2c-134">-Name</span></span>
<span data-ttu-id="f9a2c-135">Specifica il nome di un'estensione.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-135">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="f9a2c-136">-ProtectedSettings</span><span class="sxs-lookup"><span data-stu-id="f9a2c-136">-ProtectedSettings</span></span>
<span data-ttu-id="f9a2c-137">Specifica la configurazione privata per l'estensione, come tabella hash.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-137">Specifies private configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="f9a2c-138">Questo cmdlet crittografa la configurazione privata.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-138">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Settings
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9a2c-139">-ProtectedSettingString</span><span class="sxs-lookup"><span data-stu-id="f9a2c-139">-ProtectedSettingString</span></span>
<span data-ttu-id="f9a2c-140">Specifica la configurazione privata per l'estensione, come stringa.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-140">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="f9a2c-141">Questo cmdlet crittografa la configurazione privata.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-141">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SettingString
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9a2c-142">-Publisher</span><span class="sxs-lookup"><span data-stu-id="f9a2c-142">-Publisher</span></span>
<span data-ttu-id="f9a2c-143">Specifica il nome dell'autore dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-143">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="f9a2c-144">L'editore fornisce un nome quando l'editore registra un'estensione.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-144">The publisher provides a name when the publisher registers an extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9a2c-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9a2c-145">-ResourceGroupName</span></span>
<span data-ttu-id="f9a2c-146">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-146">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="f9a2c-147">-Impostazioni</span><span class="sxs-lookup"><span data-stu-id="f9a2c-147">-Settings</span></span>
<span data-ttu-id="f9a2c-148">Specifica la configurazione pubblica per l'estensione, come tabella hash.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-148">Specifies public configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="f9a2c-149">Questo cmdlet non crittografa la configurazione pubblica.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-149">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Settings
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9a2c-150">-SettingString</span><span class="sxs-lookup"><span data-stu-id="f9a2c-150">-SettingString</span></span>
<span data-ttu-id="f9a2c-151">Specifica la configurazione pubblica per l'estensione, come stringa.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-151">Specifies public configuration for the extension, as a string.</span></span>
<span data-ttu-id="f9a2c-152">Questo cmdlet non crittografa la configurazione pubblica.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-152">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SettingString
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9a2c-153">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="f9a2c-153">-TypeHandlerVersion</span></span>
<span data-ttu-id="f9a2c-154">Specifica la versione dell'estensione da usare per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-154">Specifies the version of the extension to use for this virtual machine.</span></span>

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

### <span data-ttu-id="f9a2c-155">-VMName</span><span class="sxs-lookup"><span data-stu-id="f9a2c-155">-VMName</span></span>
<span data-ttu-id="f9a2c-156">Specifica il nome di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-156">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="f9a2c-157">Questo cmdlet modifica le estensioni per la macchina virtuale specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-157">This cmdlet modifies extensions for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="f9a2c-158">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f9a2c-158">-Confirm</span></span>
<span data-ttu-id="f9a2c-159">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9a2c-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9a2c-160">-WhatIf</span></span>
<span data-ttu-id="f9a2c-161">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-161">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="f9a2c-162">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9a2c-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9a2c-163">CommonParameters</span></span>
<span data-ttu-id="f9a2c-164">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9a2c-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9a2c-165">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9a2c-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9a2c-166">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f9a2c-166">INPUTS</span></span>

## <span data-ttu-id="f9a2c-167">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f9a2c-167">OUTPUTS</span></span>

## <span data-ttu-id="f9a2c-168">Note</span><span class="sxs-lookup"><span data-stu-id="f9a2c-168">NOTES</span></span>

## <span data-ttu-id="f9a2c-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f9a2c-169">RELATED LINKS</span></span>

[<span data-ttu-id="f9a2c-170">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="f9a2c-170">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="f9a2c-171">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="f9a2c-171">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)


