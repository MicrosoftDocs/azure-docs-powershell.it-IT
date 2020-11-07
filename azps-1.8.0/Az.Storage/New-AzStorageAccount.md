---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: 316bcbd8efa101a53dc36ede5e56e2b9379f02e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676589"
---
# <span data-ttu-id="45c73-101">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="45c73-101">New-AzStorageAccount</span></span>

## <span data-ttu-id="45c73-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="45c73-102">SYNOPSIS</span></span>
<span data-ttu-id="45c73-103">Crea un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="45c73-103">Creates a Storage account.</span></span>

## <span data-ttu-id="45c73-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="45c73-104">SYNTAX</span></span>

```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="45c73-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="45c73-105">DESCRIPTION</span></span>
<span data-ttu-id="45c73-106">Il cmdlet **New-AzStorageAccount** crea un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="45c73-106">The **New-AzStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="45c73-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="45c73-107">EXAMPLES</span></span>

### <span data-ttu-id="45c73-108">Esempio 1: creare un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="45c73-108">Example 1: Create a Storage account</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="45c73-109">Questo comando crea un account di archiviazione per il nome del gruppo di risorse MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="45c73-109">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="45c73-110">Esempio 2: creare un account di archiviazione BLOB con BlobStorage Kind e Hot AccessTier</span><span class="sxs-lookup"><span data-stu-id="45c73-110">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="45c73-111">Questo comando crea un account di archiviazione BLOB con BlobStorage Kind e Hot AccessTier</span><span class="sxs-lookup"><span data-stu-id="45c73-111">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="45c73-112">Esempio 3: creare un account di archiviazione con Kind StorageV2 e generare e assegnare un'identità per il Vault di Azure.</span><span class="sxs-lookup"><span data-stu-id="45c73-112">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="45c73-113">Questo comando crea un account di archiviazione con Kind StorageV2.</span><span class="sxs-lookup"><span data-stu-id="45c73-113">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="45c73-114">Viene inoltre generata e assegnata un'identità che può essere usata per gestire le chiavi dell'account tramite Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="45c73-114">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="45c73-115">Esempio 4: creare un account di archiviazione con NetworkRuleSet da JSON</span><span class="sxs-lookup"><span data-stu-id="45c73-115">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="45c73-116">Questo comando crea un account di archiviazione con proprietà NetworkRuleSet da JSON</span><span class="sxs-lookup"><span data-stu-id="45c73-116">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

### <span data-ttu-id="45c73-117">Esempio 5: creare un account di archiviazione con lo spazio dei nomi gerarchico abilitato.</span><span class="sxs-lookup"><span data-stu-id="45c73-117">Example 5: Create a Storage account with Hierarchical Namespace enabled.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

<span data-ttu-id="45c73-118">Questo comando crea un account di archiviazione con lo spazio dei nomi gerarchico abilitato.</span><span class="sxs-lookup"><span data-stu-id="45c73-118">This command creates a Storage account with Hierarchical Namespace enabled.</span></span>

## <span data-ttu-id="45c73-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="45c73-119">PARAMETERS</span></span>

### <span data-ttu-id="45c73-120">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="45c73-120">-AccessTier</span></span>
<span data-ttu-id="45c73-121">Specifica il livello di accesso dell'account di archiviazione creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45c73-121">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="45c73-122">I valori accettabili per questo parametro sono: caldo e freddo.</span><span class="sxs-lookup"><span data-stu-id="45c73-122">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="45c73-123">Se specifichi un valore di BlobStorage per il parametro *Kind* , devi specificare un valore per il parametro *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="45c73-123">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="45c73-124">Se specifichi un valore di spazio di archiviazione per questo parametro di *tipo* , non specificare il parametro *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="45c73-124">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="45c73-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="45c73-125">-AsJob</span></span>
<span data-ttu-id="45c73-126">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="45c73-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="45c73-127">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="45c73-127">-AssignIdentity</span></span>
<span data-ttu-id="45c73-128">Genera e assegna una nuova identità dell'account di archiviazione per l'account di archiviazione per l'uso con i servizi di gestione delle chiavi, ad esempio Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="45c73-128">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="45c73-129">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="45c73-129">-CustomDomainName</span></span>
<span data-ttu-id="45c73-130">Specifica il nome del dominio personalizzato dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="45c73-130">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="45c73-131">Il valore predefinito è lo spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="45c73-131">The default value is Storage.</span></span>

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

### <span data-ttu-id="45c73-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45c73-132">-DefaultProfile</span></span>
<span data-ttu-id="45c73-133">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="45c73-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45c73-134">-EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="45c73-134">-EnableHierarchicalNamespace</span></span>
<span data-ttu-id="45c73-135">Indica se l'account di archiviazione Abilita lo spazio dei nomi gerarchico.</span><span class="sxs-lookup"><span data-stu-id="45c73-135">Indicates whether or not the Storage account enables Hierarchical Namespace.</span></span>

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

### <span data-ttu-id="45c73-136">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="45c73-136">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="45c73-137">Indica se l'account di archiviazione Abilita o meno solo il traffico HTTPS.</span><span class="sxs-lookup"><span data-stu-id="45c73-137">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="45c73-138">-Tipo</span><span class="sxs-lookup"><span data-stu-id="45c73-138">-Kind</span></span>
<span data-ttu-id="45c73-139">Specifica il tipo di account di archiviazione creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45c73-139">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="45c73-140">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="45c73-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="45c73-141">Archiviazione.</span><span class="sxs-lookup"><span data-stu-id="45c73-141">Storage.</span></span> <span data-ttu-id="45c73-142">Account di archiviazione di uso generale che supporta l'archiviazione di BLOB, tabelle, code, file e dischi.</span><span class="sxs-lookup"><span data-stu-id="45c73-142">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="45c73-143">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="45c73-143">StorageV2.</span></span> <span data-ttu-id="45c73-144">Account di archiviazione per usi generali versione 2 (GPv2) che supporta BLOB, tabelle, code, file e dischi, con funzionalità avanzate come il livello dei dati.</span><span class="sxs-lookup"><span data-stu-id="45c73-144">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="45c73-145">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="45c73-145">BlobStorage.</span></span> <span data-ttu-id="45c73-146">Account di archiviazione BLOB che supporta l'archiviazione solo di BLOB.</span><span class="sxs-lookup"><span data-stu-id="45c73-146">Blob Storage account which supports storage of Blobs only.</span></span>
<span data-ttu-id="45c73-147">Il valore predefinito è lo spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="45c73-147">The default value is Storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Storage, StorageV2, BlobStorage, BlockBlobStorage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45c73-148">-Posizione</span><span class="sxs-lookup"><span data-stu-id="45c73-148">-Location</span></span>
<span data-ttu-id="45c73-149">Specifica la posizione dell'account di archiviazione da creare.</span><span class="sxs-lookup"><span data-stu-id="45c73-149">Specifies the location of the Storage account to create.</span></span>

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

### <span data-ttu-id="45c73-150">-Nome</span><span class="sxs-lookup"><span data-stu-id="45c73-150">-Name</span></span>
<span data-ttu-id="45c73-151">Specifica il nome dell'account di archiviazione da creare.</span><span class="sxs-lookup"><span data-stu-id="45c73-151">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="45c73-152">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="45c73-152">-NetworkRuleSet</span></span>
<span data-ttu-id="45c73-153">NetworkRuleSet viene usato per definire un set di regole di configurazione per i firewall e le reti virtuali, nonché per impostare i valori per le proprietà di rete, ad esempio i servizi autorizzati ad aggirare le regole e come gestire le richieste che non corrispondono a nessuna delle regole definite.</span><span class="sxs-lookup"><span data-stu-id="45c73-153">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="45c73-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45c73-154">-ResourceGroupName</span></span>
<span data-ttu-id="45c73-155">Specifica il nome del gruppo di risorse in cui aggiungere l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="45c73-155">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="45c73-156">-SkuName</span><span class="sxs-lookup"><span data-stu-id="45c73-156">-SkuName</span></span>
<span data-ttu-id="45c73-157">Specifica il nome SKU dell'account di archiviazione creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45c73-157">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="45c73-158">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="45c73-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="45c73-159">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="45c73-159">Standard_LRS.</span></span> <span data-ttu-id="45c73-160">Spazio di archiviazione locale ridondante.</span><span class="sxs-lookup"><span data-stu-id="45c73-160">Locally-redundant storage.</span></span>
- <span data-ttu-id="45c73-161">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="45c73-161">Standard_ZRS.</span></span> <span data-ttu-id="45c73-162">Area-archiviazione ridondante.</span><span class="sxs-lookup"><span data-stu-id="45c73-162">Zone-redundant storage.</span></span>
- <span data-ttu-id="45c73-163">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="45c73-163">Standard_GRS.</span></span> <span data-ttu-id="45c73-164">Spazio di archiviazione Geo-ridondante.</span><span class="sxs-lookup"><span data-stu-id="45c73-164">Geo-redundant storage.</span></span>
- <span data-ttu-id="45c73-165">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="45c73-165">Standard_RAGRS.</span></span> <span data-ttu-id="45c73-166">Accesso in lettura archiviazione Geo-ridondante.</span><span class="sxs-lookup"><span data-stu-id="45c73-166">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="45c73-167">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="45c73-167">Premium_LRS.</span></span> <span data-ttu-id="45c73-168">Spazio di archiviazione locale ridondante Premium.</span><span class="sxs-lookup"><span data-stu-id="45c73-168">Premium locally-redundant storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45c73-169">-Tag</span><span class="sxs-lookup"><span data-stu-id="45c73-169">-Tag</span></span>
<span data-ttu-id="45c73-170">Coppie chiave-valore nella forma di una tabella hash impostata come tag nel server.</span><span class="sxs-lookup"><span data-stu-id="45c73-170">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="45c73-171">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="45c73-171">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="45c73-172">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="45c73-172">-UseSubDomain</span></span>
<span data-ttu-id="45c73-173">Indica se abilitare la convalida CName indiretta.</span><span class="sxs-lookup"><span data-stu-id="45c73-173">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="45c73-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45c73-174">CommonParameters</span></span>
<span data-ttu-id="45c73-175">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45c73-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45c73-176">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45c73-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45c73-177">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="45c73-177">INPUTS</span></span>

### <span data-ttu-id="45c73-178">System. String</span><span class="sxs-lookup"><span data-stu-id="45c73-178">System.String</span></span>

## <span data-ttu-id="45c73-179">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="45c73-179">OUTPUTS</span></span>

### <span data-ttu-id="45c73-180">Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="45c73-180">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="45c73-181">Note</span><span class="sxs-lookup"><span data-stu-id="45c73-181">NOTES</span></span>

## <span data-ttu-id="45c73-182">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="45c73-182">RELATED LINKS</span></span>

[<span data-ttu-id="45c73-183">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="45c73-183">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="45c73-184">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="45c73-184">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="45c73-185">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="45c73-185">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)