---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: c88e56a485f9e42daf229667ab4c07d7a7464578
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021104"
---
# <span data-ttu-id="52fdc-101">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="52fdc-101">New-AzStorageAccount</span></span>

## <span data-ttu-id="52fdc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="52fdc-102">SYNOPSIS</span></span>
<span data-ttu-id="52fdc-103">Crea un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="52fdc-103">Creates a Storage account.</span></span>

## <span data-ttu-id="52fdc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="52fdc-104">SYNTAX</span></span>

```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>]
 [-EnableLargeFileShare] [-AsJob] [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52fdc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="52fdc-105">DESCRIPTION</span></span>
<span data-ttu-id="52fdc-106">Il cmdlet **New-AzStorageAccount** crea un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="52fdc-106">The **New-AzStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="52fdc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="52fdc-107">EXAMPLES</span></span>

### <span data-ttu-id="52fdc-108">Esempio 1: creare un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="52fdc-108">Example 1: Create a Storage account</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="52fdc-109">Questo comando crea un account di archiviazione per il nome del gruppo di risorse MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="52fdc-109">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="52fdc-110">Esempio 2: creare un account di archiviazione BLOB con BlobStorage Kind e Hot AccessTier</span><span class="sxs-lookup"><span data-stu-id="52fdc-110">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="52fdc-111">Questo comando crea un account di archiviazione BLOB con BlobStorage Kind e Hot AccessTier</span><span class="sxs-lookup"><span data-stu-id="52fdc-111">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="52fdc-112">Esempio 3: creare un account di archiviazione con Kind StorageV2 e generare e assegnare un'identità per il Vault di Azure.</span><span class="sxs-lookup"><span data-stu-id="52fdc-112">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="52fdc-113">Questo comando crea un account di archiviazione con Kind StorageV2.</span><span class="sxs-lookup"><span data-stu-id="52fdc-113">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="52fdc-114">Viene inoltre generata e assegnata un'identità che può essere usata per gestire le chiavi dell'account tramite Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="52fdc-114">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="52fdc-115">Esempio 4: creare un account di archiviazione con NetworkRuleSet da JSON</span><span class="sxs-lookup"><span data-stu-id="52fdc-115">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="52fdc-116">Questo comando crea un account di archiviazione con proprietà NetworkRuleSet da JSON</span><span class="sxs-lookup"><span data-stu-id="52fdc-116">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

### <span data-ttu-id="52fdc-117">Esempio 5: creare un account di archiviazione con lo spazio dei nomi gerarchico abilitato.</span><span class="sxs-lookup"><span data-stu-id="52fdc-117">Example 5: Create a Storage account with Hierarchical Namespace enabled.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

<span data-ttu-id="52fdc-118">Questo comando crea un account di archiviazione con lo spazio dei nomi gerarchico abilitato.</span><span class="sxs-lookup"><span data-stu-id="52fdc-118">This command creates a Storage account with Hierarchical Namespace enabled.</span></span>

### <span data-ttu-id="52fdc-119">Esempio 6: creare un account di archiviazione con l'autenticazione dei file di Azure AAD e abilitare la condivisione di file di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="52fdc-119">Example 6: Create a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true -EnableLargeFileShare
```

<span data-ttu-id="52fdc-120">Questo comando crea un account di archiviazione con l'autenticazione dei file di Azure AAD e consente la condivisione di file di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="52fdc-120">This command creates a Storage account with Azure Files AAD DS Authentication, and enable large file share..</span></span>

### <span data-ttu-id="52fdc-121">Esempio 8: creare un account di archiviazione con coda e servizio di tabella usare la chiave di crittografia con ambito account.</span><span class="sxs-lookup"><span data-stu-id="52fdc-121">Example 8: Create a Storage account with Queue and Table Service use account-scoped encryption key.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EncryptionKeyTypeForTable Account -EncryptionKeyTypeForQueue Account

PS C:\>$account = get-AzStorageAccount -ResourceGroupName $rgname -StorageAccountName $accountName

PS C:\>$account.Encryption.Services.Queue

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account

