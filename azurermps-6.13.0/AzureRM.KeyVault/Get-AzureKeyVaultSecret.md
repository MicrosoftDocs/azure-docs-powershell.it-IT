---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 8C9B33EE-10DE-4803-B76D-FE9FC2AC3372
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultSecret.md
ms.openlocfilehash: aa8306070eb560deb465cbaa9ddae2bce24c5600
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520207"
---
# <span data-ttu-id="9bc3b-101">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="9bc3b-101">Get-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="9bc3b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9bc3b-102">SYNOPSIS</span></span>
<span data-ttu-id="9bc3b-103">Ottiene i segreti in un caveau chiave.</span><span class="sxs-lookup"><span data-stu-id="9bc3b-103">Gets the secrets in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9bc3b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9bc3b-104">SYNTAX</span></span>

### <span data-ttu-id="9bc3b-105">ByVaultName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9bc3b-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9bc3b-106">BySecretName</span><span class="sxs-lookup"><span data-stu-id="9bc3b-106">BySecretName</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9bc3b-107">BySecretVersions</span><span class="sxs-lookup"><span data-stu-id="9bc3b-107">BySecretVersions</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9bc3b-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="9bc3b-108">ByInputObjectVaultName</span></span>
```
Get-AzureKeyVaultSecret [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9bc3b-109">ByInputObjectSecretName</span><span class="sxs-lookup"><span data-stu-id="9bc3b-109">ByInputObjectSecretName</span></span>
```
Get-AzureKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9bc3b-110">ByInputObjectSecretVersions</span><span class="sxs-lookup"><span data-stu-id="9bc3b-110">ByInputObjectSecretVersions</span></span>
```
Get-AzureKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9bc3b-111">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="9bc3b-111">ByResourceIdVaultName</span></span>
```
Get-AzureKeyVaultSecret [-ResourceId] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9bc3b-112">ByResourceIdSecretName</span><span class="sxs-lookup"><span data-stu-id="9bc3b-112">ByResourceIdSecretName</span></span>
```
Get-AzureKeyVaultSecret [-ResourceId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9bc3b-113">ByResourceIdSecretVersions</span><span class="sxs-lookup"><span data-stu-id="9bc3b-113">ByResourceIdSecretVersions</span></span>
```
Get-AzureKeyVaultSecret [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9bc3b-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9bc3b-114">DESCRIPTION</span></span>
<span data-ttu-id="9bc3b-115">Il cmdlet **Get-AzureKeyVaultSecret** ottiene segreti in un caveau chiave.</span><span class="sxs-lookup"><span data-stu-id="9bc3b-115">The **Get-AzureKeyVaultSecret** cmdlet gets secrets in a key vault.</span></span>
<span data-ttu-id="9bc3b-116">Questo cmdlet ottiene un segreto specifico o tutti i segreti in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="9bc3b-116">This cmdlet gets a specific secret or all the secrets in a key vault.</span></span>

## <span data-ttu-id="9bc3b-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9bc3b-117">EXAMPLES</span></span>

### <span data-ttu-id="9bc3b-118">Esempio 1: ottenere tutte le versioni correnti di tutti i segreti in un Vault chiave</span><span class="sxs-lookup"><span data-stu-id="9bc3b-118">Example 1: Get all current versions of all secrets in a key vault</span></span>
```powershell
PS C:\> Get-AzureKeyVaultSecret -VaultName 'Contoso'

Vault Name   : contoso
Name         : secret1
Version      :
Id           : https://contoso.vault.azure.net:443/secrets/secret1
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :

Vault Name   : contoso
Name         : secret2
Version      :
Id           : https://contoso.vault.azure.net:443/secrets/secret2
Enabled      : True
Expires      :
Not Before   :
Created      : 4/11/2018 11:45:06 PM
Updated      : 4/11/2018 11:45:06 PM
Content Type :
Tags         :
```

<span data-ttu-id="9bc3b-119">Questo comando consente di ottenere le versioni correnti di tutti i segreti nel caveau della chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="9bc3b-119">This command gets the current versions of all secrets in the key vault named Contoso.</span></span>

### <span data-ttu-id="9bc3b-120">Esempio 2: ottenere tutte le versioni di un segreto specifico</span><span class="sxs-lookup"><span data-stu-id="9bc3b-120">Example 2: Get all versions of a specific secret</span></span>
```powershell
PS C:\> Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'secret1' -IncludeVersions

Vault Name   : contoso
Name         : secret1
Version      : 7128133570f84a71b48d7d0550deb74c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/7128133570f84a71b48d7d0550deb74c
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :

Vault Name   : contoso
Name         : secret1
Version      : 5d1a74ba2c454439886fb8509b6cab3c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/5d1a74ba2c454439886fb8509b6cab3c
Enabled      : True
Expires      :
Not Before   :
Created      : 4/5/2018 11:44:50 PM
Updated      : 4/5/2018 11:44:50 PM
Content Type :
Tags         :
```

<span data-ttu-id="9bc3b-121">Questo comando consente di ottenere tutte le versioni del segreto denominato secret1 nel caveau della chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="9bc3b-121">This command gets all versions of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="9bc3b-122">Esempio 3: ottenere la versione corrente di un segreto specifico</span><span class="sxs-lookup"><span data-stu-id="9bc3b-122">Example 3: Get the current version of a specific secret</span></span>
```powershell
PS C:\> Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'secret1'

Vault Name   : contoso
Name         : secret1
Version      : 7128133570f84a71b48d7d0550deb74c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/7128133570f84a71b48d7d0550deb74c
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :
```

<span data-ttu-id="9bc3b-123">Questo comando consente di ottenere la versione corrente del segreto denominato secret1 nel caveau della chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="9bc3b-123">This command gets the current version of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="9bc3b-124">Esempio 4: ottenere una versione specifica di un segreto specifico</span><span class="sxs-lookup"><span data-stu-id="9bc3b-124">Example 4: Get a specific version of a specific secret</span></span>
```powershell
PS C:\> Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'secret1' -Version '5d1a74ba2c454439886fb8509b6cab3c'

Vault Name   : contoso
Name         : secret1
Version      : 5d1a74ba2c454439886fb8509b6cab3c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/5d1a74ba2c454439886fb8509b6cab3c
Enabled      : True
Expires      :
Not Before   :
Created      : 4/5/2018 11:44:50 PM
Updated      : 4/5/2018 11:44:50 PM
Content Type :
Tags         :
```

<span data-ttu-id="9bc3b-125">Questo comando consente di ottenere una versione specifica del segreto denominata secret1 nel caveau della chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="9bc3b-125">This command gets a specific version of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="9bc3b-126">Esempio 5: ottenere il valore di testo normale della versione corrente di un segreto specifico</span><span class="sxs-lookup"><span data-stu-id="9bc3b-126">Example 5: Get the plain text value of the current version of a specific secret</span></span>
```powershell
PS C:\> $secret = Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
PS C:\> Write-Host "Secret Value is:" $secret.SecretValueText

Secret Value is: P@ssw0rd
```

<span data-ttu-id="9bc3b-127">Questi comandi ottengono la versione corrente di un segreto denominato ITSecret e quindi Visualizza il valore di testo normale di tale segreto.</span><span class="sxs-lookup"><span data-stu-id="9bc3b-127">These commands get the current version of a secret named ITSecret, and then displays the plain text value of that secret.</span></span>

### <span data-ttu-id="9bc3b-128">Esempio 6: ottenere tutti i segreti eliminati ma non eliminati per il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="9bc3b-128">Example 6: Get all the secrets that have been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzureKeyVaultSecret -VaultName 'Contoso' -InRemovedState

Vault Name           : contoso
Name                 : secret1
Id                   : https://contoso.vault.azure.net:443/secrets/secret1
Deleted Date         : 4/4/2018 8:51:58 PM
Scheduled Purge Date : 7/3/2018 8:51:58 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/4/2018 8:51:03 PM
Updated              : 4/4/2018 8:51:03 PM
Content Type         :
Tags                 :

Vault Name           : contoso
Name                 : secret2
Id                   : https://contoso.vault.azure.net:443/secrets/secret2
Deleted Date         : 5/7/2018 7:56:34 PM
Scheduled Purge Date : 8/5/2018 7:56:34 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/6/2018 8:39:15 PM
Updated              : 4/6/2018 10:11:24 PM
Content Type         : 
Tags                 :
```

<span data-ttu-id="9bc3b-129">Questo comando ottiene tutti i segreti eliminati in precedenza, ma non eliminati, nel caveau della chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="9bc3b-129">This command gets all the secrets that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="9bc3b-130">Esempio 7: Ottiene il ITSecret segreto che è stato eliminato ma non eliminato per questo Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="9bc3b-130">Example 7: Gets the secret ITSecret that has been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzureKeyVaultSecret -VaultName 'Contoso' -KeyName 'secret1' -InRemovedState

Vault Name           : contoso
Name                 : secret1
Version              : 689d23346e9c42a2a64f4e3d75094dcc
Id                   : https://contoso.vault.azure.net:443/secrets/secret1/689d23346e9c42a2a64f4e3d75094dcc
Deleted Date         : 4/4/2018 8:51:58 PM
Scheduled Purge Date : 7/3/2018 8:51:58 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/4/2018 8:51:03 PM
Updated              : 4/4/2018 8:51:03 PM
Content Type         :
Tags                 :
```

<span data-ttu-id="9bc3b-131">Questo comando ottiene il segreto "secret1" che è stato eliminato in precedenza, ma non è stato eliminato, nel caveau della chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="9bc3b-131">This command gets the secret 'secret1' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="9bc3b-132">Questo comando restituirà metadati come la data di eliminazione e la data di eliminazione pianificata di questo segreto eliminato.</span><span class="sxs-lookup"><span data-stu-id="9bc3b-132">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted secret.</span></span>

## <span data-ttu-id="9bc3b-133">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9bc3b-133">PARAMETERS</span></span>

### <span data-ttu-id="9bc3b-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bc3b-134">-DefaultProfile</span></span>
<span data-ttu-id="9bc3b-135">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9bc3b-135">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9bc3b-136">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="9bc3b-136">-IncludeVersions</span></span>
<span data-ttu-id="9bc3b-137">Indica che questo cmdlet ottiene tutte le versioni di un segreto.</span><span class="sxs-lookup"><span data-stu-id="9bc3b-137">Indicates that this cmdlet gets all versions of a secret.</span></span>
<span data-ttu-id="9bc3b-138">La versione corrente di un segreto è la prima nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="9bc3b-138">The current version of a secret is the first one on the list.</span></span>
<span data-ttu-id="9bc3b-139">Se specifichi questo parametro devi anche specificare i parametri *Name* e *VAULTNAME* .</span><span class="sxs-lookup"><span data-stu-id="9bc3b-139">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="9bc3b-140">Se non specifichi il parametro *includeVersions* , questo cmdlet ottiene la versione corrente del segreto con il *nome* specificato.</span><span class="sxs-lookup"><span data-stu-id="9bc3b-140">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the secret with the specified *Name*.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BySecretVersions, ByInputObjectSecretVersions, ByResourceIdSecretVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bc3b-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9bc3b-141">-InputObject</span></span>
<span data-ttu-id="9bc3b-142">Oggetto di Vault.</span><span class="sxs-lookup"><span data-stu-id="9bc3b-142">KeyVault Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObjectVaultName, ByInputObjectSecretName, ByInputObjectSecretVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9bc3b-143">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="9bc3b-143">-InRemovedState</span></span>
<span data-ttu-id="9bc3b-144">Specifica se visualizzare i segreti eliminati in precedenza nell'output</span><span class="sxs-lookup"><span data-stu-id="9bc3b-144">Specifies whether to show the previously deleted secrets in the output</span></span>

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

### <span data-ttu-id="9bc3b-145">-Nome</span><span class="sxs-lookup"><span data-stu-id="9bc3b-145">-Name</span></span>
<span data-ttu-id="9bc3b-146">Specifica il nome del segreto da ottenere.</span><span class="sxs-lookup"><span data-stu-id="9bc3b-146">Specifies the name of the secret to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, ByInputObjectVaultName, ByResourceIdVaultName
Aliases: SecretName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: BySecretName, BySecretVersions, ByInputObjectSecretName, ByInputObjectSecretVersions, ByResourceIdSecretName, ByResourceIdSecretVersions
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bc3b-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9bc3b-147">-ResourceId</span></span>
<span data-ttu-id="9bc3b-148">ID risorsa di un Vault.</span><span class="sxs-lookup"><span data-stu-id="9bc3b-148">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdVaultName, ByResourceIdSecretName, ByResourceIdSecretVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bc3b-149">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="9bc3b-149">-VaultName</span></span>
<span data-ttu-id="9bc3b-150">Specifica il nome del Vault chiave a cui appartiene il segreto.</span><span class="sxs-lookup"><span data-stu-id="9bc3b-150">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="9bc3b-151">Questo cmdlet costruisce il nome di dominio completo (FQDN) di un Vault chiave in base al nome specificato da questo parametro e all'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="9bc3b-151">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, BySecretName, BySecretVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bc3b-152">-Versione</span><span class="sxs-lookup"><span data-stu-id="9bc3b-152">-Version</span></span>
<span data-ttu-id="9bc3b-153">Specifica la versione segreta.</span><span class="sxs-lookup"><span data-stu-id="9bc3b-153">Specifies the secret version.</span></span>
<span data-ttu-id="9bc3b-154">Questo cmdlet crea l'FQDN di un segreto in base al nome del Vault chiave, all'ambiente selezionato, al nome segreto e alla versione segreta.</span><span class="sxs-lookup"><span data-stu-id="9bc3b-154">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

```yaml
Type: System.String
Parameter Sets: BySecretName, ByInputObjectSecretName, ByResourceIdSecretName
Aliases: SecretVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bc3b-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bc3b-155">CommonParameters</span></span>
<span data-ttu-id="9bc3b-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bc3b-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bc3b-157">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bc3b-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bc3b-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9bc3b-158">INPUTS</span></span>

### <span data-ttu-id="9bc3b-159">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="9bc3b-159">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="9bc3b-160">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9bc3b-160">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="9bc3b-161">System. String</span><span class="sxs-lookup"><span data-stu-id="9bc3b-161">System.String</span></span>

## <span data-ttu-id="9bc3b-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9bc3b-162">OUTPUTS</span></span>

### <span data-ttu-id="9bc3b-163">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="9bc3b-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

### <span data-ttu-id="9bc3b-164">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="9bc3b-164">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

### <span data-ttu-id="9bc3b-165">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="9bc3b-165">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>

### <span data-ttu-id="9bc3b-166">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="9bc3b-166">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span></span>

## <span data-ttu-id="9bc3b-167">Note</span><span class="sxs-lookup"><span data-stu-id="9bc3b-167">NOTES</span></span>

## <span data-ttu-id="9bc3b-168">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9bc3b-168">RELATED LINKS</span></span>

[<span data-ttu-id="9bc3b-169">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="9bc3b-169">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

[<span data-ttu-id="9bc3b-170">Undo-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="9bc3b-170">Undo-AzureKeyVaultSecretRemoval</span></span>](./Undo-AzureKeyVaultSecretRemoval.md)

[<span data-ttu-id="9bc3b-171">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="9bc3b-171">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

