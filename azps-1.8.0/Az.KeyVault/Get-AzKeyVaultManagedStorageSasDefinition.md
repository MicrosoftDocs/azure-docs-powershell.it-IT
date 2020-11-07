---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: ff384b456d6cbaac3fa0c28f01038a60b211dfca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835736"
---
# <span data-ttu-id="a52c0-101">Get-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="a52c0-101">Get-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="a52c0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a52c0-102">SYNOPSIS</span></span>
<span data-ttu-id="a52c0-103">Ottiene le definizioni SAS di archiviazione Managed Key Vault.</span><span class="sxs-lookup"><span data-stu-id="a52c0-103">Gets Key Vault managed Storage SAS Definitions.</span></span>

## <span data-ttu-id="a52c0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a52c0-104">SYNTAX</span></span>

### <span data-ttu-id="a52c0-105">ByDefinitionName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a52c0-105">ByDefinitionName (Default)</span></span>
```
Get-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [[-Name] <String>]
 [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a52c0-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a52c0-106">ByInputObject</span></span>
```
Get-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-Name] <String>] [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a52c0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a52c0-107">DESCRIPTION</span></span>
<span data-ttu-id="a52c0-108">Ottiene una definizione della chiave di archiviazione gestita di SAS se il nome della definizione è specificato.</span><span class="sxs-lookup"><span data-stu-id="a52c0-108">Gets a Key Vault managed Storage SAS Definition if the name of the definition is specified.</span></span> <span data-ttu-id="a52c0-109">Se il nome della definizione non viene specificato, verranno elencate tutte le definizioni SAS associate all'account di archiviazione gestita Key Vault specificato nel Vault.</span><span class="sxs-lookup"><span data-stu-id="a52c0-109">If the definition name is not specified, then all the SAS definitions associated with the specified Key Vault managed Storage Account in the vault are listed.</span></span>

## <span data-ttu-id="a52c0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a52c0-110">EXAMPLES</span></span>

### <span data-ttu-id="a52c0-111">Esempio 1: elencare tutte le definizioni di archiviazione SAS Key Vault Managed</span><span class="sxs-lookup"><span data-stu-id="a52c0-111">Example 1: List all Key Vault managed Storage SAS Definitions</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount'

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/accountsas
Vault Name  : myvault
AccountName : mystorageaccount
Name        : accountsas
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="a52c0-112">Elenca tutte le definizioni SAS associate all'account di archiviazione gestita Key Vault ' mystorageaccount ' gestito dal Vault ' Vault '</span><span class="sxs-lookup"><span data-stu-id="a52c0-112">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'</span></span>

### <span data-ttu-id="a52c0-113">Esempio 2: ottenere un account di archiviazione gestito Key Vault</span><span class="sxs-lookup"><span data-stu-id="a52c0-113">Example 2: Get a Key Vault managed Storage Account</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'accountsas'

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

<span data-ttu-id="a52c0-114">Ottiene i dettagli della definizione SAS "Accounts" associata all'account di archiviazione gestita Key Vault "mystorageaccount" gestito dalla volta "Vault".</span><span class="sxs-lookup"><span data-stu-id="a52c0-114">Gets the details of SAS Definition 'accountsas' associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'.</span></span>

### <span data-ttu-id="a52c0-115">Esempio 3: elencare tutte le definizioni di archiviazione SAS chiave archiviate con filtro</span><span class="sxs-lookup"><span data-stu-id="a52c0-115">Example 3: List all Key Vault managed Storage SAS Definitions using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name "account*"

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/accountsas1
Vault Name  : myvault
AccountName : mystorageaccount
Name        : accountsas1
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/accountsas2
Vault Name  : myvault
AccountName : mystorageaccount
Name        : accountsas2
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="a52c0-116">Elenca tutte le definizioni SAS associate all'account di archiviazione Managed Key Vault ' mystorageaccount ' gestito dal Vault ' Vault ' che inizia con "account".</span><span class="sxs-lookup"><span data-stu-id="a52c0-116">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault' that start with "account".</span></span>

## <span data-ttu-id="a52c0-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a52c0-117">PARAMETERS</span></span>

### <span data-ttu-id="a52c0-118">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a52c0-118">-AccountName</span></span>
<span data-ttu-id="a52c0-119">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="a52c0-119">Vault name.</span></span>
<span data-ttu-id="a52c0-120">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="a52c0-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="a52c0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a52c0-121">-DefaultProfile</span></span>
<span data-ttu-id="a52c0-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a52c0-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a52c0-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a52c0-123">-InputObject</span></span>
<span data-ttu-id="a52c0-124">Oggetto ManagedStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="a52c0-124">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="a52c0-125">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="a52c0-125">-InRemovedState</span></span>
<span data-ttu-id="a52c0-126">Specifica se visualizzare le definizioni SAS di archiviazione eliminate in precedenza nell'output.</span><span class="sxs-lookup"><span data-stu-id="a52c0-126">Specifies whether to show the previously deleted storage sas definitions in the output.</span></span>

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

### <span data-ttu-id="a52c0-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="a52c0-127">-Name</span></span>
<span data-ttu-id="a52c0-128">Nome della definizione di archiviazione SAS.</span><span class="sxs-lookup"><span data-stu-id="a52c0-128">Storage sas definition name.</span></span>
<span data-ttu-id="a52c0-129">Cmdlet costruisce il nome di dominio completo di una definizione SAS di archiviazione dal nome della volta, dall'ambiente attualmente selezionato, dal nome dell'account di archiviazione e dalla definizione SAS.</span><span class="sxs-lookup"><span data-stu-id="a52c0-129">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

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

### <span data-ttu-id="a52c0-130">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="a52c0-130">-VaultName</span></span>
<span data-ttu-id="a52c0-131">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="a52c0-131">Vault name.</span></span>
<span data-ttu-id="a52c0-132">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="a52c0-132">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="a52c0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a52c0-133">CommonParameters</span></span>
<span data-ttu-id="a52c0-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a52c0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a52c0-135">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a52c0-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a52c0-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a52c0-136">INPUTS</span></span>

### <span data-ttu-id="a52c0-137">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="a52c0-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="a52c0-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a52c0-138">OUTPUTS</span></span>

### <span data-ttu-id="a52c0-139">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="a52c0-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

### <span data-ttu-id="a52c0-140">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="a52c0-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

### <span data-ttu-id="a52c0-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="a52c0-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span></span>

### <span data-ttu-id="a52c0-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="a52c0-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="a52c0-143">Note</span><span class="sxs-lookup"><span data-stu-id="a52c0-143">NOTES</span></span>

## <span data-ttu-id="a52c0-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a52c0-144">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

