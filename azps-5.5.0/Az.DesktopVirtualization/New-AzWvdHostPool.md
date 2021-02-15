---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdHostPool.md
ms.openlocfilehash: 6f579dfcba74f68eafaa149be15649e496c46f82
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204266"
---
# <span data-ttu-id="1c66b-101">New-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="1c66b-101">New-AzWvdHostPool</span></span>

## <span data-ttu-id="1c66b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c66b-102">SYNOPSIS</span></span>
<span data-ttu-id="1c66b-103">Creare o aggiornare un pool host.</span><span class="sxs-lookup"><span data-stu-id="1c66b-103">Create or update a host pool.</span></span>

## <span data-ttu-id="1c66b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1c66b-104">SYNTAX</span></span>

### <span data-ttu-id="1c66b-105">CreateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1c66b-105">CreateExpanded (Default)</span></span>
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

### <span data-ttu-id="1c66b-106">FullSenerioCreate</span><span class="sxs-lookup"><span data-stu-id="1c66b-106">FullSenerioCreate</span></span>
```
New-AzWvdHostPool -HostPoolType <HostPoolType> -LoadBalancerType <LoadBalancerType> -Location <String>
 -Name <String> -PreferredAppGroupType <PreferredAppGroupType> -ResourceGroupName <String>
 [-DesktopAppGroupName <String>] [-SubscriptionId <String>] [-WorkspaceName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1c66b-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1c66b-107">DESCRIPTION</span></span>
<span data-ttu-id="1c66b-108">Creare o aggiornare un pool host.</span><span class="sxs-lookup"><span data-stu-id="1c66b-108">Create or update a host pool.</span></span>

## <span data-ttu-id="1c66b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1c66b-109">EXAMPLES</span></span>

### <span data-ttu-id="1c66b-110">Esempio 1: Creare un pool di desktop virtuali Windows in base al nome</span><span class="sxs-lookup"><span data-stu-id="1c66b-110">Example 1: Create a Windows Virtual Desktop HostPool by name</span></span>
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

<span data-ttu-id="1c66b-111">Questo comando crea un pool di desktop virtuali Windows in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1c66b-111">This command creates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

### <span data-ttu-id="1c66b-112">Esempio 1: Creare un pool di desktop virtuali Windows in base al nome</span><span class="sxs-lookup"><span data-stu-id="1c66b-112">Example 1: Create a Windows Virtual Desktop HostPool by name</span></span>
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

<span data-ttu-id="1c66b-113">Questo comando crea un pool di desktop virtuali Windows in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1c66b-113">This command creates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="1c66b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c66b-114">PARAMETERS</span></span>

### <span data-ttu-id="1c66b-115">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="1c66b-115">-CustomRdpProperty</span></span>
<span data-ttu-id="1c66b-116">Proprietà rdp personalizzata di HostPool.</span><span class="sxs-lookup"><span data-stu-id="1c66b-116">Custom rdp property of HostPool.</span></span>

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

### <span data-ttu-id="1c66b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c66b-117">-DefaultProfile</span></span>
<span data-ttu-id="1c66b-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1c66b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c66b-119">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="1c66b-119">-Description</span></span>
<span data-ttu-id="1c66b-120">Descrizione di HostPool.</span><span class="sxs-lookup"><span data-stu-id="1c66b-120">Description of HostPool.</span></span>

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

### <span data-ttu-id="1c66b-121">-DesktopAppGroupName</span><span class="sxs-lookup"><span data-stu-id="1c66b-121">-DesktopAppGroupName</span></span>
<span data-ttu-id="1c66b-122">Nome gruppo app desktop</span><span class="sxs-lookup"><span data-stu-id="1c66b-122">Desktop App Group Name</span></span>

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

### <span data-ttu-id="1c66b-123">-ExpirationTime</span><span class="sxs-lookup"><span data-stu-id="1c66b-123">-ExpirationTime</span></span>
<span data-ttu-id="1c66b-124">Ora di scadenza del token di registrazione.</span><span class="sxs-lookup"><span data-stu-id="1c66b-124">Expiration time of registration token.</span></span>

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

### <span data-ttu-id="1c66b-125">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="1c66b-125">-FriendlyName</span></span>
<span data-ttu-id="1c66b-126">Nome descrittivo di HostPool.</span><span class="sxs-lookup"><span data-stu-id="1c66b-126">Friendly name of HostPool.</span></span>

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

### <span data-ttu-id="1c66b-127">-HostPoolType</span><span class="sxs-lookup"><span data-stu-id="1c66b-127">-HostPoolType</span></span>
<span data-ttu-id="1c66b-128">Tipo HostPool per desktop.</span><span class="sxs-lookup"><span data-stu-id="1c66b-128">HostPool type for desktop.</span></span>

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

### <span data-ttu-id="1c66b-129">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="1c66b-129">-LoadBalancerType</span></span>
<span data-ttu-id="1c66b-130">Tipo di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="1c66b-130">The type of the load balancer.</span></span>

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

### <span data-ttu-id="1c66b-131">-Location</span><span class="sxs-lookup"><span data-stu-id="1c66b-131">-Location</span></span>
<span data-ttu-id="1c66b-132">Posizione geografica in cui si trova la risorsa</span><span class="sxs-lookup"><span data-stu-id="1c66b-132">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="1c66b-133">-MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="1c66b-133">-MaxSessionLimit</span></span>
<span data-ttu-id="1c66b-134">Limite massimo di sessione di HostPool.</span><span class="sxs-lookup"><span data-stu-id="1c66b-134">The max session limit of HostPool.</span></span>

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

### <span data-ttu-id="1c66b-135">-Name</span><span class="sxs-lookup"><span data-stu-id="1c66b-135">-Name</span></span>
<span data-ttu-id="1c66b-136">Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="1c66b-136">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="1c66b-137">-PersonalDesktopAssignmentType</span><span class="sxs-lookup"><span data-stu-id="1c66b-137">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="1c66b-138">PersonalDesktopAssignment type for HostPool.</span><span class="sxs-lookup"><span data-stu-id="1c66b-138">PersonalDesktopAssignment type for HostPool.</span></span>

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

### <span data-ttu-id="1c66b-139">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="1c66b-139">-PreferredAppGroupType</span></span>
<span data-ttu-id="1c66b-140">Tipo di gruppo di applicazioni preferito, predefinito per Gruppo applicazioni desktop</span><span class="sxs-lookup"><span data-stu-id="1c66b-140">The type of preferred application group type, default to Desktop Application Group</span></span>

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

### <span data-ttu-id="1c66b-141">-RegistrationInfoToken</span><span class="sxs-lookup"><span data-stu-id="1c66b-141">-RegistrationInfoToken</span></span>
<span data-ttu-id="1c66b-142">Stringa codificata base64 del token di registrazione.</span><span class="sxs-lookup"><span data-stu-id="1c66b-142">The registration token base64 encoded string.</span></span>

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

### <span data-ttu-id="1c66b-143">-RegistrationTokenOperation</span><span class="sxs-lookup"><span data-stu-id="1c66b-143">-RegistrationTokenOperation</span></span>
<span data-ttu-id="1c66b-144">Tipo di reimpostazione del token.</span><span class="sxs-lookup"><span data-stu-id="1c66b-144">The type of resetting the token.</span></span>

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

### <span data-ttu-id="1c66b-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c66b-145">-ResourceGroupName</span></span>
<span data-ttu-id="1c66b-146">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1c66b-146">The name of the resource group.</span></span>
<span data-ttu-id="1c66b-147">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="1c66b-147">The name is case insensitive.</span></span>

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

### <span data-ttu-id="1c66b-148">-Anello</span><span class="sxs-lookup"><span data-stu-id="1c66b-148">-Ring</span></span>
<span data-ttu-id="1c66b-149">Il numero di anello di HostPool.</span><span class="sxs-lookup"><span data-stu-id="1c66b-149">The ring number of HostPool.</span></span>

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

### <span data-ttu-id="1c66b-150">-SsoadfsAuthority</span><span class="sxs-lookup"><span data-stu-id="1c66b-150">-SsoadfsAuthority</span></span>
<span data-ttu-id="1c66b-151">URL del server ADFS del cliente per la firma dei certificati SSO WVD.</span><span class="sxs-lookup"><span data-stu-id="1c66b-151">URL to customer ADFS server for signing WVD SSO certificates.</span></span>

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

### <span data-ttu-id="1c66b-152">-SsoClientId</span><span class="sxs-lookup"><span data-stu-id="1c66b-152">-SsoClientId</span></span>
<span data-ttu-id="1c66b-153">ClientId per il relying party registrato usato per emettere certificati SSO WVD.</span><span class="sxs-lookup"><span data-stu-id="1c66b-153">ClientId for the registered Relying Party used to issue WVD SSO certificates.</span></span>

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

### <span data-ttu-id="1c66b-154">-SsoClientSecretKeyVaultPath</span><span class="sxs-lookup"><span data-stu-id="1c66b-154">-SsoClientSecretKeyVaultPath</span></span>
<span data-ttu-id="1c66b-155">Percorso di Azure KeyVault che archivia il segreto usato per la comunicazione in ADFS.</span><span class="sxs-lookup"><span data-stu-id="1c66b-155">Path to Azure KeyVault storing the secret used for communication to ADFS.</span></span>

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

### <span data-ttu-id="1c66b-156">-SsoContext</span><span class="sxs-lookup"><span data-stu-id="1c66b-156">-SsoContext</span></span>
<span data-ttu-id="1c66b-157">Percorso di keyvault contenente segreto ssoContext.</span><span class="sxs-lookup"><span data-stu-id="1c66b-157">Path to keyvault containing ssoContext secret.</span></span>

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

### <span data-ttu-id="1c66b-158">-SsoSecretType</span><span class="sxs-lookup"><span data-stu-id="1c66b-158">-SsoSecretType</span></span>
<span data-ttu-id="1c66b-159">Tipo di Single #A0 Tipo di segreto.</span><span class="sxs-lookup"><span data-stu-id="1c66b-159">The type of single sign on Secret Type.</span></span>

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

### <span data-ttu-id="1c66b-160">-StartVMOnConnect</span><span class="sxs-lookup"><span data-stu-id="1c66b-160">-StartVMOnConnect</span></span>
<span data-ttu-id="1c66b-161">Il contrassegno per attivare/disattivare la funzionalità StartVMOnConnect.</span><span class="sxs-lookup"><span data-stu-id="1c66b-161">The flag to turn on/off StartVMOnConnect feature.</span></span>

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

### <span data-ttu-id="1c66b-162">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1c66b-162">-SubscriptionId</span></span>
<span data-ttu-id="1c66b-163">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1c66b-163">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="1c66b-164">-Tag</span><span class="sxs-lookup"><span data-stu-id="1c66b-164">-Tag</span></span>
<span data-ttu-id="1c66b-165">Tag di risorse.</span><span class="sxs-lookup"><span data-stu-id="1c66b-165">Resource tags.</span></span>

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

### <span data-ttu-id="1c66b-166">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="1c66b-166">-ValidationEnvironment</span></span>
<span data-ttu-id="1c66b-167">Ambiente di convalida.</span><span class="sxs-lookup"><span data-stu-id="1c66b-167">Is validation environment.</span></span>

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

### <span data-ttu-id="1c66b-168">-VMTemplate</span><span class="sxs-lookup"><span data-stu-id="1c66b-168">-VMTemplate</span></span>
<span data-ttu-id="1c66b-169">Modello di VM per la configurazione sessionhosts all'interno di hostpool.</span><span class="sxs-lookup"><span data-stu-id="1c66b-169">VM template for sessionhosts configuration within hostpool.</span></span>

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

### <span data-ttu-id="1c66b-170">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1c66b-170">-WorkspaceName</span></span>
<span data-ttu-id="1c66b-171">Nome area di lavoro</span><span class="sxs-lookup"><span data-stu-id="1c66b-171">Workspace Name</span></span>

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

### <span data-ttu-id="1c66b-172">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1c66b-172">-Confirm</span></span>
<span data-ttu-id="1c66b-173">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c66b-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c66b-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c66b-174">-WhatIf</span></span>
<span data-ttu-id="1c66b-175">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1c66b-175">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c66b-176">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1c66b-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c66b-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c66b-177">CommonParameters</span></span>
<span data-ttu-id="1c66b-178">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c66b-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c66b-179">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1c66b-179">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c66b-180">INPUT</span><span class="sxs-lookup"><span data-stu-id="1c66b-180">INPUTS</span></span>

## <span data-ttu-id="1c66b-181">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1c66b-181">OUTPUTS</span></span>

### <span data-ttu-id="1c66b-182">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span><span class="sxs-lookup"><span data-stu-id="1c66b-182">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span></span>

## <span data-ttu-id="1c66b-183">NOTE</span><span class="sxs-lookup"><span data-stu-id="1c66b-183">NOTES</span></span>

<span data-ttu-id="1c66b-184">ALIAS</span><span class="sxs-lookup"><span data-stu-id="1c66b-184">ALIASES</span></span>

## <span data-ttu-id="1c66b-185">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1c66b-185">RELATED LINKS</span></span>

