---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccount.md
ms.openlocfilehash: 1b00930332d9f3f5a78e4cfe8ab7478a5dc5fa19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520322"
---
# <span data-ttu-id="aa172-101">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="aa172-101">New-AzureRmStorageAccount</span></span>

## <span data-ttu-id="aa172-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aa172-102">SYNOPSIS</span></span>
<span data-ttu-id="aa172-103">Crea un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="aa172-103">Creates a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa172-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aa172-104">SYNTAX</span></span>

```
New-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String>
 [-Location] <String> [[-Kind] <String>] [[-AccessTier] <String>] [[-CustomDomainName] <String>]
 [[-UseSubDomain] <Boolean>] [[-EnableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="aa172-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aa172-105">DESCRIPTION</span></span>
<span data-ttu-id="aa172-106">Il cmdlet **New-AzureRmStorageAccount** crea un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="aa172-106">The **New-AzureRmStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="aa172-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aa172-107">EXAMPLES</span></span>

### <span data-ttu-id="aa172-108">Esempio 1: creare un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="aa172-108">Example 1: Create a Storage Account</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "West US" -SkuName "Standard_GRS"
```

<span data-ttu-id="aa172-109">Questo comando crea un account di archiviazione per il nome del gruppo di risorse MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="aa172-109">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="aa172-110">Esempio 2: creare un account di archiviazione BLOB che usa la crittografia del servizio di archiviazione</span><span class="sxs-lookup"><span data-stu-id="aa172-110">Example 2: Create a Blob Storage account that uses Storage Service Encryption</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "West US" -SkuName "Standard_GRS" -EnableEncryptionService Blob -Kind "BlobStorage" -AccessTier Hot
```

<span data-ttu-id="aa172-111">Questo comando crea un account di archiviazione BLOB che usa il tipo di accesso caldo.</span><span class="sxs-lookup"><span data-stu-id="aa172-111">This command creates a Blob Storage account that uses the hot access type.</span></span>
<span data-ttu-id="aa172-112">L'account ha abilitato la crittografia del servizio di archiviazione nel servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="aa172-112">The account has enabled Storage Service encryption on Blob Service.</span></span>

### <span data-ttu-id="aa172-113">Esempio 3: creare un account di archiviazione che consente la crittografia del servizio di archiviazione su BLOB e servizi file e generare e assegnare un'identità per il Vault di Azure.</span><span class="sxs-lookup"><span data-stu-id="aa172-113">Example 3: Create a Storage Account that Enables Storage Service Encryption on Blob and File Services, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "West US" -SkuName "Standard_GRS" -EnableEncryptionService "Blob,File" -AssignIdentity
```

<span data-ttu-id="aa172-114">Questo comando crea un account di archiviazione che ha abilitato la crittografia del servizio di archiviazione su BLOB e servizi file.</span><span class="sxs-lookup"><span data-stu-id="aa172-114">This command creates a Storage account that enabled Storage Service encryption on Blob and File Services.</span></span>  <span data-ttu-id="aa172-115">Viene inoltre generata e assegnata un'identità che può essere usata per gestire le chiavi dell'account tramite Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="aa172-115">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

## <span data-ttu-id="aa172-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aa172-116">PARAMETERS</span></span>

### <span data-ttu-id="aa172-117">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="aa172-117">-AccessTier</span></span>
<span data-ttu-id="aa172-118">Specifica il livello di accesso dell'account di archiviazione creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa172-118">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="aa172-119">I valori accettabili per questo parametro sono: caldo e freddo.</span><span class="sxs-lookup"><span data-stu-id="aa172-119">The acceptable values for this parameter are: Hot and Cool.</span></span>

<span data-ttu-id="aa172-120">Se specifichi un valore di BlobStorage per il parametro *Kind* , devi specificare un valore per il parametro *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="aa172-120">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span>

