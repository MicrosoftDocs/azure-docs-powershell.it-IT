---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
ms.openlocfilehash: 8c2026e7ef8ed5c0eeb1e5a4cb7f605c1a030b9e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200950"
---
# <span data-ttu-id="b2bf3-101">Update-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="b2bf3-101">Update-AzWvdApplication</span></span>

## <span data-ttu-id="b2bf3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b2bf3-102">SYNOPSIS</span></span>
<span data-ttu-id="b2bf3-103">Aggiornare un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b2bf3-103">Update an application.</span></span>

## <span data-ttu-id="b2bf3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b2bf3-104">SYNTAX</span></span>

### <span data-ttu-id="b2bf3-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b2bf3-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-CommandLineArgument <String>] [-CommandLineSetting <CommandLineSetting>]
 [-Description <String>] [-FilePath <String>] [-FriendlyName <String>] [-IconIndex <Int32>]
 [-IconPath <String>] [-ShowInPortal] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="b2bf3-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b2bf3-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity> [-CommandLineArgument <String>]
 [-CommandLineSetting <CommandLineSetting>] [-Description <String>] [-FilePath <String>]
 [-FriendlyName <String>] [-IconIndex <Int32>] [-IconPath <String>] [-ShowInPortal] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b2bf3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2bf3-107">DESCRIPTION</span></span>
<span data-ttu-id="b2bf3-108">Aggiornare un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b2bf3-108">Update an application.</span></span>

## <span data-ttu-id="b2bf3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b2bf3-109">EXAMPLES</span></span>

### <span data-ttu-id="b2bf3-110">Esempio 1: aggiornare un'applicazione desktop virtuale di Windows</span><span class="sxs-lookup"><span data-stu-id="b2bf3-110">Example 1: Update a Windows Virtual Desktop Application</span></span>
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

<span data-ttu-id="b2bf3-111">Questo comando aggiorna un'applicazione desktop virtuale di Windows in un gruppo di Applicaton.</span><span class="sxs-lookup"><span data-stu-id="b2bf3-111">This command updates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="b2bf3-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b2bf3-112">PARAMETERS</span></span>

### <span data-ttu-id="b2bf3-113">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="b2bf3-113">-CommandLineArgument</span></span>
<span data-ttu-id="b2bf3-114">Argomenti della riga di comando per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b2bf3-114">Command Line Arguments for Application.</span></span>

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

### <span data-ttu-id="b2bf3-115">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="b2bf3-115">-CommandLineSetting</span></span>
<span data-ttu-id="b2bf3-116">Specifica se l'applicazione pubblicata può essere avviata con gli argomenti della riga di comando forniti dal client, gli argomenti della riga di comando specificati in fase di pubblicazione o nessun argomento della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="b2bf3-116">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

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

### <span data-ttu-id="b2bf3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2bf3-117">-DefaultProfile</span></span>
<span data-ttu-id="b2bf3-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b2bf3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2bf3-119">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2bf3-119">-Description</span></span>
<span data-ttu-id="b2bf3-120">Descrizione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b2bf3-120">Description of Application.</span></span>

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

### <span data-ttu-id="b2bf3-121">-FilePath</span><span class="sxs-lookup"><span data-stu-id="b2bf3-121">-FilePath</span></span>
<span data-ttu-id="b2bf3-122">Specifica un percorso per il file eseguibile per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b2bf3-122">Specifies a path for the executable file for the application.</span></span>

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

### <span data-ttu-id="b2bf3-123">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="b2bf3-123">-FriendlyName</span></span>
<span data-ttu-id="b2bf3-124">Nome descrittivo dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b2bf3-124">Friendly name of Application.</span></span>

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

### <span data-ttu-id="b2bf3-125">-GroupName</span><span class="sxs-lookup"><span data-stu-id="b2bf3-125">-GroupName</span></span>
<span data-ttu-id="b2bf3-126">Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="b2bf3-126">The name of the application group</span></span>

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

### <span data-ttu-id="b2bf3-127">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="b2bf3-127">-IconIndex</span></span>
<span data-ttu-id="b2bf3-128">Indice dell'icona.</span><span class="sxs-lookup"><span data-stu-id="b2bf3-128">Index of the icon.</span></span>

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

