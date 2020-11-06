---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Set-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Set-AzureRmStorageAccount.md
ms.openlocfilehash: 5ca65c09746f6bb9a050c14fe10987702465b484
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515944"
---
# <span data-ttu-id="878a0-101">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="878a0-101">Set-AzureRmStorageAccount</span></span>

## <span data-ttu-id="878a0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="878a0-102">SYNOPSIS</span></span>
<span data-ttu-id="878a0-103">Modifica un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="878a0-103">Modifies a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="878a0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="878a0-104">SYNTAX</span></span>

### <span data-ttu-id="878a0-105">StorageEncryption (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="878a0-105">StorageEncryption (Default)</span></span>
```
Set-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [[-SkuName] <String>]
 [[-AccessTier] <String>] [[-CustomDomainName] <String>] [[-UseSubDomain] <Boolean>]
 [[-EnableEncryptionService] <EncryptionSupportServiceEnum>]
 [[-DisableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="878a0-106">KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="878a0-106">KeyvaultEncryption</span></span>
```
Set-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [[-SkuName] <String>]
 [[-AccessTier] <String>] [[-CustomDomainName] <String>] [[-UseSubDomain] <Boolean>]
 [[-EnableEncryptionService] <EncryptionSupportServiceEnum>]
 [[-DisableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="878a0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="878a0-107">DESCRIPTION</span></span>
<span data-ttu-id="878a0-108">Il cmdlet **set-AzureRmStorageAccount** modifica un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="878a0-108">The **Set-AzureRmStorageAccount** cmdlet modifies an Azure Storage account.</span></span>
<span data-ttu-id="878a0-109">Puoi usare questo cmdlet per modificare il tipo di account, aggiornare un dominio del cliente o impostare i contrassegni in un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="878a0-109">You can use this cmdlet to modify the account type, update a customer domain, or set tags on a Storage account.</span></span>

## <span data-ttu-id="878a0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="878a0-110">EXAMPLES</span></span>

### <span data-ttu-id="878a0-111">Esempio 1: impostare il tipo di account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="878a0-111">Example 1: Set the Storage account type</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Type "Standard_RAGRS"
```

<span data-ttu-id="878a0-112">Questo comando imposta il tipo di account di archiviazione su Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="878a0-112">This command sets the Storage account type to Standard_RAGRS.</span></span>

### <span data-ttu-id="878a0-113">Esempio 2: impostare un dominio personalizzato per un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="878a0-113">Example 2: Set a custom domain for a Storage account</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

<span data-ttu-id="878a0-114">Questo comando imposta un dominio personalizzato per un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="878a0-114">This command sets a custom domain for a Storage account.</span></span>

### <span data-ttu-id="878a0-115">Esempio 3: abilitare la crittografia per i servizi BLOB e file</span><span class="sxs-lookup"><span data-stu-id="878a0-115">Example 3: Enable encryption on Blob and File Services</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -EnableEncryptionService "Blob,File"
```

<span data-ttu-id="878a0-116">Questo comando consente la crittografia del servizio di archiviazione su BLOB e file per un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="878a0-116">This command enables Storage Service encryption on Blob and File for a Storage account.</span></span>

### <span data-ttu-id="878a0-117">Esempio 4: impostare il valore di livello di accesso</span><span class="sxs-lookup"><span data-stu-id="878a0-117">Example 4: Set the access tier value</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -AccessTier Cool
```

<span data-ttu-id="878a0-118">Il comando imposta il valore di livello di Access come cool.</span><span class="sxs-lookup"><span data-stu-id="878a0-118">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="878a0-119">Esempio 4: impostare il dominio e i tag personalizzati</span><span class="sxs-lookup"><span data-stu-id="878a0-119">Example 4: Set the custom domain and tags</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="878a0-120">Il comando imposta il valore di livello di Access come cool.</span><span class="sxs-lookup"><span data-stu-id="878a0-120">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="878a0-121">Esempio 5: abilitare la crittografia nei servizi BLOB con il Vault</span><span class="sxs-lookup"><span data-stu-id="878a0-121">Example 5: Enable encryption on Blob Services with Keyvault</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -AssignIdentity
PS C:\>$account = Get-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount"

PS C:\>$keyVault = New-AzureRmKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzureKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey

PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -EnableEncryptionService "Blob" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

<span data-ttu-id="878a0-122">Questo comando consente la crittografia del servizio di archiviazione su BLOB con un nuovo Vault creato.</span><span class="sxs-lookup"><span data-stu-id="878a0-122">This command enables Storage Service encryption on Blob with a new created Keyvault.</span></span>

### <span data-ttu-id="878a0-123">Esempio 6: disabilitare la crittografia in Servizi file con la sorgente di origine impostata su "Microsoft. storage"</span><span class="sxs-lookup"><span data-stu-id="878a0-123">Example 6: Disable encryption on File Services with KeySource set to "Microsoft.Storage"</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -DisableEncryptionService File  -StorageEncryption
```

<span data-ttu-id="878a0-124">Questo comando Disabilita la crittografia in Servizi file con la sorgente di origine impostata su "Microsoft. storage"</span><span class="sxs-lookup"><span data-stu-id="878a0-124">This command disables encryption on File Services with KeySource set to "Microsoft.Storage"</span></span>

## <span data-ttu-id="878a0-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="878a0-125">PARAMETERS</span></span>

### <span data-ttu-id="878a0-126">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="878a0-126">-AccessTier</span></span>
<span data-ttu-id="878a0-127">Specifica il livello di accesso dell'account di archiviazione modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="878a0-127">Specifies the access tier of the Storage account that this cmdlet modifies.</span></span>
<span data-ttu-id="878a0-128">I valori accettabili per questo parametro sono: caldo e freddo.</span><span class="sxs-lookup"><span data-stu-id="878a0-128">The acceptable values for this parameter are: Hot and Cool.</span></span>

<span data-ttu-id="878a0-129">Se si modifica il livello di accesso, potrebbero essere presenti ulteriori addebiti.</span><span class="sxs-lookup"><span data-stu-id="878a0-129">If you change the access tier, it may result in additional charges.</span></span>
<span data-ttu-id="878a0-130">Per altre informazioni, vedere Archiviazione BLOB di Azure: livelli di archiviazione caldi e freddi https://go.microsoft.com/fwlink/?LinkId=786482 ( https://go.microsoft.com/fwlink/?LinkId=786482) .</span><span class="sxs-lookup"><span data-stu-id="878a0-130">For more information, see Azure Blob Storage: Hot and cool storage tiershttps://go.microsoft.com/fwlink/?LinkId=786482 (https://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="878a0-131">Se il tipo di account di archiviazione è lo spazio di archiviazione, non specificare questo parametro.</span><span class="sxs-lookup"><span data-stu-id="878a0-131">If the kind of Storage account is Storage, do not specify this parameter.</span></span>

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

### <span data-ttu-id="878a0-132">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="878a0-132">-AssignIdentity</span></span>
<span data-ttu-id="878a0-133">Genera e assegna una nuova identità dell'account di archiviazione per l'account di archiviazione per l'uso con i servizi di gestione delle chiavi, ad esempio Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="878a0-133">Generate and assign a new Storage Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="878a0-134">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="878a0-134">-CustomDomainName</span></span>
<span data-ttu-id="878a0-135">Specifica il nome del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="878a0-135">Specifies the name of the custom domain.</span></span>

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

### <span data-ttu-id="878a0-136">-DisableEncryptionService</span><span class="sxs-lookup"><span data-stu-id="878a0-136">-DisableEncryptionService</span></span>
<span data-ttu-id="878a0-137">Indica se questo cmdlet disabilita la crittografia del servizio di archiviazione nel servizio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="878a0-137">Indicates whether this cmdlet disables Storage Service encryption on the Storage Service.</span></span>
<span data-ttu-id="878a0-138">Sono supportati i servizi file Azure BLOB e Azure.</span><span class="sxs-lookup"><span data-stu-id="878a0-138">Azure Blob and Azure File Services are supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Storage.StorageAccountBaseCmdlet+EncryptionSupportServiceEnum]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="878a0-139">-EnableEncryptionService</span><span class="sxs-lookup"><span data-stu-id="878a0-139">-EnableEncryptionService</span></span>
<span data-ttu-id="878a0-140">Indica se questo cmdlet Abilita la crittografia del servizio di archiviazione nel servizio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="878a0-140">Indicates whether this cmdlet enables Storage Service encryption on the Storage Service.</span></span>
<span data-ttu-id="878a0-141">Sono supportati i servizi file Azure BLOB e Azure.</span><span class="sxs-lookup"><span data-stu-id="878a0-141">Azure Blob and Azure File Services are supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Storage.StorageAccountBaseCmdlet+EncryptionSupportServiceEnum]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="878a0-142">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="878a0-142">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="878a0-143">Indica se l'account di archiviazione consente o meno solo il traffico HTTPS.</span><span class="sxs-lookup"><span data-stu-id="878a0-143">Indicates whether or not the Storage Account only enable https traffic.</span></span>

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

