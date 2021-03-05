---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/powershell/module/az.addomainservices/new-azaddomainservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainService.md
ms.openlocfilehash: 61918dd4bce5279a2528e94c4e46fbe1c8813aff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986325"
---
# <span data-ttu-id="c94d3-101">New-AzADDomainService</span><span class="sxs-lookup"><span data-stu-id="c94d3-101">New-AzADDomainService</span></span>

## <span data-ttu-id="c94d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c94d3-102">SYNOPSIS</span></span>
<span data-ttu-id="c94d3-103">L'operazione Crea servizio di dominio crea un nuovo servizio di dominio con i parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="c94d3-103">The Create Domain Service operation creates a new domain service with the specified parameters.</span></span>
<span data-ttu-id="c94d3-104">Se il servizio specifico esiste già, le eventuali proprietà modificabili verranno aggiornate e le eventuali proprietà non modificabili rimarranno invariate.</span><span class="sxs-lookup"><span data-stu-id="c94d3-104">If the specific service already exists, then any patchable properties will be updated and any immutable properties will remain unchanged.</span></span>

## <span data-ttu-id="c94d3-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c94d3-105">SYNTAX</span></span>

```
New-AzADDomainService -Name <String> -ResourceGroupName <String> -DomainName <String>
 -ReplicaSet <IReplicaSet[]> [-SubscriptionId <String>] [-DomainConfigurationType <String>]
 [-DomainSecuritySettingNtlmV1 <String>] [-DomainSecuritySettingSyncKerberosPassword <String>]
 [-DomainSecuritySettingSyncNtlmPassword <String>] [-DomainSecuritySettingSyncOnPremPassword <String>]
 [-DomainSecuritySettingTlsV1 <String>] [-FilteredSync <String>] [-ForestTrust <IForestTrust[]>]
 [-LdapSettingExternalAccess <String>] [-LdapSettingLdaps <String>] [-LdapSettingPfxCertificate <String>]
 [-LdapSettingPfxCertificatePassword <SecureString>] [-NotificationSettingAdditionalRecipient <String[]>]
 [-NotificationSettingNotifyDcAdmin <String>] [-NotificationSettingNotifyGlobalAdmin <String>]
 [-ResourceForest <String>] [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c94d3-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c94d3-106">DESCRIPTION</span></span>
<span data-ttu-id="c94d3-107">L'operazione Crea servizio di dominio crea un nuovo servizio di dominio con i parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="c94d3-107">The Create Domain Service operation creates a new domain service with the specified parameters.</span></span>
<span data-ttu-id="c94d3-108">Se il servizio specifico esiste già, le eventuali proprietà modificabili verranno aggiornate e le eventuali proprietà non modificabili rimarranno invariate.</span><span class="sxs-lookup"><span data-stu-id="c94d3-108">If the specific service already exists, then any patchable properties will be updated and any immutable properties will remain unchanged.</span></span>

## <span data-ttu-id="c94d3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c94d3-109">EXAMPLES</span></span>

### <span data-ttu-id="c94d3-110">Esempio 1: Creare un nuovo servizio ADDomain</span><span class="sxs-lookup"><span data-stu-id="c94d3-110">Example 1: Create new ADDomainService</span></span>
```powershell
PS C:\> $replicaSet = New-AzADDomainServiceReplicaSetObject -Location westus -SubnetId /subscriptions/********-****-****-****-**********/resourceGroups/yishitest/providers/Microsoft.Network/virtualNetworks/aadds-vnet/subnets/default
New-AzADDomainService -name youriADdomain -ResourceGroupName youriAddomain -DomainName youriAddomain.com -ReplicaSet $replicaSet -debug

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="c94d3-111">Creare un nuovo servizio ADDomain</span><span class="sxs-lookup"><span data-stu-id="c94d3-111">Create new ADDomainService</span></span>

## <span data-ttu-id="c94d3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c94d3-112">PARAMETERS</span></span>

### <span data-ttu-id="c94d3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c94d3-113">-AsJob</span></span>
<span data-ttu-id="c94d3-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="c94d3-114">Run the command as a job</span></span>

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

### <span data-ttu-id="c94d3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c94d3-115">-DefaultProfile</span></span>
<span data-ttu-id="c94d3-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c94d3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c94d3-117">-DomainConfigurationType</span><span class="sxs-lookup"><span data-stu-id="c94d3-117">-DomainConfigurationType</span></span>
<span data-ttu-id="c94d3-118">Tipo di configurazione del dominio</span><span class="sxs-lookup"><span data-stu-id="c94d3-118">Domain Configuration Type</span></span>

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

