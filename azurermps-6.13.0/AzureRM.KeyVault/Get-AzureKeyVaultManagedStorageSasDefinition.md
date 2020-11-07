---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: e37236e4e5fbced90a6dbd5f33d22d02947b20d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687307"
---
# <span data-ttu-id="ad3a6-101">Get-AzureKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="ad3a6-101">Get-AzureKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="ad3a6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ad3a6-102">SYNOPSIS</span></span>
<span data-ttu-id="ad3a6-103">Ottiene le definizioni SAS di archiviazione Managed Key Vault.</span><span class="sxs-lookup"><span data-stu-id="ad3a6-103">Gets Key Vault managed Storage SAS Definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad3a6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ad3a6-104">SYNTAX</span></span>

### <span data-ttu-id="ad3a6-105">ByDefinitionName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ad3a6-105">ByDefinitionName (Default)</span></span>
```
Get-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [[-Name] <String>]
 [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad3a6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ad3a6-106">ByInputObject</span></span>
```
Get-AzureKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-Name] <String>] [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad3a6-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad3a6-107">DESCRIPTION</span></span>
<span data-ttu-id="ad3a6-108">Ottiene una definizione della chiave di archiviazione gestita di SAS se il nome della definizione è specificato.</span><span class="sxs-lookup"><span data-stu-id="ad3a6-108">Gets a Key Vault managed Storage SAS Definition if the name of the definition is specified.</span></span> <span data-ttu-id="ad3a6-109">Se il nome della definizione non viene specificato, verranno elencate tutte le definizioni SAS associate all'account di archiviazione gestita Key Vault specificato nel Vault.</span><span class="sxs-lookup"><span data-stu-id="ad3a6-109">If the definition name is not specified, then all the SAS definitions associated with the specified Key Vault managed Storage Account in the vault are listed.</span></span>

## <span data-ttu-id="ad3a6-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ad3a6-110">EXAMPLES</span></span>

### <span data-ttu-id="ad3a6-111">Esempio 1: elencare tutte le definizioni di archiviazione SAS Key Vault Managed</span><span class="sxs-lookup"><span data-stu-id="ad3a6-111">Example 1: List all Key Vault managed Storage SAS Definitions</span></span>
```powershell
PS C:\> Get-AzureKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount'

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/accountsas
Vault Name  : myvault
AccountName : mystorageaccount
Name        : accountsas
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="ad3a6-112">Elenca tutte le definizioni SAS associate all'account di archiviazione gestita Key Vault ' mystorageaccount ' gestito dal Vault ' Vault '</span><span class="sxs-lookup"><span data-stu-id="ad3a6-112">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'</span></span>

### <span data-ttu-id="ad3a6-113">Esempio 2: ottenere un account di archiviazione gestito Key Vault</span><span class="sxs-lookup"><span data-stu-id="ad3a6-113">Example 2: Get a Key Vault managed Storage Account</span></span>
```powershell
PS C:\> Get-AzureKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'accountsas'

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/accountsas
Secret Id   : https://myvault.vault.azure.net/secrets/mystorageaccount-accountsas
Vault Name  : myvault
AccountName : mystorageaccount
Name        : accountsas
Parameter   :
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="ad3a6-114">Ottiene i dettagli della definizione SAS "Accounts" associata all'account di archiviazione gestita Key Vault "mystorageaccount" gestito dalla volta "Vault".</span><span class="sxs-lookup"><span data-stu-id="ad3a6-114">Gets the details of SAS Definition 'accountsas' associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'.</span></span>

## <span data-ttu-id="ad3a6-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ad3a6-115">PARAMETERS</span></span>

### <span data-ttu-id="ad3a6-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ad3a6-116">-AccountName</span></span>
<span data-ttu-id="ad3a6-117">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="ad3a6-117">Vault name.</span></span>
<span data-ttu-id="ad3a6-118">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="ad3a6-118">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad3a6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad3a6-119">-DefaultProfile</span></span>
<span data-ttu-id="ad3a6-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ad3a6-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ad3a6-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad3a6-121">-InputObject</span></span>
<span data-ttu-id="ad3a6-122">Oggetto ManagedStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="ad3a6-122">ManagedStorageAccount object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad3a6-123">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="ad3a6-123">-InRemovedState</span></span>
<span data-ttu-id="ad3a6-124">Specifica se visualizzare le definizioni SAS di archiviazione eliminate in precedenza nell'output.</span><span class="sxs-lookup"><span data-stu-id="ad3a6-124">Specifies whether to show the previously deleted storage sas definitions in the output.</span></span>

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

### <span data-ttu-id="ad3a6-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="ad3a6-125">-Name</span></span>
<span data-ttu-id="ad3a6-126">Nome della definizione di archiviazione SAS.</span><span class="sxs-lookup"><span data-stu-id="ad3a6-126">Storage sas definition name.</span></span>
<span data-ttu-id="ad3a6-127">Cmdlet costruisce il nome di dominio completo di una definizione SAS di archiviazione dal nome della volta, dall'ambiente attualmente selezionato, dal nome dell'account di archiviazione e dalla definizione SAS.</span><span class="sxs-lookup"><span data-stu-id="ad3a6-127">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad3a6-128">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="ad3a6-128">-VaultName</span></span>
<span data-ttu-id="ad3a6-129">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="ad3a6-129">Vault name.</span></span>
<span data-ttu-id="ad3a6-130">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="ad3a6-130">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad3a6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad3a6-131">CommonParameters</span></span>
<span data-ttu-id="ad3a6-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad3a6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad3a6-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad3a6-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad3a6-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ad3a6-134">INPUTS</span></span>

### <span data-ttu-id="ad3a6-135">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="ad3a6-135">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>
<span data-ttu-id="ad3a6-136">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ad3a6-136">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="ad3a6-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ad3a6-137">OUTPUTS</span></span>

### <span data-ttu-id="ad3a6-138">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="ad3a6-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

### <span data-ttu-id="ad3a6-139">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="ad3a6-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

### <span data-ttu-id="ad3a6-140">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="ad3a6-140">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span></span>

### <span data-ttu-id="ad3a6-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="ad3a6-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="ad3a6-142">Note</span><span class="sxs-lookup"><span data-stu-id="ad3a6-142">NOTES</span></span>

## <span data-ttu-id="ad3a6-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ad3a6-143">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

