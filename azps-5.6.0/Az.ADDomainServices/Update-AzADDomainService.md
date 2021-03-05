---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/powershell/module/az.addomainservices/update-azaddomainservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Update-AzADDomainService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Update-AzADDomainService.md
ms.openlocfilehash: 4504eaf26331fa4e881d6a86f284a74b7f249565
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991786"
---
# <span data-ttu-id="2486b-101">Update-AzADDomainService</span><span class="sxs-lookup"><span data-stu-id="2486b-101">Update-AzADDomainService</span></span>

## <span data-ttu-id="2486b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2486b-102">SYNOPSIS</span></span>
<span data-ttu-id="2486b-103">L'operazione Update Domain Service può essere usata per aggiornare la distribuzione esistente.</span><span class="sxs-lookup"><span data-stu-id="2486b-103">The Update Domain Service operation can be used to update the existing deployment.</span></span>
<span data-ttu-id="2486b-104">La chiamata di aggiornamento supporta solo le proprietà elencate nel corpo PATCH.</span><span class="sxs-lookup"><span data-stu-id="2486b-104">The update call only supports the properties listed in the PATCH body.</span></span>

## <span data-ttu-id="2486b-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2486b-105">SYNTAX</span></span>

### <span data-ttu-id="2486b-106">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2486b-106">UpdateExpanded (Default)</span></span>
```
Update-AzADDomainService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DomainConfigurationType <String>] [-DomainSecuritySettingNtlmV1 <String>]
 [-DomainSecuritySettingSyncKerberosPassword <String>] [-DomainSecuritySettingSyncNtlmPassword <String>]
 [-DomainSecuritySettingSyncOnPremPassword <String>] [-DomainSecuritySettingTlsV1 <String>]
 [-FilteredSync <String>] [-ForestTrust <IForestTrust[]>] [-LdapSettingExternalAccess <String>]
 [-LdapSettingLdaps <String>] [-LdapSettingPfxCertificate <String>]
 [-LdapSettingPfxCertificatePassword <SecureString>] [-NotificationSettingAdditionalRecipient <String[]>]
 [-NotificationSettingNotifyDcAdmin <String>] [-NotificationSettingNotifyGlobalAdmin <String>]
 [-ReplicaSet <IReplicaSet[]>] [-ResourceForest <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2486b-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="2486b-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzADDomainService -InputObject <IAdDomainServicesIdentity> [-DomainConfigurationType <String>]
 [-DomainSecuritySettingNtlmV1 <String>] [-DomainSecuritySettingSyncKerberosPassword <String>]
 [-DomainSecuritySettingSyncNtlmPassword <String>] [-DomainSecuritySettingSyncOnPremPassword <String>]
 [-DomainSecuritySettingTlsV1 <String>] [-FilteredSync <String>] [-ForestTrust <IForestTrust[]>]
 [-LdapSettingExternalAccess <String>] [-LdapSettingLdaps <String>] [-LdapSettingPfxCertificate <String>]
 [-LdapSettingPfxCertificatePassword <SecureString>] [-NotificationSettingAdditionalRecipient <String[]>]
 [-NotificationSettingNotifyDcAdmin <String>] [-NotificationSettingNotifyGlobalAdmin <String>]
 [-ReplicaSet <IReplicaSet[]>] [-ResourceForest <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2486b-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2486b-108">DESCRIPTION</span></span>
<span data-ttu-id="2486b-109">L'operazione Update Domain Service può essere usata per aggiornare la distribuzione esistente.</span><span class="sxs-lookup"><span data-stu-id="2486b-109">The Update Domain Service operation can be used to update the existing deployment.</span></span>
<span data-ttu-id="2486b-110">La chiamata di aggiornamento supporta solo le proprietà elencate nel corpo PATCH.</span><span class="sxs-lookup"><span data-stu-id="2486b-110">The update call only supports the properties listed in the PATCH body.</span></span>

## <span data-ttu-id="2486b-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2486b-111">EXAMPLES</span></span>

### <span data-ttu-id="2486b-112">Esempio 1: Aggiornare AzADDomainService in base al nome e al nome ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2486b-112">Example 1: Update AzADDomainService By ResourceGroupName and Name</span></span>
```powershell
PS C:\> $ADDomainSetting = New-AzADDomainServiceDomainSecuritySettingObject -TlsV1 Disabled
Update-AzADDomainService -Name youriADdomain -ResourceGroupName youriADdomain -DomainSecuritySetting $ADDomainSetting

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="2486b-113">Aggiornare AzADDomainService in base al nome e al nome DelGruppo Risorse</span><span class="sxs-lookup"><span data-stu-id="2486b-113">Update AzADDomainService By ResourceGroupName and Name</span></span>

