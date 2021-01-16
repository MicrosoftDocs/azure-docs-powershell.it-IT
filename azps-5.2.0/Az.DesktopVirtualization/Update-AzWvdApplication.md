---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
ms.openlocfilehash: 6907967acfd86f151b038e26aa9c33f62db50a5a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338407"
---
# <span data-ttu-id="798fb-101">Update-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="798fb-101">Update-AzWvdApplication</span></span>

## <span data-ttu-id="798fb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="798fb-102">SYNOPSIS</span></span>
<span data-ttu-id="798fb-103">Aggiornare un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="798fb-103">Update an application.</span></span>

## <span data-ttu-id="798fb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="798fb-104">SYNTAX</span></span>

### <span data-ttu-id="798fb-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="798fb-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ApplicationType <RemoteApplicationType>] [-CommandLineArgument <String>]
 [-CommandLineSetting <CommandLineSetting>] [-Description <String>] [-FilePath <String>]
 [-FriendlyName <String>] [-IconIndex <Int32>] [-IconPath <String>] [-MsixPackageApplicationId <String>]
 [-MsixPackageFamilyName <String>] [-ShowInPortal] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="798fb-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="798fb-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity>
 [-ApplicationType <RemoteApplicationType>] [-CommandLineArgument <String>]
 [-CommandLineSetting <CommandLineSetting>] [-Description <String>] [-FilePath <String>]
 [-FriendlyName <String>] [-IconIndex <Int32>] [-IconPath <String>] [-MsixPackageApplicationId <String>]
 [-MsixPackageFamilyName <String>] [-ShowInPortal] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="798fb-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="798fb-107">DESCRIPTION</span></span>
<span data-ttu-id="798fb-108">Aggiornare un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="798fb-108">Update an application.</span></span>

## <span data-ttu-id="798fb-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="798fb-109">EXAMPLES</span></span>

### <span data-ttu-id="798fb-110">Esempio 1: aggiornare un'applicazione desktop virtuale di Windows</span><span class="sxs-lookup"><span data-stu-id="798fb-110">Example 1: Update a Windows Virtual Desktop Application</span></span>
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

<span data-ttu-id="798fb-111">Questo comando aggiorna un'applicazione desktop virtuale di Windows in un gruppo di Applicaton.</span><span class="sxs-lookup"><span data-stu-id="798fb-111">This command updates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="798fb-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="798fb-112">PARAMETERS</span></span>

### <span data-ttu-id="798fb-113">-ApplicationType</span><span class="sxs-lookup"><span data-stu-id="798fb-113">-ApplicationType</span></span>
<span data-ttu-id="798fb-114">Tipo di risorsa dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="798fb-114">Resource Type of Application.</span></span>

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

### <span data-ttu-id="798fb-115">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="798fb-115">-CommandLineArgument</span></span>
<span data-ttu-id="798fb-116">Argomenti della riga di comando per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="798fb-116">Command Line Arguments for Application.</span></span>

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

### <span data-ttu-id="798fb-117">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="798fb-117">-CommandLineSetting</span></span>
<span data-ttu-id="798fb-118">Specifica se l'applicazione pubblicata può essere avviata con gli argomenti della riga di comando forniti dal client, gli argomenti della riga di comando specificati in fase di pubblicazione o nessun argomento della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="798fb-118">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

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

### <span data-ttu-id="798fb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="798fb-119">-DefaultProfile</span></span>
<span data-ttu-id="798fb-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="798fb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="798fb-121">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="798fb-121">-Description</span></span>
<span data-ttu-id="798fb-122">Descrizione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="798fb-122">Description of Application.</span></span>

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

### <span data-ttu-id="798fb-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="798fb-123">-FilePath</span></span>
<span data-ttu-id="798fb-124">Specifica un percorso per il file eseguibile per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="798fb-124">Specifies a path for the executable file for the application.</span></span>

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

### <span data-ttu-id="798fb-125">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="798fb-125">-FriendlyName</span></span>
<span data-ttu-id="798fb-126">Nome descrittivo dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="798fb-126">Friendly name of Application.</span></span>

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

### <span data-ttu-id="798fb-127">-GroupName</span><span class="sxs-lookup"><span data-stu-id="798fb-127">-GroupName</span></span>
<span data-ttu-id="798fb-128">Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="798fb-128">The name of the application group</span></span>

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

### <span data-ttu-id="798fb-129">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="798fb-129">-IconIndex</span></span>
<span data-ttu-id="798fb-130">Indice dell'icona.</span><span class="sxs-lookup"><span data-stu-id="798fb-130">Index of the icon.</span></span>

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

### <span data-ttu-id="798fb-131">-IconPath</span><span class="sxs-lookup"><span data-stu-id="798fb-131">-IconPath</span></span>
<span data-ttu-id="798fb-132">Percorso dell'icona.</span><span class="sxs-lookup"><span data-stu-id="798fb-132">Path to icon.</span></span>

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

