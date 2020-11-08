---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdWorkspace.md
ms.openlocfilehash: 30c0734656b79f532c56b47b64e9d7e918f92fa8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031251"
---
# <span data-ttu-id="0efd7-101">Update-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="0efd7-101">Update-AzWvdWorkspace</span></span>

## <span data-ttu-id="0efd7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0efd7-102">SYNOPSIS</span></span>
<span data-ttu-id="0efd7-103">Aggiornare un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="0efd7-103">Update a workspace.</span></span>

## <span data-ttu-id="0efd7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0efd7-104">SYNTAX</span></span>

### <span data-ttu-id="0efd7-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0efd7-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-ApplicationGroupReference <String[]>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0efd7-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="0efd7-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdWorkspace -InputObject <IDesktopVirtualizationIdentity> [-ApplicationGroupReference <String[]>]
 [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0efd7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0efd7-107">DESCRIPTION</span></span>
<span data-ttu-id="0efd7-108">Aggiornare un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="0efd7-108">Update a workspace.</span></span>

## <span data-ttu-id="0efd7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0efd7-109">EXAMPLES</span></span>

### <span data-ttu-id="0efd7-110">Esempio 1: aggiornare un desktop di Windows Virtual worksapce per nome</span><span class="sxs-lookup"><span data-stu-id="0efd7-110">Example 1: Update a Windows Virtual Desktop Worksapce by name</span></span>
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

<span data-ttu-id="0efd7-111">Questo comando aggiorna un'area di lavoro desktop virtuale di Windows in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0efd7-111">This command updates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="0efd7-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0efd7-112">PARAMETERS</span></span>

### <span data-ttu-id="0efd7-113">-ApplicationGroupReference</span><span class="sxs-lookup"><span data-stu-id="0efd7-113">-ApplicationGroupReference</span></span>
<span data-ttu-id="0efd7-114">Elenco dei collegamenti di applicationGroup.</span><span class="sxs-lookup"><span data-stu-id="0efd7-114">List of applicationGroup links.</span></span>

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

### <span data-ttu-id="0efd7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0efd7-115">-DefaultProfile</span></span>
<span data-ttu-id="0efd7-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0efd7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0efd7-117">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="0efd7-117">-Description</span></span>
<span data-ttu-id="0efd7-118">Descrizione dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="0efd7-118">Description of Workspace.</span></span>

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

### <span data-ttu-id="0efd7-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="0efd7-119">-FriendlyName</span></span>
<span data-ttu-id="0efd7-120">Nome descrittivo dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="0efd7-120">Friendly name of Workspace.</span></span>

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

### <span data-ttu-id="0efd7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0efd7-121">-InputObject</span></span>
<span data-ttu-id="0efd7-122">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="0efd7-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0efd7-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="0efd7-123">-Name</span></span>
<span data-ttu-id="0efd7-124">Nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="0efd7-124">The name of the workspace</span></span>

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

### <span data-ttu-id="0efd7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0efd7-125">-ResourceGroupName</span></span>
<span data-ttu-id="0efd7-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0efd7-126">The name of the resource group.</span></span>
<span data-ttu-id="0efd7-127">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="0efd7-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0efd7-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0efd7-128">-SubscriptionId</span></span>
<span data-ttu-id="0efd7-129">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0efd7-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0efd7-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="0efd7-130">-Tag</span></span>
<span data-ttu-id="0efd7-131">Tag da aggiornare</span><span class="sxs-lookup"><span data-stu-id="0efd7-131">tags to be updated</span></span>

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

### <span data-ttu-id="0efd7-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0efd7-132">-Confirm</span></span>
<span data-ttu-id="0efd7-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0efd7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0efd7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0efd7-134">-WhatIf</span></span>
<span data-ttu-id="0efd7-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0efd7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0efd7-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0efd7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0efd7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0efd7-137">CommonParameters</span></span>
<span data-ttu-id="0efd7-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0efd7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0efd7-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0efd7-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0efd7-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0efd7-140">INPUTS</span></span>

### <span data-ttu-id="0efd7-141">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="0efd7-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="0efd7-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0efd7-142">OUTPUTS</span></span>

### <span data-ttu-id="0efd7-143">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20191210Preview. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="0efd7-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="0efd7-144">Note</span><span class="sxs-lookup"><span data-stu-id="0efd7-144">NOTES</span></span>

<span data-ttu-id="0efd7-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="0efd7-145">ALIASES</span></span>

<span data-ttu-id="0efd7-146">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0efd7-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0efd7-147">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="0efd7-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0efd7-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0efd7-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0efd7-149">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="0efd7-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0efd7-150">`[ApplicationGroupName <String>]`: Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="0efd7-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="0efd7-151">`[ApplicationName <String>]`: Nome dell'applicazione nel gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="0efd7-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="0efd7-152">`[DesktopName <String>]`: Nome del desktop nel gruppo desktop specificato</span><span class="sxs-lookup"><span data-stu-id="0efd7-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="0efd7-153">`[HostPoolName <String>]`: Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="0efd7-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="0efd7-154">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="0efd7-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0efd7-155">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0efd7-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="0efd7-156">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="0efd7-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="0efd7-157">`[SessionHostName <String>]`: Nome dell'host di sessione nel pool di host specificato</span><span class="sxs-lookup"><span data-stu-id="0efd7-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="0efd7-158">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0efd7-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="0efd7-159">`[UserSessionId <String>]`: Nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="0efd7-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="0efd7-160">`[WorkspaceName <String>]`: Nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="0efd7-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="0efd7-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0efd7-161">RELATED LINKS</span></span>

