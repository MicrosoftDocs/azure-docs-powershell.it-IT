---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
ms.openlocfilehash: ffb38dd20c5bc43c3d243e5a6f320fdc5d48d008
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031775"
---
# <span data-ttu-id="5f838-101">Update-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="5f838-101">Update-AzWvdHostPool</span></span>

## <span data-ttu-id="5f838-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5f838-102">SYNOPSIS</span></span>
<span data-ttu-id="5f838-103">Aggiornare un pool host.</span><span class="sxs-lookup"><span data-stu-id="5f838-103">Update a host pool.</span></span>

## <span data-ttu-id="5f838-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5f838-104">SYNTAX</span></span>

### <span data-ttu-id="5f838-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5f838-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-CustomRdpProperty <String>] [-Description <String>] [-FriendlyName <String>]
 [-LoadBalancerType <LoadBalancerType>] [-MaxSessionLimit <Int32>]
 [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>]
 [-PreferredAppGroupType <PreferredAppGroupType>] [-RegistrationInfoExpirationTime <DateTime>]
 [-RegistrationInfoRegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>]
 [-SsoContext <String>] [-Tag <Hashtable>] [-ValidationEnvironment] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5f838-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="5f838-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-CustomRdpProperty <String>]
 [-Description <String>] [-FriendlyName <String>] [-LoadBalancerType <LoadBalancerType>]
 [-MaxSessionLimit <Int32>] [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>]
 [-PreferredAppGroupType <PreferredAppGroupType>] [-RegistrationInfoExpirationTime <DateTime>]
 [-RegistrationInfoRegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>]
 [-SsoContext <String>] [-Tag <Hashtable>] [-ValidationEnvironment] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5f838-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5f838-107">DESCRIPTION</span></span>
<span data-ttu-id="5f838-108">Aggiornare un pool host.</span><span class="sxs-lookup"><span data-stu-id="5f838-108">Update a host pool.</span></span>

## <span data-ttu-id="5f838-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5f838-109">EXAMPLES</span></span>

### <span data-ttu-id="5f838-110">Esempio 1: aggiornare un desktop di Windows Virtual HostPool per nome</span><span class="sxs-lookup"><span data-stu-id="5f838-110">Example 1: Update a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> Update-AzWvdHostPool -ResourceGroupName ResourceGroupName `
                            -Name HostPoolName `
                            -LoadBalancerType 'BreadthFirst' `
                            -Description 'Description' `
                            -FriendlyName 'Friendly Name' `
                            -MaxSessionLimit 6 `
                            -SsoContext $null `
                            -CustomRdpProperty $null `
                            -Ring $null `
                            -ValidationEnvironment:$false

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="5f838-111">Questo comando aggiorna un HostPool desktop virtuale di Windows in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5f838-111">This command updates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="5f838-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5f838-112">PARAMETERS</span></span>

### <span data-ttu-id="5f838-113">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="5f838-113">-CustomRdpProperty</span></span>
<span data-ttu-id="5f838-114">Proprietà RDP personalizzata di HostPool.</span><span class="sxs-lookup"><span data-stu-id="5f838-114">Custom rdp property of HostPool.</span></span>

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

### <span data-ttu-id="5f838-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f838-115">-DefaultProfile</span></span>
<span data-ttu-id="5f838-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5f838-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f838-117">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="5f838-117">-Description</span></span>
<span data-ttu-id="5f838-118">Descrizione di HostPool.</span><span class="sxs-lookup"><span data-stu-id="5f838-118">Description of HostPool.</span></span>

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

### <span data-ttu-id="5f838-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="5f838-119">-FriendlyName</span></span>
<span data-ttu-id="5f838-120">Nome descrittivo di HostPool.</span><span class="sxs-lookup"><span data-stu-id="5f838-120">Friendly name of HostPool.</span></span>

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

### <span data-ttu-id="5f838-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5f838-121">-InputObject</span></span>
<span data-ttu-id="5f838-122">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="5f838-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5f838-123">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="5f838-123">-LoadBalancerType</span></span>
<span data-ttu-id="5f838-124">Tipo di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="5f838-124">The type of the load balancer.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.LoadBalancerType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f838-125">-MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="5f838-125">-MaxSessionLimit</span></span>
<span data-ttu-id="5f838-126">Limite massimo della sessione di HostPool.</span><span class="sxs-lookup"><span data-stu-id="5f838-126">The max session limit of HostPool.</span></span>

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