### <span data-ttu-id="b2bf3-129">-IconPath</span><span class="sxs-lookup"><span data-stu-id="b2bf3-129">-IconPath</span></span>
<span data-ttu-id="b2bf3-130">Percorso dell'icona.</span><span class="sxs-lookup"><span data-stu-id="b2bf3-130">Path to icon.</span></span>

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

### <span data-ttu-id="b2bf3-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b2bf3-131">-InputObject</span></span>
<span data-ttu-id="b2bf3-132">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="b2bf3-132">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b2bf3-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="b2bf3-133">-Name</span></span>
<span data-ttu-id="b2bf3-134">Nome dell'applicazione nel gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="b2bf3-134">The name of the application within the specified application group</span></span>

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

### <span data-ttu-id="b2bf3-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2bf3-135">-ResourceGroupName</span></span>
<span data-ttu-id="b2bf3-136">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b2bf3-136">The name of the resource group.</span></span>
<span data-ttu-id="b2bf3-137">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="b2bf3-137">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b2bf3-138">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="b2bf3-138">-ShowInPortal</span></span>
<span data-ttu-id="b2bf3-139">Specifica se visualizzare il programma RemoteApp nel server di accesso Web Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="b2bf3-139">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="b2bf3-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b2bf3-140">-SubscriptionId</span></span>
<span data-ttu-id="b2bf3-141">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b2bf3-141">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b2bf3-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="b2bf3-142">-Tag</span></span>
<span data-ttu-id="b2bf3-143">Tag da aggiornare</span><span class="sxs-lookup"><span data-stu-id="b2bf3-143">tags to be updated</span></span>

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

### <span data-ttu-id="b2bf3-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b2bf3-144">-Confirm</span></span>
<span data-ttu-id="b2bf3-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2bf3-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2bf3-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2bf3-146">-WhatIf</span></span>
<span data-ttu-id="b2bf3-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b2bf3-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2bf3-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b2bf3-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2bf3-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2bf3-149">CommonParameters</span></span>
<span data-ttu-id="b2bf3-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2bf3-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2bf3-151">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2bf3-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2bf3-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b2bf3-152">INPUTS</span></span>

### <span data-ttu-id="b2bf3-153">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="b2bf3-153">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="b2bf3-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b2bf3-154">OUTPUTS</span></span>

### <span data-ttu-id="b2bf3-155">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20191210Preview. IApplication</span><span class="sxs-lookup"><span data-stu-id="b2bf3-155">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplication</span></span>

## <span data-ttu-id="b2bf3-156">Note</span><span class="sxs-lookup"><span data-stu-id="b2bf3-156">NOTES</span></span>

<span data-ttu-id="b2bf3-157">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b2bf3-157">ALIASES</span></span>

<span data-ttu-id="b2bf3-158">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b2bf3-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b2bf3-159">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="b2bf3-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b2bf3-160">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b2bf3-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b2bf3-161">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="b2bf3-161">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b2bf3-162">`[ApplicationGroupName <String>]`: Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="b2bf3-162">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="b2bf3-163">`[ApplicationName <String>]`: Nome dell'applicazione nel gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="b2bf3-163">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="b2bf3-164">`[DesktopName <String>]`: Nome del desktop nel gruppo desktop specificato</span><span class="sxs-lookup"><span data-stu-id="b2bf3-164">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="b2bf3-165">`[HostPoolName <String>]`: Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="b2bf3-165">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="b2bf3-166">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="b2bf3-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b2bf3-167">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b2bf3-167">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b2bf3-168">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="b2bf3-168">The name is case insensitive.</span></span>
  - <span data-ttu-id="b2bf3-169">`[SessionHostName <String>]`: Nome dell'host di sessione nel pool di host specificato</span><span class="sxs-lookup"><span data-stu-id="b2bf3-169">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="b2bf3-170">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b2bf3-170">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b2bf3-171">`[UserSessionId <String>]`: Nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="b2bf3-171">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="b2bf3-172">`[WorkspaceName <String>]`: Nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="b2bf3-172">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="b2bf3-173">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b2bf3-173">RELATED LINKS</span></span>