### <span data-ttu-id="c94d3-119">-DomainName</span><span class="sxs-lookup"><span data-stu-id="c94d3-119">-DomainName</span></span>
<span data-ttu-id="c94d3-120">Nome del dominio di Azure in cui l'utente vuole distribuire Servizi di dominio.</span><span class="sxs-lookup"><span data-stu-id="c94d3-120">The name of the Azure domain that the user would like to deploy Domain Services to.</span></span>

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

### <span data-ttu-id="c94d3-121">-DomainSecuritySettingNtlmV1</span><span class="sxs-lookup"><span data-stu-id="c94d3-121">-DomainSecuritySettingNtlmV1</span></span>
<span data-ttu-id="c94d3-122">Un flag per determinare se NtlmV1 è abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="c94d3-122">A flag to determine whether or not NtlmV1 is enabled or disabled.</span></span>

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

### <span data-ttu-id="c94d3-123">-DomainSecuritySettingSyncKerberosPassword</span><span class="sxs-lookup"><span data-stu-id="c94d3-123">-DomainSecuritySettingSyncKerberosPassword</span></span>
<span data-ttu-id="c94d3-124">Un flag per determinare se SyncKerberosPasswords è abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="c94d3-124">A flag to determine whether or not SyncKerberosPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="c94d3-125">-DomainSecuritySettingSyncNtlmPassword</span><span class="sxs-lookup"><span data-stu-id="c94d3-125">-DomainSecuritySettingSyncNtlmPassword</span></span>
<span data-ttu-id="c94d3-126">Un flag per determinare se SyncNtlmPasswords è abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="c94d3-126">A flag to determine whether or not SyncNtlmPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="c94d3-127">-DomainSecuritySettingSyncOnPremPassword</span><span class="sxs-lookup"><span data-stu-id="c94d3-127">-DomainSecuritySettingSyncOnPremPassword</span></span>
<span data-ttu-id="c94d3-128">Un flag per determinare se SyncOnPremPasswords è abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="c94d3-128">A flag to determine whether or not SyncOnPremPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="c94d3-129">-DomainSecuritySettingTlsV1</span><span class="sxs-lookup"><span data-stu-id="c94d3-129">-DomainSecuritySettingTlsV1</span></span>
<span data-ttu-id="c94d3-130">Un flag per determinare se TlsV1 è abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="c94d3-130">A flag to determine whether or not TlsV1 is enabled or disabled.</span></span>

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

### <span data-ttu-id="c94d3-131">-FilteredSync</span><span class="sxs-lookup"><span data-stu-id="c94d3-131">-FilteredSync</span></span>
<span data-ttu-id="c94d3-132">Contrassegno Abilitato o Disabilitato per attivare la sincronizzazione filtrata basata su gruppo</span><span class="sxs-lookup"><span data-stu-id="c94d3-132">Enabled or Disabled flag to turn on Group-based filtered sync</span></span>

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

