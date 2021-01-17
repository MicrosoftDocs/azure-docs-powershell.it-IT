---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/new-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/New-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/New-AzConnectedMachineExtension.md
ms.openlocfilehash: 13095d24bd095e27bac788d0d578bdcdf3e1a0f7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488071"
---
# <span data-ttu-id="d56f0-101">New-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="d56f0-101">New-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="d56f0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d56f0-102">SYNOPSIS</span></span>
<span data-ttu-id="d56f0-103">Operazione per creare o aggiornare l'estensione.</span><span class="sxs-lookup"><span data-stu-id="d56f0-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="d56f0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d56f0-104">SYNTAX</span></span>

### <span data-ttu-id="d56f0-105">CreateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d56f0-105">CreateExpanded (Default)</span></span>
```
New-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -Location <String> [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ExtensionType <String>]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="d56f0-106">Creare</span><span class="sxs-lookup"><span data-stu-id="d56f0-106">Create</span></span>
```
New-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtension> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d56f0-107">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d56f0-107">CreateViaIdentity</span></span>
```
New-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity>
 -ExtensionParameter <IMachineExtension> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="d56f0-108">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d56f0-108">CreateViaIdentityExpanded</span></span>
```
New-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> -Location <String>
 [-AutoUpgradeMinorVersion] [-ExtensionType <String>] [-ForceRerun <String>]
 [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>] [-Publisher <String>]
 [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>] [-TypeHandlerVersion <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d56f0-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d56f0-109">DESCRIPTION</span></span>
<span data-ttu-id="d56f0-110">Operazione per creare o aggiornare l'estensione.</span><span class="sxs-lookup"><span data-stu-id="d56f0-110">The operation to create or update the extension.</span></span>

## <span data-ttu-id="d56f0-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d56f0-111">EXAMPLES</span></span>

### <span data-ttu-id="d56f0-112">Esempio 1: aggiungere una nuova estensione a un computer</span><span class="sxs-lookup"><span data-stu-id="d56f0-112">Example 1: Add a new extension to a machine</span></span>
```powershell
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> New-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName win-eastus1 -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="d56f0-113">Imposta un'estensione in un computer.</span><span class="sxs-lookup"><span data-stu-id="d56f0-113">Sets an extension on a machine.</span></span>

### <span data-ttu-id="d56f0-114">Esempio 2: aggiungere una nuova estensione con i parametri di estensione specificati tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="d56f0-114">Example 2: Add a new extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $otherExtension = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $otherExtension | New-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName important

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="d56f0-115">Verrà creata una nuova estensione con i parametri di estensione forniti dall'oggetto passato tramite la pipeline.</span><span class="sxs-lookup"><span data-stu-id="d56f0-115">This creates a new extension with the extension parameters provided by the object passed in via the pipeline.</span></span>
<span data-ttu-id="d56f0-116">Questa operazione è utile se si vuole afferrare i parametri di un computer e applicarlo a un altro computer.</span><span class="sxs-lookup"><span data-stu-id="d56f0-116">This is great if you want to grab the parameters of one machine and apply it to another machine.</span></span>

### <span data-ttu-id="d56f0-117">Esempio 3: aggiungere una nuova estensione con il percorso specificato tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="d56f0-117">Example 3: Add a new extension with location specified via the pipeline</span></span>
```powershell
PS C:\> $identity = [Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.ConnectedMachineIdentity]@{
    Id = "/subscriptions/$($SubscriptionId)/resourceGroups/$($ResourceGroupName)/providers/Microsoft.HybridCompute/machines/$MachineName/extensions/$ExtensionName"
}
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> $identity | New-AzConnectedMachineExtension -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="d56f0-118">Verrà creata una nuova estensione del computer utilizzando l'identità fornita tramite la pipeline.</span><span class="sxs-lookup"><span data-stu-id="d56f0-118">This creates a new machine extension using the identity provided via the pipeline.</span></span>
<span data-ttu-id="d56f0-119">Probabilmente non lo farai, ma è possibile.</span><span class="sxs-lookup"><span data-stu-id="d56f0-119">You likely won't do this, but it's possible.</span></span>

### <span data-ttu-id="d56f0-120">Esempio 4: aggiungere una nuova estensione usando un oggetto Extension come posizione e parametri per l'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="d56f0-120">Example 4: Add a new extension using an extension object as both the location and parameters for updating</span></span>
```powershell
PS C:\> $ext = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $ext | New-AzConnectedMachineExtension -ExtensionParameter $ext
```

<span data-ttu-id="d56f0-121">In questo modo, viene creata una nuova estensione del computer utilizzando l'identità fornita tramite la pipeline e i dettagli dell'estensione forniti dall'oggetto di estensione passato.</span><span class="sxs-lookup"><span data-stu-id="d56f0-121">This creates a new machine extension using the identity provided via the pipeline and the extension details provided by the passed in extension object.</span></span>
<span data-ttu-id="d56f0-122">Probabilmente non lo farai, ma è possibile.</span><span class="sxs-lookup"><span data-stu-id="d56f0-122">You likely won't do this, but it's possible.</span></span>

## <span data-ttu-id="d56f0-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d56f0-123">PARAMETERS</span></span>

### <span data-ttu-id="d56f0-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d56f0-124">-AsJob</span></span>
<span data-ttu-id="d56f0-125">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="d56f0-125">Run the command as a job</span></span>

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

### <span data-ttu-id="d56f0-126">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="d56f0-126">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="d56f0-127">Indica se l'estensione deve usare una versione secondaria più recente, se disponibile in fase di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="d56f0-127">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="d56f0-128">Una volta distribuita, tuttavia, l'estensione non aggiornerà le versioni secondarie, a meno che non vengano ridistribuite, anche se questa proprietà è impostata su true.</span><span class="sxs-lookup"><span data-stu-id="d56f0-128">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d56f0-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d56f0-129">-DefaultProfile</span></span>
<span data-ttu-id="d56f0-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d56f0-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d56f0-131">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="d56f0-131">-ExtensionParameter</span></span>
<span data-ttu-id="d56f0-132">Descrive un'estensione del computer.</span><span class="sxs-lookup"><span data-stu-id="d56f0-132">Describes a Machine Extension.</span></span>
<span data-ttu-id="d56f0-133">Per costruire, vedere la sezione Note per le proprietà di EXTENSIONPARAMETER e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="d56f0-133">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension
Parameter Sets: Create, CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d56f0-134">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="d56f0-134">-ExtensionType</span></span>
<span data-ttu-id="d56f0-135">Specifica il tipo di estensione; un esempio è "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="d56f0-135">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d56f0-136">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="d56f0-136">-ForceRerun</span></span>
<span data-ttu-id="d56f0-137">Come il gestore dell'estensione deve essere costretto ad aggiornare anche se la configurazione dell'estensione non è cambiata.</span><span class="sxs-lookup"><span data-stu-id="d56f0-137">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d56f0-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d56f0-138">-InputObject</span></span>
<span data-ttu-id="d56f0-139">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="d56f0-139">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity
Parameter Sets: CreateViaIdentity, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d56f0-140">-Posizione</span><span class="sxs-lookup"><span data-stu-id="d56f0-140">-Location</span></span>
<span data-ttu-id="d56f0-141">Posizione geografica in cui vive la risorsa</span><span class="sxs-lookup"><span data-stu-id="d56f0-141">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d56f0-142">-MachineName</span><span class="sxs-lookup"><span data-stu-id="d56f0-142">-MachineName</span></span>
<span data-ttu-id="d56f0-143">Il nome del computer in cui deve essere creata o aggiornata l'estensione.</span><span class="sxs-lookup"><span data-stu-id="d56f0-143">The name of the machine where the extension should be created or updated.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d56f0-144">-Nome</span><span class="sxs-lookup"><span data-stu-id="d56f0-144">-Name</span></span>
<span data-ttu-id="d56f0-145">Nome dell'estensione del computer.</span><span class="sxs-lookup"><span data-stu-id="d56f0-145">The name of the machine extension.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d56f0-146">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="d56f0-146">-NoWait</span></span>
<span data-ttu-id="d56f0-147">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="d56f0-147">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d56f0-148">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="d56f0-148">-ProtectedSetting</span></span>
<span data-ttu-id="d56f0-149">L'estensione può contenere protectedSettings o protectedSettingsFromKeyVault o nessuna impostazione protetta.</span><span class="sxs-lookup"><span data-stu-id="d56f0-149">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionPropertiesProtectedSettings
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases: ProtectedSettings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d56f0-150">-Publisher</span><span class="sxs-lookup"><span data-stu-id="d56f0-150">-Publisher</span></span>
<span data-ttu-id="d56f0-151">Nome dell'autore del gestore di estensione.</span><span class="sxs-lookup"><span data-stu-id="d56f0-151">The name of the extension handler publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d56f0-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d56f0-152">-ResourceGroupName</span></span>
<span data-ttu-id="d56f0-153">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d56f0-153">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d56f0-154">-Impostazione</span><span class="sxs-lookup"><span data-stu-id="d56f0-154">-Setting</span></span>
<span data-ttu-id="d56f0-155">Impostazioni pubbliche in formato JSON per l'estensione.</span><span class="sxs-lookup"><span data-stu-id="d56f0-155">Json formatted public settings for the extension.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionPropertiesSettings
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases: Settings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d56f0-156">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d56f0-156">-SubscriptionId</span></span>
<span data-ttu-id="d56f0-157">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d56f0-157">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d56f0-158">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="d56f0-158">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d56f0-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="d56f0-159">-Tag</span></span>
<span data-ttu-id="d56f0-160">Tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="d56f0-160">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d56f0-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="d56f0-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="d56f0-162">Specifica la versione del gestore di script.</span><span class="sxs-lookup"><span data-stu-id="d56f0-162">Specifies the version of the script handler.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d56f0-163">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d56f0-163">-Confirm</span></span>
<span data-ttu-id="d56f0-164">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d56f0-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d56f0-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d56f0-165">-WhatIf</span></span>
<span data-ttu-id="d56f0-166">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d56f0-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d56f0-167">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d56f0-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d56f0-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d56f0-168">CommonParameters</span></span>
<span data-ttu-id="d56f0-169">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d56f0-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d56f0-170">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d56f0-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d56f0-171">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d56f0-171">INPUTS</span></span>

### <span data-ttu-id="d56f0-172">Microsoft. Azure. PowerShell. Cmdlets. ConnectedMachine. Models. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="d56f0-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

### <span data-ttu-id="d56f0-173">Microsoft. Azure. PowerShell. Cmdlets. ConnectedMachine. Models. IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="d56f0-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="d56f0-174">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d56f0-174">OUTPUTS</span></span>

### <span data-ttu-id="d56f0-175">Microsoft. Azure. PowerShell. Cmdlets. ConnectedMachine. Models. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="d56f0-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="d56f0-176">Note</span><span class="sxs-lookup"><span data-stu-id="d56f0-176">NOTES</span></span>

<span data-ttu-id="d56f0-177">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d56f0-177">ALIASES</span></span>

<span data-ttu-id="d56f0-178">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d56f0-178">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d56f0-179">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="d56f0-179">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d56f0-180">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d56f0-180">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d56f0-181">EXTENSIONPARAMETER <IMachineExtension> : descrive un'estensione del computer.</span><span class="sxs-lookup"><span data-stu-id="d56f0-181">EXTENSIONPARAMETER <IMachineExtension>: Describes a Machine Extension.</span></span>
  - <span data-ttu-id="d56f0-182">`Location <String>`: La posizione geografica in cui vive la risorsa</span><span class="sxs-lookup"><span data-stu-id="d56f0-182">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="d56f0-183">`[Tag <ITrackedResourceTags>]`: Tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="d56f0-183">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="d56f0-184">`[(Any) <String>]`: Indica che qualsiasi proprietà può essere aggiunta a questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="d56f0-184">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="d56f0-185">`[AutoUpgradeMinorVersion <Boolean?>]`: Indica se l'estensione deve usare una versione secondaria più recente, se disponibile al momento della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="d56f0-185">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="d56f0-186">Una volta distribuita, tuttavia, l'estensione non aggiornerà le versioni secondarie, a meno che non vengano ridistribuite, anche se questa proprietà è impostata su true.</span><span class="sxs-lookup"><span data-stu-id="d56f0-186">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="d56f0-187">`[ForceUpdateTag <String>]`: Come deve essere forzata l'aggiornamento del gestore dell'estensione anche se la configurazione dell'estensione non è cambiata.</span><span class="sxs-lookup"><span data-stu-id="d56f0-187">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="d56f0-188">`[MachineExtensionType <String>]`: Specifica il tipo di estensione; un esempio è "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="d56f0-188">`[MachineExtensionType <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="d56f0-189">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: L'estensione può contenere protectedSettings o protectedSettingsFromKeyVault o nessuna impostazione protetta.</span><span class="sxs-lookup"><span data-stu-id="d56f0-189">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="d56f0-190">`[Publisher <String>]`: Nome dell'editore del gestore di estensione.</span><span class="sxs-lookup"><span data-stu-id="d56f0-190">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="d56f0-191">`[Setting <IMachineExtensionPropertiesSettings>]`: Le impostazioni pubbliche formattate JSON per l'estensione.</span><span class="sxs-lookup"><span data-stu-id="d56f0-191">`[Setting <IMachineExtensionPropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="d56f0-192">`[TypeHandlerVersion <String>]`: Specifica la versione del gestore script.</span><span class="sxs-lookup"><span data-stu-id="d56f0-192">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

<span data-ttu-id="d56f0-193">INPUTOBJECT <IConnectedMachineIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="d56f0-193">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d56f0-194">`[ExtensionName <String>]`: Nome dell'estensione del computer.</span><span class="sxs-lookup"><span data-stu-id="d56f0-194">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="d56f0-195">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="d56f0-195">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d56f0-196">`[Name <String>]`: Nome della macchina ibrida.</span><span class="sxs-lookup"><span data-stu-id="d56f0-196">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="d56f0-197">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d56f0-197">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="d56f0-198">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d56f0-198">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d56f0-199">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="d56f0-199">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d56f0-200">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d56f0-200">RELATED LINKS</span></span>

