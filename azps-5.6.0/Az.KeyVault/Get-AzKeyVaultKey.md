---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
ms.openlocfilehash: 81276c0896d6cb6685d3ce3ee71bb72cb39b690a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955822"
---
# <span data-ttu-id="be4bc-101">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="be4bc-101">Get-AzKeyVaultKey</span></span>

## <span data-ttu-id="be4bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be4bc-102">SYNOPSIS</span></span>
<span data-ttu-id="be4bc-103">Recupera le chiavi del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="be4bc-103">Gets Key Vault keys.</span></span>

## <span data-ttu-id="be4bc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="be4bc-104">SYNTAX</span></span>

### <span data-ttu-id="be4bc-105">ByVaultName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="be4bc-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be4bc-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="be4bc-106">ByKeyName</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be4bc-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="be4bc-107">ByKeyVersions</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be4bc-108">HsmByKeyName</span><span class="sxs-lookup"><span data-stu-id="be4bc-108">HsmByKeyName</span></span>
```
Get-AzKeyVaultKey -HsmName <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be4bc-109">HsmByVaultName</span><span class="sxs-lookup"><span data-stu-id="be4bc-109">HsmByVaultName</span></span>
```
Get-AzKeyVaultKey -HsmName <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be4bc-110">HsmByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="be4bc-110">HsmByKeyVersions</span></span>
```
Get-AzKeyVaultKey -HsmName <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be4bc-111">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="be4bc-111">ByInputObjectVaultName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be4bc-112">ByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="be4bc-112">ByInputObjectKeyName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be4bc-113">ByInputObjectKeyVersions</span><span class="sxs-lookup"><span data-stu-id="be4bc-113">ByInputObjectKeyVersions</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be4bc-114">HsmByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="be4bc-114">HsmByInputObjectVaultName</span></span>
```
Get-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be4bc-115">HsmByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="be4bc-115">HsmByInputObjectKeyName</span></span>
```
Get-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be4bc-116">HsmByInputObjectKeyVersions</span><span class="sxs-lookup"><span data-stu-id="be4bc-116">HsmByInputObjectKeyVersions</span></span>
```
Get-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be4bc-117">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="be4bc-117">ByResourceIdVaultName</span></span>
```
Get-AzKeyVaultKey -ResourceId <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be4bc-118">ByResourceIdKeyName</span><span class="sxs-lookup"><span data-stu-id="be4bc-118">ByResourceIdKeyName</span></span>
```
Get-AzKeyVaultKey -ResourceId <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be4bc-119">ByResourceIdKeyVersions</span><span class="sxs-lookup"><span data-stu-id="be4bc-119">ByResourceIdKeyVersions</span></span>
```
Get-AzKeyVaultKey -ResourceId <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be4bc-120">HsmByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="be4bc-120">HsmByResourceIdVaultName</span></span>
```
Get-AzKeyVaultKey -HsmResourceId <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be4bc-121">HsmByResourceIdKeyName</span><span class="sxs-lookup"><span data-stu-id="be4bc-121">HsmByResourceIdKeyName</span></span>
```
Get-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be4bc-122">HsmByResourceIdKeyVersions</span><span class="sxs-lookup"><span data-stu-id="be4bc-122">HsmByResourceIdKeyVersions</span></span>
```
Get-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be4bc-123">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="be4bc-123">DESCRIPTION</span></span>
<span data-ttu-id="be4bc-124">Il **cmdlet Get-AzKeyVaultKey** ottiene le chiavi del Vault della chiave di Azure.</span><span class="sxs-lookup"><span data-stu-id="be4bc-124">The **Get-AzKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="be4bc-125">Questo cmdlet ottiene uno specifico **oggetto Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** o un elenco di tutti gli oggetti **KeyBundle** in un vault delle chiavi o in base alla versione.</span><span class="sxs-lookup"><span data-stu-id="be4bc-125">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="be4bc-126">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="be4bc-126">EXAMPLES</span></span>

### <span data-ttu-id="be4bc-127">Esempio 1: Ottenere tutte le chiavi in un vault delle chiavi</span><span class="sxs-lookup"><span data-stu-id="be4bc-127">Example 1: Get all the keys in a key vault</span></span>
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

