---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
ms.openlocfilehash: 0da8ce1e7da509c140e5893240fadb37d7852ad8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367779"
---
# <span data-ttu-id="969f5-101">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="969f5-101">New-AzKeyVault</span></span>

## <span data-ttu-id="969f5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="969f5-102">SYNOPSIS</span></span>
<span data-ttu-id="969f5-103">Crea un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="969f5-103">Creates a key vault.</span></span>

## <span data-ttu-id="969f5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="969f5-104">SYNTAX</span></span>

```
New-AzKeyVault [-Name] <String> [-ResourceGroupName] <String> [-Location] <String> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-EnablePurgeProtection]
 [-EnableRbacAuthorization] [-SoftDeleteRetentionInDays <Int32>] [-Sku <String>] [-Tag <Hashtable>]
 [-NetworkRuleSet <PSKeyVaultNetworkRuleSet>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="969f5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="969f5-105">DESCRIPTION</span></span>
<span data-ttu-id="969f5-106">Il cmdlet **New-AzKeyVault** crea un Vault Key nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="969f5-106">The **New-AzKeyVault** cmdlet creates a key vault in the specified resource group.</span></span> <span data-ttu-id="969f5-107">Questo cmdlet concede anche le autorizzazioni per l'utente attualmente connesso per aggiungere, rimuovere o elencare chiavi e segreti nel caveau della chiave.</span><span class="sxs-lookup"><span data-stu-id="969f5-107">This cmdlet also grants permissions to the currently logged on user to add, remove, or list keys and secrets in the key vault.</span></span>
<span data-ttu-id="969f5-108">Nota: se viene visualizzato l'errore **l'abbonamento non è registrato per l'uso dello spazio dei nomi "Microsoft. Key Vault"** quando si tenta di creare il nuovo Vault chiave, eseguire **Register-AzResourceProvider-ProviderNamespace "Microsoft. Key Vault"** e quindi eseguire di nuovo il comando **New-AzKeyVault** .</span><span class="sxs-lookup"><span data-stu-id="969f5-108">Note: If you see the error **The subscription is not registered to use namespace 'Microsoft.KeyVault'** when you try to create your new key vault, run **Register-AzResourceProvider -ProviderNamespace "Microsoft.KeyVault"** and then rerun your **New-AzKeyVault** command.</span></span> <span data-ttu-id="969f5-109">Per altre informazioni, vedere Register-AzResourceProvider.</span><span class="sxs-lookup"><span data-stu-id="969f5-109">For more information, see Register-AzResourceProvider.</span></span>

## <span data-ttu-id="969f5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="969f5-110">EXAMPLES</span></span>

### <span data-ttu-id="969f5-111">Esempio 1: creare un Vault chiave standard</span><span class="sxs-lookup"><span data-stu-id="969f5-111">Example 1: Create a Standard key vault</span></span>
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

<span data-ttu-id="969f5-112">Questo comando crea un Vault chiave denominato Contoso03Vault, nell'area di Azure est US.</span><span class="sxs-lookup"><span data-stu-id="969f5-112">This command creates a key vault named Contoso03Vault, in the Azure region East US.</span></span> <span data-ttu-id="969f5-113">Il comando aggiunge il Vault chiave al gruppo di risorse denominato Group14.</span><span class="sxs-lookup"><span data-stu-id="969f5-113">The command adds the key vault to the resource group named Group14.</span></span> <span data-ttu-id="969f5-114">Poiché il comando non specifica un valore per il parametro *SKU* , crea un Vault chiave standard.</span><span class="sxs-lookup"><span data-stu-id="969f5-114">Because the command does not specify a value for the *SKU* parameter, it creates a Standard key vault.</span></span>

### <span data-ttu-id="969f5-115">Esempio 2: creare un Vault Key Premium</span><span class="sxs-lookup"><span data-stu-id="969f5-115">Example 2: Create a Premium key vault</span></span>
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

<span data-ttu-id="969f5-116">Questo comando crea un Vault chiave, proprio come nell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="969f5-116">This command creates a key vault, just like the previous example.</span></span> <span data-ttu-id="969f5-117">Tuttavia, specifica un valore Premium per il parametro *SKU* per creare un Vault Key Premium.</span><span class="sxs-lookup"><span data-stu-id="969f5-117">However, it specifies a value of Premium for the *SKU* parameter to create a Premium key vault.</span></span>

### <span data-ttu-id="969f5-118">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="969f5-118">Example 3</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "110.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "110.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> $ruleSet = New-AzKeyVaultNetworkRuleSetObject -DefaultAction Allow -Bypass AzureServices -IpAddressRange "110.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId
PS C:\> New-AzKeyVault -ResourceGroupName "myRg" -VaultName "myVault" -NetworkRuleSet $ruleSet
```