### <span data-ttu-id="5f838-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="5f838-127">-Name</span></span>
<span data-ttu-id="5f838-128">Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="5f838-128">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: HostPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f838-129">-PersonalDesktopAssignmentType</span><span class="sxs-lookup"><span data-stu-id="5f838-129">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="5f838-130">Tipo PersonalDesktopAssignment per HostPool.</span><span class="sxs-lookup"><span data-stu-id="5f838-130">PersonalDesktopAssignment type for HostPool.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.PersonalDesktopAssignmentType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f838-131">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="5f838-131">-PreferredAppGroupType</span></span>
<span data-ttu-id="5f838-132">Tipo di tipo di gruppo di applicazioni preferito, predefinito per il gruppo applicazione desktop</span><span class="sxs-lookup"><span data-stu-id="5f838-132">The type of preferred application group type, default to Desktop Application Group</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.PreferredAppGroupType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f838-133">-RegistrationInfoExpirationTime</span><span class="sxs-lookup"><span data-stu-id="5f838-133">-RegistrationInfoExpirationTime</span></span>
<span data-ttu-id="5f838-134">Data di scadenza del token di registrazione.</span><span class="sxs-lookup"><span data-stu-id="5f838-134">Expiration time of registration token.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f838-135">-RegistrationInfoRegistrationTokenOperation</span><span class="sxs-lookup"><span data-stu-id="5f838-135">-RegistrationInfoRegistrationTokenOperation</span></span>
<span data-ttu-id="5f838-136">Tipo di reimpostazione del token.</span><span class="sxs-lookup"><span data-stu-id="5f838-136">The type of resetting the token.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.RegistrationTokenOperation
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f838-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f838-137">-ResourceGroupName</span></span>
<span data-ttu-id="5f838-138">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5f838-138">The name of the resource group.</span></span>
<span data-ttu-id="5f838-139">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="5f838-139">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5f838-140">-Ring</span><span class="sxs-lookup"><span data-stu-id="5f838-140">-Ring</span></span>
<span data-ttu-id="5f838-141">Numero ring di HostPool.</span><span class="sxs-lookup"><span data-stu-id="5f838-141">The ring number of HostPool.</span></span>

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

### <span data-ttu-id="5f838-142">-SsoContext</span><span class="sxs-lookup"><span data-stu-id="5f838-142">-SsoContext</span></span>
<span data-ttu-id="5f838-143">Percorso di un Vault contenente ssoContext segreto.</span><span class="sxs-lookup"><span data-stu-id="5f838-143">Path to keyvault containing ssoContext secret.</span></span>

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

### <span data-ttu-id="5f838-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5f838-144">-SubscriptionId</span></span>
<span data-ttu-id="5f838-145">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="5f838-145">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="5f838-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="5f838-146">-Tag</span></span>
<span data-ttu-id="5f838-147">Tag da aggiornare</span><span class="sxs-lookup"><span data-stu-id="5f838-147">tags to be updated</span></span>

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

### <span data-ttu-id="5f838-148">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="5f838-148">-ValidationEnvironment</span></span>
<span data-ttu-id="5f838-149">È l'ambiente di convalida.</span><span class="sxs-lookup"><span data-stu-id="5f838-149">Is validation environment.</span></span>

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

### <span data-ttu-id="5f838-150">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5f838-150">-Confirm</span></span>
<span data-ttu-id="5f838-151">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f838-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f838-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f838-152">-WhatIf</span></span>
<span data-ttu-id="5f838-153">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5f838-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f838-154">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5f838-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f838-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f838-155">CommonParameters</span></span>
<span data-ttu-id="5f838-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f838-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f838-157">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5f838-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f838-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5f838-158">INPUTS</span></span>

### <span data-ttu-id="5f838-159">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="5f838-159">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="5f838-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5f838-160">OUTPUTS</span></span>

### <span data-ttu-id="5f838-161">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20191210Preview. IHostPool</span><span class="sxs-lookup"><span data-stu-id="5f838-161">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IHostPool</span></span>

## <span data-ttu-id="5f838-162">Note</span><span class="sxs-lookup"><span data-stu-id="5f838-162">NOTES</span></span>

<span data-ttu-id="5f838-163">ALIAS</span><span class="sxs-lookup"><span data-stu-id="5f838-163">ALIASES</span></span>

<span data-ttu-id="5f838-164">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5f838-164">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5f838-165">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="5f838-165">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5f838-166">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5f838-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5f838-167">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="5f838-167">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5f838-168">`[ApplicationGroupName <String>]`: Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="5f838-168">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="5f838-169">`[ApplicationName <String>]`: Nome dell'applicazione nel gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="5f838-169">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="5f838-170">`[DesktopName <String>]`: Nome del desktop nel gruppo desktop specificato</span><span class="sxs-lookup"><span data-stu-id="5f838-170">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="5f838-171">`[HostPoolName <String>]`: Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="5f838-171">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="5f838-172">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="5f838-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5f838-173">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5f838-173">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="5f838-174">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="5f838-174">The name is case insensitive.</span></span>
  - <span data-ttu-id="5f838-175">`[SessionHostName <String>]`: Nome dell'host di sessione nel pool di host specificato</span><span class="sxs-lookup"><span data-stu-id="5f838-175">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="5f838-176">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="5f838-176">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="5f838-177">`[UserSessionId <String>]`: Nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="5f838-177">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="5f838-178">`[WorkspaceName <String>]`: Nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="5f838-178">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="5f838-179">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5f838-179">RELATED LINKS</span></span>

