---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/New-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/New-AzureRmStorageAccount.md
ms.openlocfilehash: 50384630658f7626ee02ca1dee223e82bf122ef1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688486"
---
# <span data-ttu-id="c6080-101">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c6080-101">New-AzureRmStorageAccount</span></span>

## <span data-ttu-id="c6080-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c6080-102">SYNOPSIS</span></span>
<span data-ttu-id="c6080-103">Crea un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c6080-103">Creates a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6080-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c6080-104">SYNTAX</span></span>

```
New-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String>
 [-Location] <String> [[-Kind] <String>] [[-AccessTier] <String>] [[-CustomDomainName] <String>]
 [[-UseSubDomain] <Boolean>] [[-EnableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c6080-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c6080-105">DESCRIPTION</span></span>
<span data-ttu-id="c6080-106">Il cmdlet **New-AzureRmStorageAccount** crea un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="c6080-106">The **New-AzureRmStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="c6080-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c6080-107">EXAMPLES</span></span>

### <span data-ttu-id="c6080-108">Esempio 1: creare un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="c6080-108">Example 1: Create a Storage Account</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "US West" -SkuName "Standard_GRS"
```

<span data-ttu-id="c6080-109">Questo comando crea un account di archiviazione per il nome del gruppo di risorse MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c6080-109">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="c6080-110">Esempio 2: creare un account di archiviazione BLOB che usa la crittografia del servizio di archiviazione</span><span class="sxs-lookup"><span data-stu-id="c6080-110">Example 2: Create a Blob Storage account that uses Storage Service Encryption</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "US West" -SkuName "Standard_GRS" -EnableEncryptionService Blob -Kind "BlobStorage" -AccessTier Hot
```

<span data-ttu-id="c6080-111">Questo comando crea un account di archiviazione BLOB che usa il tipo di accesso caldo.</span><span class="sxs-lookup"><span data-stu-id="c6080-111">This command creates a Blob Storage account that uses the hot access type.</span></span>
<span data-ttu-id="c6080-112">L'account ha abilitato la crittografia del servizio di archiviazione nel servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="c6080-112">The account has enabled Storage Service encryption on Blob Service.</span></span>

### <span data-ttu-id="c6080-113">Esempio 3: creare un account di archiviazione che consente la crittografia del servizio di archiviazione su BLOB e servizi file e generare e assegnare un'identità per il Vault di Azure.</span><span class="sxs-lookup"><span data-stu-id="c6080-113">Example 3: Create a Storage Account that Enables Storage Service Encryption on Blob and File Services, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "US West" -SkuName "Standard_GRS" -EnableEncryptionService "Blob,File" -AssignIdentity
```

<span data-ttu-id="c6080-114">Questo comando crea un account di archiviazione che ha abilitato la crittografia del servizio di archiviazione su BLOB e servizi file.</span><span class="sxs-lookup"><span data-stu-id="c6080-114">This command creates a Storage account that enabled Storage Service encryption on Blob and File Services.</span></span>  <span data-ttu-id="c6080-115">Viene inoltre generata e assegnata un'identità che può essere usata per gestire le chiavi dell'account tramite Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="c6080-115">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

## <span data-ttu-id="c6080-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c6080-116">PARAMETERS</span></span>

### <span data-ttu-id="c6080-117">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="c6080-117">-AccessTier</span></span>
<span data-ttu-id="c6080-118">Specifica il livello di accesso dell'account di archiviazione creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6080-118">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="c6080-119">I valori accettabili per questo parametro sono: caldo e freddo.</span><span class="sxs-lookup"><span data-stu-id="c6080-119">The acceptable values for this parameter are: Hot and Cool.</span></span>

<span data-ttu-id="c6080-120">Se specifichi un valore di BlobStorage per il parametro *Kind* , devi specificare un valore per il parametro *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="c6080-120">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span>