<span data-ttu-id="be4bc-128">Questo comando recupera tutte le chiavi nel vault delle chiavi denominato Contoso.</span><span class="sxs-lookup"><span data-stu-id="be4bc-128">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="be4bc-129">Esempio 2: Ottenere la versione corrente di un codice</span><span class="sxs-lookup"><span data-stu-id="be4bc-129">Example 2: Get the current version of a key</span></span>
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

<span data-ttu-id="be4bc-130">Questo comando ottiene la versione corrente della chiave denominata test1 nella chiave vault denominata Contoso.</span><span class="sxs-lookup"><span data-stu-id="be4bc-130">This command gets the current version of the key named test1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="be4bc-131">Esempio 3: Ottenere tutte le versioni di un codice</span><span class="sxs-lookup"><span data-stu-id="be4bc-131">Example 3: Get all versions of a key</span></span>
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

<span data-ttu-id="be4bc-132">Questo comando recupera tutte le versioni della chiave ITPfx nella chiave vault denominata Contoso.</span><span class="sxs-lookup"><span data-stu-id="be4bc-132">This command gets all versions the key named ITPfx in the key vault named Contoso.</span></span>

### <span data-ttu-id="be4bc-133">Esempio 4: Ottenere una versione specifica di un codice</span><span class="sxs-lookup"><span data-stu-id="be4bc-133">Example 4: Get a specific version of a key</span></span>
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

<span data-ttu-id="be4bc-134">Questo comando ottiene una versione specifica della chiave denominata test1 nella chiave vault denominata Contoso.</span><span class="sxs-lookup"><span data-stu-id="be4bc-134">This command gets a specific version of the key named test1 in the key vault named Contoso.</span></span>
<span data-ttu-id="be4bc-135">Dopo aver eseguito questo comando, è possibile esaminare le varie proprietà della chiave esplorando l$Key o object.</span><span class="sxs-lookup"><span data-stu-id="be4bc-135">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="be4bc-136">Esempio 5: Ottenere tutte le chiavi eliminate ma non eliminate per il vault delle chiavi</span><span class="sxs-lookup"><span data-stu-id="be4bc-136">Example 5: Get all the keys that have been deleted but not purged for this key vault</span></span>
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

<span data-ttu-id="be4bc-137">Questo comando recupera tutte le chiavi eliminate in precedenza, ma non eliminate, nella chiave vault denominata Contoso.</span><span class="sxs-lookup"><span data-stu-id="be4bc-137">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="be4bc-138">Esempio 6: ottiene la chiave ITPfx che è stata eliminata ma non eliminata per il vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="be4bc-138">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="be4bc-139">Questo comando ottiene il test della chiave3 eliminato in precedenza, ma non ripulito, nella chiave vault denominata Contoso.</span><span class="sxs-lookup"><span data-stu-id="be4bc-139">This command gets the key test3 that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="be4bc-140">Questo comando restituisce metadati come la data di eliminazione e la data di eliminazione pianificata della chiave eliminata.</span><span class="sxs-lookup"><span data-stu-id="be4bc-140">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

### <span data-ttu-id="be4bc-141">Esempio 7: Ottenere tutte le chiavi in un vault delle chiavi usando i filtri</span><span class="sxs-lookup"><span data-stu-id="be4bc-141">Example 7: Get all the keys in a key vault using filtering</span></span>
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

<span data-ttu-id="be4bc-142">Questo comando recupera tutte le chiavi nel vault delle chiavi denominate Contoso che iniziano con "test".</span><span class="sxs-lookup"><span data-stu-id="be4bc-142">This command gets all the keys in the key vault named Contoso that start with "test".</span></span>

### <span data-ttu-id="be4bc-143">Esempio 8: Scaricare una chiave pubblica come file PEM</span><span class="sxs-lookup"><span data-stu-id="be4bc-143">Example 8: Download a public key as a .pem file</span></span>

```powershell
PS C:\> $path = "D:\public.pem"
PS C:\> Get-AzKeyVaultKey -VaultName $vaultName -KeyName $keyName -OutFile $path
```

