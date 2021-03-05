---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/update-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
ms.openlocfilehash: 5b69ff6bb04f1e8b1ae5e13fbab2c6a5f7c67927
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983582"
---
# <span data-ttu-id="ec309-101">Update-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="ec309-101">Update-AzWvdHostPool</span></span>

## <span data-ttu-id="ec309-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec309-102">SYNOPSIS</span></span>
<span data-ttu-id="ec309-103">Aggiornare un pool host.</span><span class="sxs-lookup"><span data-stu-id="ec309-103">Update a host pool.</span></span>

## <span data-ttu-id="ec309-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ec309-104">SYNTAX</span></span>

### <span data-ttu-id="ec309-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ec309-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-CustomRdpProperty <String>] [-Description <String>] [-FriendlyName <String>]
 [-LoadBalancerType <LoadBalancerType>] [-MaxSessionLimit <Int32>]
 [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>]
 [-PreferredAppGroupType <PreferredAppGroupType>] [-RegistrationInfoExpirationTime <DateTime>]
 [-RegistrationInfoRegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>]
 [-SsoadfsAuthority <String>] [-SsoClientId <String>] [-SsoClientSecretKeyVaultPath <String>]
 [-SsoContext <String>] [-SsoSecretType <SsoSecretType>] [-StartVMOnConnect] [-Tag <Hashtable>]
 [-ValidationEnvironment] [-VMTemplate <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="ec309-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ec309-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-CustomRdpProperty <String>]
 [-Description <String>] [-FriendlyName <String>] [-LoadBalancerType <LoadBalancerType>]
 [-MaxSessionLimit <Int32>] [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>]
 [-PreferredAppGroupType <PreferredAppGroupType>] [-RegistrationInfoExpirationTime <DateTime>]
 [-RegistrationInfoRegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>]
 [-SsoadfsAuthority <String>] [-SsoClientId <String>] [-SsoClientSecretKeyVaultPath <String>]
 [-SsoContext <String>] [-SsoSecretType <SsoSecretType>] [-StartVMOnConnect] [-Tag <Hashtable>]
 [-ValidationEnvironment] [-VMTemplate <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="ec309-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ec309-107">DESCRIPTION</span></span>
<span data-ttu-id="ec309-108">Aggiornare un pool host.</span><span class="sxs-lookup"><span data-stu-id="ec309-108">Update a host pool.</span></span>

## <span data-ttu-id="ec309-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ec309-109">EXAMPLES</span></span>

### <span data-ttu-id="ec309-110">Esempio 1: Aggiornare un pool di desktop virtuali Windows in base al nome</span><span class="sxs-lookup"><span data-stu-id="ec309-110">Example 1: Update a Windows Virtual Desktop HostPool by name</span></span>
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

<span data-ttu-id="ec309-111">Questo comando aggiorna un Windows Virtual Desktop HostPool in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ec309-111">This command updates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="ec309-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec309-112">PARAMETERS</span></span>

### <span data-ttu-id="ec309-113">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="ec309-113">-CustomRdpProperty</span></span>
<span data-ttu-id="ec309-114">Proprietà rdp personalizzata di HostPool.</span><span class="sxs-lookup"><span data-stu-id="ec309-114">Custom rdp property of HostPool.</span></span>

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

### <span data-ttu-id="ec309-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec309-115">-DefaultProfile</span></span>
<span data-ttu-id="ec309-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ec309-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec309-117">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="ec309-117">-Description</span></span>
<span data-ttu-id="ec309-118">Descrizione di HostPool.</span><span class="sxs-lookup"><span data-stu-id="ec309-118">Description of HostPool.</span></span>

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

### <span data-ttu-id="ec309-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="ec309-119">-FriendlyName</span></span>
<span data-ttu-id="ec309-120">Nome descrittivo di HostPool.</span><span class="sxs-lookup"><span data-stu-id="ec309-120">Friendly name of HostPool.</span></span>

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

### <span data-ttu-id="ec309-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec309-121">-InputObject</span></span>
<span data-ttu-id="ec309-122">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="ec309-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ec309-123">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="ec309-123">-LoadBalancerType</span></span>
<span data-ttu-id="ec309-124">Tipo di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="ec309-124">The type of the load balancer.</span></span>

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

### <span data-ttu-id="ec309-125">-MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="ec309-125">-MaxSessionLimit</span></span>
<span data-ttu-id="ec309-126">Limite massimo di sessione di HostPool.</span><span class="sxs-lookup"><span data-stu-id="ec309-126">The max session limit of HostPool.</span></span>

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

### <span data-ttu-id="ec309-127">-Name</span><span class="sxs-lookup"><span data-stu-id="ec309-127">-Name</span></span>
<span data-ttu-id="ec309-128">Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="ec309-128">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="ec309-129">-PersonalDesktopAssignmentType</span><span class="sxs-lookup"><span data-stu-id="ec309-129">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="ec309-130">PersonalDesktopAssignment type for HostPool.</span><span class="sxs-lookup"><span data-stu-id="ec309-130">PersonalDesktopAssignment type for HostPool.</span></span>

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

### <span data-ttu-id="ec309-131">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="ec309-131">-PreferredAppGroupType</span></span>
<span data-ttu-id="ec309-132">Tipo di gruppo di applicazioni preferito, predefinito per Gruppo applicazioni desktop</span><span class="sxs-lookup"><span data-stu-id="ec309-132">The type of preferred application group type, default to Desktop Application Group</span></span>

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

### <span data-ttu-id="ec309-133">-RegistrationInfoExpirationTime</span><span class="sxs-lookup"><span data-stu-id="ec309-133">-RegistrationInfoExpirationTime</span></span>
<span data-ttu-id="ec309-134">Ora di scadenza del token di registrazione.</span><span class="sxs-lookup"><span data-stu-id="ec309-134">Expiration time of registration token.</span></span>

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

### <span data-ttu-id="ec309-135">-RegistrationInfoRegistrationTokenOperation</span><span class="sxs-lookup"><span data-stu-id="ec309-135">-RegistrationInfoRegistrationTokenOperation</span></span>
<span data-ttu-id="ec309-136">Tipo di reimpostazione del token.</span><span class="sxs-lookup"><span data-stu-id="ec309-136">The type of resetting the token.</span></span>

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

### <span data-ttu-id="ec309-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec309-137">-ResourceGroupName</span></span>
<span data-ttu-id="ec309-138">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ec309-138">The name of the resource group.</span></span>
<span data-ttu-id="ec309-139">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="ec309-139">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ec309-140">-Anello</span><span class="sxs-lookup"><span data-stu-id="ec309-140">-Ring</span></span>
<span data-ttu-id="ec309-141">Il numero di anello di HostPool.</span><span class="sxs-lookup"><span data-stu-id="ec309-141">The ring number of HostPool.</span></span>

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

### <span data-ttu-id="ec309-142">-SsoadfsAuthority</span><span class="sxs-lookup"><span data-stu-id="ec309-142">-SsoadfsAuthority</span></span>
<span data-ttu-id="ec309-143">URL del server ADFS del cliente per la firma dei certificati SSO WVD.</span><span class="sxs-lookup"><span data-stu-id="ec309-143">URL to customer ADFS server for signing WVD SSO certificates.</span></span>

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

### <span data-ttu-id="ec309-144">-SsoClientId</span><span class="sxs-lookup"><span data-stu-id="ec309-144">-SsoClientId</span></span>
<span data-ttu-id="ec309-145">ClientId per il relying party registrato usato per emettere certificati SSO WVD.</span><span class="sxs-lookup"><span data-stu-id="ec309-145">ClientId for the registered Relying Party used to issue WVD SSO certificates.</span></span>

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

### <span data-ttu-id="ec309-146">-SsoClientSecretKeyVaultPath</span><span class="sxs-lookup"><span data-stu-id="ec309-146">-SsoClientSecretKeyVaultPath</span></span>
<span data-ttu-id="ec309-147">Percorso di Azure KeyVault che archivia il segreto usato per la comunicazione in ADFS.</span><span class="sxs-lookup"><span data-stu-id="ec309-147">Path to Azure KeyVault storing the secret used for communication to ADFS.</span></span>

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

### <span data-ttu-id="ec309-148">-SsoContext</span><span class="sxs-lookup"><span data-stu-id="ec309-148">-SsoContext</span></span>
<span data-ttu-id="ec309-149">Percorso di keyvault contenente segreto ssoContext.</span><span class="sxs-lookup"><span data-stu-id="ec309-149">Path to keyvault containing ssoContext secret.</span></span>

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

### <span data-ttu-id="ec309-150">-SsoSecretType</span><span class="sxs-lookup"><span data-stu-id="ec309-150">-SsoSecretType</span></span>
<span data-ttu-id="ec309-151">Il tipo di Single #A0 Tipo di segreto.</span><span class="sxs-lookup"><span data-stu-id="ec309-151">The type of single sign on Secret Type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.SsoSecretType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec309-152">-StartVMOnConnect</span><span class="sxs-lookup"><span data-stu-id="ec309-152">-StartVMOnConnect</span></span>
<span data-ttu-id="ec309-153">Il contrassegno per attivare/disattivare la funzionalità StartVMOnConnect.</span><span class="sxs-lookup"><span data-stu-id="ec309-153">The flag to turn on/off StartVMOnConnect feature.</span></span>

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

### <span data-ttu-id="ec309-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ec309-154">-SubscriptionId</span></span>
<span data-ttu-id="ec309-155">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ec309-155">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ec309-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="ec309-156">-Tag</span></span>
<span data-ttu-id="ec309-157">Tag da aggiornare</span><span class="sxs-lookup"><span data-stu-id="ec309-157">tags to be updated</span></span>

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

### <span data-ttu-id="ec309-158">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="ec309-158">-ValidationEnvironment</span></span>
<span data-ttu-id="ec309-159">Ambiente di convalida.</span><span class="sxs-lookup"><span data-stu-id="ec309-159">Is validation environment.</span></span>

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

### <span data-ttu-id="ec309-160">-VMTemplate</span><span class="sxs-lookup"><span data-stu-id="ec309-160">-VMTemplate</span></span>
<span data-ttu-id="ec309-161">Modello DI VM per la configurazione sessionhosts all'interno di hostpool.</span><span class="sxs-lookup"><span data-stu-id="ec309-161">VM template for sessionhosts configuration within hostpool.</span></span>

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

### <span data-ttu-id="ec309-162">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ec309-162">-Confirm</span></span>
<span data-ttu-id="ec309-163">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec309-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec309-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec309-164">-WhatIf</span></span>
<span data-ttu-id="ec309-165">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ec309-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec309-166">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ec309-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec309-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec309-167">CommonParameters</span></span>
<span data-ttu-id="ec309-168">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec309-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec309-169">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ec309-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec309-170">INPUT</span><span class="sxs-lookup"><span data-stu-id="ec309-170">INPUTS</span></span>

### <span data-ttu-id="ec309-171">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="ec309-171">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="ec309-172">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ec309-172">OUTPUTS</span></span>

### <span data-ttu-id="ec309-173">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span><span class="sxs-lookup"><span data-stu-id="ec309-173">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span></span>

## <span data-ttu-id="ec309-174">NOTE</span><span class="sxs-lookup"><span data-stu-id="ec309-174">NOTES</span></span>

<span data-ttu-id="ec309-175">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ec309-175">ALIASES</span></span>

<span data-ttu-id="ec309-176">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="ec309-176">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ec309-177">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="ec309-177">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ec309-178">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ec309-178">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ec309-179">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="ec309-179">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ec309-180">`[ApplicationGroupName <String>]`: nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="ec309-180">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="ec309-181">`[ApplicationName <String>]`: nome dell'applicazione all'interno del gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="ec309-181">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="ec309-182">`[DesktopName <String>]`: nome del desktop all'interno del gruppo di desktop specificato</span><span class="sxs-lookup"><span data-stu-id="ec309-182">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="ec309-183">`[HostPoolName <String>]`: nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="ec309-183">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="ec309-184">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="ec309-184">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ec309-185">`[MsixPackageFullName <String>]`: nome completo del pacchetto specifico della versione del pacchetto MSIX all'interno dello pool host specificato</span><span class="sxs-lookup"><span data-stu-id="ec309-185">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="ec309-186">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ec309-186">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ec309-187">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="ec309-187">The name is case insensitive.</span></span>
  - <span data-ttu-id="ec309-188">`[SessionHostName <String>]`: nome dell'host di sessione all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="ec309-188">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="ec309-189">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ec309-189">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="ec309-190">`[UserSessionId <String>]`: nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="ec309-190">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="ec309-191">`[WorkspaceName <String>]`: nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="ec309-191">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="ec309-192">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ec309-192">RELATED LINKS</span></span>