### <span data-ttu-id="878a0-144">-Force</span><span class="sxs-lookup"><span data-stu-id="878a0-144">-Force</span></span>
<span data-ttu-id="878a0-145">Se si modifica il livello di accesso, potrebbero essere presenti ulteriori addebiti.</span><span class="sxs-lookup"><span data-stu-id="878a0-145">If you change the access tier, it may result in additional charges.</span></span>
<span data-ttu-id="878a0-146">Per altre informazioni, vedere Archiviazione BLOB di Azure: livelli di archiviazione caldi e freddi https://go.microsoft.com/fwlink/?LinkId=786482 ( https://go.microsoft.com/fwlink/?LinkId=786482) .</span><span class="sxs-lookup"><span data-stu-id="878a0-146">For more information, see Azure Blob Storage: Hot and cool storage tiershttps://go.microsoft.com/fwlink/?LinkId=786482 (https://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="878a0-147">Se il tipo di account di archiviazione è lo spazio di archiviazione, non specificare questo parametro.</span><span class="sxs-lookup"><span data-stu-id="878a0-147">If the kind of Storage account is Storage, do not specify this parameter.</span></span>

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

### <span data-ttu-id="878a0-148">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="878a0-148">-InformationAction</span></span>
<span data-ttu-id="878a0-149">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="878a0-149">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="878a0-150">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="878a0-150">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="878a0-151">Continuare</span><span class="sxs-lookup"><span data-stu-id="878a0-151">Continue</span></span>
- <span data-ttu-id="878a0-152">Ignora</span><span class="sxs-lookup"><span data-stu-id="878a0-152">Ignore</span></span>
- <span data-ttu-id="878a0-153">Informarsi</span><span class="sxs-lookup"><span data-stu-id="878a0-153">Inquire</span></span>
- <span data-ttu-id="878a0-154">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="878a0-154">SilentlyContinue</span></span>
- <span data-ttu-id="878a0-155">Stop</span><span class="sxs-lookup"><span data-stu-id="878a0-155">Stop</span></span>
- <span data-ttu-id="878a0-156">Sospensione</span><span class="sxs-lookup"><span data-stu-id="878a0-156">Suspend</span></span>

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

