---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
ms.openlocfilehash: 0b5e34fe3d7fe4c680ac20da53a32e1e5bad36fa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193737"
---
# <span data-ttu-id="e1dfd-101">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e1dfd-101">Set-AzStorageAccount</span></span>

## <span data-ttu-id="e1dfd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e1dfd-102">SYNOPSIS</span></span>
<span data-ttu-id="e1dfd-103">Modifica un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-103">Modifies a Storage account.</span></span>

## <span data-ttu-id="e1dfd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e1dfd-104">SYNTAX</span></span>

### <span data-ttu-id="e1dfd-105">StorageEncryption (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e1dfd-105">StorageEncryption (Default)</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-EnableLargeFileShare]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1dfd-106">KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="e1dfd-106">KeyvaultEncryption</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> [-KeyVersion <String>]
 -KeyVaultUri <String> [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-EnableLargeFileShare]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1dfd-107">ActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="e1dfd-107">ActiveDirectoryDomainServicesForFile</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-UpgradeToStorageV2] [-EnableLargeFileShare] -EnableActiveDirectoryDomainServicesForFile <Boolean>
 [-ActiveDirectoryDomainName <String>] [-ActiveDirectoryNetBiosDomainName <String>]
 [-ActiveDirectoryForestName <String>] [-ActiveDirectoryDomainGuid <String>]
 [-ActiveDirectoryDomainSid <String>] [-ActiveDirectoryAzureStorageSid <String>]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1dfd-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e1dfd-108">DESCRIPTION</span></span>
<span data-ttu-id="e1dfd-109">Il cmdlet **set-AzStorageAccount** modifica un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-109">The **Set-AzStorageAccount** cmdlet modifies an Azure Storage account.</span></span>
<span data-ttu-id="e1dfd-110">Puoi usare questo cmdlet per modificare il tipo di account, aggiornare un dominio del cliente o impostare i contrassegni in un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-110">You can use this cmdlet to modify the account type, update a customer domain, or set tags on a Storage account.</span></span>

## <span data-ttu-id="e1dfd-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e1dfd-111">EXAMPLES</span></span>

### <span data-ttu-id="e1dfd-112">Esempio 1: impostare il tipo di account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="e1dfd-112">Example 1: Set the Storage account type</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Type "Standard_RAGRS"
```

<span data-ttu-id="e1dfd-113">Questo comando imposta il tipo di account di archiviazione su Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-113">This command sets the Storage account type to Standard_RAGRS.</span></span>

### <span data-ttu-id="e1dfd-114">Esempio 2: impostare un dominio personalizzato per un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="e1dfd-114">Example 2: Set a custom domain for a Storage account</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

<span data-ttu-id="e1dfd-115">Questo comando imposta un dominio personalizzato per un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-115">This command sets a custom domain for a Storage account.</span></span>

### <span data-ttu-id="e1dfd-116">Esempio 3: impostare il valore di livello di accesso</span><span class="sxs-lookup"><span data-stu-id="e1dfd-116">Example 3: Set the access tier value</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AccessTier Cool
```

<span data-ttu-id="e1dfd-117">Il comando imposta il valore di livello di Access come cool.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-117">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="e1dfd-118">Esempio 4: impostare il dominio e i tag personalizzati</span><span class="sxs-lookup"><span data-stu-id="e1dfd-118">Example 4: Set the custom domain and tags</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="e1dfd-119">Il comando imposta il dominio e i tag personalizzati per un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-119">The command sets the custom domain and tags for a Storage account.</span></span>

### <span data-ttu-id="e1dfd-120">Esempio 5: impostare la sorgente di crittografia su un Vault</span><span class="sxs-lookup"><span data-stu-id="e1dfd-120">Example 5: Set Encryption KeySource to Keyvault</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AssignIdentity
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"

PS C:\>$keyVault = New-AzKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get

PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

<span data-ttu-id="e1dfd-121">Questo comando imposta la sorgente di crittografia con un nuovo Vault creato.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-121">This command set Encryption KeySource with a new created Keyvault.</span></span>