<span data-ttu-id="aa172-121">Se specifichi un valore di spazio di archiviazione per questo parametro di *tipo* , non specificare il parametro *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="aa172-121">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa172-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="aa172-122">-AssignIdentity</span></span>
<span data-ttu-id="aa172-123">Genera e assegna una nuova identità dell'account di archiviazione per l'account di archiviazione per l'uso con i servizi di gestione delle chiavi, ad esempio Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="aa172-123">Generate and assign a new Storage Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa172-124">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="aa172-124">-CustomDomainName</span></span>
<span data-ttu-id="aa172-125">Specifica il nome del dominio personalizzato dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="aa172-125">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="aa172-126">Il valore predefinito è lo spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="aa172-126">The default value is Storage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa172-127">-EnableEncryptionService</span><span class="sxs-lookup"><span data-stu-id="aa172-127">-EnableEncryptionService</span></span>
<span data-ttu-id="aa172-128">Indica se questo cmdlet Abilita la crittografia del servizio di archiviazione nel servizio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="aa172-128">Indicates whether this cmdlet enables Storage Service encryption on the Storage Service.</span></span>
<span data-ttu-id="aa172-129">Sono supportati i servizi file Azure BLOB e Azure.</span><span class="sxs-lookup"><span data-stu-id="aa172-129">Azure Blob and Azure File Services are supported.</span></span>