### <span data-ttu-id="878a0-157">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="878a0-157">-InformationVariable</span></span>
<span data-ttu-id="878a0-158">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="878a0-158">Specifies an information variable.</span></span>

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

### <span data-ttu-id="878a0-159">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="878a0-159">-KeyName</span></span>
<span data-ttu-id="878a0-160">Nome del file di crittografia dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="878a0-160">Storage Account encryption keySource KeyVault KeyName</span></span>

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

### <span data-ttu-id="878a0-161">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="878a0-161">-KeyvaultEncryption</span></span>
<span data-ttu-id="878a0-162">Se impostare la fonte di crittografia dell'account di archiviazione su Microsoft. Vault o meno.</span><span class="sxs-lookup"><span data-stu-id="878a0-162">Whether to set Storage Account Encryption KeySource to Microsoft.Keyvault or not.</span></span> <span data-ttu-id="878a0-163">Se specifichi il nome di codice, la versione di base e KeyvaultUri, la sorgente di crittografia dell'account di archiviazione sarà impostata anche su Microsoft. temporizzatore Meteo questo parametro è impostato o meno.</span><span class="sxs-lookup"><span data-stu-id="878a0-163">If you specify KeyName, KeyVersion and KeyvaultUri, Storage Account encryption keySource will also be set to Microsoft.Keyvault weather this parameter is set or not.</span></span>
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

### <span data-ttu-id="878a0-164">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="878a0-164">-KeyVaultUri</span></span>
<span data-ttu-id="878a0-165">Archiviazione dell'account di crittografia del codice sorgente di KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="878a0-165">Storage Account encryption keySource KeyVault KeyVaultUri</span></span>

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

### <span data-ttu-id="878a0-166">-Versione</span><span class="sxs-lookup"><span data-stu-id="878a0-166">-KeyVersion</span></span>
<span data-ttu-id="878a0-167">Crittografia dell'account di archiviazione della versione di base del Vault</span><span class="sxs-lookup"><span data-stu-id="878a0-167">Storage Account encryption keySource KeyVault KeyVersion</span></span>

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

### <span data-ttu-id="878a0-168">-Nome</span><span class="sxs-lookup"><span data-stu-id="878a0-168">-Name</span></span>
<span data-ttu-id="878a0-169">Specifica il nome dell'account di archiviazione da modificare.</span><span class="sxs-lookup"><span data-stu-id="878a0-169">Specifies the name of the Storage account to Modify.</span></span>

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

### <span data-ttu-id="878a0-170">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="878a0-170">-NetworkRuleSet</span></span>
<span data-ttu-id="878a0-171">NetworkRuleSet account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="878a0-171">Storage Account NetworkRuleSet</span></span>

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

### <span data-ttu-id="878a0-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="878a0-172">-ResourceGroupName</span></span>
<span data-ttu-id="878a0-173">Specifica il nome del gruppo di risorse in cui modificare l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="878a0-173">Specifies the name of the resource group in which to modify the Storage account.</span></span>

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

