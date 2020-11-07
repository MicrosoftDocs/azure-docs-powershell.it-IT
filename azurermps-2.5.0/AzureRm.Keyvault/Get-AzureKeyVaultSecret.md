---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 8C9B33EE-10DE-4803-B76D-FE9FC2AC3372
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultsecret
schema: 2.0.0
ms.openlocfilehash: 522268cb215a393ef54209b7606c8556d2566fd7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866688"
---
# <span data-ttu-id="3b4d7-101">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="3b4d7-101">Get-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="3b4d7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3b4d7-102">SYNOPSIS</span></span>
<span data-ttu-id="3b4d7-103">Ottiene i segreti in un caveau chiave.</span><span class="sxs-lookup"><span data-stu-id="3b4d7-103">Gets the secrets in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b4d7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3b4d7-104">SYNTAX</span></span>

### <span data-ttu-id="3b4d7-105">ByVaultName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3b4d7-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b4d7-106">BySecretName</span><span class="sxs-lookup"><span data-stu-id="3b4d7-106">BySecretName</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b4d7-107">BySecretVersions</span><span class="sxs-lookup"><span data-stu-id="3b4d7-107">BySecretVersions</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b4d7-108">ByDeletedSecrets</span><span class="sxs-lookup"><span data-stu-id="3b4d7-108">ByDeletedSecrets</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b4d7-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3b4d7-109">DESCRIPTION</span></span>
<span data-ttu-id="3b4d7-110">Il cmdlet **Get-AzureKeyVaultSecret** ottiene segreti in un caveau chiave.</span><span class="sxs-lookup"><span data-stu-id="3b4d7-110">The **Get-AzureKeyVaultSecret** cmdlet gets secrets in a key vault.</span></span>
<span data-ttu-id="3b4d7-111">Questo cmdlet ottiene un segreto specifico o tutti i segreti in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="3b4d7-111">This cmdlet gets a specific secret or all the secrets in a key vault.</span></span>

## <span data-ttu-id="3b4d7-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3b4d7-112">EXAMPLES</span></span>

### <span data-ttu-id="3b4d7-113">Esempio 1: ottenere tutte le versioni correnti di tutti i segreti in un Vault chiave</span><span class="sxs-lookup"><span data-stu-id="3b4d7-113">Example 1: Get all current versions of all secrets in a key vault</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso'
```

<span data-ttu-id="3b4d7-114">Questo comando consente di ottenere le versioni correnti di tutti i segreti nel caveau della chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="3b4d7-114">This command gets the current versions of all secrets in the key vault named Contoso.</span></span>

### <span data-ttu-id="3b4d7-115">Esempio 2: ottenere tutte le versioni di un segreto specifico</span><span class="sxs-lookup"><span data-stu-id="3b4d7-115">Example 2: Get all versions of a specific secret</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -IncludeVersions
```

<span data-ttu-id="3b4d7-116">Questo comando consente di ottenere tutte le versioni del segreto denominato ITSecret nel caveau della chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="3b4d7-116">This command gets all versions of the secret named ITSecret in the key vault named Contoso.</span></span>

### <span data-ttu-id="3b4d7-117">Esempio 3: ottenere la versione corrente di un segreto specifico</span><span class="sxs-lookup"><span data-stu-id="3b4d7-117">Example 3: Get the current version of a specific secret</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
```

<span data-ttu-id="3b4d7-118">Questo comando consente di ottenere la versione corrente del segreto denominato ITSecret nel caveau della chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="3b4d7-118">This command gets the current version of the secret named ITSecret in the key vault named Contoso.</span></span>

### <span data-ttu-id="3b4d7-119">Esempio 4: ottenere una versione specifica di un segreto specifico</span><span class="sxs-lookup"><span data-stu-id="3b4d7-119">Example 4: Get a specific version of a specific secret</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -Version '6A12A286385949DB8B5F82AFEF85CAE9'
```

<span data-ttu-id="3b4d7-120">Questo comando consente di ottenere una versione specifica del segreto denominata ITSecret nel caveau della chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="3b4d7-120">This command gets a specific version of the secret named ITSecret in the key vault named Contoso.</span></span>

### <span data-ttu-id="3b4d7-121">Esempio 5: ottenere il valore di testo normale della versione corrente di un segreto specifico</span><span class="sxs-lookup"><span data-stu-id="3b4d7-121">Example 5: Get the plain text value of the current version of a specific secret</span></span>
```
PS C:\>$secret = Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
PS C:\> Write-Host "Secret Value is: " $secret.SecretValueText
```

<span data-ttu-id="3b4d7-122">Questi comandi ottengono la versione corrente di un segreto denominato ITSecret e quindi Visualizza il valore di testo normale di tale segreto.</span><span class="sxs-lookup"><span data-stu-id="3b4d7-122">These commands get the current version of a secret named ITSecret, and then displays the plain text value of that secret.</span></span>

