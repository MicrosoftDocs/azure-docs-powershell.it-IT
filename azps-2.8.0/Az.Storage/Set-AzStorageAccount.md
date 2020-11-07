---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
ms.openlocfilehash: 69c71cd0401b8509943ef7e5ad7316db99f03670
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93858277"
---
# <span data-ttu-id="c7470-101">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c7470-101">Set-AzStorageAccount</span></span>

## <span data-ttu-id="c7470-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c7470-102">SYNOPSIS</span></span>
<span data-ttu-id="c7470-103">Modifica un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c7470-103">Modifies a Storage account.</span></span>

## <span data-ttu-id="c7470-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c7470-104">SYNTAX</span></span>

### <span data-ttu-id="c7470-105">StorageEncryption (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c7470-105">StorageEncryption (Default)</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7470-106">KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="c7470-106">KeyvaultEncryption</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7470-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c7470-107">DESCRIPTION</span></span>
<span data-ttu-id="c7470-108">Il cmdlet **set-AzStorageAccount** modifica un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="c7470-108">The **Set-AzStorageAccount** cmdlet modifies an Azure Storage account.</span></span>
<span data-ttu-id="c7470-109">Puoi usare questo cmdlet per modificare il tipo di account, aggiornare un dominio del cliente o impostare i contrassegni in un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c7470-109">You can use this cmdlet to modify the account type, update a customer domain, or set tags on a Storage account.</span></span>

## <span data-ttu-id="c7470-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c7470-110">EXAMPLES</span></span>

### <span data-ttu-id="c7470-111">Esempio 1: impostare il tipo di account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="c7470-111">Example 1: Set the Storage account type</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Type "Standard_RAGRS"
```

<span data-ttu-id="c7470-112">Questo comando imposta il tipo di account di archiviazione su Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="c7470-112">This command sets the Storage account type to Standard_RAGRS.</span></span>

### <span data-ttu-id="c7470-113">Esempio 2: impostare un dominio personalizzato per un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="c7470-113">Example 2: Set a custom domain for a Storage account</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

<span data-ttu-id="c7470-114">Questo comando imposta un dominio personalizzato per un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c7470-114">This command sets a custom domain for a Storage account.</span></span>

### <span data-ttu-id="c7470-115">Esempio 3: impostare il valore di livello di accesso</span><span class="sxs-lookup"><span data-stu-id="c7470-115">Example 3: Set the access tier value</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AccessTier Cool
```

<span data-ttu-id="c7470-116">Il comando imposta il valore di livello di Access come cool.</span><span class="sxs-lookup"><span data-stu-id="c7470-116">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="c7470-117">Esempio 4: impostare il dominio e i tag personalizzati</span><span class="sxs-lookup"><span data-stu-id="c7470-117">Example 4: Set the custom domain and tags</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="c7470-118">Il comando imposta il dominio e i tag personalizzati per un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c7470-118">The command sets the custom domain and tags for a Storage account.</span></span>

### <span data-ttu-id="c7470-119">Esempio 5: impostare la sorgente di crittografia su un Vault</span><span class="sxs-lookup"><span data-stu-id="c7470-119">Example 5: Set Encryption KeySource to Keyvault</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AssignIdentity
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"

PS C:\>$keyVault = New-AzKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get

PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

<span data-ttu-id="c7470-120">Questo comando imposta la sorgente di crittografia con un nuovo Vault creato.</span><span class="sxs-lookup"><span data-stu-id="c7470-120">This command set Encryption KeySource with a new created Keyvault.</span></span>

### <span data-ttu-id="c7470-121">Esempio 6: impostare la fonte di crittografia su "Microsoft. storage"</span><span class="sxs-lookup"><span data-stu-id="c7470-121">Example 6: Set Encryption KeySource to "Microsoft.Storage"</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -StorageEncryption
```

<span data-ttu-id="c7470-122">Questo comando imposta la sorgente di crittografia su "Microsoft. storage"</span><span class="sxs-lookup"><span data-stu-id="c7470-122">This command set Encryption KeySource to "Microsoft.Storage"</span></span>

### <span data-ttu-id="c7470-123">Esempio 7: impostare la proprietà NetworkRuleSet di un account di archiviazione con JSON</span><span class="sxs-lookup"><span data-stu-id="c7470-123">Example 7: Set NetworkRuleSet property of a Storage account with JSON</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="allow"})
```

