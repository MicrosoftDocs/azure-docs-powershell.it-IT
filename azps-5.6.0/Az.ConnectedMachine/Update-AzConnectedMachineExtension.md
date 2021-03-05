---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/powershell/module/az.connectedmachine/update-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Update-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Update-AzConnectedMachineExtension.md
ms.openlocfilehash: e6da084f13d85f8c4f5a8934cd5fd4f05882c251
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012318"
---
# <span data-ttu-id="72b65-101">Update-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="72b65-101">Update-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="72b65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72b65-102">SYNOPSIS</span></span>
<span data-ttu-id="72b65-103">Operazione per creare o aggiornare l'estensione.</span><span class="sxs-lookup"><span data-stu-id="72b65-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="72b65-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="72b65-104">SYNTAX</span></span>

### <span data-ttu-id="72b65-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="72b65-105">UpdateExpanded (Default)</span></span>
```
Update-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>] [-Publisher <String>]
 [-Setting <IMachineExtensionUpdatePropertiesSettings>] [-Tag <Hashtable>] [-Type <String>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="72b65-106">Aggiorna</span><span class="sxs-lookup"><span data-stu-id="72b65-106">Update</span></span>
```
Update-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtensionUpdate> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="72b65-107">UpdateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="72b65-107">UpdateViaIdentity</span></span>
```
Update-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity>
 -ExtensionParameter <IMachineExtensionUpdate> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="72b65-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="72b65-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> [-AutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionUpdatePropertiesSettings>] [-Tag <Hashtable>]
 [-Type <String>] [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="72b65-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="72b65-109">DESCRIPTION</span></span>
<span data-ttu-id="72b65-110">Operazione per creare o aggiornare l'estensione.</span><span class="sxs-lookup"><span data-stu-id="72b65-110">The operation to create or update the extension.</span></span>

## <span data-ttu-id="72b65-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="72b65-111">EXAMPLES</span></span>

### <span data-ttu-id="72b65-112">Esempio 1: Aggiornare un'estensione</span><span class="sxs-lookup"><span data-stu-id="72b65-112">Example 1: Update an extension</span></span>
```powershell
PS C:\> $splat = @{
            ResourceGroupName = "connectedMachines"
            MachineName = "linux-eastus1_1"
            Name = "customScript"
            Settings = @{
                commandToExecute = "ls -l"
            }
        }
PS C:\> Update-AzConnectedMachineExtension @splat

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="72b65-113">Aggiorna un'estensione in un computer specifico.</span><span class="sxs-lookup"><span data-stu-id="72b65-113">Updates an extension on a specific machine.</span></span>

### <span data-ttu-id="72b65-114">Esempio 2: Aggiornare un'estensione con la posizione specificata tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="72b65-114">Example 2: Update an extension with location specified via the pipeline</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension -Settings @{
                commandToExecute = "ls -l"
            }

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="72b65-115">Aggiorna una specifica estensione passata tramite la pipeline.</span><span class="sxs-lookup"><span data-stu-id="72b65-115">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="72b65-116">Qui viene in uso l'estensione passata tramite la pipeline per aiutare Microsoft a identificare l'estensione su cui si vuole operare e a specificare cosa si vuole modificare con i parametri normali ( ad esempio `-Settings` )</span><span class="sxs-lookup"><span data-stu-id="72b65-116">Here we are using the extension passed in via the pipeline to help us identify which extension we want to operate on and are specifying what we want to change via the normal parameters (like `-Settings`)</span></span>

### <span data-ttu-id="72b65-117">Esempio 3: Aggiornare un'estensione con i parametri di estensione specificati tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="72b65-117">Example 3: Update an extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> # Update the settings on the object that will be used via the pipeline
PS C:\> $extToUpdate.Setting.commandToExecute = "ls -l"
PS C:\> $splat = @{
            ResourceGroupName = "connectedMachines"
            MachineName = "linux-eastus1_1"
            Name = "customScript"
        }
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension @splat

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="72b65-118">Aggiorna una specifica estensione passata tramite la pipeline.</span><span class="sxs-lookup"><span data-stu-id="72b65-118">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="72b65-119">Qui stiamo usando l'estensione passata tramite la pipeline per fornire le modifiche da apportare all'estensione.</span><span class="sxs-lookup"><span data-stu-id="72b65-119">Here we are using the extension passed in via the pipeline to provide the changes we want to make on the extension.</span></span>
<span data-ttu-id="72b65-120">La posizione dell'estensione non viene recuperata tramite la pipeline, ma tramite i parametri specificati normalmente (dal parametro splat).</span><span class="sxs-lookup"><span data-stu-id="72b65-120">The location of the extension is not retrieved via the pipeline but rather via the parameters specified normally (by the splat parameter).</span></span>

