---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/set-azurermstorageaccount
schema: 2.0.0
ms.openlocfilehash: a6f16c4ef9012f7aaf5216e0cfb24edf65ce9f4d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866174"
---
# <span data-ttu-id="c3928-101">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c3928-101">Set-AzureRmStorageAccount</span></span>

## <span data-ttu-id="c3928-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c3928-102">SYNOPSIS</span></span>
<span data-ttu-id="c3928-103">Modifica un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c3928-103">Modifies a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3928-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c3928-104">SYNTAX</span></span>

### <span data-ttu-id="c3928-105">StorageEncryption (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c3928-105">StorageEncryption (Default)</span></span>
```
Set-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3928-106">KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="c3928-106">KeyvaultEncryption</span></span>
```
Set-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3928-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c3928-107">DESCRIPTION</span></span>
<span data-ttu-id="c3928-108">Il cmdlet **set-AzureRmStorageAccount** modifica un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="c3928-108">The **Set-AzureRmStorageAccount** cmdlet modifies an Azure Storage account.</span></span>
<span data-ttu-id="c3928-109">Puoi usare questo cmdlet per modificare il tipo di account, aggiornare un dominio del cliente o impostare i contrassegni in un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c3928-109">You can use this cmdlet to modify the account type, update a customer domain, or set tags on a Storage account.</span></span>

## <span data-ttu-id="c3928-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c3928-110">EXAMPLES</span></span>

### <span data-ttu-id="c3928-111">Esempio 1: impostare il tipo di account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="c3928-111">Example 1: Set the Storage account type</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Type "Standard_RAGRS"
```

<span data-ttu-id="c3928-112">Questo comando imposta il tipo di account di archiviazione su Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="c3928-112">This command sets the Storage account type to Standard_RAGRS.</span></span>

### <span data-ttu-id="c3928-113">Esempio 2: impostare un dominio personalizzato per un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="c3928-113">Example 2: Set a custom domain for a Storage account</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

<span data-ttu-id="c3928-114">Questo comando imposta un dominio personalizzato per un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c3928-114">This command sets a custom domain for a Storage account.</span></span>

### <span data-ttu-id="c3928-115">Esempio 3: impostare il valore di livello di accesso</span><span class="sxs-lookup"><span data-stu-id="c3928-115">Example 3: Set the access tier value</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AccessTier Cool
```

<span data-ttu-id="c3928-116">Il comando imposta il valore di livello di Access come cool.</span><span class="sxs-lookup"><span data-stu-id="c3928-116">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="c3928-117">Esempio 4: impostare il dominio e i tag personalizzati</span><span class="sxs-lookup"><span data-stu-id="c3928-117">Example 4: Set the custom domain and tags</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="c3928-118">Il comando imposta il dominio e i tag personalizzati per un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c3928-118">The command sets the custom domain and tags for a Storage account.</span></span>

### <span data-ttu-id="c3928-119">Esempio 5: impostare la sorgente di crittografia su un Vault</span><span class="sxs-lookup"><span data-stu-id="c3928-119">Example 5: Set Encryption KeySource to Keyvault</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AssignIdentity
PS C:\>$account = Get-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"

PS C:\>$keyVault = New-AzureRmKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzureKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get

PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

<span data-ttu-id="c3928-120">Questo comando imposta la sorgente di crittografia con un nuovo Vault creato.</span><span class="sxs-lookup"><span data-stu-id="c3928-120">This command set Encryption KeySource with a new created Keyvault.</span></span>

### <span data-ttu-id="c3928-121">Esempio 6: impostare la fonte di crittografia su "Microsoft. storage"</span><span class="sxs-lookup"><span data-stu-id="c3928-121">Example 6: Set Encryption KeySource to "Microsoft.Storage"</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -StorageEncryption
```

<span data-ttu-id="c3928-122">Questo comando imposta la sorgente di crittografia su "Microsoft. storage"</span><span class="sxs-lookup"><span data-stu-id="c3928-122">This command set Encryption KeySource to "Microsoft.Storage"</span></span>

### <span data-ttu-id="c3928-123">Esempio 7: impostare la proprietà NetworkRuleSet di un account di archiviazione con JSON</span><span class="sxs-lookup"><span data-stu-id="c3928-123">Example 7: Set NetworkRuleSet property of a Storage account with JSON</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="allow"})
```

