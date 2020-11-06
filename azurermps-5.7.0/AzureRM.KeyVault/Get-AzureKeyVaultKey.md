---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultKey.md
ms.openlocfilehash: eaddfaa6be725d588c8856031a34e1bdefcc3892
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519453"
---
# <span data-ttu-id="5e1c0-101">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5e1c0-101">Get-AzureKeyVaultKey</span></span>

## <span data-ttu-id="5e1c0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5e1c0-102">SYNOPSIS</span></span>
<span data-ttu-id="5e1c0-103">Ottiene le chiavi di volta chiave.</span><span class="sxs-lookup"><span data-stu-id="5e1c0-103">Gets Key Vault keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e1c0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5e1c0-104">SYNTAX</span></span>

### <span data-ttu-id="5e1c0-105">ByVaultName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5e1c0-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e1c0-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="5e1c0-106">ByKeyName</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e1c0-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="5e1c0-107">ByKeyVersions</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e1c0-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="5e1c0-108">ByInputObjectVaultName</span></span>
```
Get-AzureKeyVaultKey [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e1c0-109">ByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="5e1c0-109">ByInputObjectKeyName</span></span>
```
Get-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e1c0-110">ByKInputObjecteyVersions</span><span class="sxs-lookup"><span data-stu-id="5e1c0-110">ByKInputObjecteyVersions</span></span>
```
Get-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e1c0-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5e1c0-111">DESCRIPTION</span></span>
<span data-ttu-id="5e1c0-112">Il cmdlet **Get-AzureKeyVaultKey** ottiene le chiavi di volta di Azure Key.</span><span class="sxs-lookup"><span data-stu-id="5e1c0-112">The **Get-AzureKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="5e1c0-113">Questo cmdlet consente di ottenere uno specifico **Microsoft. Azure. Commands. Key Vault. Models. bundle** o un elenco di tutti gli oggetti del **pacchetto** di chiavi in un Vault chiave o in base alla versione.</span><span class="sxs-lookup"><span data-stu-id="5e1c0-113">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="5e1c0-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5e1c0-114">EXAMPLES</span></span>

### <span data-ttu-id="5e1c0-115">Esempio 1: ottenere tutte le chiavi in un Vault chiave</span><span class="sxs-lookup"><span data-stu-id="5e1c0-115">Example 1: Get all the keys in a key vault</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso'
```

<span data-ttu-id="5e1c0-116">Questo comando consente di ottenere tutte le chiavi nel caveau della chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="5e1c0-116">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="5e1c0-117">Esempio 2: ottenere la versione corrente di una chiave</span><span class="sxs-lookup"><span data-stu-id="5e1c0-117">Example 2: Get the current version of a key</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx'
```

<span data-ttu-id="5e1c0-118">Questo comando ottiene la versione corrente della chiave denominata ITPfx nel caveau della chiave denominata Contoso.</span><span class="sxs-lookup"><span data-stu-id="5e1c0-118">This command gets the current version of the key named ITPfx in the key vault named Contoso.</span></span>

### <span data-ttu-id="5e1c0-119">Esempio 3: ottenere tutte le versioni di una chiave</span><span class="sxs-lookup"><span data-stu-id="5e1c0-119">Example 3: Get all versions of a key</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -IncludeVersions
```

<span data-ttu-id="5e1c0-120">Questo comando consente di ottenere tutte le versioni della chiave denominata ITPfx nella chiave vaultnamed contoso.</span><span class="sxs-lookup"><span data-stu-id="5e1c0-120">This command gets all versions the key named ITPfx in the key vaultnamed Contoso.</span></span>

### <span data-ttu-id="5e1c0-121">Esempio 4: ottenere una versione specifica di una chiave</span><span class="sxs-lookup"><span data-stu-id="5e1c0-121">Example 4: Get a specific version of a key</span></span>
```
PS C:\>$Key = Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -Version '5A12A276385949DB8B5F82AFEE85CAED'
```

