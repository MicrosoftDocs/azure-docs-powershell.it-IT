---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
ms.openlocfilehash: cab778247e6e3ae9db3549beae7fcd7495526757
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412096"
---
# <span data-ttu-id="d9a00-101">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d9a00-101">Get-AzKeyVaultKey</span></span>

## <span data-ttu-id="d9a00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9a00-102">SYNOPSIS</span></span>
<span data-ttu-id="d9a00-103">Recupera le chiavi del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="d9a00-103">Gets Key Vault keys.</span></span>

## <span data-ttu-id="d9a00-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d9a00-104">SYNTAX</span></span>

### <span data-ttu-id="d9a00-105">ByVaultName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d9a00-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9a00-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="d9a00-106">ByKeyName</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9a00-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="d9a00-107">ByKeyVersions</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9a00-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="d9a00-108">ByInputObjectVaultName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9a00-109">ByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="d9a00-109">ByInputObjectKeyName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9a00-110">ByInputObjectKeyVersions</span><span class="sxs-lookup"><span data-stu-id="d9a00-110">ByInputObjectKeyVersions</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9a00-111">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="d9a00-111">ByResourceIdVaultName</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9a00-112">ByResourceIdKeyName</span><span class="sxs-lookup"><span data-stu-id="d9a00-112">ByResourceIdKeyName</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9a00-113">ByResourceIdKeyVersions</span><span class="sxs-lookup"><span data-stu-id="d9a00-113">ByResourceIdKeyVersions</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9a00-114">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d9a00-114">DESCRIPTION</span></span>
<span data-ttu-id="d9a00-115">Il **cmdlet Get-AzKeyVaultKey** ottiene le chiavi del Vault della chiave di Azure.</span><span class="sxs-lookup"><span data-stu-id="d9a00-115">The **Get-AzKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="d9a00-116">Questo cmdlet ottiene uno specifico **oggetto Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** o un elenco di tutti gli oggetti **KeyBundle** in un vault delle chiavi o in base alla versione.</span><span class="sxs-lookup"><span data-stu-id="d9a00-116">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="d9a00-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d9a00-117">EXAMPLES</span></span>

### <span data-ttu-id="d9a00-118">Esempio 1: Ottenere tutte le chiavi in un vault delle chiavi</span><span class="sxs-lookup"><span data-stu-id="d9a00-118">Example 1: Get all the keys in a key vault</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso'

Vault Name     : contoso
Name           : test1
Version        :
Id             : https://contoso.vault.azure.net:443/keys/test1
Enabled        : True
Expires        : 11/24/2018 6:08:13 PM
Not Before     : 5/24/2018 5:58:13 PM
Created        : 5/24/2018 6:08:13 PM
Updated        : 5/24/2018 6:08:13 PM
Purge Disabled : False
Tags           :

Vault Name     : contoso
Name           : test2
Version        :
Id             : https://contoso.vault.azure.net:443/keys/test2
Enabled        : True
Expires        : 11/24/2018 6:09:44 PM
Not Before     : 5/24/2018 5:59:44 PM
Created        : 5/24/2018 6:09:44 PM
Updated        : 5/24/2018 6:09:44 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="d9a00-119">Questo comando recupera tutte le chiavi nel vault delle chiavi denominato Contoso.</span><span class="sxs-lookup"><span data-stu-id="d9a00-119">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="d9a00-120">Esempio 2: Ottenere la versione corrente di un codice</span><span class="sxs-lookup"><span data-stu-id="d9a00-120">Example 2: Get the current version of a key</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName 'test1'

Vault Name     : contoso
Name           : test1
Version        : 7fe415d5518240c1a6fce89986b8d334
Id             : https://contoso.vault.azure.net:443/keys/test1/7fe415d5518240c1a6fce89986b8d334
Enabled        : True
Expires        : 11/24/2018 6:08:13 PM
Not Before     : 5/24/2018 5:58:13 PM
Created        : 5/24/2018 6:08:13 PM
Updated        : 5/24/2018 6:08:13 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="d9a00-121">Questo comando ottiene la versione corrente della chiave denominata test1 nella chiave vault denominata Contoso.</span><span class="sxs-lookup"><span data-stu-id="d9a00-121">This command gets the current version of the key named test1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="d9a00-122">Esempio 3: Ottenere tutte le versioni di un codice</span><span class="sxs-lookup"><span data-stu-id="d9a00-122">Example 3: Get all versions of a key</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName 'test1' -IncludeVersions

Vault Name     : contoso
Name           : test1
Version        : 7fe415d5518240c1a6fce89986b8d334
Id             : https://contoso.vault.azure.net:443/keys/test1/7fe415d5518240c1a6fce89986b8d334
Enabled        : True
Expires        : 11/24/2018 6:08:13 PM
Not Before     : 5/24/2018 5:58:13 PM
Created        : 5/24/2018 6:08:13 PM
Updated        : 5/24/2018 6:08:13 PM
Purge Disabled : False
Tags           :

