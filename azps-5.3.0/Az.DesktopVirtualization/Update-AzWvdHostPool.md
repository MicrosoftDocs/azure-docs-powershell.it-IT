---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
ms.openlocfilehash: e6b77d9d779931d9b50de2b504b357ecd22a2b92
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476361"
---
# <span data-ttu-id="160d5-101">Update-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="160d5-101">Update-AzWvdHostPool</span></span>

## <span data-ttu-id="160d5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="160d5-102">SYNOPSIS</span></span>
<span data-ttu-id="160d5-103">Aggiornare un pool host.</span><span class="sxs-lookup"><span data-stu-id="160d5-103">Update a host pool.</span></span>

## <span data-ttu-id="160d5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="160d5-104">SYNTAX</span></span>

### <span data-ttu-id="160d5-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="160d5-105">UpdateExpanded (Default)</span></span>
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

### <span data-ttu-id="160d5-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="160d5-106">UpdateViaIdentityExpanded</span></span>
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

## <span data-ttu-id="160d5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="160d5-107">DESCRIPTION</span></span>
<span data-ttu-id="160d5-108">Aggiornare un pool host.</span><span class="sxs-lookup"><span data-stu-id="160d5-108">Update a host pool.</span></span>

## <span data-ttu-id="160d5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="160d5-109">EXAMPLES</span></span>

### <span data-ttu-id="160d5-110">Esempio 1: aggiornare un desktop di Windows Virtual HostPool per nome</span><span class="sxs-lookup"><span data-stu-id="160d5-110">Example 1: Update a Windows Virtual Desktop HostPool by name</span></span>
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

<span data-ttu-id="160d5-111">Questo comando aggiorna un HostPool desktop virtuale di Windows in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="160d5-111">This command updates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="160d5-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="160d5-112">PARAMETERS</span></span>

### <span data-ttu-id="160d5-113">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="160d5-113">-CustomRdpProperty</span></span>
<span data-ttu-id="160d5-114">Proprietà RDP personalizzata di HostPool.</span><span class="sxs-lookup"><span data-stu-id="160d5-114">Custom rdp property of HostPool.</span></span>

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

### <span data-ttu-id="160d5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="160d5-115">-DefaultProfile</span></span>
<span data-ttu-id="160d5-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="160d5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="160d5-117">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="160d5-117">-Description</span></span>
<span data-ttu-id="160d5-118">Descrizione di HostPool.</span><span class="sxs-lookup"><span data-stu-id="160d5-118">Description of HostPool.</span></span>

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

### <span data-ttu-id="160d5-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="160d5-119">-FriendlyName</span></span>
<span data-ttu-id="160d5-120">Nome descrittivo di HostPool.</span><span class="sxs-lookup"><span data-stu-id="160d5-120">Friendly name of HostPool.</span></span>

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

### <span data-ttu-id="160d5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="160d5-121">-InputObject</span></span>
<span data-ttu-id="160d5-122">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="160d5-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="160d5-123">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="160d5-123">-LoadBalancerType</span></span>
<span data-ttu-id="160d5-124">Tipo di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="160d5-124">The type of the load balancer.</span></span>

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

### <span data-ttu-id="160d5-125">-MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="160d5-125">-MaxSessionLimit</span></span>
<span data-ttu-id="160d5-126">Limite massimo della sessione di HostPool.</span><span class="sxs-lookup"><span data-stu-id="160d5-126">The max session limit of HostPool.</span></span>

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

### <span data-ttu-id="160d5-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="160d5-127">-Name</span></span>
<span data-ttu-id="160d5-128">Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="160d5-128">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="160d5-129">-PersonalDesktopAssignmentType</span><span class="sxs-lookup"><span data-stu-id="160d5-129">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="160d5-130">Tipo PersonalDesktopAssignment per HostPool.</span><span class="sxs-lookup"><span data-stu-id="160d5-130">PersonalDesktopAssignment type for HostPool.</span></span>

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

