---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplicationGroup.md
ms.openlocfilehash: b03fe0c62a446c9ed54c9330708f29737e18bd59
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476363"
---
# <span data-ttu-id="bbee2-101">Update-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="bbee2-101">Update-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="bbee2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bbee2-102">SYNOPSIS</span></span>
<span data-ttu-id="bbee2-103">Aggiornare un applicationGroup.</span><span class="sxs-lookup"><span data-stu-id="bbee2-103">Update an applicationGroup.</span></span>

## <span data-ttu-id="bbee2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bbee2-104">SYNTAX</span></span>

### <span data-ttu-id="bbee2-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bbee2-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bbee2-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="bbee2-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-Description <String>]
 [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="bbee2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bbee2-107">DESCRIPTION</span></span>
<span data-ttu-id="bbee2-108">Aggiornare un applicationGroup.</span><span class="sxs-lookup"><span data-stu-id="bbee2-108">Update an applicationGroup.</span></span>

## <span data-ttu-id="bbee2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bbee2-109">EXAMPLES</span></span>

### <span data-ttu-id="bbee2-110">Esempio 1: creare un desktop virtuale di Windows ApplicationGroup per nome</span><span class="sxs-lookup"><span data-stu-id="bbee2-110">Example 1: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> New-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                            -Name ApplicationGroupName `
                            -FriendlyName 'Friendly Name' `
                            -Description 'Description' `

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="bbee2-111">Questo comando crea un ApplicationGroup desktop virtuale di Windows in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bbee2-111">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="bbee2-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bbee2-112">PARAMETERS</span></span>

### <span data-ttu-id="bbee2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbee2-113">-DefaultProfile</span></span>
<span data-ttu-id="bbee2-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bbee2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbee2-115">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="bbee2-115">-Description</span></span>
<span data-ttu-id="bbee2-116">Descrizione di ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="bbee2-116">Description of ApplicationGroup.</span></span>

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

### <span data-ttu-id="bbee2-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="bbee2-117">-FriendlyName</span></span>
<span data-ttu-id="bbee2-118">Nome descrittivo di ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="bbee2-118">Friendly name of ApplicationGroup.</span></span>

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

### <span data-ttu-id="bbee2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bbee2-119">-InputObject</span></span>
<span data-ttu-id="bbee2-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="bbee2-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bbee2-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="bbee2-121">-Name</span></span>
<span data-ttu-id="bbee2-122">Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="bbee2-122">The name of the application group</span></span>

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

### <span data-ttu-id="bbee2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbee2-123">-ResourceGroupName</span></span>
<span data-ttu-id="bbee2-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bbee2-124">The name of the resource group.</span></span>
<span data-ttu-id="bbee2-125">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="bbee2-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="bbee2-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bbee2-126">-SubscriptionId</span></span>
<span data-ttu-id="bbee2-127">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="bbee2-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="bbee2-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="bbee2-128">-Tag</span></span>
<span data-ttu-id="bbee2-129">Tag da aggiornare</span><span class="sxs-lookup"><span data-stu-id="bbee2-129">tags to be updated</span></span>

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

### <span data-ttu-id="bbee2-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bbee2-130">-Confirm</span></span>
<span data-ttu-id="bbee2-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbee2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbee2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbee2-132">-WhatIf</span></span>
<span data-ttu-id="bbee2-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bbee2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbee2-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bbee2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbee2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbee2-135">CommonParameters</span></span>
<span data-ttu-id="bbee2-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbee2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbee2-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bbee2-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbee2-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bbee2-138">INPUTS</span></span>

### <span data-ttu-id="bbee2-139">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="bbee2-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="bbee2-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bbee2-140">OUTPUTS</span></span>

### <span data-ttu-id="bbee2-141">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20201102Preview. IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="bbee2-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span></span>

## <span data-ttu-id="bbee2-142">Note</span><span class="sxs-lookup"><span data-stu-id="bbee2-142">NOTES</span></span>

<span data-ttu-id="bbee2-143">ALIAS</span><span class="sxs-lookup"><span data-stu-id="bbee2-143">ALIASES</span></span>

<span data-ttu-id="bbee2-144">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bbee2-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bbee2-145">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="bbee2-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bbee2-146">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bbee2-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bbee2-147">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="bbee2-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bbee2-148">`[ApplicationGroupName <String>]`: Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="bbee2-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="bbee2-149">`[ApplicationName <String>]`: Nome dell'applicazione nel gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="bbee2-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="bbee2-150">`[DesktopName <String>]`: Nome del desktop nel gruppo desktop specificato</span><span class="sxs-lookup"><span data-stu-id="bbee2-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="bbee2-151">`[HostPoolName <String>]`: Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="bbee2-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="bbee2-152">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="bbee2-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bbee2-153">`[MsixPackageFullName <String>]`: Pacchetto specifico della versione nome completo del pacchetto MSIX all'interno di hostpool specificato</span><span class="sxs-lookup"><span data-stu-id="bbee2-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="bbee2-154">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bbee2-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="bbee2-155">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="bbee2-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="bbee2-156">`[SessionHostName <String>]`: Nome dell'host di sessione nel pool di host specificato</span><span class="sxs-lookup"><span data-stu-id="bbee2-156">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="bbee2-157">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="bbee2-157">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="bbee2-158">`[UserSessionId <String>]`: Nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="bbee2-158">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="bbee2-159">`[WorkspaceName <String>]`: Nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="bbee2-159">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="bbee2-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bbee2-160">RELATED LINKS</span></span>

