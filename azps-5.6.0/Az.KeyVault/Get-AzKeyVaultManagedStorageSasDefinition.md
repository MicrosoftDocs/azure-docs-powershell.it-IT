---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: acb0e2811f184f7c3162635b87849a35ce9156ac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001470"
---
# <span data-ttu-id="ff13e-101">Get-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="ff13e-101">Get-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="ff13e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff13e-102">SYNOPSIS</span></span>
<span data-ttu-id="ff13e-103">Recupera le definizioni della firma di accesso condiviso di archiviazione gestite da Vault.</span><span class="sxs-lookup"><span data-stu-id="ff13e-103">Gets Key Vault managed Storage SAS Definitions.</span></span>

## <span data-ttu-id="ff13e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ff13e-104">SYNTAX</span></span>

### <span data-ttu-id="ff13e-105">ByDefinitionName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ff13e-105">ByDefinitionName (Default)</span></span>
```
Get-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [[-Name] <String>]
 [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff13e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ff13e-106">ByInputObject</span></span>
```
Get-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-Name] <String>] [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff13e-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ff13e-107">DESCRIPTION</span></span>
<span data-ttu-id="ff13e-108">Ottiene una definizione della firma di accesso condiviso gestita dal Vault della chiave se è specificato il nome della definizione.</span><span class="sxs-lookup"><span data-stu-id="ff13e-108">Gets a Key Vault managed Storage SAS Definition if the name of the definition is specified.</span></span> <span data-ttu-id="ff13e-109">Se il nome della definizione non è specificato, vengono elencate tutte le definizioni di firma di accesso condiviso associate all'account di archiviazione gestito dal Vault delle chiavi specificato nel vault.</span><span class="sxs-lookup"><span data-stu-id="ff13e-109">If the definition name is not specified, then all the SAS definitions associated with the specified Key Vault managed Storage Account in the vault are listed.</span></span>

## <span data-ttu-id="ff13e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ff13e-110">EXAMPLES</span></span>

### <span data-ttu-id="ff13e-111">Esempio 1: Elencare tutte le definizioni saS di archiviazione gestite da Vault</span><span class="sxs-lookup"><span data-stu-id="ff13e-111">Example 1: List all Key Vault managed Storage SAS Definitions</span></span>
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

<span data-ttu-id="ff13e-112">Elenca tutte le definizioni di firma di accesso condiviso associate all'account di archiviazione gestito da Vault chiave 'mystorageaccount' gestito dal vault 'myvault'</span><span class="sxs-lookup"><span data-stu-id="ff13e-112">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'</span></span>

### <span data-ttu-id="ff13e-113">Esempio 2: Ottenere un account di archiviazione gestito da Vault chiave</span><span class="sxs-lookup"><span data-stu-id="ff13e-113">Example 2: Get a Key Vault managed Storage Account</span></span>
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

<span data-ttu-id="ff13e-114">Recupera i dettagli della definizione della firma di accesso condiviso "accountsas" associata all'account di archiviazione gestito da Vault chiave 'mystorageaccount' gestito dal vault 'myvault'.</span><span class="sxs-lookup"><span data-stu-id="ff13e-114">Gets the details of SAS Definition 'accountsas' associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'.</span></span>

### <span data-ttu-id="ff13e-115">Esempio 3: Elencare tutte le definizioni saS di archiviazione gestite da Vault con il filtro</span><span class="sxs-lookup"><span data-stu-id="ff13e-115">Example 3: List all Key Vault managed Storage SAS Definitions using filtering</span></span>
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

<span data-ttu-id="ff13e-116">Elenca tutte le definizioni di firma di accesso condiviso associate all'account di archiviazione gestito da Vault chiave 'mystorageaccount' gestito dal vault 'myvault' che iniziano con "account".</span><span class="sxs-lookup"><span data-stu-id="ff13e-116">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault' that start with "account".</span></span>

## <span data-ttu-id="ff13e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff13e-117">PARAMETERS</span></span>

### <span data-ttu-id="ff13e-118">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ff13e-118">-AccountName</span></span>
<span data-ttu-id="ff13e-119">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="ff13e-119">Vault name.</span></span>
<span data-ttu-id="ff13e-120">Il cmdlet crea l'FQDN di un vault in base al nome e all'ambiente attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="ff13e-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="ff13e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff13e-121">-DefaultProfile</span></span>
<span data-ttu-id="ff13e-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ff13e-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff13e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff13e-123">-InputObject</span></span>
<span data-ttu-id="ff13e-124">Oggetto ManagedStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="ff13e-124">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="ff13e-125">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="ff13e-125">-InRemovedState</span></span>
<span data-ttu-id="ff13e-126">Specifica se visualizzare le definizioni sas di archiviazione eliminate in precedenza nell'output.</span><span class="sxs-lookup"><span data-stu-id="ff13e-126">Specifies whether to show the previously deleted storage sas definitions in the output.</span></span>

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

### <span data-ttu-id="ff13e-127">-Name</span><span class="sxs-lookup"><span data-stu-id="ff13e-127">-Name</span></span>
<span data-ttu-id="ff13e-128">Nome della definizione della firma di accesso condiviso per l'archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ff13e-128">Storage sas definition name.</span></span>
<span data-ttu-id="ff13e-129">Il cmdlet crea l'FQDN di una definizione di firma di accesso condiviso per l'archiviazione dal nome del vault, dall'ambiente attualmente selezionato, dal nome dell'account di archiviazione e dal nome della definizione della firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="ff13e-129">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

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

### <span data-ttu-id="ff13e-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ff13e-130">-VaultName</span></span>
<span data-ttu-id="ff13e-131">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="ff13e-131">Vault name.</span></span>
<span data-ttu-id="ff13e-132">Il cmdlet crea l'FQDN di un vault in base al nome e all'ambiente attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="ff13e-132">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="ff13e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff13e-133">CommonParameters</span></span>
<span data-ttu-id="ff13e-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff13e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff13e-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ff13e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff13e-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="ff13e-136">INPUTS</span></span>

### <span data-ttu-id="ff13e-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="ff13e-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="ff13e-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ff13e-138">OUTPUTS</span></span>

### <span data-ttu-id="ff13e-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="ff13e-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

### <span data-ttu-id="ff13e-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="ff13e-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

### <span data-ttu-id="ff13e-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="ff13e-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span></span>

### <span data-ttu-id="ff13e-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="ff13e-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="ff13e-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="ff13e-143">NOTES</span></span>

## <span data-ttu-id="ff13e-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ff13e-144">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

