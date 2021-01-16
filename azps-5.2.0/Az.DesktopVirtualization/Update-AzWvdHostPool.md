---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
ms.openlocfilehash: a6c7572808184f3c83037932f45d36c7af3ff7a5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341071"
---
# <span data-ttu-id="15a96-101">Update-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="15a96-101">Update-AzWvdHostPool</span></span>

## <span data-ttu-id="15a96-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="15a96-102">SYNOPSIS</span></span>
<span data-ttu-id="15a96-103">Aggiornare un pool host.</span><span class="sxs-lookup"><span data-stu-id="15a96-103">Update a host pool.</span></span>

## <span data-ttu-id="15a96-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="15a96-104">SYNTAX</span></span>

### <span data-ttu-id="15a96-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="15a96-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-CustomRdpProperty <String>] [-Description <String>] [-FriendlyName <String>]
 [-LoadBalancerType <LoadBalancerType>] [-MaxSessionLimit <Int32>]
 [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>]
 [-PreferredAppGroupType <PreferredAppGroupType>] [-RegistrationInfoExpirationTime <DateTime>]
 [-RegistrationInfoRegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>]
 [-SsoadfsAuthority <String>] [-SsoClientId <String>] [-SsoClientSecretKeyVaultPath <String>]
 [-SsoContext <String>] [-SsoSecretType <SsoSecretType>] [-Tag <Hashtable>] [-ValidationEnvironment]
 [-VMTemplate <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="15a96-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="15a96-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-CustomRdpProperty <String>]
 [-Description <String>] [-FriendlyName <String>] [-LoadBalancerType <LoadBalancerType>]
 [-MaxSessionLimit <Int32>] [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>]
 [-PreferredAppGroupType <PreferredAppGroupType>] [-RegistrationInfoExpirationTime <DateTime>]
 [-RegistrationInfoRegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>]
 [-SsoadfsAuthority <String>] [-SsoClientId <String>] [-SsoClientSecretKeyVaultPath <String>]
 [-SsoContext <String>] [-SsoSecretType <SsoSecretType>] [-Tag <Hashtable>] [-ValidationEnvironment]
 [-VMTemplate <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="15a96-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="15a96-107">DESCRIPTION</span></span>
<span data-ttu-id="15a96-108">Aggiornare un pool host.</span><span class="sxs-lookup"><span data-stu-id="15a96-108">Update a host pool.</span></span>

## <span data-ttu-id="15a96-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="15a96-109">EXAMPLES</span></span>

### <span data-ttu-id="15a96-110">Esempio 1: aggiornare un desktop di Windows Virtual HostPool per nome</span><span class="sxs-lookup"><span data-stu-id="15a96-110">Example 1: Update a Windows Virtual Desktop HostPool by name</span></span>
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

<span data-ttu-id="15a96-111">Questo comando aggiorna un HostPool desktop virtuale di Windows in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="15a96-111">This command updates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="15a96-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="15a96-112">PARAMETERS</span></span>

### <span data-ttu-id="15a96-113">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="15a96-113">-CustomRdpProperty</span></span>
<span data-ttu-id="15a96-114">Proprietà RDP personalizzata di HostPool.</span><span class="sxs-lookup"><span data-stu-id="15a96-114">Custom rdp property of HostPool.</span></span>

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

### <span data-ttu-id="15a96-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15a96-115">-DefaultProfile</span></span>
<span data-ttu-id="15a96-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="15a96-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15a96-117">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="15a96-117">-Description</span></span>
<span data-ttu-id="15a96-118">Descrizione di HostPool.</span><span class="sxs-lookup"><span data-stu-id="15a96-118">Description of HostPool.</span></span>

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

### <span data-ttu-id="15a96-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="15a96-119">-FriendlyName</span></span>
<span data-ttu-id="15a96-120">Nome descrittivo di HostPool.</span><span class="sxs-lookup"><span data-stu-id="15a96-120">Friendly name of HostPool.</span></span>

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

### <span data-ttu-id="15a96-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="15a96-121">-InputObject</span></span>
<span data-ttu-id="15a96-122">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="15a96-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="15a96-123">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="15a96-123">-LoadBalancerType</span></span>
<span data-ttu-id="15a96-124">Tipo di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="15a96-124">The type of the load balancer.</span></span>

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

### <span data-ttu-id="15a96-125">-MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="15a96-125">-MaxSessionLimit</span></span>
<span data-ttu-id="15a96-126">Limite massimo della sessione di HostPool.</span><span class="sxs-lookup"><span data-stu-id="15a96-126">The max session limit of HostPool.</span></span>

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

### <span data-ttu-id="15a96-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="15a96-127">-Name</span></span>
<span data-ttu-id="15a96-128">Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="15a96-128">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="15a96-129">-PersonalDesktopAssignmentType</span><span class="sxs-lookup"><span data-stu-id="15a96-129">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="15a96-130">Tipo PersonalDesktopAssignment per HostPool.</span><span class="sxs-lookup"><span data-stu-id="15a96-130">PersonalDesktopAssignment type for HostPool.</span></span>

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

### <span data-ttu-id="15a96-131">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="15a96-131">-PreferredAppGroupType</span></span>
<span data-ttu-id="15a96-132">Tipo di tipo di gruppo di applicazioni preferito, predefinito per il gruppo applicazione desktop</span><span class="sxs-lookup"><span data-stu-id="15a96-132">The type of preferred application group type, default to Desktop Application Group</span></span>

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

### <span data-ttu-id="15a96-133">-RegistrationInfoExpirationTime</span><span class="sxs-lookup"><span data-stu-id="15a96-133">-RegistrationInfoExpirationTime</span></span>
<span data-ttu-id="15a96-134">Data di scadenza del token di registrazione.</span><span class="sxs-lookup"><span data-stu-id="15a96-134">Expiration time of registration token.</span></span>

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

### <span data-ttu-id="15a96-135">-RegistrationInfoRegistrationTokenOperation</span><span class="sxs-lookup"><span data-stu-id="15a96-135">-RegistrationInfoRegistrationTokenOperation</span></span>
<span data-ttu-id="15a96-136">Tipo di reimpostazione del token.</span><span class="sxs-lookup"><span data-stu-id="15a96-136">The type of resetting the token.</span></span>

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

### <span data-ttu-id="15a96-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15a96-137">-ResourceGroupName</span></span>
<span data-ttu-id="15a96-138">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="15a96-138">The name of the resource group.</span></span>
<span data-ttu-id="15a96-139">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="15a96-139">The name is case insensitive.</span></span>

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

### <span data-ttu-id="15a96-140">-Ring</span><span class="sxs-lookup"><span data-stu-id="15a96-140">-Ring</span></span>
<span data-ttu-id="15a96-141">Numero ring di HostPool.</span><span class="sxs-lookup"><span data-stu-id="15a96-141">The ring number of HostPool.</span></span>

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

### <span data-ttu-id="15a96-142">-SsoadfsAuthority</span><span class="sxs-lookup"><span data-stu-id="15a96-142">-SsoadfsAuthority</span></span>
<span data-ttu-id="15a96-143">URL del server ADFS per la firma di certificati SSO WVD.</span><span class="sxs-lookup"><span data-stu-id="15a96-143">URL to customer ADFS server for signing WVD SSO certificates.</span></span>

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

### <span data-ttu-id="15a96-144">-SsoClientId</span><span class="sxs-lookup"><span data-stu-id="15a96-144">-SsoClientId</span></span>
<span data-ttu-id="15a96-145">ClientID per il componente registrato usato per emettere certificati SSO WVD.</span><span class="sxs-lookup"><span data-stu-id="15a96-145">ClientId for the registered Relying Party used to issue WVD SSO certificates.</span></span>

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

### <span data-ttu-id="15a96-146">-SsoClientSecretKeyVaultPath</span><span class="sxs-lookup"><span data-stu-id="15a96-146">-SsoClientSecretKeyVaultPath</span></span>
<span data-ttu-id="15a96-147">Percorso di Azure Vault archiviazione del segreto usato per la comunicazione ad ADFS.</span><span class="sxs-lookup"><span data-stu-id="15a96-147">Path to Azure KeyVault storing the secret used for communication to ADFS.</span></span>

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

### <span data-ttu-id="15a96-148">-SsoContext</span><span class="sxs-lookup"><span data-stu-id="15a96-148">-SsoContext</span></span>
<span data-ttu-id="15a96-149">Percorso di un Vault contenente ssoContext segreto.</span><span class="sxs-lookup"><span data-stu-id="15a96-149">Path to keyvault containing ssoContext secret.</span></span>

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

### <span data-ttu-id="15a96-150">-SsoSecretType</span><span class="sxs-lookup"><span data-stu-id="15a96-150">-SsoSecretType</span></span>
<span data-ttu-id="15a96-151">Tipo di tipo Single Sign-on segreto.</span><span class="sxs-lookup"><span data-stu-id="15a96-151">The type of single sign on Secret Type.</span></span>

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

### <span data-ttu-id="15a96-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="15a96-152">-SubscriptionId</span></span>
<span data-ttu-id="15a96-153">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="15a96-153">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="15a96-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="15a96-154">-Tag</span></span>
<span data-ttu-id="15a96-155">Tag da aggiornare</span><span class="sxs-lookup"><span data-stu-id="15a96-155">tags to be updated</span></span>

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

### <span data-ttu-id="15a96-156">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="15a96-156">-ValidationEnvironment</span></span>
<span data-ttu-id="15a96-157">È l'ambiente di convalida.</span><span class="sxs-lookup"><span data-stu-id="15a96-157">Is validation environment.</span></span>

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

### <span data-ttu-id="15a96-158">-VMTemplate</span><span class="sxs-lookup"><span data-stu-id="15a96-158">-VMTemplate</span></span>
<span data-ttu-id="15a96-159">Modello VM per la configurazione di sessionhosts all'interno di hostpool.</span><span class="sxs-lookup"><span data-stu-id="15a96-159">VM template for sessionhosts configuration within hostpool.</span></span>

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

### <span data-ttu-id="15a96-160">-Confermare</span><span class="sxs-lookup"><span data-stu-id="15a96-160">-Confirm</span></span>
<span data-ttu-id="15a96-161">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15a96-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15a96-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15a96-162">-WhatIf</span></span>
<span data-ttu-id="15a96-163">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="15a96-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15a96-164">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="15a96-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15a96-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15a96-165">CommonParameters</span></span>
<span data-ttu-id="15a96-166">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15a96-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15a96-167">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="15a96-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15a96-168">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="15a96-168">INPUTS</span></span>

### <span data-ttu-id="15a96-169">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="15a96-169">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="15a96-170">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="15a96-170">OUTPUTS</span></span>

### <span data-ttu-id="15a96-171">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20201019Preview. IHostPool</span><span class="sxs-lookup"><span data-stu-id="15a96-171">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IHostPool</span></span>

## <span data-ttu-id="15a96-172">Note</span><span class="sxs-lookup"><span data-stu-id="15a96-172">NOTES</span></span>

<span data-ttu-id="15a96-173">ALIAS</span><span class="sxs-lookup"><span data-stu-id="15a96-173">ALIASES</span></span>

<span data-ttu-id="15a96-174">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="15a96-174">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="15a96-175">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="15a96-175">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="15a96-176">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="15a96-176">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="15a96-177">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="15a96-177">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="15a96-178">`[ApplicationGroupName <String>]`: Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="15a96-178">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="15a96-179">`[ApplicationName <String>]`: Nome dell'applicazione nel gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="15a96-179">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="15a96-180">`[DesktopName <String>]`: Nome del desktop nel gruppo desktop specificato</span><span class="sxs-lookup"><span data-stu-id="15a96-180">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="15a96-181">`[HostPoolName <String>]`: Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="15a96-181">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="15a96-182">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="15a96-182">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="15a96-183">`[MsixPackageFullName <String>]`: Pacchetto specifico della versione nome completo del pacchetto MSIX all'interno di hostpool specificato</span><span class="sxs-lookup"><span data-stu-id="15a96-183">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="15a96-184">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="15a96-184">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="15a96-185">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="15a96-185">The name is case insensitive.</span></span>
  - <span data-ttu-id="15a96-186">`[SessionHostName <String>]`: Nome dell'host di sessione nel pool di host specificato</span><span class="sxs-lookup"><span data-stu-id="15a96-186">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="15a96-187">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="15a96-187">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="15a96-188">`[UserSessionId <String>]`: Nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="15a96-188">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="15a96-189">`[WorkspaceName <String>]`: Nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="15a96-189">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="15a96-190">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="15a96-190">RELATED LINKS</span></span>