### <span data-ttu-id="2486b-114">Esempio 2: Aggiornare AzADDomainService per Inputobject</span><span class="sxs-lookup"><span data-stu-id="2486b-114">Example 2: Update AzADDomainService By Inputobject</span></span>
```powershell
PS C:\> $getAzAddomain = Get-AzADDomainService -Name youriADdomain -ResourceGroupName youriADdomain
$ADDomainSetting = New-AzADDomainServiceDomainSecuritySettingObject -TlsV1 Disabled
Update-AzADDomainService -InputObject $getAzAddomain -DomainSecuritySetting $ADDomainSetting

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="2486b-115">Aggiornare AzADDomainService per inputobject</span><span class="sxs-lookup"><span data-stu-id="2486b-115">Update AzADDomainService By Inputobject</span></span>

## <span data-ttu-id="2486b-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2486b-116">PARAMETERS</span></span>

### <span data-ttu-id="2486b-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2486b-117">-AsJob</span></span>
<span data-ttu-id="2486b-118">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="2486b-118">Run the command as a job</span></span>

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

### <span data-ttu-id="2486b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2486b-119">-DefaultProfile</span></span>
<span data-ttu-id="2486b-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2486b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2486b-121">-DomainConfigurationType</span><span class="sxs-lookup"><span data-stu-id="2486b-121">-DomainConfigurationType</span></span>
<span data-ttu-id="2486b-122">Tipo di configurazione del dominio</span><span class="sxs-lookup"><span data-stu-id="2486b-122">Domain Configuration Type</span></span>

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

### <span data-ttu-id="2486b-123">-DomainSecuritySettingNtlmV1</span><span class="sxs-lookup"><span data-stu-id="2486b-123">-DomainSecuritySettingNtlmV1</span></span>
<span data-ttu-id="2486b-124">Un flag per determinare se NtlmV1 è abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="2486b-124">A flag to determine whether or not NtlmV1 is enabled or disabled.</span></span>

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

### <span data-ttu-id="2486b-125">-DomainSecuritySettingSyncKerberosPassword</span><span class="sxs-lookup"><span data-stu-id="2486b-125">-DomainSecuritySettingSyncKerberosPassword</span></span>
<span data-ttu-id="2486b-126">Un flag per determinare se SyncKerberosPasswords è abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="2486b-126">A flag to determine whether or not SyncKerberosPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="2486b-127">-DomainSecuritySettingSyncNtlmPassword</span><span class="sxs-lookup"><span data-stu-id="2486b-127">-DomainSecuritySettingSyncNtlmPassword</span></span>
<span data-ttu-id="2486b-128">Un flag per determinare se SyncNtlmPasswords è abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="2486b-128">A flag to determine whether or not SyncNtlmPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="2486b-129">-DomainSecuritySettingSyncOnPremPassword</span><span class="sxs-lookup"><span data-stu-id="2486b-129">-DomainSecuritySettingSyncOnPremPassword</span></span>
<span data-ttu-id="2486b-130">Un flag per determinare se SyncOnPremPasswords è abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="2486b-130">A flag to determine whether or not SyncOnPremPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="2486b-131">-DomainSecuritySettingTlsV1</span><span class="sxs-lookup"><span data-stu-id="2486b-131">-DomainSecuritySettingTlsV1</span></span>
<span data-ttu-id="2486b-132">Un flag per determinare se TlsV1 è abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="2486b-132">A flag to determine whether or not TlsV1 is enabled or disabled.</span></span>

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

### <span data-ttu-id="2486b-133">-FilteredSync</span><span class="sxs-lookup"><span data-stu-id="2486b-133">-FilteredSync</span></span>
<span data-ttu-id="2486b-134">Contrassegno Abilitato o Disabilitato per attivare la sincronizzazione filtrata basata su gruppo</span><span class="sxs-lookup"><span data-stu-id="2486b-134">Enabled or Disabled flag to turn on Group-based filtered sync</span></span>

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

### <span data-ttu-id="2486b-135">-ForestTrust</span><span class="sxs-lookup"><span data-stu-id="2486b-135">-ForestTrust</span></span>
<span data-ttu-id="2486b-136">Elenco delle impostazioni per la costruzione della foresta delle risorse To, vedere la sezione NOTES per le proprietà FORESTTRUST e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="2486b-136">List of settings for Resource Forest To construct, see NOTES section for FORESTTRUST properties and create a hash table.</span></span>

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

### <span data-ttu-id="2486b-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2486b-137">-InputObject</span></span>
<span data-ttu-id="2486b-138">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="2486b-138">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2486b-139">-LdapSettingExternalAccess</span><span class="sxs-lookup"><span data-stu-id="2486b-139">-LdapSettingExternalAccess</span></span>
<span data-ttu-id="2486b-140">Un flag per determinare se l'accesso LDAP sicuro via Internet è abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="2486b-140">A flag to determine whether or not Secure LDAP access over the internet is enabled or disabled.</span></span>

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

### <span data-ttu-id="2486b-141">-LdapSettingLdaps</span><span class="sxs-lookup"><span data-stu-id="2486b-141">-LdapSettingLdaps</span></span>
<span data-ttu-id="2486b-142">Un flag per determinare se secure LDAP è abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="2486b-142">A flag to determine whether or not Secure LDAP is enabled or disabled.</span></span>

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

### <span data-ttu-id="2486b-143">-LdapSettingPfxCertificate</span><span class="sxs-lookup"><span data-stu-id="2486b-143">-LdapSettingPfxCertificate</span></span>
<span data-ttu-id="2486b-144">Certificato necessario per configurare Secure LDAP.</span><span class="sxs-lookup"><span data-stu-id="2486b-144">The certificate required to configure Secure LDAP.</span></span>
<span data-ttu-id="2486b-145">Il parametro passato qui deve essere una rappresentazione in base64encoded del file pfx del certificato.</span><span class="sxs-lookup"><span data-stu-id="2486b-145">The parameter passed here should be a base64encoded representation of the certificate pfx file.</span></span>

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

### <span data-ttu-id="2486b-146">-LdapSettingPfxCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="2486b-146">-LdapSettingPfxCertificatePassword</span></span>
<span data-ttu-id="2486b-147">Password per decrittografare il file Pfx del certificato LDAP sicuro fornito.</span><span class="sxs-lookup"><span data-stu-id="2486b-147">The password to decrypt the provided Secure LDAP certificate pfx file.</span></span>

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

### <span data-ttu-id="2486b-148">-Name</span><span class="sxs-lookup"><span data-stu-id="2486b-148">-Name</span></span>
<span data-ttu-id="2486b-149">Nome del servizio di dominio.</span><span class="sxs-lookup"><span data-stu-id="2486b-149">The name of the domain service.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DomainServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2486b-150">-NotificationSettingAdditionalRecipient</span><span class="sxs-lookup"><span data-stu-id="2486b-150">-NotificationSettingAdditionalRecipient</span></span>
<span data-ttu-id="2486b-151">Elenco di altri destinatari</span><span class="sxs-lookup"><span data-stu-id="2486b-151">The list of additional recipients</span></span>

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

### <span data-ttu-id="2486b-152">-NotificationSettingNotifyDcAdmin</span><span class="sxs-lookup"><span data-stu-id="2486b-152">-NotificationSettingNotifyDcAdmin</span></span>
<span data-ttu-id="2486b-153">Gli amministratori del controller di dominio devono ricevere una notifica</span><span class="sxs-lookup"><span data-stu-id="2486b-153">Should domain controller admins be notified</span></span>

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

### <span data-ttu-id="2486b-154">-NotificationSettingNotifyGlobalAdmin</span><span class="sxs-lookup"><span data-stu-id="2486b-154">-NotificationSettingNotifyGlobalAdmin</span></span>
<span data-ttu-id="2486b-155">Se gli amministratori globali vengono informati</span><span class="sxs-lookup"><span data-stu-id="2486b-155">Should global admins be notified</span></span>

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

### <span data-ttu-id="2486b-156">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2486b-156">-NoWait</span></span>
<span data-ttu-id="2486b-157">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="2486b-157">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2486b-158">-ReplicaSet</span><span class="sxs-lookup"><span data-stu-id="2486b-158">-ReplicaSet</span></span>
<span data-ttu-id="2486b-159">Elenco dei ReplicaSet da creare, vedere la sezione NOTES relativa alle proprietà REPLICASET e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="2486b-159">List of ReplicaSets To construct, see NOTES section for REPLICASET properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IReplicaSet[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2486b-160">-ResourceForest</span><span class="sxs-lookup"><span data-stu-id="2486b-160">-ResourceForest</span></span>
<span data-ttu-id="2486b-161">Foresta delle risorse</span><span class="sxs-lookup"><span data-stu-id="2486b-161">Resource Forest</span></span>

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

### <span data-ttu-id="2486b-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2486b-162">-ResourceGroupName</span></span>
<span data-ttu-id="2486b-163">Nome del gruppo di risorse nella sottoscrizione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="2486b-163">The name of the resource group within the user's subscription.</span></span>
<span data-ttu-id="2486b-164">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="2486b-164">The name is case insensitive.</span></span>

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

### <span data-ttu-id="2486b-165">-SKU</span><span class="sxs-lookup"><span data-stu-id="2486b-165">-Sku</span></span>
<span data-ttu-id="2486b-166">Tipo di SKU</span><span class="sxs-lookup"><span data-stu-id="2486b-166">Sku Type</span></span>

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

### <span data-ttu-id="2486b-167">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2486b-167">-SubscriptionId</span></span>
<span data-ttu-id="2486b-168">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2486b-168">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="2486b-169">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="2486b-169">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2486b-170">-Tag</span><span class="sxs-lookup"><span data-stu-id="2486b-170">-Tag</span></span>
<span data-ttu-id="2486b-171">Tag di risorse</span><span class="sxs-lookup"><span data-stu-id="2486b-171">Resource tags</span></span>

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

### <span data-ttu-id="2486b-172">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2486b-172">-Confirm</span></span>
<span data-ttu-id="2486b-173">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2486b-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2486b-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2486b-174">-WhatIf</span></span>
<span data-ttu-id="2486b-175">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2486b-175">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2486b-176">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2486b-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2486b-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2486b-177">CommonParameters</span></span>
<span data-ttu-id="2486b-178">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2486b-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2486b-179">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2486b-179">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2486b-180">INPUT</span><span class="sxs-lookup"><span data-stu-id="2486b-180">INPUTS</span></span>

### <span data-ttu-id="2486b-181">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="2486b-181">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span></span>

## <span data-ttu-id="2486b-182">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2486b-182">OUTPUTS</span></span>

### <span data-ttu-id="2486b-183">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span><span class="sxs-lookup"><span data-stu-id="2486b-183">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span></span>

## <span data-ttu-id="2486b-184">NOTE</span><span class="sxs-lookup"><span data-stu-id="2486b-184">NOTES</span></span>

<span data-ttu-id="2486b-185">ALIAS</span><span class="sxs-lookup"><span data-stu-id="2486b-185">ALIASES</span></span>

<span data-ttu-id="2486b-186">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="2486b-186">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2486b-187">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="2486b-187">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2486b-188">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2486b-188">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2486b-189">FORESTTRUST <IForestTrust[]>: elenco delle impostazioni per la foresta delle risorse</span><span class="sxs-lookup"><span data-stu-id="2486b-189">FORESTTRUST <IForestTrust[]>: List of settings for Resource Forest</span></span>
  - <span data-ttu-id="2486b-190">`[FriendlyName <String>]`: nome descrittivo</span><span class="sxs-lookup"><span data-stu-id="2486b-190">`[FriendlyName <String>]`: Friendly Name</span></span>
  - <span data-ttu-id="2486b-191">`[RemoteDnsIP <String>]`: ip Dns remoti</span><span class="sxs-lookup"><span data-stu-id="2486b-191">`[RemoteDnsIP <String>]`: Remote Dns ips</span></span>
  - <span data-ttu-id="2486b-192">`[TrustDirection <String>]`: Direzione protezione</span><span class="sxs-lookup"><span data-stu-id="2486b-192">`[TrustDirection <String>]`: Trust Direction</span></span>
  - <span data-ttu-id="2486b-193">`[TrustPassword <String>]`: password di attendibilità</span><span class="sxs-lookup"><span data-stu-id="2486b-193">`[TrustPassword <String>]`: Trust Password</span></span>
  - <span data-ttu-id="2486b-194">`[TrustedDomainFqdn <String>]`: FQDN dominio attendibile</span><span class="sxs-lookup"><span data-stu-id="2486b-194">`[TrustedDomainFqdn <String>]`: Trusted Domain FQDN</span></span>

<span data-ttu-id="2486b-195">INPUTOBJECT <IAdDomainServicesIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="2486b-195">INPUTOBJECT <IAdDomainServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2486b-196">`[DomainServiceName <String>]`: nome del servizio di dominio.</span><span class="sxs-lookup"><span data-stu-id="2486b-196">`[DomainServiceName <String>]`: The name of the domain service.</span></span>
  - <span data-ttu-id="2486b-197">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="2486b-197">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2486b-198">`[ResourceGroupName <String>]`: nome del gruppo di risorse nella sottoscrizione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="2486b-198">`[ResourceGroupName <String>]`: The name of the resource group within the user's subscription.</span></span> <span data-ttu-id="2486b-199">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="2486b-199">The name is case insensitive.</span></span>
  - <span data-ttu-id="2486b-200">`[SubscriptionId <String>]`: recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2486b-200">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="2486b-201">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="2486b-201">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="2486b-202">REPLICASET <IReplicaSet[]>: Elenco di ReplicaSet</span><span class="sxs-lookup"><span data-stu-id="2486b-202">REPLICASET <IReplicaSet[]>: List of ReplicaSets</span></span>
  - <span data-ttu-id="2486b-203">`[Location <String>]`: percorso di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="2486b-203">`[Location <String>]`: Virtual network location</span></span>
  - <span data-ttu-id="2486b-204">`[SubnetId <String>]`: nome della rete virtuale in cui verrà distribuito Servizi di dominio.</span><span class="sxs-lookup"><span data-stu-id="2486b-204">`[SubnetId <String>]`: The name of the virtual network that Domain Services will be deployed on.</span></span> <span data-ttu-id="2486b-205">ID della subnet in cui verranno distribuiti i Servizi di dominio.</span><span class="sxs-lookup"><span data-stu-id="2486b-205">The id of the subnet that Domain Services will be deployed on.</span></span> <span data-ttu-id="2486b-206">/virtualNetwork/vnetName/subnets/subnetName.</span><span class="sxs-lookup"><span data-stu-id="2486b-206">/virtualNetwork/vnetName/subnets/subnetName.</span></span>

## <span data-ttu-id="2486b-207">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2486b-207">RELATED LINKS</span></span>