PS C:\>$account.Encryption.Services.Table

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account
```

<span data-ttu-id="52fdc-122">Questo comando crea un account di archiviazione con coda e servizio tabella usare la chiave di crittografia con ambito account, quindi Queue e Table useranno la stessa chiave di crittografia con BLOB e il servizio file.</span><span class="sxs-lookup"><span data-stu-id="52fdc-122">This command creates a Storage account with Queue and Table Service use account-scoped encryption key, so Queue and Table will use same encryption key with Blob and File service.</span></span> <span data-ttu-id="52fdc-123">Ottieni quindi le proprietà dell'account di archiviazione e visualizza il tipo di crittografia del servizio di Accodamento e tabella.</span><span class="sxs-lookup"><span data-stu-id="52fdc-123">Then get the Storage account properties, and view the encryption keytype of Queue and Table Service.</span></span>

## <span data-ttu-id="52fdc-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="52fdc-124">PARAMETERS</span></span>

### <span data-ttu-id="52fdc-125">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="52fdc-125">-AccessTier</span></span>
<span data-ttu-id="52fdc-126">Specifica il livello di accesso dell'account di archiviazione creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52fdc-126">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="52fdc-127">I valori accettabili per questo parametro sono: caldo e freddo.</span><span class="sxs-lookup"><span data-stu-id="52fdc-127">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="52fdc-128">Se specifichi un valore di BlobStorage per il parametro *Kind* , devi specificare un valore per il parametro *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="52fdc-128">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="52fdc-129">Se specifichi un valore di spazio di archiviazione per questo parametro di *tipo* , non specificare il parametro *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="52fdc-129">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="52fdc-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="52fdc-130">-AsJob</span></span>
<span data-ttu-id="52fdc-131">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="52fdc-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="52fdc-132">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="52fdc-132">-AssignIdentity</span></span>
<span data-ttu-id="52fdc-133">Genera e assegna una nuova identità dell'account di archiviazione per l'account di archiviazione per l'uso con i servizi di gestione delle chiavi, ad esempio Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="52fdc-133">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="52fdc-134">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="52fdc-134">-CustomDomainName</span></span>
<span data-ttu-id="52fdc-135">Specifica il nome del dominio personalizzato dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="52fdc-135">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="52fdc-136">Il valore predefinito è lo spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="52fdc-136">The default value is Storage.</span></span>

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

### <span data-ttu-id="52fdc-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52fdc-137">-DefaultProfile</span></span>
<span data-ttu-id="52fdc-138">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="52fdc-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52fdc-139">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="52fdc-139">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="52fdc-140">Abilitare Azure files Azure Active Directory Domain Service Authentication per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="52fdc-140">Enable Azure Files Azure Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="52fdc-141">-EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="52fdc-141">-EnableHierarchicalNamespace</span></span>
<span data-ttu-id="52fdc-142">Indica se l'account di archiviazione Abilita lo spazio dei nomi gerarchico.</span><span class="sxs-lookup"><span data-stu-id="52fdc-142">Indicates whether or not the Storage account enables Hierarchical Namespace.</span></span>

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

### <span data-ttu-id="52fdc-143">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="52fdc-143">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="52fdc-144">Indica se l'account di archiviazione Abilita o meno solo il traffico HTTPS.</span><span class="sxs-lookup"><span data-stu-id="52fdc-144">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="52fdc-145">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="52fdc-145">-EnableLargeFileShare</span></span>
<span data-ttu-id="52fdc-146">Indica se l'account di archiviazione può supportare condivisioni di file di grandi dimensioni con più di 5 capacità TiB.</span><span class="sxs-lookup"><span data-stu-id="52fdc-146">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="52fdc-147">Quando l'account è abilitato, la caratteristica non può essere disabilitata.</span><span class="sxs-lookup"><span data-stu-id="52fdc-147">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="52fdc-148">Attualmente supportato solo per i tipi di replica LRS e ZRS, quindi le conversioni degli account con gli account Geo-ridondanti non sarebbero possibili.</span><span class="sxs-lookup"><span data-stu-id="52fdc-148">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="52fdc-149">Altre informazioni in https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="52fdc-149">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="52fdc-150">-EncryptionKeyTypeForQueue</span><span class="sxs-lookup"><span data-stu-id="52fdc-150">-EncryptionKeyTypeForQueue</span></span>
<span data-ttu-id="52fdc-151">Impostare il tipo di crittografia per la coda.</span><span class="sxs-lookup"><span data-stu-id="52fdc-151">Set the Encryption KeyType for Queue.</span></span> <span data-ttu-id="52fdc-152">Il valore predefinito è Service.</span><span class="sxs-lookup"><span data-stu-id="52fdc-152">The default value is Service.</span></span>
<span data-ttu-id="52fdc-153">-Account: la coda verrà crittografata con la chiave di crittografia con ambito account.</span><span class="sxs-lookup"><span data-stu-id="52fdc-153">-Account: Queue will be encrypted with account-scoped encryption key.</span></span> <span data-ttu-id="52fdc-154">-Servizio: la coda verrà sempre crittografata con Service-Managed tasti.</span><span class="sxs-lookup"><span data-stu-id="52fdc-154">-Service: Queue will always be encrypted with Service-Managed keys.</span></span> 

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

### <span data-ttu-id="52fdc-155">-EncryptionKeyTypeForTable</span><span class="sxs-lookup"><span data-stu-id="52fdc-155">-EncryptionKeyTypeForTable</span></span>
<span data-ttu-id="52fdc-156">Impostare il tipo di crittografia per la tabella.</span><span class="sxs-lookup"><span data-stu-id="52fdc-156">Set the Encryption KeyType for Table.</span></span> <span data-ttu-id="52fdc-157">Il valore predefinito è Service.</span><span class="sxs-lookup"><span data-stu-id="52fdc-157">The default value is Service.</span></span>
- <span data-ttu-id="52fdc-158">Account: la tabella verrà crittografata con la chiave di crittografia con ambito account.</span><span class="sxs-lookup"><span data-stu-id="52fdc-158">Account: Table will be encrypted with account-scoped encryption key.</span></span> 
- <span data-ttu-id="52fdc-159">Service: la tabella verrà sempre crittografata con Service-Managed tasti.</span><span class="sxs-lookup"><span data-stu-id="52fdc-159">Service: Table will always be encrypted with Service-Managed keys.</span></span> 

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

### <span data-ttu-id="52fdc-160">-Tipo</span><span class="sxs-lookup"><span data-stu-id="52fdc-160">-Kind</span></span>
<span data-ttu-id="52fdc-161">Specifica il tipo di account di archiviazione creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52fdc-161">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="52fdc-162">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="52fdc-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="52fdc-163">Archiviazione.</span><span class="sxs-lookup"><span data-stu-id="52fdc-163">Storage.</span></span> <span data-ttu-id="52fdc-164">Account di archiviazione di uso generale che supporta l'archiviazione di BLOB, tabelle, code, file e dischi.</span><span class="sxs-lookup"><span data-stu-id="52fdc-164">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="52fdc-165">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="52fdc-165">StorageV2.</span></span> <span data-ttu-id="52fdc-166">Account di archiviazione per usi generali versione 2 (GPv2) che supporta BLOB, tabelle, code, file e dischi, con funzionalità avanzate come il livello dei dati.</span><span class="sxs-lookup"><span data-stu-id="52fdc-166">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="52fdc-167">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="52fdc-167">BlobStorage.</span></span> <span data-ttu-id="52fdc-168">Account di archiviazione BLOB che supporta l'archiviazione solo di BLOB.</span><span class="sxs-lookup"><span data-stu-id="52fdc-168">Blob Storage account which supports storage of Blobs only.</span></span>
- <span data-ttu-id="52fdc-169">BlockBlobStorage.</span><span class="sxs-lookup"><span data-stu-id="52fdc-169">BlockBlobStorage.</span></span> <span data-ttu-id="52fdc-170">Bloccare l'account di archiviazione BLOB che supporta l'archiviazione solo dei BLOB di blocco.</span><span class="sxs-lookup"><span data-stu-id="52fdc-170">Block Blob Storage account which supports storage of Block Blobs only.</span></span>
- <span data-ttu-id="52fdc-171">FileStorage.</span><span class="sxs-lookup"><span data-stu-id="52fdc-171">FileStorage.</span></span> <span data-ttu-id="52fdc-172">Account di archiviazione file che supporta solo l'archiviazione dei file.</span><span class="sxs-lookup"><span data-stu-id="52fdc-172">File Storage account which supports storage of Files only.</span></span>
<span data-ttu-id="52fdc-173">Il valore predefinito è StorageV2.</span><span class="sxs-lookup"><span data-stu-id="52fdc-173">The default value is StorageV2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Storage, StorageV2, BlobStorage, BlockBlobStorage, FileStorage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52fdc-174">-Posizione</span><span class="sxs-lookup"><span data-stu-id="52fdc-174">-Location</span></span>
<span data-ttu-id="52fdc-175">Specifica la posizione dell'account di archiviazione da creare.</span><span class="sxs-lookup"><span data-stu-id="52fdc-175">Specifies the location of the Storage account to create.</span></span>

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

### <span data-ttu-id="52fdc-176">-Nome</span><span class="sxs-lookup"><span data-stu-id="52fdc-176">-Name</span></span>
<span data-ttu-id="52fdc-177">Specifica il nome dell'account di archiviazione da creare.</span><span class="sxs-lookup"><span data-stu-id="52fdc-177">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="52fdc-178">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="52fdc-178">-NetworkRuleSet</span></span>
<span data-ttu-id="52fdc-179">NetworkRuleSet viene usato per definire un set di regole di configurazione per i firewall e le reti virtuali, nonché per impostare i valori per le proprietà di rete, ad esempio i servizi autorizzati ad aggirare le regole e come gestire le richieste che non corrispondono a nessuna delle regole definite.</span><span class="sxs-lookup"><span data-stu-id="52fdc-179">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="52fdc-180">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52fdc-180">-ResourceGroupName</span></span>
<span data-ttu-id="52fdc-181">Specifica il nome del gruppo di risorse in cui aggiungere l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="52fdc-181">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="52fdc-182">-SkuName</span><span class="sxs-lookup"><span data-stu-id="52fdc-182">-SkuName</span></span>
<span data-ttu-id="52fdc-183">Specifica il nome SKU dell'account di archiviazione creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52fdc-183">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="52fdc-184">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="52fdc-184">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="52fdc-185">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="52fdc-185">Standard_LRS.</span></span> <span data-ttu-id="52fdc-186">Spazio di archiviazione locale ridondante.</span><span class="sxs-lookup"><span data-stu-id="52fdc-186">Locally-redundant storage.</span></span>
- <span data-ttu-id="52fdc-187">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="52fdc-187">Standard_ZRS.</span></span> <span data-ttu-id="52fdc-188">Area-archiviazione ridondante.</span><span class="sxs-lookup"><span data-stu-id="52fdc-188">Zone-redundant storage.</span></span>
- <span data-ttu-id="52fdc-189">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="52fdc-189">Standard_GRS.</span></span> <span data-ttu-id="52fdc-190">Spazio di archiviazione Geo-ridondante.</span><span class="sxs-lookup"><span data-stu-id="52fdc-190">Geo-redundant storage.</span></span>
- <span data-ttu-id="52fdc-191">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="52fdc-191">Standard_RAGRS.</span></span> <span data-ttu-id="52fdc-192">Accesso in lettura archiviazione Geo-ridondante.</span><span class="sxs-lookup"><span data-stu-id="52fdc-192">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="52fdc-193">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="52fdc-193">Premium_LRS.</span></span> <span data-ttu-id="52fdc-194">Spazio di archiviazione locale ridondante Premium.</span><span class="sxs-lookup"><span data-stu-id="52fdc-194">Premium locally-redundant storage.</span></span>
- <span data-ttu-id="52fdc-195">Premium_ZRS.</span><span class="sxs-lookup"><span data-stu-id="52fdc-195">Premium_ZRS.</span></span> <span data-ttu-id="52fdc-196">Zona Premium-spazio di archiviazione ridondante.</span><span class="sxs-lookup"><span data-stu-id="52fdc-196">Premium zone-redundant storage.</span></span>
- <span data-ttu-id="52fdc-197">Standard_GZRS-area geo-ridondante-spazio di archiviazione ridondante.</span><span class="sxs-lookup"><span data-stu-id="52fdc-197">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="52fdc-198">Standard_RAGZRS-Read Access area geo-ridondante-archiviazione ridondante.</span><span class="sxs-lookup"><span data-stu-id="52fdc-198">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>

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

### <span data-ttu-id="52fdc-199">-Tag</span><span class="sxs-lookup"><span data-stu-id="52fdc-199">-Tag</span></span>
<span data-ttu-id="52fdc-200">Coppie chiave-valore nella forma di una tabella hash impostata come tag nel server.</span><span class="sxs-lookup"><span data-stu-id="52fdc-200">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="52fdc-201">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="52fdc-201">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="52fdc-202">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="52fdc-202">-UseSubDomain</span></span>
<span data-ttu-id="52fdc-203">Indica se abilitare la convalida CName indiretta.</span><span class="sxs-lookup"><span data-stu-id="52fdc-203">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="52fdc-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52fdc-204">CommonParameters</span></span>
<span data-ttu-id="52fdc-205">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52fdc-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52fdc-206">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52fdc-206">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52fdc-207">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="52fdc-207">INPUTS</span></span>

### <span data-ttu-id="52fdc-208">System. String</span><span class="sxs-lookup"><span data-stu-id="52fdc-208">System.String</span></span>

## <span data-ttu-id="52fdc-209">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="52fdc-209">OUTPUTS</span></span>

### <span data-ttu-id="52fdc-210">Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="52fdc-210">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="52fdc-211">Note</span><span class="sxs-lookup"><span data-stu-id="52fdc-211">NOTES</span></span>

## <span data-ttu-id="52fdc-212">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="52fdc-212">RELATED LINKS</span></span>

[<span data-ttu-id="52fdc-213">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="52fdc-213">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="52fdc-214">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="52fdc-214">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="52fdc-215">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="52fdc-215">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)