<span data-ttu-id="c6080-121">Se specifichi un valore di spazio di archiviazione per questo parametro di *tipo* , non specificare il parametro *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="c6080-121">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6080-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="c6080-122">-AssignIdentity</span></span>
<span data-ttu-id="c6080-123">Genera e assegna una nuova identità dell'account di archiviazione per l'account di archiviazione per l'uso con i servizi di gestione delle chiavi, ad esempio Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="c6080-123">Generate and assign a new Storage Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="c6080-124">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="c6080-124">-CustomDomainName</span></span>
<span data-ttu-id="c6080-125">Specifica il nome del dominio personalizzato dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c6080-125">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="c6080-126">Il valore predefinito è lo spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c6080-126">The default value is Storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6080-127">-EnableEncryptionService</span><span class="sxs-lookup"><span data-stu-id="c6080-127">-EnableEncryptionService</span></span>
<span data-ttu-id="c6080-128">Indica se questo cmdlet Abilita la crittografia del servizio di archiviazione nel servizio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c6080-128">Indicates whether this cmdlet enables Storage Service encryption on the Storage Service.</span></span>
<span data-ttu-id="c6080-129">Sono supportati i servizi file Azure BLOB e Azure.</span><span class="sxs-lookup"><span data-stu-id="c6080-129">Azure Blob and Azure File Services are supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Storage.StorageAccountBaseCmdlet+EncryptionSupportServiceEnum]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6080-130">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="c6080-130">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="c6080-131">Indica se l'account di archiviazione consente o meno solo il traffico HTTPS.</span><span class="sxs-lookup"><span data-stu-id="c6080-131">Indicates whether or not the Storage Account only enable https traffic.</span></span>

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

### <span data-ttu-id="c6080-132">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c6080-132">-InformationAction</span></span>
<span data-ttu-id="c6080-133">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="c6080-133">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c6080-134">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c6080-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c6080-135">Continuare</span><span class="sxs-lookup"><span data-stu-id="c6080-135">Continue</span></span>
- <span data-ttu-id="c6080-136">Ignora</span><span class="sxs-lookup"><span data-stu-id="c6080-136">Ignore</span></span>
- <span data-ttu-id="c6080-137">Informarsi</span><span class="sxs-lookup"><span data-stu-id="c6080-137">Inquire</span></span>
- <span data-ttu-id="c6080-138">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c6080-138">SilentlyContinue</span></span>
- <span data-ttu-id="c6080-139">Stop</span><span class="sxs-lookup"><span data-stu-id="c6080-139">Stop</span></span>
- <span data-ttu-id="c6080-140">Sospensione</span><span class="sxs-lookup"><span data-stu-id="c6080-140">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6080-141">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c6080-141">-InformationVariable</span></span>
<span data-ttu-id="c6080-142">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="c6080-142">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6080-143">-Tipo</span><span class="sxs-lookup"><span data-stu-id="c6080-143">-Kind</span></span>
<span data-ttu-id="c6080-144">Specifica il tipo di account di archiviazione creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6080-144">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="c6080-145">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c6080-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c6080-146">Archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c6080-146">Storage.</span></span>
<span data-ttu-id="c6080-147">Account di archiviazione di uso generale che supporta l'archiviazione di BLOB, tabelle, code, file e dischi.</span><span class="sxs-lookup"><span data-stu-id="c6080-147">General purpose storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
 
- <span data-ttu-id="c6080-148">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="c6080-148">BlobStorage.</span></span>
<span data-ttu-id="c6080-149">Account di archiviazione BLOB che supporta l'archiviazione solo di BLOB.</span><span class="sxs-lookup"><span data-stu-id="c6080-149">Blob storage account which supports storage of Blobs only.</span></span>
 

<span data-ttu-id="c6080-150">Il valore predefinito è lo spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c6080-150">The default value is Storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6080-151">-Posizione</span><span class="sxs-lookup"><span data-stu-id="c6080-151">-Location</span></span>
<span data-ttu-id="c6080-152">Specifica la posizione dell'account di archiviazione da creare.</span><span class="sxs-lookup"><span data-stu-id="c6080-152">Specifies the location of the Storage account to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6080-153">-Nome</span><span class="sxs-lookup"><span data-stu-id="c6080-153">-Name</span></span>
<span data-ttu-id="c6080-154">Specifica il nome dell'account di archiviazione da creare.</span><span class="sxs-lookup"><span data-stu-id="c6080-154">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="c6080-155">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="c6080-155">-NetworkRuleSet</span></span>
<span data-ttu-id="c6080-156">NetworkRuleSet account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="c6080-156">Storage Account NetworkRuleSet</span></span>

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

