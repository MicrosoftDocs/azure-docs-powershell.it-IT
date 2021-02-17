---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/set-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Set-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Set-AzConnectedMachineExtension.md
ms.openlocfilehash: b136f5194bdc7e0f4b4dfc969564d7ef8476d9bf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209899"
---
# <span data-ttu-id="ed768-101">Set-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="ed768-101">Set-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="ed768-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed768-102">SYNOPSIS</span></span>
<span data-ttu-id="ed768-103">Operazione per creare o aggiornare l'estensione.</span><span class="sxs-lookup"><span data-stu-id="ed768-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="ed768-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ed768-104">SYNTAX</span></span>

### <span data-ttu-id="ed768-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ed768-105">UpdateExpanded (Default)</span></span>
```
Set-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -Location <String> [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ExtensionType <String>]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="ed768-106">Aggiorna</span><span class="sxs-lookup"><span data-stu-id="ed768-106">Update</span></span>
```
Set-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtension> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ed768-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ed768-107">DESCRIPTION</span></span>
<span data-ttu-id="ed768-108">Operazione per creare o aggiornare l'estensione.</span><span class="sxs-lookup"><span data-stu-id="ed768-108">The operation to create or update the extension.</span></span>

## <span data-ttu-id="ed768-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ed768-109">EXAMPLES</span></span>

