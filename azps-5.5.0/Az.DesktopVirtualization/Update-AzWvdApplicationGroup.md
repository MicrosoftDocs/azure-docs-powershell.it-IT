---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplicationGroup.md
ms.openlocfilehash: b03fe0c62a446c9ed54c9330708f29737e18bd59
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188550"
---
# <span data-ttu-id="51a94-101">Update-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="51a94-101">Update-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="51a94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51a94-102">SYNOPSIS</span></span>
<span data-ttu-id="51a94-103">Aggiornare un applicationGroup.</span><span class="sxs-lookup"><span data-stu-id="51a94-103">Update an applicationGroup.</span></span>

## <span data-ttu-id="51a94-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="51a94-104">SYNTAX</span></span>

### <span data-ttu-id="51a94-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="51a94-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="51a94-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="51a94-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-Description <String>]
 [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="51a94-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="51a94-107">DESCRIPTION</span></span>
<span data-ttu-id="51a94-108">Aggiornare un applicationGroup.</span><span class="sxs-lookup"><span data-stu-id="51a94-108">Update an applicationGroup.</span></span>

## <span data-ttu-id="51a94-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="51a94-109">EXAMPLES</span></span>

### <span data-ttu-id="51a94-110">Esempio 1: Creare un gruppo applicazioni desktop virtuale di Windows in base al nome</span><span class="sxs-lookup"><span data-stu-id="51a94-110">Example 1: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> New-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                            -Name ApplicationGroupName `
                            -FriendlyName 'Friendly Name' `
                            -Description 'Description' `

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="51a94-111">Questo comando crea un Gruppo Applicazioni Desktop virtuale Windows in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="51a94-111">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="51a94-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="51a94-112">PARAMETERS</span></span>

### <span data-ttu-id="51a94-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51a94-113">-DefaultProfile</span></span>
<span data-ttu-id="51a94-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="51a94-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51a94-115">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="51a94-115">-Description</span></span>
<span data-ttu-id="51a94-116">Descrizione di ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="51a94-116">Description of ApplicationGroup.</span></span>

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

### <span data-ttu-id="51a94-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="51a94-117">-FriendlyName</span></span>
<span data-ttu-id="51a94-118">Nome descrittivo di ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="51a94-118">Friendly name of ApplicationGroup.</span></span>

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

### <span data-ttu-id="51a94-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51a94-119">-InputObject</span></span>
<span data-ttu-id="51a94-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="51a94-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="51a94-121">-Name</span><span class="sxs-lookup"><span data-stu-id="51a94-121">-Name</span></span>
<span data-ttu-id="51a94-122">Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="51a94-122">The name of the application group</span></span>

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

### <span data-ttu-id="51a94-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51a94-123">-ResourceGroupName</span></span>
<span data-ttu-id="51a94-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="51a94-124">The name of the resource group.</span></span>
<span data-ttu-id="51a94-125">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="51a94-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="51a94-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="51a94-126">-SubscriptionId</span></span>
<span data-ttu-id="51a94-127">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="51a94-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="51a94-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="51a94-128">-Tag</span></span>
<span data-ttu-id="51a94-129">Tag da aggiornare</span><span class="sxs-lookup"><span data-stu-id="51a94-129">tags to be updated</span></span>

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

### <span data-ttu-id="51a94-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="51a94-130">-Confirm</span></span>
<span data-ttu-id="51a94-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51a94-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51a94-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51a94-132">-WhatIf</span></span>
<span data-ttu-id="51a94-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="51a94-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51a94-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="51a94-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51a94-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51a94-135">CommonParameters</span></span>
<span data-ttu-id="51a94-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51a94-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51a94-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="51a94-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51a94-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="51a94-138">INPUTS</span></span>

### <span data-ttu-id="51a94-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="51a94-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="51a94-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="51a94-140">OUTPUTS</span></span>

### <span data-ttu-id="51a94-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="51a94-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span></span>

## <span data-ttu-id="51a94-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="51a94-142">NOTES</span></span>

<span data-ttu-id="51a94-143">ALIAS</span><span class="sxs-lookup"><span data-stu-id="51a94-143">ALIASES</span></span>

<span data-ttu-id="51a94-144">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="51a94-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="51a94-145">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="51a94-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="51a94-146">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="51a94-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="51a94-147">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="51a94-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="51a94-148">`[ApplicationGroupName <String>]`: nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="51a94-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="51a94-149">`[ApplicationName <String>]`: nome dell'applicazione all'interno del gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="51a94-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="51a94-150">`[DesktopName <String>]`: nome del desktop all'interno del gruppo di desktop specificato</span><span class="sxs-lookup"><span data-stu-id="51a94-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="51a94-151">`[HostPoolName <String>]`: nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="51a94-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="51a94-152">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="51a94-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="51a94-153">`[MsixPackageFullName <String>]`: nome completo del pacchetto specifico della versione del pacchetto MSIX all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="51a94-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="51a94-154">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="51a94-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="51a94-155">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="51a94-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="51a94-156">`[SessionHostName <String>]`: nome dell'host di sessione all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="51a94-156">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="51a94-157">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="51a94-157">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="51a94-158">`[UserSessionId <String>]`: nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="51a94-158">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="51a94-159">`[WorkspaceName <String>]`: nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="51a94-159">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="51a94-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="51a94-160">RELATED LINKS</span></span>

