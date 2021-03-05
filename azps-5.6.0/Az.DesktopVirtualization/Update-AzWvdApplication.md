---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/update-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
ms.openlocfilehash: 8770b9e3b07b677f0f4bd4f59a6c38928421523e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001614"
---
# <span data-ttu-id="dee5e-101">Update-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="dee5e-101">Update-AzWvdApplication</span></span>

## <span data-ttu-id="dee5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dee5e-102">SYNOPSIS</span></span>
<span data-ttu-id="dee5e-103">Aggiornare un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="dee5e-103">Update an application.</span></span>

## <span data-ttu-id="dee5e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dee5e-104">SYNTAX</span></span>

### <span data-ttu-id="dee5e-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dee5e-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ApplicationType <RemoteApplicationType>] [-CommandLineArgument <String>]
 [-CommandLineSetting <CommandLineSetting>] [-Description <String>] [-FilePath <String>]
 [-FriendlyName <String>] [-IconIndex <Int32>] [-IconPath <String>] [-MsixPackageApplicationId <String>]
 [-MsixPackageFamilyName <String>] [-ShowInPortal] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="dee5e-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="dee5e-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity>
 [-ApplicationType <RemoteApplicationType>] [-CommandLineArgument <String>]
 [-CommandLineSetting <CommandLineSetting>] [-Description <String>] [-FilePath <String>]
 [-FriendlyName <String>] [-IconIndex <Int32>] [-IconPath <String>] [-MsixPackageApplicationId <String>]
 [-MsixPackageFamilyName <String>] [-ShowInPortal] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dee5e-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="dee5e-107">DESCRIPTION</span></span>
<span data-ttu-id="dee5e-108">Aggiornare un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="dee5e-108">Update an application.</span></span>

## <span data-ttu-id="dee5e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dee5e-109">EXAMPLES</span></span>

### <span data-ttu-id="dee5e-110">Esempio 1: Aggiornare un'applicazione Desktop virtuale di Windows</span><span class="sxs-lookup"><span data-stu-id="dee5e-110">Example 1: Update a Windows Virtual Desktop Application</span></span>
```powershell
PS C:\> Update-AzWvdApplication -ResourceGroupName ResourceGroupName `
                             -GroupName ApplicationGroupName `
                             -Name ApplicationName `
                             -FilePath 'C:\windows\system32\mspaint.exe' `
                             -FriendlyName 'Friendly name' `
                             -Description 'Description' `
                             -IconIndex 0 `
                             -IconPath 'C:\windows\system32\mspaint.exe' `
                             -CommandLineSetting 'Allow' `
                             -ShowInPortal:$true

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="dee5e-111">Questo comando aggiorna un'applicazione Desktop virtuale di Windows in un gruppo applicato.</span><span class="sxs-lookup"><span data-stu-id="dee5e-111">This command updates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="dee5e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dee5e-112">PARAMETERS</span></span>

### <span data-ttu-id="dee5e-113">-ApplicationType</span><span class="sxs-lookup"><span data-stu-id="dee5e-113">-ApplicationType</span></span>
<span data-ttu-id="dee5e-114">Tipo di risorsa dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="dee5e-114">Resource Type of Application.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.RemoteApplicationType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dee5e-115">-CommandLine Argument</span><span class="sxs-lookup"><span data-stu-id="dee5e-115">-CommandLineArgument</span></span>
<span data-ttu-id="dee5e-116">Argomenti della riga di comando per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="dee5e-116">Command Line Arguments for Application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dee5e-117">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="dee5e-117">-CommandLineSetting</span></span>
<span data-ttu-id="dee5e-118">Specifica se l'applicazione pubblicata può essere avviata con argomenti della riga di comando forniti dal client, argomenti della riga di comando specificati al momento della pubblicazione o nessun argomento della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="dee5e-118">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.CommandLineSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dee5e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dee5e-119">-DefaultProfile</span></span>
<span data-ttu-id="dee5e-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dee5e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dee5e-121">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="dee5e-121">-Description</span></span>
<span data-ttu-id="dee5e-122">Descrizione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="dee5e-122">Description of Application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dee5e-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="dee5e-123">-FilePath</span></span>
<span data-ttu-id="dee5e-124">Specifica un percorso per il file eseguibile per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="dee5e-124">Specifies a path for the executable file for the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dee5e-125">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="dee5e-125">-FriendlyName</span></span>
<span data-ttu-id="dee5e-126">Nome descrittivo dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="dee5e-126">Friendly name of Application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dee5e-127">-GroupName</span><span class="sxs-lookup"><span data-stu-id="dee5e-127">-GroupName</span></span>
<span data-ttu-id="dee5e-128">Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="dee5e-128">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dee5e-129">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="dee5e-129">-IconIndex</span></span>
<span data-ttu-id="dee5e-130">Indice dell'icona.</span><span class="sxs-lookup"><span data-stu-id="dee5e-130">Index of the icon.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dee5e-131">-IconPath</span><span class="sxs-lookup"><span data-stu-id="dee5e-131">-IconPath</span></span>
<span data-ttu-id="dee5e-132">Path to icon.</span><span class="sxs-lookup"><span data-stu-id="dee5e-132">Path to icon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dee5e-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dee5e-133">-InputObject</span></span>
<span data-ttu-id="dee5e-134">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="dee5e-134">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dee5e-135">-MsixPackageApplicationId</span><span class="sxs-lookup"><span data-stu-id="dee5e-135">-MsixPackageApplicationId</span></span>
<span data-ttu-id="dee5e-136">Specifica l'ID applicazione del pacchetto per le applicazioni MSIX</span><span class="sxs-lookup"><span data-stu-id="dee5e-136">Specifies the package application Id for MSIX applications</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dee5e-137">-MsixPackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="dee5e-137">-MsixPackageFamilyName</span></span>
<span data-ttu-id="dee5e-138">Specifica il nome della famiglia di pacchetti per le applicazioni MSIX</span><span class="sxs-lookup"><span data-stu-id="dee5e-138">Specifies the package family name for MSIX applications</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dee5e-139">-Name</span><span class="sxs-lookup"><span data-stu-id="dee5e-139">-Name</span></span>
<span data-ttu-id="dee5e-140">Nome dell'applicazione all'interno del gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="dee5e-140">The name of the application within the specified application group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dee5e-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dee5e-141">-ResourceGroupName</span></span>
<span data-ttu-id="dee5e-142">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dee5e-142">The name of the resource group.</span></span>
<span data-ttu-id="dee5e-143">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="dee5e-143">The name is case insensitive.</span></span>

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

