---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 8C9B33EE-10DE-4803-B76D-FE9FC2AC3372
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
ms.openlocfilehash: b14e97ba09cba70a9ec571b2fbf1273de7157930
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863042"
---
# <span data-ttu-id="577d2-101">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="577d2-101">Get-AzKeyVaultSecret</span></span>

## <span data-ttu-id="577d2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="577d2-102">SYNOPSIS</span></span>
<span data-ttu-id="577d2-103">Ottiene i segreti in un caveau chiave.</span><span class="sxs-lookup"><span data-stu-id="577d2-103">Gets the secrets in a key vault.</span></span>

## <span data-ttu-id="577d2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="577d2-104">SYNTAX</span></span>

### <span data-ttu-id="577d2-105">ByVaultName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="577d2-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="577d2-106">BySecretName</span><span class="sxs-lookup"><span data-stu-id="577d2-106">BySecretName</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="577d2-107">BySecretVersions</span><span class="sxs-lookup"><span data-stu-id="577d2-107">BySecretVersions</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="577d2-108">ByDeletedSecrets</span><span class="sxs-lookup"><span data-stu-id="577d2-108">ByDeletedSecrets</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="577d2-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="577d2-109">DESCRIPTION</span></span>
<span data-ttu-id="577d2-110">Il cmdlet **Get-AzKeyVaultSecret** ottiene segreti in un caveau chiave.</span><span class="sxs-lookup"><span data-stu-id="577d2-110">The **Get-AzKeyVaultSecret** cmdlet gets secrets in a key vault.</span></span>
<span data-ttu-id="577d2-111">Questo cmdlet ottiene un segreto specifico o tutti i segreti in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="577d2-111">This cmdlet gets a specific secret or all the secrets in a key vault.</span></span>

## <span data-ttu-id="577d2-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="577d2-112">EXAMPLES</span></span>

### <span data-ttu-id="577d2-113">Esempio 1: ottenere tutte le versioni correnti di tutti i segreti in un Vault chiave</span><span class="sxs-lookup"><span data-stu-id="577d2-113">Example 1: Get all current versions of all secrets in a key vault</span></span>
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso'
```

<span data-ttu-id="577d2-114">Questo comando consente di ottenere le versioni correnti di tutti i segreti nel caveau della chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="577d2-114">This command gets the current versions of all secrets in the key vault named Contoso.</span></span>

### <span data-ttu-id="577d2-115">Esempio 2: ottenere tutte le versioni di un segreto specifico</span><span class="sxs-lookup"><span data-stu-id="577d2-115">Example 2: Get all versions of a specific secret</span></span>
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -IncludeVersions
```

<span data-ttu-id="577d2-116">Questo comando consente di ottenere tutte le versioni del segreto denominato ITSecret nel caveau della chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="577d2-116">This command gets all versions of the secret named ITSecret in the key vault named Contoso.</span></span>

### <span data-ttu-id="577d2-117">Esempio 3: ottenere la versione corrente di un segreto specifico</span><span class="sxs-lookup"><span data-stu-id="577d2-117">Example 3: Get the current version of a specific secret</span></span>
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
```

<span data-ttu-id="577d2-118">Questo comando consente di ottenere la versione corrente del segreto denominato ITSecret nel caveau della chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="577d2-118">This command gets the current version of the secret named ITSecret in the key vault named Contoso.</span></span>

### <span data-ttu-id="577d2-119">Esempio 4: ottenere una versione specifica di un segreto specifico</span><span class="sxs-lookup"><span data-stu-id="577d2-119">Example 4: Get a specific version of a specific secret</span></span>
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -Version '6A12A286385949DB8B5F82AFEF85CAE9'
```

<span data-ttu-id="577d2-120">Questo comando consente di ottenere una versione specifica del segreto denominata ITSecret nel caveau della chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="577d2-120">This command gets a specific version of the secret named ITSecret in the key vault named Contoso.</span></span>

### <span data-ttu-id="577d2-121">Esempio 5: ottenere il valore di testo normale della versione corrente di un segreto specifico</span><span class="sxs-lookup"><span data-stu-id="577d2-121">Example 5: Get the plain text value of the current version of a specific secret</span></span>
```
PS C:\>$secret = Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
PS C:\> Write-Host "Secret Value is: " $secret.SecretValueText
```

<span data-ttu-id="577d2-122">Questi comandi ottengono la versione corrente di un segreto denominato ITSecret e quindi Visualizza il valore di testo normale di tale segreto.</span><span class="sxs-lookup"><span data-stu-id="577d2-122">These commands get the current version of a secret named ITSecret, and then displays the plain text value of that secret.</span></span>