<span data-ttu-id="c3928-124">Questo comando imposta la proprietà NetworkRuleSet di un account di archiviazione con JSON</span><span class="sxs-lookup"><span data-stu-id="c3928-124">This command sets NetworkRuleSet property of a Storage account with JSON</span></span>

### <span data-ttu-id="c3928-125">Esempio 8: ottenere la proprietà NetworkRuleSet da un account di archiviazione e impostarla su un altro account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="c3928-125">Example 8: Get NetworkRuleSet property from a Storage account, and set it to another Storage account</span></span>
```
PS C:\> $networkRuleSet = (Get-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount").NetworkRuleSet 
PS C:\> Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount2" -NetworkRuleSet $networkRuleSet
```

<span data-ttu-id="c3928-126">Questo primo comando ottiene la proprietà NetworkRuleSet da un account di archiviazione e il secondo comando lo imposta su un altro account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="c3928-126">This first command gets NetworkRuleSet property from a Storage account, and the second command sets it to another Storage account</span></span> 

### <span data-ttu-id="c3928-127">Esempio 9: aggiornare un account di archiviazione con il tipo "Storage" o "BlobStorage" con l'account di archiviazione tipo "StorageV2"</span><span class="sxs-lookup"><span data-stu-id="c3928-127">Example 9: Upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account</span></span>
```
PS C:\> Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -UpgradeToStorageV2
```

<span data-ttu-id="c3928-128">Il comando aggiorna un account di archiviazione con tipo "Storage" o "BlobStorage" per l'account di archiviazione tipo "StorageV2".</span><span class="sxs-lookup"><span data-stu-id="c3928-128">The command upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account.</span></span>

## <span data-ttu-id="c3928-129">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c3928-129">PARAMETERS</span></span>