<span data-ttu-id="969f5-119">Creare un Vault chiave e specificare le regole di rete per consentire l'accesso all'indirizzo IP specificato dalla rete virtuale identificata da $myNetworkResId.</span><span class="sxs-lookup"><span data-stu-id="969f5-119">Creating a key vault and specifies network rules to allow access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span> <span data-ttu-id="969f5-120">`New-AzKeyVaultNetworkRuleSetObject`Per altre informazioni, vedere.</span><span class="sxs-lookup"><span data-stu-id="969f5-120">See `New-AzKeyVaultNetworkRuleSetObject` for more information.</span></span>

## <span data-ttu-id="969f5-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="969f5-121">PARAMETERS</span></span>

### <span data-ttu-id="969f5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="969f5-122">-DefaultProfile</span></span>
<span data-ttu-id="969f5-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="969f5-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="969f5-124">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="969f5-124">-EnabledForDeployment</span></span>
<span data-ttu-id="969f5-125">Consente al provider di risorse Microsoft. Compute di recuperare i segreti da questo Vault chiave quando si fa riferimento a questo Vault chiave nella creazione di risorse, ad esempio quando si crea una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="969f5-125">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

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

### <span data-ttu-id="969f5-126">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="969f5-126">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="969f5-127">Abilita il servizio di crittografia di Azure disk per ottenere segreti e scartare le chiavi da questo caveau chiave.</span><span class="sxs-lookup"><span data-stu-id="969f5-127">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

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

### <span data-ttu-id="969f5-128">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="969f5-128">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="969f5-129">Consente a Azure Resource Manager di ottenere segreti da questo Vault chiave quando si fa riferimento a questo Vault chiave in una distribuzione di modelli.</span><span class="sxs-lookup"><span data-stu-id="969f5-129">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

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

### <span data-ttu-id="969f5-130">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="969f5-130">-EnablePurgeProtection</span></span>
<span data-ttu-id="969f5-131">Se specificato, la protezione dall'eliminazione immediata è abilitata per il Vault; è necessario abilitare l'eliminazione morbida anche.</span><span class="sxs-lookup"><span data-stu-id="969f5-131">If specified, protection against immediate deletion is enabled for this vault; requires soft delete to be enabled as well.</span></span>

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

### <span data-ttu-id="969f5-132">-EnableRbacAuthorization</span><span class="sxs-lookup"><span data-stu-id="969f5-132">-EnableRbacAuthorization</span></span>
<span data-ttu-id="969f5-133">Se specificato, consente di autorizzare le azioni di dati tramite il controllo di accesso basato sui ruoli (RBAC) e quindi i criteri di accesso specificati nelle proprietà del Vault verranno ignorati.</span><span class="sxs-lookup"><span data-stu-id="969f5-133">If specified, enables to authorize data actions by Role Based Access Control (RBAC), and then the access policies specified in vault properties will be ignored.</span></span> <span data-ttu-id="969f5-134">Tieni presente che le azioni di gestione sono sempre autorizzate con RBAC.</span><span class="sxs-lookup"><span data-stu-id="969f5-134">Note that management actions are always authorized with RBAC.</span></span>

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

### <span data-ttu-id="969f5-135">-Posizione</span><span class="sxs-lookup"><span data-stu-id="969f5-135">-Location</span></span>
<span data-ttu-id="969f5-136">Specifica l'area di Azure in cui creare il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="969f5-136">Specifies the Azure region in which to create the key vault.</span></span> <span data-ttu-id="969f5-137">Usare il comando [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) per visualizzare le opzioni desiderate.</span><span class="sxs-lookup"><span data-stu-id="969f5-137">Use the command [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) to see your choices.</span></span>

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

### <span data-ttu-id="969f5-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="969f5-138">-Name</span></span>
<span data-ttu-id="969f5-139">Specifica un nome per il Vault della chiave da creare.</span><span class="sxs-lookup"><span data-stu-id="969f5-139">Specifies a name of the key vault to create.</span></span> <span data-ttu-id="969f5-140">Il nome può essere costituito da qualsiasi combinazione di lettere, cifre o trattini.</span><span class="sxs-lookup"><span data-stu-id="969f5-140">The name can be any combination of letters, digits, or hyphens.</span></span> <span data-ttu-id="969f5-141">Il nome deve iniziare e terminare con una lettera o una cifra.</span><span class="sxs-lookup"><span data-stu-id="969f5-141">The name must start and end with a letter or digit.</span></span> <span data-ttu-id="969f5-142">Il nome deve essere universalmente univoco.</span><span class="sxs-lookup"><span data-stu-id="969f5-142">The name must be universally unique.</span></span>

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

