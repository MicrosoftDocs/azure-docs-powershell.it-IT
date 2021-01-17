---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/update-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Update-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Update-AzAppConfigurationStore.md
ms.openlocfilehash: 8aea57e0c2bea5dbaa2e3233e886c97bfebe4bd4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381429"
---
# <span data-ttu-id="37fba-101">Update-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="37fba-101">Update-AzAppConfigurationStore</span></span>

## <span data-ttu-id="37fba-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="37fba-102">SYNOPSIS</span></span>
<span data-ttu-id="37fba-103">Aggiorna un archivio di configurazione con i parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="37fba-103">Updates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="37fba-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="37fba-104">SYNTAX</span></span>

### <span data-ttu-id="37fba-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="37fba-105">UpdateExpanded (Default)</span></span>
```
Update-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EncryptionKeyIdentifier <String>] [-IdentityType <IdentityType>] [-KeyVaultIdentityClientId <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="37fba-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="37fba-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-EncryptionKeyIdentifier <String>]
 [-IdentityType <IdentityType>] [-KeyVaultIdentityClientId <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="37fba-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="37fba-107">DESCRIPTION</span></span>
<span data-ttu-id="37fba-108">Aggiorna un archivio di configurazione con i parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="37fba-108">Updates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="37fba-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="37fba-109">EXAMPLES</span></span>

### <span data-ttu-id="37fba-110">Esempio 1: abilitare la crittografia dei dati dell'archivio di configurazione dell'app in base all'identità gestita assegnata dal sistema</span><span class="sxs-lookup"><span data-stu-id="37fba-110">Example 1: Enable data encryption of the app configuration store by system-assigned managed identity</span></span>
```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName kv-Name -Name key-Name -Destination 'Software'
PS C:\> $systemAssignedAppStore = New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location $env.location -Sku 'standard' -IdentityType "SystemAssigned"
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName kv-Name -ObjectId $systemAssignedAppStore.IdentityPrincipalId -PermissionsToKeys get,unwrapKey,wrapKey -PassThru
PS C:\> Update-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -EncryptionKeyIdentifier $key.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="37fba-111">Questo comando consente la crittografia dei dati tramite una chiave archiviata in Azure Key Vault usando un'identità gestita assegnata dal sistema.</span><span class="sxs-lookup"><span data-stu-id="37fba-111">This command enables data encryption by a key stored in Azure Key Vault using a system-assigned managed identity.</span></span>
<span data-ttu-id="37fba-112">Il Vault deve avere abilitato la protezione soft-delete e Purge e l'identità gestita deve avere le autorizzazioni principali seguenti: Get, wrapKey, unwrapKey.</span><span class="sxs-lookup"><span data-stu-id="37fba-112">The vault must have enabled soft-delete and purge-protection, and the managed identity must have these key permissions: get, wrapKey, unwrapKey.</span></span>

### <span data-ttu-id="37fba-113">Esempio 2: abilitare la crittografia dei dati dello Store di configurazione dell'app per identità gestita assegnata dall'utente</span><span class="sxs-lookup"><span data-stu-id="37fba-113">Example 2: Enable data encryption of the app configuration store by user-assigned managed identity</span></span>
```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName kv-Name -Name key-Name -Destination 'Software'
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location $env.location -Sku 'standard' -IdentityType "UserAssigned" -UserAssignedIdentity $assignedIdentity.Id
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName kv-Name -ObjectId $assignedIdentity.PrincipalId -PermissionsToKeys get,unwrapKey,wrapKey -PassThru
PS C:\> Update-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test11 -EncryptionKeyIdentifier $key.Id -KeyVaultIdentityClientId $assignedIdentity.ClientId

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="37fba-114">Questo comando consente la crittografia dei dati tramite una chiave archiviata in Azure Key Vault usando un'identità gestita assegnata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="37fba-114">This command enables data encryption by a key stored in Azure Key Vault using a user-assigned managed identity.</span></span>
<span data-ttu-id="37fba-115">Deve essere stata impostata l'identità assegnata dall'utente `-UserAssignedIdentity` .</span><span class="sxs-lookup"><span data-stu-id="37fba-115">The user-assigned identity must have been set with `-UserAssignedIdentity`.</span></span>
<span data-ttu-id="37fba-116">Il Vault deve avere abilitato la protezione soft-delete e Purge e l'identità gestita deve avere le autorizzazioni principali seguenti: Get, wrapKey, unwrapKey.</span><span class="sxs-lookup"><span data-stu-id="37fba-116">The vault must have enabled soft-delete and purge-protection, and the managed identity must have these key permissions: get, wrapKey, unwrapKey.</span></span>

### <span data-ttu-id="37fba-117">Esempio 3: disabilitare la crittografia di un archivio di configurazione dell'app.</span><span class="sxs-lookup"><span data-stu-id="37fba-117">Example 3: Disable encryption of an app configuration store.</span></span>
```powershell
PS C:\> $appConf = Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test10 | Update-AzAppConfigurationStore -EncryptionKeyIdentifier $null

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="37fba-118">Questo comando Disabilita la crittografia di un archivio di configurazione dell'app.</span><span class="sxs-lookup"><span data-stu-id="37fba-118">This command disables encryption of an app configuration store.</span></span>

