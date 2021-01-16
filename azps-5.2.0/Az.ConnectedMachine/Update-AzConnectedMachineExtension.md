---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/update-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Update-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Update-AzConnectedMachineExtension.md
ms.openlocfilehash: 95334b4f67685183e499518b068f1003f5bb6547
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325606"
---
# <span data-ttu-id="99a38-101">Update-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="99a38-101">Update-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="99a38-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="99a38-102">SYNOPSIS</span></span>
<span data-ttu-id="99a38-103">Operazione per creare o aggiornare l'estensione.</span><span class="sxs-lookup"><span data-stu-id="99a38-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="99a38-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="99a38-104">SYNTAX</span></span>

### <span data-ttu-id="99a38-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="99a38-105">UpdateExpanded (Default)</span></span>
```
Update-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>] [-Publisher <String>]
 [-Setting <IMachineExtensionUpdatePropertiesSettings>] [-Tag <Hashtable>] [-Type <String>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="99a38-106">Aggiornamento</span><span class="sxs-lookup"><span data-stu-id="99a38-106">Update</span></span>
```
Update-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtensionUpdate> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="99a38-107">UpdateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="99a38-107">UpdateViaIdentity</span></span>
```
Update-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity>
 -ExtensionParameter <IMachineExtensionUpdate> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="99a38-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="99a38-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> [-AutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionUpdatePropertiesSettings>] [-Tag <Hashtable>]
 [-Type <String>] [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="99a38-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="99a38-109">DESCRIPTION</span></span>
<span data-ttu-id="99a38-110">Operazione per creare o aggiornare l'estensione.</span><span class="sxs-lookup"><span data-stu-id="99a38-110">The operation to create or update the extension.</span></span>

## <span data-ttu-id="99a38-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="99a38-111">EXAMPLES</span></span>

### <span data-ttu-id="99a38-112">Esempio 1: aggiornare un'estensione</span><span class="sxs-lookup"><span data-stu-id="99a38-112">Example 1: Update an extension</span></span>
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

<span data-ttu-id="99a38-113">Aggiorna un'estensione in un computer specifico.</span><span class="sxs-lookup"><span data-stu-id="99a38-113">Updates an extension on a specific machine.</span></span>

### <span data-ttu-id="99a38-114">Esempio 2: aggiornare un'estensione con la posizione specificata tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="99a38-114">Example 2: Update an extension with location specified via the pipeline</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension -Settings @{
                commandToExecute = "ls -l"
            }

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="99a38-115">Aggiorna un'estensione specifica passata tramite la pipeline.</span><span class="sxs-lookup"><span data-stu-id="99a38-115">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="99a38-116">Qui usiamo l'estensione passata tramite la pipeline per aiutarci a identificare l'estensione a cui vogliamo operare e a specificare ciò che vogliamo cambiare con i parametri normali (ad esempio `-Settings` )</span><span class="sxs-lookup"><span data-stu-id="99a38-116">Here we are using the extension passed in via the pipeline to help us identify which extension we want to operate on and are specifying what we want to change via the normal parameters (like `-Settings`)</span></span>

### <span data-ttu-id="99a38-117">Esempio 3: aggiornare un'estensione con i parametri di estensione specificati tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="99a38-117">Example 3: Update an extension with extension parameters specified via the pipeline</span></span>
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

<span data-ttu-id="99a38-118">Aggiorna un'estensione specifica passata tramite la pipeline.</span><span class="sxs-lookup"><span data-stu-id="99a38-118">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="99a38-119">In questo caso si usa l'estensione passata tramite la pipeline per apportare le modifiche desiderate per l'estensione.</span><span class="sxs-lookup"><span data-stu-id="99a38-119">Here we are using the extension passed in via the pipeline to provide the changes we want to make on the extension.</span></span>
<span data-ttu-id="99a38-120">La posizione dell'estensione non viene recuperata tramite la pipeline, ma piuttosto tramite i parametri specificati normalmente (tramite il parametro splat).</span><span class="sxs-lookup"><span data-stu-id="99a38-120">The location of the extension is not retrieved via the pipeline but rather via the parameters specified normally (by the splat parameter).</span></span>

### <span data-ttu-id="99a38-121">Esempio 4: uso di un oggetto Extension come posizione e parametri per l'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="99a38-121">Example 4: Using an extension object as both the location and parameters for updating</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> # Update the settings on the object that will be used via the pipeline
PS C:\> $extToUpdate.Setting.commandToExecute = "ls -l"
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension -ExtensionParameter $extToUpdate

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="99a38-122">Aggiorna un'estensione specifica passata tramite la pipeline.</span><span class="sxs-lookup"><span data-stu-id="99a38-122">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="99a38-123">Qui usiamo l'estensione passata tramite la pipeline per aiutarci a identificare l'estensione su cui vogliamo operare.</span><span class="sxs-lookup"><span data-stu-id="99a38-123">Here we are using the extension passed in via the pipeline to help us identify which extension we want to operate on.</span></span>
<span data-ttu-id="99a38-124">Oltre a questo, stiamo usando i parametri dell'oggetto Extension per specificare cosa aggiornare.</span><span class="sxs-lookup"><span data-stu-id="99a38-124">In addition to that, we are using the parameters of the extension object to specify what to update.</span></span>

## <span data-ttu-id="99a38-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="99a38-125">PARAMETERS</span></span>

### <span data-ttu-id="99a38-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="99a38-126">-AsJob</span></span>
<span data-ttu-id="99a38-127">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="99a38-127">Run the command as a job</span></span>

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

### <span data-ttu-id="99a38-128">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="99a38-128">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="99a38-129">Indica se l'estensione deve usare una versione secondaria più recente, se disponibile in fase di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="99a38-129">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="99a38-130">Una volta distribuita, tuttavia, l'estensione non aggiornerà le versioni secondarie, a meno che non vengano ridistribuite, anche se questa proprietà è impostata su true.</span><span class="sxs-lookup"><span data-stu-id="99a38-130">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

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

### <span data-ttu-id="99a38-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99a38-131">-DefaultProfile</span></span>
<span data-ttu-id="99a38-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="99a38-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99a38-133">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="99a38-133">-ExtensionParameter</span></span>
<span data-ttu-id="99a38-134">Descrive un aggiornamento dell'estensione del computer.</span><span class="sxs-lookup"><span data-stu-id="99a38-134">Describes a Machine Extension Update.</span></span>
<span data-ttu-id="99a38-135">Per costruire, vedere la sezione Note per le proprietà di EXTENSIONPARAMETER e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="99a38-135">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="99a38-136">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="99a38-136">-ForceRerun</span></span>
<span data-ttu-id="99a38-137">Come il gestore dell'estensione deve essere costretto ad aggiornare anche se la configurazione dell'estensione non è cambiata.</span><span class="sxs-lookup"><span data-stu-id="99a38-137">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="99a38-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99a38-138">-InputObject</span></span>
<span data-ttu-id="99a38-139">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="99a38-139">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="99a38-140">-MachineName</span><span class="sxs-lookup"><span data-stu-id="99a38-140">-MachineName</span></span>
<span data-ttu-id="99a38-141">Il nome del computer in cui deve essere creata o aggiornata l'estensione.</span><span class="sxs-lookup"><span data-stu-id="99a38-141">The name of the machine where the extension should be created or updated.</span></span>

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

### <span data-ttu-id="99a38-142">-Nome</span><span class="sxs-lookup"><span data-stu-id="99a38-142">-Name</span></span>
<span data-ttu-id="99a38-143">Nome dell'estensione del computer.</span><span class="sxs-lookup"><span data-stu-id="99a38-143">The name of the machine extension.</span></span>

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

### <span data-ttu-id="99a38-144">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="99a38-144">-NoWait</span></span>
<span data-ttu-id="99a38-145">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="99a38-145">Run the command asynchronously</span></span>

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

### <span data-ttu-id="99a38-146">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="99a38-146">-ProtectedSetting</span></span>
<span data-ttu-id="99a38-147">L'estensione può contenere protectedSettings o protectedSettingsFromKeyVault o nessuna impostazione protetta.</span><span class="sxs-lookup"><span data-stu-id="99a38-147">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

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

### <span data-ttu-id="99a38-148">-Publisher</span><span class="sxs-lookup"><span data-stu-id="99a38-148">-Publisher</span></span>
<span data-ttu-id="99a38-149">Nome dell'autore del gestore di estensione.</span><span class="sxs-lookup"><span data-stu-id="99a38-149">The name of the extension handler publisher.</span></span>

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

### <span data-ttu-id="99a38-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99a38-150">-ResourceGroupName</span></span>
<span data-ttu-id="99a38-151">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="99a38-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="99a38-152">-Impostazione</span><span class="sxs-lookup"><span data-stu-id="99a38-152">-Setting</span></span>
<span data-ttu-id="99a38-153">Impostazioni pubbliche in formato JSON per l'estensione.</span><span class="sxs-lookup"><span data-stu-id="99a38-153">Json formatted public settings for the extension.</span></span>

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

### <span data-ttu-id="99a38-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="99a38-154">-SubscriptionId</span></span>
<span data-ttu-id="99a38-155">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="99a38-155">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="99a38-156">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="99a38-156">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="99a38-157">-Tag</span><span class="sxs-lookup"><span data-stu-id="99a38-157">-Tag</span></span>
<span data-ttu-id="99a38-158">Tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="99a38-158">Resource tags</span></span>

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

### <span data-ttu-id="99a38-159">-Digitare</span><span class="sxs-lookup"><span data-stu-id="99a38-159">-Type</span></span>
<span data-ttu-id="99a38-160">Specifica il tipo di estensione; un esempio è "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="99a38-160">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

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

### <span data-ttu-id="99a38-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="99a38-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="99a38-162">Specifica la versione del gestore di script.</span><span class="sxs-lookup"><span data-stu-id="99a38-162">Specifies the version of the script handler.</span></span>

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

### <span data-ttu-id="99a38-163">-Confermare</span><span class="sxs-lookup"><span data-stu-id="99a38-163">-Confirm</span></span>
<span data-ttu-id="99a38-164">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99a38-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99a38-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99a38-165">-WhatIf</span></span>
<span data-ttu-id="99a38-166">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="99a38-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99a38-167">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="99a38-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99a38-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99a38-168">CommonParameters</span></span>
<span data-ttu-id="99a38-169">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99a38-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99a38-170">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99a38-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99a38-171">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="99a38-171">INPUTS</span></span>

### <span data-ttu-id="99a38-172">Microsoft. Azure. PowerShell. Cmdlets. ConnectedMachine. Models. Api20200802. IMachineExtensionUpdate</span><span class="sxs-lookup"><span data-stu-id="99a38-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdate</span></span>

### <span data-ttu-id="99a38-173">Microsoft. Azure. PowerShell. Cmdlets. ConnectedMachine. Models. IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="99a38-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="99a38-174">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="99a38-174">OUTPUTS</span></span>

### <span data-ttu-id="99a38-175">Microsoft. Azure. PowerShell. Cmdlets. ConnectedMachine. Models. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="99a38-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="99a38-176">Note</span><span class="sxs-lookup"><span data-stu-id="99a38-176">NOTES</span></span>

<span data-ttu-id="99a38-177">ALIAS</span><span class="sxs-lookup"><span data-stu-id="99a38-177">ALIASES</span></span>

<span data-ttu-id="99a38-178">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="99a38-178">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="99a38-179">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="99a38-179">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="99a38-180">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="99a38-180">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="99a38-181">EXTENSIONPARAMETER <IMachineExtensionUpdate> : descrive un aggiornamento dell'estensione del computer.</span><span class="sxs-lookup"><span data-stu-id="99a38-181">EXTENSIONPARAMETER <IMachineExtensionUpdate>: Describes a Machine Extension Update.</span></span>
  - <span data-ttu-id="99a38-182">`[Tag <IUpdateResourceTags>]`: Tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="99a38-182">`[Tag <IUpdateResourceTags>]`: Resource tags</span></span>
    - <span data-ttu-id="99a38-183">`[(Any) <String>]`: Indica che qualsiasi proprietà può essere aggiunta a questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="99a38-183">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="99a38-184">`[AutoUpgradeMinorVersion <Boolean?>]`: Indica se l'estensione deve usare una versione secondaria più recente, se disponibile al momento della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="99a38-184">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="99a38-185">Una volta distribuita, tuttavia, l'estensione non aggiornerà le versioni secondarie, a meno che non vengano ridistribuite, anche se questa proprietà è impostata su true.</span><span class="sxs-lookup"><span data-stu-id="99a38-185">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="99a38-186">`[ForceUpdateTag <String>]`: Come deve essere forzata l'aggiornamento del gestore dell'estensione anche se la configurazione dell'estensione non è cambiata.</span><span class="sxs-lookup"><span data-stu-id="99a38-186">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="99a38-187">`[ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]`: L'estensione può contenere protectedSettings o protectedSettingsFromKeyVault o nessuna impostazione protetta.</span><span class="sxs-lookup"><span data-stu-id="99a38-187">`[ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="99a38-188">`[Publisher <String>]`: Nome dell'editore del gestore di estensione.</span><span class="sxs-lookup"><span data-stu-id="99a38-188">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="99a38-189">`[Setting <IMachineExtensionUpdatePropertiesSettings>]`: Le impostazioni pubbliche formattate JSON per l'estensione.</span><span class="sxs-lookup"><span data-stu-id="99a38-189">`[Setting <IMachineExtensionUpdatePropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="99a38-190">`[Type <String>]`: Specifica il tipo di estensione; un esempio è "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="99a38-190">`[Type <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="99a38-191">`[TypeHandlerVersion <String>]`: Specifica la versione del gestore script.</span><span class="sxs-lookup"><span data-stu-id="99a38-191">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

<span data-ttu-id="99a38-192">INPUTOBJECT <IConnectedMachineIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="99a38-192">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="99a38-193">`[ExtensionName <String>]`: Nome dell'estensione del computer.</span><span class="sxs-lookup"><span data-stu-id="99a38-193">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="99a38-194">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="99a38-194">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="99a38-195">`[Name <String>]`: Nome della macchina ibrida.</span><span class="sxs-lookup"><span data-stu-id="99a38-195">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="99a38-196">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="99a38-196">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="99a38-197">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="99a38-197">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="99a38-198">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="99a38-198">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="99a38-199">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="99a38-199">RELATED LINKS</span></span>

