---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdHostPool.md
ms.openlocfilehash: 6f579dfcba74f68eafaa149be15649e496c46f82
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475360"
---
# <span data-ttu-id="e3aa7-101">New-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="e3aa7-101">New-AzWvdHostPool</span></span>

## <span data-ttu-id="e3aa7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e3aa7-102">SYNOPSIS</span></span>
<span data-ttu-id="e3aa7-103">Creare o aggiornare un pool host.</span><span class="sxs-lookup"><span data-stu-id="e3aa7-103">Create or update a host pool.</span></span>

## <span data-ttu-id="e3aa7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e3aa7-104">SYNTAX</span></span>

### <span data-ttu-id="e3aa7-105">CreateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e3aa7-105">CreateExpanded (Default)</span></span>
```
New-AzWvdHostPool -HostPoolType <HostPoolType> -LoadBalancerType <LoadBalancerType> -Location <String>
 -Name <String> -PreferredAppGroupType <PreferredAppGroupType> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-CustomRdpProperty <String>] [-Description <String>] [-ExpirationTime <DateTime>]
 [-FriendlyName <String>] [-MaxSessionLimit <Int32>]
 [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>] [-RegistrationInfoToken <String>]
 [-RegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>] [-SsoadfsAuthority <String>]
 [-SsoClientId <String>] [-SsoClientSecretKeyVaultPath <String>] [-SsoContext <String>]
 [-SsoSecretType <SsoSecretType>] [-StartVMOnConnect] [-Tag <Hashtable>] [-ValidationEnvironment]
 [-VMTemplate <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e3aa7-106">FullSenerioCreate</span><span class="sxs-lookup"><span data-stu-id="e3aa7-106">FullSenerioCreate</span></span>
```
New-AzWvdHostPool -HostPoolType <HostPoolType> -LoadBalancerType <LoadBalancerType> -Location <String>
 -Name <String> -PreferredAppGroupType <PreferredAppGroupType> -ResourceGroupName <String>
 [-DesktopAppGroupName <String>] [-SubscriptionId <String>] [-WorkspaceName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e3aa7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3aa7-107">DESCRIPTION</span></span>
<span data-ttu-id="e3aa7-108">Creare o aggiornare un pool host.</span><span class="sxs-lookup"><span data-stu-id="e3aa7-108">Create or update a host pool.</span></span>

## <span data-ttu-id="e3aa7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e3aa7-109">EXAMPLES</span></span>

### <span data-ttu-id="e3aa7-110">Esempio 1: creare un desktop virtuale di Windows HostPool per nome</span><span class="sxs-lookup"><span data-stu-id="e3aa7-110">Example 1: Create a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> New-AzWvdHostPool -ResourceGroupName ResourceGroupName `
                            -Name HostPoolName `
                            -Location 'eastus' `
                            -HostPoolType 'Pooled' `
                            -LoadBalancerType 'DepthFirst' `
                            -RegistrationTokenOperation 'Update' `
                            -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ')) `
                            -Description 'Description' `
                            -FriendlyName 'Friendly Name' `
                            -MaxSessionLimit 5 `
                            -VMTemplate $null `
                            -SsoContext $null `
                            -SsoClientId $null `
                            -SsoClientSecretKeyVaultPath $null `
                            -SsoSecretType $null `
                            -SsoadfsAuthority $null `
                            -CustomRdpProperty $null `
                            -Ring $null `
                            -ValidationEnvironment:$false

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="e3aa7-111">Questo comando crea un HostPool desktop virtuale di Windows in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e3aa7-111">This command creates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

### <span data-ttu-id="e3aa7-112">Esempio 1: creare un desktop virtuale di Windows HostPool per nome</span><span class="sxs-lookup"><span data-stu-id="e3aa7-112">Example 1: Create a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> New-AzWvdHostPool -ResourceGroupName ResourceGroupName `
                            -Name HostPoolName `
                            -Location 'eastus' `
                            -HostPoolType 'Personal' `
                            -LoadBalancerType 'Persistent' `
                            -RegistrationTokenOperation 'Update' `
                            -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ')) `
                            -Description 'Description' `
                            -FriendlyName 'Friendly Name' `
                            -MaxSessionLimit 5 `
                            -VMTemplate $null `
                            -SsoContext $null `
                            -SsoClientId $null `
                            -SsoClientSecretKeyVaultPath $null `
                            -SsoSecretType $null `
                            -SsoadfsAuthority $null `
                            -CustomRdpProperty $null `
                            -Ring $null `
                            -ValidationEnvironment:$false

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="e3aa7-113">Questo comando crea un HostPool desktop virtuale di Windows in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e3aa7-113">This command creates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="e3aa7-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e3aa7-114">PARAMETERS</span></span>

### <span data-ttu-id="e3aa7-115">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="e3aa7-115">-CustomRdpProperty</span></span>
<span data-ttu-id="e3aa7-116">Proprietà RDP personalizzata di HostPool.</span><span class="sxs-lookup"><span data-stu-id="e3aa7-116">Custom rdp property of HostPool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3aa7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3aa7-117">-DefaultProfile</span></span>
<span data-ttu-id="e3aa7-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e3aa7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3aa7-119">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3aa7-119">-Description</span></span>
<span data-ttu-id="e3aa7-120">Descrizione di HostPool.</span><span class="sxs-lookup"><span data-stu-id="e3aa7-120">Description of HostPool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3aa7-121">-DesktopAppGroupName</span><span class="sxs-lookup"><span data-stu-id="e3aa7-121">-DesktopAppGroupName</span></span>
<span data-ttu-id="e3aa7-122">Nome gruppo app desktop</span><span class="sxs-lookup"><span data-stu-id="e3aa7-122">Desktop App Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FullSenerioCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3aa7-123">-ExpirationTime</span><span class="sxs-lookup"><span data-stu-id="e3aa7-123">-ExpirationTime</span></span>
<span data-ttu-id="e3aa7-124">Data di scadenza del token di registrazione.</span><span class="sxs-lookup"><span data-stu-id="e3aa7-124">Expiration time of registration token.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3aa7-125">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="e3aa7-125">-FriendlyName</span></span>
<span data-ttu-id="e3aa7-126">Nome descrittivo di HostPool.</span><span class="sxs-lookup"><span data-stu-id="e3aa7-126">Friendly name of HostPool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3aa7-127">-HostPoolType</span><span class="sxs-lookup"><span data-stu-id="e3aa7-127">-HostPoolType</span></span>
<span data-ttu-id="e3aa7-128">Tipo HostPool per desktop.</span><span class="sxs-lookup"><span data-stu-id="e3aa7-128">HostPool type for desktop.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.HostPoolType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3aa7-129">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="e3aa7-129">-LoadBalancerType</span></span>
<span data-ttu-id="e3aa7-130">Tipo di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="e3aa7-130">The type of the load balancer.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.LoadBalancerType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3aa7-131">-Posizione</span><span class="sxs-lookup"><span data-stu-id="e3aa7-131">-Location</span></span>
<span data-ttu-id="e3aa7-132">Posizione geografica in cui vive la risorsa</span><span class="sxs-lookup"><span data-stu-id="e3aa7-132">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3aa7-133">-MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="e3aa7-133">-MaxSessionLimit</span></span>
<span data-ttu-id="e3aa7-134">Limite massimo della sessione di HostPool.</span><span class="sxs-lookup"><span data-stu-id="e3aa7-134">The max session limit of HostPool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3aa7-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="e3aa7-135">-Name</span></span>
<span data-ttu-id="e3aa7-136">Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="e3aa7-136">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HostPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3aa7-137">-PersonalDesktopAssignmentType</span><span class="sxs-lookup"><span data-stu-id="e3aa7-137">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="e3aa7-138">Tipo PersonalDesktopAssignment per HostPool.</span><span class="sxs-lookup"><span data-stu-id="e3aa7-138">PersonalDesktopAssignment type for HostPool.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.PersonalDesktopAssignmentType
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3aa7-139">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="e3aa7-139">-PreferredAppGroupType</span></span>
<span data-ttu-id="e3aa7-140">Tipo di tipo di gruppo di applicazioni preferito, predefinito per il gruppo applicazione desktop</span><span class="sxs-lookup"><span data-stu-id="e3aa7-140">The type of preferred application group type, default to Desktop Application Group</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.PreferredAppGroupType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3aa7-141">-RegistrationInfoToken</span><span class="sxs-lookup"><span data-stu-id="e3aa7-141">-RegistrationInfoToken</span></span>
<span data-ttu-id="e3aa7-142">Il token di registrazione stringa con codifica Base64.</span><span class="sxs-lookup"><span data-stu-id="e3aa7-142">The registration token base64 encoded string.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3aa7-143">-RegistrationTokenOperation</span><span class="sxs-lookup"><span data-stu-id="e3aa7-143">-RegistrationTokenOperation</span></span>
<span data-ttu-id="e3aa7-144">Tipo di reimpostazione del token.</span><span class="sxs-lookup"><span data-stu-id="e3aa7-144">The type of resetting the token.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.RegistrationTokenOperation
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3aa7-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3aa7-145">-ResourceGroupName</span></span>
<span data-ttu-id="e3aa7-146">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e3aa7-146">The name of the resource group.</span></span>
<span data-ttu-id="e3aa7-147">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="e3aa7-147">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3aa7-148">-Ring</span><span class="sxs-lookup"><span data-stu-id="e3aa7-148">-Ring</span></span>
<span data-ttu-id="e3aa7-149">Numero ring di HostPool.</span><span class="sxs-lookup"><span data-stu-id="e3aa7-149">The ring number of HostPool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3aa7-150">-SsoadfsAuthority</span><span class="sxs-lookup"><span data-stu-id="e3aa7-150">-SsoadfsAuthority</span></span>
<span data-ttu-id="e3aa7-151">URL del server ADFS per la firma di certificati SSO WVD.</span><span class="sxs-lookup"><span data-stu-id="e3aa7-151">URL to customer ADFS server for signing WVD SSO certificates.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3aa7-152">-SsoClientId</span><span class="sxs-lookup"><span data-stu-id="e3aa7-152">-SsoClientId</span></span>
<span data-ttu-id="e3aa7-153">ClientID per il componente registrato usato per emettere certificati SSO WVD.</span><span class="sxs-lookup"><span data-stu-id="e3aa7-153">ClientId for the registered Relying Party used to issue WVD SSO certificates.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3aa7-154">-SsoClientSecretKeyVaultPath</span><span class="sxs-lookup"><span data-stu-id="e3aa7-154">-SsoClientSecretKeyVaultPath</span></span>
<span data-ttu-id="e3aa7-155">Percorso di Azure Vault archiviazione del segreto usato per la comunicazione ad ADFS.</span><span class="sxs-lookup"><span data-stu-id="e3aa7-155">Path to Azure KeyVault storing the secret used for communication to ADFS.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3aa7-156">-SsoContext</span><span class="sxs-lookup"><span data-stu-id="e3aa7-156">-SsoContext</span></span>
<span data-ttu-id="e3aa7-157">Percorso di un Vault contenente ssoContext segreto.</span><span class="sxs-lookup"><span data-stu-id="e3aa7-157">Path to keyvault containing ssoContext secret.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3aa7-158">-SsoSecretType</span><span class="sxs-lookup"><span data-stu-id="e3aa7-158">-SsoSecretType</span></span>
<span data-ttu-id="e3aa7-159">Tipo di tipo Single Sign-on segreto.</span><span class="sxs-lookup"><span data-stu-id="e3aa7-159">The type of single sign on Secret Type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.SsoSecretType
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3aa7-160">-StartVMOnConnect</span><span class="sxs-lookup"><span data-stu-id="e3aa7-160">-StartVMOnConnect</span></span>
<span data-ttu-id="e3aa7-161">Il contrassegno per attivare/disattivare la caratteristica StartVMOnConnect.</span><span class="sxs-lookup"><span data-stu-id="e3aa7-161">The flag to turn on/off StartVMOnConnect feature.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3aa7-162">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e3aa7-162">-SubscriptionId</span></span>
<span data-ttu-id="e3aa7-163">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e3aa7-163">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3aa7-164">-Tag</span><span class="sxs-lookup"><span data-stu-id="e3aa7-164">-Tag</span></span>
<span data-ttu-id="e3aa7-165">Tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="e3aa7-165">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3aa7-166">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="e3aa7-166">-ValidationEnvironment</span></span>
<span data-ttu-id="e3aa7-167">È l'ambiente di convalida.</span><span class="sxs-lookup"><span data-stu-id="e3aa7-167">Is validation environment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3aa7-168">-VMTemplate</span><span class="sxs-lookup"><span data-stu-id="e3aa7-168">-VMTemplate</span></span>
<span data-ttu-id="e3aa7-169">Modello VM per la configurazione di sessionhosts all'interno di hostpool.</span><span class="sxs-lookup"><span data-stu-id="e3aa7-169">VM template for sessionhosts configuration within hostpool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3aa7-170">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e3aa7-170">-WorkspaceName</span></span>
<span data-ttu-id="e3aa7-171">Nome area di lavoro</span><span class="sxs-lookup"><span data-stu-id="e3aa7-171">Workspace Name</span></span>

```yaml
Type: System.String
Parameter Sets: FullSenerioCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3aa7-172">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e3aa7-172">-Confirm</span></span>
<span data-ttu-id="e3aa7-173">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3aa7-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3aa7-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3aa7-174">-WhatIf</span></span>
<span data-ttu-id="e3aa7-175">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3aa7-175">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3aa7-176">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3aa7-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3aa7-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3aa7-177">CommonParameters</span></span>
<span data-ttu-id="e3aa7-178">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3aa7-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3aa7-179">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3aa7-179">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3aa7-180">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e3aa7-180">INPUTS</span></span>

## <span data-ttu-id="e3aa7-181">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e3aa7-181">OUTPUTS</span></span>

### <span data-ttu-id="e3aa7-182">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20201102Preview. IHostPool</span><span class="sxs-lookup"><span data-stu-id="e3aa7-182">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span></span>

## <span data-ttu-id="e3aa7-183">Note</span><span class="sxs-lookup"><span data-stu-id="e3aa7-183">NOTES</span></span>

<span data-ttu-id="e3aa7-184">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e3aa7-184">ALIASES</span></span>

## <span data-ttu-id="e3aa7-185">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e3aa7-185">RELATED LINKS</span></span>