### <span data-ttu-id="72b65-121">Esempio 4: Uso di un oggetto di estensione come posizione e parametri per l'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="72b65-121">Example 4: Using an extension object as both the location and parameters for updating</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> # Update the settings on the object that will be used via the pipeline
PS C:\> $extToUpdate.Setting.commandToExecute = "ls -l"
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension -ExtensionParameter $extToUpdate

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="72b65-122">Aggiorna una specifica estensione passata tramite la pipeline.</span><span class="sxs-lookup"><span data-stu-id="72b65-122">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="72b65-123">Qui è in uso l'estensione passata tramite la pipeline per aiutare Microsoft a identificare l'estensione su cui si vuole operare.</span><span class="sxs-lookup"><span data-stu-id="72b65-123">Here we are using the extension passed in via the pipeline to help us identify which extension we want to operate on.</span></span>
<span data-ttu-id="72b65-124">Inoltre, vengono utilizzati i parametri dell'oggetto estensione per specificare gli elementi da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="72b65-124">In addition to that, we are using the parameters of the extension object to specify what to update.</span></span>

## <span data-ttu-id="72b65-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72b65-125">PARAMETERS</span></span>

### <span data-ttu-id="72b65-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="72b65-126">-AsJob</span></span>
<span data-ttu-id="72b65-127">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="72b65-127">Run the command as a job</span></span>

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

### <span data-ttu-id="72b65-128">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="72b65-128">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="72b65-129">Indica se l'estensione deve usare una versione secondaria più recente, se disponibile al momento della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="72b65-129">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="72b65-130">Una volta distribuita, tuttavia, l'estensione non aggiorna le versioni secondarie a meno che non venga ridistribuito, anche con questa proprietà impostata su true.</span><span class="sxs-lookup"><span data-stu-id="72b65-130">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72b65-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72b65-131">-DefaultProfile</span></span>
<span data-ttu-id="72b65-132">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="72b65-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72b65-133">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="72b65-133">-ExtensionParameter</span></span>
<span data-ttu-id="72b65-134">Descrive un aggiornamento dell'estensione del computer.</span><span class="sxs-lookup"><span data-stu-id="72b65-134">Describes a Machine Extension Update.</span></span>
<span data-ttu-id="72b65-135">Per creare, vedere la sezione NOTE per le proprietà EXTENSIONPARAMETER e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="72b65-135">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdate
Parameter Sets: Update, UpdateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72b65-136">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="72b65-136">-ForceRerun</span></span>
<span data-ttu-id="72b65-137">Come deve essere forzato l'aggiornamento del gestore delle estensioni anche se la configurazione dell'estensione non è cambiata.</span><span class="sxs-lookup"><span data-stu-id="72b65-137">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72b65-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72b65-138">-InputObject</span></span>
<span data-ttu-id="72b65-139">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="72b65-139">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity
Parameter Sets: UpdateViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72b65-140">-MachineName</span><span class="sxs-lookup"><span data-stu-id="72b65-140">-MachineName</span></span>
<span data-ttu-id="72b65-141">Nome del computer in cui deve essere creata o aggiornata l'estensione.</span><span class="sxs-lookup"><span data-stu-id="72b65-141">The name of the machine where the extension should be created or updated.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72b65-142">-Name</span><span class="sxs-lookup"><span data-stu-id="72b65-142">-Name</span></span>
<span data-ttu-id="72b65-143">Nome dell'estensione del computer.</span><span class="sxs-lookup"><span data-stu-id="72b65-143">The name of the machine extension.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72b65-144">-NoWait</span><span class="sxs-lookup"><span data-stu-id="72b65-144">-NoWait</span></span>
<span data-ttu-id="72b65-145">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="72b65-145">Run the command asynchronously</span></span>

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

### <span data-ttu-id="72b65-146">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="72b65-146">-ProtectedSetting</span></span>
<span data-ttu-id="72b65-147">L'estensione può contenere protectedSettings o protectedSettingsFromKeyVault o nessuna impostazione protetta.</span><span class="sxs-lookup"><span data-stu-id="72b65-147">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdatePropertiesProtectedSettings
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases: ProtectedSettings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72b65-148">-Publisher</span><span class="sxs-lookup"><span data-stu-id="72b65-148">-Publisher</span></span>
<span data-ttu-id="72b65-149">Nome dell'autore del gestore estensioni.</span><span class="sxs-lookup"><span data-stu-id="72b65-149">The name of the extension handler publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72b65-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72b65-150">-ResourceGroupName</span></span>
<span data-ttu-id="72b65-151">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="72b65-151">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72b65-152">-Setting</span><span class="sxs-lookup"><span data-stu-id="72b65-152">-Setting</span></span>
<span data-ttu-id="72b65-153">Impostazioni pubbliche in formato Json per l'estensione.</span><span class="sxs-lookup"><span data-stu-id="72b65-153">Json formatted public settings for the extension.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdatePropertiesSettings
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases: Settings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72b65-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="72b65-154">-SubscriptionId</span></span>
<span data-ttu-id="72b65-155">Credenziali di abbonamento che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="72b65-155">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="72b65-156">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="72b65-156">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72b65-157">-Tag</span><span class="sxs-lookup"><span data-stu-id="72b65-157">-Tag</span></span>
<span data-ttu-id="72b65-158">Tag di risorse</span><span class="sxs-lookup"><span data-stu-id="72b65-158">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72b65-159">-Type</span><span class="sxs-lookup"><span data-stu-id="72b65-159">-Type</span></span>
<span data-ttu-id="72b65-160">Specifica il tipo di estensione; un esempio è "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="72b65-160">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72b65-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="72b65-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="72b65-162">Specifica la versione del gestore di script.</span><span class="sxs-lookup"><span data-stu-id="72b65-162">Specifies the version of the script handler.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72b65-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="72b65-163">-Confirm</span></span>
<span data-ttu-id="72b65-164">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72b65-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72b65-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72b65-165">-WhatIf</span></span>
<span data-ttu-id="72b65-166">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="72b65-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72b65-167">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="72b65-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72b65-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72b65-168">CommonParameters</span></span>
<span data-ttu-id="72b65-169">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72b65-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72b65-170">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="72b65-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72b65-171">INPUT</span><span class="sxs-lookup"><span data-stu-id="72b65-171">INPUTS</span></span>