### <span data-ttu-id="c3928-130">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="c3928-130">-AccessTier</span></span>
<span data-ttu-id="c3928-131">Specifica il livello di accesso dell'account di archiviazione modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3928-131">Specifies the access tier of the Storage account that this cmdlet modifies.</span></span>
<span data-ttu-id="c3928-132">I valori accettabili per questo parametro sono: caldo e freddo.</span><span class="sxs-lookup"><span data-stu-id="c3928-132">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="c3928-133">Se si modifica il livello di accesso, potrebbero essere presenti ulteriori addebiti.</span><span class="sxs-lookup"><span data-stu-id="c3928-133">If you change the access tier, it may result in additional charges.</span></span> <span data-ttu-id="c3928-134">Per altre informazioni, vedere [archiviazione BLOB di Azure: livelli di archiviazione caldi e freddi](https://go.microsoft.com/fwlink/?LinkId=786482).</span><span class="sxs-lookup"><span data-stu-id="c3928-134">For more information, see [Azure Blob Storage: Hot and cool storage tiers](https://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="c3928-135">Se l'account di archiviazione è di tipo StorageV2 o BlobStorage, è possibile specificare il parametro *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="c3928-135">If the Storage account has Kind as StorageV2 or BlobStorage, you can specify the *AccessTier* parameter.</span></span> <span data-ttu-id="c3928-136">Se l'account di archiviazione ha un tipo di spazio di archiviazione, non specificare il parametro *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="c3928-136">If the Storage account has Kind as Storage, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="c3928-137">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c3928-137">-AsJob</span></span>
<span data-ttu-id="c3928-138">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c3928-138">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c3928-139">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="c3928-139">-AssignIdentity</span></span>
<span data-ttu-id="c3928-140">Genera e assegna una nuova identità dell'account di archiviazione per l'account di archiviazione per l'uso con i servizi di gestione delle chiavi, ad esempio Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="c3928-140">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="c3928-141">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="c3928-141">-CustomDomainName</span></span>
<span data-ttu-id="c3928-142">Specifica il nome del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="c3928-142">Specifies the name of the custom domain.</span></span>

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

### <span data-ttu-id="c3928-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3928-143">-DefaultProfile</span></span>
<span data-ttu-id="c3928-144">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c3928-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3928-145">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="c3928-145">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="c3928-146">Indica se l'account di archiviazione Abilita o meno solo il traffico HTTPS.</span><span class="sxs-lookup"><span data-stu-id="c3928-146">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3928-147">-Force</span><span class="sxs-lookup"><span data-stu-id="c3928-147">-Force</span></span>
<span data-ttu-id="c3928-148">Impone che la modifica venga scritta nell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c3928-148">Forces the change to be written to the Storage account.</span></span>

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

### <span data-ttu-id="c3928-149">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="c3928-149">-KeyName</span></span>
<span data-ttu-id="c3928-150">Se si usa-KeyvaultEncryption per abilitare la crittografia con il Vault delle chiavi, specificare la proprietà nome chiave con questa opzione.</span><span class="sxs-lookup"><span data-stu-id="c3928-150">If using -KeyvaultEncryption to enable encryption with Key Vault, specify the Keyname property with this option.</span></span>

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

### <span data-ttu-id="c3928-151">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="c3928-151">-KeyvaultEncryption</span></span>
<span data-ttu-id="c3928-152">Indica se usare o meno Microsoft Key Vault per le chiavi di crittografia quando si usa la crittografia del servizio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c3928-152">Indicates whether or not to use Microsoft KeyVault for the encryption keys when using Storage Service Encryption.</span></span> <span data-ttu-id="c3928-153">Se il nome di codice, la versione di base e KeyVaultUri sono tutti impostati, la sorgente di origine verrà impostata su Microsoft. Vault se questo parametro è impostato o meno.</span><span class="sxs-lookup"><span data-stu-id="c3928-153">If KeyName, KeyVersion, and KeyVaultUri are all set, KeySource will be set to Microsoft.Keyvault whether this parameter is set or not.</span></span> 

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

### <span data-ttu-id="c3928-154">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="c3928-154">-KeyVaultUri</span></span>
<span data-ttu-id="c3928-155">Quando usi la crittografia key Vault specificando il parametro-KeyvaultEncryption, usa questa opzione per specificare l'URI per il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="c3928-155">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Vault.</span></span>

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

### <span data-ttu-id="c3928-156">-Versione</span><span class="sxs-lookup"><span data-stu-id="c3928-156">-KeyVersion</span></span>
<span data-ttu-id="c3928-157">Quando usi la crittografia key Vault specificando il parametro-KeyvaultEncryption, usa questa opzione per specificare l'URI alla versione chiave.</span><span class="sxs-lookup"><span data-stu-id="c3928-157">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Version.</span></span>

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

### <span data-ttu-id="c3928-158">-Nome</span><span class="sxs-lookup"><span data-stu-id="c3928-158">-Name</span></span>
<span data-ttu-id="c3928-159">Specifica il nome dell'account di archiviazione da modificare.</span><span class="sxs-lookup"><span data-stu-id="c3928-159">Specifies the name of the Storage account to modify.</span></span>

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

### <span data-ttu-id="c3928-160">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="c3928-160">-NetworkRuleSet</span></span>
<span data-ttu-id="c3928-161">NetworkRuleSet viene usato per definire un set di regole di configurazione per i firewall e le reti virtuali, nonché per impostare i valori per le proprietà di rete, ad esempio i servizi autorizzati ad aggirare le regole e come gestire le richieste che non corrispondono a nessuna delle regole definite.</span><span class="sxs-lookup"><span data-stu-id="c3928-161">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="c3928-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3928-162">-ResourceGroupName</span></span>
<span data-ttu-id="c3928-163">Specifica il nome del gruppo di risorse in cui modificare l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c3928-163">Specifies the name of the resource group in which to modify the Storage account.</span></span>

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

### <span data-ttu-id="c3928-164">-SkuName</span><span class="sxs-lookup"><span data-stu-id="c3928-164">-SkuName</span></span>
<span data-ttu-id="c3928-165">Specifica il nome SKU dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c3928-165">Specifies the SKU name of the Storage account.</span></span>
<span data-ttu-id="c3928-166">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c3928-166">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c3928-167">Spazio di archiviazione Standard_LRS-locale-ridondante.</span><span class="sxs-lookup"><span data-stu-id="c3928-167">Standard_LRS - Locally-redundant storage.</span></span>
- <span data-ttu-id="c3928-168">Spazio di archiviazione ridondante di Standard_ZRS-area.</span><span class="sxs-lookup"><span data-stu-id="c3928-168">Standard_ZRS - Zone-redundant storage.</span></span>
- <span data-ttu-id="c3928-169">Standard_GRS-spazio di archiviazione Geo-ridondante.</span><span class="sxs-lookup"><span data-stu-id="c3928-169">Standard_GRS - Geo-redundant storage.</span></span>
- <span data-ttu-id="c3928-170">Standard_RAGRS-Read Access Storage Geo-ridondante.</span><span class="sxs-lookup"><span data-stu-id="c3928-170">Standard_RAGRS - Read access geo-redundant storage.</span></span>
- <span data-ttu-id="c3928-171">Premium_LRS-spazio di archiviazione locale ridondante Premium.</span><span class="sxs-lookup"><span data-stu-id="c3928-171">Premium_LRS - Premium locally-redundant storage.</span></span>
<span data-ttu-id="c3928-172">Non è possibile modificare i tipi di Standard_ZRS e Premium_LRS in altri tipi di account.</span><span class="sxs-lookup"><span data-stu-id="c3928-172">You cannot change Standard_ZRS and Premium_LRS types to other account types.</span></span>
<span data-ttu-id="c3928-173">Non è possibile modificare altri tipi di account in Standard_ZRS o Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="c3928-173">You cannot change other account types to Standard_ZRS or Premium_LRS.</span></span>

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

### <span data-ttu-id="c3928-174">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="c3928-174">-StorageEncryption</span></span>
<span data-ttu-id="c3928-175">Indica se impostare o meno la crittografia dell'account di archiviazione per l'uso delle chiavi gestite da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c3928-175">Indicates whether or not to set the Storage account encryption to use Microsoft-managed keys.</span></span>

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

### <span data-ttu-id="c3928-176">-Tag</span><span class="sxs-lookup"><span data-stu-id="c3928-176">-Tag</span></span>
<span data-ttu-id="c3928-177">Coppie chiave-valore nella forma di una tabella hash impostata come tag nel server.</span><span class="sxs-lookup"><span data-stu-id="c3928-177">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="c3928-178">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="c3928-178">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c3928-179">-UpgradeToStorageV2</span><span class="sxs-lookup"><span data-stu-id="c3928-179">-UpgradeToStorageV2</span></span>
<span data-ttu-id="c3928-180">Aggiornare il tipo di account di archiviazione da archiviazione o BlobStorage a StorageV2.</span><span class="sxs-lookup"><span data-stu-id="c3928-180">Upgrade Storage account Kind from  Storage or BlobStorage to StorageV2.</span></span>

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

### <span data-ttu-id="c3928-181">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="c3928-181">-UseSubDomain</span></span>
<span data-ttu-id="c3928-182">Indica se abilitare la convalida CName indiretta.</span><span class="sxs-lookup"><span data-stu-id="c3928-182">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="c3928-183">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c3928-183">-Confirm</span></span>
<span data-ttu-id="c3928-184">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3928-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3928-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3928-185">-WhatIf</span></span>
<span data-ttu-id="c3928-186">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c3928-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3928-187">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c3928-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3928-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3928-188">CommonParameters</span></span>
<span data-ttu-id="c3928-189">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3928-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3928-190">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3928-190">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3928-191">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c3928-191">INPUTS</span></span>

### <span data-ttu-id="c3928-192">System. String</span><span class="sxs-lookup"><span data-stu-id="c3928-192">System.String</span></span>

### <span data-ttu-id="c3928-193">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c3928-193">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c3928-194">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c3928-194">System.Boolean</span></span>

## <span data-ttu-id="c3928-195">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c3928-195">OUTPUTS</span></span>

### <span data-ttu-id="c3928-196">Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c3928-196">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="c3928-197">Note</span><span class="sxs-lookup"><span data-stu-id="c3928-197">NOTES</span></span>

## <span data-ttu-id="c3928-198">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c3928-198">RELATED LINKS</span></span>

[<span data-ttu-id="c3928-199">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c3928-199">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="c3928-200">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c3928-200">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="c3928-201">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c3928-201">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)
