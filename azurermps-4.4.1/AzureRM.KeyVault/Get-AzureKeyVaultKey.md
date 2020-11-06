---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://go.microsoft.com/fwlink/?LinkId=690297
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultKey.md
ms.openlocfilehash: 48d050623ea75bed1aee1b78a26bf81bf3305e06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510599"
---
# <span data-ttu-id="76bdc-101">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="76bdc-101">Get-AzureKeyVaultKey</span></span>

## <span data-ttu-id="76bdc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="76bdc-102">SYNOPSIS</span></span>
<span data-ttu-id="76bdc-103">Ottiene le chiavi di volta chiave.</span><span class="sxs-lookup"><span data-stu-id="76bdc-103">Gets Key Vault keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76bdc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="76bdc-104">SYNTAX</span></span>

### <span data-ttu-id="76bdc-105">ByVaultName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="76bdc-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76bdc-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="76bdc-106">ByKeyName</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76bdc-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="76bdc-107">ByKeyVersions</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76bdc-108">ByDeletedKey</span><span class="sxs-lookup"><span data-stu-id="76bdc-108">ByDeletedKey</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76bdc-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="76bdc-109">DESCRIPTION</span></span>
<span data-ttu-id="76bdc-110">Il cmdlet **Get-AzureKeyVaultKey** ottiene le chiavi di volta di Azure Key.</span><span class="sxs-lookup"><span data-stu-id="76bdc-110">The **Get-AzureKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="76bdc-111">Questo cmdlet consente di ottenere uno specifico **Microsoft. Azure. Commands. Key Vault. Models. bundle** o un elenco di tutti gli oggetti del **pacchetto** di chiavi in un Vault chiave o in base alla versione.</span><span class="sxs-lookup"><span data-stu-id="76bdc-111">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="76bdc-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="76bdc-112">EXAMPLES</span></span>

### <span data-ttu-id="76bdc-113">Esempio 1: ottenere tutte le chiavi in un Vault chiave</span><span class="sxs-lookup"><span data-stu-id="76bdc-113">Example 1: Get all the keys in a key vault</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso'
```

<span data-ttu-id="76bdc-114">Questo comando consente di ottenere tutte le chiavi nel caveau della chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="76bdc-114">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="76bdc-115">Esempio 2: ottenere la versione corrente di una chiave</span><span class="sxs-lookup"><span data-stu-id="76bdc-115">Example 2: Get the current version of a key</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx'
```

<span data-ttu-id="76bdc-116">Questo comando ottiene la versione corrente della chiave denominata ITPfx nel caveau della chiave denominata Contoso.</span><span class="sxs-lookup"><span data-stu-id="76bdc-116">This command gets the current version of the key named ITPfx in the key vault named Contoso.</span></span>

### <span data-ttu-id="76bdc-117">Esempio 3: ottenere tutte le versioni di una chiave</span><span class="sxs-lookup"><span data-stu-id="76bdc-117">Example 3: Get all versions of a key</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -IncludeVersions
```

<span data-ttu-id="76bdc-118">Questo comando consente di ottenere tutte le versioni della chiave denominata ITPfx nella chiave vaultnamed contoso.</span><span class="sxs-lookup"><span data-stu-id="76bdc-118">This command gets all versions the key named ITPfx in the key vaultnamed Contoso.</span></span>

### <span data-ttu-id="76bdc-119">Esempio 4: ottenere una versione specifica di una chiave</span><span class="sxs-lookup"><span data-stu-id="76bdc-119">Example 4: Get a specific version of a key</span></span>
```
PS C:\>$Key = Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -Version '5A12A276385949DB8B5F82AFEE85CAED'
```

<span data-ttu-id="76bdc-120">Questo comando ottiene una versione specifica della chiave denominata ITPfx nel caveau della chiave denominata Contoso.</span><span class="sxs-lookup"><span data-stu-id="76bdc-120">This command gets a specific version of the key named ITPfx in the key vault named Contoso.</span></span>
<span data-ttu-id="76bdc-121">Dopo aver eseguito questo comando, è possibile esaminare varie proprietà della chiave spostando l'oggetto $Key.</span><span class="sxs-lookup"><span data-stu-id="76bdc-121">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="76bdc-122">Esempio 5: ottenere tutte le chiavi eliminate ma non eliminate per questo Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="76bdc-122">Example 5: Get all the keys that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="76bdc-123">Questo comando consente di ottenere tutte le chiavi eliminate in precedenza, ma non eliminate, nel caveau della chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="76bdc-123">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="76bdc-124">Esempio 6: ottiene la chiave ITPfx che è stata eliminata ma non eliminata per il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="76bdc-124">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -InRemovedState
```

