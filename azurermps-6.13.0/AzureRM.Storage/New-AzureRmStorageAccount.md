---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/new-azurermstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccount.md
ms.openlocfilehash: 2ceb395805607809593054880415dccac7e1e28c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517315"
---
# <span data-ttu-id="fda4b-101">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fda4b-101">New-AzureRmStorageAccount</span></span>

## <span data-ttu-id="fda4b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fda4b-102">SYNOPSIS</span></span>
<span data-ttu-id="fda4b-103">Crea un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="fda4b-103">Creates a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fda4b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fda4b-104">SYNTAX</span></span>

```
New-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String>
 [-Location] <String> [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>]
 [-UseSubDomain <Boolean>] [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fda4b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fda4b-105">DESCRIPTION</span></span>
<span data-ttu-id="fda4b-106">Il cmdlet **New-AzureRmStorageAccount** crea un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="fda4b-106">The **New-AzureRmStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="fda4b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fda4b-107">EXAMPLES</span></span>

### <span data-ttu-id="fda4b-108">Esempio 1: creare un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="fda4b-108">Example 1: Create a Storage account</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="fda4b-109">Questo comando crea un account di archiviazione per il nome del gruppo di risorse MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="fda4b-109">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="fda4b-110">Esempio 2: creare un account di archiviazione BLOB con BlobStorage Kind e Hot AccessTier</span><span class="sxs-lookup"><span data-stu-id="fda4b-110">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="fda4b-111">Questo comando crea un account di archiviazione BLOB con BlobStorage Kind e Hot AccessTier</span><span class="sxs-lookup"><span data-stu-id="fda4b-111">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="fda4b-112">Esempio 3: creare un account di archiviazione con Kind StorageV2 e generare e assegnare un'identità per il Vault di Azure.</span><span class="sxs-lookup"><span data-stu-id="fda4b-112">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="fda4b-113">Questo comando crea un account di archiviazione con Kind StorageV2.</span><span class="sxs-lookup"><span data-stu-id="fda4b-113">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="fda4b-114">Viene inoltre generata e assegnata un'identità che può essere usata per gestire le chiavi dell'account tramite Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="fda4b-114">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="fda4b-115">Esempio 4: creare un account di archiviazione con NetworkRuleSet da JSON</span><span class="sxs-lookup"><span data-stu-id="fda4b-115">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="fda4b-116">Questo comando crea un account di archiviazione con proprietà NetworkRuleSet da JSON</span><span class="sxs-lookup"><span data-stu-id="fda4b-116">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

## <span data-ttu-id="fda4b-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fda4b-117">PARAMETERS</span></span>

### <span data-ttu-id="fda4b-118">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="fda4b-118">-AccessTier</span></span>
<span data-ttu-id="fda4b-119">Specifica il livello di accesso dell'account di archiviazione creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fda4b-119">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="fda4b-120">I valori accettabili per questo parametro sono: caldo e freddo.</span><span class="sxs-lookup"><span data-stu-id="fda4b-120">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="fda4b-121">Se specifichi un valore di BlobStorage per il parametro *Kind* , devi specificare un valore per il parametro *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="fda4b-121">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="fda4b-122">Se specifichi un valore di spazio di archiviazione per questo parametro di *tipo* , non specificare il parametro *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="fda4b-122">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="fda4b-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fda4b-123">-AsJob</span></span>
<span data-ttu-id="fda4b-124">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="fda4b-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fda4b-125">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="fda4b-125">-AssignIdentity</span></span>
<span data-ttu-id="fda4b-126">Genera e assegna una nuova identità dell'account di archiviazione per l'account di archiviazione per l'uso con i servizi di gestione delle chiavi, ad esempio Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="fda4b-126">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="fda4b-127">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="fda4b-127">-CustomDomainName</span></span>
<span data-ttu-id="fda4b-128">Specifica il nome del dominio personalizzato dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="fda4b-128">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="fda4b-129">Il valore predefinito è lo spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="fda4b-129">The default value is Storage.</span></span>

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

### <span data-ttu-id="fda4b-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fda4b-130">-DefaultProfile</span></span>
<span data-ttu-id="fda4b-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fda4b-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fda4b-132">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="fda4b-132">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="fda4b-133">Indica se l'account di archiviazione Abilita o meno solo il traffico HTTPS.</span><span class="sxs-lookup"><span data-stu-id="fda4b-133">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="fda4b-134">-Tipo</span><span class="sxs-lookup"><span data-stu-id="fda4b-134">-Kind</span></span>
<span data-ttu-id="fda4b-135">Specifica il tipo di account di archiviazione creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fda4b-135">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="fda4b-136">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="fda4b-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fda4b-137">Archiviazione.</span><span class="sxs-lookup"><span data-stu-id="fda4b-137">Storage.</span></span> <span data-ttu-id="fda4b-138">Account di archiviazione di uso generale che supporta l'archiviazione di BLOB, tabelle, code, file e dischi.</span><span class="sxs-lookup"><span data-stu-id="fda4b-138">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="fda4b-139">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="fda4b-139">StorageV2.</span></span> <span data-ttu-id="fda4b-140">Account di archiviazione per usi generali versione 2 (GPv2) che supporta BLOB, tabelle, code, file e dischi, con funzionalità avanzate come il livello dei dati.</span><span class="sxs-lookup"><span data-stu-id="fda4b-140">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="fda4b-141">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="fda4b-141">BlobStorage.</span></span> <span data-ttu-id="fda4b-142">Account di archiviazione BLOB che supporta l'archiviazione solo di BLOB.</span><span class="sxs-lookup"><span data-stu-id="fda4b-142">Blob Storage account which supports storage of Blobs only.</span></span>
<span data-ttu-id="fda4b-143">Il valore predefinito è lo spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="fda4b-143">The default value is Storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Storage, StorageV2, BlobStorage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fda4b-144">-Posizione</span><span class="sxs-lookup"><span data-stu-id="fda4b-144">-Location</span></span>
<span data-ttu-id="fda4b-145">Specifica la posizione dell'account di archiviazione da creare.</span><span class="sxs-lookup"><span data-stu-id="fda4b-145">Specifies the location of the Storage account to create.</span></span>

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

### <span data-ttu-id="fda4b-146">-Nome</span><span class="sxs-lookup"><span data-stu-id="fda4b-146">-Name</span></span>
<span data-ttu-id="fda4b-147">Specifica il nome dell'account di archiviazione da creare.</span><span class="sxs-lookup"><span data-stu-id="fda4b-147">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="fda4b-148">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="fda4b-148">-NetworkRuleSet</span></span>
<span data-ttu-id="fda4b-149">NetworkRuleSet viene usato per definire un set di regole di configurazione per i firewall e le reti virtuali, nonché per impostare i valori per le proprietà di rete, ad esempio i servizi autorizzati ad aggirare le regole e come gestire le richieste che non corrispondono a nessuna delle regole definite.</span><span class="sxs-lookup"><span data-stu-id="fda4b-149">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="fda4b-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fda4b-150">-ResourceGroupName</span></span>
<span data-ttu-id="fda4b-151">Specifica il nome del gruppo di risorse in cui aggiungere l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="fda4b-151">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="fda4b-152">-SkuName</span><span class="sxs-lookup"><span data-stu-id="fda4b-152">-SkuName</span></span>
<span data-ttu-id="fda4b-153">Specifica il nome SKU dell'account di archiviazione creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fda4b-153">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="fda4b-154">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="fda4b-154">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fda4b-155">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="fda4b-155">Standard_LRS.</span></span> <span data-ttu-id="fda4b-156">Spazio di archiviazione locale ridondante.</span><span class="sxs-lookup"><span data-stu-id="fda4b-156">Locally-redundant storage.</span></span>
- <span data-ttu-id="fda4b-157">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="fda4b-157">Standard_ZRS.</span></span> <span data-ttu-id="fda4b-158">Area-archiviazione ridondante.</span><span class="sxs-lookup"><span data-stu-id="fda4b-158">Zone-redundant storage.</span></span>
- <span data-ttu-id="fda4b-159">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="fda4b-159">Standard_GRS.</span></span> <span data-ttu-id="fda4b-160">Spazio di archiviazione Geo-ridondante.</span><span class="sxs-lookup"><span data-stu-id="fda4b-160">Geo-redundant storage.</span></span>
- <span data-ttu-id="fda4b-161">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="fda4b-161">Standard_RAGRS.</span></span> <span data-ttu-id="fda4b-162">Accesso in lettura archiviazione Geo-ridondante.</span><span class="sxs-lookup"><span data-stu-id="fda4b-162">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="fda4b-163">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="fda4b-163">Premium_LRS.</span></span> <span data-ttu-id="fda4b-164">Spazio di archiviazione locale ridondante Premium.</span><span class="sxs-lookup"><span data-stu-id="fda4b-164">Premium locally-redundant storage.</span></span>

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

### <span data-ttu-id="fda4b-165">-Tag</span><span class="sxs-lookup"><span data-stu-id="fda4b-165">-Tag</span></span>
<span data-ttu-id="fda4b-166">Coppie chiave-valore nella forma di una tabella hash impostata come tag nel server.</span><span class="sxs-lookup"><span data-stu-id="fda4b-166">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="fda4b-167">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="fda4b-167">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="fda4b-168">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="fda4b-168">-UseSubDomain</span></span>
<span data-ttu-id="fda4b-169">Indica se abilitare la convalida CName indiretta.</span><span class="sxs-lookup"><span data-stu-id="fda4b-169">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="fda4b-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fda4b-170">CommonParameters</span></span>
<span data-ttu-id="fda4b-171">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fda4b-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fda4b-172">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fda4b-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fda4b-173">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fda4b-173">INPUTS</span></span>

### <span data-ttu-id="fda4b-174">System. String</span><span class="sxs-lookup"><span data-stu-id="fda4b-174">System.String</span></span>

### <span data-ttu-id="fda4b-175">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fda4b-175">System.Boolean</span></span>

## <span data-ttu-id="fda4b-176">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fda4b-176">OUTPUTS</span></span>

### <span data-ttu-id="fda4b-177">Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fda4b-177">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="fda4b-178">Note</span><span class="sxs-lookup"><span data-stu-id="fda4b-178">NOTES</span></span>

## <span data-ttu-id="fda4b-179">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fda4b-179">RELATED LINKS</span></span>

[<span data-ttu-id="fda4b-180">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fda4b-180">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="fda4b-181">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fda4b-181">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)

[<span data-ttu-id="fda4b-182">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fda4b-182">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)