### <span data-ttu-id="e1dfd-122">Esempio 6: impostare la fonte di crittografia su "Microsoft. storage"</span><span class="sxs-lookup"><span data-stu-id="e1dfd-122">Example 6: Set Encryption KeySource to "Microsoft.Storage"</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -StorageEncryption
```

<span data-ttu-id="e1dfd-123">Questo comando imposta la sorgente di crittografia su "Microsoft. storage"</span><span class="sxs-lookup"><span data-stu-id="e1dfd-123">This command set Encryption KeySource to "Microsoft.Storage"</span></span>

### <span data-ttu-id="e1dfd-124">Esempio 7: impostare la proprietà NetworkRuleSet di un account di archiviazione con JSON</span><span class="sxs-lookup"><span data-stu-id="e1dfd-124">Example 7: Set NetworkRuleSet property of a Storage account with JSON</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="allow"})
```

<span data-ttu-id="e1dfd-125">Questo comando imposta la proprietà NetworkRuleSet di un account di archiviazione con JSON</span><span class="sxs-lookup"><span data-stu-id="e1dfd-125">This command sets NetworkRuleSet property of a Storage account with JSON</span></span>

### <span data-ttu-id="e1dfd-126">Esempio 8: ottenere la proprietà NetworkRuleSet da un account di archiviazione e impostarla su un altro account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="e1dfd-126">Example 8: Get NetworkRuleSet property from a Storage account, and set it to another Storage account</span></span>
```
PS C:\> $networkRuleSet = (Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount").NetworkRuleSet 
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount2" -NetworkRuleSet $networkRuleSet
```

<span data-ttu-id="e1dfd-127">Questo primo comando ottiene la proprietà NetworkRuleSet da un account di archiviazione e il secondo comando lo imposta su un altro account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="e1dfd-127">This first command gets NetworkRuleSet property from a Storage account, and the second command sets it to another Storage account</span></span> 

### <span data-ttu-id="e1dfd-128">Esempio 9: aggiornare un account di archiviazione con il tipo "Storage" o "BlobStorage" con l'account di archiviazione tipo "StorageV2"</span><span class="sxs-lookup"><span data-stu-id="e1dfd-128">Example 9: Upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account</span></span>
```
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -UpgradeToStorageV2
```

<span data-ttu-id="e1dfd-129">Il comando aggiorna un account di archiviazione con tipo "Storage" o "BlobStorage" per l'account di archiviazione tipo "StorageV2".</span><span class="sxs-lookup"><span data-stu-id="e1dfd-129">The command upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account.</span></span>

### <span data-ttu-id="e1dfd-130">Esempio 10: aggiornare un account di archiviazione tramite Enable Azure file di autenticazione di AAD DS.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-130">Example 10: Update a Storage account by enable Azure Files AAD DS Authentication.</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -EnableAzureActiveDirectoryDomainServicesForFile $true PS

PS C:\> $account.AzureFilesIdentityBasedAuth.DirectoryServiceOptions
AADDS
```

<span data-ttu-id="e1dfd-131">Il comando aggiorna un account di archiviazione tramite Enable Azure file di autenticazione di AAD DS.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-131">The command update a Storage account by enable Azure Files AAD DS Authentication.</span></span>

### <span data-ttu-id="e1dfd-132">Esempio 11: aggiornare un account di archiviazione abilitando i file autenticazione del servizio di dominio Active Directory e quindi visualizzare l'impostazione di autenticazione basata su identità file</span><span class="sxs-lookup"><span data-stu-id="e1dfd-132">Example 11: Update a Storage account by enable Files Active Directory Domain Service Authentication, and then show the File Identity Based authentication setting</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -EnableActiveDirectoryDomainServicesForFile $true `
        -ActiveDirectoryDomainName "mydomain.com" `
        -ActiveDirectoryNetBiosDomainName "mydomain.com" `
        -ActiveDirectoryForestName "mydomain.com" `
        -ActiveDirectoryDomainGuid "12345678-1234-1234-1234-123456789012" `
        -ActiveDirectoryDomainSid "S-1-5-21-1234567890-1234567890-1234567890" `
        -ActiveDirectoryAzureStorageSid "S-1-5-21-1234567890-1234567890-1234567890-1234"
        
PS C:\> $account.AzureFilesIdentityBasedAuth.DirectoryServiceOptions
AD

PS C:\> $account.AzureFilesIdentityBasedAuth.ActiveDirectoryProperties

DomainName        : mydomain.com
NetBiosDomainName : mydomain.com
ForestName        : mydomain.com
DomainGuid        : 12345678-1234-1234-1234-123456789012
DomainSid         : S-1-5-21-1234567890-1234567890-1234567890
AzureStorageSid   : S-1-5-21-1234567890-1234567890-1234567890-1234
```

