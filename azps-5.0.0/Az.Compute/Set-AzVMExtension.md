---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 064196C3-ABF3-4F3A-A4AB-EB0D27098C70
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMExtension.md
ms.openlocfilehash: babe273e97d2b1b9a1e09959ba252557e2a7e7d0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296503"
---
# <span data-ttu-id="ea322-101">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="ea322-101">Set-AzVMExtension</span></span>

## <span data-ttu-id="ea322-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ea322-102">SYNOPSIS</span></span>
<span data-ttu-id="ea322-103">Aggiorna le proprietà delle estensioni o aggiunge un'estensione a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ea322-103">Updates extension properties or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="ea322-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ea322-104">SYNTAX</span></span>

### <span data-ttu-id="ea322-105">Impostazioni (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ea322-105">Settings (Default)</span></span>
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-Settings <Hashtable>]
 [-ProtectedSettings <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea322-106">SettingString</span><span class="sxs-lookup"><span data-stu-id="ea322-106">SettingString</span></span>
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-SettingString <String>]
 [-ProtectedSettingString <String>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea322-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ea322-107">DESCRIPTION</span></span>
<span data-ttu-id="ea322-108">Il cmdlet **set-AzVMExtension** aggiorna le proprietà per le estensioni esistenti della macchina virtuale o aggiunge un'estensione a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ea322-108">The **Set-AzVMExtension** cmdlet updates properties for existing Virtual Machine Extensions or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="ea322-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ea322-109">EXAMPLES</span></span>

### <span data-ttu-id="ea322-110">Esempio 1: modificare le impostazioni usando le tabelle hash</span><span class="sxs-lookup"><span data-stu-id="ea322-110">Example 1: Modify settings by using hash tables</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "ContosoTest" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -Settings $Settings -ProtectedSettings $ProtectedSettings;
```

<span data-ttu-id="ea322-111">I primi due comandi usano la sintassi standard di Windows PowerShell per creare tabelle hash e quindi archivia le tabelle hash nelle variabili $Settings e $ProtectedSettings.</span><span class="sxs-lookup"><span data-stu-id="ea322-111">The first two commands use standard Windows PowerShell syntax to create hash tables, and then stores those hash tables in the $Settings and $ProtectedSettings variables.</span></span>
<span data-ttu-id="ea322-112">Per altre informazioni, digitare `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="ea322-112">For more information, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="ea322-113">Il secondo comando include due valori creati in precedenza e archiviati in variabili.</span><span class="sxs-lookup"><span data-stu-id="ea322-113">The second command includes two values previously created and stored in variables.</span></span>
<span data-ttu-id="ea322-114">Il comando finale modifica un'estensione della macchina virtuale denominata VirtualMachine22 in ResourceGroup11 in base al contenuto di $Settings e $ProtectedSettings.</span><span class="sxs-lookup"><span data-stu-id="ea322-114">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $Settings and $ProtectedSettings.</span></span>
<span data-ttu-id="ea322-115">Il comando specifica altre informazioni necessarie che includono l'editore e il tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="ea322-115">The command specifies other required information that includes the publisher and the extension type.</span></span>

### <span data-ttu-id="ea322-116">Esempio 2: modificare le impostazioni usando le stringhe</span><span class="sxs-lookup"><span data-stu-id="ea322-116">Example 2: Modify settings by using strings</span></span>
```
PS C:\> $SettingsString = '{"fileUris":[],"commandToExecute":""}';
PS C:\> $ProtectedSettingsString = '{"storageAccountName":"' + $stoname + '","storageAccountKey":"' + $stokey + '"}';
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -SettingString $SettingsString -ProtectedSettingString $ProtectedSettingsString ;
```

<span data-ttu-id="ea322-117">I primi due comandi creano stringhe che contengono impostazioni e le memorizzano nelle variabili $SettingsString e $ProtectedSettingsString.</span><span class="sxs-lookup"><span data-stu-id="ea322-117">The first two commands create strings that contain settings, and then stores them in the $SettingsString and $ProtectedSettingsString variables.</span></span>
<span data-ttu-id="ea322-118">Il comando finale modifica un'estensione della macchina virtuale denominata VirtualMachine22 in ResourceGroup11 in base al contenuto di $SettingsString e $ProtectedSettingsString.</span><span class="sxs-lookup"><span data-stu-id="ea322-118">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $SettingsString and $ProtectedSettingsString.</span></span>
<span data-ttu-id="ea322-119">Il comando specifica altre informazioni necessarie che includono l'editore e il tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="ea322-119">The command specifies other required information that includes the publisher and the extension type.</span></span>

## <span data-ttu-id="ea322-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ea322-120">PARAMETERS</span></span>

### <span data-ttu-id="ea322-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ea322-121">-AsJob</span></span>
<span data-ttu-id="ea322-122">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ea322-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ea322-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea322-123">-DefaultProfile</span></span>
<span data-ttu-id="ea322-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ea322-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea322-125">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="ea322-125">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="ea322-126">Indica che questo cmdlet impedisce all'agente guest Azure di aggiornare automaticamente le estensioni a una versione secondaria più recente.</span><span class="sxs-lookup"><span data-stu-id="ea322-126">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extensions to a newer minor version.</span></span>
<span data-ttu-id="ea322-127">Per impostazione predefinita, questo cmdlet consente all'agente guest di aggiornare le estensioni.</span><span class="sxs-lookup"><span data-stu-id="ea322-127">By default, this cmdlet enables the guest agent to update the extensions.</span></span>

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

### <span data-ttu-id="ea322-128">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="ea322-128">-ExtensionType</span></span>
<span data-ttu-id="ea322-129">Specifica il tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="ea322-129">Specifies the extension type.</span></span>

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

### <span data-ttu-id="ea322-130">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="ea322-130">-ForceRerun</span></span>
<span data-ttu-id="ea322-131">Indica che questo cmdlet impone la ripetizione della stessa configurazione di estensione nella macchina virtuale senza disinstallare e reinstallare l'estensione.</span><span class="sxs-lookup"><span data-stu-id="ea322-131">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="ea322-132">Il valore può essere qualsiasi stringa diversa dal valore corrente.</span><span class="sxs-lookup"><span data-stu-id="ea322-132">The value can be any string different from the current value.</span></span>
<span data-ttu-id="ea322-133">Se forceUpdateTag non viene modificato, le modifiche apportate alle impostazioni pubbliche o protette verranno ancora applicate dal gestore.</span><span class="sxs-lookup"><span data-stu-id="ea322-133">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="ea322-134">-Posizione</span><span class="sxs-lookup"><span data-stu-id="ea322-134">-Location</span></span>
<span data-ttu-id="ea322-135">Specifica la posizione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ea322-135">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="ea322-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="ea322-136">-Name</span></span>
<span data-ttu-id="ea322-137">Specifica il nome di un'estensione.</span><span class="sxs-lookup"><span data-stu-id="ea322-137">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="ea322-138">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="ea322-138">-NoWait</span></span>
<span data-ttu-id="ea322-139">Avvia l'operazione e restituisce immediatamente, prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="ea322-139">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="ea322-140">Per determinare se l'operazione è stata completata correttamente, usare un altro meccanismo.</span><span class="sxs-lookup"><span data-stu-id="ea322-140">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="ea322-141">-ProtectedSettings</span><span class="sxs-lookup"><span data-stu-id="ea322-141">-ProtectedSettings</span></span>
<span data-ttu-id="ea322-142">Specifica la configurazione privata per l'estensione, come tabella hash.</span><span class="sxs-lookup"><span data-stu-id="ea322-142">Specifies private configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="ea322-143">Questo cmdlet crittografa la configurazione privata.</span><span class="sxs-lookup"><span data-stu-id="ea322-143">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="ea322-144">-ProtectedSettingString</span><span class="sxs-lookup"><span data-stu-id="ea322-144">-ProtectedSettingString</span></span>
<span data-ttu-id="ea322-145">Specifica la configurazione privata per l'estensione, come stringa.</span><span class="sxs-lookup"><span data-stu-id="ea322-145">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="ea322-146">Questo cmdlet crittografa la configurazione privata.</span><span class="sxs-lookup"><span data-stu-id="ea322-146">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="ea322-147">-Publisher</span><span class="sxs-lookup"><span data-stu-id="ea322-147">-Publisher</span></span>
<span data-ttu-id="ea322-148">Specifica il nome dell'autore dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="ea322-148">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="ea322-149">L'editore fornisce un nome quando l'editore registra un'estensione.</span><span class="sxs-lookup"><span data-stu-id="ea322-149">The publisher provides a name when the publisher registers an extension.</span></span>

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

### <span data-ttu-id="ea322-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea322-150">-ResourceGroupName</span></span>
<span data-ttu-id="ea322-151">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ea322-151">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="ea322-152">-Impostazioni</span><span class="sxs-lookup"><span data-stu-id="ea322-152">-Settings</span></span>
<span data-ttu-id="ea322-153">Specifica la configurazione pubblica per l'estensione, come tabella hash.</span><span class="sxs-lookup"><span data-stu-id="ea322-153">Specifies public configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="ea322-154">Questo cmdlet non crittografa la configurazione pubblica.</span><span class="sxs-lookup"><span data-stu-id="ea322-154">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="ea322-155">-SettingString</span><span class="sxs-lookup"><span data-stu-id="ea322-155">-SettingString</span></span>
<span data-ttu-id="ea322-156">Specifica la configurazione pubblica per l'estensione, come stringa.</span><span class="sxs-lookup"><span data-stu-id="ea322-156">Specifies public configuration for the extension, as a string.</span></span>
<span data-ttu-id="ea322-157">Questo cmdlet non crittografa la configurazione pubblica.</span><span class="sxs-lookup"><span data-stu-id="ea322-157">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="ea322-158">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="ea322-158">-TypeHandlerVersion</span></span>
<span data-ttu-id="ea322-159">Specifica la versione dell'estensione da usare per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ea322-159">Specifies the version of the extension to use for this virtual machine.</span></span>

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

### <span data-ttu-id="ea322-160">-VMName</span><span class="sxs-lookup"><span data-stu-id="ea322-160">-VMName</span></span>
<span data-ttu-id="ea322-161">Specifica il nome di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ea322-161">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="ea322-162">Questo cmdlet modifica le estensioni per la macchina virtuale specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="ea322-162">This cmdlet modifies extensions for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="ea322-163">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ea322-163">-Confirm</span></span>
<span data-ttu-id="ea322-164">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea322-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea322-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea322-165">-WhatIf</span></span>
<span data-ttu-id="ea322-166">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ea322-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea322-167">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ea322-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea322-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea322-168">CommonParameters</span></span>
<span data-ttu-id="ea322-169">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea322-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea322-170">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea322-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea322-171">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ea322-171">INPUTS</span></span>

### <span data-ttu-id="ea322-172">System. String</span><span class="sxs-lookup"><span data-stu-id="ea322-172">System.String</span></span>

### <span data-ttu-id="ea322-173">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ea322-173">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ea322-174">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ea322-174">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ea322-175">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ea322-175">OUTPUTS</span></span>

### <span data-ttu-id="ea322-176">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ea322-176">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="ea322-177">Note</span><span class="sxs-lookup"><span data-stu-id="ea322-177">NOTES</span></span>

## <span data-ttu-id="ea322-178">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ea322-178">RELATED LINKS</span></span>

[<span data-ttu-id="ea322-179">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="ea322-179">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="ea322-180">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="ea322-180">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)


