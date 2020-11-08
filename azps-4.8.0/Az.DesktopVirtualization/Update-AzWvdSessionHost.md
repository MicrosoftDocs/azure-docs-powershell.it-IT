---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdSessionHost.md
ms.openlocfilehash: ec80e3382c401f9d64fb469c58a074ed47719ee9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033120"
---
# <span data-ttu-id="377bd-101">Update-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="377bd-101">Update-AzWvdSessionHost</span></span>

## <span data-ttu-id="377bd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="377bd-102">SYNOPSIS</span></span>
<span data-ttu-id="377bd-103">Aggiornare un host di sessione.</span><span class="sxs-lookup"><span data-stu-id="377bd-103">Update a session host.</span></span>

## <span data-ttu-id="377bd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="377bd-104">SYNTAX</span></span>

### <span data-ttu-id="377bd-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="377bd-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AllowNewSession] [-AssignedUser <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="377bd-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="377bd-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-AllowNewSession]
 [-AssignedUser <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="377bd-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="377bd-107">DESCRIPTION</span></span>
<span data-ttu-id="377bd-108">Aggiornare un host di sessione.</span><span class="sxs-lookup"><span data-stu-id="377bd-108">Update a session host.</span></span>

## <span data-ttu-id="377bd-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="377bd-109">EXAMPLES</span></span>

### <span data-ttu-id="377bd-110">Esempio 1: aggiornare un desktop di Windows Virtual SessionHost per nome</span><span class="sxs-lookup"><span data-stu-id="377bd-110">Example 1: Update a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Update-AzWvdSessionHost -ResourceGroupName ResourceGroupName `
                            -HostPoolName HostPoolName `
                            -Name SessionHostName `
                            -AllowNewSession:$false

Name                                               Type
----                                               ----
HostPoolName/SessionHostName Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="377bd-111">Questo comando aggiorna un SessionHost desktop virtuale di Windows in un pool host.</span><span class="sxs-lookup"><span data-stu-id="377bd-111">This command updates a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

## <span data-ttu-id="377bd-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="377bd-112">PARAMETERS</span></span>

### <span data-ttu-id="377bd-113">-AllowNewSession</span><span class="sxs-lookup"><span data-stu-id="377bd-113">-AllowNewSession</span></span>
<span data-ttu-id="377bd-114">Consentire una nuova sessione.</span><span class="sxs-lookup"><span data-stu-id="377bd-114">Allow a new session.</span></span>

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

### <span data-ttu-id="377bd-115">-AssignedUser</span><span class="sxs-lookup"><span data-stu-id="377bd-115">-AssignedUser</span></span>
<span data-ttu-id="377bd-116">Utente assegnato a SessionHost.</span><span class="sxs-lookup"><span data-stu-id="377bd-116">User assigned to SessionHost.</span></span>

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

### <span data-ttu-id="377bd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="377bd-117">-DefaultProfile</span></span>
<span data-ttu-id="377bd-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="377bd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="377bd-119">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="377bd-119">-HostPoolName</span></span>
<span data-ttu-id="377bd-120">Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="377bd-120">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="377bd-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="377bd-121">-InputObject</span></span>
<span data-ttu-id="377bd-122">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="377bd-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="377bd-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="377bd-123">-Name</span></span>
<span data-ttu-id="377bd-124">Nome dell'host di sessione nel pool di host specificato</span><span class="sxs-lookup"><span data-stu-id="377bd-124">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="377bd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="377bd-125">-ResourceGroupName</span></span>
<span data-ttu-id="377bd-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="377bd-126">The name of the resource group.</span></span>
<span data-ttu-id="377bd-127">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="377bd-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="377bd-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="377bd-128">-SubscriptionId</span></span>
<span data-ttu-id="377bd-129">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="377bd-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="377bd-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="377bd-130">-Confirm</span></span>
<span data-ttu-id="377bd-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="377bd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="377bd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="377bd-132">-WhatIf</span></span>
<span data-ttu-id="377bd-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="377bd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="377bd-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="377bd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="377bd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="377bd-135">CommonParameters</span></span>
<span data-ttu-id="377bd-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="377bd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="377bd-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="377bd-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="377bd-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="377bd-138">INPUTS</span></span>

### <span data-ttu-id="377bd-139">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="377bd-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="377bd-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="377bd-140">OUTPUTS</span></span>

### <span data-ttu-id="377bd-141">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20191210Preview. ISessionHost</span><span class="sxs-lookup"><span data-stu-id="377bd-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.ISessionHost</span></span>

## <span data-ttu-id="377bd-142">Note</span><span class="sxs-lookup"><span data-stu-id="377bd-142">NOTES</span></span>

<span data-ttu-id="377bd-143">ALIAS</span><span class="sxs-lookup"><span data-stu-id="377bd-143">ALIASES</span></span>

<span data-ttu-id="377bd-144">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="377bd-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="377bd-145">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="377bd-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="377bd-146">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="377bd-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="377bd-147">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="377bd-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="377bd-148">`[ApplicationGroupName <String>]`: Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="377bd-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="377bd-149">`[ApplicationName <String>]`: Nome dell'applicazione nel gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="377bd-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="377bd-150">`[DesktopName <String>]`: Nome del desktop nel gruppo desktop specificato</span><span class="sxs-lookup"><span data-stu-id="377bd-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="377bd-151">`[HostPoolName <String>]`: Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="377bd-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="377bd-152">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="377bd-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="377bd-153">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="377bd-153">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="377bd-154">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="377bd-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="377bd-155">`[SessionHostName <String>]`: Nome dell'host di sessione nel pool di host specificato</span><span class="sxs-lookup"><span data-stu-id="377bd-155">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="377bd-156">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="377bd-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="377bd-157">`[UserSessionId <String>]`: Nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="377bd-157">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="377bd-158">`[WorkspaceName <String>]`: Nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="377bd-158">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="377bd-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="377bd-159">RELATED LINKS</span></span>

