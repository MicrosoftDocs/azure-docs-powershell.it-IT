---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://docs.microsoft.com/powershell/module/az.keyvault/new-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
ms.openlocfilehash: 6af82533540bd93b90847c51b9aaf0bd603dc727
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001374"
---
# <span data-ttu-id="d4020-101">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="d4020-101">New-AzKeyVault</span></span>

## <span data-ttu-id="d4020-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4020-102">SYNOPSIS</span></span>
<span data-ttu-id="d4020-103">Crea un vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="d4020-103">Creates a key vault.</span></span>

## <span data-ttu-id="d4020-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d4020-104">SYNTAX</span></span>

```
New-AzKeyVault [-Name] <String> [-ResourceGroupName] <String> [-Location] <String> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-EnablePurgeProtection]
 [-EnableRbacAuthorization] [-SoftDeleteRetentionInDays <Int32>] [-Sku <String>] [-Tag <Hashtable>]
 [-NetworkRuleSet <PSKeyVaultNetworkRuleSet>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d4020-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d4020-105">DESCRIPTION</span></span>
<span data-ttu-id="d4020-106">Il cmdlet **New-AzKeyVault** crea un vault delle chiavi nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="d4020-106">The **New-AzKeyVault** cmdlet creates a key vault in the specified resource group.</span></span> <span data-ttu-id="d4020-107">Questo cmdlet concede anche all'utente attualmente connesso le autorizzazioni per aggiungere, rimuovere o elencare chiavi e segreti nel vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="d4020-107">This cmdlet also grants permissions to the currently logged on user to add, remove, or list keys and secrets in the key vault.</span></span>
<span data-ttu-id="d4020-108">Nota: se viene visualizzato l'errore L'abbonamento non è registrato per l'uso dello spazio dei nomi **'Microsoft.KeyVault'** quando si prova a creare il nuovo vault delle chiavi, eseguire **Register-AzResourceProvider -ProviderResource "Microsoft.KeyVault"** e quindi eseguire di nuovo il comando **New-AzKeyVault.**</span><span class="sxs-lookup"><span data-stu-id="d4020-108">Note: If you see the error **The subscription is not registered to use namespace 'Microsoft.KeyVault'** when you try to create your new key vault, run **Register-AzResourceProvider -ProviderNamespace "Microsoft.KeyVault"** and then rerun your **New-AzKeyVault** command.</span></span> <span data-ttu-id="d4020-109">Per altre informazioni, vedere Register-AzResourceProvider.</span><span class="sxs-lookup"><span data-stu-id="d4020-109">For more information, see Register-AzResourceProvider.</span></span>

## <span data-ttu-id="d4020-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d4020-110">EXAMPLES</span></span>

### <span data-ttu-id="d4020-111">Esempio 1: Creare un vault delle chiavi standard</span><span class="sxs-lookup"><span data-stu-id="d4020-111">Example 1: Create a Standard key vault</span></span>
```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'

Vault Name                       : contoso03vault
Resource Group Name              : group14
Location                         : East US
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/group14/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : False
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             :
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : get, create, delete, list, update,
                                   import, backup, restore, recover
                                   Permissions to Secrets                     : get, list, set, delete, backup,
                                   restore, recover
                                   Permissions to Certificates                : get, delete, list, create, import,
                                   update, deleteissuers, getissuers, listissuers, managecontacts, manageissuers,
                                   setissuers, recover, backup, restore
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update, recover, backup, restore

Tags                             :
```

<span data-ttu-id="d4020-112">Questo comando crea una chiave vault denominata Contoso03Vault, nell'area di Azure negli Stati Uniti orientali.</span><span class="sxs-lookup"><span data-stu-id="d4020-112">This command creates a key vault named Contoso03Vault, in the Azure region East US.</span></span> <span data-ttu-id="d4020-113">Il comando aggiunge la chiave vault al gruppo di risorse denominato Gruppo14.</span><span class="sxs-lookup"><span data-stu-id="d4020-113">The command adds the key vault to the resource group named Group14.</span></span> <span data-ttu-id="d4020-114">Poiché il comando non specifica un valore per il *parametro SKU,* crea un vault di chiavi standard.</span><span class="sxs-lookup"><span data-stu-id="d4020-114">Because the command does not specify a value for the *SKU* parameter, it creates a Standard key vault.</span></span>

### <span data-ttu-id="d4020-115">Esempio 2: Creare un vault chiave Premium</span><span class="sxs-lookup"><span data-stu-id="d4020-115">Example 2: Create a Premium key vault</span></span>
```powershell
PS C:\>New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -Sku 'Premium'

