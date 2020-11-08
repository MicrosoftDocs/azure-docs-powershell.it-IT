---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/set-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Set-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Set-AzConnectedMachineExtension.md
ms.openlocfilehash: b136f5194bdc7e0f4b4dfc969564d7ef8476d9bf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202194"
---
# <span data-ttu-id="57b6c-101">Set-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="57b6c-101">Set-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="57b6c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="57b6c-102">SYNOPSIS</span></span>
<span data-ttu-id="57b6c-103">Operazione per creare o aggiornare l'estensione.</span><span class="sxs-lookup"><span data-stu-id="57b6c-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="57b6c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="57b6c-104">SYNTAX</span></span>

### <span data-ttu-id="57b6c-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="57b6c-105">UpdateExpanded (Default)</span></span>
```
Set-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -Location <String> [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ExtensionType <String>]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="57b6c-106">Aggiornamento</span><span class="sxs-lookup"><span data-stu-id="57b6c-106">Update</span></span>
```
Set-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtension> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="57b6c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="57b6c-107">DESCRIPTION</span></span>
<span data-ttu-id="57b6c-108">Operazione per creare o aggiornare l'estensione.</span><span class="sxs-lookup"><span data-stu-id="57b6c-108">The operation to create or update the extension.</span></span>

## <span data-ttu-id="57b6c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="57b6c-109">EXAMPLES</span></span>

