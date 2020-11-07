---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: c8ac7139c44adc8bd748eef9a6c762a71c3a777f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93858082"
---
# <span data-ttu-id="35fb4-101">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="35fb4-101">New-AzStorageAccount</span></span>

## <span data-ttu-id="35fb4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="35fb4-102">SYNOPSIS</span></span>
<span data-ttu-id="35fb4-103">Crea un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="35fb4-103">Creates a Storage account.</span></span>

## <span data-ttu-id="35fb4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="35fb4-104">SYNTAX</span></span>

```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35fb4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="35fb4-105">DESCRIPTION</span></span>
<span data-ttu-id="35fb4-106">Il cmdlet **New-AzStorageAccount** crea un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="35fb4-106">The **New-AzStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="35fb4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="35fb4-107">EXAMPLES</span></span>

### <span data-ttu-id="35fb4-108">Esempio 1: creare un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="35fb4-108">Example 1: Create a Storage account</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="35fb4-109">Questo comando crea un account di archiviazione per il nome del gruppo di risorse MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="35fb4-109">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="35fb4-110">Esempio 2: creare un account di archiviazione BLOB con BlobStorage Kind e Hot AccessTier</span><span class="sxs-lookup"><span data-stu-id="35fb4-110">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="35fb4-111">Questo comando crea un account di archiviazione BLOB con BlobStorage Kind e Hot AccessTier</span><span class="sxs-lookup"><span data-stu-id="35fb4-111">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="35fb4-112">Esempio 3: creare un account di archiviazione con Kind StorageV2 e generare e assegnare un'identità per il Vault di Azure.</span><span class="sxs-lookup"><span data-stu-id="35fb4-112">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="35fb4-113">Questo comando crea un account di archiviazione con Kind StorageV2.</span><span class="sxs-lookup"><span data-stu-id="35fb4-113">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="35fb4-114">Viene inoltre generata e assegnata un'identità che può essere usata per gestire le chiavi dell'account tramite Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="35fb4-114">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="35fb4-115">Esempio 4: creare un account di archiviazione con NetworkRuleSet da JSON</span><span class="sxs-lookup"><span data-stu-id="35fb4-115">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="35fb4-116">Questo comando crea un account di archiviazione con proprietà NetworkRuleSet da JSON</span><span class="sxs-lookup"><span data-stu-id="35fb4-116">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

### <span data-ttu-id="35fb4-117">Esempio 5: creare un account di archiviazione con lo spazio dei nomi gerarchico abilitato.</span><span class="sxs-lookup"><span data-stu-id="35fb4-117">Example 5: Create a Storage account with Hierarchical Namespace enabled.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

<span data-ttu-id="35fb4-118">Questo comando crea un account di archiviazione con lo spazio dei nomi gerarchico abilitato.</span><span class="sxs-lookup"><span data-stu-id="35fb4-118">This command creates a Storage account with Hierarchical Namespace enabled.</span></span>

### <span data-ttu-id="35fb4-119">Esempio 6: creare un account di archiviazione con l'autenticazione di Azure file AAD.</span><span class="sxs-lookup"><span data-stu-id="35fb4-119">Example 6: Create a Storage account with Azure Files AAD DS Authentication.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true
```

<span data-ttu-id="35fb4-120">Questo comando crea un account di archiviazione con l'autenticazione di Azure file AAD.</span><span class="sxs-lookup"><span data-stu-id="35fb4-120">This command creates a Storage account with Azure Files AAD DS Authentication.</span></span>

## <span data-ttu-id="35fb4-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="35fb4-121">PARAMETERS</span></span>

### <span data-ttu-id="35fb4-122">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="35fb4-122">-AccessTier</span></span>
<span data-ttu-id="35fb4-123">Specifica il livello di accesso dell'account di archiviazione creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35fb4-123">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="35fb4-124">I valori accettabili per questo parametro sono: caldo e freddo.</span><span class="sxs-lookup"><span data-stu-id="35fb4-124">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="35fb4-125">Se specifichi un valore di BlobStorage per il parametro *Kind* , devi specificare un valore per il parametro *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="35fb4-125">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="35fb4-126">Se specifichi un valore di spazio di archiviazione per questo parametro di *tipo* , non specificare il parametro *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="35fb4-126">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="35fb4-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35fb4-127">-AsJob</span></span>
<span data-ttu-id="35fb4-128">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="35fb4-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="35fb4-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="35fb4-129">-AssignIdentity</span></span>
<span data-ttu-id="35fb4-130">Genera e assegna una nuova identità dell'account di archiviazione per l'account di archiviazione per l'uso con i servizi di gestione delle chiavi, ad esempio Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="35fb4-130">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="35fb4-131">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="35fb4-131">-CustomDomainName</span></span>
<span data-ttu-id="35fb4-132">Specifica il nome del dominio personalizzato dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="35fb4-132">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="35fb4-133">Il valore predefinito è lo spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="35fb4-133">The default value is Storage.</span></span>

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

