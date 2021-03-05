---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/update-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdSessionHost.md
ms.openlocfilehash: 9e8599edaa1a1c19d5b0629d290402c792cf2563
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983566"
---
# <span data-ttu-id="37c2b-101">Update-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="37c2b-101">Update-AzWvdSessionHost</span></span>

## <span data-ttu-id="37c2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37c2b-102">SYNOPSIS</span></span>
<span data-ttu-id="37c2b-103">Aggiornare un host di sessione.</span><span class="sxs-lookup"><span data-stu-id="37c2b-103">Update a session host.</span></span>

## <span data-ttu-id="37c2b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="37c2b-104">SYNTAX</span></span>

### <span data-ttu-id="37c2b-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="37c2b-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AllowNewSession] [-AssignedUser <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="37c2b-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="37c2b-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-AllowNewSession]
 [-AssignedUser <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="37c2b-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="37c2b-107">DESCRIPTION</span></span>
<span data-ttu-id="37c2b-108">Aggiornare un host di sessione.</span><span class="sxs-lookup"><span data-stu-id="37c2b-108">Update a session host.</span></span>

## <span data-ttu-id="37c2b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="37c2b-109">EXAMPLES</span></span>

### <span data-ttu-id="37c2b-110">Esempio 1: Aggiornare un sessionHost di Desktop virtuale di Windows in base al nome</span><span class="sxs-lookup"><span data-stu-id="37c2b-110">Example 1: Update a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Update-AzWvdSessionHost -ResourceGroupName ResourceGroupName `
                            -HostPoolName HostPoolName `
                            -Name SessionHostName `
                            -AllowNewSession:$false

Name                                               Type
----                                               ----
HostPoolName/SessionHostName Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="37c2b-111">Questo comando aggiorna un sessionhost di Desktop virtuale di Windows in un pool host.</span><span class="sxs-lookup"><span data-stu-id="37c2b-111">This command updates a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

## <span data-ttu-id="37c2b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37c2b-112">PARAMETERS</span></span>

### <span data-ttu-id="37c2b-113">-AllowNewSession</span><span class="sxs-lookup"><span data-stu-id="37c2b-113">-AllowNewSession</span></span>
<span data-ttu-id="37c2b-114">Consentire una nuova sessione.</span><span class="sxs-lookup"><span data-stu-id="37c2b-114">Allow a new session.</span></span>

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

### <span data-ttu-id="37c2b-115">-AssignedUser</span><span class="sxs-lookup"><span data-stu-id="37c2b-115">-AssignedUser</span></span>
<span data-ttu-id="37c2b-116">Utente assegnato a SessionHost.</span><span class="sxs-lookup"><span data-stu-id="37c2b-116">User assigned to SessionHost.</span></span>

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

### <span data-ttu-id="37c2b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37c2b-117">-DefaultProfile</span></span>
<span data-ttu-id="37c2b-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="37c2b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37c2b-119">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="37c2b-119">-HostPoolName</span></span>
<span data-ttu-id="37c2b-120">Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="37c2b-120">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="37c2b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37c2b-121">-InputObject</span></span>
<span data-ttu-id="37c2b-122">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="37c2b-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="37c2b-123">-Name</span><span class="sxs-lookup"><span data-stu-id="37c2b-123">-Name</span></span>
<span data-ttu-id="37c2b-124">Nome dell'host di sessione all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="37c2b-124">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: SessionHostName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37c2b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37c2b-125">-ResourceGroupName</span></span>
<span data-ttu-id="37c2b-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="37c2b-126">The name of the resource group.</span></span>
<span data-ttu-id="37c2b-127">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="37c2b-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="37c2b-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="37c2b-128">-SubscriptionId</span></span>
<span data-ttu-id="37c2b-129">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="37c2b-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="37c2b-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37c2b-130">-Confirm</span></span>
<span data-ttu-id="37c2b-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37c2b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37c2b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37c2b-132">-WhatIf</span></span>
<span data-ttu-id="37c2b-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="37c2b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37c2b-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="37c2b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37c2b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37c2b-135">CommonParameters</span></span>
<span data-ttu-id="37c2b-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37c2b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37c2b-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="37c2b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37c2b-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="37c2b-138">INPUTS</span></span>

### <span data-ttu-id="37c2b-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="37c2b-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="37c2b-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="37c2b-140">OUTPUTS</span></span>

### <span data-ttu-id="37c2b-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.ISessionHost</span><span class="sxs-lookup"><span data-stu-id="37c2b-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.ISessionHost</span></span>

## <span data-ttu-id="37c2b-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="37c2b-142">NOTES</span></span>

<span data-ttu-id="37c2b-143">ALIAS</span><span class="sxs-lookup"><span data-stu-id="37c2b-143">ALIASES</span></span>

<span data-ttu-id="37c2b-144">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="37c2b-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="37c2b-145">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="37c2b-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="37c2b-146">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="37c2b-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="37c2b-147">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="37c2b-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="37c2b-148">`[ApplicationGroupName <String>]`: nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="37c2b-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="37c2b-149">`[ApplicationName <String>]`: nome dell'applicazione all'interno del gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="37c2b-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="37c2b-150">`[DesktopName <String>]`: nome del desktop all'interno del gruppo di desktop specificato</span><span class="sxs-lookup"><span data-stu-id="37c2b-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="37c2b-151">`[HostPoolName <String>]`: nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="37c2b-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="37c2b-152">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="37c2b-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="37c2b-153">`[MsixPackageFullName <String>]`: nome completo del pacchetto specifico della versione del pacchetto MSIX all'interno dello pool host specificato</span><span class="sxs-lookup"><span data-stu-id="37c2b-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="37c2b-154">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="37c2b-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="37c2b-155">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="37c2b-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="37c2b-156">`[SessionHostName <String>]`: nome dell'host di sessione all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="37c2b-156">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="37c2b-157">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="37c2b-157">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="37c2b-158">`[UserSessionId <String>]`: nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="37c2b-158">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="37c2b-159">`[WorkspaceName <String>]`: nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="37c2b-159">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="37c2b-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="37c2b-160">RELATED LINKS</span></span>