### <span data-ttu-id="57b6c-110">Esempio 1: impostare un'estensione in un computer</span><span class="sxs-lookup"><span data-stu-id="57b6c-110">Example 1: Set an extension on a machine</span></span>
```powershell
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> Set-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName win-eastus1 -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="57b6c-111">Imposta un'estensione in un computer.</span><span class="sxs-lookup"><span data-stu-id="57b6c-111">Sets an extension on a machine.</span></span>

### <span data-ttu-id="57b6c-112">Esempio 2: impostare un'estensione con i parametri di estensione specificati tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="57b6c-112">Example 2: Set an extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $otherExtension = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $otherExtension | Set-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName important

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="57b6c-113">In questo modo viene impostata un'estensione con i parametri di estensione forniti dall'oggetto passato tramite la pipeline.</span><span class="sxs-lookup"><span data-stu-id="57b6c-113">This sets an extension with the extension parameters provided by the object passed in via the pipeline.</span></span>
<span data-ttu-id="57b6c-114">Questa operazione è utile se si vuole afferrare i parametri di un computer e applicarlo a un altro computer.</span><span class="sxs-lookup"><span data-stu-id="57b6c-114">This is great if you want to grab the parameters of one machine and apply it to another machine.</span></span>

## <span data-ttu-id="57b6c-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="57b6c-115">PARAMETERS</span></span>

### <span data-ttu-id="57b6c-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="57b6c-116">-AsJob</span></span>
<span data-ttu-id="57b6c-117">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="57b6c-117">Run the command as a job</span></span>

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

### <span data-ttu-id="57b6c-118">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="57b6c-118">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="57b6c-119">Indica se l'estensione deve usare una versione secondaria più recente, se disponibile in fase di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="57b6c-119">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="57b6c-120">Una volta distribuita, tuttavia, l'estensione non aggiornerà le versioni secondarie, a meno che non vengano ridistribuite, anche se questa proprietà è impostata su true.</span><span class="sxs-lookup"><span data-stu-id="57b6c-120">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

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

### <span data-ttu-id="57b6c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57b6c-121">-DefaultProfile</span></span>
<span data-ttu-id="57b6c-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="57b6c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57b6c-123">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="57b6c-123">-ExtensionParameter</span></span>
<span data-ttu-id="57b6c-124">Descrive un'estensione del computer.</span><span class="sxs-lookup"><span data-stu-id="57b6c-124">Describes a Machine Extension.</span></span>
<span data-ttu-id="57b6c-125">Per costruire, vedere la sezione Note per le proprietà di EXTENSIONPARAMETER e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="57b6c-125">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="57b6c-126">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="57b6c-126">-ExtensionType</span></span>
<span data-ttu-id="57b6c-127">Specifica il tipo di estensione; un esempio è "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="57b6c-127">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

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

### <span data-ttu-id="57b6c-128">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="57b6c-128">-ForceRerun</span></span>
<span data-ttu-id="57b6c-129">Come il gestore dell'estensione deve essere costretto ad aggiornare anche se la configurazione dell'estensione non è cambiata.</span><span class="sxs-lookup"><span data-stu-id="57b6c-129">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="57b6c-130">-Posizione</span><span class="sxs-lookup"><span data-stu-id="57b6c-130">-Location</span></span>
<span data-ttu-id="57b6c-131">Posizione geografica in cui vive la risorsa</span><span class="sxs-lookup"><span data-stu-id="57b6c-131">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="57b6c-132">-MachineName</span><span class="sxs-lookup"><span data-stu-id="57b6c-132">-MachineName</span></span>
<span data-ttu-id="57b6c-133">Il nome del computer in cui deve essere creata o aggiornata l'estensione.</span><span class="sxs-lookup"><span data-stu-id="57b6c-133">The name of the machine where the extension should be created or updated.</span></span>

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

### <span data-ttu-id="57b6c-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="57b6c-134">-Name</span></span>
<span data-ttu-id="57b6c-135">Nome dell'estensione del computer.</span><span class="sxs-lookup"><span data-stu-id="57b6c-135">The name of the machine extension.</span></span>

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

### <span data-ttu-id="57b6c-136">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="57b6c-136">-NoWait</span></span>
<span data-ttu-id="57b6c-137">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="57b6c-137">Run the command asynchronously</span></span>

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

### <span data-ttu-id="57b6c-138">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="57b6c-138">-ProtectedSetting</span></span>
<span data-ttu-id="57b6c-139">L'estensione può contenere protectedSettings o protectedSettingsFromKeyVault o nessuna impostazione protetta.</span><span class="sxs-lookup"><span data-stu-id="57b6c-139">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

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

### <span data-ttu-id="57b6c-140">-Publisher</span><span class="sxs-lookup"><span data-stu-id="57b6c-140">-Publisher</span></span>
<span data-ttu-id="57b6c-141">Nome dell'autore del gestore di estensione.</span><span class="sxs-lookup"><span data-stu-id="57b6c-141">The name of the extension handler publisher.</span></span>

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

### <span data-ttu-id="57b6c-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57b6c-142">-ResourceGroupName</span></span>
<span data-ttu-id="57b6c-143">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="57b6c-143">The name of the resource group.</span></span>

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

### <span data-ttu-id="57b6c-144">-Impostazione</span><span class="sxs-lookup"><span data-stu-id="57b6c-144">-Setting</span></span>
<span data-ttu-id="57b6c-145">Impostazioni pubbliche in formato JSON per l'estensione.</span><span class="sxs-lookup"><span data-stu-id="57b6c-145">Json formatted public settings for the extension.</span></span>

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

### <span data-ttu-id="57b6c-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="57b6c-146">-SubscriptionId</span></span>
<span data-ttu-id="57b6c-147">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="57b6c-147">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="57b6c-148">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="57b6c-148">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="57b6c-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="57b6c-149">-Tag</span></span>
<span data-ttu-id="57b6c-150">Tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="57b6c-150">Resource tags.</span></span>

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

### <span data-ttu-id="57b6c-151">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="57b6c-151">-TypeHandlerVersion</span></span>
<span data-ttu-id="57b6c-152">Specifica la versione del gestore di script.</span><span class="sxs-lookup"><span data-stu-id="57b6c-152">Specifies the version of the script handler.</span></span>

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

### <span data-ttu-id="57b6c-153">-Confermare</span><span class="sxs-lookup"><span data-stu-id="57b6c-153">-Confirm</span></span>
<span data-ttu-id="57b6c-154">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57b6c-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57b6c-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57b6c-155">-WhatIf</span></span>
<span data-ttu-id="57b6c-156">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="57b6c-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57b6c-157">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="57b6c-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57b6c-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57b6c-158">CommonParameters</span></span>
<span data-ttu-id="57b6c-159">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57b6c-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57b6c-160">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="57b6c-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57b6c-161">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="57b6c-161">INPUTS</span></span>

### <span data-ttu-id="57b6c-162">Microsoft. Azure. PowerShell. Cmdlets. ConnectedMachine. Models. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="57b6c-162">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="57b6c-163">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="57b6c-163">OUTPUTS</span></span>

### <span data-ttu-id="57b6c-164">Microsoft. Azure. PowerShell. Cmdlets. ConnectedMachine. Models. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="57b6c-164">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="57b6c-165">Note</span><span class="sxs-lookup"><span data-stu-id="57b6c-165">NOTES</span></span>

<span data-ttu-id="57b6c-166">ALIAS</span><span class="sxs-lookup"><span data-stu-id="57b6c-166">ALIASES</span></span>

<span data-ttu-id="57b6c-167">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="57b6c-167">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="57b6c-168">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="57b6c-168">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="57b6c-169">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="57b6c-169">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="57b6c-170">EXTENSIONPARAMETER <IMachineExtension> : descrive un'estensione del computer.</span><span class="sxs-lookup"><span data-stu-id="57b6c-170">EXTENSIONPARAMETER <IMachineExtension>: Describes a Machine Extension.</span></span>
  - <span data-ttu-id="57b6c-171">`Location <String>`: La posizione geografica in cui vive la risorsa</span><span class="sxs-lookup"><span data-stu-id="57b6c-171">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="57b6c-172">`[Tag <ITrackedResourceTags>]`: Tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="57b6c-172">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="57b6c-173">`[(Any) <String>]`: Indica che qualsiasi proprietà può essere aggiunta a questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="57b6c-173">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="57b6c-174">`[AutoUpgradeMinorVersion <Boolean?>]`: Indica se l'estensione deve usare una versione secondaria più recente, se disponibile al momento della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="57b6c-174">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="57b6c-175">Una volta distribuita, tuttavia, l'estensione non aggiornerà le versioni secondarie, a meno che non vengano ridistribuite, anche se questa proprietà è impostata su true.</span><span class="sxs-lookup"><span data-stu-id="57b6c-175">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="57b6c-176">`[ForceUpdateTag <String>]`: Come deve essere forzata l'aggiornamento del gestore dell'estensione anche se la configurazione dell'estensione non è cambiata.</span><span class="sxs-lookup"><span data-stu-id="57b6c-176">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="57b6c-177">`[MachineExtensionType <String>]`: Specifica il tipo di estensione; un esempio è "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="57b6c-177">`[MachineExtensionType <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="57b6c-178">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: L'estensione può contenere protectedSettings o protectedSettingsFromKeyVault o nessuna impostazione protetta.</span><span class="sxs-lookup"><span data-stu-id="57b6c-178">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="57b6c-179">`[Publisher <String>]`: Nome dell'editore del gestore di estensione.</span><span class="sxs-lookup"><span data-stu-id="57b6c-179">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="57b6c-180">`[Setting <IMachineExtensionPropertiesSettings>]`: Le impostazioni pubbliche formattate JSON per l'estensione.</span><span class="sxs-lookup"><span data-stu-id="57b6c-180">`[Setting <IMachineExtensionPropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="57b6c-181">`[TypeHandlerVersion <String>]`: Specifica la versione del gestore script.</span><span class="sxs-lookup"><span data-stu-id="57b6c-181">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

## <span data-ttu-id="57b6c-182">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="57b6c-182">RELATED LINKS</span></span>