<span data-ttu-id="76bdc-125">Questo comando ottiene la chiave ITPfx che è stata eliminata, ma non eliminata, nel caveau della chiave denominata Contoso.</span><span class="sxs-lookup"><span data-stu-id="76bdc-125">This command gets the key ITPfx that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="76bdc-126">Questo comando restituirà metadati, ad esempio la data di eliminazione, e la data di eliminazione pianificata di questa chiave eliminata.</span><span class="sxs-lookup"><span data-stu-id="76bdc-126">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

## <span data-ttu-id="76bdc-127">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="76bdc-127">PARAMETERS</span></span>

### <span data-ttu-id="76bdc-128">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="76bdc-128">-IncludeVersions</span></span>
<span data-ttu-id="76bdc-129">Indica che questo cmdlet ottiene tutte le versioni di una chiave.</span><span class="sxs-lookup"><span data-stu-id="76bdc-129">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="76bdc-130">La versione corrente di una chiave è la prima nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="76bdc-130">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="76bdc-131">Se specifichi questo parametro devi anche specificare i parametri *Name* e *VAULTNAME* .</span><span class="sxs-lookup"><span data-stu-id="76bdc-131">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>

<span data-ttu-id="76bdc-132">Se non specifichi il parametro *includeVersions* , questo cmdlet ottiene la versione corrente della chiave con il *nome* specificato.</span><span class="sxs-lookup"><span data-stu-id="76bdc-132">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByKeyVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76bdc-133">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="76bdc-133">-InRemovedState</span></span>
<span data-ttu-id="76bdc-134">Specifica se visualizzare le chiavi eliminate in precedenza nell'output.</span><span class="sxs-lookup"><span data-stu-id="76bdc-134">Specifies whether to show the previously deleted keys in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedKey
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76bdc-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="76bdc-135">-Name</span></span>
<span data-ttu-id="76bdc-136">Specifica il nome del bundle della chiave da ottenere.</span><span class="sxs-lookup"><span data-stu-id="76bdc-136">Specifies the name of the key bundle to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName, ByKeyVersions
Aliases: KeyName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedKey
Aliases: KeyName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76bdc-137">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="76bdc-137">-VaultName</span></span>
<span data-ttu-id="76bdc-138">Specifica il nome del Vault chiave da cui questo cmdlet ottiene le chiavi.</span><span class="sxs-lookup"><span data-stu-id="76bdc-138">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="76bdc-139">Questo cmdlet costruisce il nome di dominio completo (FQDN) di un Vault chiave in base al nome specificato da questo parametro e dall'ambiente selezionato.</span><span class="sxs-lookup"><span data-stu-id="76bdc-139">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76bdc-140">-Versione</span><span class="sxs-lookup"><span data-stu-id="76bdc-140">-Version</span></span>
<span data-ttu-id="76bdc-141">Specifica la versione chiave.</span><span class="sxs-lookup"><span data-stu-id="76bdc-141">Specifies the key version.</span></span>
<span data-ttu-id="76bdc-142">Questo cmdlet crea l'FQDN di una chiave in base al nome del Vault chiave, all'ambiente attualmente selezionato, al nome della chiave e alla versione chiave.</span><span class="sxs-lookup"><span data-stu-id="76bdc-142">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases: KeyVersion

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76bdc-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76bdc-143">-DefaultProfile</span></span>
<span data-ttu-id="76bdc-144">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="76bdc-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76bdc-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76bdc-145">CommonParameters</span></span>
<span data-ttu-id="76bdc-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76bdc-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76bdc-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76bdc-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76bdc-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="76bdc-148">INPUTS</span></span>

### <span data-ttu-id="76bdc-149">Stringa</span><span class="sxs-lookup"><span data-stu-id="76bdc-149">String</span></span>

## <span data-ttu-id="76bdc-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="76bdc-150">OUTPUTS</span></span>

### <span data-ttu-id="76bdc-151">Elenco<Microsoft. Azure. Commands. Vault. Models. KeyIdentityItem>, Microsoft. Azure. Commands. DataVault. Models. bundle, List<Microsoft. Azure. Commands. Vault. Models. DeletedKeyIdentityItem>, Microsoft. Azure. Commands. Vault. Models. DeletedKeyBundle</span><span class="sxs-lookup"><span data-stu-id="76bdc-151">List<Microsoft.Azure.Commands.KeyVault.Models.KeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.KeyBundle, List<Microsoft.Azure.Commands.KeyVault.Models.DeletedKeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.DeletedKeyBundle</span></span>

## <span data-ttu-id="76bdc-152">Note</span><span class="sxs-lookup"><span data-stu-id="76bdc-152">NOTES</span></span>

## <span data-ttu-id="76bdc-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="76bdc-153">RELATED LINKS</span></span>

[<span data-ttu-id="76bdc-154">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="76bdc-154">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="76bdc-155">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="76bdc-155">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="76bdc-156">Undo-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="76bdc-156">Undo-AzureKeyVaultKeyRemoval</span></span>](./Undo-AzureKeyVaultKeyRemoval.md)

[<span data-ttu-id="76bdc-157">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="76bdc-157">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)