### <span data-ttu-id="37fba-119">Esempio 3: aggiornare SKU e tag di un archivio di configurazione dell'app in base alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="37fba-119">Example 3: Update sku and tag of an app configuration store by pipeline.</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test10 | Update-AzAppConfigurationStore -Sku 'standard' -Tag @{'key'='update'}

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="37fba-120">Questo comando Aggiorna SKU e tag di un archivio di configurazione dell'app in base alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="37fba-120">This command updates sku and tag of an app configuration store by pipeline.</span></span>

## <span data-ttu-id="37fba-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="37fba-121">PARAMETERS</span></span>

### <span data-ttu-id="37fba-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="37fba-122">-AsJob</span></span>
<span data-ttu-id="37fba-123">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="37fba-123">Run the command as a job</span></span>

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

### <span data-ttu-id="37fba-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37fba-124">-DefaultProfile</span></span>
<span data-ttu-id="37fba-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="37fba-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37fba-126">-EncryptionKeyIdentifier</span><span class="sxs-lookup"><span data-stu-id="37fba-126">-EncryptionKeyIdentifier</span></span>
<span data-ttu-id="37fba-127">URI della chiave del Vault chiave usata per crittografare i dati.</span><span class="sxs-lookup"><span data-stu-id="37fba-127">The URI of the key vault key used to encrypt data.</span></span>

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

### <span data-ttu-id="37fba-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="37fba-128">-IdentityType</span></span>
<span data-ttu-id="37fba-129">Tipo di identità gestita usata.</span><span class="sxs-lookup"><span data-stu-id="37fba-129">The type of managed identity used.</span></span>
<span data-ttu-id="37fba-130">Il tipo ' SystemAssignedAndUserAssigned ' include sia un'identità creata in modo implicito che un set di identità assegnate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="37fba-130">The type 'SystemAssignedAndUserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="37fba-131">Il tipo "None" rimuoverà le identità.</span><span class="sxs-lookup"><span data-stu-id="37fba-131">The type 'None' will remove any identities.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Support.IdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37fba-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37fba-132">-InputObject</span></span>
<span data-ttu-id="37fba-133">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="37fba-133">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37fba-134">-KeyVaultIdentityClientId</span><span class="sxs-lookup"><span data-stu-id="37fba-134">-KeyVaultIdentityClientId</span></span>
<span data-ttu-id="37fba-135">ID client dell'identità che verrà usata per accedere a Key Vault.</span><span class="sxs-lookup"><span data-stu-id="37fba-135">The client id of the identity which will be used to access key vault.</span></span>

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

### <span data-ttu-id="37fba-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="37fba-136">-Name</span></span>
<span data-ttu-id="37fba-137">Nome dell'archivio di configurazione.</span><span class="sxs-lookup"><span data-stu-id="37fba-137">The name of the configuration store.</span></span>

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