<span data-ttu-id="be4bc-144">È possibile scaricare la chiave pubblica di una chiave RSA specificando il `-OutFile` parametro.</span><span class="sxs-lookup"><span data-stu-id="be4bc-144">You can download the public key of a RSA key by specifying the `-OutFile` parameter.</span></span>
<span data-ttu-id="be4bc-145">Questo è un passaggio per l'importazione delle chiavi protette da HSM nel Vault delle chiavi di Azure.</span><span class="sxs-lookup"><span data-stu-id="be4bc-145">This is one step of importing HSM-protected keys to Azure Key Vault.</span></span> <span data-ttu-id="be4bc-146">Vedi https://docs.microsoft.com/azure/key-vault/keys/hsm-protected-keys</span><span class="sxs-lookup"><span data-stu-id="be4bc-146">See https://docs.microsoft.com/azure/key-vault/keys/hsm-protected-keys</span></span>

## <span data-ttu-id="be4bc-147">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be4bc-147">PARAMETERS</span></span>

### <span data-ttu-id="be4bc-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be4bc-148">-DefaultProfile</span></span>
<span data-ttu-id="be4bc-149">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="be4bc-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be4bc-150">-HsmName</span><span class="sxs-lookup"><span data-stu-id="be4bc-150">-HsmName</span></span>
<span data-ttu-id="be4bc-151">Nome HSM.</span><span class="sxs-lookup"><span data-stu-id="be4bc-151">HSM name.</span></span> <span data-ttu-id="be4bc-152">Il cmdlet crea l'FQDN di un servizio HSM gestito in base al nome e all'ambiente attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="be4bc-152">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByKeyName, HsmByVaultName, HsmByKeyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be4bc-153">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="be4bc-153">-HsmObject</span></span>
<span data-ttu-id="be4bc-154">Oggetto HSM.</span><span class="sxs-lookup"><span data-stu-id="be4bc-154">HSM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: HsmByInputObjectVaultName, HsmByInputObjectKeyName, HsmByInputObjectKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be4bc-155">-HsmResourceId</span><span class="sxs-lookup"><span data-stu-id="be4bc-155">-HsmResourceId</span></span>
<span data-ttu-id="be4bc-156">ID risorsa HSM.</span><span class="sxs-lookup"><span data-stu-id="be4bc-156">HSM Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByResourceIdVaultName, HsmByResourceIdKeyName, HsmByResourceIdKeyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be4bc-157">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="be4bc-157">-IncludeVersions</span></span>
<span data-ttu-id="be4bc-158">Indica che questo cmdlet ottiene tutte le versioni di una chiave.</span><span class="sxs-lookup"><span data-stu-id="be4bc-158">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="be4bc-159">La versione corrente di un codice è la prima nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="be4bc-159">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="be4bc-160">Se si specifica questo parametro, è necessario specificare anche i *parametri Name* e *VaultName.*</span><span class="sxs-lookup"><span data-stu-id="be4bc-160">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="be4bc-161">Se non si specifica il *parametro IncludeVersions,* questo cmdlet ottiene la versione corrente della chiave con il nome *specificato.*</span><span class="sxs-lookup"><span data-stu-id="be4bc-161">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByKeyVersions, HsmByKeyVersions, ByInputObjectKeyVersions, HsmByInputObjectKeyVersions, ByResourceIdKeyVersions, HsmByResourceIdKeyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be4bc-162">-InputObject</span><span class="sxs-lookup"><span data-stu-id="be4bc-162">-InputObject</span></span>
<span data-ttu-id="be4bc-163">Oggetto KeyVault.</span><span class="sxs-lookup"><span data-stu-id="be4bc-163">KeyVault object.</span></span>

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

