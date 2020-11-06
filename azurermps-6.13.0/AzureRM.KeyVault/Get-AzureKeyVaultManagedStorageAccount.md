---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: f3a1e4d1e938b84a434c07451f3d2294e203f440
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520210"
---
# <span data-ttu-id="d3a72-101">Get-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d3a72-101">Get-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="d3a72-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d3a72-102">SYNOPSIS</span></span>
<span data-ttu-id="d3a72-103">Ottiene gli account di archiviazione Azure gestiti Key Vault.</span><span class="sxs-lookup"><span data-stu-id="d3a72-103">Gets Key Vault managed Azure Storage Accounts.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3a72-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d3a72-104">SYNTAX</span></span>

### <span data-ttu-id="d3a72-105">ByAccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d3a72-105">ByAccountName (Default)</span></span>
```
Get-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [[-AccountName] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3a72-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d3a72-106">ByInputObject</span></span>
```
Get-AzureKeyVaultManagedStorageAccount [-InputObject] <PSKeyVault> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3a72-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d3a72-107">ByResourceId</span></span>
```
Get-AzureKeyVaultManagedStorageAccount [-ResourceId] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3a72-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3a72-108">DESCRIPTION</span></span>
<span data-ttu-id="d3a72-109">Ottiene un account di archiviazione di Azure Key Vault gestito se viene specificato il nome dell'account e le chiavi dell'account sono gestite dall'archivio specificato.</span><span class="sxs-lookup"><span data-stu-id="d3a72-109">Gets a Key Vault managed Azure Storage Account if the name of the account is specified and the account keys are managed by the specified vault.</span></span> <span data-ttu-id="d3a72-110">Se il nome dell'account non è specificato, verranno elencati tutti gli account le cui chiavi sono gestite da Vault specificato.</span><span class="sxs-lookup"><span data-stu-id="d3a72-110">If the account name is not specified, then all the accounts whose keys are managed by specified vault are listed.</span></span>

## <span data-ttu-id="d3a72-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d3a72-111">EXAMPLES</span></span>

### <span data-ttu-id="d3a72-112">Esempio 1: elenca tutti gli account di archiviazione gestiti Key Vault</span><span class="sxs-lookup"><span data-stu-id="d3a72-112">Example 1: List all Key Vault managed Storage Accounts</span></span>
```powershell
PS C:\> Get-AzureKeyVaultManagedStorageAccount -VaultName 'myvault'

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

<span data-ttu-id="d3a72-113">Elenca tutti gli account le cui chiavi sono gestite dalla volta "archivio"</span><span class="sxs-lookup"><span data-stu-id="d3a72-113">Lists all the accounts whose keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="d3a72-114">Esempio 2: ottenere un account di archiviazione gestito Key Vault</span><span class="sxs-lookup"><span data-stu-id="d3a72-114">Example 2: Get a Key Vault managed Storage Account</span></span>
```powershell
PS C:\> Get-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -Name 'mystorageaccount'

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

<span data-ttu-id="d3a72-115">Ottiene i dettagli dell'account di archiviazione gestita Key Vault di "mystorageaccount" se le relative chiavi vengono gestite dal Vault "archivio dati"</span><span class="sxs-lookup"><span data-stu-id="d3a72-115">Gets the details of Key Vault managed Storage Account of 'mystorageaccount' if its keys are managed by vault 'myvault'</span></span>

## <span data-ttu-id="d3a72-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d3a72-116">PARAMETERS</span></span>

### <span data-ttu-id="d3a72-117">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d3a72-117">-AccountName</span></span>
<span data-ttu-id="d3a72-118">Nome dell'account di archiviazione gestito Key Vault.</span><span class="sxs-lookup"><span data-stu-id="d3a72-118">Key Vault managed storage account name.</span></span> <span data-ttu-id="d3a72-119">Cmdlet crea l'FQDN di un nome di account di archiviazione gestito dal nome del Vault, dall'ambiente selezionato e dal nome dell'account di archiviazione modificato.</span><span class="sxs-lookup"><span data-stu-id="d3a72-119">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAccountName
Aliases: StorageAccountName, Name

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3a72-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3a72-120">-DefaultProfile</span></span>
<span data-ttu-id="d3a72-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d3a72-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d3a72-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3a72-122">-InputObject</span></span>
<span data-ttu-id="d3a72-123">Oggetto Vault.</span><span class="sxs-lookup"><span data-stu-id="d3a72-123">Vault object.</span></span>

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

### <span data-ttu-id="d3a72-124">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="d3a72-124">-InRemovedState</span></span>
<span data-ttu-id="d3a72-125">Specifica se visualizzare gli account di archiviazione eliminati in precedenza nell'output.</span><span class="sxs-lookup"><span data-stu-id="d3a72-125">Specifies whether to show the previously deleted storage accounts in the output.</span></span>

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

### <span data-ttu-id="d3a72-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3a72-126">-ResourceId</span></span>
<span data-ttu-id="d3a72-127">ID risorsa del Vault.</span><span class="sxs-lookup"><span data-stu-id="d3a72-127">Vault resource id.</span></span>

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

### <span data-ttu-id="d3a72-128">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="d3a72-128">-VaultName</span></span>
<span data-ttu-id="d3a72-129">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="d3a72-129">Vault name.</span></span>
<span data-ttu-id="d3a72-130">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="d3a72-130">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="d3a72-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3a72-131">CommonParameters</span></span>
<span data-ttu-id="d3a72-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3a72-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3a72-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3a72-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3a72-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d3a72-134">INPUTS</span></span>

### <span data-ttu-id="d3a72-135">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="d3a72-135">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="d3a72-136">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d3a72-136">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="d3a72-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d3a72-137">System.String</span></span>

## <span data-ttu-id="d3a72-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d3a72-138">OUTPUTS</span></span>

### <span data-ttu-id="d3a72-139">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="d3a72-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="d3a72-140">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d3a72-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

### <span data-ttu-id="d3a72-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="d3a72-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="d3a72-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d3a72-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="d3a72-143">Note</span><span class="sxs-lookup"><span data-stu-id="d3a72-143">NOTES</span></span>

## <span data-ttu-id="d3a72-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d3a72-144">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