### <span data-ttu-id="72b65-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdate</span><span class="sxs-lookup"><span data-stu-id="72b65-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdate</span></span>

### <span data-ttu-id="72b65-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="72b65-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="72b65-174">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="72b65-174">OUTPUTS</span></span>

### <span data-ttu-id="72b65-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="72b65-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="72b65-176">NOTE</span><span class="sxs-lookup"><span data-stu-id="72b65-176">NOTES</span></span>

<span data-ttu-id="72b65-177">ALIAS</span><span class="sxs-lookup"><span data-stu-id="72b65-177">ALIASES</span></span>

<span data-ttu-id="72b65-178">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="72b65-178">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="72b65-179">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="72b65-179">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="72b65-180">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="72b65-180">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="72b65-181"><IMachineExtensionUpdate>EXTENSIONPARAMETER: descrive un aggiornamento dell'estensione del computer.</span><span class="sxs-lookup"><span data-stu-id="72b65-181">EXTENSIONPARAMETER <IMachineExtensionUpdate>: Describes a Machine Extension Update.</span></span>
  - <span data-ttu-id="72b65-182">`[Tag <IUpdateResourceTags>]`: tag di risorse</span><span class="sxs-lookup"><span data-stu-id="72b65-182">`[Tag <IUpdateResourceTags>]`: Resource tags</span></span>
    - <span data-ttu-id="72b65-183">`[(Any) <String>]`: indica che è possibile aggiungere qualsiasi proprietà all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="72b65-183">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="72b65-184">`[AutoUpgradeMinorVersion <Boolean?>]`: indica se l'estensione deve usare una versione secondaria più recente, se disponibile al momento della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="72b65-184">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="72b65-185">Una volta distribuita, tuttavia, l'estensione non aggiorna le versioni secondarie a meno che non venga ridistribuito, anche con questa proprietà impostata su true.</span><span class="sxs-lookup"><span data-stu-id="72b65-185">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="72b65-186">`[ForceUpdateTag <String>]`: come deve essere forzato l'aggiornamento del gestore delle estensioni anche se la configurazione dell'estensione non è cambiata.</span><span class="sxs-lookup"><span data-stu-id="72b65-186">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="72b65-187">`[ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]`: l'estensione può contenere protectedSettings o protectedSettingsFromKeyVault o nessuna impostazione protetta.</span><span class="sxs-lookup"><span data-stu-id="72b65-187">`[ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="72b65-188">`[Publisher <String>]`: nome dell'autore del gestore estensioni.</span><span class="sxs-lookup"><span data-stu-id="72b65-188">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="72b65-189">`[Setting <IMachineExtensionUpdatePropertiesSettings>]`: impostazioni pubbliche in formato Json per l'estensione.</span><span class="sxs-lookup"><span data-stu-id="72b65-189">`[Setting <IMachineExtensionUpdatePropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="72b65-190">`[Type <String>]`: specifica il tipo dell'estensione; un esempio è "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="72b65-190">`[Type <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="72b65-191">`[TypeHandlerVersion <String>]`: specifica la versione del gestore di script.</span><span class="sxs-lookup"><span data-stu-id="72b65-191">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

<span data-ttu-id="72b65-192">INPUTOBJECT <IConnectedMachineIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="72b65-192">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="72b65-193">`[ExtensionName <String>]`: nome dell'estensione del computer.</span><span class="sxs-lookup"><span data-stu-id="72b65-193">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="72b65-194">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="72b65-194">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="72b65-195">`[Name <String>]`: nome del computer ibrido.</span><span class="sxs-lookup"><span data-stu-id="72b65-195">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="72b65-196">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="72b65-196">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="72b65-197">`[SubscriptionId <String>]`: credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="72b65-197">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="72b65-198">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="72b65-198">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="72b65-199">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="72b65-199">RELATED LINKS</span></span>

