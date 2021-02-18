---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 064196C3-ABF3-4F3A-A4AB-EB0D27098C70
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMExtension.md
ms.openlocfilehash: dc19566a9baaee7aa70dc03e5d9effa22df8d758
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204730"
---
# <span data-ttu-id="df49d-101">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="df49d-101">Set-AzVMExtension</span></span>

## <span data-ttu-id="df49d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df49d-102">SYNOPSIS</span></span>
<span data-ttu-id="df49d-103">Aggiorna le proprietà dell'estensione o aggiunge un'estensione a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="df49d-103">Updates extension properties or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="df49d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="df49d-104">SYNTAX</span></span>

### <span data-ttu-id="df49d-105">Impostazioni (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="df49d-105">Settings (Default)</span></span>
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-Settings <Hashtable>]
 [-ProtectedSettings <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-EnableAutomaticUpgrade <Boolean>] [-ForceRerun <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df49d-106">SettingString</span><span class="sxs-lookup"><span data-stu-id="df49d-106">SettingString</span></span>
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-SettingString <String>]
 [-ProtectedSettingString <String>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-EnableAutomaticUpgrade <Boolean>] [-ForceRerun <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df49d-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="df49d-107">DESCRIPTION</span></span>
<span data-ttu-id="df49d-108">Il cmdlet **Set-AzVMExtension** aggiorna le proprietà per le estensioni delle macchine virtuali esistenti o aggiunge un'estensione a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="df49d-108">The **Set-AzVMExtension** cmdlet updates properties for existing Virtual Machine Extensions or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="df49d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="df49d-109">EXAMPLES</span></span>

### <span data-ttu-id="df49d-110">Esempio 1: Modificare le impostazioni usando tabelle hash</span><span class="sxs-lookup"><span data-stu-id="df49d-110">Example 1: Modify settings by using hash tables</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "ContosoTest" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -Settings $Settings -ProtectedSettings $ProtectedSettings;
```

<span data-ttu-id="df49d-111">I primi due comandi usano la sintassi Windows PowerShell per creare tabelle hash e quindi le archiviano nelle $Settings e nelle $ProtectedSettings variabili.</span><span class="sxs-lookup"><span data-stu-id="df49d-111">The first two commands use standard Windows PowerShell syntax to create hash tables, and then stores those hash tables in the $Settings and $ProtectedSettings variables.</span></span>
<span data-ttu-id="df49d-112">Per altre informazioni, digitare `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="df49d-112">For more information, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="df49d-113">Il secondo comando include due valori creati in precedenza e archiviati nelle variabili.</span><span class="sxs-lookup"><span data-stu-id="df49d-113">The second command includes two values previously created and stored in variables.</span></span>
<span data-ttu-id="df49d-114">Il comando finale modifica un'estensione della macchina virtuale denominata VirtualMachine22 in ResourceGroup11 in base al contenuto di $Settings e $ProtectedSettings.</span><span class="sxs-lookup"><span data-stu-id="df49d-114">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $Settings and $ProtectedSettings.</span></span>
<span data-ttu-id="df49d-115">Il comando specifica altre informazioni obbligatorie che includono l'autore e il tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="df49d-115">The command specifies other required information that includes the publisher and the extension type.</span></span>

### <span data-ttu-id="df49d-116">Esempio 2: Modificare le impostazioni usando stringhe</span><span class="sxs-lookup"><span data-stu-id="df49d-116">Example 2: Modify settings by using strings</span></span>
```
PS C:\> $SettingsString = '{"fileUris":[],"commandToExecute":""}';
PS C:\> $ProtectedSettingsString = '{"storageAccountName":"' + $stoname + '","storageAccountKey":"' + $stokey + '"}';
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -SettingString $SettingsString -ProtectedSettingString $ProtectedSettingsString ;
```

<span data-ttu-id="df49d-117">I primi due comandi creano stringhe contenenti impostazioni e quindi le archiviano nelle variabili $SettingsString e $ProtectedSettingsString variabili.</span><span class="sxs-lookup"><span data-stu-id="df49d-117">The first two commands create strings that contain settings, and then stores them in the $SettingsString and $ProtectedSettingsString variables.</span></span>
<span data-ttu-id="df49d-118">Il comando finale modifica un'estensione della macchina virtuale denominata VirtualMachine22 in ResourceGroup11 in base al contenuto di $SettingsString e $ProtectedSettingsString.</span><span class="sxs-lookup"><span data-stu-id="df49d-118">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $SettingsString and $ProtectedSettingsString.</span></span>
<span data-ttu-id="df49d-119">Il comando specifica altre informazioni obbligatorie che includono l'autore e il tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="df49d-119">The command specifies other required information that includes the publisher and the extension type.</span></span>

## <span data-ttu-id="df49d-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df49d-120">PARAMETERS</span></span>

### <span data-ttu-id="df49d-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="df49d-121">-AsJob</span></span>
<span data-ttu-id="df49d-122">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="df49d-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="df49d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df49d-123">-DefaultProfile</span></span>
<span data-ttu-id="df49d-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="df49d-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df49d-125">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="df49d-125">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="df49d-126">Indica che questo cmdlet impedisce all'agente guest di Azure di aggiornare automaticamente le estensioni a una versione secondaria più recente.</span><span class="sxs-lookup"><span data-stu-id="df49d-126">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extensions to a newer minor version.</span></span>
<span data-ttu-id="df49d-127">Per impostazione predefinita, questo cmdlet consente all'agente guest di aggiornare le estensioni.</span><span class="sxs-lookup"><span data-stu-id="df49d-127">By default, this cmdlet enables the guest agent to update the extensions.</span></span>

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

### <span data-ttu-id="df49d-128">-EnableAutomaticUpgrade</span><span class="sxs-lookup"><span data-stu-id="df49d-128">-EnableAutomaticUpgrade</span></span>
<span data-ttu-id="df49d-129">Indica se l'estensione deve essere aggiornata automaticamente dalla piattaforma se è disponibile una versione più recente dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="df49d-129">Indicates whether the extension should be automatically upgraded by the platform if there is a newer version of the extension available.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df49d-130">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="df49d-130">-ExtensionType</span></span>
<span data-ttu-id="df49d-131">Specifica il tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="df49d-131">Specifies the extension type.</span></span>

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

### <span data-ttu-id="df49d-132">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="df49d-132">-ForceRerun</span></span>
<span data-ttu-id="df49d-133">Indica che questo cmdlet forza una nuova esecuzione della stessa configurazione dell'estensione nella macchina virtuale senza disinstallare e reinstallare l'estensione.</span><span class="sxs-lookup"><span data-stu-id="df49d-133">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="df49d-134">Il valore può essere qualsiasi stringa diversa dal valore corrente.</span><span class="sxs-lookup"><span data-stu-id="df49d-134">The value can be any string different from the current value.</span></span>
<span data-ttu-id="df49d-135">Se forceUpdateTag non viene modificato, gli aggiornamenti alle impostazioni pubbliche o protette vengono comunque applicati dal gestore.</span><span class="sxs-lookup"><span data-stu-id="df49d-135">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="df49d-136">-Location</span><span class="sxs-lookup"><span data-stu-id="df49d-136">-Location</span></span>
<span data-ttu-id="df49d-137">Specifica la posizione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="df49d-137">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="df49d-138">-Name</span><span class="sxs-lookup"><span data-stu-id="df49d-138">-Name</span></span>
<span data-ttu-id="df49d-139">Specifica il nome di un'estensione.</span><span class="sxs-lookup"><span data-stu-id="df49d-139">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="df49d-140">-NoWait</span><span class="sxs-lookup"><span data-stu-id="df49d-140">-NoWait</span></span>
<span data-ttu-id="df49d-141">Avvia l'operazione e restituisce immediatamente, prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="df49d-141">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="df49d-142">Per determinare se l'operazione è stata completata correttamente, usare un altro meccanismo.</span><span class="sxs-lookup"><span data-stu-id="df49d-142">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="df49d-143">-ProtectedSettings</span><span class="sxs-lookup"><span data-stu-id="df49d-143">-ProtectedSettings</span></span>
<span data-ttu-id="df49d-144">Specifica la configurazione privata per l'estensione, come tabella hash.</span><span class="sxs-lookup"><span data-stu-id="df49d-144">Specifies private configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="df49d-145">Questo cmdlet crittografa la configurazione privata.</span><span class="sxs-lookup"><span data-stu-id="df49d-145">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="df49d-146">-ProtectedSettingString</span><span class="sxs-lookup"><span data-stu-id="df49d-146">-ProtectedSettingString</span></span>
<span data-ttu-id="df49d-147">Specifica la configurazione privata per l'estensione, come stringa.</span><span class="sxs-lookup"><span data-stu-id="df49d-147">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="df49d-148">Questo cmdlet crittografa la configurazione privata.</span><span class="sxs-lookup"><span data-stu-id="df49d-148">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="df49d-149">-Publisher</span><span class="sxs-lookup"><span data-stu-id="df49d-149">-Publisher</span></span>
<span data-ttu-id="df49d-150">Specifica il nome dell'autore dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="df49d-150">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="df49d-151">L'editore fornisce un nome quando l'editore registra un'estensione.</span><span class="sxs-lookup"><span data-stu-id="df49d-151">The publisher provides a name when the publisher registers an extension.</span></span>

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

### <span data-ttu-id="df49d-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df49d-152">-ResourceGroupName</span></span>
<span data-ttu-id="df49d-153">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="df49d-153">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="df49d-154">-Settings</span><span class="sxs-lookup"><span data-stu-id="df49d-154">-Settings</span></span>
<span data-ttu-id="df49d-155">Specifica la configurazione pubblica per l'estensione, come tabella hash.</span><span class="sxs-lookup"><span data-stu-id="df49d-155">Specifies public configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="df49d-156">Questo cmdlet non crittografa la configurazione pubblica.</span><span class="sxs-lookup"><span data-stu-id="df49d-156">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="df49d-157">-SettingString</span><span class="sxs-lookup"><span data-stu-id="df49d-157">-SettingString</span></span>
<span data-ttu-id="df49d-158">Specifica la configurazione pubblica per l'estensione, come stringa.</span><span class="sxs-lookup"><span data-stu-id="df49d-158">Specifies public configuration for the extension, as a string.</span></span>
<span data-ttu-id="df49d-159">Questo cmdlet non crittografa la configurazione pubblica.</span><span class="sxs-lookup"><span data-stu-id="df49d-159">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="df49d-160">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="df49d-160">-TypeHandlerVersion</span></span>
<span data-ttu-id="df49d-161">Specifica la versione dell'estensione da usare per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="df49d-161">Specifies the version of the extension to use for this virtual machine.</span></span>

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

### <span data-ttu-id="df49d-162">-VMName</span><span class="sxs-lookup"><span data-stu-id="df49d-162">-VMName</span></span>
<span data-ttu-id="df49d-163">Specifica il nome di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="df49d-163">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="df49d-164">Questo cmdlet modifica le estensioni per la macchina virtuale specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="df49d-164">This cmdlet modifies extensions for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="df49d-165">-Confirm</span><span class="sxs-lookup"><span data-stu-id="df49d-165">-Confirm</span></span>
<span data-ttu-id="df49d-166">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df49d-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df49d-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df49d-167">-WhatIf</span></span>
<span data-ttu-id="df49d-168">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="df49d-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df49d-169">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="df49d-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df49d-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df49d-170">CommonParameters</span></span>
<span data-ttu-id="df49d-171">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df49d-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df49d-172">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="df49d-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df49d-173">INPUT</span><span class="sxs-lookup"><span data-stu-id="df49d-173">INPUTS</span></span>

### <span data-ttu-id="df49d-174">System.String</span><span class="sxs-lookup"><span data-stu-id="df49d-174">System.String</span></span>

### <span data-ttu-id="df49d-175">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="df49d-175">System.Collections.Hashtable</span></span>

### <span data-ttu-id="df49d-176">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="df49d-176">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="df49d-177">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="df49d-177">OUTPUTS</span></span>

### <span data-ttu-id="df49d-178">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="df49d-178">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="df49d-179">NOTE</span><span class="sxs-lookup"><span data-stu-id="df49d-179">NOTES</span></span>

## <span data-ttu-id="df49d-180">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="df49d-180">RELATED LINKS</span></span>

[<span data-ttu-id="df49d-181">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="df49d-181">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="df49d-182">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="df49d-182">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)