Vault Name                       : contoso03vault
Resource Group Name              : group14
Location                         : East US
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/group14/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Premium
Enabled For Deployment?          : False
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             :
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : get, create, delete, list, update,
                                   import, backup, restore, recover
                                   Permissions to Secrets                     : get, list, set, delete, backup,
                                   restore, recover
                                   Permissions to Certificates                : get, delete, list, create, import,
                                   update, deleteissuers, getissuers, listissuers, managecontacts, manageissuers,
                                   setissuers, recover, backup, restore
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update, recover, backup, restore

Tags                             :
```

<span data-ttu-id="d4020-116">Questo comando crea un vault delle chiavi, come nell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="d4020-116">This command creates a key vault, just like the previous example.</span></span> <span data-ttu-id="d4020-117">Specifica tuttavia un valore Premium per il parametro *SKU* per creare un vault delle chiavi Premium.</span><span class="sxs-lookup"><span data-stu-id="d4020-117">However, it specifies a value of Premium for the *SKU* parameter to create a Premium key vault.</span></span>

### <span data-ttu-id="d4020-118">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="d4020-118">Example 3</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "110.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "110.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> $ruleSet = New-AzKeyVaultNetworkRuleSetObject -DefaultAction Allow -Bypass AzureServices -IpAddressRange "110.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId
PS C:\> New-AzKeyVault -ResourceGroupName "myRg" -VaultName "myVault" -NetworkRuleSet $ruleSet
```

<span data-ttu-id="d4020-119">Creazione di un vault delle chiavi e specifica le regole di rete per consentire l'accesso all'indirizzo IP specificato dalla rete virtuale identificata $myNetworkResId.</span><span class="sxs-lookup"><span data-stu-id="d4020-119">Creating a key vault and specifies network rules to allow access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span> <span data-ttu-id="d4020-120">Per `New-AzKeyVaultNetworkRuleSetObject` altre informazioni, vedere.</span><span class="sxs-lookup"><span data-stu-id="d4020-120">See `New-AzKeyVaultNetworkRuleSetObject` for more information.</span></span>

## <span data-ttu-id="d4020-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4020-121">PARAMETERS</span></span>

### <span data-ttu-id="d4020-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4020-122">-DefaultProfile</span></span>
<span data-ttu-id="d4020-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d4020-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4020-124">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="d4020-124">-EnabledForDeployment</span></span>
<span data-ttu-id="d4020-125">Consente al provider di risorse Microsoft.Compute di recuperare i dati nascosti da questo vault della chiave quando si fa riferimento a questo vault chiave nella creazione di risorse, ad esempio durante la creazione di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d4020-125">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4020-126">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="d4020-126">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="d4020-127">Consente al servizio di crittografia del disco di Azure di ottenere informazioni segrete e chiavi di annullamento della sincronizzazione da questo vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="d4020-127">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4020-128">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="d4020-128">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="d4020-129">Consente a Gestione risorse di Azure di ottenere informazioni segrete da questo vault chiave quando si fa riferimento a questo vault chiave in una distribuzione di modelli.</span><span class="sxs-lookup"><span data-stu-id="d4020-129">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4020-130">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="d4020-130">-EnablePurgeProtection</span></span>
<span data-ttu-id="d4020-131">Se specificato, la protezione contro l'eliminazione immediata è abilitata per questo vault; richiede che sia abilitata anche l'eliminazione rescisa.</span><span class="sxs-lookup"><span data-stu-id="d4020-131">If specified, protection against immediate deletion is enabled for this vault; requires soft delete to be enabled as well.</span></span>

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

### <span data-ttu-id="d4020-132">-EnableRbacAuthorization</span><span class="sxs-lookup"><span data-stu-id="d4020-132">-EnableRbacAuthorization</span></span>
<span data-ttu-id="d4020-133">Se specificato, consente di autorizzare le azioni dei dati tramite il controllo dell'accesso basato sui ruoli e quindi i criteri di accesso specificati nelle proprietà del vault verranno ignorati.</span><span class="sxs-lookup"><span data-stu-id="d4020-133">If specified, enables to authorize data actions by Role Based Access Control (RBAC), and then the access policies specified in vault properties will be ignored.</span></span> <span data-ttu-id="d4020-134">Si noti che le azioni di gestione sono sempre autorizzate con il controllo degli accessi in base al ruolo.</span><span class="sxs-lookup"><span data-stu-id="d4020-134">Note that management actions are always authorized with RBAC.</span></span>

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