### <span data-ttu-id="35fb4-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35fb4-134">-DefaultProfile</span></span>
<span data-ttu-id="35fb4-135">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="35fb4-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35fb4-136">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="35fb4-136">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="35fb4-137">Abilitare Azure files Azure Active Directory Domain Service Authentication per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="35fb4-137">Enable Azure Files Azure Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="35fb4-138">-EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="35fb4-138">-EnableHierarchicalNamespace</span></span>
<span data-ttu-id="35fb4-139">Indica se l'account di archiviazione Abilita lo spazio dei nomi gerarchico.</span><span class="sxs-lookup"><span data-stu-id="35fb4-139">Indicates whether or not the Storage account enables Hierarchical Namespace.</span></span>

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

### <span data-ttu-id="35fb4-140">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="35fb4-140">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="35fb4-141">Indica se l'account di archiviazione Abilita o meno solo il traffico HTTPS.</span><span class="sxs-lookup"><span data-stu-id="35fb4-141">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="35fb4-142">-Tipo</span><span class="sxs-lookup"><span data-stu-id="35fb4-142">-Kind</span></span>
<span data-ttu-id="35fb4-143">Specifica il tipo di account di archiviazione creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35fb4-143">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="35fb4-144">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="35fb4-144">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="35fb4-145">Archiviazione.</span><span class="sxs-lookup"><span data-stu-id="35fb4-145">Storage.</span></span> <span data-ttu-id="35fb4-146">Account di archiviazione di uso generale che supporta l'archiviazione di BLOB, tabelle, code, file e dischi.</span><span class="sxs-lookup"><span data-stu-id="35fb4-146">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="35fb4-147">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="35fb4-147">StorageV2.</span></span> <span data-ttu-id="35fb4-148">Account di archiviazione per usi generali versione 2 (GPv2) che supporta BLOB, tabelle, code, file e dischi, con funzionalità avanzate come il livello dei dati.</span><span class="sxs-lookup"><span data-stu-id="35fb4-148">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="35fb4-149">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="35fb4-149">BlobStorage.</span></span> <span data-ttu-id="35fb4-150">Account di archiviazione BLOB che supporta l'archiviazione solo di BLOB.</span><span class="sxs-lookup"><span data-stu-id="35fb4-150">Blob Storage account which supports storage of Blobs only.</span></span>
- <span data-ttu-id="35fb4-151">BlockBlobStorage.</span><span class="sxs-lookup"><span data-stu-id="35fb4-151">BlockBlobStorage.</span></span> <span data-ttu-id="35fb4-152">Bloccare l'account di archiviazione BLOB che supporta l'archiviazione solo dei BLOB di blocco.</span><span class="sxs-lookup"><span data-stu-id="35fb4-152">Block Blob Storage account which supports storage of Block Blobs only.</span></span>
- <span data-ttu-id="35fb4-153">FileStorage.</span><span class="sxs-lookup"><span data-stu-id="35fb4-153">FileStorage.</span></span> <span data-ttu-id="35fb4-154">Account di archiviazione file che supporta solo l'archiviazione dei file.</span><span class="sxs-lookup"><span data-stu-id="35fb4-154">File Storage account which supports storage of Files only.</span></span>
<span data-ttu-id="35fb4-155">Il valore predefinito è StorageV2.</span><span class="sxs-lookup"><span data-stu-id="35fb4-155">The default value is StorageV2.</span></span>

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

### <span data-ttu-id="35fb4-156">-Posizione</span><span class="sxs-lookup"><span data-stu-id="35fb4-156">-Location</span></span>
<span data-ttu-id="35fb4-157">Specifica la posizione dell'account di archiviazione da creare.</span><span class="sxs-lookup"><span data-stu-id="35fb4-157">Specifies the location of the Storage account to create.</span></span>

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