### <span data-ttu-id="ed768-110">Esempio 1: Impostare un'estensione in un computer</span><span class="sxs-lookup"><span data-stu-id="ed768-110">Example 1: Set an extension on a machine</span></span>
```powershell
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> Set-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName win-eastus1 -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="ed768-111">Imposta un'estensione in un computer.</span><span class="sxs-lookup"><span data-stu-id="ed768-111">Sets an extension on a machine.</span></span>

### <span data-ttu-id="ed768-112">Esempio 2: Impostare un'estensione con i parametri di estensione specificati tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="ed768-112">Example 2: Set an extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $otherExtension = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $otherExtension | Set-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName important

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="ed768-113">Imposta un'estensione con i parametri di estensione forniti dall'oggetto passato tramite la pipeline.</span><span class="sxs-lookup"><span data-stu-id="ed768-113">This sets an extension with the extension parameters provided by the object passed in via the pipeline.</span></span>
<span data-ttu-id="ed768-114">Questa opzione è ideale se vuoi recuperare i parametri di un computer e applicarlo a un altro computer.</span><span class="sxs-lookup"><span data-stu-id="ed768-114">This is great if you want to grab the parameters of one machine and apply it to another machine.</span></span>

## <span data-ttu-id="ed768-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed768-115">PARAMETERS</span></span>

### <span data-ttu-id="ed768-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ed768-116">-AsJob</span></span>
<span data-ttu-id="ed768-117">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="ed768-117">Run the command as a job</span></span>

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

### <span data-ttu-id="ed768-118">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="ed768-118">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="ed768-119">Indica se l'estensione deve usare una versione secondaria più recente, se disponibile al momento della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="ed768-119">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="ed768-120">Una volta distribuita, tuttavia, l'estensione non aggiorna le versioni secondarie a meno che non venga ridistribuito, anche con questa proprietà impostata su true.</span><span class="sxs-lookup"><span data-stu-id="ed768-120">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed768-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed768-121">-DefaultProfile</span></span>
<span data-ttu-id="ed768-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ed768-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed768-123">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="ed768-123">-ExtensionParameter</span></span>
<span data-ttu-id="ed768-124">Descrive un'estensione del computer.</span><span class="sxs-lookup"><span data-stu-id="ed768-124">Describes a Machine Extension.</span></span>
<span data-ttu-id="ed768-125">Per creare, vedere la sezione NOTE per le proprietà EXTENSIONPARAMETER e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="ed768-125">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed768-126">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="ed768-126">-ExtensionType</span></span>
<span data-ttu-id="ed768-127">Specifica il tipo di estensione; un esempio è "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="ed768-127">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed768-128">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="ed768-128">-ForceRerun</span></span>
<span data-ttu-id="ed768-129">Come deve essere forzato l'aggiornamento del gestore delle estensioni anche se la configurazione dell'estensione non è cambiata.</span><span class="sxs-lookup"><span data-stu-id="ed768-129">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed768-130">-Location</span><span class="sxs-lookup"><span data-stu-id="ed768-130">-Location</span></span>
<span data-ttu-id="ed768-131">Posizione geografica in cui si trova la risorsa</span><span class="sxs-lookup"><span data-stu-id="ed768-131">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed768-132">-MachineName</span><span class="sxs-lookup"><span data-stu-id="ed768-132">-MachineName</span></span>
<span data-ttu-id="ed768-133">Nome del computer in cui deve essere creata o aggiornata l'estensione.</span><span class="sxs-lookup"><span data-stu-id="ed768-133">The name of the machine where the extension should be created or updated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed768-134">-Name</span><span class="sxs-lookup"><span data-stu-id="ed768-134">-Name</span></span>
<span data-ttu-id="ed768-135">Nome dell'estensione del computer.</span><span class="sxs-lookup"><span data-stu-id="ed768-135">The name of the machine extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed768-136">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ed768-136">-NoWait</span></span>
<span data-ttu-id="ed768-137">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="ed768-137">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ed768-138">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="ed768-138">-ProtectedSetting</span></span>
<span data-ttu-id="ed768-139">L'estensione può contenere protectedSettings o protectedSettingsFromKeyVault o nessuna impostazione protetta.</span><span class="sxs-lookup"><span data-stu-id="ed768-139">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionPropertiesProtectedSettings
Parameter Sets: UpdateExpanded
Aliases: ProtectedSettings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed768-140">-Publisher</span><span class="sxs-lookup"><span data-stu-id="ed768-140">-Publisher</span></span>
<span data-ttu-id="ed768-141">Nome dell'autore del gestore estensioni.</span><span class="sxs-lookup"><span data-stu-id="ed768-141">The name of the extension handler publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed768-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed768-142">-ResourceGroupName</span></span>
<span data-ttu-id="ed768-143">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ed768-143">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed768-144">-Setting</span><span class="sxs-lookup"><span data-stu-id="ed768-144">-Setting</span></span>
<span data-ttu-id="ed768-145">Impostazioni pubbliche in formato Json per l'estensione.</span><span class="sxs-lookup"><span data-stu-id="ed768-145">Json formatted public settings for the extension.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionPropertiesSettings
Parameter Sets: UpdateExpanded
Aliases: Settings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed768-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ed768-146">-SubscriptionId</span></span>
<span data-ttu-id="ed768-147">Credenziali di abbonamento che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ed768-147">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ed768-148">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="ed768-148">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed768-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="ed768-149">-Tag</span></span>
<span data-ttu-id="ed768-150">Tag di risorse.</span><span class="sxs-lookup"><span data-stu-id="ed768-150">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed768-151">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="ed768-151">-TypeHandlerVersion</span></span>
<span data-ttu-id="ed768-152">Specifica la versione del gestore di script.</span><span class="sxs-lookup"><span data-stu-id="ed768-152">Specifies the version of the script handler.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed768-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed768-153">-Confirm</span></span>
<span data-ttu-id="ed768-154">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed768-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed768-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed768-155">-WhatIf</span></span>
<span data-ttu-id="ed768-156">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ed768-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed768-157">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ed768-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed768-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed768-158">CommonParameters</span></span>
<span data-ttu-id="ed768-159">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed768-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed768-160">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ed768-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed768-161">INPUT</span><span class="sxs-lookup"><span data-stu-id="ed768-161">INPUTS</span></span>

### <span data-ttu-id="ed768-162">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="ed768-162">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="ed768-163">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ed768-163">OUTPUTS</span></span>

### <span data-ttu-id="ed768-164">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="ed768-164">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="ed768-165">NOTE</span><span class="sxs-lookup"><span data-stu-id="ed768-165">NOTES</span></span>

<span data-ttu-id="ed768-166">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ed768-166">ALIASES</span></span>

<span data-ttu-id="ed768-167">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="ed768-167">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ed768-168">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="ed768-168">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ed768-169">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ed768-169">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ed768-170"><IMachineExtension>EXTENSIONPARAMETER: descrive un'estensione del computer.</span><span class="sxs-lookup"><span data-stu-id="ed768-170">EXTENSIONPARAMETER <IMachineExtension>: Describes a Machine Extension.</span></span>
  - <span data-ttu-id="ed768-171">`Location <String>`: posizione geografica in cui si trova la risorsa</span><span class="sxs-lookup"><span data-stu-id="ed768-171">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="ed768-172">`[Tag <ITrackedResourceTags>]`: tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="ed768-172">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="ed768-173">`[(Any) <String>]`: indica che è possibile aggiungere qualsiasi proprietà all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ed768-173">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="ed768-174">`[AutoUpgradeMinorVersion <Boolean?>]`: indica se l'estensione deve usare una versione secondaria più recente, se disponibile al momento della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="ed768-174">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="ed768-175">Una volta distribuita, tuttavia, l'estensione non aggiorna le versioni secondarie a meno che non venga ridistribuito, anche con questa proprietà impostata su true.</span><span class="sxs-lookup"><span data-stu-id="ed768-175">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="ed768-176">`[ForceUpdateTag <String>]`: come deve essere forzato l'aggiornamento del gestore delle estensioni anche se la configurazione dell'estensione non è cambiata.</span><span class="sxs-lookup"><span data-stu-id="ed768-176">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="ed768-177">`[MachineExtensionType <String>]`: specifica il tipo dell'estensione; un esempio è "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="ed768-177">`[MachineExtensionType <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="ed768-178">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: l'estensione può contenere protectedSettings o protectedSettingsFromKeyVault o nessuna impostazione protetta.</span><span class="sxs-lookup"><span data-stu-id="ed768-178">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="ed768-179">`[Publisher <String>]`: nome dell'autore del gestore estensioni.</span><span class="sxs-lookup"><span data-stu-id="ed768-179">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="ed768-180">`[Setting <IMachineExtensionPropertiesSettings>]`: impostazioni pubbliche in formato Json per l'estensione.</span><span class="sxs-lookup"><span data-stu-id="ed768-180">`[Setting <IMachineExtensionPropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="ed768-181">`[TypeHandlerVersion <String>]`: specifica la versione del gestore di script.</span><span class="sxs-lookup"><span data-stu-id="ed768-181">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

## <span data-ttu-id="ed768-182">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ed768-182">RELATED LINKS</span></span>