### <span data-ttu-id="c6080-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6080-157">-ResourceGroupName</span></span>
<span data-ttu-id="c6080-158">Specifica il nome del gruppo di risorse in cui aggiungere l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c6080-158">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="c6080-159">-SkuName</span><span class="sxs-lookup"><span data-stu-id="c6080-159">-SkuName</span></span>
<span data-ttu-id="c6080-160">Specifica il nome SKU dell'account di archiviazione creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6080-160">Specifies the SKU name of the storage account that this cmdlet creates.</span></span>
<span data-ttu-id="c6080-161">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c6080-161">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c6080-162">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="c6080-162">Standard_LRS.</span></span>
<span data-ttu-id="c6080-163">Spazio di archiviazione locale ridondante.</span><span class="sxs-lookup"><span data-stu-id="c6080-163">Locally-redundant storage.</span></span> 
- <span data-ttu-id="c6080-164">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="c6080-164">Standard_ZRS.</span></span>
<span data-ttu-id="c6080-165">Area-archiviazione ridondante.</span><span class="sxs-lookup"><span data-stu-id="c6080-165">Zone-redundant storage.</span></span>
- <span data-ttu-id="c6080-166">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="c6080-166">Standard_GRS.</span></span>
<span data-ttu-id="c6080-167">Spazio di archiviazione Geo-ridondante.</span><span class="sxs-lookup"><span data-stu-id="c6080-167">Geo-redundant storage.</span></span> 
- <span data-ttu-id="c6080-168">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="c6080-168">Standard_RAGRS.</span></span>
<span data-ttu-id="c6080-169">Accesso in lettura archiviazione Geo-ridondante.</span><span class="sxs-lookup"><span data-stu-id="c6080-169">Read access geo-redundant storage.</span></span> 
- <span data-ttu-id="c6080-170">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="c6080-170">Premium_LRS.</span></span>
<span data-ttu-id="c6080-171">Spazio di archiviazione locale ridondante Premium.</span><span class="sxs-lookup"><span data-stu-id="c6080-171">Premium locally-redundant storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6080-172">-Tag</span><span class="sxs-lookup"><span data-stu-id="c6080-172">-Tag</span></span>
<span data-ttu-id="c6080-173">Se specifichi un valore di BlobStorage per il parametro *Kind* , devi specificare un valore per il parametro *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="c6080-173">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span>

<span data-ttu-id="c6080-174">Se specifichi un valore di spazio di archiviazione per questo parametro di *tipo* , non specificare il parametro *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="c6080-174">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6080-175">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="c6080-175">-UseSubDomain</span></span>
<span data-ttu-id="c6080-176">Indica se abilitare la convalida CName indiretta.</span><span class="sxs-lookup"><span data-stu-id="c6080-176">Indicates whether to enable indirect CName validation.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6080-177">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6080-177">-DefaultProfile</span></span>
<span data-ttu-id="c6080-178">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c6080-178">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6080-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6080-179">CommonParameters</span></span>
<span data-ttu-id="c6080-180">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6080-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6080-181">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6080-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6080-182">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c6080-182">INPUTS</span></span>

## <span data-ttu-id="c6080-183">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c6080-183">OUTPUTS</span></span>

## <span data-ttu-id="c6080-184">Note</span><span class="sxs-lookup"><span data-stu-id="c6080-184">NOTES</span></span>

## <span data-ttu-id="c6080-185">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c6080-185">RELATED LINKS</span></span>

[<span data-ttu-id="c6080-186">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c6080-186">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="c6080-187">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c6080-187">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)

[<span data-ttu-id="c6080-188">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c6080-188">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