### <span data-ttu-id="878a0-174">-SkuName</span><span class="sxs-lookup"><span data-stu-id="878a0-174">-SkuName</span></span>
<span data-ttu-id="878a0-175">Specifica il nome SKU dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="878a0-175">Specifies the SKU name of the storage account.</span></span>
<span data-ttu-id="878a0-176">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="878a0-176">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="878a0-177">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="878a0-177">Standard_LRS.</span></span>
<span data-ttu-id="878a0-178">Spazio di archiviazione locale ridondante.</span><span class="sxs-lookup"><span data-stu-id="878a0-178">Locally-redundant storage.</span></span> 
- <span data-ttu-id="878a0-179">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="878a0-179">Standard_ZRS.</span></span>
<span data-ttu-id="878a0-180">Area-archiviazione ridondante.</span><span class="sxs-lookup"><span data-stu-id="878a0-180">Zone-redundant storage.</span></span>
- <span data-ttu-id="878a0-181">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="878a0-181">Standard_GRS.</span></span>
<span data-ttu-id="878a0-182">Spazio di archiviazione Geo-ridondante.</span><span class="sxs-lookup"><span data-stu-id="878a0-182">Geo-redundant storage.</span></span> 
- <span data-ttu-id="878a0-183">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="878a0-183">Standard_RAGRS.</span></span>
<span data-ttu-id="878a0-184">Accesso in lettura archiviazione Geo-ridondante.</span><span class="sxs-lookup"><span data-stu-id="878a0-184">Read access geo-redundant storage.</span></span> 
- <span data-ttu-id="878a0-185">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="878a0-185">Premium_LRS.</span></span>
<span data-ttu-id="878a0-186">Spazio di archiviazione locale ridondante Premium.</span><span class="sxs-lookup"><span data-stu-id="878a0-186">Premium locally-redundant storage.</span></span>

<span data-ttu-id="878a0-187">Non è possibile modificare i tipi di Standard_ZRS e Premium_LRS in altri tipi di account.</span><span class="sxs-lookup"><span data-stu-id="878a0-187">You cannot change Standard_ZRS and Premium_LRS types to other account types.</span></span>
<span data-ttu-id="878a0-188">Non è possibile modificare altri tipi di account in Standard_ZRS o Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="878a0-188">You cannot change other account types to Standard_ZRS or Premium_LRS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="878a0-189">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="878a0-189">-StorageEncryption</span></span>
<span data-ttu-id="878a0-190">Se impostare la fonte di crittografia dell'account di archiviazione in Microsoft. storage o meno.</span><span class="sxs-lookup"><span data-stu-id="878a0-190">Whether to set Storage Account Encryption KeySource to Microsoft.Storage or not.</span></span>

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

### <span data-ttu-id="878a0-191">-Tag</span><span class="sxs-lookup"><span data-stu-id="878a0-191">-Tag</span></span>
<span data-ttu-id="878a0-192">Se specifichi un valore di BlobStorage per il parametro *Kind* del cmdlet New-AzureRmStorageAccount, devi specificare un valore per il parametro *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="878a0-192">If you specify a value of BlobStorage for the *Kind* parameter of the New-AzureRmStorageAccount cmdlet, you must specify a value for the *AccessTier* parameter.</span></span>

<span data-ttu-id="878a0-193">Se specifichi un valore di spazio di archiviazione per questo parametro di *tipo* , non specificare il parametro *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="878a0-193">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="878a0-194">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="878a0-194">-UseSubDomain</span></span>
<span data-ttu-id="878a0-195">Indica se abilitare la convalida CName indiretta.</span><span class="sxs-lookup"><span data-stu-id="878a0-195">Indicates whether to enable indirect CName validation.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="878a0-196">-Confermare</span><span class="sxs-lookup"><span data-stu-id="878a0-196">-Confirm</span></span>
<span data-ttu-id="878a0-197">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="878a0-197">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="878a0-198">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="878a0-198">-WhatIf</span></span>
<span data-ttu-id="878a0-199">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="878a0-199">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="878a0-200">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="878a0-200">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="878a0-201">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="878a0-201">-DefaultProfile</span></span>
<span data-ttu-id="878a0-202">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="878a0-202">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="878a0-203">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="878a0-203">CommonParameters</span></span>
<span data-ttu-id="878a0-204">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="878a0-204">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="878a0-205">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="878a0-205">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="878a0-206">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="878a0-206">INPUTS</span></span>

## <span data-ttu-id="878a0-207">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="878a0-207">OUTPUTS</span></span>

## <span data-ttu-id="878a0-208">Note</span><span class="sxs-lookup"><span data-stu-id="878a0-208">NOTES</span></span>

## <span data-ttu-id="878a0-209">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="878a0-209">RELATED LINKS</span></span>

[<span data-ttu-id="878a0-210">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="878a0-210">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="878a0-211">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="878a0-211">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="878a0-212">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="878a0-212">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)