### <span data-ttu-id="37fba-138">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="37fba-138">-NoWait</span></span>
<span data-ttu-id="37fba-139">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="37fba-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="37fba-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37fba-140">-ResourceGroupName</span></span>
<span data-ttu-id="37fba-141">Nome del gruppo di risorse a cui appartiene il registro di sistema del contenitore.</span><span class="sxs-lookup"><span data-stu-id="37fba-141">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="37fba-142">-SKU</span><span class="sxs-lookup"><span data-stu-id="37fba-142">-Sku</span></span>
<span data-ttu-id="37fba-143">Il nome SKU dell'archivio di configurazione.</span><span class="sxs-lookup"><span data-stu-id="37fba-143">The SKU name of the configuration store.</span></span>

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

### <span data-ttu-id="37fba-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="37fba-144">-SubscriptionId</span></span>
<span data-ttu-id="37fba-145">ID abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="37fba-145">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="37fba-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="37fba-146">-Tag</span></span>
<span data-ttu-id="37fba-147">Tag delle risorse ARM.</span><span class="sxs-lookup"><span data-stu-id="37fba-147">The ARM resource tags.</span></span>

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

### <span data-ttu-id="37fba-148">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="37fba-148">-UserAssignedIdentity</span></span>
<span data-ttu-id="37fba-149">Elenco delle identità assegnate dall'utente associato alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="37fba-149">The list of user-assigned identities associated with the resource.</span></span>
<span data-ttu-id="37fba-150">Le chiavi del dizionario delle identità assegnate dall'utente saranno ID delle risorse ARM nella forma:'/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span><span class="sxs-lookup"><span data-stu-id="37fba-150">The user-assigned identity dictionary keys will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="37fba-151">-Confermare</span><span class="sxs-lookup"><span data-stu-id="37fba-151">-Confirm</span></span>
<span data-ttu-id="37fba-152">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37fba-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37fba-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37fba-153">-WhatIf</span></span>
<span data-ttu-id="37fba-154">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="37fba-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37fba-155">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="37fba-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37fba-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37fba-156">CommonParameters</span></span>
<span data-ttu-id="37fba-157">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37fba-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37fba-158">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37fba-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37fba-159">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="37fba-159">INPUTS</span></span>

### <span data-ttu-id="37fba-160">Microsoft. Azure. PowerShell. Cmdlets. AppConfiguration. Models. IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="37fba-160">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="37fba-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="37fba-161">OUTPUTS</span></span>

### <span data-ttu-id="37fba-162">Microsoft. Azure. PowerShell. Cmdlets. AppConfiguration. Models. Api20200601. IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="37fba-162">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="37fba-163">Note</span><span class="sxs-lookup"><span data-stu-id="37fba-163">NOTES</span></span>

<span data-ttu-id="37fba-164">ALIAS</span><span class="sxs-lookup"><span data-stu-id="37fba-164">ALIASES</span></span>

<span data-ttu-id="37fba-165">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="37fba-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="37fba-166">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="37fba-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="37fba-167">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="37fba-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="37fba-168">INPUTOBJECT <IAppConfigurationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="37fba-168">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="37fba-169">`[ConfigStoreName <String>]`: Nome dell'archivio di configurazione.</span><span class="sxs-lookup"><span data-stu-id="37fba-169">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="37fba-170">`[GroupName <String>]`: Nome del gruppo di risorse private link.</span><span class="sxs-lookup"><span data-stu-id="37fba-170">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="37fba-171">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="37fba-171">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="37fba-172">`[PrivateEndpointConnectionName <String>]`: Nome connessione endpoint privato</span><span class="sxs-lookup"><span data-stu-id="37fba-172">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="37fba-173">`[ResourceGroupName <String>]`: Nome del gruppo di risorse a cui appartiene il registro di sistema del contenitore.</span><span class="sxs-lookup"><span data-stu-id="37fba-173">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="37fba-174">`[SubscriptionId <String>]`: ID abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="37fba-174">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="37fba-175">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="37fba-175">RELATED LINKS</span></span>



<span data-ttu-id="37fba-176">[Set-AzKeyVaultAccessPolicy](https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy?view=azps-4.4.0) 
 [New-AzUserAssignedIdentity](https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)</span><span class="sxs-lookup"><span data-stu-id="37fba-176">[Set-AzKeyVaultAccessPolicy](https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy?view=azps-4.4.0)
[New-AzUserAssignedIdentity](https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)</span></span>