Vault Name     : contoso
Name           : test1
Version        : e4e95940e669407fbdb4298bc21a3e1d
Id             : https://contoso.vault.azure.net:443/keys/test1/e4e95940e669407fbdb4298bc21a3e1d
Enabled        : False
Expires        : 11/24/2018 6:08:08 PM
Not Before     : 5/24/2018 5:58:08 PM
Created        : 5/24/2018 6:08:08 PM
Updated        : 5/24/2018 6:08:08 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="d9a00-123">Questo comando recupera tutte le versioni della chiave denominata ITPfx nella chiave vaultnamed Contoso.</span><span class="sxs-lookup"><span data-stu-id="d9a00-123">This command gets all versions the key named ITPfx in the key vaultnamed Contoso.</span></span>

### <span data-ttu-id="d9a00-124">Esempio 4: Ottenere una versione specifica di una chiave</span><span class="sxs-lookup"><span data-stu-id="d9a00-124">Example 4: Get a specific version of a key</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName 'test1' -Version 'e4e95940e669407fbdb4298bc21a3e1d'

Vault Name     : contoso
Name           : test1
Version        : e4e95940e669407fbdb4298bc21a3e1d
Id             : https://contoso.vault.azure.net:443/keys/test1/e4e95940e669407fbdb4298bc21a3e1d
Enabled        : False
Expires        : 11/24/2018 6:08:08 PM
Not Before     : 5/24/2018 5:58:08 PM
Created        : 5/24/2018 6:08:08 PM
Updated        : 5/24/2018 6:08:08 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="d9a00-125">Questo comando ottiene una versione specifica della chiave denominata test1 nella chiave vault denominata Contoso.</span><span class="sxs-lookup"><span data-stu-id="d9a00-125">This command gets a specific version of the key named test1 in the key vault named Contoso.</span></span>
<span data-ttu-id="d9a00-126">Dopo aver eseguito questo comando, è possibile esaminare le varie proprietà della chiave spostandosi sull$Key o object.</span><span class="sxs-lookup"><span data-stu-id="d9a00-126">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="d9a00-127">Esempio 5: Ottenere tutte le chiavi eliminate ma non eliminate per il vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="d9a00-127">Example 5: Get all the keys that have been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -InRemovedState

Vault Name           : contoso
Name                 : test3
Id                   : https://contoso.vault.azure.net:443/keys/test3
Deleted Date         : 5/24/2018 8:32:42 PM
Scheduled Purge Date : 8/22/2018 8:32:42 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 5/24/2018 8:32:27 PM
Updated              : 5/24/2018 8:32:27 PM
Purge Disabled       : False
Tags                 :
```

<span data-ttu-id="d9a00-128">Questo comando recupera tutte le chiavi eliminate in precedenza, ma non eliminate, nella chiave vault denominata Contoso.</span><span class="sxs-lookup"><span data-stu-id="d9a00-128">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="d9a00-129">Esempio 6: ottiene la chiave ITPfx che è stata eliminata ma non eliminata per il vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="d9a00-129">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName 'test3' -InRemovedState

Vault Name           : contoso
Name                 : test3
Id                   : https://contoso.vault.azure.net:443/keys/test3/1af807cc331a49d0b52b7c75e1b2366e
Deleted Date         : 5/24/2018 8:32:42 PM
Scheduled Purge Date : 8/22/2018 8:32:42 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 5/24/2018 8:32:27 PM
Updated              : 5/24/2018 8:32:27 PM
Purge Disabled       : False
Tags                 :
```

<span data-ttu-id="d9a00-130">Questo comando ottiene il test della chiave3 eliminato in precedenza, ma non ripulito, nella chiave vault denominata Contoso.</span><span class="sxs-lookup"><span data-stu-id="d9a00-130">This command gets the key test3 that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="d9a00-131">Questo comando restituisce metadati come la data di eliminazione e la data di eliminazione pianificata della chiave eliminata.</span><span class="sxs-lookup"><span data-stu-id="d9a00-131">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

### <span data-ttu-id="d9a00-132">Esempio 7: Ottenere tutte le chiavi in un vault delle chiavi usando i filtri</span><span class="sxs-lookup"><span data-stu-id="d9a00-132">Example 7: Get all the keys in a key vault using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName "test*"

Vault Name     : contoso
Name           : test1
Version        :
Id             : https://contoso.vault.azure.net:443/keys/test1
Enabled        : True
Expires        : 11/24/2018 6:08:13 PM
Not Before     : 5/24/2018 5:58:13 PM
Created        : 5/24/2018 6:08:13 PM
Updated        : 5/24/2018 6:08:13 PM
Purge Disabled : False
Tags           :

Vault Name     : contoso
Name           : test2
Version        :
Id             : https://contoso.vault.azure.net:443/keys/test2
Enabled        : True
Expires        : 11/24/2018 6:09:44 PM
Not Before     : 5/24/2018 5:59:44 PM
Created        : 5/24/2018 6:09:44 PM
Updated        : 5/24/2018 6:09:44 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="d9a00-133">Questo comando recupera tutte le chiavi nel vault delle chiavi denominate Contoso che iniziano con "test".</span><span class="sxs-lookup"><span data-stu-id="d9a00-133">This command gets all the keys in the key vault named Contoso that start with "test".</span></span>