### <span data-ttu-id="3b4d7-123">Esempio 6: ottenere tutti i segreti eliminati ma non eliminati per il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="3b4d7-123">Example 6: Get all the secrets that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="3b4d7-124">Questo comando ottiene tutti i segreti eliminati in precedenza, ma non eliminati, nel caveau della chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="3b4d7-124">This command gets all the secrets that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="3b4d7-125">Esempio 7: Ottiene il ITSecret segreto che è stato eliminato ma non eliminato per questo Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="3b4d7-125">Example 7: Gets the secret ITSecret that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -KeyName 'ITSecret' -InRemovedState
```

<span data-ttu-id="3b4d7-126">Questo comando ottiene il ITSecret segreto che è stato eliminato in precedenza, ma non è stato eliminato, nel caveau della chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="3b4d7-126">This command gets the secret ITSecret that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="3b4d7-127">Questo comando restituirà metadati come la data di eliminazione e la data di eliminazione pianificata di questo segreto eliminato.</span><span class="sxs-lookup"><span data-stu-id="3b4d7-127">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted secret.</span></span>

## <span data-ttu-id="3b4d7-128">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3b4d7-128">PARAMETERS</span></span>

### <span data-ttu-id="3b4d7-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b4d7-129">-DefaultProfile</span></span>
<span data-ttu-id="3b4d7-130">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3b4d7-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3b4d7-131">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="3b4d7-131">-IncludeVersions</span></span>
<span data-ttu-id="3b4d7-132">Indica che questo cmdlet ottiene tutte le versioni di un segreto.</span><span class="sxs-lookup"><span data-stu-id="3b4d7-132">Indicates that this cmdlet gets all versions of a secret.</span></span>
<span data-ttu-id="3b4d7-133">La versione corrente di un segreto è la prima nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="3b4d7-133">The current version of a secret is the first one on the list.</span></span>
<span data-ttu-id="3b4d7-134">Se specifichi questo parametro devi anche specificare i parametri *Name* e *VAULTNAME* .</span><span class="sxs-lookup"><span data-stu-id="3b4d7-134">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>

<span data-ttu-id="3b4d7-135">Se non specifichi il parametro *includeVersions* , questo cmdlet ottiene la versione corrente del segreto con il *nome* specificato.</span><span class="sxs-lookup"><span data-stu-id="3b4d7-135">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the secret with the specified *Name*.</span></span>

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

### <span data-ttu-id="3b4d7-136">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="3b4d7-136">-InRemovedState</span></span>
<span data-ttu-id="3b4d7-137">Specifica se visualizzare i segreti eliminati in precedenza nell'output</span><span class="sxs-lookup"><span data-stu-id="3b4d7-137">Specifies whether to show the previously deleted secrets in the output</span></span>

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

### <span data-ttu-id="3b4d7-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="3b4d7-138">-Name</span></span>
<span data-ttu-id="3b4d7-139">Specifica il nome del segreto da ottenere.</span><span class="sxs-lookup"><span data-stu-id="3b4d7-139">Specifies the name of the secret to get.</span></span>

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

### <span data-ttu-id="3b4d7-140">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="3b4d7-140">-VaultName</span></span>
<span data-ttu-id="3b4d7-141">Specifica il nome del Vault chiave a cui appartiene il segreto.</span><span class="sxs-lookup"><span data-stu-id="3b4d7-141">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="3b4d7-142">Questo cmdlet costruisce il nome di dominio completo (FQDN) di un Vault chiave in base al nome specificato da questo parametro e all'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="3b4d7-142">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="3b4d7-143">-Versione</span><span class="sxs-lookup"><span data-stu-id="3b4d7-143">-Version</span></span>
<span data-ttu-id="3b4d7-144">Specifica la versione segreta.</span><span class="sxs-lookup"><span data-stu-id="3b4d7-144">Specifies the secret version.</span></span>
<span data-ttu-id="3b4d7-145">Questo cmdlet crea l'FQDN di un segreto in base al nome del Vault chiave, all'ambiente selezionato, al nome segreto e alla versione segreta.</span><span class="sxs-lookup"><span data-stu-id="3b4d7-145">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

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

### <span data-ttu-id="3b4d7-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b4d7-146">CommonParameters</span></span>
<span data-ttu-id="3b4d7-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b4d7-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b4d7-148">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b4d7-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b4d7-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3b4d7-149">INPUTS</span></span>

### <span data-ttu-id="3b4d7-150">Stringa</span><span class="sxs-lookup"><span data-stu-id="3b4d7-150">String</span></span>

## <span data-ttu-id="3b4d7-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3b4d7-151">OUTPUTS</span></span>

### <span data-ttu-id="3b4d7-152">Elenco<Microsoft. Azure. Commands. Vault. Models. SecretIdentityItem>, Microsoft. Azure. Commands. Vault. Models. Secret, List<Microsoft. Azure. Commands. Vault. Models. DeletedSecretIdentityItem>, Microsoft. Azure. Commands. Vault. Models. DeletedSecret</span><span class="sxs-lookup"><span data-stu-id="3b4d7-152">List<Microsoft.Azure.Commands.KeyVault.Models.SecretIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.Secret, List<Microsoft.Azure.Commands.KeyVault.Models.DeletedSecretIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.DeletedSecret</span></span>

## <span data-ttu-id="3b4d7-153">Note</span><span class="sxs-lookup"><span data-stu-id="3b4d7-153">NOTES</span></span>

## <span data-ttu-id="3b4d7-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3b4d7-154">RELATED LINKS</span></span>

[<span data-ttu-id="3b4d7-155">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="3b4d7-155">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

[<span data-ttu-id="3b4d7-156">Undo-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="3b4d7-156">Undo-AzureKeyVaultSecretRemoval</span></span>](./Undo-AzureKeyVaultSecretRemoval.md)

[<span data-ttu-id="3b4d7-157">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="3b4d7-157">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