<span data-ttu-id="e1dfd-133">Il comando aggiorna un account di archiviazione abilitando l'autenticazione dei servizi di dominio Active Directory di Azure e quindi Mostra l'impostazione di autenticazione basata su identità file</span><span class="sxs-lookup"><span data-stu-id="e1dfd-133">The command updates a Storage account by enable Azure Files Active Directory Domain Service Authentication, and then shows the File Identity Based authentication setting</span></span>

### <span data-ttu-id="e1dfd-134">Esempio 12: impostare MinimumTlsVersion e AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="e1dfd-134">Example 12: Set MinimumTlsVersion and AllowBlobPublicAccess</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False
```

<span data-ttu-id="e1dfd-135">Il comando imposta MinimumTlsVersion e AllowBlobPublicAccess e quindi Mostra le due proprietà dell'account</span><span class="sxs-lookup"><span data-stu-id="e1dfd-135">The command sets MinimumTlsVersion  and AllowBlobPublicAccess, and then show the the 2 properties of the account</span></span> 

## <span data-ttu-id="e1dfd-136">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e1dfd-136">PARAMETERS</span></span>

### <span data-ttu-id="e1dfd-137">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="e1dfd-137">-AccessTier</span></span>
<span data-ttu-id="e1dfd-138">Specifica il livello di accesso dell'account di archiviazione modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-138">Specifies the access tier of the Storage account that this cmdlet modifies.</span></span>
<span data-ttu-id="e1dfd-139">I valori accettabili per questo parametro sono: caldo e freddo.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-139">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="e1dfd-140">Se si modifica il livello di accesso, potrebbero essere presenti ulteriori addebiti.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-140">If you change the access tier, it may result in additional charges.</span></span> <span data-ttu-id="e1dfd-141">Per altre informazioni, vedere [archiviazione BLOB di Azure: livelli di archiviazione caldi e freddi](http://go.microsoft.com/fwlink/?LinkId=786482).</span><span class="sxs-lookup"><span data-stu-id="e1dfd-141">For more information, see [Azure Blob Storage: Hot and cool storage tiers](http://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="e1dfd-142">Se l'account di archiviazione è di tipo StorageV2 o BlobStorage, è possibile specificare il parametro *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="e1dfd-142">If the Storage account has Kind as StorageV2 or BlobStorage, you can specify the *AccessTier* parameter.</span></span> <span data-ttu-id="e1dfd-143">Se l'account di archiviazione ha un tipo di spazio di archiviazione, non specificare il parametro *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="e1dfd-143">If the Storage account has Kind as Storage, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="e1dfd-144">-ActiveDirectoryAzureStorageSid</span><span class="sxs-lookup"><span data-stu-id="e1dfd-144">-ActiveDirectoryAzureStorageSid</span></span>
<span data-ttu-id="e1dfd-145">Specifica l'identificatore di sicurezza (SID) per lo spazio di archiviazione Azure.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-145">Specifies the security identifier (SID) for Azure Storage.</span></span> <span data-ttu-id="e1dfd-146">Questo parametro deve essere impostato quando-EnableActiveDirectoryDomainServicesForFile è impostato su true.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-146">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1dfd-147">-ActiveDirectoryDomainGuid</span><span class="sxs-lookup"><span data-stu-id="e1dfd-147">-ActiveDirectoryDomainGuid</span></span>
<span data-ttu-id="e1dfd-148">Specifica il GUID del dominio.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-148">Specifies the domain GUID.</span></span> <span data-ttu-id="e1dfd-149">Questo parametro deve essere impostato quando-EnableActiveDirectoryDomainServicesForFile è impostato su true.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-149">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1dfd-150">-ActiveDirectoryDomainName</span><span class="sxs-lookup"><span data-stu-id="e1dfd-150">-ActiveDirectoryDomainName</span></span>
<span data-ttu-id="e1dfd-151">Specifica il dominio primario per cui è autorevole il server DNS AD.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-151">Specifies the primary domain that the AD DNS server is authoritative for.</span></span> <span data-ttu-id="e1dfd-152">Questo parametro deve essere impostato quando-EnableActiveDirectoryDomainServicesForFile è impostato su true.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-152">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1dfd-153">-ActiveDirectoryDomainSid</span><span class="sxs-lookup"><span data-stu-id="e1dfd-153">-ActiveDirectoryDomainSid</span></span>
<span data-ttu-id="e1dfd-154">Specifica l'identificatore di sicurezza (SID).</span><span class="sxs-lookup"><span data-stu-id="e1dfd-154">Specifies the security identifier (SID).</span></span> <span data-ttu-id="e1dfd-155">Questo parametro deve essere impostato quando-EnableActiveDirectoryDomainServicesForFile è impostato su true.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-155">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1dfd-156">-ActiveDirectoryForestName</span><span class="sxs-lookup"><span data-stu-id="e1dfd-156">-ActiveDirectoryForestName</span></span>
<span data-ttu-id="e1dfd-157">Specifica la foresta di Active Directory da ottenere.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-157">Specifies the Active Directory forest to get.</span></span> <span data-ttu-id="e1dfd-158">Questo parametro deve essere impostato quando-EnableActiveDirectoryDomainServicesForFile è impostato su true.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-158">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1dfd-159">-ActiveDirectoryNetBiosDomainName</span><span class="sxs-lookup"><span data-stu-id="e1dfd-159">-ActiveDirectoryNetBiosDomainName</span></span>
<span data-ttu-id="e1dfd-160">Specifica il nome di dominio NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-160">Specifies the NetBIOS domain name.</span></span> <span data-ttu-id="e1dfd-161">Questo parametro deve essere impostato quando-EnableActiveDirectoryDomainServicesForFile è impostato su true.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-161">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1dfd-162">-AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="e1dfd-162">-AllowBlobPublicAccess</span></span>
<span data-ttu-id="e1dfd-163">Consentire o impedire l'accesso pubblico a tutti i BLOB o i contenitori nell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-163">Allow or disallow public access to all blobs or containers in the storage account.</span></span>

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

### <span data-ttu-id="e1dfd-164">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e1dfd-164">-AsJob</span></span>
<span data-ttu-id="e1dfd-165">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e1dfd-165">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e1dfd-166">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="e1dfd-166">-AssignIdentity</span></span>
<span data-ttu-id="e1dfd-167">Genera e assegna una nuova identità dell'account di archiviazione per l'account di archiviazione per l'uso con i servizi di gestione delle chiavi, ad esempio Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-167">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="e1dfd-168">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="e1dfd-168">-CustomDomainName</span></span>
<span data-ttu-id="e1dfd-169">Specifica il nome del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-169">Specifies the name of the custom domain.</span></span>

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

### <span data-ttu-id="e1dfd-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1dfd-170">-DefaultProfile</span></span>
<span data-ttu-id="e1dfd-171">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-171">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1dfd-172">-EnableActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="e1dfd-172">-EnableActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="e1dfd-173">Abilitare l'autenticazione dei servizi di dominio Active Directory di Azure per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-173">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1dfd-174">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="e1dfd-174">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="e1dfd-175">Abilitare l'autenticazione dei servizi di dominio Active Directory di Azure per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-175">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: StorageEncryption, KeyvaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1dfd-176">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="e1dfd-176">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="e1dfd-177">Indica se l'account di archiviazione Abilita o meno solo il traffico HTTPS.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-177">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="e1dfd-178">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="e1dfd-178">-EnableLargeFileShare</span></span>
<span data-ttu-id="e1dfd-179">Indica se l'account di archiviazione può supportare condivisioni di file di grandi dimensioni con più di 5 capacità TiB.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-179">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="e1dfd-180">Quando l'account è abilitato, la caratteristica non può essere disabilitata.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-180">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="e1dfd-181">Attualmente supportato solo per i tipi di replica LRS e ZRS, quindi le conversioni degli account con gli account Geo-ridondanti non sarebbero possibili.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-181">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="e1dfd-182">Altre informazioni in https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="e1dfd-182">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="e1dfd-183">-Force</span><span class="sxs-lookup"><span data-stu-id="e1dfd-183">-Force</span></span>
<span data-ttu-id="e1dfd-184">Impone che la modifica venga scritta nell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-184">Forces the change to be written to the Storage account.</span></span>

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

### <span data-ttu-id="e1dfd-185">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="e1dfd-185">-KeyName</span></span>
<span data-ttu-id="e1dfd-186">Se si usa-KeyvaultEncryption per abilitare la crittografia con il Vault delle chiavi, specificare la proprietà nome chiave con questa opzione.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-186">If using -KeyvaultEncryption to enable encryption with Key Vault, specify the Keyname property with this option.</span></span>

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

### <span data-ttu-id="e1dfd-187">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="e1dfd-187">-KeyvaultEncryption</span></span>
<span data-ttu-id="e1dfd-188">Indica se usare o meno Microsoft Key Vault per le chiavi di crittografia quando si usa la crittografia del servizio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-188">Indicates whether or not to use Microsoft KeyVault for the encryption keys when using Storage Service Encryption.</span></span> <span data-ttu-id="e1dfd-189">Se il nome di codice, la versione di base e KeyVaultUri sono tutti impostati, la sorgente di origine verrà impostata su Microsoft. Vault se questo parametro è impostato o meno.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-189">If KeyName, KeyVersion, and KeyVaultUri are all set, KeySource will be set to Microsoft.Keyvault whether this parameter is set or not.</span></span> 

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

### <span data-ttu-id="e1dfd-190">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="e1dfd-190">-KeyVaultUri</span></span>
<span data-ttu-id="e1dfd-191">Quando usi la crittografia key Vault specificando il parametro-KeyvaultEncryption, usa questa opzione per specificare l'URI per il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-191">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Vault.</span></span>

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

### <span data-ttu-id="e1dfd-192">-Versione</span><span class="sxs-lookup"><span data-stu-id="e1dfd-192">-KeyVersion</span></span>
<span data-ttu-id="e1dfd-193">Quando usi la crittografia key Vault specificando il parametro-KeyvaultEncryption, usa questa opzione per specificare l'URI alla versione chiave.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-193">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Version.</span></span>

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1dfd-194">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="e1dfd-194">-MinimumTlsVersion</span></span>
<span data-ttu-id="e1dfd-195">La versione minima di TLS consentita per le richieste di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-195">The minimum TLS version to be permitted on requests to storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TLS1_0, TLS1_1, TLS1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1dfd-196">-Nome</span><span class="sxs-lookup"><span data-stu-id="e1dfd-196">-Name</span></span>
<span data-ttu-id="e1dfd-197">Specifica il nome dell'account di archiviazione da modificare.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-197">Specifies the name of the Storage account to modify.</span></span>

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

### <span data-ttu-id="e1dfd-198">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="e1dfd-198">-NetworkRuleSet</span></span>
<span data-ttu-id="e1dfd-199">NetworkRuleSet viene usato per definire un set di regole di configurazione per i firewall e le reti virtuali, nonché per impostare i valori per le proprietà di rete, ad esempio i servizi autorizzati ad aggirare le regole e come gestire le richieste che non corrispondono a nessuna delle regole definite.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-199">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="e1dfd-200">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1dfd-200">-ResourceGroupName</span></span>
<span data-ttu-id="e1dfd-201">Specifica il nome del gruppo di risorse in cui modificare l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-201">Specifies the name of the resource group in which to modify the Storage account.</span></span>

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

### <span data-ttu-id="e1dfd-202">-SkuName</span><span class="sxs-lookup"><span data-stu-id="e1dfd-202">-SkuName</span></span>
<span data-ttu-id="e1dfd-203">Specifica il nome SKU dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-203">Specifies the SKU name of the Storage account.</span></span>
<span data-ttu-id="e1dfd-204">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="e1dfd-204">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e1dfd-205">Spazio di archiviazione Standard_LRS-locale-ridondante.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-205">Standard_LRS - Locally-redundant storage.</span></span>
- <span data-ttu-id="e1dfd-206">Spazio di archiviazione ridondante di Standard_ZRS-area.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-206">Standard_ZRS - Zone-redundant storage.</span></span>
- <span data-ttu-id="e1dfd-207">Standard_GRS-spazio di archiviazione Geo-ridondante.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-207">Standard_GRS - Geo-redundant storage.</span></span>
- <span data-ttu-id="e1dfd-208">Standard_RAGRS-Read Access Storage Geo-ridondante.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-208">Standard_RAGRS - Read access geo-redundant storage.</span></span>
- <span data-ttu-id="e1dfd-209">Premium_LRS-spazio di archiviazione locale ridondante Premium.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-209">Premium_LRS - Premium locally-redundant storage.</span></span>
- <span data-ttu-id="e1dfd-210">Standard_GZRS-area geo-ridondante-spazio di archiviazione ridondante.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-210">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="e1dfd-211">Standard_RAGZRS-Read Access area geo-ridondante-archiviazione ridondante.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-211">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>
<span data-ttu-id="e1dfd-212">Non è possibile modificare i tipi di Standard_ZRS e Premium_LRS in altri tipi di account.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-212">You cannot change Standard_ZRS and Premium_LRS types to other account types.</span></span>
<span data-ttu-id="e1dfd-213">Non è possibile modificare altri tipi di account in Standard_ZRS o Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-213">You cannot change other account types to Standard_ZRS or Premium_LRS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS, Standard_GZRS, Standard_RAGZRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1dfd-214">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="e1dfd-214">-StorageEncryption</span></span>
<span data-ttu-id="e1dfd-215">Indica se impostare o meno la crittografia dell'account di archiviazione per l'uso delle chiavi gestite da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-215">Indicates whether or not to set the Storage account encryption to use Microsoft-managed keys.</span></span>

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

### <span data-ttu-id="e1dfd-216">-Tag</span><span class="sxs-lookup"><span data-stu-id="e1dfd-216">-Tag</span></span>
<span data-ttu-id="e1dfd-217">Coppie chiave-valore nella forma di una tabella hash impostata come tag nel server.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-217">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="e1dfd-218">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="e1dfd-218">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e1dfd-219">-UpgradeToStorageV2</span><span class="sxs-lookup"><span data-stu-id="e1dfd-219">-UpgradeToStorageV2</span></span>
<span data-ttu-id="e1dfd-220">Aggiornare il tipo di account di archiviazione da archiviazione o BlobStorage a StorageV2.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-220">Upgrade Storage account Kind from  Storage or BlobStorage to StorageV2.</span></span>

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

### <span data-ttu-id="e1dfd-221">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="e1dfd-221">-UseSubDomain</span></span>
<span data-ttu-id="e1dfd-222">Indica se abilitare la convalida CName indiretta.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-222">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="e1dfd-223">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e1dfd-223">-Confirm</span></span>
<span data-ttu-id="e1dfd-224">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-224">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1dfd-225">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1dfd-225">-WhatIf</span></span>
<span data-ttu-id="e1dfd-226">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-226">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1dfd-227">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-227">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1dfd-228">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1dfd-228">CommonParameters</span></span>
<span data-ttu-id="e1dfd-229">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1dfd-229">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1dfd-230">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1dfd-230">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1dfd-231">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e1dfd-231">INPUTS</span></span>

### <span data-ttu-id="e1dfd-232">System. String</span><span class="sxs-lookup"><span data-stu-id="e1dfd-232">System.String</span></span>

### <span data-ttu-id="e1dfd-233">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e1dfd-233">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e1dfd-234">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e1dfd-234">OUTPUTS</span></span>

### <span data-ttu-id="e1dfd-235">Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e1dfd-235">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="e1dfd-236">Note</span><span class="sxs-lookup"><span data-stu-id="e1dfd-236">NOTES</span></span>

## <span data-ttu-id="e1dfd-237">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e1dfd-237">RELATED LINKS</span></span>

[<span data-ttu-id="e1dfd-238">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e1dfd-238">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="e1dfd-239">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e1dfd-239">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="e1dfd-240">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e1dfd-240">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)