## <span data-ttu-id="d9a00-134">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9a00-134">PARAMETERS</span></span>

### <span data-ttu-id="d9a00-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9a00-135">-DefaultProfile</span></span>
<span data-ttu-id="d9a00-136">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="d9a00-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9a00-137">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="d9a00-137">-IncludeVersions</span></span>
<span data-ttu-id="d9a00-138">Indica che questo cmdlet ottiene tutte le versioni di una chiave.</span><span class="sxs-lookup"><span data-stu-id="d9a00-138">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="d9a00-139">La versione corrente di un codice è la prima nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="d9a00-139">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="d9a00-140">Se si specifica questo parametro, è necessario specificare anche i *parametri Name* e *VaultName.*</span><span class="sxs-lookup"><span data-stu-id="d9a00-140">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="d9a00-141">Se non si specifica il *parametro IncludeVersions,* questo cmdlet ottiene la versione corrente della chiave con il nome *specificato.*</span><span class="sxs-lookup"><span data-stu-id="d9a00-141">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByKeyVersions, ByInputObjectKeyVersions, ByResourceIdKeyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a00-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9a00-142">-InputObject</span></span>
<span data-ttu-id="d9a00-143">Oggetto KeyVault.</span><span class="sxs-lookup"><span data-stu-id="d9a00-143">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObjectVaultName, ByInputObjectKeyName, ByInputObjectKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9a00-144">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="d9a00-144">-InRemovedState</span></span>
<span data-ttu-id="d9a00-145">Specifica se visualizzare le chiavi eliminate in precedenza nell'output</span><span class="sxs-lookup"><span data-stu-id="d9a00-145">Specifies whether to show the previously deleted keys in the output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByVaultName, ByInputObjectVaultName, ByResourceIdVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a00-146">-Name</span><span class="sxs-lookup"><span data-stu-id="d9a00-146">-Name</span></span>
<span data-ttu-id="d9a00-147">Specifica il nome del bundle di chiavi da ottenere.</span><span class="sxs-lookup"><span data-stu-id="d9a00-147">Specifies the name of the key bundle to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, ByInputObjectVaultName, ByResourceIdVaultName
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByKeyName, ByKeyVersions, ByInputObjectKeyName, ByInputObjectKeyVersions, ByResourceIdKeyName, ByResourceIdKeyVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a00-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9a00-148">-ResourceId</span></span>
<span data-ttu-id="d9a00-149">ID risorsa KeyVault.</span><span class="sxs-lookup"><span data-stu-id="d9a00-149">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdVaultName, ByResourceIdKeyName, ByResourceIdKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9a00-150">-VaultName</span><span class="sxs-lookup"><span data-stu-id="d9a00-150">-VaultName</span></span>
<span data-ttu-id="d9a00-151">Specifica il nome del vault delle chiavi da cui il cmdlet ottiene le chiavi.</span><span class="sxs-lookup"><span data-stu-id="d9a00-151">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="d9a00-152">Questo cmdlet crea il nome di dominio completo (FQDN) di un vault delle chiavi in base al nome specificato da questo parametro e all'ambiente selezionato.</span><span class="sxs-lookup"><span data-stu-id="d9a00-152">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, ByKeyName, ByKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a00-153">-Version</span><span class="sxs-lookup"><span data-stu-id="d9a00-153">-Version</span></span>
<span data-ttu-id="d9a00-154">Specifica la versione chiave.</span><span class="sxs-lookup"><span data-stu-id="d9a00-154">Specifies the key version.</span></span>
<span data-ttu-id="d9a00-155">Questo cmdlet crea l'FQDN di una chiave in base al nome del vault della chiave, all'ambiente attualmente selezionato, al nome della chiave e alla versione della chiave.</span><span class="sxs-lookup"><span data-stu-id="d9a00-155">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName, ByInputObjectKeyName, ByResourceIdKeyName
Aliases: KeyVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a00-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9a00-156">CommonParameters</span></span>
<span data-ttu-id="d9a00-157">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9a00-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9a00-158">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d9a00-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9a00-159">INPUT</span><span class="sxs-lookup"><span data-stu-id="d9a00-159">INPUTS</span></span>

### <span data-ttu-id="d9a00-160">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="d9a00-160">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="d9a00-161">System.String</span><span class="sxs-lookup"><span data-stu-id="d9a00-161">System.String</span></span>

## <span data-ttu-id="d9a00-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d9a00-162">OUTPUTS</span></span>

### <span data-ttu-id="d9a00-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="d9a00-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="d9a00-164">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d9a00-164">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

### <span data-ttu-id="d9a00-165">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="d9a00-165">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="d9a00-166">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d9a00-166">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="d9a00-167">NOTE</span><span class="sxs-lookup"><span data-stu-id="d9a00-167">NOTES</span></span>

## <span data-ttu-id="d9a00-168">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d9a00-168">RELATED LINKS</span></span>

[<span data-ttu-id="d9a00-169">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d9a00-169">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="d9a00-170">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d9a00-170">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="d9a00-171">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="d9a00-171">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)


