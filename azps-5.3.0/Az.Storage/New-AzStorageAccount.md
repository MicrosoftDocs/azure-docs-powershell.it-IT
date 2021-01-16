---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: 022c27b3eec589e395e1044f165ee9f8f17d1cad
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479440"
---
# <span data-ttu-id="de108-101">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="de108-101">New-AzStorageAccount</span></span>

## <span data-ttu-id="de108-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="de108-102">SYNOPSIS</span></span>
<span data-ttu-id="de108-103">Crea un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="de108-103">Creates a Storage account.</span></span>

## <span data-ttu-id="de108-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="de108-104">SYNTAX</span></span>

### <span data-ttu-id="de108-105">AzureActiveDirectoryDomainServicesForFile (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="de108-105">AzureActiveDirectoryDomainServicesForFile (Default)</span></span>
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>]
 [-EnableLargeFileShare] [-AsJob] [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>]
 [-RequireInfrastructureEncryption] [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de108-106">ActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="de108-106">ActiveDirectoryDomainServicesForFile</span></span>
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableLargeFileShare]
 [-EnableActiveDirectoryDomainServicesForFile <Boolean>] [-ActiveDirectoryDomainName <String>]
 [-ActiveDirectoryNetBiosDomainName <String>] [-ActiveDirectoryForestName <String>]
 [-ActiveDirectoryDomainGuid <String>] [-ActiveDirectoryDomainSid <String>]
 [-ActiveDirectoryAzureStorageSid <String>] [-AsJob] [-EncryptionKeyTypeForTable <String>]
 [-EncryptionKeyTypeForQueue <String>] [-RequireInfrastructureEncryption] [-AllowBlobPublicAccess <Boolean>]
 [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de108-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="de108-107">DESCRIPTION</span></span>
<span data-ttu-id="de108-108">Il cmdlet **New-AzStorageAccount** crea un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="de108-108">The **New-AzStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="de108-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="de108-109">EXAMPLES</span></span>

### <span data-ttu-id="de108-110">Esempio 1: creare un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="de108-110">Example 1: Create a Storage account</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="de108-111">Questo comando crea un account di archiviazione per il nome del gruppo di risorse MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="de108-111">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="de108-112">Esempio 2: creare un account di archiviazione BLOB con BlobStorage Kind e Hot AccessTier</span><span class="sxs-lookup"><span data-stu-id="de108-112">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="de108-113">Questo comando crea un account di archiviazione BLOB con BlobStorage Kind e Hot AccessTier</span><span class="sxs-lookup"><span data-stu-id="de108-113">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="de108-114">Esempio 3: creare un account di archiviazione con Kind StorageV2 e generare e assegnare un'identità per il Vault di Azure.</span><span class="sxs-lookup"><span data-stu-id="de108-114">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="de108-115">Questo comando crea un account di archiviazione con Kind StorageV2.</span><span class="sxs-lookup"><span data-stu-id="de108-115">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="de108-116">Viene inoltre generata e assegnata un'identità che può essere usata per gestire le chiavi dell'account tramite Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="de108-116">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="de108-117">Esempio 4: creare un account di archiviazione con NetworkRuleSet da JSON</span><span class="sxs-lookup"><span data-stu-id="de108-117">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="de108-118">Questo comando crea un account di archiviazione con proprietà NetworkRuleSet da JSON</span><span class="sxs-lookup"><span data-stu-id="de108-118">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

### <span data-ttu-id="de108-119">Esempio 5: creare un account di archiviazione con lo spazio dei nomi gerarchico abilitato.</span><span class="sxs-lookup"><span data-stu-id="de108-119">Example 5: Create a Storage account with Hierarchical Namespace enabled.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

<span data-ttu-id="de108-120">Questo comando crea un account di archiviazione con lo spazio dei nomi gerarchico abilitato.</span><span class="sxs-lookup"><span data-stu-id="de108-120">This command creates a Storage account with Hierarchical Namespace enabled.</span></span>

### <span data-ttu-id="de108-121">Esempio 6: creare un account di archiviazione con l'autenticazione dei file di Azure AAD e abilitare la condivisione di file di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="de108-121">Example 6: Create a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true -EnableLargeFileShare
```

<span data-ttu-id="de108-122">Questo comando crea un account di archiviazione con l'autenticazione dei file di Azure AAD e consente la condivisione di file di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="de108-122">This command creates a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>

### <span data-ttu-id="de108-123">Esempio 7: creare un account di archiviazione con l'autenticazione dei servizi di dominio Active Directory Abilita file.</span><span class="sxs-lookup"><span data-stu-id="de108-123">Example 7: Create a Storage account with enable Files Active Directory Domain Service Authentication.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableActiveDirectoryDomainServicesForFile $true `
        -ActiveDirectoryDomainName "mydomain.com" `
        -ActiveDirectoryNetBiosDomainName "mydomain.com" `
        -ActiveDirectoryForestName "mydomain.com" `
        -ActiveDirectoryDomainGuid "12345678-1234-1234-1234-123456789012" `
        -ActiveDirectoryDomainSid "S-1-5-21-1234567890-1234567890-1234567890" `
        -ActiveDirectoryAzureStorageSid "S-1-5-21-1234567890-1234567890-1234567890-1234"
```

<span data-ttu-id="de108-124">Questo comando crea un account di archiviazione withenable file di autenticazione del servizio di dominio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="de108-124">This command creates a Storage account withenable Files Active Directory Domain Service Authentication.</span></span>

### <span data-ttu-id="de108-125">Esempio 8: creare un account di archiviazione con il servizio coda e tabella usare la chiave di crittografia con ambito account e richiedere la crittografia dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="de108-125">Example 8: Create a Storage account with Queue and Table Service use account-scoped encryption key, and Require Infrastructure Encryption.</span></span>
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

<span data-ttu-id="de108-126">Questo comando crea un account di archiviazione con coda e servizio tabella usare la chiave di crittografia con ambito account e richiedere la crittografia dell'infrastruttura, quindi Queue e Table useranno la stessa chiave di crittografia con BLOB e il servizio file e il servizio applicherà un livello secondario di crittografia con le chiavi gestite della piattaforma per i dati a riposo.</span><span class="sxs-lookup"><span data-stu-id="de108-126">This command creates a Storage account with Queue and Table Service use account-scoped encryption key and Require Infrastructure Encryption, so Queue and Table will use same encryption key with Blob and File service, and the service will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>
<span data-ttu-id="de108-127">Ottieni quindi le proprietà dell'account di archiviazione e visualizza il tipo di crittografia del servizio di Accodamento e tabella e il valore di RequireInfrastructureEncryption.</span><span class="sxs-lookup"><span data-stu-id="de108-127">Then get the Storage account properties, and view the encryption keytype of Queue and Table Service, and RequireInfrastructureEncryption value.</span></span>

### <span data-ttu-id="de108-128">Esempio 9: creare l'account MinimumTlsVersion e AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="de108-128">Example 9: Create account MinimumTlsVersion  and AllowBlobPublicAccess</span></span>
```
PS C:\> $account = New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2 -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False
```

<span data-ttu-id="de108-129">Il comando Crea account con MinimumTlsVersion e AllowBlobPublicAccess e quindi Mostra le due proprietà dell'account creato</span><span class="sxs-lookup"><span data-stu-id="de108-129">The command create account with MinimumTlsVersion  and AllowBlobPublicAccess, and then show the the 2 properties of the created account</span></span> 

## <span data-ttu-id="de108-130">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="de108-130">PARAMETERS</span></span>

### <span data-ttu-id="de108-131">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="de108-131">-AccessTier</span></span>
<span data-ttu-id="de108-132">Specifica il livello di accesso dell'account di archiviazione creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de108-132">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="de108-133">I valori accettabili per questo parametro sono: caldo e freddo.</span><span class="sxs-lookup"><span data-stu-id="de108-133">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="de108-134">Se specifichi un valore di BlobStorage per il parametro *Kind* , devi specificare un valore per il parametro *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="de108-134">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="de108-135">Se specifichi un valore di spazio di archiviazione per questo parametro di *tipo* , non specificare il parametro *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="de108-135">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="de108-136">-ActiveDirectoryAzureStorageSid</span><span class="sxs-lookup"><span data-stu-id="de108-136">-ActiveDirectoryAzureStorageSid</span></span>
<span data-ttu-id="de108-137">Specifica l'identificatore di sicurezza (SID) per lo spazio di archiviazione Azure.</span><span class="sxs-lookup"><span data-stu-id="de108-137">Specifies the security identifier (SID) for Azure Storage.</span></span> <span data-ttu-id="de108-138">Questo parametro deve essere impostato quando-EnableActiveDirectoryDomainServicesForFile è impostato su true.</span><span class="sxs-lookup"><span data-stu-id="de108-138">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="de108-139">-ActiveDirectoryDomainGuid</span><span class="sxs-lookup"><span data-stu-id="de108-139">-ActiveDirectoryDomainGuid</span></span>
<span data-ttu-id="de108-140">Specifica il GUID del dominio.</span><span class="sxs-lookup"><span data-stu-id="de108-140">Specifies the domain GUID.</span></span> <span data-ttu-id="de108-141">Questo parametro deve essere impostato quando-EnableActiveDirectoryDomainServicesForFile è impostato su true.</span><span class="sxs-lookup"><span data-stu-id="de108-141">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="de108-142">-ActiveDirectoryDomainName</span><span class="sxs-lookup"><span data-stu-id="de108-142">-ActiveDirectoryDomainName</span></span>
<span data-ttu-id="de108-143">Specifica il dominio primario per cui è autorevole il server DNS AD.</span><span class="sxs-lookup"><span data-stu-id="de108-143">Specifies the primary domain that the AD DNS server is authoritative for.</span></span> <span data-ttu-id="de108-144">Questo parametro deve essere impostato quando-EnableActiveDirectoryDomainServicesForFile è impostato su true.</span><span class="sxs-lookup"><span data-stu-id="de108-144">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="de108-145">-ActiveDirectoryDomainSid</span><span class="sxs-lookup"><span data-stu-id="de108-145">-ActiveDirectoryDomainSid</span></span>
<span data-ttu-id="de108-146">Specifica l'identificatore di sicurezza (SID).</span><span class="sxs-lookup"><span data-stu-id="de108-146">Specifies the security identifier (SID).</span></span> <span data-ttu-id="de108-147">Questo parametro deve essere impostato quando-EnableActiveDirectoryDomainServicesForFile è impostato su true.</span><span class="sxs-lookup"><span data-stu-id="de108-147">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="de108-148">-ActiveDirectoryForestName</span><span class="sxs-lookup"><span data-stu-id="de108-148">-ActiveDirectoryForestName</span></span>
<span data-ttu-id="de108-149">Specifica la foresta di Active Directory da ottenere.</span><span class="sxs-lookup"><span data-stu-id="de108-149">Specifies the Active Directory forest to get.</span></span> <span data-ttu-id="de108-150">Questo parametro deve essere impostato quando-EnableActiveDirectoryDomainServicesForFile è impostato su true.</span><span class="sxs-lookup"><span data-stu-id="de108-150">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="de108-151">-ActiveDirectoryNetBiosDomainName</span><span class="sxs-lookup"><span data-stu-id="de108-151">-ActiveDirectoryNetBiosDomainName</span></span>
<span data-ttu-id="de108-152">Specifica il nome di dominio NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="de108-152">Specifies the NetBIOS domain name.</span></span> <span data-ttu-id="de108-153">Questo parametro deve essere impostato quando-EnableActiveDirectoryDomainServicesForFile è impostato su true.</span><span class="sxs-lookup"><span data-stu-id="de108-153">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="de108-154">-AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="de108-154">-AllowBlobPublicAccess</span></span>
<span data-ttu-id="de108-155">Consentire l'accesso pubblico a tutti i BLOB o contenitori nell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="de108-155">Allow public access to all blobs or containers in the storage account.</span></span> <span data-ttu-id="de108-156">L'interpretazione predefinita è true per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="de108-156">The default interpretation is true for this property.</span></span>

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

### <span data-ttu-id="de108-157">-AsJob</span><span class="sxs-lookup"><span data-stu-id="de108-157">-AsJob</span></span>
<span data-ttu-id="de108-158">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="de108-158">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="de108-159">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="de108-159">-AssignIdentity</span></span>
<span data-ttu-id="de108-160">Genera e assegna una nuova identità dell'account di archiviazione per l'account di archiviazione per l'uso con i servizi di gestione delle chiavi, ad esempio Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="de108-160">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="de108-161">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="de108-161">-CustomDomainName</span></span>
<span data-ttu-id="de108-162">Specifica il nome del dominio personalizzato dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="de108-162">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="de108-163">Il valore predefinito è lo spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="de108-163">The default value is Storage.</span></span>

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

### <span data-ttu-id="de108-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de108-164">-DefaultProfile</span></span>
<span data-ttu-id="de108-165">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="de108-165">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de108-166">-EnableActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="de108-166">-EnableActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="de108-167">Abilitare l'autenticazione dei servizi di dominio Active Directory di Azure per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="de108-167">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="de108-168">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="de108-168">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="de108-169">Abilitare Azure files Azure Active Directory Domain Service Authentication per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="de108-169">Enable Azure Files Azure Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="de108-170">-EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="de108-170">-EnableHierarchicalNamespace</span></span>
<span data-ttu-id="de108-171">Indica se l'account di archiviazione Abilita lo spazio dei nomi gerarchico.</span><span class="sxs-lookup"><span data-stu-id="de108-171">Indicates whether or not the Storage account enables Hierarchical Namespace.</span></span>

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

### <span data-ttu-id="de108-172">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="de108-172">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="de108-173">Indica se l'account di archiviazione Abilita o meno solo il traffico HTTPS.</span><span class="sxs-lookup"><span data-stu-id="de108-173">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="de108-174">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="de108-174">-EnableLargeFileShare</span></span>
<span data-ttu-id="de108-175">Indica se l'account di archiviazione può supportare condivisioni di file di grandi dimensioni con più di 5 capacità TiB.</span><span class="sxs-lookup"><span data-stu-id="de108-175">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="de108-176">Quando l'account è abilitato, la caratteristica non può essere disabilitata.</span><span class="sxs-lookup"><span data-stu-id="de108-176">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="de108-177">Attualmente supportato solo per i tipi di replica LRS e ZRS, quindi le conversioni degli account con gli account Geo-ridondanti non sarebbero possibili.</span><span class="sxs-lookup"><span data-stu-id="de108-177">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="de108-178">Altre informazioni in https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="de108-178">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="de108-179">-EncryptionKeyTypeForQueue</span><span class="sxs-lookup"><span data-stu-id="de108-179">-EncryptionKeyTypeForQueue</span></span>
<span data-ttu-id="de108-180">Impostare il tipo di crittografia per la coda.</span><span class="sxs-lookup"><span data-stu-id="de108-180">Set the Encryption KeyType for Queue.</span></span> <span data-ttu-id="de108-181">Il valore predefinito è Service.</span><span class="sxs-lookup"><span data-stu-id="de108-181">The default value is Service.</span></span>
<span data-ttu-id="de108-182">-Account: la coda verrà crittografata con la chiave di crittografia con ambito account.</span><span class="sxs-lookup"><span data-stu-id="de108-182">-Account: Queue will be encrypted with account-scoped encryption key.</span></span> <span data-ttu-id="de108-183">-Servizio: la coda verrà sempre crittografata con Service-Managed tasti.</span><span class="sxs-lookup"><span data-stu-id="de108-183">-Service: Queue will always be encrypted with Service-Managed keys.</span></span> 

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

### <span data-ttu-id="de108-184">-EncryptionKeyTypeForTable</span><span class="sxs-lookup"><span data-stu-id="de108-184">-EncryptionKeyTypeForTable</span></span>
<span data-ttu-id="de108-185">Impostare il tipo di crittografia per la tabella.</span><span class="sxs-lookup"><span data-stu-id="de108-185">Set the Encryption KeyType for Table.</span></span> <span data-ttu-id="de108-186">Il valore predefinito è Service.</span><span class="sxs-lookup"><span data-stu-id="de108-186">The default value is Service.</span></span>
- <span data-ttu-id="de108-187">Account: la tabella verrà crittografata con la chiave di crittografia con ambito account.</span><span class="sxs-lookup"><span data-stu-id="de108-187">Account: Table will be encrypted with account-scoped encryption key.</span></span> 
- <span data-ttu-id="de108-188">Service: la tabella verrà sempre crittografata con Service-Managed tasti.</span><span class="sxs-lookup"><span data-stu-id="de108-188">Service: Table will always be encrypted with Service-Managed keys.</span></span> 

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

### <span data-ttu-id="de108-189">-Tipo</span><span class="sxs-lookup"><span data-stu-id="de108-189">-Kind</span></span>
<span data-ttu-id="de108-190">Specifica il tipo di account di archiviazione creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de108-190">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="de108-191">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="de108-191">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="de108-192">Archiviazione.</span><span class="sxs-lookup"><span data-stu-id="de108-192">Storage.</span></span> <span data-ttu-id="de108-193">Account di archiviazione di uso generale che supporta l'archiviazione di BLOB, tabelle, code, file e dischi.</span><span class="sxs-lookup"><span data-stu-id="de108-193">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="de108-194">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="de108-194">StorageV2.</span></span> <span data-ttu-id="de108-195">Account di archiviazione per usi generali versione 2 (GPv2) che supporta BLOB, tabelle, code, file e dischi, con funzionalità avanzate come il livello dei dati.</span><span class="sxs-lookup"><span data-stu-id="de108-195">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="de108-196">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="de108-196">BlobStorage.</span></span> <span data-ttu-id="de108-197">Account di archiviazione BLOB che supporta l'archiviazione solo di BLOB.</span><span class="sxs-lookup"><span data-stu-id="de108-197">Blob Storage account which supports storage of Blobs only.</span></span>
- <span data-ttu-id="de108-198">BlockBlobStorage.</span><span class="sxs-lookup"><span data-stu-id="de108-198">BlockBlobStorage.</span></span> <span data-ttu-id="de108-199">Bloccare l'account di archiviazione BLOB che supporta l'archiviazione solo dei BLOB di blocco.</span><span class="sxs-lookup"><span data-stu-id="de108-199">Block Blob Storage account which supports storage of Block Blobs only.</span></span>
- <span data-ttu-id="de108-200">FileStorage.</span><span class="sxs-lookup"><span data-stu-id="de108-200">FileStorage.</span></span> <span data-ttu-id="de108-201">Account di archiviazione file che supporta solo l'archiviazione dei file.</span><span class="sxs-lookup"><span data-stu-id="de108-201">File Storage account which supports storage of Files only.</span></span>
<span data-ttu-id="de108-202">Il valore predefinito è StorageV2.</span><span class="sxs-lookup"><span data-stu-id="de108-202">The default value is StorageV2.</span></span>

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

### <span data-ttu-id="de108-203">-Posizione</span><span class="sxs-lookup"><span data-stu-id="de108-203">-Location</span></span>
<span data-ttu-id="de108-204">Specifica la posizione dell'account di archiviazione da creare.</span><span class="sxs-lookup"><span data-stu-id="de108-204">Specifies the location of the Storage account to create.</span></span>

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

### <span data-ttu-id="de108-205">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="de108-205">-MinimumTlsVersion</span></span>
<span data-ttu-id="de108-206">La versione minima di TLS consentita per le richieste di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="de108-206">The minimum TLS version to be permitted on requests to storage.</span></span> <span data-ttu-id="de108-207">L'interpretazione predefinita è TLS 1,0 per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="de108-207">The default interpretation is TLS 1.0 for this property.</span></span>

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

### <span data-ttu-id="de108-208">-Nome</span><span class="sxs-lookup"><span data-stu-id="de108-208">-Name</span></span>
<span data-ttu-id="de108-209">Specifica il nome dell'account di archiviazione da creare.</span><span class="sxs-lookup"><span data-stu-id="de108-209">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="de108-210">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="de108-210">-NetworkRuleSet</span></span>
<span data-ttu-id="de108-211">NetworkRuleSet viene usato per definire un set di regole di configurazione per i firewall e le reti virtuali, nonché per impostare i valori per le proprietà di rete, ad esempio i servizi autorizzati ad aggirare le regole e come gestire le richieste che non corrispondono a nessuna delle regole definite.</span><span class="sxs-lookup"><span data-stu-id="de108-211">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="de108-212">-RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="de108-212">-RequireInfrastructureEncryption</span></span>
<span data-ttu-id="de108-213">Il servizio applica un livello secondario di crittografia con le chiavi gestite della piattaforma per i dati a riposo.</span><span class="sxs-lookup"><span data-stu-id="de108-213">The service will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>

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

### <span data-ttu-id="de108-214">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de108-214">-ResourceGroupName</span></span>
<span data-ttu-id="de108-215">Specifica il nome del gruppo di risorse in cui aggiungere l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="de108-215">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="de108-216">-SkuName</span><span class="sxs-lookup"><span data-stu-id="de108-216">-SkuName</span></span>
<span data-ttu-id="de108-217">Specifica il nome SKU dell'account di archiviazione creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de108-217">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="de108-218">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="de108-218">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="de108-219">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="de108-219">Standard_LRS.</span></span> <span data-ttu-id="de108-220">Spazio di archiviazione locale ridondante.</span><span class="sxs-lookup"><span data-stu-id="de108-220">Locally-redundant storage.</span></span>
- <span data-ttu-id="de108-221">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="de108-221">Standard_ZRS.</span></span> <span data-ttu-id="de108-222">Area-archiviazione ridondante.</span><span class="sxs-lookup"><span data-stu-id="de108-222">Zone-redundant storage.</span></span>
- <span data-ttu-id="de108-223">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="de108-223">Standard_GRS.</span></span> <span data-ttu-id="de108-224">Spazio di archiviazione Geo-ridondante.</span><span class="sxs-lookup"><span data-stu-id="de108-224">Geo-redundant storage.</span></span>
- <span data-ttu-id="de108-225">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="de108-225">Standard_RAGRS.</span></span> <span data-ttu-id="de108-226">Accesso in lettura archiviazione Geo-ridondante.</span><span class="sxs-lookup"><span data-stu-id="de108-226">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="de108-227">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="de108-227">Premium_LRS.</span></span> <span data-ttu-id="de108-228">Spazio di archiviazione locale ridondante Premium.</span><span class="sxs-lookup"><span data-stu-id="de108-228">Premium locally-redundant storage.</span></span>
- <span data-ttu-id="de108-229">Premium_ZRS.</span><span class="sxs-lookup"><span data-stu-id="de108-229">Premium_ZRS.</span></span> <span data-ttu-id="de108-230">Zona Premium-spazio di archiviazione ridondante.</span><span class="sxs-lookup"><span data-stu-id="de108-230">Premium zone-redundant storage.</span></span>
- <span data-ttu-id="de108-231">Standard_GZRS-area geo-ridondante-spazio di archiviazione ridondante.</span><span class="sxs-lookup"><span data-stu-id="de108-231">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="de108-232">Standard_RAGZRS-Read Access area geo-ridondante-archiviazione ridondante.</span><span class="sxs-lookup"><span data-stu-id="de108-232">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>

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

### <span data-ttu-id="de108-233">-Tag</span><span class="sxs-lookup"><span data-stu-id="de108-233">-Tag</span></span>
<span data-ttu-id="de108-234">Coppie chiave-valore nella forma di una tabella hash impostata come tag nel server.</span><span class="sxs-lookup"><span data-stu-id="de108-234">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="de108-235">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="de108-235">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="de108-236">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="de108-236">-UseSubDomain</span></span>
<span data-ttu-id="de108-237">Indica se abilitare la convalida CName indiretta.</span><span class="sxs-lookup"><span data-stu-id="de108-237">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="de108-238">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de108-238">CommonParameters</span></span>
<span data-ttu-id="de108-239">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de108-239">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de108-240">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de108-240">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de108-241">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="de108-241">INPUTS</span></span>

### <span data-ttu-id="de108-242">System. String</span><span class="sxs-lookup"><span data-stu-id="de108-242">System.String</span></span>

## <span data-ttu-id="de108-243">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="de108-243">OUTPUTS</span></span>

### <span data-ttu-id="de108-244">Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="de108-244">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="de108-245">Note</span><span class="sxs-lookup"><span data-stu-id="de108-245">NOTES</span></span>

## <span data-ttu-id="de108-246">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="de108-246">RELATED LINKS</span></span>

[<span data-ttu-id="de108-247">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="de108-247">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="de108-248">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="de108-248">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="de108-249">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="de108-249">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)
