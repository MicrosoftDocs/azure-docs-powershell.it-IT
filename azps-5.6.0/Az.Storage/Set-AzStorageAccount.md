---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
ms.openlocfilehash: 05166cbfad437858b85e189d75df9b8216db4fae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977630"
---
# <span data-ttu-id="eaf62-101">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="eaf62-101">Set-AzStorageAccount</span></span>

## <span data-ttu-id="eaf62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eaf62-102">SYNOPSIS</span></span>
<span data-ttu-id="eaf62-103">Modifica un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="eaf62-103">Modifies a Storage account.</span></span>

## <span data-ttu-id="eaf62-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eaf62-104">SYNTAX</span></span>

### <span data-ttu-id="eaf62-105">StorageEncryption (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="eaf62-105">StorageEncryption (Default)</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-EnableLargeFileShare]
 [-PublishMicrosoftEndpoint <Boolean>] [-PublishInternetEndpoint <Boolean>] [-AllowBlobPublicAccess <Boolean>]
 [-MinimumTlsVersion <String>] [-AllowSharedKeyAccess <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eaf62-106">KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="eaf62-106">KeyvaultEncryption</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> [-KeyVersion <String>]
 -KeyVaultUri <String> [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-EnableLargeFileShare]
 [-PublishMicrosoftEndpoint <Boolean>] [-PublishInternetEndpoint <Boolean>] [-AllowBlobPublicAccess <Boolean>]
 [-MinimumTlsVersion <String>] [-AllowSharedKeyAccess <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eaf62-107">ActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="eaf62-107">ActiveDirectoryDomainServicesForFile</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-UpgradeToStorageV2] [-EnableLargeFileShare] [-PublishMicrosoftEndpoint <Boolean>]
 [-PublishInternetEndpoint <Boolean>] -EnableActiveDirectoryDomainServicesForFile <Boolean>
 [-ActiveDirectoryDomainName <String>] [-ActiveDirectoryNetBiosDomainName <String>]
 [-ActiveDirectoryForestName <String>] [-ActiveDirectoryDomainGuid <String>]
 [-ActiveDirectoryDomainSid <String>] [-ActiveDirectoryAzureStorageSid <String>]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AllowSharedKeyAccess <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eaf62-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="eaf62-108">DESCRIPTION</span></span>
<span data-ttu-id="eaf62-109">Il cmdlet **Set-AzStorageAccount** modifica un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="eaf62-109">The **Set-AzStorageAccount** cmdlet modifies an Azure Storage account.</span></span>
<span data-ttu-id="eaf62-110">È possibile usare questo cmdlet per modificare il tipo di account, aggiornare un dominio del cliente o impostare tag su un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="eaf62-110">You can use this cmdlet to modify the account type, update a customer domain, or set tags on a Storage account.</span></span>

## <span data-ttu-id="eaf62-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eaf62-111">EXAMPLES</span></span>

### <span data-ttu-id="eaf62-112">Esempio 1: Impostare il tipo di account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="eaf62-112">Example 1: Set the Storage account type</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Type "Standard_RAGRS"
```

<span data-ttu-id="eaf62-113">Questo comando imposta il tipo di account di archiviazione su Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="eaf62-113">This command sets the Storage account type to Standard_RAGRS.</span></span>

### <span data-ttu-id="eaf62-114">Esempio 2: Impostare un dominio personalizzato per un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="eaf62-114">Example 2: Set a custom domain for a Storage account</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

<span data-ttu-id="eaf62-115">Questo comando imposta un dominio personalizzato per un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="eaf62-115">This command sets a custom domain for a Storage account.</span></span>

### <span data-ttu-id="eaf62-116">Esempio 3: Impostare il valore del livello di accesso</span><span class="sxs-lookup"><span data-stu-id="eaf62-116">Example 3: Set the access tier value</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AccessTier Cool
```

<span data-ttu-id="eaf62-117">Il comando imposta il valore di Access Tier su cool.</span><span class="sxs-lookup"><span data-stu-id="eaf62-117">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="eaf62-118">Esempio 4: Impostare il dominio personalizzato e i tag</span><span class="sxs-lookup"><span data-stu-id="eaf62-118">Example 4: Set the custom domain and tags</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="eaf62-119">Il comando imposta il dominio personalizzato e i tag per un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="eaf62-119">The command sets the custom domain and tags for a Storage account.</span></span>

### <span data-ttu-id="eaf62-120">Esempio 5: Impostare Encryption KeySource su Keyvault</span><span class="sxs-lookup"><span data-stu-id="eaf62-120">Example 5: Set Encryption KeySource to Keyvault</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AssignIdentity
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"

PS C:\>$keyVault = New-AzKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get

PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

<span data-ttu-id="eaf62-121">Questo comando imposta Encryption KeySource con una nuova chiave creata.</span><span class="sxs-lookup"><span data-stu-id="eaf62-121">This command set Encryption KeySource with a new created Keyvault.</span></span>

### <span data-ttu-id="eaf62-122">Esempio 6: Impostare Encryption KeySource su "Microsoft.Storage"</span><span class="sxs-lookup"><span data-stu-id="eaf62-122">Example 6: Set Encryption KeySource to "Microsoft.Storage"</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -StorageEncryption
```

<span data-ttu-id="eaf62-123">Questo comando imposta Encryption KeySource su "Microsoft.Storage"</span><span class="sxs-lookup"><span data-stu-id="eaf62-123">This command set Encryption KeySource to "Microsoft.Storage"</span></span>

### <span data-ttu-id="eaf62-124">Esempio 7: Impostare la proprietà NetworkRuleSet di un account di archiviazione con JSON</span><span class="sxs-lookup"><span data-stu-id="eaf62-124">Example 7: Set NetworkRuleSet property of a Storage account with JSON</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="allow"})
```

<span data-ttu-id="eaf62-125">Questo comando imposta la proprietà NetworkRuleSet di un account di archiviazione con JSON</span><span class="sxs-lookup"><span data-stu-id="eaf62-125">This command sets NetworkRuleSet property of a Storage account with JSON</span></span>

### <span data-ttu-id="eaf62-126">Esempio 8: Ottenere la proprietà NetworkRuleSet da un account di archiviazione e impostarla su un altro account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="eaf62-126">Example 8: Get NetworkRuleSet property from a Storage account, and set it to another Storage account</span></span>
```
PS C:\> $networkRuleSet = (Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount").NetworkRuleSet 
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount2" -NetworkRuleSet $networkRuleSet
```

<span data-ttu-id="eaf62-127">Il primo comando recupera la proprietà NetworkRuleSet da un account di archiviazione, il secondo la imposta su un altro account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="eaf62-127">This first command gets NetworkRuleSet property from a Storage account, and the second command sets it to another Storage account</span></span> 

### <span data-ttu-id="eaf62-128">Esempio 9: Aggiornare un account di archiviazione con tipo "Archiviazione" o "BlobStorage" all'account di archiviazione di tipo "StorageV2"</span><span class="sxs-lookup"><span data-stu-id="eaf62-128">Example 9: Upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account</span></span>
```
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -UpgradeToStorageV2
```

<span data-ttu-id="eaf62-129">Il comando aggiorna un account di archiviazione con tipo "Archiviazione" o "BlobStorage" a un account di archiviazione di tipo "StorageV2".</span><span class="sxs-lookup"><span data-stu-id="eaf62-129">The command upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account.</span></span>

### <span data-ttu-id="eaf62-130">Esempio 10: Aggiornare un account di archiviazione abilitando l'autenticazione DS di Azure Files AAD.</span><span class="sxs-lookup"><span data-stu-id="eaf62-130">Example 10: Update a Storage account by enable Azure Files AAD DS Authentication.</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -EnableAzureActiveDirectoryDomainServicesForFile $true PS

PS C:\> $account.AzureFilesIdentityBasedAuth.DirectoryServiceOptions
AADDS
```

<span data-ttu-id="eaf62-131">Il comando aggiorna un account di archiviazione abilitando l'autenticazione DS di Azure Files AAD.</span><span class="sxs-lookup"><span data-stu-id="eaf62-131">The command update a Storage account by enable Azure Files AAD DS Authentication.</span></span>

### <span data-ttu-id="eaf62-132">Esempio 11: Aggiornare un account di archiviazione abilitando l'autenticazione di File Active Directory Domain Service e quindi visualizzare l'impostazione di autenticazione basata sull'identità dei file</span><span class="sxs-lookup"><span data-stu-id="eaf62-132">Example 11: Update a Storage account by enable Files Active Directory Domain Service Authentication, and then show the File Identity Based authentication setting</span></span>
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

<span data-ttu-id="eaf62-133">Il comando aggiorna un account di archiviazione abilitando l'autenticazione di Azure Files Active Directory Domain Service e quindi mostra l'impostazione di autenticazione basata sull'identità dei file</span><span class="sxs-lookup"><span data-stu-id="eaf62-133">The command updates a Storage account by enable Azure Files Active Directory Domain Service Authentication, and then shows the File Identity Based authentication setting</span></span>

### <span data-ttu-id="eaf62-134">Esempio 12: Set MinimumTlsVersion, AllowBlobPublicAccess e AllowSharedKeyAccess</span><span class="sxs-lookup"><span data-stu-id="eaf62-134">Example 12: Set MinimumTlsVersion, AllowBlobPublicAccess and AllowSharedKeyAccess</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false -AllowSharedKeyAccess $true

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False

PS C:\> $a.AllowSharedKeyAccess
True
```

<span data-ttu-id="eaf62-135">Il comando imposta MinimumTlsVersion, AllowBlobPublicAccess e AllowSharedKeyAccess, quindi mostra le 3 proprietà dell'account</span><span class="sxs-lookup"><span data-stu-id="eaf62-135">The command sets MinimumTlsVersion, AllowBlobPublicAccess and AllowSharedKeyAccess, and then show the the 3 properties of the account</span></span> 

### <span data-ttu-id="eaf62-136">Esempio 13: Aggiornare un account di archiviazione con l'impostazione RoutingPreference</span><span class="sxs-lookup"><span data-stu-id="eaf62-136">Example 13: Update a Storage account with RoutingPreference setting</span></span>
```powershell
PS C:\>$account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -PublishMicrosoftEndpoint $false -PublishInternetEndpoint $true -RoutingChoice InternetRouting

PS C:\>$account.RoutingPreference

RoutingChoice   PublishMicrosoftEndpoints PublishInternetEndpoints
-------------   ------------------------- ------------------------
InternetRouting                     False                     True

PS C:\>$account.PrimaryEndpoints

Blob               : https://mystorageaccount.blob.core.windows.net/
Queue              : https://mystorageaccount.queue.core.windows.net/
Table              : https://mystorageaccount.table.core.windows.net/
File               : https://mystorageaccount.file.core.windows.net/
Web                : https://mystorageaccount.z2.web.core.windows.net/
Dfs                : https://mystorageaccount.dfs.core.windows.net/
MicrosoftEndpoints : 
InternetEndpoints  : {"Blob":"https://mystorageaccount-internetrouting.blob.core.windows.net/","File":"https://mystorageaccount-internetrouting.file.core.windows.net/","Web":"https://mystorageaccount-internetrouting.z2.web.core.windows.net/","Dfs":"https://w
                     eirp3-internetrouting.dfs.core.windows.net/"}
```

<span data-ttu-id="eaf62-137">Questo comando aggiorna un account di archiviazione con l'impostazione RoutingPreference: PublishMicrosoftEndpoint as false, PublishInternetEndpoint as true e RoutingChoice as MicrosoftRouting.</span><span class="sxs-lookup"><span data-stu-id="eaf62-137">This command updates a Storage account with RoutingPreference setting: PublishMicrosoftEndpoint as false, PublishInternetEndpoint as true, and RoutingChoice as MicrosoftRouting.</span></span>

## <span data-ttu-id="eaf62-138">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eaf62-138">PARAMETERS</span></span>

### <span data-ttu-id="eaf62-139">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="eaf62-139">-AccessTier</span></span>
<span data-ttu-id="eaf62-140">Specifica il livello di accesso dell'account di archiviazione modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eaf62-140">Specifies the access tier of the Storage account that this cmdlet modifies.</span></span>
<span data-ttu-id="eaf62-141">I valori accettabili per questo parametro sono: Hot e Cool.</span><span class="sxs-lookup"><span data-stu-id="eaf62-141">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="eaf62-142">Se cambi il livello di accesso, potrebbero verificarsi costi aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="eaf62-142">If you change the access tier, it may result in additional charges.</span></span> <span data-ttu-id="eaf62-143">Per altre informazioni, vedere [Archiviazione BLOB Azure: livelli di archiviazione più](http://go.microsoft.com/fwlink/?LinkId=786482)interessanti e interessanti.</span><span class="sxs-lookup"><span data-stu-id="eaf62-143">For more information, see [Azure Blob Storage: Hot and cool storage tiers](http://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="eaf62-144">Se l'account di archiviazione ha Kind as StorageV2 o BlobStorage, è possibile specificare il *parametro AccessTier.*</span><span class="sxs-lookup"><span data-stu-id="eaf62-144">If the Storage account has Kind as StorageV2 or BlobStorage, you can specify the *AccessTier* parameter.</span></span> <span data-ttu-id="eaf62-145">Se l'account di archiviazione ha Kind as Storage, non specificare il *parametro AccessTier.*</span><span class="sxs-lookup"><span data-stu-id="eaf62-145">If the Storage account has Kind as Storage, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="eaf62-146">-ActiveDirectoryAzureStorageSid</span><span class="sxs-lookup"><span data-stu-id="eaf62-146">-ActiveDirectoryAzureStorageSid</span></span>
<span data-ttu-id="eaf62-147">Specifica l'identificatore di sicurezza (SID) per Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="eaf62-147">Specifies the security identifier (SID) for Azure Storage.</span></span> <span data-ttu-id="eaf62-148">Questo parametro deve essere impostato quando -EnableActiveDirectoryDomainServicesForFile è impostato su true.</span><span class="sxs-lookup"><span data-stu-id="eaf62-148">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="eaf62-149">-ActiveDirectoryDomainGuid</span><span class="sxs-lookup"><span data-stu-id="eaf62-149">-ActiveDirectoryDomainGuid</span></span>
<span data-ttu-id="eaf62-150">Specifica il GUID del dominio.</span><span class="sxs-lookup"><span data-stu-id="eaf62-150">Specifies the domain GUID.</span></span> <span data-ttu-id="eaf62-151">Questo parametro deve essere impostato quando -EnableActiveDirectoryDomainServicesForFile è impostato su true.</span><span class="sxs-lookup"><span data-stu-id="eaf62-151">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="eaf62-152">-ActiveDirectoryDomainName</span><span class="sxs-lookup"><span data-stu-id="eaf62-152">-ActiveDirectoryDomainName</span></span>
<span data-ttu-id="eaf62-153">Specifica il dominio primario per cui è autorevole il server DNS di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="eaf62-153">Specifies the primary domain that the AD DNS server is authoritative for.</span></span> <span data-ttu-id="eaf62-154">Questo parametro deve essere impostato quando -EnableActiveDirectoryDomainServicesForFile è impostato su true.</span><span class="sxs-lookup"><span data-stu-id="eaf62-154">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="eaf62-155">-ActiveDirectoryDomainSid</span><span class="sxs-lookup"><span data-stu-id="eaf62-155">-ActiveDirectoryDomainSid</span></span>
<span data-ttu-id="eaf62-156">Specifica l'identificatore di sicurezza (SID).</span><span class="sxs-lookup"><span data-stu-id="eaf62-156">Specifies the security identifier (SID).</span></span> <span data-ttu-id="eaf62-157">Questo parametro deve essere impostato quando -EnableActiveDirectoryDomainServicesForFile è impostato su true.</span><span class="sxs-lookup"><span data-stu-id="eaf62-157">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="eaf62-158">-ActiveDirectoryForestName</span><span class="sxs-lookup"><span data-stu-id="eaf62-158">-ActiveDirectoryForestName</span></span>
<span data-ttu-id="eaf62-159">Specifica la foresta di Active Directory da recuperare.</span><span class="sxs-lookup"><span data-stu-id="eaf62-159">Specifies the Active Directory forest to get.</span></span> <span data-ttu-id="eaf62-160">Questo parametro deve essere impostato quando -EnableActiveDirectoryDomainServicesForFile è impostato su true.</span><span class="sxs-lookup"><span data-stu-id="eaf62-160">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="eaf62-161">-ActiveDirectoryNetDomainName</span><span class="sxs-lookup"><span data-stu-id="eaf62-161">-ActiveDirectoryNetBiosDomainName</span></span>
<span data-ttu-id="eaf62-162">Specifica il nome di dominio Net PIÙ.ER.</span><span class="sxs-lookup"><span data-stu-id="eaf62-162">Specifies the NetBIOS domain name.</span></span> <span data-ttu-id="eaf62-163">Questo parametro deve essere impostato quando -EnableActiveDirectoryDomainServicesForFile è impostato su true.</span><span class="sxs-lookup"><span data-stu-id="eaf62-163">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="eaf62-164">-AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="eaf62-164">-AllowBlobPublicAccess</span></span>
<span data-ttu-id="eaf62-165">Consentire o non consentire l'accesso pubblico a tutti i BLOB o contenitori nell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="eaf62-165">Allow or disallow public access to all blobs or containers in the storage account.</span></span>

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

### <span data-ttu-id="eaf62-166">-AllowSharedKeyAccess</span><span class="sxs-lookup"><span data-stu-id="eaf62-166">-AllowSharedKeyAccess</span></span>
<span data-ttu-id="eaf62-167">Indica se l'account di archiviazione consente di autorizzare le richieste con la chiave di accesso dell'account tramite chiave condivisa.</span><span class="sxs-lookup"><span data-stu-id="eaf62-167">Indicates whether the storage account permits requests to be authorized with the account access key via Shared Key.</span></span> <span data-ttu-id="eaf62-168">Se false, tutte le richieste, incluse le firme di accesso condiviso, devono essere autorizzate con Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="eaf62-168">If false, then all requests, including shared access signatures, must be authorized with Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="eaf62-169">Il valore predefinito è Null, che equivale a true.</span><span class="sxs-lookup"><span data-stu-id="eaf62-169">The default value is null, which is equivalent to true.</span></span>

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

### <span data-ttu-id="eaf62-170">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eaf62-170">-AsJob</span></span>
<span data-ttu-id="eaf62-171">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="eaf62-171">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eaf62-172">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="eaf62-172">-AssignIdentity</span></span>
<span data-ttu-id="eaf62-173">Generare e assegnare una nuova identità dell'account di archiviazione per questo account di archiviazione da usare con servizi di gestione delle chiavi come Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="eaf62-173">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="eaf62-174">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="eaf62-174">-CustomDomainName</span></span>
<span data-ttu-id="eaf62-175">Specifica il nome del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="eaf62-175">Specifies the name of the custom domain.</span></span>

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

### <span data-ttu-id="eaf62-176">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaf62-176">-DefaultProfile</span></span>
<span data-ttu-id="eaf62-177">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eaf62-177">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eaf62-178">-EnableActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="eaf62-178">-EnableActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="eaf62-179">Abilitare l'autenticazione di Active Directory Domain Service per i file di Azure per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="eaf62-179">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="eaf62-180">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="eaf62-180">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="eaf62-181">Abilitare l'autenticazione di Active Directory Domain Service per i file di Azure per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="eaf62-181">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="eaf62-182">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="eaf62-182">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="eaf62-183">Indica se l'account di archiviazione abilita o meno solo il traffico HTTPS.</span><span class="sxs-lookup"><span data-stu-id="eaf62-183">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="eaf62-184">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="eaf62-184">-EnableLargeFileShare</span></span>
<span data-ttu-id="eaf62-185">Indica se l'account di archiviazione può supportare condivisioni file di grandi dimensioni con una capacità superiore a 5 TB.</span><span class="sxs-lookup"><span data-stu-id="eaf62-185">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="eaf62-186">Una volta abilitato l'account, la funzionalità non può essere disabilitata.</span><span class="sxs-lookup"><span data-stu-id="eaf62-186">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="eaf62-187">Attualmente supportato solo per i tipi di replica LRS e ZRS, pertanto non sarebbe possibile eseguire la conversione degli account in account geo-ridondanti.</span><span class="sxs-lookup"><span data-stu-id="eaf62-187">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="eaf62-188">Scopri di più in https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="eaf62-188">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="eaf62-189">-Force</span><span class="sxs-lookup"><span data-stu-id="eaf62-189">-Force</span></span>
<span data-ttu-id="eaf62-190">Forza la scrittura della modifica nell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="eaf62-190">Forces the change to be written to the Storage account.</span></span>

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

### <span data-ttu-id="eaf62-191">-KeyName</span><span class="sxs-lookup"><span data-stu-id="eaf62-191">-KeyName</span></span>
<span data-ttu-id="eaf62-192">Se si usa -KeyvaultEncryption per abilitare la crittografia con il Vault delle chiavi, specificare la proprietà Keyname con questa opzione.</span><span class="sxs-lookup"><span data-stu-id="eaf62-192">If using -KeyvaultEncryption to enable encryption with Key Vault, specify the Keyname property with this option.</span></span>

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

### <span data-ttu-id="eaf62-193">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="eaf62-193">-KeyvaultEncryption</span></span>
<span data-ttu-id="eaf62-194">Indica se usare o meno Microsoft KeyVault per le chiavi di crittografia quando si usa La crittografia del servizio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="eaf62-194">Indicates whether or not to use Microsoft KeyVault for the encryption keys when using Storage Service Encryption.</span></span> <span data-ttu-id="eaf62-195">Se KeyName, KeyVersion e KeyVaultUri sono tutti impostati, KeySource verrà impostato su Microsoft.Keyvault, indipendentemente dal fatto che questo parametro sia impostato o meno.</span><span class="sxs-lookup"><span data-stu-id="eaf62-195">If KeyName, KeyVersion, and KeyVaultUri are all set, KeySource will be set to Microsoft.Keyvault whether this parameter is set or not.</span></span> 

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

### <span data-ttu-id="eaf62-196">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="eaf62-196">-KeyVaultUri</span></span>
<span data-ttu-id="eaf62-197">Quando si usa la crittografia del Vault delle chiavi specificando il parametro -KeyvaultEncryption, usare questa opzione per specificare l'URI per il Vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="eaf62-197">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Vault.</span></span>

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

### <span data-ttu-id="eaf62-198">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="eaf62-198">-KeyVersion</span></span>
<span data-ttu-id="eaf62-199">Quando si usa la crittografia del Vault delle chiavi specificando il parametro -KeyvaultEncryption, usare questa opzione per specificare l'URI per la versione della chiave.</span><span class="sxs-lookup"><span data-stu-id="eaf62-199">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Version.</span></span>

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

### <span data-ttu-id="eaf62-200">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="eaf62-200">-MinimumTlsVersion</span></span>
<span data-ttu-id="eaf62-201">La versione minima di TLS da poter usare per le richieste di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="eaf62-201">The minimum TLS version to be permitted on requests to storage.</span></span>

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

### <span data-ttu-id="eaf62-202">-Name</span><span class="sxs-lookup"><span data-stu-id="eaf62-202">-Name</span></span>
<span data-ttu-id="eaf62-203">Specifica il nome dell'account di archiviazione da modificare.</span><span class="sxs-lookup"><span data-stu-id="eaf62-203">Specifies the name of the Storage account to modify.</span></span>

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

### <span data-ttu-id="eaf62-204">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="eaf62-204">-NetworkRuleSet</span></span>
<span data-ttu-id="eaf62-205">NetworkRuleSet viene usato per definire un set di regole di configurazione per firewall e reti virtuali, nonché per impostare i valori per le proprietà di rete, ad esempio i servizi autorizzati a ignorare le regole e come gestire le richieste che non corrispondono a nessuna delle regole definite.</span><span class="sxs-lookup"><span data-stu-id="eaf62-205">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="eaf62-206">-PublishInternetEndpoint</span><span class="sxs-lookup"><span data-stu-id="eaf62-206">-PublishInternetEndpoint</span></span>
<span data-ttu-id="eaf62-207">Indica se gli endpoint di archiviazione del routing Internet devono essere pubblicati</span><span class="sxs-lookup"><span data-stu-id="eaf62-207">Indicates whether internet  routing storage endpoints are to be published</span></span>

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

### <span data-ttu-id="eaf62-208">-PublishMicrosoftEndpoint</span><span class="sxs-lookup"><span data-stu-id="eaf62-208">-PublishMicrosoftEndpoint</span></span>
<span data-ttu-id="eaf62-209">Indica se gli endpoint di archiviazione del routing Microsoft devono essere pubblicati</span><span class="sxs-lookup"><span data-stu-id="eaf62-209">Indicates whether microsoft routing storage endpoints are to be published</span></span>

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

### <span data-ttu-id="eaf62-210">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eaf62-210">-ResourceGroupName</span></span>
<span data-ttu-id="eaf62-211">Specifica il nome del gruppo di risorse in cui modificare l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="eaf62-211">Specifies the name of the resource group in which to modify the Storage account.</span></span>

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

### <span data-ttu-id="eaf62-212">-RoutingChoice</span><span class="sxs-lookup"><span data-stu-id="eaf62-212">-RoutingChoice</span></span>
<span data-ttu-id="eaf62-213">Routing Choice definisce il tipo di routing di rete scelto dall'utente.</span><span class="sxs-lookup"><span data-stu-id="eaf62-213">Routing Choice defines the kind of network routing opted by the user.</span></span> <span data-ttu-id="eaf62-214">I valori possibili includono: 'MicrosoftRouting', 'InternetRouting'</span><span class="sxs-lookup"><span data-stu-id="eaf62-214">Possible values include: 'MicrosoftRouting', 'InternetRouting'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MicrosoftRouting, InternetRouting

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaf62-215">-SKUName</span><span class="sxs-lookup"><span data-stu-id="eaf62-215">-SkuName</span></span>
<span data-ttu-id="eaf62-216">Specifica il nome SKU dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="eaf62-216">Specifies the SKU name of the Storage account.</span></span>
<span data-ttu-id="eaf62-217">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="eaf62-217">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="eaf62-218">Standard_LRS: archiviazione ridondante in locale.</span><span class="sxs-lookup"><span data-stu-id="eaf62-218">Standard_LRS - Locally-redundant storage.</span></span>
- <span data-ttu-id="eaf62-219">Standard_ZRS - Spazio di archiviazione ridondante.</span><span class="sxs-lookup"><span data-stu-id="eaf62-219">Standard_ZRS - Zone-redundant storage.</span></span>
- <span data-ttu-id="eaf62-220">Standard_GRS: archiviazione geo-ridondante.</span><span class="sxs-lookup"><span data-stu-id="eaf62-220">Standard_GRS - Geo-redundant storage.</span></span>
- <span data-ttu-id="eaf62-221">Standard_RAGRS- Accesso in lettura all'archiviazione geo-ridondante.</span><span class="sxs-lookup"><span data-stu-id="eaf62-221">Standard_RAGRS - Read access geo-redundant storage.</span></span>
- <span data-ttu-id="eaf62-222">Premium_LRS- Spazio di archiviazione premium ridondante localmente.</span><span class="sxs-lookup"><span data-stu-id="eaf62-222">Premium_LRS - Premium locally-redundant storage.</span></span>
- <span data-ttu-id="eaf62-223">Standard_GZRS: archiviazione con ridondanza geografica e con ridondanza d'area.</span><span class="sxs-lookup"><span data-stu-id="eaf62-223">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="eaf62-224">Standard_RAGZRS - Accesso in lettura con accesso geo-ridondante e archiviazione ridondante.</span><span class="sxs-lookup"><span data-stu-id="eaf62-224">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>
<span data-ttu-id="eaf62-225">Non è possibile modificare Standard_ZRS e Premium_LRS ad altri tipi di account.</span><span class="sxs-lookup"><span data-stu-id="eaf62-225">You cannot change Standard_ZRS and Premium_LRS types to other account types.</span></span>
<span data-ttu-id="eaf62-226">Non è possibile modificare altri tipi di account Standard_ZRS o Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="eaf62-226">You cannot change other account types to Standard_ZRS or Premium_LRS.</span></span>

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

### <span data-ttu-id="eaf62-227">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="eaf62-227">-StorageEncryption</span></span>
<span data-ttu-id="eaf62-228">Indica se impostare o meno la crittografia dell'account di archiviazione per l'uso delle chiavi gestite da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="eaf62-228">Indicates whether or not to set the Storage account encryption to use Microsoft-managed keys.</span></span>

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

### <span data-ttu-id="eaf62-229">-Tag</span><span class="sxs-lookup"><span data-stu-id="eaf62-229">-Tag</span></span>
<span data-ttu-id="eaf62-230">Coppie chiave-valore sotto forma di tabella hash impostata come tag nel server.</span><span class="sxs-lookup"><span data-stu-id="eaf62-230">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="eaf62-231">Ad esempio: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="eaf62-231">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="eaf62-232">-UpgradeToStorageV2</span><span class="sxs-lookup"><span data-stu-id="eaf62-232">-UpgradeToStorageV2</span></span>
<span data-ttu-id="eaf62-233">Aggiornare il tipo di account di archiviazione da Archiviazione o BlobStorage a StorageV2.</span><span class="sxs-lookup"><span data-stu-id="eaf62-233">Upgrade Storage account Kind from  Storage or BlobStorage to StorageV2.</span></span>

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

### <span data-ttu-id="eaf62-234">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="eaf62-234">-UseSubDomain</span></span>
<span data-ttu-id="eaf62-235">Indica se abilitare la convalida indiretta di CName.</span><span class="sxs-lookup"><span data-stu-id="eaf62-235">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="eaf62-236">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eaf62-236">-Confirm</span></span>
<span data-ttu-id="eaf62-237">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eaf62-237">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eaf62-238">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eaf62-238">-WhatIf</span></span>
<span data-ttu-id="eaf62-239">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eaf62-239">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eaf62-240">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eaf62-240">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eaf62-241">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaf62-241">CommonParameters</span></span>
<span data-ttu-id="eaf62-242">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eaf62-242">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaf62-243">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eaf62-243">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaf62-244">INPUT</span><span class="sxs-lookup"><span data-stu-id="eaf62-244">INPUTS</span></span>

### <span data-ttu-id="eaf62-245">System.String</span><span class="sxs-lookup"><span data-stu-id="eaf62-245">System.String</span></span>

### <span data-ttu-id="eaf62-246">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="eaf62-246">System.Collections.Hashtable</span></span>

## <span data-ttu-id="eaf62-247">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eaf62-247">OUTPUTS</span></span>

### <span data-ttu-id="eaf62-248">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="eaf62-248">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="eaf62-249">NOTE</span><span class="sxs-lookup"><span data-stu-id="eaf62-249">NOTES</span></span>

## <span data-ttu-id="eaf62-250">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eaf62-250">RELATED LINKS</span></span>

[<span data-ttu-id="eaf62-251">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="eaf62-251">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="eaf62-252">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="eaf62-252">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="eaf62-253">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="eaf62-253">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)
