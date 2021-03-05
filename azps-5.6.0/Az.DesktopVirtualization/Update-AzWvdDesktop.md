---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/update-azwvddesktop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdDesktop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdDesktop.md
ms.openlocfilehash: fbc61ec485be94eacb0267a9698a861f962c61a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001597"
---
# <span data-ttu-id="3bcc3-101">Update-AzWvdDesktop</span><span class="sxs-lookup"><span data-stu-id="3bcc3-101">Update-AzWvdDesktop</span></span>

## <span data-ttu-id="3bcc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3bcc3-102">SYNOPSIS</span></span>
<span data-ttu-id="3bcc3-103">Aggiornare un desktop.</span><span class="sxs-lookup"><span data-stu-id="3bcc3-103">Update a desktop.</span></span>

## <span data-ttu-id="3bcc3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3bcc3-104">SYNTAX</span></span>

### <span data-ttu-id="3bcc3-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3bcc3-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdDesktop -ApplicationGroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3bcc3-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="3bcc3-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdDesktop -InputObject <IDesktopVirtualizationIdentity> [-Description <String>]
 [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="3bcc3-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3bcc3-107">DESCRIPTION</span></span>
<span data-ttu-id="3bcc3-108">Aggiornare un desktop.</span><span class="sxs-lookup"><span data-stu-id="3bcc3-108">Update a desktop.</span></span>

## <span data-ttu-id="3bcc3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3bcc3-109">EXAMPLES</span></span>

### <span data-ttu-id="3bcc3-110">Esempio 1: Aggiornare un desktop virtuale di Windows</span><span class="sxs-lookup"><span data-stu-id="3bcc3-110">Example 1: Update a Windows Virtual Desktop Desktop</span></span>
```powershell
PS C:\> Update-AzWvdDesktop -ResourceGroupName ResourceGroupName `
                             -GroupName ApplicationGroupName `
                             -Name DesktopName `
                             -FriendlyName 'Friendly name' `
                             -Description 'Description' `

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="3bcc3-111">Questo comando aggiorna un Desktop virtuale di Windows in un gruppo applicato.</span><span class="sxs-lookup"><span data-stu-id="3bcc3-111">This command updates a Windows Virtual Desktop Desktop in an applicaton Group.</span></span>

## <span data-ttu-id="3bcc3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3bcc3-112">PARAMETERS</span></span>

### <span data-ttu-id="3bcc3-113">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="3bcc3-113">-ApplicationGroupName</span></span>
<span data-ttu-id="3bcc3-114">Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="3bcc3-114">The name of the application group</span></span>

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

### <span data-ttu-id="3bcc3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bcc3-115">-DefaultProfile</span></span>
<span data-ttu-id="3bcc3-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3bcc3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bcc3-117">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="3bcc3-117">-Description</span></span>
<span data-ttu-id="3bcc3-118">Descrizione del desktop.</span><span class="sxs-lookup"><span data-stu-id="3bcc3-118">Description of Desktop.</span></span>

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

### <span data-ttu-id="3bcc3-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="3bcc3-119">-FriendlyName</span></span>
<span data-ttu-id="3bcc3-120">Nome descrittivo del desktop.</span><span class="sxs-lookup"><span data-stu-id="3bcc3-120">Friendly name of Desktop.</span></span>

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

### <span data-ttu-id="3bcc3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3bcc3-121">-InputObject</span></span>
<span data-ttu-id="3bcc3-122">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="3bcc3-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3bcc3-123">-Name</span><span class="sxs-lookup"><span data-stu-id="3bcc3-123">-Name</span></span>
<span data-ttu-id="3bcc3-124">Nome del desktop all'interno del gruppo di desktop specificato</span><span class="sxs-lookup"><span data-stu-id="3bcc3-124">The name of the desktop within the specified desktop group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DesktopName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bcc3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bcc3-125">-ResourceGroupName</span></span>
<span data-ttu-id="3bcc3-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3bcc3-126">The name of the resource group.</span></span>
<span data-ttu-id="3bcc3-127">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="3bcc3-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="3bcc3-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3bcc3-128">-SubscriptionId</span></span>
<span data-ttu-id="3bcc3-129">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3bcc3-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="3bcc3-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="3bcc3-130">-Tag</span></span>
<span data-ttu-id="3bcc3-131">Tag da aggiornare</span><span class="sxs-lookup"><span data-stu-id="3bcc3-131">tags to be updated</span></span>

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

### <span data-ttu-id="3bcc3-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3bcc3-132">-Confirm</span></span>
<span data-ttu-id="3bcc3-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bcc3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bcc3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bcc3-134">-WhatIf</span></span>
<span data-ttu-id="3bcc3-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3bcc3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bcc3-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3bcc3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bcc3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bcc3-137">CommonParameters</span></span>
<span data-ttu-id="3bcc3-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bcc3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bcc3-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3bcc3-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bcc3-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="3bcc3-140">INPUTS</span></span>

### <span data-ttu-id="3bcc3-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="3bcc3-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="3bcc3-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3bcc3-142">OUTPUTS</span></span>

### <span data-ttu-id="3bcc3-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktop</span><span class="sxs-lookup"><span data-stu-id="3bcc3-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktop</span></span>

## <span data-ttu-id="3bcc3-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="3bcc3-144">NOTES</span></span>

<span data-ttu-id="3bcc3-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="3bcc3-145">ALIASES</span></span>

<span data-ttu-id="3bcc3-146">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="3bcc3-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3bcc3-147">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="3bcc3-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3bcc3-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3bcc3-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3bcc3-149">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="3bcc3-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3bcc3-150">`[ApplicationGroupName <String>]`: nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="3bcc3-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="3bcc3-151">`[ApplicationName <String>]`: nome dell'applicazione all'interno del gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="3bcc3-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="3bcc3-152">`[DesktopName <String>]`: nome del desktop all'interno del gruppo di desktop specificato</span><span class="sxs-lookup"><span data-stu-id="3bcc3-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="3bcc3-153">`[HostPoolName <String>]`: nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="3bcc3-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="3bcc3-154">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="3bcc3-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3bcc3-155">`[MsixPackageFullName <String>]`: nome completo del pacchetto specifico della versione del pacchetto MSIX all'interno dello pool host specificato</span><span class="sxs-lookup"><span data-stu-id="3bcc3-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="3bcc3-156">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3bcc3-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="3bcc3-157">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="3bcc3-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="3bcc3-158">`[SessionHostName <String>]`: nome dell'host di sessione all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="3bcc3-158">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="3bcc3-159">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3bcc3-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="3bcc3-160">`[UserSessionId <String>]`: nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="3bcc3-160">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="3bcc3-161">`[WorkspaceName <String>]`: nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="3bcc3-161">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="3bcc3-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3bcc3-162">RELATED LINKS</span></span>