### <span data-ttu-id="160d5-131">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="160d5-131">-PreferredAppGroupType</span></span>
<span data-ttu-id="160d5-132">Tipo di tipo di gruppo di applicazioni preferito, predefinito per il gruppo applicazione desktop</span><span class="sxs-lookup"><span data-stu-id="160d5-132">The type of preferred application group type, default to Desktop Application Group</span></span>

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

### <span data-ttu-id="160d5-133">-RegistrationInfoExpirationTime</span><span class="sxs-lookup"><span data-stu-id="160d5-133">-RegistrationInfoExpirationTime</span></span>
<span data-ttu-id="160d5-134">Data di scadenza del token di registrazione.</span><span class="sxs-lookup"><span data-stu-id="160d5-134">Expiration time of registration token.</span></span>

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

### <span data-ttu-id="160d5-135">-RegistrationInfoRegistrationTokenOperation</span><span class="sxs-lookup"><span data-stu-id="160d5-135">-RegistrationInfoRegistrationTokenOperation</span></span>
<span data-ttu-id="160d5-136">Tipo di reimpostazione del token.</span><span class="sxs-lookup"><span data-stu-id="160d5-136">The type of resetting the token.</span></span>

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

### <span data-ttu-id="160d5-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="160d5-137">-ResourceGroupName</span></span>
<span data-ttu-id="160d5-138">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="160d5-138">The name of the resource group.</span></span>
<span data-ttu-id="160d5-139">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="160d5-139">The name is case insensitive.</span></span>

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

### <span data-ttu-id="160d5-140">-Ring</span><span class="sxs-lookup"><span data-stu-id="160d5-140">-Ring</span></span>
<span data-ttu-id="160d5-141">Numero ring di HostPool.</span><span class="sxs-lookup"><span data-stu-id="160d5-141">The ring number of HostPool.</span></span>

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

### <span data-ttu-id="160d5-142">-SsoadfsAuthority</span><span class="sxs-lookup"><span data-stu-id="160d5-142">-SsoadfsAuthority</span></span>
<span data-ttu-id="160d5-143">URL del server ADFS per la firma di certificati SSO WVD.</span><span class="sxs-lookup"><span data-stu-id="160d5-143">URL to customer ADFS server for signing WVD SSO certificates.</span></span>

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

### <span data-ttu-id="160d5-144">-SsoClientId</span><span class="sxs-lookup"><span data-stu-id="160d5-144">-SsoClientId</span></span>
<span data-ttu-id="160d5-145">ClientID per il componente registrato usato per emettere certificati SSO WVD.</span><span class="sxs-lookup"><span data-stu-id="160d5-145">ClientId for the registered Relying Party used to issue WVD SSO certificates.</span></span>

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

### <span data-ttu-id="160d5-146">-SsoClientSecretKeyVaultPath</span><span class="sxs-lookup"><span data-stu-id="160d5-146">-SsoClientSecretKeyVaultPath</span></span>
<span data-ttu-id="160d5-147">Percorso di Azure Vault archiviazione del segreto usato per la comunicazione ad ADFS.</span><span class="sxs-lookup"><span data-stu-id="160d5-147">Path to Azure KeyVault storing the secret used for communication to ADFS.</span></span>

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

### <span data-ttu-id="160d5-148">-SsoContext</span><span class="sxs-lookup"><span data-stu-id="160d5-148">-SsoContext</span></span>
<span data-ttu-id="160d5-149">Percorso di un Vault contenente ssoContext segreto.</span><span class="sxs-lookup"><span data-stu-id="160d5-149">Path to keyvault containing ssoContext secret.</span></span>

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

### <span data-ttu-id="160d5-150">-SsoSecretType</span><span class="sxs-lookup"><span data-stu-id="160d5-150">-SsoSecretType</span></span>
<span data-ttu-id="160d5-151">Tipo di tipo Single Sign-on segreto.</span><span class="sxs-lookup"><span data-stu-id="160d5-151">The type of single sign on Secret Type.</span></span>

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

