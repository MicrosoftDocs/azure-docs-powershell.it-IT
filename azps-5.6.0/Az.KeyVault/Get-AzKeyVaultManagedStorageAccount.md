---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 552a696a31b8c5fb26a1c6a17434ef53380d0491
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001485"
---
# <span data-ttu-id="27845-101">Get-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27845-101">Get-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="27845-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27845-102">SYNOPSIS</span></span>
<span data-ttu-id="27845-103">Recupera gli account di archiviazione di Azure gestiti da Vault.</span><span class="sxs-lookup"><span data-stu-id="27845-103">Gets Key Vault managed Azure Storage Accounts.</span></span>

## <span data-ttu-id="27845-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="27845-104">SYNTAX</span></span>

### <span data-ttu-id="27845-105">ByAccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="27845-105">ByAccountName (Default)</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-VaultName] <String> [[-AccountName] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27845-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="27845-106">ByInputObject</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVault> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27845-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="27845-107">ByResourceId</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-ResourceId] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27845-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="27845-108">DESCRIPTION</span></span>
<span data-ttu-id="27845-109">Ottiene un account di archiviazione di Azure gestito da Vault delle chiavi se il nome dell'account è specificato e le chiavi dell'account sono gestite dal vault specificato.</span><span class="sxs-lookup"><span data-stu-id="27845-109">Gets a Key Vault managed Azure Storage Account if the name of the account is specified and the account keys are managed by the specified vault.</span></span> <span data-ttu-id="27845-110">Se il nome dell'account non è specificato, vengono elencati tutti gli account le cui chiavi sono gestite dal vault specificato.</span><span class="sxs-lookup"><span data-stu-id="27845-110">If the account name is not specified, then all the accounts whose keys are managed by specified vault are listed.</span></span>

## <span data-ttu-id="27845-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="27845-111">EXAMPLES</span></span>

### <span data-ttu-id="27845-112">Esempio 1: Elencare tutti gli account di archiviazione gestiti da Vault chiave</span><span class="sxs-lookup"><span data-stu-id="27845-112">Example 1: List all Key Vault managed Storage Accounts</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault'

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="27845-113">Elenca tutti gli account le cui chiavi sono gestite dal vault 'myvault'</span><span class="sxs-lookup"><span data-stu-id="27845-113">Lists all the accounts whose keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="27845-114">Esempio 2: Ottenere un account di archiviazione gestito da Vault chiave</span><span class="sxs-lookup"><span data-stu-id="27845-114">Example 2: Get a Key Vault managed Storage Account</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -Name 'mystorageaccount'

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/maddie1/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key2
Auto Regenerate Key : False
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="27845-115">Recupera i dettagli dell'account di archiviazione gestito da Vault delle chiavi di 'mystorageaccount' se le chiavi sono gestite dal vault 'myvault'</span><span class="sxs-lookup"><span data-stu-id="27845-115">Gets the details of Key Vault managed Storage Account of 'mystorageaccount' if its keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="27845-116">Esempio 3: Elencare tutti gli account di archiviazione gestiti da Vault chiave usando il filtro</span><span class="sxs-lookup"><span data-stu-id="27845-116">Example 3: List all Key Vault managed Storage Accounts using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -Name "test*"

Id                  : https://myvault.vault.azure.net:443/storage/test1
Vault Name          : myvault
AccountName         : test1
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/test1
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :

Id                  : https://myvault.vault.azure.net:443/storage/test2
Vault Name          : myvault
AccountName         : test2
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/test2
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="27845-117">Elenca tutti gli account le cui chiavi sono gestite dal vault 'myvault' che iniziano con "test"</span><span class="sxs-lookup"><span data-stu-id="27845-117">Lists all the accounts whose keys are managed by vault 'myvault' that start with "test"</span></span>

## <span data-ttu-id="27845-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27845-118">PARAMETERS</span></span>

### <span data-ttu-id="27845-119">-AccountName</span><span class="sxs-lookup"><span data-stu-id="27845-119">-AccountName</span></span>
<span data-ttu-id="27845-120">Nome dell'account di archiviazione gestito dal Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="27845-120">Key Vault managed storage account name.</span></span> <span data-ttu-id="27845-121">Il cmdlet crea l'FQDN di un account di archiviazione gestito dal nome del vault, dall'ambiente attualmente selezionato e dal nome dell'account di archiviazione gestito.</span><span class="sxs-lookup"><span data-stu-id="27845-121">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAccountName
Aliases: StorageAccountName, Name

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="27845-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27845-122">-DefaultProfile</span></span>
<span data-ttu-id="27845-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="27845-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="27845-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27845-124">-InputObject</span></span>
<span data-ttu-id="27845-125">Oggetto Vault.</span><span class="sxs-lookup"><span data-stu-id="27845-125">Vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27845-126">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="27845-126">-InRemovedState</span></span>
<span data-ttu-id="27845-127">Specifica se visualizzare gli account di archiviazione eliminati in precedenza nell'output.</span><span class="sxs-lookup"><span data-stu-id="27845-127">Specifies whether to show the previously deleted storage accounts in the output.</span></span>

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

### <span data-ttu-id="27845-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27845-128">-ResourceId</span></span>
<span data-ttu-id="27845-129">ID risorsa Vault.</span><span class="sxs-lookup"><span data-stu-id="27845-129">Vault resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27845-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="27845-130">-VaultName</span></span>
<span data-ttu-id="27845-131">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="27845-131">Vault name.</span></span>
<span data-ttu-id="27845-132">Il cmdlet crea l'FQDN di un vault in base al nome e all'ambiente attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="27845-132">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27845-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27845-133">CommonParameters</span></span>
<span data-ttu-id="27845-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27845-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27845-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="27845-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27845-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="27845-136">INPUTS</span></span>

### <span data-ttu-id="27845-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="27845-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="27845-138">System.String</span><span class="sxs-lookup"><span data-stu-id="27845-138">System.String</span></span>

## <span data-ttu-id="27845-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="27845-139">OUTPUTS</span></span>

### <span data-ttu-id="27845-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="27845-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="27845-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27845-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

### <span data-ttu-id="27845-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="27845-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="27845-143">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27845-143">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="27845-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="27845-144">NOTES</span></span>

## <span data-ttu-id="27845-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="27845-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