### <span data-ttu-id="798fb-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="798fb-133">-InputObject</span></span>
<span data-ttu-id="798fb-134">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="798fb-134">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="798fb-135">-MsixPackageApplicationId</span><span class="sxs-lookup"><span data-stu-id="798fb-135">-MsixPackageApplicationId</span></span>
<span data-ttu-id="798fb-136">Specifica l'ID applicazione pacchetto per le applicazioni MSIX</span><span class="sxs-lookup"><span data-stu-id="798fb-136">Specifies the package application Id for MSIX applications</span></span>

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

### <span data-ttu-id="798fb-137">-MsixPackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="798fb-137">-MsixPackageFamilyName</span></span>
<span data-ttu-id="798fb-138">Specifica il nome della famiglia di pacchetti per le applicazioni MSIX</span><span class="sxs-lookup"><span data-stu-id="798fb-138">Specifies the package family name for MSIX applications</span></span>

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

### <span data-ttu-id="798fb-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="798fb-139">-Name</span></span>
<span data-ttu-id="798fb-140">Nome dell'applicazione nel gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="798fb-140">The name of the application within the specified application group</span></span>

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

### <span data-ttu-id="798fb-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="798fb-141">-ResourceGroupName</span></span>
<span data-ttu-id="798fb-142">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="798fb-142">The name of the resource group.</span></span>
<span data-ttu-id="798fb-143">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="798fb-143">The name is case insensitive.</span></span>

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

### <span data-ttu-id="798fb-144">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="798fb-144">-ShowInPortal</span></span>
<span data-ttu-id="798fb-145">Specifica se visualizzare il programma RemoteApp nel server di accesso Web Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="798fb-145">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="798fb-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="798fb-146">-SubscriptionId</span></span>
<span data-ttu-id="798fb-147">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="798fb-147">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="798fb-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="798fb-148">-Tag</span></span>
<span data-ttu-id="798fb-149">Tag da aggiornare</span><span class="sxs-lookup"><span data-stu-id="798fb-149">tags to be updated</span></span>

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

### <span data-ttu-id="798fb-150">-Confermare</span><span class="sxs-lookup"><span data-stu-id="798fb-150">-Confirm</span></span>
<span data-ttu-id="798fb-151">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="798fb-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="798fb-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="798fb-152">-WhatIf</span></span>
<span data-ttu-id="798fb-153">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="798fb-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="798fb-154">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="798fb-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="798fb-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="798fb-155">CommonParameters</span></span>
<span data-ttu-id="798fb-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="798fb-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="798fb-157">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="798fb-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="798fb-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="798fb-158">INPUTS</span></span>

### <span data-ttu-id="798fb-159">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="798fb-159">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="798fb-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="798fb-160">OUTPUTS</span></span>

### <span data-ttu-id="798fb-161">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20201019Preview. IApplication</span><span class="sxs-lookup"><span data-stu-id="798fb-161">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IApplication</span></span>

## <span data-ttu-id="798fb-162">Note</span><span class="sxs-lookup"><span data-stu-id="798fb-162">NOTES</span></span>

<span data-ttu-id="798fb-163">ALIAS</span><span class="sxs-lookup"><span data-stu-id="798fb-163">ALIASES</span></span>

<span data-ttu-id="798fb-164">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="798fb-164">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="798fb-165">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="798fb-165">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="798fb-166">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="798fb-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="798fb-167">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="798fb-167">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="798fb-168">`[ApplicationGroupName <String>]`: Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="798fb-168">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="798fb-169">`[ApplicationName <String>]`: Nome dell'applicazione nel gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="798fb-169">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="798fb-170">`[DesktopName <String>]`: Nome del desktop nel gruppo desktop specificato</span><span class="sxs-lookup"><span data-stu-id="798fb-170">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="798fb-171">`[HostPoolName <String>]`: Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="798fb-171">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="798fb-172">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="798fb-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="798fb-173">`[MsixPackageFullName <String>]`: Pacchetto specifico della versione nome completo del pacchetto MSIX all'interno di hostpool specificato</span><span class="sxs-lookup"><span data-stu-id="798fb-173">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="798fb-174">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="798fb-174">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="798fb-175">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="798fb-175">The name is case insensitive.</span></span>
  - <span data-ttu-id="798fb-176">`[SessionHostName <String>]`: Nome dell'host di sessione nel pool di host specificato</span><span class="sxs-lookup"><span data-stu-id="798fb-176">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="798fb-177">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="798fb-177">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="798fb-178">`[UserSessionId <String>]`: Nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="798fb-178">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="798fb-179">`[WorkspaceName <String>]`: Nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="798fb-179">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="798fb-180">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="798fb-180">RELATED LINKS</span></span>

