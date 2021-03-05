---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/powershell/module/az.appconfiguration/update-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Update-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Update-AzAppConfigurationStore.md
ms.openlocfilehash: b8297580f088678f1fdd61b8bff670adb03d2bcf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965309"
---
# <span data-ttu-id="f6185-101">Update-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="f6185-101">Update-AzAppConfigurationStore</span></span>

## <span data-ttu-id="f6185-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6185-102">SYNOPSIS</span></span>
<span data-ttu-id="f6185-103">Aggiorna un archivio di configurazione con i parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="f6185-103">Updates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="f6185-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f6185-104">SYNTAX</span></span>

### <span data-ttu-id="f6185-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f6185-105">UpdateExpanded (Default)</span></span>
```
Update-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EncryptionKeyIdentifier <String>] [-IdentityType <IdentityType>] [-KeyVaultIdentityClientId <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f6185-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f6185-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-EncryptionKeyIdentifier <String>]
 [-IdentityType <IdentityType>] [-KeyVaultIdentityClientId <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="f6185-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f6185-107">DESCRIPTION</span></span>
<span data-ttu-id="f6185-108">Aggiorna un archivio di configurazione con i parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="f6185-108">Updates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="f6185-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f6185-109">EXAMPLES</span></span>

### <span data-ttu-id="f6185-110">Esempio 1: Abilitare la crittografia dei dati dell'archivio di configurazione delle app in base all'identità gestita assegnata dal sistema</span><span class="sxs-lookup"><span data-stu-id="f6185-110">Example 1: Enable data encryption of the app configuration store by system-assigned managed identity</span></span>
```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName kv-Name -Name key-Name -Destination 'Software'
PS C:\> $systemAssignedAppStore = New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location $env.location -Sku 'standard' -IdentityType "SystemAssigned"
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName kv-Name -ObjectId $systemAssignedAppStore.IdentityPrincipalId -PermissionsToKeys get,unwrapKey,wrapKey -PassThru
PS C:\> Update-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -EncryptionKeyIdentifier $key.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="f6185-111">Questo comando abilita la crittografia dei dati con una chiave archiviata nel Vault della chiave di Azure usando un'identità gestita assegnata al sistema.</span><span class="sxs-lookup"><span data-stu-id="f6185-111">This command enables data encryption by a key stored in Azure Key Vault using a system-assigned managed identity.</span></span>
<span data-ttu-id="f6185-112">Il vault deve aver abilitato l'eliminazione soft e la protezione per l'eliminazione e l'identità gestita deve avere le autorizzazioni chiave seguenti: get, wrapKey, unwrapKey.</span><span class="sxs-lookup"><span data-stu-id="f6185-112">The vault must have enabled soft-delete and purge-protection, and the managed identity must have these key permissions: get, wrapKey, unwrapKey.</span></span>

### <span data-ttu-id="f6185-113">Esempio 2: Abilitare la crittografia dei dati dell'archivio di configurazione delle app in base all'identità gestita assegnata dall'utente</span><span class="sxs-lookup"><span data-stu-id="f6185-113">Example 2: Enable data encryption of the app configuration store by user-assigned managed identity</span></span>
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

<span data-ttu-id="f6185-114">Questo comando abilita la crittografia dei dati con una chiave archiviata nel Vault della chiave di Azure usando un'identità gestita assegnata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="f6185-114">This command enables data encryption by a key stored in Azure Key Vault using a user-assigned managed identity.</span></span>
<span data-ttu-id="f6185-115">L'identità assegnata all'utente deve essere stata impostata con `-UserAssignedIdentity` .</span><span class="sxs-lookup"><span data-stu-id="f6185-115">The user-assigned identity must have been set with `-UserAssignedIdentity`.</span></span>
<span data-ttu-id="f6185-116">Il vault deve aver abilitato l'eliminazione soft e la protezione per l'eliminazione e l'identità gestita deve avere le autorizzazioni chiave seguenti: get, wrapKey, unwrapKey.</span><span class="sxs-lookup"><span data-stu-id="f6185-116">The vault must have enabled soft-delete and purge-protection, and the managed identity must have these key permissions: get, wrapKey, unwrapKey.</span></span>

