---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvddesktop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdDesktop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdDesktop.md
ms.openlocfilehash: 7aec3e71e65c20810d8a17e8f7fa14df3c69f577
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033119"
---
# <span data-ttu-id="cfba4-101">Update-AzWvdDesktop</span><span class="sxs-lookup"><span data-stu-id="cfba4-101">Update-AzWvdDesktop</span></span>

## <span data-ttu-id="cfba4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cfba4-102">SYNOPSIS</span></span>
<span data-ttu-id="cfba4-103">Aggiornare un desktop.</span><span class="sxs-lookup"><span data-stu-id="cfba4-103">Update a desktop.</span></span>

## <span data-ttu-id="cfba4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cfba4-104">SYNTAX</span></span>

### <span data-ttu-id="cfba4-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cfba4-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdDesktop -ApplicationGroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cfba4-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="cfba4-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdDesktop -InputObject <IDesktopVirtualizationIdentity> [-Description <String>]
 [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="cfba4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cfba4-107">DESCRIPTION</span></span>
<span data-ttu-id="cfba4-108">Aggiornare un desktop.</span><span class="sxs-lookup"><span data-stu-id="cfba4-108">Update a desktop.</span></span>

## <span data-ttu-id="cfba4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cfba4-109">EXAMPLES</span></span>

### <span data-ttu-id="cfba4-110">Esempio 1: aggiornare un desktop desktop virtuale di Windows</span><span class="sxs-lookup"><span data-stu-id="cfba4-110">Example 1: Update a Windows Virtual Desktop Desktop</span></span>
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

<span data-ttu-id="cfba4-111">Questo comando aggiorna un desktop desktop virtuale di Windows in un gruppo di Applicaton.</span><span class="sxs-lookup"><span data-stu-id="cfba4-111">This command updates a Windows Virtual Desktop Desktop in an applicaton Group.</span></span>

## <span data-ttu-id="cfba4-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cfba4-112">PARAMETERS</span></span>

### <span data-ttu-id="cfba4-113">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="cfba4-113">-ApplicationGroupName</span></span>
<span data-ttu-id="cfba4-114">Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="cfba4-114">The name of the application group</span></span>

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

### <span data-ttu-id="cfba4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfba4-115">-DefaultProfile</span></span>
<span data-ttu-id="cfba4-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cfba4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfba4-117">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="cfba4-117">-Description</span></span>
<span data-ttu-id="cfba4-118">Descrizione del desktop.</span><span class="sxs-lookup"><span data-stu-id="cfba4-118">Description of Desktop.</span></span>

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

### <span data-ttu-id="cfba4-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="cfba4-119">-FriendlyName</span></span>
<span data-ttu-id="cfba4-120">Nome descrittivo del desktop.</span><span class="sxs-lookup"><span data-stu-id="cfba4-120">Friendly name of Desktop.</span></span>

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

### <span data-ttu-id="cfba4-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cfba4-121">-InputObject</span></span>
<span data-ttu-id="cfba4-122">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="cfba4-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cfba4-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="cfba4-123">-Name</span></span>
<span data-ttu-id="cfba4-124">Nome del desktop nel gruppo desktop specificato</span><span class="sxs-lookup"><span data-stu-id="cfba4-124">The name of the desktop within the specified desktop group</span></span>

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

### <span data-ttu-id="cfba4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfba4-125">-ResourceGroupName</span></span>
<span data-ttu-id="cfba4-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cfba4-126">The name of the resource group.</span></span>
<span data-ttu-id="cfba4-127">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="cfba4-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="cfba4-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cfba4-128">-SubscriptionId</span></span>
<span data-ttu-id="cfba4-129">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="cfba4-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="cfba4-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="cfba4-130">-Tag</span></span>
<span data-ttu-id="cfba4-131">Tag da aggiornare</span><span class="sxs-lookup"><span data-stu-id="cfba4-131">tags to be updated</span></span>

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

### <span data-ttu-id="cfba4-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cfba4-132">-Confirm</span></span>
<span data-ttu-id="cfba4-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cfba4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfba4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfba4-134">-WhatIf</span></span>
<span data-ttu-id="cfba4-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cfba4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfba4-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cfba4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfba4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfba4-137">CommonParameters</span></span>
<span data-ttu-id="cfba4-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfba4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfba4-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cfba4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfba4-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cfba4-140">INPUTS</span></span>

### <span data-ttu-id="cfba4-141">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="cfba4-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="cfba4-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cfba4-142">OUTPUTS</span></span>

### <span data-ttu-id="cfba4-143">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20191210Preview. IDesktop</span><span class="sxs-lookup"><span data-stu-id="cfba4-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IDesktop</span></span>

## <span data-ttu-id="cfba4-144">Note</span><span class="sxs-lookup"><span data-stu-id="cfba4-144">NOTES</span></span>

<span data-ttu-id="cfba4-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="cfba4-145">ALIASES</span></span>

<span data-ttu-id="cfba4-146">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cfba4-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cfba4-147">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="cfba4-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cfba4-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cfba4-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cfba4-149">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="cfba4-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cfba4-150">`[ApplicationGroupName <String>]`: Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="cfba4-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="cfba4-151">`[ApplicationName <String>]`: Nome dell'applicazione nel gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="cfba4-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="cfba4-152">`[DesktopName <String>]`: Nome del desktop nel gruppo desktop specificato</span><span class="sxs-lookup"><span data-stu-id="cfba4-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="cfba4-153">`[HostPoolName <String>]`: Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="cfba4-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="cfba4-154">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="cfba4-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cfba4-155">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cfba4-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="cfba4-156">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="cfba4-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="cfba4-157">`[SessionHostName <String>]`: Nome dell'host di sessione nel pool di host specificato</span><span class="sxs-lookup"><span data-stu-id="cfba4-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="cfba4-158">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="cfba4-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="cfba4-159">`[UserSessionId <String>]`: Nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="cfba4-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="cfba4-160">`[WorkspaceName <String>]`: Nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="cfba4-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="cfba4-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cfba4-161">RELATED LINKS</span></span>