<span data-ttu-id="c7470-124">Questo comando imposta la proprietà NetworkRuleSet di un account di archiviazione con JSON</span><span class="sxs-lookup"><span data-stu-id="c7470-124">This command sets NetworkRuleSet property of a Storage account with JSON</span></span>

### <span data-ttu-id="c7470-125">Esempio 8: ottenere la proprietà NetworkRuleSet da un account di archiviazione e impostarla su un altro account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="c7470-125">Example 8: Get NetworkRuleSet property from a Storage account, and set it to another Storage account</span></span>
```
PS C:\> $networkRuleSet = (Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount").NetworkRuleSet 
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount2" -NetworkRuleSet $networkRuleSet
```

<span data-ttu-id="c7470-126">Questo primo comando ottiene la proprietà NetworkRuleSet da un account di archiviazione e il secondo comando lo imposta su un altro account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="c7470-126">This first command gets NetworkRuleSet property from a Storage account, and the second command sets it to another Storage account</span></span> 

### <span data-ttu-id="c7470-127">Esempio 9: aggiornare un account di archiviazione con il tipo "Storage" o "BlobStorage" con l'account di archiviazione tipo "StorageV2"</span><span class="sxs-lookup"><span data-stu-id="c7470-127">Example 9: Upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account</span></span>
```
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -UpgradeToStorageV2
```

<span data-ttu-id="c7470-128">Il comando aggiorna un account di archiviazione con tipo "Storage" o "BlobStorage" per l'account di archiviazione tipo "StorageV2".</span><span class="sxs-lookup"><span data-stu-id="c7470-128">The command upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account.</span></span>

### <span data-ttu-id="c7470-129">Esempio 10: aggiornare un account di archiviazione tramite Enable Azure file di autenticazione di AAD DS.</span><span class="sxs-lookup"><span data-stu-id="c7470-129">Example 10: Update a Storage account by enable Azure Files AAD DS Authentication.</span></span>
```
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -EnableAzureActiveDirectoryDomainServicesForFile $true
```

<span data-ttu-id="c7470-130">Il comando aggiorna un account di archiviazione tramite Enable Azure file di autenticazione di AAD DS.</span><span class="sxs-lookup"><span data-stu-id="c7470-130">The command update a Storage account by enable Azure Files AAD DS Authentication.</span></span>

## <span data-ttu-id="c7470-131">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c7470-131">PARAMETERS</span></span>