### <span data-ttu-id="f6185-117">Esempio 3: Disabilitare la crittografia di un archivio di configurazione delle app.</span><span class="sxs-lookup"><span data-stu-id="f6185-117">Example 3: Disable encryption of an app configuration store.</span></span>
```powershell
PS C:\> $appConf = Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test10 | Update-AzAppConfigurationStore -EncryptionKeyIdentifier $null

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="f6185-118">Questo comando disabilita la crittografia di un archivio di configurazione delle app.</span><span class="sxs-lookup"><span data-stu-id="f6185-118">This command disables encryption of an app configuration store.</span></span>

### <span data-ttu-id="f6185-119">Esempio 3: Aggiornare sKU e tag di un archivio di configurazione dell'app in base alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="f6185-119">Example 3: Update sku and tag of an app configuration store by pipeline.</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test10 | Update-AzAppConfigurationStore -Sku 'standard' -Tag @{'key'='update'}

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="f6185-120">Questo comando aggiorna sKU e tag di un archivio di configurazione delle app in base alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="f6185-120">This command updates sku and tag of an app configuration store by pipeline.</span></span>

## <span data-ttu-id="f6185-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f6185-121">PARAMETERS</span></span>

### <span data-ttu-id="f6185-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f6185-122">-AsJob</span></span>
<span data-ttu-id="f6185-123">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="f6185-123">Run the command as a job</span></span>

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

### <span data-ttu-id="f6185-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6185-124">-DefaultProfile</span></span>
<span data-ttu-id="f6185-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f6185-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6185-126">-EncryptionKeyIdentifier</span><span class="sxs-lookup"><span data-stu-id="f6185-126">-EncryptionKeyIdentifier</span></span>
<span data-ttu-id="f6185-127">URI della chiave vault usata per crittografare i dati.</span><span class="sxs-lookup"><span data-stu-id="f6185-127">The URI of the key vault key used to encrypt data.</span></span>

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

### <span data-ttu-id="f6185-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="f6185-128">-IdentityType</span></span>
<span data-ttu-id="f6185-129">Tipo di identità gestita usata.</span><span class="sxs-lookup"><span data-stu-id="f6185-129">The type of managed identity used.</span></span>
<span data-ttu-id="f6185-130">Il tipo 'SystemAssignedAndUserAssigned' include sia un'identità creata in modo implicito che un set di identità assegnate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="f6185-130">The type 'SystemAssignedAndUserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="f6185-131">Il tipo "Nessuna" rimuove le identità.</span><span class="sxs-lookup"><span data-stu-id="f6185-131">The type 'None' will remove any identities.</span></span>

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

### <span data-ttu-id="f6185-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6185-132">-InputObject</span></span>
<span data-ttu-id="f6185-133">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="f6185-133">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f6185-134">-KeyVaultIdentityClientId</span><span class="sxs-lookup"><span data-stu-id="f6185-134">-KeyVaultIdentityClientId</span></span>
<span data-ttu-id="f6185-135">ID client dell'identità che verrà usata per accedere al vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="f6185-135">The client id of the identity which will be used to access key vault.</span></span>

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

### <span data-ttu-id="f6185-136">-Name</span><span class="sxs-lookup"><span data-stu-id="f6185-136">-Name</span></span>
<span data-ttu-id="f6185-137">Nome dell'archivio di configurazione.</span><span class="sxs-lookup"><span data-stu-id="f6185-137">The name of the configuration store.</span></span>

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

### <span data-ttu-id="f6185-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f6185-138">-NoWait</span></span>
<span data-ttu-id="f6185-139">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="f6185-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f6185-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6185-140">-ResourceGroupName</span></span>
<span data-ttu-id="f6185-141">Nome del gruppo di risorse a cui appartiene il Registro di sistema del contenitore.</span><span class="sxs-lookup"><span data-stu-id="f6185-141">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="f6185-142">-SKU</span><span class="sxs-lookup"><span data-stu-id="f6185-142">-Sku</span></span>
<span data-ttu-id="f6185-143">Nome SKU dell'archivio di configurazione.</span><span class="sxs-lookup"><span data-stu-id="f6185-143">The SKU name of the configuration store.</span></span>

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

### <span data-ttu-id="f6185-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f6185-144">-SubscriptionId</span></span>
<span data-ttu-id="f6185-145">ID sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f6185-145">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="f6185-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="f6185-146">-Tag</span></span>
<span data-ttu-id="f6185-147">Tag ARM risorse.</span><span class="sxs-lookup"><span data-stu-id="f6185-147">The ARM resource tags.</span></span>

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

### <span data-ttu-id="f6185-148">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="f6185-148">-UserAssignedIdentity</span></span>
<span data-ttu-id="f6185-149">Elenco delle identità assegnate dall'utente associate alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="f6185-149">The list of user-assigned identities associated with the resource.</span></span>
<span data-ttu-id="f6185-150">Le chiavi del dizionario di identità assegnate dall'utente saranno id di risorse nel formato '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'. ARM</span><span class="sxs-lookup"><span data-stu-id="f6185-150">The user-assigned identity dictionary keys will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="f6185-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f6185-151">-Confirm</span></span>
<span data-ttu-id="f6185-152">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6185-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6185-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6185-153">-WhatIf</span></span>
<span data-ttu-id="f6185-154">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f6185-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6185-155">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f6185-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6185-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6185-156">CommonParameters</span></span>
<span data-ttu-id="f6185-157">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6185-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6185-158">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f6185-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6185-159">INPUT</span><span class="sxs-lookup"><span data-stu-id="f6185-159">INPUTS</span></span>

### <span data-ttu-id="f6185-160">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="f6185-160">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="f6185-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f6185-161">OUTPUTS</span></span>

### <span data-ttu-id="f6185-162">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="f6185-162">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="f6185-163">NOTE</span><span class="sxs-lookup"><span data-stu-id="f6185-163">NOTES</span></span>

<span data-ttu-id="f6185-164">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f6185-164">ALIASES</span></span>

<span data-ttu-id="f6185-165">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="f6185-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f6185-166">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="f6185-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f6185-167">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f6185-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f6185-168">INPUTOBJECT <IAppConfigurationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="f6185-168">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f6185-169">`[ConfigStoreName <String>]`: nome dell'archivio di configurazione.</span><span class="sxs-lookup"><span data-stu-id="f6185-169">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="f6185-170">`[GroupName <String>]`: nome del gruppo di risorse collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="f6185-170">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="f6185-171">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="f6185-171">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f6185-172">`[PrivateEndpointConnectionName <String>]`: nome della connessione all'endpoint privato</span><span class="sxs-lookup"><span data-stu-id="f6185-172">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="f6185-173">`[ResourceGroupName <String>]`: nome del gruppo di risorse a cui appartiene il Registro di sistema del contenitore.</span><span class="sxs-lookup"><span data-stu-id="f6185-173">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="f6185-174">`[SubscriptionId <String>]`: ID sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f6185-174">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="f6185-175">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f6185-175">RELATED LINKS</span></span>



<span data-ttu-id="f6185-176">[Set-AzKeyVaultAccessPolicy](https://docs.microsoft.com/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy?view=azps-4.4.0) 
 [New-AzUserAssignedIdentity](https://docs.microsoft.com/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)</span><span class="sxs-lookup"><span data-stu-id="f6185-176">[Set-AzKeyVaultAccessPolicy](https://docs.microsoft.com/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy?view=azps-4.4.0)
[New-AzUserAssignedIdentity](https://docs.microsoft.com/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)</span></span>

