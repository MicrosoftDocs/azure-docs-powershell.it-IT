---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
ms.openlocfilehash: 21d2f6efa039dbd9b229562fcefd53c715f400fe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835744"
---
# <span data-ttu-id="a511e-101">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a511e-101">Get-AzKeyVaultKey</span></span>

## <span data-ttu-id="a511e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a511e-102">SYNOPSIS</span></span>
<span data-ttu-id="a511e-103">Ottiene le chiavi di volta chiave.</span><span class="sxs-lookup"><span data-stu-id="a511e-103">Gets Key Vault keys.</span></span>

## <span data-ttu-id="a511e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a511e-104">SYNTAX</span></span>

### <span data-ttu-id="a511e-105">ByVaultName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a511e-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a511e-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="a511e-106">ByKeyName</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a511e-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="a511e-107">ByKeyVersions</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a511e-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="a511e-108">ByInputObjectVaultName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a511e-109">ByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="a511e-109">ByInputObjectKeyName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a511e-110">ByInputObjectKeyVersions</span><span class="sxs-lookup"><span data-stu-id="a511e-110">ByInputObjectKeyVersions</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a511e-111">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="a511e-111">ByResourceIdVaultName</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a511e-112">ByResourceIdKeyName</span><span class="sxs-lookup"><span data-stu-id="a511e-112">ByResourceIdKeyName</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a511e-113">ByResourceIdKeyVersions</span><span class="sxs-lookup"><span data-stu-id="a511e-113">ByResourceIdKeyVersions</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a511e-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a511e-114">DESCRIPTION</span></span>
<span data-ttu-id="a511e-115">Il cmdlet **Get-AzKeyVaultKey** ottiene le chiavi di volta di Azure Key.</span><span class="sxs-lookup"><span data-stu-id="a511e-115">The **Get-AzKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="a511e-116">Questo cmdlet consente di ottenere uno specifico **Microsoft. Azure. Commands. Key Vault. Models. bundle** o un elenco di tutti gli oggetti del **pacchetto** di chiavi in un Vault chiave o in base alla versione.</span><span class="sxs-lookup"><span data-stu-id="a511e-116">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="a511e-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a511e-117">EXAMPLES</span></span>

### <span data-ttu-id="a511e-118">Esempio 1: ottenere tutte le chiavi in un Vault chiave</span><span class="sxs-lookup"><span data-stu-id="a511e-118">Example 1: Get all the keys in a key vault</span></span>
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

<span data-ttu-id="a511e-119">Questo comando consente di ottenere tutte le chiavi nel caveau della chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="a511e-119">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="a511e-120">Esempio 2: ottenere la versione corrente di una chiave</span><span class="sxs-lookup"><span data-stu-id="a511e-120">Example 2: Get the current version of a key</span></span>
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

<span data-ttu-id="a511e-121">Questo comando ottiene la versione corrente della chiave denominata Test1 nel caveau della chiave denominata Contoso.</span><span class="sxs-lookup"><span data-stu-id="a511e-121">This command gets the current version of the key named test1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="a511e-122">Esempio 3: ottenere tutte le versioni di una chiave</span><span class="sxs-lookup"><span data-stu-id="a511e-122">Example 3: Get all versions of a key</span></span>
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

<span data-ttu-id="a511e-123">Questo comando consente di ottenere tutte le versioni della chiave denominata ITPfx nella chiave vaultnamed contoso.</span><span class="sxs-lookup"><span data-stu-id="a511e-123">This command gets all versions the key named ITPfx in the key vaultnamed Contoso.</span></span>

### <span data-ttu-id="a511e-124">Esempio 4: ottenere una versione specifica di una chiave</span><span class="sxs-lookup"><span data-stu-id="a511e-124">Example 4: Get a specific version of a key</span></span>
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

<span data-ttu-id="a511e-125">Questo comando ottiene una versione specifica della chiave denominata Test1 nel caveau della chiave denominata Contoso.</span><span class="sxs-lookup"><span data-stu-id="a511e-125">This command gets a specific version of the key named test1 in the key vault named Contoso.</span></span>
<span data-ttu-id="a511e-126">Dopo aver eseguito questo comando, è possibile esaminare varie proprietà della chiave spostando l'oggetto $Key.</span><span class="sxs-lookup"><span data-stu-id="a511e-126">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="a511e-127">Esempio 5: ottenere tutte le chiavi eliminate ma non eliminate per questo Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="a511e-127">Example 5: Get all the keys that have been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="a511e-128">Questo comando consente di ottenere tutte le chiavi eliminate in precedenza, ma non eliminate, nel caveau della chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="a511e-128">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="a511e-129">Esempio 6: ottiene la chiave ITPfx che è stata eliminata ma non eliminata per il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="a511e-129">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="a511e-130">Questo comando ottiene la chiave test3 che è stata eliminata, ma non eliminata, nel caveau della chiave denominata Contoso.</span><span class="sxs-lookup"><span data-stu-id="a511e-130">This command gets the key test3 that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="a511e-131">Questo comando restituirà metadati, ad esempio la data di eliminazione, e la data di eliminazione pianificata di questa chiave eliminata.</span><span class="sxs-lookup"><span data-stu-id="a511e-131">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