### <span data-ttu-id="160d5-152">-StartVMOnConnect</span><span class="sxs-lookup"><span data-stu-id="160d5-152">-StartVMOnConnect</span></span>
<span data-ttu-id="160d5-153">Il contrassegno per attivare/disattivare la caratteristica StartVMOnConnect.</span><span class="sxs-lookup"><span data-stu-id="160d5-153">The flag to turn on/off StartVMOnConnect feature.</span></span>

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

### <span data-ttu-id="160d5-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="160d5-154">-SubscriptionId</span></span>
<span data-ttu-id="160d5-155">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="160d5-155">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="160d5-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="160d5-156">-Tag</span></span>
<span data-ttu-id="160d5-157">Tag da aggiornare</span><span class="sxs-lookup"><span data-stu-id="160d5-157">tags to be updated</span></span>

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

### <span data-ttu-id="160d5-158">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="160d5-158">-ValidationEnvironment</span></span>
<span data-ttu-id="160d5-159">È l'ambiente di convalida.</span><span class="sxs-lookup"><span data-stu-id="160d5-159">Is validation environment.</span></span>

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

### <span data-ttu-id="160d5-160">-VMTemplate</span><span class="sxs-lookup"><span data-stu-id="160d5-160">-VMTemplate</span></span>
<span data-ttu-id="160d5-161">Modello VM per la configurazione di sessionhosts all'interno di hostpool.</span><span class="sxs-lookup"><span data-stu-id="160d5-161">VM template for sessionhosts configuration within hostpool.</span></span>

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

### <span data-ttu-id="160d5-162">-Confermare</span><span class="sxs-lookup"><span data-stu-id="160d5-162">-Confirm</span></span>
<span data-ttu-id="160d5-163">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="160d5-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="160d5-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="160d5-164">-WhatIf</span></span>
<span data-ttu-id="160d5-165">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="160d5-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="160d5-166">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="160d5-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="160d5-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="160d5-167">CommonParameters</span></span>
<span data-ttu-id="160d5-168">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="160d5-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="160d5-169">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="160d5-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="160d5-170">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="160d5-170">INPUTS</span></span>

### <span data-ttu-id="160d5-171">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="160d5-171">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="160d5-172">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="160d5-172">OUTPUTS</span></span>

### <span data-ttu-id="160d5-173">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20201102Preview. IHostPool</span><span class="sxs-lookup"><span data-stu-id="160d5-173">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span></span>

## <span data-ttu-id="160d5-174">Note</span><span class="sxs-lookup"><span data-stu-id="160d5-174">NOTES</span></span>

<span data-ttu-id="160d5-175">ALIAS</span><span class="sxs-lookup"><span data-stu-id="160d5-175">ALIASES</span></span>

<span data-ttu-id="160d5-176">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="160d5-176">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="160d5-177">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="160d5-177">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="160d5-178">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="160d5-178">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="160d5-179">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="160d5-179">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="160d5-180">`[ApplicationGroupName <String>]`: Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="160d5-180">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="160d5-181">`[ApplicationName <String>]`: Nome dell'applicazione nel gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="160d5-181">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="160d5-182">`[DesktopName <String>]`: Nome del desktop nel gruppo desktop specificato</span><span class="sxs-lookup"><span data-stu-id="160d5-182">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="160d5-183">`[HostPoolName <String>]`: Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="160d5-183">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="160d5-184">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="160d5-184">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="160d5-185">`[MsixPackageFullName <String>]`: Pacchetto specifico della versione nome completo del pacchetto MSIX all'interno di hostpool specificato</span><span class="sxs-lookup"><span data-stu-id="160d5-185">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="160d5-186">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="160d5-186">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="160d5-187">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="160d5-187">The name is case insensitive.</span></span>
  - <span data-ttu-id="160d5-188">`[SessionHostName <String>]`: Nome dell'host di sessione nel pool di host specificato</span><span class="sxs-lookup"><span data-stu-id="160d5-188">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="160d5-189">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="160d5-189">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="160d5-190">`[UserSessionId <String>]`: Nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="160d5-190">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="160d5-191">`[WorkspaceName <String>]`: Nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="160d5-191">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="160d5-192">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="160d5-192">RELATED LINKS</span></span>