### <span data-ttu-id="be4bc-164">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="be4bc-164">-InRemovedState</span></span>
<span data-ttu-id="be4bc-165">Specifica se visualizzare le chiavi eliminate in precedenza nell'output</span><span class="sxs-lookup"><span data-stu-id="be4bc-165">Specifies whether to show the previously deleted keys in the output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByVaultName, HsmByVaultName, ByInputObjectVaultName, HsmByInputObjectVaultName, ByResourceIdVaultName, HsmByResourceIdVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be4bc-166">-Name</span><span class="sxs-lookup"><span data-stu-id="be4bc-166">-Name</span></span>
<span data-ttu-id="be4bc-167">Specifica il nome del bundle di chiavi da ottenere.</span><span class="sxs-lookup"><span data-stu-id="be4bc-167">Specifies the name of the key bundle to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, HsmByVaultName, ByInputObjectVaultName, HsmByInputObjectVaultName, ByResourceIdVaultName, HsmByResourceIdVaultName
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ByKeyName, ByKeyVersions, HsmByKeyName, HsmByKeyVersions, ByInputObjectKeyName, ByInputObjectKeyVersions, HsmByInputObjectKeyName, HsmByInputObjectKeyVersions, ByResourceIdKeyName, ByResourceIdKeyVersions, HsmByResourceIdKeyName, HsmByResourceIdKeyVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="be4bc-168">-OutFile</span><span class="sxs-lookup"><span data-stu-id="be4bc-168">-OutFile</span></span>
<span data-ttu-id="be4bc-169">Specifica il file di output per cui questo cmdlet salva la chiave.</span><span class="sxs-lookup"><span data-stu-id="be4bc-169">Specifies the output file for which this cmdlet saves the key.</span></span> <span data-ttu-id="be4bc-170">Per impostazione predefinita, la chiave pubblica viene salvata in formato PEM.</span><span class="sxs-lookup"><span data-stu-id="be4bc-170">The public key is saved in PEM format by default.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be4bc-171">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="be4bc-171">-ResourceId</span></span>
<span data-ttu-id="be4bc-172">ID risorsa KeyVault.</span><span class="sxs-lookup"><span data-stu-id="be4bc-172">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdVaultName, ByResourceIdKeyName, ByResourceIdKeyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be4bc-173">-VaultName</span><span class="sxs-lookup"><span data-stu-id="be4bc-173">-VaultName</span></span>
<span data-ttu-id="be4bc-174">Specifica il nome del vault delle chiavi da cui il cmdlet recupera le chiavi.</span><span class="sxs-lookup"><span data-stu-id="be4bc-174">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="be4bc-175">Questo cmdlet crea il nome di dominio completo (FQDN) di un vault delle chiavi in base al nome specificato da questo parametro e all'ambiente selezionato.</span><span class="sxs-lookup"><span data-stu-id="be4bc-175">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

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

### <span data-ttu-id="be4bc-176">-Version</span><span class="sxs-lookup"><span data-stu-id="be4bc-176">-Version</span></span>
<span data-ttu-id="be4bc-177">Specifica la versione chiave.</span><span class="sxs-lookup"><span data-stu-id="be4bc-177">Specifies the key version.</span></span>
<span data-ttu-id="be4bc-178">Questo cmdlet crea l'FQDN di una chiave in base al nome del vault della chiave, all'ambiente attualmente selezionato, al nome della chiave e alla versione della chiave.</span><span class="sxs-lookup"><span data-stu-id="be4bc-178">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName, HsmByKeyName, ByInputObjectKeyName, HsmByInputObjectKeyName, ByResourceIdKeyName, HsmByResourceIdKeyName
Aliases: KeyVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be4bc-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be4bc-179">CommonParameters</span></span>
<span data-ttu-id="be4bc-180">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be4bc-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be4bc-181">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="be4bc-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be4bc-182">INPUT</span><span class="sxs-lookup"><span data-stu-id="be4bc-182">INPUTS</span></span>

### <span data-ttu-id="be4bc-183">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="be4bc-183">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="be4bc-184">System.String</span><span class="sxs-lookup"><span data-stu-id="be4bc-184">System.String</span></span>

## <span data-ttu-id="be4bc-185">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="be4bc-185">OUTPUTS</span></span>

### <span data-ttu-id="be4bc-186">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="be4bc-186">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="be4bc-187">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="be4bc-187">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

### <span data-ttu-id="be4bc-188">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="be4bc-188">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="be4bc-189">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="be4bc-189">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="be4bc-190">NOTE</span><span class="sxs-lookup"><span data-stu-id="be4bc-190">NOTES</span></span>

## <span data-ttu-id="be4bc-191">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="be4bc-191">RELATED LINKS</span></span>

[<span data-ttu-id="be4bc-192">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="be4bc-192">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="be4bc-193">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="be4bc-193">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="be4bc-194">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="be4bc-194">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

[<span data-ttu-id="be4bc-195">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="be4bc-195">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)

