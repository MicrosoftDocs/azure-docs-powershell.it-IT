---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdWorkspace.md
ms.openlocfilehash: 8a20777cfd6e28c3edc127117687b7aef801d94e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387222"
---
# <span data-ttu-id="18b93-101">Update-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="18b93-101">Update-AzWvdWorkspace</span></span>

## <span data-ttu-id="18b93-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="18b93-102">SYNOPSIS</span></span>
<span data-ttu-id="18b93-103">Aggiornare un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="18b93-103">Update a workspace.</span></span>

## <span data-ttu-id="18b93-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="18b93-104">SYNTAX</span></span>

### <span data-ttu-id="18b93-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="18b93-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-ApplicationGroupReference <String[]>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="18b93-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="18b93-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdWorkspace -InputObject <IDesktopVirtualizationIdentity> [-ApplicationGroupReference <String[]>]
 [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="18b93-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18b93-107">DESCRIPTION</span></span>
<span data-ttu-id="18b93-108">Aggiornare un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="18b93-108">Update a workspace.</span></span>

## <span data-ttu-id="18b93-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="18b93-109">EXAMPLES</span></span>

### <span data-ttu-id="18b93-110">Esempio 1: aggiornare un'area di lavoro desktop virtuale di Windows per nome</span><span class="sxs-lookup"><span data-stu-id="18b93-110">Example 1: Update a Windows Virtual Desktop Workspace by name</span></span>
```powershell
PS C:\> Update-AzWvdWorkspace -ResourceGroupName ResourceGroupName `
                        -Name WorkspaceName `
                        -FriendlyName 'Friendly Name' `
                        -ApplicationGroupReference "/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName1","/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName2" `
                        -Description 'Description'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="18b93-111">Questo comando aggiorna un'area di lavoro desktop virtuale di Windows in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="18b93-111">This command updates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="18b93-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="18b93-112">PARAMETERS</span></span>

### <span data-ttu-id="18b93-113">-ApplicationGroupReference</span><span class="sxs-lookup"><span data-stu-id="18b93-113">-ApplicationGroupReference</span></span>
<span data-ttu-id="18b93-114">Elenco dei collegamenti di applicationGroup.</span><span class="sxs-lookup"><span data-stu-id="18b93-114">List of applicationGroup links.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18b93-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18b93-115">-DefaultProfile</span></span>
<span data-ttu-id="18b93-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="18b93-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18b93-117">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="18b93-117">-Description</span></span>
<span data-ttu-id="18b93-118">Descrizione dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="18b93-118">Description of Workspace.</span></span>

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

### <span data-ttu-id="18b93-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="18b93-119">-FriendlyName</span></span>
<span data-ttu-id="18b93-120">Nome descrittivo dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="18b93-120">Friendly name of Workspace.</span></span>

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

### <span data-ttu-id="18b93-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18b93-121">-InputObject</span></span>
<span data-ttu-id="18b93-122">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="18b93-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="18b93-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="18b93-123">-Name</span></span>
<span data-ttu-id="18b93-124">Nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="18b93-124">The name of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18b93-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18b93-125">-ResourceGroupName</span></span>
<span data-ttu-id="18b93-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="18b93-126">The name of the resource group.</span></span>
<span data-ttu-id="18b93-127">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="18b93-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="18b93-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="18b93-128">-SubscriptionId</span></span>
<span data-ttu-id="18b93-129">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="18b93-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="18b93-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="18b93-130">-Tag</span></span>
<span data-ttu-id="18b93-131">Tag da aggiornare</span><span class="sxs-lookup"><span data-stu-id="18b93-131">tags to be updated</span></span>

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

### <span data-ttu-id="18b93-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="18b93-132">-Confirm</span></span>
<span data-ttu-id="18b93-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18b93-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18b93-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18b93-134">-WhatIf</span></span>
<span data-ttu-id="18b93-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="18b93-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18b93-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="18b93-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18b93-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18b93-137">CommonParameters</span></span>
<span data-ttu-id="18b93-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18b93-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18b93-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="18b93-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18b93-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="18b93-140">INPUTS</span></span>

### <span data-ttu-id="18b93-141">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="18b93-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="18b93-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="18b93-142">OUTPUTS</span></span>

### <span data-ttu-id="18b93-143">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20201102Preview. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="18b93-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span></span>

## <span data-ttu-id="18b93-144">Note</span><span class="sxs-lookup"><span data-stu-id="18b93-144">NOTES</span></span>

<span data-ttu-id="18b93-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="18b93-145">ALIASES</span></span>

<span data-ttu-id="18b93-146">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="18b93-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="18b93-147">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="18b93-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="18b93-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="18b93-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="18b93-149">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="18b93-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="18b93-150">`[ApplicationGroupName <String>]`: Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="18b93-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="18b93-151">`[ApplicationName <String>]`: Nome dell'applicazione nel gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="18b93-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="18b93-152">`[DesktopName <String>]`: Nome del desktop nel gruppo desktop specificato</span><span class="sxs-lookup"><span data-stu-id="18b93-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="18b93-153">`[HostPoolName <String>]`: Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="18b93-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="18b93-154">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="18b93-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="18b93-155">`[MsixPackageFullName <String>]`: Pacchetto specifico della versione nome completo del pacchetto MSIX all'interno di hostpool specificato</span><span class="sxs-lookup"><span data-stu-id="18b93-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="18b93-156">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="18b93-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="18b93-157">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="18b93-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="18b93-158">`[SessionHostName <String>]`: Nome dell'host di sessione nel pool di host specificato</span><span class="sxs-lookup"><span data-stu-id="18b93-158">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="18b93-159">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="18b93-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="18b93-160">`[UserSessionId <String>]`: Nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="18b93-160">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="18b93-161">`[WorkspaceName <String>]`: Nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="18b93-161">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="18b93-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="18b93-162">RELATED LINKS</span></span>

