---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/new-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/New-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/New-AzConnectedMachineExtension.md
ms.openlocfilehash: 13095d24bd095e27bac788d0d578bdcdf3e1a0f7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209915"
---
# <span data-ttu-id="464a2-101">New-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="464a2-101">New-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="464a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="464a2-102">SYNOPSIS</span></span>
<span data-ttu-id="464a2-103">Operazione per creare o aggiornare l'estensione.</span><span class="sxs-lookup"><span data-stu-id="464a2-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="464a2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="464a2-104">SYNTAX</span></span>

### <span data-ttu-id="464a2-105">CreateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="464a2-105">CreateExpanded (Default)</span></span>
```
New-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -Location <String> [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ExtensionType <String>]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="464a2-106">Crea</span><span class="sxs-lookup"><span data-stu-id="464a2-106">Create</span></span>
```
New-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtension> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="464a2-107">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="464a2-107">CreateViaIdentity</span></span>
```
New-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity>
 -ExtensionParameter <IMachineExtension> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="464a2-108">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="464a2-108">CreateViaIdentityExpanded</span></span>
```
New-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> -Location <String>
 [-AutoUpgradeMinorVersion] [-ExtensionType <String>] [-ForceRerun <String>]
 [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>] [-Publisher <String>]
 [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>] [-TypeHandlerVersion <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="464a2-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="464a2-109">DESCRIPTION</span></span>
<span data-ttu-id="464a2-110">Operazione per creare o aggiornare l'estensione.</span><span class="sxs-lookup"><span data-stu-id="464a2-110">The operation to create or update the extension.</span></span>

## <span data-ttu-id="464a2-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="464a2-111">EXAMPLES</span></span>

### <span data-ttu-id="464a2-112">Esempio 1: Aggiungere una nuova estensione a un computer</span><span class="sxs-lookup"><span data-stu-id="464a2-112">Example 1: Add a new extension to a machine</span></span>
```powershell
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> New-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName win-eastus1 -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="464a2-113">Imposta un'estensione in un computer.</span><span class="sxs-lookup"><span data-stu-id="464a2-113">Sets an extension on a machine.</span></span>

### <span data-ttu-id="464a2-114">Esempio 2: Aggiungere una nuova estensione con i parametri di estensione specificati tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="464a2-114">Example 2: Add a new extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $otherExtension = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $otherExtension | New-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName important

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="464a2-115">Viene creata una nuova estensione con i parametri di estensione forniti dall'oggetto passato tramite la pipeline.</span><span class="sxs-lookup"><span data-stu-id="464a2-115">This creates a new extension with the extension parameters provided by the object passed in via the pipeline.</span></span>
<span data-ttu-id="464a2-116">Questa opzione è ideale se vuoi recuperare i parametri di un computer e applicarlo a un altro computer.</span><span class="sxs-lookup"><span data-stu-id="464a2-116">This is great if you want to grab the parameters of one machine and apply it to another machine.</span></span>

### <span data-ttu-id="464a2-117">Esempio 3: Aggiungere una nuova estensione con la posizione specificata tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="464a2-117">Example 3: Add a new extension with location specified via the pipeline</span></span>
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

<span data-ttu-id="464a2-118">Verrà creata una nuova estensione del computer usando l'identità fornita tramite la pipeline.</span><span class="sxs-lookup"><span data-stu-id="464a2-118">This creates a new machine extension using the identity provided via the pipeline.</span></span>
<span data-ttu-id="464a2-119">Probabilmente non lo farete, ma è possibile.</span><span class="sxs-lookup"><span data-stu-id="464a2-119">You likely won't do this, but it's possible.</span></span>

### <span data-ttu-id="464a2-120">Esempio 4: Aggiungere una nuova estensione usando un oggetto di estensione come posizione e parametri per l'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="464a2-120">Example 4: Add a new extension using an extension object as both the location and parameters for updating</span></span>
```powershell
PS C:\> $ext = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $ext | New-AzConnectedMachineExtension -ExtensionParameter $ext
```

<span data-ttu-id="464a2-121">Viene creata una nuova estensione del computer usando l'identità fornita tramite la pipeline e i dettagli dell'estensione forniti dall'oggetto estensione passato.</span><span class="sxs-lookup"><span data-stu-id="464a2-121">This creates a new machine extension using the identity provided via the pipeline and the extension details provided by the passed in extension object.</span></span>
<span data-ttu-id="464a2-122">Probabilmente non lo farete, ma è possibile.</span><span class="sxs-lookup"><span data-stu-id="464a2-122">You likely won't do this, but it's possible.</span></span>

## <span data-ttu-id="464a2-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="464a2-123">PARAMETERS</span></span>

### <span data-ttu-id="464a2-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="464a2-124">-AsJob</span></span>
<span data-ttu-id="464a2-125">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="464a2-125">Run the command as a job</span></span>

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

### <span data-ttu-id="464a2-126">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="464a2-126">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="464a2-127">Indica se l'estensione deve usare una versione secondaria più recente, se disponibile al momento della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="464a2-127">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="464a2-128">Una volta distribuita, tuttavia, l'estensione non aggiorna le versioni secondarie a meno che non venga ridistribuito, anche con questa proprietà impostata su true.</span><span class="sxs-lookup"><span data-stu-id="464a2-128">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

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

### <span data-ttu-id="464a2-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="464a2-129">-DefaultProfile</span></span>
<span data-ttu-id="464a2-130">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="464a2-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="464a2-131">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="464a2-131">-ExtensionParameter</span></span>
<span data-ttu-id="464a2-132">Descrive un'estensione del computer.</span><span class="sxs-lookup"><span data-stu-id="464a2-132">Describes a Machine Extension.</span></span>
<span data-ttu-id="464a2-133">Per creare, vedere la sezione NOTE per le proprietà EXTENSIONPARAMETER e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="464a2-133">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="464a2-134">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="464a2-134">-ExtensionType</span></span>
<span data-ttu-id="464a2-135">Specifica il tipo di estensione; un esempio è "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="464a2-135">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

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

### <span data-ttu-id="464a2-136">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="464a2-136">-ForceRerun</span></span>
<span data-ttu-id="464a2-137">Come deve essere forzato l'aggiornamento del gestore delle estensioni anche se la configurazione dell'estensione non è cambiata.</span><span class="sxs-lookup"><span data-stu-id="464a2-137">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="464a2-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="464a2-138">-InputObject</span></span>
<span data-ttu-id="464a2-139">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="464a2-139">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="464a2-140">-Location</span><span class="sxs-lookup"><span data-stu-id="464a2-140">-Location</span></span>
<span data-ttu-id="464a2-141">Posizione geografica in cui si trova la risorsa</span><span class="sxs-lookup"><span data-stu-id="464a2-141">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="464a2-142">-MachineName</span><span class="sxs-lookup"><span data-stu-id="464a2-142">-MachineName</span></span>
<span data-ttu-id="464a2-143">Nome del computer in cui deve essere creata o aggiornata l'estensione.</span><span class="sxs-lookup"><span data-stu-id="464a2-143">The name of the machine where the extension should be created or updated.</span></span>

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

### <span data-ttu-id="464a2-144">-Name</span><span class="sxs-lookup"><span data-stu-id="464a2-144">-Name</span></span>
<span data-ttu-id="464a2-145">Nome dell'estensione del computer.</span><span class="sxs-lookup"><span data-stu-id="464a2-145">The name of the machine extension.</span></span>

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

### <span data-ttu-id="464a2-146">-NoWait</span><span class="sxs-lookup"><span data-stu-id="464a2-146">-NoWait</span></span>
<span data-ttu-id="464a2-147">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="464a2-147">Run the command asynchronously</span></span>

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

### <span data-ttu-id="464a2-148">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="464a2-148">-ProtectedSetting</span></span>
<span data-ttu-id="464a2-149">L'estensione può contenere protectedSettings o protectedSettingsFromKeyVault o nessuna impostazione protetta.</span><span class="sxs-lookup"><span data-stu-id="464a2-149">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

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

### <span data-ttu-id="464a2-150">-Publisher</span><span class="sxs-lookup"><span data-stu-id="464a2-150">-Publisher</span></span>
<span data-ttu-id="464a2-151">Nome dell'autore del gestore estensioni.</span><span class="sxs-lookup"><span data-stu-id="464a2-151">The name of the extension handler publisher.</span></span>

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

### <span data-ttu-id="464a2-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="464a2-152">-ResourceGroupName</span></span>
<span data-ttu-id="464a2-153">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="464a2-153">The name of the resource group.</span></span>

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

### <span data-ttu-id="464a2-154">-Setting</span><span class="sxs-lookup"><span data-stu-id="464a2-154">-Setting</span></span>
<span data-ttu-id="464a2-155">Impostazioni pubbliche in formato Json per l'estensione.</span><span class="sxs-lookup"><span data-stu-id="464a2-155">Json formatted public settings for the extension.</span></span>

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

### <span data-ttu-id="464a2-156">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="464a2-156">-SubscriptionId</span></span>
<span data-ttu-id="464a2-157">Credenziali di abbonamento che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="464a2-157">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="464a2-158">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="464a2-158">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="464a2-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="464a2-159">-Tag</span></span>
<span data-ttu-id="464a2-160">Tag di risorse.</span><span class="sxs-lookup"><span data-stu-id="464a2-160">Resource tags.</span></span>

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

### <span data-ttu-id="464a2-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="464a2-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="464a2-162">Specifica la versione del gestore di script.</span><span class="sxs-lookup"><span data-stu-id="464a2-162">Specifies the version of the script handler.</span></span>

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

### <span data-ttu-id="464a2-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="464a2-163">-Confirm</span></span>
<span data-ttu-id="464a2-164">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="464a2-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="464a2-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="464a2-165">-WhatIf</span></span>
<span data-ttu-id="464a2-166">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="464a2-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="464a2-167">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="464a2-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="464a2-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="464a2-168">CommonParameters</span></span>
<span data-ttu-id="464a2-169">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="464a2-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="464a2-170">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="464a2-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="464a2-171">INPUT</span><span class="sxs-lookup"><span data-stu-id="464a2-171">INPUTS</span></span>

### <span data-ttu-id="464a2-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="464a2-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

### <span data-ttu-id="464a2-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="464a2-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="464a2-174">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="464a2-174">OUTPUTS</span></span>

### <span data-ttu-id="464a2-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="464a2-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="464a2-176">NOTE</span><span class="sxs-lookup"><span data-stu-id="464a2-176">NOTES</span></span>

<span data-ttu-id="464a2-177">ALIAS</span><span class="sxs-lookup"><span data-stu-id="464a2-177">ALIASES</span></span>

<span data-ttu-id="464a2-178">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="464a2-178">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="464a2-179">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="464a2-179">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="464a2-180">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="464a2-180">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="464a2-181"><IMachineExtension>EXTENSIONPARAMETER: descrive un'estensione del computer.</span><span class="sxs-lookup"><span data-stu-id="464a2-181">EXTENSIONPARAMETER <IMachineExtension>: Describes a Machine Extension.</span></span>
  - <span data-ttu-id="464a2-182">`Location <String>`: posizione geografica in cui si trova la risorsa</span><span class="sxs-lookup"><span data-stu-id="464a2-182">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="464a2-183">`[Tag <ITrackedResourceTags>]`: tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="464a2-183">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="464a2-184">`[(Any) <String>]`: indica che è possibile aggiungere qualsiasi proprietà all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="464a2-184">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="464a2-185">`[AutoUpgradeMinorVersion <Boolean?>]`: indica se l'estensione deve usare una versione secondaria più recente, se disponibile al momento della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="464a2-185">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="464a2-186">Una volta distribuita, tuttavia, l'estensione non aggiorna le versioni secondarie a meno che non venga ridistribuito, anche con questa proprietà impostata su true.</span><span class="sxs-lookup"><span data-stu-id="464a2-186">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="464a2-187">`[ForceUpdateTag <String>]`: come deve essere forzato l'aggiornamento del gestore delle estensioni anche se la configurazione dell'estensione non è cambiata.</span><span class="sxs-lookup"><span data-stu-id="464a2-187">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="464a2-188">`[MachineExtensionType <String>]`: specifica il tipo dell'estensione; un esempio è "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="464a2-188">`[MachineExtensionType <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="464a2-189">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: l'estensione può contenere protectedSettings o protectedSettingsFromKeyVault o nessuna impostazione protetta.</span><span class="sxs-lookup"><span data-stu-id="464a2-189">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="464a2-190">`[Publisher <String>]`: nome dell'autore del gestore estensioni.</span><span class="sxs-lookup"><span data-stu-id="464a2-190">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="464a2-191">`[Setting <IMachineExtensionPropertiesSettings>]`: impostazioni pubbliche in formato Json per l'estensione.</span><span class="sxs-lookup"><span data-stu-id="464a2-191">`[Setting <IMachineExtensionPropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="464a2-192">`[TypeHandlerVersion <String>]`: specifica la versione del gestore di script.</span><span class="sxs-lookup"><span data-stu-id="464a2-192">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

<span data-ttu-id="464a2-193">INPUTOBJECT <IConnectedMachineIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="464a2-193">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="464a2-194">`[ExtensionName <String>]`: nome dell'estensione del computer.</span><span class="sxs-lookup"><span data-stu-id="464a2-194">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="464a2-195">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="464a2-195">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="464a2-196">`[Name <String>]`: nome del computer ibrido.</span><span class="sxs-lookup"><span data-stu-id="464a2-196">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="464a2-197">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="464a2-197">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="464a2-198">`[SubscriptionId <String>]`: credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="464a2-198">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="464a2-199">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="464a2-199">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="464a2-200">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="464a2-200">RELATED LINKS</span></span>

