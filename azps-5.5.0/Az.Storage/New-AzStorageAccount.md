---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: 0e1243765064717c6e0030b437c07a176a232f44
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195774"
---
# <span data-ttu-id="08d11-101">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="08d11-101">New-AzStorageAccount</span></span>

## <span data-ttu-id="08d11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08d11-102">SYNOPSIS</span></span>
<span data-ttu-id="08d11-103">Crea un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="08d11-103">Creates a Storage account.</span></span>

## <span data-ttu-id="08d11-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="08d11-104">SYNTAX</span></span>

### <span data-ttu-id="08d11-105">AzureActiveDirectoryDomainServicesForFile (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="08d11-105">AzureActiveDirectoryDomainServicesForFile (Default)</span></span>
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>]
 [-EnableLargeFileShare] [-PublishMicrosoftEndpoint <Boolean>] [-PublishInternetEndpoint <Boolean>] [-AsJob]
 [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [<CommonParameters>]
```

### <span data-ttu-id="08d11-106">ActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="08d11-106">ActiveDirectoryDomainServicesForFile</span></span>
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableLargeFileShare] [-PublishMicrosoftEndpoint <Boolean>]
 [-PublishInternetEndpoint <Boolean>] [-EnableActiveDirectoryDomainServicesForFile <Boolean>]
 [-ActiveDirectoryDomainName <String>] [-ActiveDirectoryNetBiosDomainName <String>]
 [-ActiveDirectoryForestName <String>] [-ActiveDirectoryDomainGuid <String>]
 [-ActiveDirectoryDomainSid <String>] [-ActiveDirectoryAzureStorageSid <String>] [-AsJob]
 [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [<CommonParameters>]
```

## <span data-ttu-id="08d11-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="08d11-107">DESCRIPTION</span></span>
<span data-ttu-id="08d11-108">Il cmdlet **New-AzStorageAccount** crea un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="08d11-108">The **New-AzStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="08d11-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="08d11-109">EXAMPLES</span></span>

### <span data-ttu-id="08d11-110">Esempio 1: Creare un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="08d11-110">Example 1: Create a Storage account</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="08d11-111">Questo comando crea un account di archiviazione per il gruppo di risorse denominato MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="08d11-111">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="08d11-112">Esempio 2: Creare un account di archiviazione BLOB con BlobStorage Kind e AccessTier a scelta rapida</span><span class="sxs-lookup"><span data-stu-id="08d11-112">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="08d11-113">Questo comando crea un account di Archiviazione BLOB con BlobStorage Kind e AccessTier a scelta rapida</span><span class="sxs-lookup"><span data-stu-id="08d11-113">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="08d11-114">Esempio 3: Creare un account di archiviazione con Kind StorageV2 e generare e assegnare un'identità per Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="08d11-114">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="08d11-115">Questo comando crea un account di archiviazione con Kind StorageV2.</span><span class="sxs-lookup"><span data-stu-id="08d11-115">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="08d11-116">Genera e assegna anche un'identità che può essere usata per gestire le chiavi dell'account tramite Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="08d11-116">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="08d11-117">Esempio 4: Creare un account di archiviazione con NetworkRuleSet da JSON</span><span class="sxs-lookup"><span data-stu-id="08d11-117">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="08d11-118">Questo comando crea un account di archiviazione con la proprietà NetworkRuleSet da JSON</span><span class="sxs-lookup"><span data-stu-id="08d11-118">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

### <span data-ttu-id="08d11-119">Esempio 5: Creare un account di archiviazione con spazio dei nomi gerarchico abilitato.</span><span class="sxs-lookup"><span data-stu-id="08d11-119">Example 5: Create a Storage account with Hierarchical Namespace enabled.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

<span data-ttu-id="08d11-120">Questo comando crea un account di archiviazione con Spazio dei nomi gerarchico abilitato.</span><span class="sxs-lookup"><span data-stu-id="08d11-120">This command creates a Storage account with Hierarchical Namespace enabled.</span></span>

### <span data-ttu-id="08d11-121">Esempio 6: Creare un account di archiviazione con l'autenticazione AAD DS dei file di Azure e abilitare una condivisione file di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="08d11-121">Example 6: Create a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true -EnableLargeFileShare
```

<span data-ttu-id="08d11-122">Questo comando crea un account di archiviazione con l'autenticazione DS AAD dei file di Azure e abilita una condivisione file di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="08d11-122">This command creates a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>

### <span data-ttu-id="08d11-123">Esempio 7: Creare un account di archiviazione con abilitare l'autenticazione di File Active Directory Domain Service.</span><span class="sxs-lookup"><span data-stu-id="08d11-123">Example 7: Create a Storage account with enable Files Active Directory Domain Service Authentication.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableActiveDirectoryDomainServicesForFile $true `
        -ActiveDirectoryDomainName "mydomain.com" `
        -ActiveDirectoryNetBiosDomainName "mydomain.com" `
        -ActiveDirectoryForestName "mydomain.com" `
        -ActiveDirectoryDomainGuid "12345678-1234-1234-1234-123456789012" `
        -ActiveDirectoryDomainSid "S-1-5-21-1234567890-1234567890-1234567890" `
        -ActiveDirectoryAzureStorageSid "S-1-5-21-1234567890-1234567890-1234567890-1234"
```

<span data-ttu-id="08d11-124">Questo comando crea un account di archiviazione con l'autenticazione di Servizi di dominio Active Directory per File.</span><span class="sxs-lookup"><span data-stu-id="08d11-124">This command creates a Storage account withenable Files Active Directory Domain Service Authentication.</span></span>

### <span data-ttu-id="08d11-125">Esempio 8: Creare un account di archiviazione con i servizi di coda e tabella con chiave di crittografia con ambito account e Richiedere la crittografia dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="08d11-125">Example 8: Create a Storage account with Queue and Table Service use account-scoped encryption key, and Require Infrastructure Encryption.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EncryptionKeyTypeForTable Account -EncryptionKeyTypeForQueue Account -RequireInfrastructureEncryption

PS C:\>$account = get-AzStorageAccount -ResourceGroupName $rgname -StorageAccountName $accountName

PS C:\>$account.Encryption.Services.Queue

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account

PS C:\>$account.Encryption.Services.Table

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account

PS C:\> $account.Encryption.RequireInfrastructureEncryption
True
```

<span data-ttu-id="08d11-126">Questo comando crea un account di archiviazione con Coda e Servizio tabelle con chiave di crittografia con ambito account e Richiedi crittografia infrastruttura, quindi Coda e Tabella useranno la stessa chiave di crittografia con il servizio BLOB e file e il servizio applicherà un livello secondario di crittografia con chiavi gestite della piattaforma per i dati in archivio.</span><span class="sxs-lookup"><span data-stu-id="08d11-126">This command creates a Storage account with Queue and Table Service use account-scoped encryption key and Require Infrastructure Encryption, so Queue and Table will use same encryption key with Blob and File service, and the service will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>
<span data-ttu-id="08d11-127">Ottenere quindi le proprietà dell'account di archiviazione e visualizzare il tipo di chiave di crittografia del servizio di coda e di tabella e il valore RequireInfrastructureEncryption.</span><span class="sxs-lookup"><span data-stu-id="08d11-127">Then get the Storage account properties, and view the encryption keytype of Queue and Table Service, and RequireInfrastructureEncryption value.</span></span>

### <span data-ttu-id="08d11-128">Esempio 9: Creare un account MinimumTlsVersion e AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="08d11-128">Example 9: Create account MinimumTlsVersion  and AllowBlobPublicAccess</span></span>
```
PS C:\> $account = New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2 -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False
```

<span data-ttu-id="08d11-129">Comando Crea account con MinimumTlsVersion e AllowBlobPublicAccess e quindi visualizza le 2 proprietà dell'account creato</span><span class="sxs-lookup"><span data-stu-id="08d11-129">The command create account with MinimumTlsVersion  and AllowBlobPublicAccess, and then show the the 2 properties of the created account</span></span> 

### <span data-ttu-id="08d11-130">Esempio 10: Creare un account di archiviazione con l'impostazione RoutingPreference</span><span class="sxs-lookup"><span data-stu-id="08d11-130">Example 10: Create a Storage account with RoutingPreference setting</span></span>
```powershell
PS C:\>$account = New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -PublishMicrosoftEndpoint $true -PublishInternetEndpoint $true -RoutingChoice MicrosoftRouting

PS C:\>$account.RoutingPreference

RoutingChoice    PublishMicrosoftEndpoints PublishInternetEndpoints
-------------    ------------------------- ------------------------
MicrosoftRouting                     True                     True

PS C:\>$account.PrimaryEndpoints

Blob               : https://mystorageaccount.blob.core.windows.net/
Queue              : https://mystorageaccount.queue.core.windows.net/
Table              : https://mystorageaccount.table.core.windows.net/
File               : https://mystorageaccount.file.core.windows.net/
Web                : https://mystorageaccount.z2.web.core.windows.net/
Dfs                : https://mystorageaccount.dfs.core.windows.net/
MicrosoftEndpoints : {"Blob":"https://mystorageaccount-microsoftrouting.blob.core.windows.net/","Queue":"https://mystorageaccount-microsoftrouting.queue.core.windows.net/","Table":"https://mystorageaccount-microsoftrouting.table.core.windows.net/","File":"ht
                     tps://mystorageaccount-microsoftrouting.file.core.windows.net/","Web":"https://mystorageaccount-microsoftrouting.z2.web.core.windows.net/","Dfs":"https://mystorageaccount-microsoftrouting.dfs.core.windows.net/"}
InternetEndpoints  : {"Blob":"https://mystorageaccount-internetrouting.blob.core.windows.net/","File":"https://mystorageaccount-internetrouting.file.core.windows.net/","Web":"https://mystorageaccount-internetrouting.z2.web.core.windows.net/","Dfs":"https://w
                     eirp3-internetrouting.dfs.core.windows.net/"}
```

<span data-ttu-id="08d11-131">Questo comando crea un account di archiviazione con l'impostazione RoutingPreference: PublishMicrosoftEndpoint e PublishInternetEndpoint come true e RoutingChoice come MicrosoftRouting.</span><span class="sxs-lookup"><span data-stu-id="08d11-131">This command creates a Storage account with RoutingPreference setting: PublishMicrosoftEndpoint and PublishInternetEndpoint as true, and RoutingChoice as MicrosoftRouting.</span></span>

## <span data-ttu-id="08d11-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="08d11-132">PARAMETERS</span></span>

### <span data-ttu-id="08d11-133">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="08d11-133">-AccessTier</span></span>
<span data-ttu-id="08d11-134">Specifica il livello di accesso dell'account di archiviazione creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08d11-134">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="08d11-135">I valori accettabili per questo parametro sono: Hot e Cool.</span><span class="sxs-lookup"><span data-stu-id="08d11-135">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="08d11-136">Se si specifica un valore di BlobStorage per il *parametro Kind,* è necessario specificare un valore per il *parametro AccessTier.*</span><span class="sxs-lookup"><span data-stu-id="08d11-136">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="08d11-137">Se si specifica un valore di Archiviazione per il *parametro Kind,* non specificare il *parametro AccessTier.*</span><span class="sxs-lookup"><span data-stu-id="08d11-137">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="08d11-138">-ActiveDirectoryAzureStorageSid</span><span class="sxs-lookup"><span data-stu-id="08d11-138">-ActiveDirectoryAzureStorageSid</span></span>
<span data-ttu-id="08d11-139">Specifica l'identificatore di sicurezza (SID) per Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="08d11-139">Specifies the security identifier (SID) for Azure Storage.</span></span> <span data-ttu-id="08d11-140">Questo parametro deve essere impostato quando -EnableActiveDirectoryDomainServicesForFile è impostato su true.</span><span class="sxs-lookup"><span data-stu-id="08d11-140">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="08d11-141">-ActiveDirectoryDomainGuid</span><span class="sxs-lookup"><span data-stu-id="08d11-141">-ActiveDirectoryDomainGuid</span></span>
<span data-ttu-id="08d11-142">Specifica il GUID del dominio.</span><span class="sxs-lookup"><span data-stu-id="08d11-142">Specifies the domain GUID.</span></span> <span data-ttu-id="08d11-143">Questo parametro deve essere impostato quando -EnableActiveDirectoryDomainServicesForFile è impostato su true.</span><span class="sxs-lookup"><span data-stu-id="08d11-143">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="08d11-144">-ActiveDirectoryDomainName</span><span class="sxs-lookup"><span data-stu-id="08d11-144">-ActiveDirectoryDomainName</span></span>
<span data-ttu-id="08d11-145">Specifica il dominio primario per cui è autorevole il server DNS di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="08d11-145">Specifies the primary domain that the AD DNS server is authoritative for.</span></span> <span data-ttu-id="08d11-146">Questo parametro deve essere impostato quando -EnableActiveDirectoryDomainServicesForFile è impostato su true.</span><span class="sxs-lookup"><span data-stu-id="08d11-146">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="08d11-147">-ActiveDirectoryDomainSid</span><span class="sxs-lookup"><span data-stu-id="08d11-147">-ActiveDirectoryDomainSid</span></span>
<span data-ttu-id="08d11-148">Specifica l'identificatore di sicurezza (SID).</span><span class="sxs-lookup"><span data-stu-id="08d11-148">Specifies the security identifier (SID).</span></span> <span data-ttu-id="08d11-149">Questo parametro deve essere impostato quando -EnableActiveDirectoryDomainServicesForFile è impostato su true.</span><span class="sxs-lookup"><span data-stu-id="08d11-149">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="08d11-150">-ActiveDirectoryForestName</span><span class="sxs-lookup"><span data-stu-id="08d11-150">-ActiveDirectoryForestName</span></span>
<span data-ttu-id="08d11-151">Specifica la foresta di Active Directory da recuperare.</span><span class="sxs-lookup"><span data-stu-id="08d11-151">Specifies the Active Directory forest to get.</span></span> <span data-ttu-id="08d11-152">Questo parametro deve essere impostato quando -EnableActiveDirectoryDomainServicesForFile è impostato su true.</span><span class="sxs-lookup"><span data-stu-id="08d11-152">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="08d11-153">-ActiveDirectoryNetDomainName</span><span class="sxs-lookup"><span data-stu-id="08d11-153">-ActiveDirectoryNetBiosDomainName</span></span>
<span data-ttu-id="08d11-154">Specifica il nome di dominio Net PIÙ.ER.</span><span class="sxs-lookup"><span data-stu-id="08d11-154">Specifies the NetBIOS domain name.</span></span> <span data-ttu-id="08d11-155">Questo parametro deve essere impostato quando -EnableActiveDirectoryDomainServicesForFile è impostato su true.</span><span class="sxs-lookup"><span data-stu-id="08d11-155">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="08d11-156">-AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="08d11-156">-AllowBlobPublicAccess</span></span>
<span data-ttu-id="08d11-157">Consentire l'accesso pubblico a tutti i BLOB o contenitori nell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="08d11-157">Allow public access to all blobs or containers in the storage account.</span></span> <span data-ttu-id="08d11-158">L'interpretazione predefinita è vera per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="08d11-158">The default interpretation is true for this property.</span></span>

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

### <span data-ttu-id="08d11-159">-AsJob</span><span class="sxs-lookup"><span data-stu-id="08d11-159">-AsJob</span></span>
<span data-ttu-id="08d11-160">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="08d11-160">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="08d11-161">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="08d11-161">-AssignIdentity</span></span>
<span data-ttu-id="08d11-162">Generare e assegnare una nuova identità dell'account di archiviazione per questo account di archiviazione da usare con servizi di gestione delle chiavi come Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="08d11-162">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="08d11-163">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="08d11-163">-CustomDomainName</span></span>
<span data-ttu-id="08d11-164">Specifica il nome del dominio personalizzato dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="08d11-164">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="08d11-165">Il valore predefinito è Archiviazione.</span><span class="sxs-lookup"><span data-stu-id="08d11-165">The default value is Storage.</span></span>

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

### <span data-ttu-id="08d11-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08d11-166">-DefaultProfile</span></span>
<span data-ttu-id="08d11-167">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="08d11-167">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08d11-168">-EnableActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="08d11-168">-EnableActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="08d11-169">Abilitare l'autenticazione di Active Directory Domain Service per i file di Azure per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="08d11-169">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08d11-170">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="08d11-170">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="08d11-171">Abilitare l'autenticazione di Azure Active Directory Domain Service per i file di Azure per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="08d11-171">Enable Azure Files Azure Active Directory Domain Service Authentication for the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AzureActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08d11-172">-EnableHierarchicalZone</span><span class="sxs-lookup"><span data-stu-id="08d11-172">-EnableHierarchicalNamespace</span></span>
<span data-ttu-id="08d11-173">Indica se l'account di archiviazione abilita o meno lo spazio dei nomi gerarchico.</span><span class="sxs-lookup"><span data-stu-id="08d11-173">Indicates whether or not the Storage account enables Hierarchical Namespace.</span></span>

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

### <span data-ttu-id="08d11-174">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="08d11-174">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="08d11-175">Indica se l'account di archiviazione abilita o meno solo il traffico HTTPS.</span><span class="sxs-lookup"><span data-stu-id="08d11-175">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="08d11-176">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="08d11-176">-EnableLargeFileShare</span></span>
<span data-ttu-id="08d11-177">Indica se l'account di archiviazione può supportare condivisioni file di grandi dimensioni con una capacità superiore a 5 TB.</span><span class="sxs-lookup"><span data-stu-id="08d11-177">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="08d11-178">Una volta abilitato l'account, la funzionalità non può essere disabilitata.</span><span class="sxs-lookup"><span data-stu-id="08d11-178">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="08d11-179">Attualmente supportato solo per i tipi di replica LRS e ZRS, pertanto non sarebbe possibile eseguire la conversione degli account in account geo-ridondanti.</span><span class="sxs-lookup"><span data-stu-id="08d11-179">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="08d11-180">Scopri di più in https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="08d11-180">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="08d11-181">-EncryptionKeyTypeForQueue</span><span class="sxs-lookup"><span data-stu-id="08d11-181">-EncryptionKeyTypeForQueue</span></span>
<span data-ttu-id="08d11-182">Impostare il tipo di chiave di crittografia per la coda.</span><span class="sxs-lookup"><span data-stu-id="08d11-182">Set the Encryption KeyType for Queue.</span></span> <span data-ttu-id="08d11-183">Il valore predefinito è Servizio.</span><span class="sxs-lookup"><span data-stu-id="08d11-183">The default value is Service.</span></span>
<span data-ttu-id="08d11-184">-Account: la coda verrà crittografata con la chiave di crittografia con ambito account.</span><span class="sxs-lookup"><span data-stu-id="08d11-184">-Account: Queue will be encrypted with account-scoped encryption key.</span></span> <span data-ttu-id="08d11-185">-Servizio: la coda sarà sempre crittografata con Service-Managed chiavi.</span><span class="sxs-lookup"><span data-stu-id="08d11-185">-Service: Queue will always be encrypted with Service-Managed keys.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Service, Account

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08d11-186">-EncryptionKeyTypeForTable</span><span class="sxs-lookup"><span data-stu-id="08d11-186">-EncryptionKeyTypeForTable</span></span>
<span data-ttu-id="08d11-187">Impostare il tipo di chiave di crittografia per la tabella.</span><span class="sxs-lookup"><span data-stu-id="08d11-187">Set the Encryption KeyType for Table.</span></span> <span data-ttu-id="08d11-188">Il valore predefinito è Servizio.</span><span class="sxs-lookup"><span data-stu-id="08d11-188">The default value is Service.</span></span>
- <span data-ttu-id="08d11-189">Account: la tabella verrà crittografata con la chiave di crittografia con ambito account.</span><span class="sxs-lookup"><span data-stu-id="08d11-189">Account: Table will be encrypted with account-scoped encryption key.</span></span> 
- <span data-ttu-id="08d11-190">Servizio: la tabella sarà sempre crittografata con Service-Managed chiavi.</span><span class="sxs-lookup"><span data-stu-id="08d11-190">Service: Table will always be encrypted with Service-Managed keys.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Service, Account

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08d11-191">-Kind</span><span class="sxs-lookup"><span data-stu-id="08d11-191">-Kind</span></span>
<span data-ttu-id="08d11-192">Specifica il tipo di account di archiviazione creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08d11-192">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="08d11-193">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="08d11-193">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="08d11-194">Spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="08d11-194">Storage.</span></span> <span data-ttu-id="08d11-195">Account di archiviazione generico che supporta l'archiviazione di BLOB, tabelle, code, file e dischi.</span><span class="sxs-lookup"><span data-stu-id="08d11-195">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="08d11-196">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="08d11-196">StorageV2.</span></span> <span data-ttu-id="08d11-197">Account di archiviazione generico versione 2 (GPv2) che supporta BLOB, tabelle, code, file e dischi, con caratteristiche avanzate come il livelli dei dati.</span><span class="sxs-lookup"><span data-stu-id="08d11-197">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="08d11-198">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="08d11-198">BlobStorage.</span></span> <span data-ttu-id="08d11-199">Account di Archiviazione BLOB che supporta solo l'archiviazione di BLOB.</span><span class="sxs-lookup"><span data-stu-id="08d11-199">Blob Storage account which supports storage of Blobs only.</span></span>
- <span data-ttu-id="08d11-200">BlockBlobStorage.</span><span class="sxs-lookup"><span data-stu-id="08d11-200">BlockBlobStorage.</span></span> <span data-ttu-id="08d11-201">Bloccare l'account di Archiviazione BLOB che supporta solo l'archiviazione di BLOB di blocco.</span><span class="sxs-lookup"><span data-stu-id="08d11-201">Block Blob Storage account which supports storage of Block Blobs only.</span></span>
- <span data-ttu-id="08d11-202">FileStorage.</span><span class="sxs-lookup"><span data-stu-id="08d11-202">FileStorage.</span></span> <span data-ttu-id="08d11-203">Account di archiviazione file che supporta solo l'archiviazione di file.</span><span class="sxs-lookup"><span data-stu-id="08d11-203">File Storage account which supports storage of Files only.</span></span>
<span data-ttu-id="08d11-204">Il valore predefinito è StorageV2.</span><span class="sxs-lookup"><span data-stu-id="08d11-204">The default value is StorageV2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Storage, StorageV2, BlobStorage, BlockBlobStorage, FileStorage

Required: False
Position: Named
Default value: StorageV2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08d11-205">-Location</span><span class="sxs-lookup"><span data-stu-id="08d11-205">-Location</span></span>
<span data-ttu-id="08d11-206">Specifica la posizione dell'account di archiviazione da creare.</span><span class="sxs-lookup"><span data-stu-id="08d11-206">Specifies the location of the Storage account to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08d11-207">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="08d11-207">-MinimumTlsVersion</span></span>
<span data-ttu-id="08d11-208">La versione minima di TLS da poter usare per le richieste di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="08d11-208">The minimum TLS version to be permitted on requests to storage.</span></span> <span data-ttu-id="08d11-209">L'interpretazione predefinita è TLS 1.0 per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="08d11-209">The default interpretation is TLS 1.0 for this property.</span></span>

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

### <span data-ttu-id="08d11-210">-Name</span><span class="sxs-lookup"><span data-stu-id="08d11-210">-Name</span></span>
<span data-ttu-id="08d11-211">Specifica il nome dell'account di archiviazione da creare.</span><span class="sxs-lookup"><span data-stu-id="08d11-211">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="08d11-212">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="08d11-212">-NetworkRuleSet</span></span>
<span data-ttu-id="08d11-213">NetworkRuleSet viene usato per definire un set di regole di configurazione per firewall e reti virtuali, nonché per impostare i valori per le proprietà di rete, ad esempio i servizi autorizzati a ignorare le regole e come gestire le richieste che non corrispondono a nessuna delle regole definite.</span><span class="sxs-lookup"><span data-stu-id="08d11-213">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="08d11-214">-PublishInternetEndpoint</span><span class="sxs-lookup"><span data-stu-id="08d11-214">-PublishInternetEndpoint</span></span>
<span data-ttu-id="08d11-215">Indica se gli endpoint di archiviazione del routing Internet devono essere pubblicati</span><span class="sxs-lookup"><span data-stu-id="08d11-215">Indicates whether internet  routing storage endpoints are to be published</span></span>

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

### <span data-ttu-id="08d11-216">-PublishMicrosoftEndpoint</span><span class="sxs-lookup"><span data-stu-id="08d11-216">-PublishMicrosoftEndpoint</span></span>
<span data-ttu-id="08d11-217">Indica se gli endpoint di archiviazione del routing Microsoft devono essere pubblicati</span><span class="sxs-lookup"><span data-stu-id="08d11-217">Indicates whether microsoft routing storage endpoints are to be published</span></span>

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

### <span data-ttu-id="08d11-218">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08d11-218">-ResourceGroupName</span></span>
<span data-ttu-id="08d11-219">Specifica il nome del gruppo di risorse in cui aggiungere l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="08d11-219">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="08d11-220">-RoutingChoice</span><span class="sxs-lookup"><span data-stu-id="08d11-220">-RoutingChoice</span></span>
<span data-ttu-id="08d11-221">Routing Choice definisce il tipo di routing di rete scelto dall'utente.</span><span class="sxs-lookup"><span data-stu-id="08d11-221">Routing Choice defines the kind of network routing opted by the user.</span></span> <span data-ttu-id="08d11-222">I valori possibili includono: 'MicrosoftRouting', 'InternetRouting'</span><span class="sxs-lookup"><span data-stu-id="08d11-222">Possible values include: 'MicrosoftRouting', 'InternetRouting'</span></span>

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

### <span data-ttu-id="08d11-223">-SKUName</span><span class="sxs-lookup"><span data-stu-id="08d11-223">-SkuName</span></span>
<span data-ttu-id="08d11-224">Specifica il nome SKU dell'account di archiviazione creato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08d11-224">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="08d11-225">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="08d11-225">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="08d11-226">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="08d11-226">Standard_LRS.</span></span> <span data-ttu-id="08d11-227">Archiviazione ridondante in locale.</span><span class="sxs-lookup"><span data-stu-id="08d11-227">Locally-redundant storage.</span></span>
- <span data-ttu-id="08d11-228">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="08d11-228">Standard_ZRS.</span></span> <span data-ttu-id="08d11-229">Spazio di archiviazione ridondante.</span><span class="sxs-lookup"><span data-stu-id="08d11-229">Zone-redundant storage.</span></span>
- <span data-ttu-id="08d11-230">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="08d11-230">Standard_GRS.</span></span> <span data-ttu-id="08d11-231">Archiviazione geo-ridondante.</span><span class="sxs-lookup"><span data-stu-id="08d11-231">Geo-redundant storage.</span></span>
- <span data-ttu-id="08d11-232">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="08d11-232">Standard_RAGRS.</span></span> <span data-ttu-id="08d11-233">Accesso in lettura all'archiviazione geo-ridondante.</span><span class="sxs-lookup"><span data-stu-id="08d11-233">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="08d11-234">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="08d11-234">Premium_LRS.</span></span> <span data-ttu-id="08d11-235">Spazio di archiviazione premium ridondante in locale.</span><span class="sxs-lookup"><span data-stu-id="08d11-235">Premium locally-redundant storage.</span></span>
- <span data-ttu-id="08d11-236">Premium_ZRS.</span><span class="sxs-lookup"><span data-stu-id="08d11-236">Premium_ZRS.</span></span> <span data-ttu-id="08d11-237">Spazio di archiviazione premium con ridondanza in zona.</span><span class="sxs-lookup"><span data-stu-id="08d11-237">Premium zone-redundant storage.</span></span>
- <span data-ttu-id="08d11-238">Standard_GZRS: archiviazione con zona ridondante geo-ridondante.</span><span class="sxs-lookup"><span data-stu-id="08d11-238">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="08d11-239">Standard_RAGZRS- Accesso in lettura con accesso geo-ridondante e archiviazione ridondante.</span><span class="sxs-lookup"><span data-stu-id="08d11-239">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS, Premium_ZRS, Standard_GZRS, Standard_RAGZRS

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08d11-240">-Tag</span><span class="sxs-lookup"><span data-stu-id="08d11-240">-Tag</span></span>
<span data-ttu-id="08d11-241">Coppie chiave-valore sotto forma di tabella hash impostata come tag nel server.</span><span class="sxs-lookup"><span data-stu-id="08d11-241">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="08d11-242">Ad esempio: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="08d11-242">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08d11-243">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="08d11-243">-UseSubDomain</span></span>
<span data-ttu-id="08d11-244">Indica se abilitare la convalida indiretta di CName.</span><span class="sxs-lookup"><span data-stu-id="08d11-244">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="08d11-245">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08d11-245">CommonParameters</span></span>
<span data-ttu-id="08d11-246">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08d11-246">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08d11-247">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08d11-247">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08d11-248">INPUT</span><span class="sxs-lookup"><span data-stu-id="08d11-248">INPUTS</span></span>

### <span data-ttu-id="08d11-249">System.String</span><span class="sxs-lookup"><span data-stu-id="08d11-249">System.String</span></span>

## <span data-ttu-id="08d11-250">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="08d11-250">OUTPUTS</span></span>

### <span data-ttu-id="08d11-251">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="08d11-251">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="08d11-252">NOTE</span><span class="sxs-lookup"><span data-stu-id="08d11-252">NOTES</span></span>

## <span data-ttu-id="08d11-253">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="08d11-253">RELATED LINKS</span></span>

[<span data-ttu-id="08d11-254">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="08d11-254">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="08d11-255">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="08d11-255">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="08d11-256">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="08d11-256">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)