### <span data-ttu-id="577d2-123">Esempio 6: ottenere tutti i segreti eliminati ma non eliminati per il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="577d2-123">Example 6: Get all the secrets that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="577d2-124">Questo comando ottiene tutti i segreti eliminati in precedenza, ma non eliminati, nel caveau della chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="577d2-124">This command gets all the secrets that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="577d2-125">Esempio 7: Ottiene il ITSecret segreto che è stato eliminato ma non eliminato per questo Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="577d2-125">Example 7: Gets the secret ITSecret that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -KeyName 'ITSecret' -InRemovedState
```

<span data-ttu-id="577d2-126">Questo comando ottiene il ITSecret segreto che è stato eliminato in precedenza, ma non è stato eliminato, nel caveau della chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="577d2-126">This command gets the secret ITSecret that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="577d2-127">Questo comando restituirà metadati come la data di eliminazione e la data di eliminazione pianificata di questo segreto eliminato.</span><span class="sxs-lookup"><span data-stu-id="577d2-127">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted secret.</span></span>

## <span data-ttu-id="577d2-128">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="577d2-128">PARAMETERS</span></span>

### <span data-ttu-id="577d2-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="577d2-129">-DefaultProfile</span></span>
<span data-ttu-id="577d2-130">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="577d2-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="577d2-131">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="577d2-131">-IncludeVersions</span></span>
<span data-ttu-id="577d2-132">Indica che questo cmdlet ottiene tutte le versioni di un segreto.</span><span class="sxs-lookup"><span data-stu-id="577d2-132">Indicates that this cmdlet gets all versions of a secret.</span></span>
<span data-ttu-id="577d2-133">La versione corrente di un segreto è la prima nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="577d2-133">The current version of a secret is the first one on the list.</span></span>
<span data-ttu-id="577d2-134">Se specifichi questo parametro devi anche specificare i parametri *Name* e *VAULTNAME* .</span><span class="sxs-lookup"><span data-stu-id="577d2-134">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>

<span data-ttu-id="577d2-135">Se non specifichi il parametro *includeVersions* , questo cmdlet ottiene la versione corrente del segreto con il *nome* specificato.</span><span class="sxs-lookup"><span data-stu-id="577d2-135">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the secret with the specified *Name*.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: BySecretVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="577d2-136">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="577d2-136">-InRemovedState</span></span>
<span data-ttu-id="577d2-137">Specifica se visualizzare i segreti eliminati in precedenza nell'output</span><span class="sxs-lookup"><span data-stu-id="577d2-137">Specifies whether to show the previously deleted secrets in the output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedSecrets
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="577d2-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="577d2-138">-Name</span></span>
<span data-ttu-id="577d2-139">Specifica il nome del segreto da ottenere.</span><span class="sxs-lookup"><span data-stu-id="577d2-139">Specifies the name of the secret to get.</span></span>

```yaml
Type: String
Parameter Sets: BySecretName, BySecretVersions
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedSecrets
Aliases: SecretName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="577d2-140">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="577d2-140">-VaultName</span></span>
<span data-ttu-id="577d2-141">Specifica il nome del Vault chiave a cui appartiene il segreto.</span><span class="sxs-lookup"><span data-stu-id="577d2-141">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="577d2-142">Questo cmdlet costruisce il nome di dominio completo (FQDN) di un Vault chiave in base al nome specificato da questo parametro e all'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="577d2-142">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="577d2-143">-Versione</span><span class="sxs-lookup"><span data-stu-id="577d2-143">-Version</span></span>
<span data-ttu-id="577d2-144">Specifica la versione segreta.</span><span class="sxs-lookup"><span data-stu-id="577d2-144">Specifies the secret version.</span></span>
<span data-ttu-id="577d2-145">Questo cmdlet crea l'FQDN di un segreto in base al nome del Vault chiave, all'ambiente selezionato, al nome segreto e alla versione segreta.</span><span class="sxs-lookup"><span data-stu-id="577d2-145">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

```yaml
Type: String
Parameter Sets: BySecretName
Aliases: SecretVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="577d2-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="577d2-146">CommonParameters</span></span>
<span data-ttu-id="577d2-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="577d2-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="577d2-148">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="577d2-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="577d2-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="577d2-149">INPUTS</span></span>

### <span data-ttu-id="577d2-150">Stringa</span><span class="sxs-lookup"><span data-stu-id="577d2-150">String</span></span>

## <span data-ttu-id="577d2-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="577d2-151">OUTPUTS</span></span>

### <span data-ttu-id="577d2-152">Elenco<Microsoft. Azure. Commands. Vault. Models. SecretIdentityItem>, Microsoft. Azure. Commands. Vault. Models. Secret, List<Microsoft. Azure. Commands. Vault. Models. DeletedSecretIdentityItem>, Microsoft. Azure. Commands. Vault. Models. DeletedSecret</span><span class="sxs-lookup"><span data-stu-id="577d2-152">List<Microsoft.Azure.Commands.KeyVault.Models.SecretIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.Secret, List<Microsoft.Azure.Commands.KeyVault.Models.DeletedSecretIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.DeletedSecret</span></span>

## <span data-ttu-id="577d2-153">Note</span><span class="sxs-lookup"><span data-stu-id="577d2-153">NOTES</span></span>

## <span data-ttu-id="577d2-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="577d2-154">RELATED LINKS</span></span>

[<span data-ttu-id="577d2-155">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="577d2-155">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="577d2-156">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="577d2-156">Undo-AzKeyVaultSecretRemoval</span></span>](./Undo-AzKeyVaultSecretRemoval.md)

[<span data-ttu-id="577d2-157">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="577d2-157">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