### <span data-ttu-id="35fb4-158">-Nome</span><span class="sxs-lookup"><span data-stu-id="35fb4-158">-Name</span></span>
<span data-ttu-id="35fb4-159">Specifica il nome dell'account di archiviazione da creare.</span><span class="sxs-lookup"><span data-stu-id="35fb4-159">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="35fb4-160">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="35fb4-160">-NetworkRuleSet</span></span>
<span data-ttu-id="35fb4-161">NetworkRuleSet viene usato per definire un set di regole di configurazione per i firewall e le reti virtuali, nonché per impostare i valori per le proprietà di rete, ad esempio i servizi autorizzati ad aggirare le regole e come gestire le richieste che non corrispondono a nessuna delle regole definite.</span><span class="sxs-lookup"><span data-stu-id="35fb4-161">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="35fb4-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35fb4-162">-ResourceGroupName</span></span>
<span data-ttu-id="35fb4-163">Specifica il nome del gruppo di risorse in cui aggiungere l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="35fb4-163">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="35fb4-164">-SkuName</span><span class="sxs-lookup"><span data-stu-id="35fb4-164">-SkuName</span></span>
<span data-ttu-id="35fb4-165">Specifica il nome SKU dell'account di archiviazione creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35fb4-165">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="35fb4-166">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="35fb4-166">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="35fb4-167">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="35fb4-167">Standard_LRS.</span></span> <span data-ttu-id="35fb4-168">Spazio di archiviazione locale ridondante.</span><span class="sxs-lookup"><span data-stu-id="35fb4-168">Locally-redundant storage.</span></span>
- <span data-ttu-id="35fb4-169">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="35fb4-169">Standard_ZRS.</span></span> <span data-ttu-id="35fb4-170">Area-archiviazione ridondante.</span><span class="sxs-lookup"><span data-stu-id="35fb4-170">Zone-redundant storage.</span></span>
- <span data-ttu-id="35fb4-171">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="35fb4-171">Standard_GRS.</span></span> <span data-ttu-id="35fb4-172">Spazio di archiviazione Geo-ridondante.</span><span class="sxs-lookup"><span data-stu-id="35fb4-172">Geo-redundant storage.</span></span>
- <span data-ttu-id="35fb4-173">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="35fb4-173">Standard_RAGRS.</span></span> <span data-ttu-id="35fb4-174">Accesso in lettura archiviazione Geo-ridondante.</span><span class="sxs-lookup"><span data-stu-id="35fb4-174">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="35fb4-175">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="35fb4-175">Premium_LRS.</span></span> <span data-ttu-id="35fb4-176">Spazio di archiviazione locale ridondante Premium.</span><span class="sxs-lookup"><span data-stu-id="35fb4-176">Premium locally-redundant storage.</span></span>
- <span data-ttu-id="35fb4-177">Premium_ZRS.</span><span class="sxs-lookup"><span data-stu-id="35fb4-177">Premium_ZRS.</span></span> <span data-ttu-id="35fb4-178">Zona Premium-spazio di archiviazione ridondante.</span><span class="sxs-lookup"><span data-stu-id="35fb4-178">Premium zone-redundant storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS, Premium_ZRS

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35fb4-179">-Tag</span><span class="sxs-lookup"><span data-stu-id="35fb4-179">-Tag</span></span>
<span data-ttu-id="35fb4-180">Coppie chiave-valore nella forma di una tabella hash impostata come tag nel server.</span><span class="sxs-lookup"><span data-stu-id="35fb4-180">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="35fb4-181">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="35fb4-181">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="35fb4-182">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="35fb4-182">-UseSubDomain</span></span>
<span data-ttu-id="35fb4-183">Indica se abilitare la convalida CName indiretta.</span><span class="sxs-lookup"><span data-stu-id="35fb4-183">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="35fb4-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35fb4-184">CommonParameters</span></span>
<span data-ttu-id="35fb4-185">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35fb4-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35fb4-186">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35fb4-186">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35fb4-187">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="35fb4-187">INPUTS</span></span>

### <span data-ttu-id="35fb4-188">System. String</span><span class="sxs-lookup"><span data-stu-id="35fb4-188">System.String</span></span>

## <span data-ttu-id="35fb4-189">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="35fb4-189">OUTPUTS</span></span>

### <span data-ttu-id="35fb4-190">Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="35fb4-190">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="35fb4-191">Note</span><span class="sxs-lookup"><span data-stu-id="35fb4-191">NOTES</span></span>

## <span data-ttu-id="35fb4-192">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="35fb4-192">RELATED LINKS</span></span>

[<span data-ttu-id="35fb4-193">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="35fb4-193">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="35fb4-194">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="35fb4-194">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="35fb4-195">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="35fb4-195">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)
