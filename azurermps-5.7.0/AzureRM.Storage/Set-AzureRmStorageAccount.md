---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Set-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Set-AzureRmStorageAccount.md
ms.openlocfilehash: 860e87063810251075341cd1eddd013870734384
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512136"
---
# <span data-ttu-id="5ee96-101">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5ee96-101">Set-AzureRmStorageAccount</span></span>

## <span data-ttu-id="5ee96-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5ee96-102">SYNOPSIS</span></span>
<span data-ttu-id="5ee96-103">Modifica un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="5ee96-103">Modifies a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ee96-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5ee96-104">SYNTAX</span></span>

### <span data-ttu-id="5ee96-105">StorageEncryption (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5ee96-105">StorageEncryption (Default)</span></span>
```
Set-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [[-SkuName] <String>]
 [[-AccessTier] <String>] [[-CustomDomainName] <String>] [[-UseSubDomain] <Boolean>]
 [[-EnableEncryptionService] <EncryptionSupportServiceEnum>]
 [[-DisableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ee96-106">KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="5ee96-106">KeyvaultEncryption</span></span>
```
Set-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [[-SkuName] <String>]
 [[-AccessTier] <String>] [[-CustomDomainName] <String>] [[-UseSubDomain] <Boolean>]
 [[-EnableEncryptionService] <EncryptionSupportServiceEnum>]
 [[-DisableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-AssignIdentity] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ee96-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ee96-107">DESCRIPTION</span></span>
<span data-ttu-id="5ee96-108">Il cmdlet **set-AzureRmStorageAccount** modifica un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="5ee96-108">The **Set-AzureRmStorageAccount** cmdlet modifies an Azure Storage account.</span></span>
<span data-ttu-id="5ee96-109">Puoi usare questo cmdlet per modificare il tipo di account, aggiornare un dominio del cliente o impostare i contrassegni in un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="5ee96-109">You can use this cmdlet to modify the account type, update a customer domain, or set tags on a Storage account.</span></span>

## <span data-ttu-id="5ee96-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5ee96-110">EXAMPLES</span></span>

### <span data-ttu-id="5ee96-111">Esempio 1: impostare il tipo di account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="5ee96-111">Example 1: Set the Storage account type</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Type "Standard_RAGRS"
```

<span data-ttu-id="5ee96-112">Questo comando imposta il tipo di account di archiviazione su Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="5ee96-112">This command sets the Storage account type to Standard_RAGRS.</span></span>

### <span data-ttu-id="5ee96-113">Esempio 2: impostare un dominio personalizzato per un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="5ee96-113">Example 2: Set a custom domain for a Storage account</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

<span data-ttu-id="5ee96-114">Questo comando imposta un dominio personalizzato per un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="5ee96-114">This command sets a custom domain for a Storage account.</span></span>

### <span data-ttu-id="5ee96-115">Esempio 3: abilitare la crittografia per i servizi BLOB e file</span><span class="sxs-lookup"><span data-stu-id="5ee96-115">Example 3: Enable encryption on Blob and File Services</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -EnableEncryptionService "Blob,File"
```

<span data-ttu-id="5ee96-116">Questo comando consente la crittografia del servizio di archiviazione su BLOB e file per un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="5ee96-116">This command enables Storage Service encryption on Blob and File for a Storage account.</span></span>

### <span data-ttu-id="5ee96-117">Esempio 4: impostare il valore di livello di accesso</span><span class="sxs-lookup"><span data-stu-id="5ee96-117">Example 4: Set the access tier value</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -AccessTier Cool
```

<span data-ttu-id="5ee96-118">Il comando imposta il valore di livello di Access come cool.</span><span class="sxs-lookup"><span data-stu-id="5ee96-118">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="5ee96-119">Esempio 4: impostare il dominio e i tag personalizzati</span><span class="sxs-lookup"><span data-stu-id="5ee96-119">Example 4: Set the custom domain and tags</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="5ee96-120">Il comando imposta il valore di livello di Access come cool.</span><span class="sxs-lookup"><span data-stu-id="5ee96-120">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="5ee96-121">Esempio 5: abilitare la crittografia nei servizi BLOB con il Vault</span><span class="sxs-lookup"><span data-stu-id="5ee96-121">Example 5: Enable encryption on Blob Services with Keyvault</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -AssignIdentity
PS C:\>$account = Get-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount"

PS C:\>$keyVault = New-AzureRmKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzureKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey

PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -EnableEncryptionService "Blob" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

<span data-ttu-id="5ee96-122">Questo comando consente la crittografia del servizio di archiviazione su BLOB con un nuovo Vault creato.</span><span class="sxs-lookup"><span data-stu-id="5ee96-122">This command enables Storage Service encryption on Blob with a new created Keyvault.</span></span>

### <span data-ttu-id="5ee96-123">Esempio 6: disabilitare la crittografia in Servizi file con la sorgente di origine impostata su "Microsoft. storage"</span><span class="sxs-lookup"><span data-stu-id="5ee96-123">Example 6: Disable encryption on File Services with KeySource set to "Microsoft.Storage"</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -DisableEncryptionService File  -StorageEncryption
```

<span data-ttu-id="5ee96-124">Questo comando Disabilita la crittografia in Servizi file con la sorgente di origine impostata su "Microsoft. storage"</span><span class="sxs-lookup"><span data-stu-id="5ee96-124">This command disables encryption on File Services with KeySource set to "Microsoft.Storage"</span></span>

## <span data-ttu-id="5ee96-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5ee96-125">PARAMETERS</span></span>

### <span data-ttu-id="5ee96-126">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="5ee96-126">-AccessTier</span></span>
<span data-ttu-id="5ee96-127">Specifica il livello di accesso dell'account di archiviazione modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ee96-127">Specifies the access tier of the Storage account that this cmdlet modifies.</span></span>
<span data-ttu-id="5ee96-128">I valori accettabili per questo parametro sono: caldo e freddo.</span><span class="sxs-lookup"><span data-stu-id="5ee96-128">The acceptable values for this parameter are: Hot and Cool.</span></span>

<span data-ttu-id="5ee96-129">Se si modifica il livello di accesso, potrebbero essere presenti ulteriori addebiti.</span><span class="sxs-lookup"><span data-stu-id="5ee96-129">If you change the access tier, it may result in additional charges.</span></span>
<span data-ttu-id="5ee96-130">Per altre informazioni, vedere Archiviazione BLOB di Azure: livelli di archiviazione caldi e freddi https://go.microsoft.com/fwlink/?LinkId=786482 ( https://go.microsoft.com/fwlink/?LinkId=786482) .</span><span class="sxs-lookup"><span data-stu-id="5ee96-130">For more information, see Azure Blob Storage: Hot and cool storage tiershttps://go.microsoft.com/fwlink/?LinkId=786482 (https://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="5ee96-131">Se il tipo di account di archiviazione è lo spazio di archiviazione, non specificare questo parametro.</span><span class="sxs-lookup"><span data-stu-id="5ee96-131">If the kind of Storage account is Storage, do not specify this parameter.</span></span>

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

### <span data-ttu-id="5ee96-132">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="5ee96-132">-AssignIdentity</span></span>
<span data-ttu-id="5ee96-133">Genera e assegna una nuova identità dell'account di archiviazione per l'account di archiviazione per l'uso con i servizi di gestione delle chiavi, ad esempio Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="5ee96-133">Generate and assign a new Storage Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="5ee96-134">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="5ee96-134">-CustomDomainName</span></span>
<span data-ttu-id="5ee96-135">Specifica il nome del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="5ee96-135">Specifies the name of the custom domain.</span></span>

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

### <span data-ttu-id="5ee96-136">-DisableEncryptionService</span><span class="sxs-lookup"><span data-stu-id="5ee96-136">-DisableEncryptionService</span></span>
<span data-ttu-id="5ee96-137">Indica se questo cmdlet disabilita la crittografia del servizio di archiviazione nel servizio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="5ee96-137">Indicates whether this cmdlet disables Storage Service encryption on the Storage Service.</span></span>
<span data-ttu-id="5ee96-138">Sono supportati i servizi file Azure BLOB e Azure.</span><span class="sxs-lookup"><span data-stu-id="5ee96-138">Azure Blob and Azure File Services are supported.</span></span>

```yaml
Type: EncryptionSupportServiceEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ee96-139">-EnableEncryptionService</span><span class="sxs-lookup"><span data-stu-id="5ee96-139">-EnableEncryptionService</span></span>
<span data-ttu-id="5ee96-140">Indica se questo cmdlet Abilita la crittografia del servizio di archiviazione nel servizio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="5ee96-140">Indicates whether this cmdlet enables Storage Service encryption on the Storage Service.</span></span>
<span data-ttu-id="5ee96-141">Sono supportati i servizi file Azure BLOB e Azure.</span><span class="sxs-lookup"><span data-stu-id="5ee96-141">Azure Blob and Azure File Services are supported.</span></span>

```yaml
Type: EncryptionSupportServiceEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ee96-142">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="5ee96-142">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="5ee96-143">Indica se l'account di archiviazione consente o meno solo il traffico HTTPS.</span><span class="sxs-lookup"><span data-stu-id="5ee96-143">Indicates whether or not the Storage Account only enable https traffic.</span></span>

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

### <span data-ttu-id="5ee96-144">-Force</span><span class="sxs-lookup"><span data-stu-id="5ee96-144">-Force</span></span>
<span data-ttu-id="5ee96-145">Se si modifica il livello di accesso, potrebbero essere presenti ulteriori addebiti.</span><span class="sxs-lookup"><span data-stu-id="5ee96-145">If you change the access tier, it may result in additional charges.</span></span>
<span data-ttu-id="5ee96-146">Per altre informazioni, vedere Archiviazione BLOB di Azure: livelli di archiviazione caldi e freddi https://go.microsoft.com/fwlink/?LinkId=786482 ( https://go.microsoft.com/fwlink/?LinkId=786482) .</span><span class="sxs-lookup"><span data-stu-id="5ee96-146">For more information, see Azure Blob Storage: Hot and cool storage tiershttps://go.microsoft.com/fwlink/?LinkId=786482 (https://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="5ee96-147">Se il tipo di account di archiviazione è lo spazio di archiviazione, non specificare questo parametro.</span><span class="sxs-lookup"><span data-stu-id="5ee96-147">If the kind of Storage account is Storage, do not specify this parameter.</span></span>

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

### <span data-ttu-id="5ee96-148">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="5ee96-148">-InformationAction</span></span>
<span data-ttu-id="5ee96-149">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="5ee96-149">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5ee96-150">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="5ee96-150">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5ee96-151">Continuare</span><span class="sxs-lookup"><span data-stu-id="5ee96-151">Continue</span></span>
- <span data-ttu-id="5ee96-152">Ignora</span><span class="sxs-lookup"><span data-stu-id="5ee96-152">Ignore</span></span>
- <span data-ttu-id="5ee96-153">Informarsi</span><span class="sxs-lookup"><span data-stu-id="5ee96-153">Inquire</span></span>
- <span data-ttu-id="5ee96-154">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5ee96-154">SilentlyContinue</span></span>
- <span data-ttu-id="5ee96-155">Stop</span><span class="sxs-lookup"><span data-stu-id="5ee96-155">Stop</span></span>
- <span data-ttu-id="5ee96-156">Sospensione</span><span class="sxs-lookup"><span data-stu-id="5ee96-156">Suspend</span></span>

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

### <span data-ttu-id="5ee96-157">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5ee96-157">-InformationVariable</span></span>
<span data-ttu-id="5ee96-158">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="5ee96-158">Specifies an information variable.</span></span>

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

### <span data-ttu-id="5ee96-159">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="5ee96-159">-KeyName</span></span>
<span data-ttu-id="5ee96-160">Nome del file di crittografia dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="5ee96-160">Storage Account encryption keySource KeyVault KeyName</span></span>

```yaml
Type: String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ee96-161">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="5ee96-161">-KeyvaultEncryption</span></span>
<span data-ttu-id="5ee96-162">Se impostare la fonte di crittografia dell'account di archiviazione su Microsoft. Vault o meno.</span><span class="sxs-lookup"><span data-stu-id="5ee96-162">Whether to set Storage Account Encryption KeySource to Microsoft.Keyvault or not.</span></span>
<span data-ttu-id="5ee96-163">Se specifichi il nome di codice, la versione di base e KeyvaultUri, la sorgente di crittografia dell'account di archiviazione sarà impostata anche su Microsoft. temporizzatore Meteo questo parametro è impostato o meno.</span><span class="sxs-lookup"><span data-stu-id="5ee96-163">If you specify KeyName, KeyVersion and KeyvaultUri, Storage Account encryption keySource will also be set to Microsoft.Keyvault weather this parameter is set or not.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: KeyvaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ee96-164">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="5ee96-164">-KeyVaultUri</span></span>
<span data-ttu-id="5ee96-165">Archiviazione dell'account di crittografia del codice sorgente di KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="5ee96-165">Storage Account encryption keySource KeyVault KeyVaultUri</span></span>

```yaml
Type: String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ee96-166">-Versione</span><span class="sxs-lookup"><span data-stu-id="5ee96-166">-KeyVersion</span></span>
<span data-ttu-id="5ee96-167">Crittografia dell'account di archiviazione della versione di base del Vault</span><span class="sxs-lookup"><span data-stu-id="5ee96-167">Storage Account encryption keySource KeyVault KeyVersion</span></span>

```yaml
Type: String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ee96-168">-Nome</span><span class="sxs-lookup"><span data-stu-id="5ee96-168">-Name</span></span>
<span data-ttu-id="5ee96-169">Specifica il nome dell'account di archiviazione da modificare.</span><span class="sxs-lookup"><span data-stu-id="5ee96-169">Specifies the name of the Storage account to Modify.</span></span>

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

### <span data-ttu-id="5ee96-170">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ee96-170">-ResourceGroupName</span></span>
<span data-ttu-id="5ee96-171">Specifica il nome del gruppo di risorse in cui modificare l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="5ee96-171">Specifies the name of the resource group in which to modify the Storage account.</span></span>

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

### <span data-ttu-id="5ee96-172">-SkuName</span><span class="sxs-lookup"><span data-stu-id="5ee96-172">-SkuName</span></span>
<span data-ttu-id="5ee96-173">Specifica il nome SKU dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="5ee96-173">Specifies the SKU name of the storage account.</span></span>
<span data-ttu-id="5ee96-174">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="5ee96-174">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5ee96-175">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="5ee96-175">Standard_LRS.</span></span>
<span data-ttu-id="5ee96-176">Spazio di archiviazione locale ridondante.</span><span class="sxs-lookup"><span data-stu-id="5ee96-176">Locally-redundant storage.</span></span>
- <span data-ttu-id="5ee96-177">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="5ee96-177">Standard_ZRS.</span></span>
<span data-ttu-id="5ee96-178">Area-archiviazione ridondante.</span><span class="sxs-lookup"><span data-stu-id="5ee96-178">Zone-redundant storage.</span></span>
- <span data-ttu-id="5ee96-179">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="5ee96-179">Standard_GRS.</span></span>
<span data-ttu-id="5ee96-180">Spazio di archiviazione Geo-ridondante.</span><span class="sxs-lookup"><span data-stu-id="5ee96-180">Geo-redundant storage.</span></span>
- <span data-ttu-id="5ee96-181">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="5ee96-181">Standard_RAGRS.</span></span>
<span data-ttu-id="5ee96-182">Accesso in lettura archiviazione Geo-ridondante.</span><span class="sxs-lookup"><span data-stu-id="5ee96-182">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="5ee96-183">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="5ee96-183">Premium_LRS.</span></span>
<span data-ttu-id="5ee96-184">Spazio di archiviazione locale ridondante Premium.</span><span class="sxs-lookup"><span data-stu-id="5ee96-184">Premium locally-redundant storage.</span></span>

<span data-ttu-id="5ee96-185">Non è possibile modificare i tipi di Standard_ZRS e Premium_LRS in altri tipi di account.</span><span class="sxs-lookup"><span data-stu-id="5ee96-185">You cannot change Standard_ZRS and Premium_LRS types to other account types.</span></span>
<span data-ttu-id="5ee96-186">Non è possibile modificare altri tipi di account in Standard_ZRS o Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="5ee96-186">You cannot change other account types to Standard_ZRS or Premium_LRS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ee96-187">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="5ee96-187">-StorageEncryption</span></span>
<span data-ttu-id="5ee96-188">Se impostare la fonte di crittografia dell'account di archiviazione in Microsoft. storage o meno.</span><span class="sxs-lookup"><span data-stu-id="5ee96-188">Whether to set Storage Account Encryption KeySource to Microsoft.Storage or not.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: StorageEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ee96-189">-Tag</span><span class="sxs-lookup"><span data-stu-id="5ee96-189">-Tag</span></span>
<span data-ttu-id="5ee96-190">Se specifichi un valore di BlobStorage per il parametro *Kind* del cmdlet New-AzureRmStorageAccount, devi specificare un valore per il parametro *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="5ee96-190">If you specify a value of BlobStorage for the *Kind* parameter of the New-AzureRmStorageAccount cmdlet, you must specify a value for the *AccessTier* parameter.</span></span>

<span data-ttu-id="5ee96-191">Se specifichi un valore di spazio di archiviazione per questo parametro di *tipo* , non specificare il parametro *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="5ee96-191">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ee96-192">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="5ee96-192">-UseSubDomain</span></span>
<span data-ttu-id="5ee96-193">Indica se abilitare la convalida CName indiretta.</span><span class="sxs-lookup"><span data-stu-id="5ee96-193">Indicates whether to enable indirect CName validation.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ee96-194">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5ee96-194">-Confirm</span></span>
<span data-ttu-id="5ee96-195">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ee96-195">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ee96-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ee96-196">-WhatIf</span></span>
<span data-ttu-id="5ee96-197">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5ee96-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ee96-198">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5ee96-198">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ee96-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ee96-199">CommonParameters</span></span>
<span data-ttu-id="5ee96-200">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ee96-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ee96-201">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ee96-201">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ee96-202">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5ee96-202">INPUTS</span></span>

### <span data-ttu-id="5ee96-203">Nessuno</span><span class="sxs-lookup"><span data-stu-id="5ee96-203">None</span></span>
<span data-ttu-id="5ee96-204">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="5ee96-204">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5ee96-205">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5ee96-205">OUTPUTS</span></span>

## <span data-ttu-id="5ee96-206">Note</span><span class="sxs-lookup"><span data-stu-id="5ee96-206">NOTES</span></span>

## <span data-ttu-id="5ee96-207">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5ee96-207">RELATED LINKS</span></span>

[<span data-ttu-id="5ee96-208">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5ee96-208">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="5ee96-209">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5ee96-209">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="5ee96-210">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5ee96-210">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)