### <span data-ttu-id="dee5e-144">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="dee5e-144">-ShowInPortal</span></span>
<span data-ttu-id="dee5e-145">Specifica se visualizzare il programma RemoteApp nel server Accesso Web Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="dee5e-145">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="dee5e-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dee5e-146">-SubscriptionId</span></span>
<span data-ttu-id="dee5e-147">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="dee5e-147">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dee5e-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="dee5e-148">-Tag</span></span>
<span data-ttu-id="dee5e-149">Tag da aggiornare</span><span class="sxs-lookup"><span data-stu-id="dee5e-149">tags to be updated</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dee5e-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dee5e-150">-Confirm</span></span>
<span data-ttu-id="dee5e-151">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dee5e-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dee5e-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dee5e-152">-WhatIf</span></span>
<span data-ttu-id="dee5e-153">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dee5e-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dee5e-154">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dee5e-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dee5e-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dee5e-155">CommonParameters</span></span>
<span data-ttu-id="dee5e-156">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dee5e-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dee5e-157">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="dee5e-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dee5e-158">INPUT</span><span class="sxs-lookup"><span data-stu-id="dee5e-158">INPUTS</span></span>

### <span data-ttu-id="dee5e-159">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="dee5e-159">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="dee5e-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dee5e-160">OUTPUTS</span></span>

### <span data-ttu-id="dee5e-161">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span><span class="sxs-lookup"><span data-stu-id="dee5e-161">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span></span>

## <span data-ttu-id="dee5e-162">NOTE</span><span class="sxs-lookup"><span data-stu-id="dee5e-162">NOTES</span></span>

<span data-ttu-id="dee5e-163">ALIAS</span><span class="sxs-lookup"><span data-stu-id="dee5e-163">ALIASES</span></span>

<span data-ttu-id="dee5e-164">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="dee5e-164">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dee5e-165">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="dee5e-165">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dee5e-166">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dee5e-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dee5e-167">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="dee5e-167">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dee5e-168">`[ApplicationGroupName <String>]`: nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="dee5e-168">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="dee5e-169">`[ApplicationName <String>]`: nome dell'applicazione all'interno del gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="dee5e-169">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="dee5e-170">`[DesktopName <String>]`: nome del desktop all'interno del gruppo di desktop specificato</span><span class="sxs-lookup"><span data-stu-id="dee5e-170">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="dee5e-171">`[HostPoolName <String>]`: nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="dee5e-171">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="dee5e-172">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="dee5e-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dee5e-173">`[MsixPackageFullName <String>]`: nome completo del pacchetto specifico della versione del pacchetto MSIX all'interno dello pool host specificato</span><span class="sxs-lookup"><span data-stu-id="dee5e-173">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="dee5e-174">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dee5e-174">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="dee5e-175">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="dee5e-175">The name is case insensitive.</span></span>
  - <span data-ttu-id="dee5e-176">`[SessionHostName <String>]`: nome dell'host di sessione all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="dee5e-176">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="dee5e-177">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="dee5e-177">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="dee5e-178">`[UserSessionId <String>]`: nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="dee5e-178">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="dee5e-179">`[WorkspaceName <String>]`: nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="dee5e-179">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="dee5e-180">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dee5e-180">RELATED LINKS</span></span>