```yaml
Type: EncryptionSupportServiceEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa172-130">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="aa172-130">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="aa172-131">Indica se l'account di archiviazione consente o meno solo il traffico HTTPS.</span><span class="sxs-lookup"><span data-stu-id="aa172-131">Indicates whether or not the Storage Account only enable https traffic.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa172-132">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="aa172-132">-InformationAction</span></span>
<span data-ttu-id="aa172-133">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="aa172-133">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="aa172-134">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="aa172-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="aa172-135">Continuare</span><span class="sxs-lookup"><span data-stu-id="aa172-135">Continue</span></span>
- <span data-ttu-id="aa172-136">Ignora</span><span class="sxs-lookup"><span data-stu-id="aa172-136">Ignore</span></span>
- <span data-ttu-id="aa172-137">Informarsi</span><span class="sxs-lookup"><span data-stu-id="aa172-137">Inquire</span></span>
- <span data-ttu-id="aa172-138">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="aa172-138">SilentlyContinue</span></span>
- <span data-ttu-id="aa172-139">Stop</span><span class="sxs-lookup"><span data-stu-id="aa172-139">Stop</span></span>
- <span data-ttu-id="aa172-140">Sospensione</span><span class="sxs-lookup"><span data-stu-id="aa172-140">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa172-141">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="aa172-141">-InformationVariable</span></span>
<span data-ttu-id="aa172-142">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="aa172-142">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa172-143">-Tipo</span><span class="sxs-lookup"><span data-stu-id="aa172-143">-Kind</span></span>
<span data-ttu-id="aa172-144">Specifica il tipo di account di archiviazione creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa172-144">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="aa172-145">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="aa172-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="aa172-146">Archiviazione.</span><span class="sxs-lookup"><span data-stu-id="aa172-146">Storage.</span></span>
<span data-ttu-id="aa172-147">Account di archiviazione di uso generale che supporta l'archiviazione di BLOB, tabelle, code, file e dischi.</span><span class="sxs-lookup"><span data-stu-id="aa172-147">General purpose storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>

- <span data-ttu-id="aa172-148">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="aa172-148">BlobStorage.</span></span>
<span data-ttu-id="aa172-149">Account di archiviazione BLOB che supporta l'archiviazione solo di BLOB.</span><span class="sxs-lookup"><span data-stu-id="aa172-149">Blob storage account which supports storage of Blobs only.</span></span>


<span data-ttu-id="aa172-150">Il valore predefinito è lo spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="aa172-150">The default value is Storage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa172-151">-Posizione</span><span class="sxs-lookup"><span data-stu-id="aa172-151">-Location</span></span>
<span data-ttu-id="aa172-152">Specifica la posizione dell'account di archiviazione da creare.</span><span class="sxs-lookup"><span data-stu-id="aa172-152">Specifies the location of the Storage account to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa172-153">-Nome</span><span class="sxs-lookup"><span data-stu-id="aa172-153">-Name</span></span>
<span data-ttu-id="aa172-154">Specifica il nome dell'account di archiviazione da creare.</span><span class="sxs-lookup"><span data-stu-id="aa172-154">Specifies the name of the Storage account to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa172-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa172-155">-ResourceGroupName</span></span>
<span data-ttu-id="aa172-156">Specifica il nome del gruppo di risorse in cui aggiungere l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="aa172-156">Specifies the name of the resource group in which to add the Storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa172-157">-SkuName</span><span class="sxs-lookup"><span data-stu-id="aa172-157">-SkuName</span></span>
<span data-ttu-id="aa172-158">Specifica il nome SKU dell'account di archiviazione creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa172-158">Specifies the SKU name of the storage account that this cmdlet creates.</span></span>
<span data-ttu-id="aa172-159">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="aa172-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="aa172-160">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="aa172-160">Standard_LRS.</span></span>
<span data-ttu-id="aa172-161">Spazio di archiviazione locale ridondante.</span><span class="sxs-lookup"><span data-stu-id="aa172-161">Locally-redundant storage.</span></span>
- <span data-ttu-id="aa172-162">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="aa172-162">Standard_ZRS.</span></span>
<span data-ttu-id="aa172-163">Area-archiviazione ridondante.</span><span class="sxs-lookup"><span data-stu-id="aa172-163">Zone-redundant storage.</span></span>
- <span data-ttu-id="aa172-164">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="aa172-164">Standard_GRS.</span></span>
<span data-ttu-id="aa172-165">Spazio di archiviazione Geo-ridondante.</span><span class="sxs-lookup"><span data-stu-id="aa172-165">Geo-redundant storage.</span></span>
- <span data-ttu-id="aa172-166">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="aa172-166">Standard_RAGRS.</span></span>
<span data-ttu-id="aa172-167">Accesso in lettura archiviazione Geo-ridondante.</span><span class="sxs-lookup"><span data-stu-id="aa172-167">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="aa172-168">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="aa172-168">Premium_LRS.</span></span>
<span data-ttu-id="aa172-169">Spazio di archiviazione locale ridondante Premium.</span><span class="sxs-lookup"><span data-stu-id="aa172-169">Premium locally-redundant storage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa172-170">-Tag</span><span class="sxs-lookup"><span data-stu-id="aa172-170">-Tag</span></span>
<span data-ttu-id="aa172-171">Se specifichi un valore di BlobStorage per il parametro *Kind* , devi specificare un valore per il parametro *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="aa172-171">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span>

<span data-ttu-id="aa172-172">Se specifichi un valore di spazio di archiviazione per questo parametro di *tipo* , non specificare il parametro *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="aa172-172">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa172-173">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="aa172-173">-UseSubDomain</span></span>
<span data-ttu-id="aa172-174">Indica se abilitare la convalida CName indiretta.</span><span class="sxs-lookup"><span data-stu-id="aa172-174">Indicates whether to enable indirect CName validation.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa172-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa172-175">CommonParameters</span></span>
<span data-ttu-id="aa172-176">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa172-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa172-177">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa172-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa172-178">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aa172-178">INPUTS</span></span>

### <span data-ttu-id="aa172-179">Nessuno</span><span class="sxs-lookup"><span data-stu-id="aa172-179">None</span></span>
<span data-ttu-id="aa172-180">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="aa172-180">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="aa172-181">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aa172-181">OUTPUTS</span></span>

## <span data-ttu-id="aa172-182">Note</span><span class="sxs-lookup"><span data-stu-id="aa172-182">NOTES</span></span>

## <span data-ttu-id="aa172-183">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aa172-183">RELATED LINKS</span></span>

[<span data-ttu-id="aa172-184">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="aa172-184">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="aa172-185">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="aa172-185">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)

[<span data-ttu-id="aa172-186">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="aa172-186">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)