### <span data-ttu-id="d4020-135">-Location</span><span class="sxs-lookup"><span data-stu-id="d4020-135">-Location</span></span>
<span data-ttu-id="d4020-136">Specifica l'area geografica di Azure in cui creare il vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="d4020-136">Specifies the Azure region in which to create the key vault.</span></span> <span data-ttu-id="d4020-137">Usare il comando [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) per visualizzare le opzioni disponibili.</span><span class="sxs-lookup"><span data-stu-id="d4020-137">Use the command [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) to see your choices.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4020-138">-Name</span><span class="sxs-lookup"><span data-stu-id="d4020-138">-Name</span></span>
<span data-ttu-id="d4020-139">Specifica un nome del vault della chiave da creare.</span><span class="sxs-lookup"><span data-stu-id="d4020-139">Specifies a name of the key vault to create.</span></span> <span data-ttu-id="d4020-140">Il nome può essere qualsiasi combinazione di lettere, cifre o trattini.</span><span class="sxs-lookup"><span data-stu-id="d4020-140">The name can be any combination of letters, digits, or hyphens.</span></span> <span data-ttu-id="d4020-141">Il nome deve iniziare e terminare con una lettera o una cifra.</span><span class="sxs-lookup"><span data-stu-id="d4020-141">The name must start and end with a letter or digit.</span></span> <span data-ttu-id="d4020-142">Il nome deve essere universalmente univoco.</span><span class="sxs-lookup"><span data-stu-id="d4020-142">The name must be universally unique.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VaultName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4020-143">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d4020-143">-NetworkRuleSet</span></span>
<span data-ttu-id="d4020-144">Specifica il set di regole di rete del vault.</span><span class="sxs-lookup"><span data-stu-id="d4020-144">Specifies the network rule set of the vault.</span></span> <span data-ttu-id="d4020-145">Regola l'accessibilità del vault delle chiavi da percorsi di rete specifici.</span><span class="sxs-lookup"><span data-stu-id="d4020-145">It governs the accessibility of the key vault from specific network locations.</span></span> <span data-ttu-id="d4020-146">Creato `New-AzKeyVaultNetworkRuleSetObject` da.</span><span class="sxs-lookup"><span data-stu-id="d4020-146">Created by `New-AzKeyVaultNetworkRuleSetObject`.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4020-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4020-147">-ResourceGroupName</span></span>
<span data-ttu-id="d4020-148">Specifica il nome di un gruppo di risorse esistente in cui creare il vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="d4020-148">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4020-149">-SKU</span><span class="sxs-lookup"><span data-stu-id="d4020-149">-Sku</span></span>
<span data-ttu-id="d4020-150">Specifica lo SKU dell'istanza del vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="d4020-150">Specifies the SKU of the key vault instance.</span></span> <span data-ttu-id="d4020-151">Per informazioni sulle caratteristiche disponibili per ogni SKU, vedere il sito Web prezzi del Vault delle chiavi di Azure ( https://go.microsoft.com/fwlink/?linkid=512521) .</span><span class="sxs-lookup"><span data-stu-id="d4020-151">For information about which features are available for each SKU, see the Azure Key Vault Pricing website (https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4020-152">-SoftDeleteRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="d4020-152">-SoftDeleteRetentionInDays</span></span>
<span data-ttu-id="d4020-153">Specifica per quanto tempo vengono conservate le risorse eliminate e per quanto tempo può essere eliminato un vault o un oggetto in stato di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="d4020-153">Specifies how long deleted resources are retained, and how long until a vault or an object in the deleted state can be purged.</span></span> <span data-ttu-id="d4020-154">L'impostazione predefinita è 90 giorni.</span><span class="sxs-lookup"><span data-stu-id="d4020-154">The default is 90 days.</span></span>

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

### <span data-ttu-id="d4020-155">-Tag</span><span class="sxs-lookup"><span data-stu-id="d4020-155">-Tag</span></span>
<span data-ttu-id="d4020-156">Coppie chiave-valore sotto forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="d4020-156">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d4020-157">Ad esempio: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="d4020-157">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4020-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d4020-158">-Confirm</span></span>
<span data-ttu-id="d4020-159">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4020-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4020-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4020-160">-WhatIf</span></span>
<span data-ttu-id="d4020-161">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d4020-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4020-162">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d4020-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4020-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4020-163">CommonParameters</span></span>
<span data-ttu-id="d4020-164">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4020-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4020-165">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d4020-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4020-166">INPUT</span><span class="sxs-lookup"><span data-stu-id="d4020-166">INPUTS</span></span>

### <span data-ttu-id="d4020-167">System.String</span><span class="sxs-lookup"><span data-stu-id="d4020-167">System.String</span></span>

### <span data-ttu-id="d4020-168">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d4020-168">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="d4020-169">Microsoft.Azure.Management.KeyVault.Models.SkuName</span><span class="sxs-lookup"><span data-stu-id="d4020-169">Microsoft.Azure.Management.KeyVault.Models.SkuName</span></span>

### <span data-ttu-id="d4020-170">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="d4020-170">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d4020-171">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d4020-171">OUTPUTS</span></span>

### <span data-ttu-id="d4020-172">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="d4020-172">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="d4020-173">NOTE</span><span class="sxs-lookup"><span data-stu-id="d4020-173">NOTES</span></span>

## <span data-ttu-id="d4020-174">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d4020-174">RELATED LINKS</span></span>

[<span data-ttu-id="d4020-175">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="d4020-175">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="d4020-176">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="d4020-176">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)