### <span data-ttu-id="c7470-132">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="c7470-132">-AccessTier</span></span>
<span data-ttu-id="c7470-133">Specifica il livello di accesso dell'account di archiviazione modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7470-133">Specifies the access tier of the Storage account that this cmdlet modifies.</span></span>
<span data-ttu-id="c7470-134">I valori accettabili per questo parametro sono: caldo e freddo.</span><span class="sxs-lookup"><span data-stu-id="c7470-134">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="c7470-135">Se si modifica il livello di accesso, potrebbero essere presenti ulteriori addebiti.</span><span class="sxs-lookup"><span data-stu-id="c7470-135">If you change the access tier, it may result in additional charges.</span></span> <span data-ttu-id="c7470-136">Per altre informazioni, vedere [archiviazione BLOB di Azure: livelli di archiviazione caldi e freddi](https://go.microsoft.com/fwlink/?LinkId=786482).</span><span class="sxs-lookup"><span data-stu-id="c7470-136">For more information, see [Azure Blob Storage: Hot and cool storage tiers](https://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="c7470-137">Se l'account di archiviazione è di tipo StorageV2 o BlobStorage, è possibile specificare il parametro *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="c7470-137">If the Storage account has Kind as StorageV2 or BlobStorage, you can specify the *AccessTier* parameter.</span></span> <span data-ttu-id="c7470-138">Se l'account di archiviazione ha un tipo di spazio di archiviazione, non specificare il parametro *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="c7470-138">If the Storage account has Kind as Storage, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hot, Cool

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7470-139">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c7470-139">-AsJob</span></span>
<span data-ttu-id="c7470-140">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c7470-140">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c7470-141">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="c7470-141">-AssignIdentity</span></span>
<span data-ttu-id="c7470-142">Genera e assegna una nuova identità dell'account di archiviazione per l'account di archiviazione per l'uso con i servizi di gestione delle chiavi, ad esempio Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="c7470-142">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="c7470-143">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="c7470-143">-CustomDomainName</span></span>
<span data-ttu-id="c7470-144">Specifica il nome del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="c7470-144">Specifies the name of the custom domain.</span></span>

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

### <span data-ttu-id="c7470-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7470-145">-DefaultProfile</span></span>
<span data-ttu-id="c7470-146">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c7470-146">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7470-147">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="c7470-147">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="c7470-148">Abilitare Azure files Azure Active Directory Domain Service Authentication per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c7470-148">Enable Azure Files Azure Active Directory Domain Service Authentication for the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7470-149">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="c7470-149">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="c7470-150">Indica se l'account di archiviazione Abilita o meno solo il traffico HTTPS.</span><span class="sxs-lookup"><span data-stu-id="c7470-150">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7470-151">-Force</span><span class="sxs-lookup"><span data-stu-id="c7470-151">-Force</span></span>
<span data-ttu-id="c7470-152">Impone che la modifica venga scritta nell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c7470-152">Forces the change to be written to the Storage account.</span></span>

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

### <span data-ttu-id="c7470-153">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="c7470-153">-KeyName</span></span>
<span data-ttu-id="c7470-154">Se si usa-KeyvaultEncryption per abilitare la crittografia con il Vault delle chiavi, specificare la proprietà nome chiave con questa opzione.</span><span class="sxs-lookup"><span data-stu-id="c7470-154">If using -KeyvaultEncryption to enable encryption with Key Vault, specify the Keyname property with this option.</span></span>

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7470-155">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="c7470-155">-KeyvaultEncryption</span></span>
<span data-ttu-id="c7470-156">Indica se usare o meno Microsoft Key Vault per le chiavi di crittografia quando si usa la crittografia del servizio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c7470-156">Indicates whether or not to use Microsoft KeyVault for the encryption keys when using Storage Service Encryption.</span></span> <span data-ttu-id="c7470-157">Se il nome di codice, la versione di base e KeyVaultUri sono tutti impostati, la sorgente di origine verrà impostata su Microsoft. Vault se questo parametro è impostato o meno.</span><span class="sxs-lookup"><span data-stu-id="c7470-157">If KeyName, KeyVersion, and KeyVaultUri are all set, KeySource will be set to Microsoft.Keyvault whether this parameter is set or not.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: KeyvaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7470-158">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="c7470-158">-KeyVaultUri</span></span>
<span data-ttu-id="c7470-159">Quando usi la crittografia key Vault specificando il parametro-KeyvaultEncryption, usa questa opzione per specificare l'URI per il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="c7470-159">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7470-160">-Versione</span><span class="sxs-lookup"><span data-stu-id="c7470-160">-KeyVersion</span></span>
<span data-ttu-id="c7470-161">Quando usi la crittografia key Vault specificando il parametro-KeyvaultEncryption, usa questa opzione per specificare l'URI alla versione chiave.</span><span class="sxs-lookup"><span data-stu-id="c7470-161">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Version.</span></span>

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7470-162">-Nome</span><span class="sxs-lookup"><span data-stu-id="c7470-162">-Name</span></span>
<span data-ttu-id="c7470-163">Specifica il nome dell'account di archiviazione da modificare.</span><span class="sxs-lookup"><span data-stu-id="c7470-163">Specifies the name of the Storage account to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7470-164">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="c7470-164">-NetworkRuleSet</span></span>
<span data-ttu-id="c7470-165">NetworkRuleSet viene usato per definire un set di regole di configurazione per i firewall e le reti virtuali, nonché per impostare i valori per le proprietà di rete, ad esempio i servizi autorizzati ad aggirare le regole e come gestire le richieste che non corrispondono a nessuna delle regole definite.</span><span class="sxs-lookup"><span data-stu-id="c7470-165">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7470-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7470-166">-ResourceGroupName</span></span>
<span data-ttu-id="c7470-167">Specifica il nome del gruppo di risorse in cui modificare l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c7470-167">Specifies the name of the resource group in which to modify the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7470-168">-SkuName</span><span class="sxs-lookup"><span data-stu-id="c7470-168">-SkuName</span></span>
<span data-ttu-id="c7470-169">Specifica il nome SKU dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c7470-169">Specifies the SKU name of the Storage account.</span></span>
<span data-ttu-id="c7470-170">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c7470-170">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c7470-171">Spazio di archiviazione Standard_LRS-locale-ridondante.</span><span class="sxs-lookup"><span data-stu-id="c7470-171">Standard_LRS - Locally-redundant storage.</span></span>
- <span data-ttu-id="c7470-172">Spazio di archiviazione ridondante di Standard_ZRS-area.</span><span class="sxs-lookup"><span data-stu-id="c7470-172">Standard_ZRS - Zone-redundant storage.</span></span>
- <span data-ttu-id="c7470-173">Standard_GRS-spazio di archiviazione Geo-ridondante.</span><span class="sxs-lookup"><span data-stu-id="c7470-173">Standard_GRS - Geo-redundant storage.</span></span>
- <span data-ttu-id="c7470-174">Standard_RAGRS-Read Access Storage Geo-ridondante.</span><span class="sxs-lookup"><span data-stu-id="c7470-174">Standard_RAGRS - Read access geo-redundant storage.</span></span>
- <span data-ttu-id="c7470-175">Premium_LRS-spazio di archiviazione locale ridondante Premium.</span><span class="sxs-lookup"><span data-stu-id="c7470-175">Premium_LRS - Premium locally-redundant storage.</span></span>
<span data-ttu-id="c7470-176">Non è possibile modificare i tipi di Standard_ZRS e Premium_LRS in altri tipi di account.</span><span class="sxs-lookup"><span data-stu-id="c7470-176">You cannot change Standard_ZRS and Premium_LRS types to other account types.</span></span>
<span data-ttu-id="c7470-177">Non è possibile modificare altri tipi di account in Standard_ZRS o Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="c7470-177">You cannot change other account types to Standard_ZRS or Premium_LRS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7470-178">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="c7470-178">-StorageEncryption</span></span>
<span data-ttu-id="c7470-179">Indica se impostare o meno la crittografia dell'account di archiviazione per l'uso delle chiavi gestite da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c7470-179">Indicates whether or not to set the Storage account encryption to use Microsoft-managed keys.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: StorageEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7470-180">-Tag</span><span class="sxs-lookup"><span data-stu-id="c7470-180">-Tag</span></span>
<span data-ttu-id="c7470-181">Coppie chiave-valore nella forma di una tabella hash impostata come tag nel server.</span><span class="sxs-lookup"><span data-stu-id="c7470-181">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="c7470-182">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="c7470-182">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c7470-183">-UpgradeToStorageV2</span><span class="sxs-lookup"><span data-stu-id="c7470-183">-UpgradeToStorageV2</span></span>
<span data-ttu-id="c7470-184">Aggiornare il tipo di account di archiviazione da archiviazione o BlobStorage a StorageV2.</span><span class="sxs-lookup"><span data-stu-id="c7470-184">Upgrade Storage account Kind from  Storage or BlobStorage to StorageV2.</span></span>

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

### <span data-ttu-id="c7470-185">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="c7470-185">-UseSubDomain</span></span>
<span data-ttu-id="c7470-186">Indica se abilitare la convalida CName indiretta.</span><span class="sxs-lookup"><span data-stu-id="c7470-186">Indicates whether to enable indirect CName validation.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7470-187">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c7470-187">-Confirm</span></span>
<span data-ttu-id="c7470-188">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7470-188">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7470-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7470-189">-WhatIf</span></span>
<span data-ttu-id="c7470-190">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c7470-190">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7470-191">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c7470-191">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7470-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7470-192">CommonParameters</span></span>
<span data-ttu-id="c7470-193">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7470-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7470-194">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7470-194">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7470-195">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c7470-195">INPUTS</span></span>

### <span data-ttu-id="c7470-196">System. String</span><span class="sxs-lookup"><span data-stu-id="c7470-196">System.String</span></span>

### <span data-ttu-id="c7470-197">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c7470-197">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c7470-198">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c7470-198">OUTPUTS</span></span>

### <span data-ttu-id="c7470-199">Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c7470-199">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="c7470-200">Note</span><span class="sxs-lookup"><span data-stu-id="c7470-200">NOTES</span></span>

## <span data-ttu-id="c7470-201">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c7470-201">RELATED LINKS</span></span>

[<span data-ttu-id="c7470-202">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c7470-202">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="c7470-203">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c7470-203">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="c7470-204">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c7470-204">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)