### <span data-ttu-id="969f5-143">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="969f5-143">-NetworkRuleSet</span></span>
<span data-ttu-id="969f5-144">Specifica il set di regole di rete del Vault.</span><span class="sxs-lookup"><span data-stu-id="969f5-144">Specifies the network rule set of the vault.</span></span> <span data-ttu-id="969f5-145">Regola l'accessibilità del Vault chiave da posizioni di rete specifiche.</span><span class="sxs-lookup"><span data-stu-id="969f5-145">It governs the accessibility of the key vault from specific network locations.</span></span> <span data-ttu-id="969f5-146">Creato da `New-AzKeyVaultNetworkRuleSetObject` .</span><span class="sxs-lookup"><span data-stu-id="969f5-146">Created by `New-AzKeyVaultNetworkRuleSetObject`.</span></span>

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

### <span data-ttu-id="969f5-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="969f5-147">-ResourceGroupName</span></span>
<span data-ttu-id="969f5-148">Specifica il nome di un gruppo di risorse esistente in cui creare il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="969f5-148">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="969f5-149">-SKU</span><span class="sxs-lookup"><span data-stu-id="969f5-149">-Sku</span></span>
<span data-ttu-id="969f5-150">Specifica l'USK dell'istanza Key Vault.</span><span class="sxs-lookup"><span data-stu-id="969f5-150">Specifies the SKU of the key vault instance.</span></span> <span data-ttu-id="969f5-151">Per informazioni sulle caratteristiche disponibili per ogni Usk, vedere il sito Web relativo ai prezzi di Azure Key Vault ( https://go.microsoft.com/fwlink/?linkid=512521) .</span><span class="sxs-lookup"><span data-stu-id="969f5-151">For information about which features are available for each SKU, see the Azure Key Vault Pricing website (https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

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

### <span data-ttu-id="969f5-152">-SoftDeleteRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="969f5-152">-SoftDeleteRetentionInDays</span></span>
<span data-ttu-id="969f5-153">Specifica il periodo di conservazione delle risorse eliminate e la durata della cancellazione di un Vault o di un oggetto nello stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="969f5-153">Specifies how long deleted resources are retained, and how long until a vault or an object in the deleted state can be purged.</span></span> <span data-ttu-id="969f5-154">Il valore predefinito è 90 giorni.</span><span class="sxs-lookup"><span data-stu-id="969f5-154">The default is 90 days.</span></span>

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

### <span data-ttu-id="969f5-155">-Tag</span><span class="sxs-lookup"><span data-stu-id="969f5-155">-Tag</span></span>
<span data-ttu-id="969f5-156">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="969f5-156">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="969f5-157">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="969f5-157">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="969f5-158">-Confermare</span><span class="sxs-lookup"><span data-stu-id="969f5-158">-Confirm</span></span>
<span data-ttu-id="969f5-159">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="969f5-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="969f5-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="969f5-160">-WhatIf</span></span>
<span data-ttu-id="969f5-161">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="969f5-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="969f5-162">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="969f5-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="969f5-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="969f5-163">CommonParameters</span></span>
<span data-ttu-id="969f5-164">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="969f5-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="969f5-165">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="969f5-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="969f5-166">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="969f5-166">INPUTS</span></span>

### <span data-ttu-id="969f5-167">System. String</span><span class="sxs-lookup"><span data-stu-id="969f5-167">System.String</span></span>

### <span data-ttu-id="969f5-168">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="969f5-168">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="969f5-169">Microsoft. Azure. Management. DataVault. Models. SkuName</span><span class="sxs-lookup"><span data-stu-id="969f5-169">Microsoft.Azure.Management.KeyVault.Models.SkuName</span></span>

### <span data-ttu-id="969f5-170">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="969f5-170">System.Collections.Hashtable</span></span>

## <span data-ttu-id="969f5-171">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="969f5-171">OUTPUTS</span></span>

### <span data-ttu-id="969f5-172">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="969f5-172">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="969f5-173">Note</span><span class="sxs-lookup"><span data-stu-id="969f5-173">NOTES</span></span>

## <span data-ttu-id="969f5-174">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="969f5-174">RELATED LINKS</span></span>

[<span data-ttu-id="969f5-175">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="969f5-175">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="969f5-176">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="969f5-176">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)