### <span data-ttu-id="c94d3-133">-ForestTrust</span><span class="sxs-lookup"><span data-stu-id="c94d3-133">-ForestTrust</span></span>
<span data-ttu-id="c94d3-134">Elenco delle impostazioni per la costruzione della foresta delle risorse To, vedere la sezione NOTES per le proprietà FORESTTRUST e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="c94d3-134">List of settings for Resource Forest To construct, see NOTES section for FORESTTRUST properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IForestTrust[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c94d3-135">-LdapSettingExternalAccess</span><span class="sxs-lookup"><span data-stu-id="c94d3-135">-LdapSettingExternalAccess</span></span>
<span data-ttu-id="c94d3-136">Un flag per determinare se l'accesso LDAP sicuro via Internet è abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="c94d3-136">A flag to determine whether or not Secure LDAP access over the internet is enabled or disabled.</span></span>

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

### <span data-ttu-id="c94d3-137">-LdapSettingLdaps</span><span class="sxs-lookup"><span data-stu-id="c94d3-137">-LdapSettingLdaps</span></span>
<span data-ttu-id="c94d3-138">Un flag per determinare se l'opzione Secure LDAP è abilitata o disabilitata.</span><span class="sxs-lookup"><span data-stu-id="c94d3-138">A flag to determine whether or not Secure LDAP is enabled or disabled.</span></span>

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

### <span data-ttu-id="c94d3-139">-LdapSettingPfxCertificate</span><span class="sxs-lookup"><span data-stu-id="c94d3-139">-LdapSettingPfxCertificate</span></span>
<span data-ttu-id="c94d3-140">Certificato necessario per configurare Secure LDAP.</span><span class="sxs-lookup"><span data-stu-id="c94d3-140">The certificate required to configure Secure LDAP.</span></span>
<span data-ttu-id="c94d3-141">Il parametro passato qui deve essere una rappresentazione in base64encoded del file pfx del certificato.</span><span class="sxs-lookup"><span data-stu-id="c94d3-141">The parameter passed here should be a base64encoded representation of the certificate pfx file.</span></span>

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

### <span data-ttu-id="c94d3-142">-LdapSettingPfxCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="c94d3-142">-LdapSettingPfxCertificatePassword</span></span>
<span data-ttu-id="c94d3-143">Password per decrittografare il file Pfx del certificato LDAP sicuro fornito.</span><span class="sxs-lookup"><span data-stu-id="c94d3-143">The password to decrypt the provided Secure LDAP certificate pfx file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c94d3-144">-Name</span><span class="sxs-lookup"><span data-stu-id="c94d3-144">-Name</span></span>
<span data-ttu-id="c94d3-145">Nome del servizio di dominio.</span><span class="sxs-lookup"><span data-stu-id="c94d3-145">The name of the domain service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DomainServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c94d3-146">-NotificationSettingAdditionalRecipient</span><span class="sxs-lookup"><span data-stu-id="c94d3-146">-NotificationSettingAdditionalRecipient</span></span>
<span data-ttu-id="c94d3-147">Elenco di altri destinatari</span><span class="sxs-lookup"><span data-stu-id="c94d3-147">The list of additional recipients</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c94d3-148">-NotificationSettingNotifyDcAdmin</span><span class="sxs-lookup"><span data-stu-id="c94d3-148">-NotificationSettingNotifyDcAdmin</span></span>
<span data-ttu-id="c94d3-149">Gli amministratori del controller di dominio devono ricevere una notifica</span><span class="sxs-lookup"><span data-stu-id="c94d3-149">Should domain controller admins be notified</span></span>

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

### <span data-ttu-id="c94d3-150">-NotificationSettingNotifyGlobalAdmin</span><span class="sxs-lookup"><span data-stu-id="c94d3-150">-NotificationSettingNotifyGlobalAdmin</span></span>
<span data-ttu-id="c94d3-151">Se gli amministratori globali vengono informati</span><span class="sxs-lookup"><span data-stu-id="c94d3-151">Should global admins be notified</span></span>

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

### <span data-ttu-id="c94d3-152">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c94d3-152">-NoWait</span></span>
<span data-ttu-id="c94d3-153">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="c94d3-153">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c94d3-154">-ReplicaSet</span><span class="sxs-lookup"><span data-stu-id="c94d3-154">-ReplicaSet</span></span>
<span data-ttu-id="c94d3-155">Elenco dei ReplicaSet da creare, vedere la sezione NOTES relativa alle proprietà REPLICASET e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="c94d3-155">List of ReplicaSets To construct, see NOTES section for REPLICASET properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IReplicaSet[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c94d3-156">-ResourceForest</span><span class="sxs-lookup"><span data-stu-id="c94d3-156">-ResourceForest</span></span>
<span data-ttu-id="c94d3-157">Foresta delle risorse</span><span class="sxs-lookup"><span data-stu-id="c94d3-157">Resource Forest</span></span>

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

### <span data-ttu-id="c94d3-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c94d3-158">-ResourceGroupName</span></span>
<span data-ttu-id="c94d3-159">Nome del gruppo di risorse nella sottoscrizione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c94d3-159">The name of the resource group within the user's subscription.</span></span>
<span data-ttu-id="c94d3-160">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="c94d3-160">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c94d3-161">-SKU</span><span class="sxs-lookup"><span data-stu-id="c94d3-161">-Sku</span></span>
<span data-ttu-id="c94d3-162">Tipo di SKU</span><span class="sxs-lookup"><span data-stu-id="c94d3-162">Sku Type</span></span>

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

### <span data-ttu-id="c94d3-163">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c94d3-163">-SubscriptionId</span></span>
<span data-ttu-id="c94d3-164">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c94d3-164">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="c94d3-165">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="c94d3-165">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c94d3-166">-Tag</span><span class="sxs-lookup"><span data-stu-id="c94d3-166">-Tag</span></span>
<span data-ttu-id="c94d3-167">Tag di risorse</span><span class="sxs-lookup"><span data-stu-id="c94d3-167">Resource tags</span></span>

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

### <span data-ttu-id="c94d3-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c94d3-168">-Confirm</span></span>
<span data-ttu-id="c94d3-169">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c94d3-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c94d3-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c94d3-170">-WhatIf</span></span>
<span data-ttu-id="c94d3-171">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c94d3-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c94d3-172">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c94d3-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c94d3-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c94d3-173">CommonParameters</span></span>
<span data-ttu-id="c94d3-174">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c94d3-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c94d3-175">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c94d3-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c94d3-176">INPUT</span><span class="sxs-lookup"><span data-stu-id="c94d3-176">INPUTS</span></span>

## <span data-ttu-id="c94d3-177">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c94d3-177">OUTPUTS</span></span>

### <span data-ttu-id="c94d3-178">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span><span class="sxs-lookup"><span data-stu-id="c94d3-178">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span></span>

## <span data-ttu-id="c94d3-179">NOTE</span><span class="sxs-lookup"><span data-stu-id="c94d3-179">NOTES</span></span>

<span data-ttu-id="c94d3-180">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c94d3-180">ALIASES</span></span>

<span data-ttu-id="c94d3-181">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="c94d3-181">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c94d3-182">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="c94d3-182">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c94d3-183">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c94d3-183">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c94d3-184">FORESTTRUST <IForestTrust[]>: elenco delle impostazioni per la foresta delle risorse</span><span class="sxs-lookup"><span data-stu-id="c94d3-184">FORESTTRUST <IForestTrust[]>: List of settings for Resource Forest</span></span>
  - <span data-ttu-id="c94d3-185">`[FriendlyName <String>]`: nome descrittivo</span><span class="sxs-lookup"><span data-stu-id="c94d3-185">`[FriendlyName <String>]`: Friendly Name</span></span>
  - <span data-ttu-id="c94d3-186">`[RemoteDnsIP <String>]`: ip Dns remoti</span><span class="sxs-lookup"><span data-stu-id="c94d3-186">`[RemoteDnsIP <String>]`: Remote Dns ips</span></span>
  - <span data-ttu-id="c94d3-187">`[TrustDirection <String>]`: direzione di protezione</span><span class="sxs-lookup"><span data-stu-id="c94d3-187">`[TrustDirection <String>]`: Trust Direction</span></span>
  - <span data-ttu-id="c94d3-188">`[TrustPassword <String>]`: password di attendibilità</span><span class="sxs-lookup"><span data-stu-id="c94d3-188">`[TrustPassword <String>]`: Trust Password</span></span>
  - <span data-ttu-id="c94d3-189">`[TrustedDomainFqdn <String>]`: FQDN dominio attendibile</span><span class="sxs-lookup"><span data-stu-id="c94d3-189">`[TrustedDomainFqdn <String>]`: Trusted Domain FQDN</span></span>

<span data-ttu-id="c94d3-190">REPLICASET <IReplicaSet[]>: Elenco di ReplicaSet</span><span class="sxs-lookup"><span data-stu-id="c94d3-190">REPLICASET <IReplicaSet[]>: List of ReplicaSets</span></span>
  - <span data-ttu-id="c94d3-191">`[Location <String>]`: percorso di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="c94d3-191">`[Location <String>]`: Virtual network location</span></span>
  - <span data-ttu-id="c94d3-192">`[SubnetId <String>]`: nome della rete virtuale in cui verrà distribuito Servizi di dominio.</span><span class="sxs-lookup"><span data-stu-id="c94d3-192">`[SubnetId <String>]`: The name of the virtual network that Domain Services will be deployed on.</span></span> <span data-ttu-id="c94d3-193">ID della subnet in cui verranno distribuiti i Servizi di dominio.</span><span class="sxs-lookup"><span data-stu-id="c94d3-193">The id of the subnet that Domain Services will be deployed on.</span></span> <span data-ttu-id="c94d3-194">/virtualNetwork/vnetName/subnets/subnetName.</span><span class="sxs-lookup"><span data-stu-id="c94d3-194">/virtualNetwork/vnetName/subnets/subnetName.</span></span>

## <span data-ttu-id="c94d3-195">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c94d3-195">RELATED LINKS</span></span>