<span data-ttu-id="5e1c0-122">Questo comando ottiene una versione specifica della chiave denominata ITPfx nel caveau della chiave denominata Contoso.</span><span class="sxs-lookup"><span data-stu-id="5e1c0-122">This command gets a specific version of the key named ITPfx in the key vault named Contoso.</span></span>
<span data-ttu-id="5e1c0-123">Dopo aver eseguito questo comando, è possibile esaminare varie proprietà della chiave spostando l'oggetto $Key.</span><span class="sxs-lookup"><span data-stu-id="5e1c0-123">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="5e1c0-124">Esempio 5: ottenere tutte le chiavi eliminate ma non eliminate per questo Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="5e1c0-124">Example 5: Get all the keys that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="5e1c0-125">Questo comando consente di ottenere tutte le chiavi eliminate in precedenza, ma non eliminate, nel caveau della chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="5e1c0-125">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="5e1c0-126">Esempio 6: ottiene la chiave ITPfx che è stata eliminata ma non eliminata per il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="5e1c0-126">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -InRemovedState
```

<span data-ttu-id="5e1c0-127">Questo comando ottiene la chiave ITPfx che è stata eliminata, ma non eliminata, nel caveau della chiave denominata Contoso.</span><span class="sxs-lookup"><span data-stu-id="5e1c0-127">This command gets the key ITPfx that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="5e1c0-128">Questo comando restituirà metadati, ad esempio la data di eliminazione, e la data di eliminazione pianificata di questa chiave eliminata.</span><span class="sxs-lookup"><span data-stu-id="5e1c0-128">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

## <span data-ttu-id="5e1c0-129">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5e1c0-129">PARAMETERS</span></span>

### <span data-ttu-id="5e1c0-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e1c0-130">-DefaultProfile</span></span>
<span data-ttu-id="5e1c0-131">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5e1c0-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e1c0-132">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="5e1c0-132">-IncludeVersions</span></span>
<span data-ttu-id="5e1c0-133">Indica che questo cmdlet ottiene tutte le versioni di una chiave.</span><span class="sxs-lookup"><span data-stu-id="5e1c0-133">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="5e1c0-134">La versione corrente di una chiave è la prima nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="5e1c0-134">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="5e1c0-135">Se specifichi questo parametro devi anche specificare i parametri *Name* e *VAULTNAME* .</span><span class="sxs-lookup"><span data-stu-id="5e1c0-135">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>

<span data-ttu-id="5e1c0-136">Se non specifichi il parametro *includeVersions* , questo cmdlet ottiene la versione corrente della chiave con il *nome* specificato.</span><span class="sxs-lookup"><span data-stu-id="5e1c0-136">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByKeyVersions, ByKInputObjecteyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e1c0-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e1c0-137">-InputObject</span></span>
<span data-ttu-id="5e1c0-138">Oggetto di Vault.</span><span class="sxs-lookup"><span data-stu-id="5e1c0-138">KeyVault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObjectVaultName, ByInputObjectKeyName, ByKInputObjecteyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e1c0-139">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="5e1c0-139">-InRemovedState</span></span>
<span data-ttu-id="5e1c0-140">Specifica se visualizzare le chiavi eliminate in precedenza nell'output</span><span class="sxs-lookup"><span data-stu-id="5e1c0-140">Specifies whether to show the previously deleted keys in the output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByVaultName, ByInputObjectVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e1c0-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="5e1c0-141">-Name</span></span>
<span data-ttu-id="5e1c0-142">Specifica il nome del bundle della chiave da ottenere.</span><span class="sxs-lookup"><span data-stu-id="5e1c0-142">Specifies the name of the key bundle to get.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName, ByInputObjectVaultName
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByKeyName, ByKeyVersions, ByInputObjectKeyName, ByKInputObjecteyVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e1c0-143">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="5e1c0-143">-VaultName</span></span>
<span data-ttu-id="5e1c0-144">Specifica il nome del Vault chiave da cui questo cmdlet ottiene le chiavi.</span><span class="sxs-lookup"><span data-stu-id="5e1c0-144">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="5e1c0-145">Questo cmdlet costruisce il nome di dominio completo (FQDN) di un Vault chiave in base al nome specificato da questo parametro e dall'ambiente selezionato.</span><span class="sxs-lookup"><span data-stu-id="5e1c0-145">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName, ByKeyName, ByKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e1c0-146">-Versione</span><span class="sxs-lookup"><span data-stu-id="5e1c0-146">-Version</span></span>
<span data-ttu-id="5e1c0-147">Specifica la versione chiave.</span><span class="sxs-lookup"><span data-stu-id="5e1c0-147">Specifies the key version.</span></span>
<span data-ttu-id="5e1c0-148">Questo cmdlet crea l'FQDN di una chiave in base al nome del Vault chiave, all'ambiente attualmente selezionato, al nome della chiave e alla versione chiave.</span><span class="sxs-lookup"><span data-stu-id="5e1c0-148">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: String
Parameter Sets: ByKeyName, ByInputObjectKeyName
Aliases: KeyVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e1c0-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e1c0-149">CommonParameters</span></span>
<span data-ttu-id="5e1c0-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e1c0-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e1c0-151">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e1c0-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e1c0-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5e1c0-152">INPUTS</span></span>

### <span data-ttu-id="5e1c0-153">Stringa</span><span class="sxs-lookup"><span data-stu-id="5e1c0-153">String</span></span>

## <span data-ttu-id="5e1c0-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5e1c0-154">OUTPUTS</span></span>

### <span data-ttu-id="5e1c0-155">Elenco<Microsoft. Azure. Commands. Vault. Models. PSKeyVaultKeyIdentityItem>, Microsoft. Azure. Commands. Vault. Models. PSKeyVaultKey, List<Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5e1c0-155">List<Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey, List<Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="5e1c0-156">Note</span><span class="sxs-lookup"><span data-stu-id="5e1c0-156">NOTES</span></span>

## <span data-ttu-id="5e1c0-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5e1c0-157">RELATED LINKS</span></span>

[<span data-ttu-id="5e1c0-158">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5e1c0-158">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="5e1c0-159">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5e1c0-159">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="5e1c0-160">Undo-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="5e1c0-160">Undo-AzureKeyVaultKeyRemoval</span></span>](./Undo-AzureKeyVaultKeyRemoval.md)

[<span data-ttu-id="5e1c0-161">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="5e1c0-161">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)