### <span data-ttu-id="a511e-132">Esempio 7: ottenere tutte le chiavi in un Vault chiave usando il filtro</span><span class="sxs-lookup"><span data-stu-id="a511e-132">Example 7: Get all the keys in a key vault using filtering</span></span>
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

<span data-ttu-id="a511e-133">Questo comando ottiene tutte le chiavi nel Vault chiave denominato Contoso che iniziano con "test".</span><span class="sxs-lookup"><span data-stu-id="a511e-133">This command gets all the keys in the key vault named Contoso that start with "test".</span></span>

## <span data-ttu-id="a511e-134">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a511e-134">PARAMETERS</span></span>

### <span data-ttu-id="a511e-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a511e-135">-DefaultProfile</span></span>
<span data-ttu-id="a511e-136">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a511e-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a511e-137">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="a511e-137">-IncludeVersions</span></span>
<span data-ttu-id="a511e-138">Indica che questo cmdlet ottiene tutte le versioni di una chiave.</span><span class="sxs-lookup"><span data-stu-id="a511e-138">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="a511e-139">La versione corrente di una chiave è la prima nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="a511e-139">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="a511e-140">Se specifichi questo parametro devi anche specificare i parametri *Name* e *VAULTNAME* .</span><span class="sxs-lookup"><span data-stu-id="a511e-140">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="a511e-141">Se non specifichi il parametro *includeVersions* , questo cmdlet ottiene la versione corrente della chiave con il *nome* specificato.</span><span class="sxs-lookup"><span data-stu-id="a511e-141">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

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

### <span data-ttu-id="a511e-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a511e-142">-InputObject</span></span>
<span data-ttu-id="a511e-143">Oggetto di Vault.</span><span class="sxs-lookup"><span data-stu-id="a511e-143">KeyVault object.</span></span>

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

### <span data-ttu-id="a511e-144">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="a511e-144">-InRemovedState</span></span>
<span data-ttu-id="a511e-145">Specifica se visualizzare le chiavi eliminate in precedenza nell'output</span><span class="sxs-lookup"><span data-stu-id="a511e-145">Specifies whether to show the previously deleted keys in the output</span></span>

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

### <span data-ttu-id="a511e-146">-Nome</span><span class="sxs-lookup"><span data-stu-id="a511e-146">-Name</span></span>
<span data-ttu-id="a511e-147">Specifica il nome del bundle della chiave da ottenere.</span><span class="sxs-lookup"><span data-stu-id="a511e-147">Specifies the name of the key bundle to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, ByInputObjectVaultName, ByResourceIdVaultName
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ByKeyName, ByKeyVersions, ByInputObjectKeyName, ByInputObjectKeyVersions, ByResourceIdKeyName, ByResourceIdKeyVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="a511e-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a511e-148">-ResourceId</span></span>
<span data-ttu-id="a511e-149">ID risorsa di un Vault.</span><span class="sxs-lookup"><span data-stu-id="a511e-149">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="a511e-150">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="a511e-150">-VaultName</span></span>
<span data-ttu-id="a511e-151">Specifica il nome del Vault chiave da cui questo cmdlet ottiene le chiavi.</span><span class="sxs-lookup"><span data-stu-id="a511e-151">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="a511e-152">Questo cmdlet costruisce il nome di dominio completo (FQDN) di un Vault chiave in base al nome specificato da questo parametro e dall'ambiente selezionato.</span><span class="sxs-lookup"><span data-stu-id="a511e-152">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

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

### <span data-ttu-id="a511e-153">-Versione</span><span class="sxs-lookup"><span data-stu-id="a511e-153">-Version</span></span>
<span data-ttu-id="a511e-154">Specifica la versione chiave.</span><span class="sxs-lookup"><span data-stu-id="a511e-154">Specifies the key version.</span></span>
<span data-ttu-id="a511e-155">Questo cmdlet crea l'FQDN di una chiave in base al nome del Vault chiave, all'ambiente attualmente selezionato, al nome della chiave e alla versione chiave.</span><span class="sxs-lookup"><span data-stu-id="a511e-155">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

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

### <span data-ttu-id="a511e-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a511e-156">CommonParameters</span></span>
<span data-ttu-id="a511e-157">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a511e-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a511e-158">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a511e-158">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a511e-159">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a511e-159">INPUTS</span></span>

### <span data-ttu-id="a511e-160">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="a511e-160">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="a511e-161">System. String</span><span class="sxs-lookup"><span data-stu-id="a511e-161">System.String</span></span>

## <span data-ttu-id="a511e-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a511e-162">OUTPUTS</span></span>

### <span data-ttu-id="a511e-163">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="a511e-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="a511e-164">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a511e-164">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

### <span data-ttu-id="a511e-165">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="a511e-165">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="a511e-166">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a511e-166">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="a511e-167">Note</span><span class="sxs-lookup"><span data-stu-id="a511e-167">NOTES</span></span>

## <span data-ttu-id="a511e-168">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a511e-168">RELATED LINKS</span></span>

[<span data-ttu-id="a511e-169">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a511e-169">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="a511e-170">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a511e-170">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="a511e-171">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="a511e-171">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

[<span data-ttu-id="a511e-172">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="a511e-172">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)

