---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 89452f2a00aea9d3ab42300c2f28bde67fec0905
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323940"
---
# <span data-ttu-id="14f5e-101">Get-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="14f5e-101">Get-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="14f5e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="14f5e-102">SYNOPSIS</span></span>
<span data-ttu-id="14f5e-103">Ottiene gli account di archiviazione Azure gestiti Key Vault.</span><span class="sxs-lookup"><span data-stu-id="14f5e-103">Gets Key Vault managed Azure Storage Accounts.</span></span>

## <span data-ttu-id="14f5e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="14f5e-104">SYNTAX</span></span>

### <span data-ttu-id="14f5e-105">ByAccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="14f5e-105">ByAccountName (Default)</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-VaultName] <String> [[-AccountName] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14f5e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="14f5e-106">ByInputObject</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVault> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14f5e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="14f5e-107">ByResourceId</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-ResourceId] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14f5e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="14f5e-108">DESCRIPTION</span></span>
<span data-ttu-id="14f5e-109">Ottiene un account di archiviazione di Azure Key Vault gestito se viene specificato il nome dell'account e le chiavi dell'account sono gestite dall'archivio specificato.</span><span class="sxs-lookup"><span data-stu-id="14f5e-109">Gets a Key Vault managed Azure Storage Account if the name of the account is specified and the account keys are managed by the specified vault.</span></span> <span data-ttu-id="14f5e-110">Se il nome dell'account non è specificato, verranno elencati tutti gli account le cui chiavi sono gestite da Vault specificato.</span><span class="sxs-lookup"><span data-stu-id="14f5e-110">If the account name is not specified, then all the accounts whose keys are managed by specified vault are listed.</span></span>

## <span data-ttu-id="14f5e-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="14f5e-111">EXAMPLES</span></span>

### <span data-ttu-id="14f5e-112">Esempio 1: elenca tutti gli account di archiviazione gestiti Key Vault</span><span class="sxs-lookup"><span data-stu-id="14f5e-112">Example 1: List all Key Vault managed Storage Accounts</span></span>
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

<span data-ttu-id="14f5e-113">Elenca tutti gli account le cui chiavi sono gestite dalla volta "archivio"</span><span class="sxs-lookup"><span data-stu-id="14f5e-113">Lists all the accounts whose keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="14f5e-114">Esempio 2: ottenere un account di archiviazione gestito Key Vault</span><span class="sxs-lookup"><span data-stu-id="14f5e-114">Example 2: Get a Key Vault managed Storage Account</span></span>
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

<span data-ttu-id="14f5e-115">Ottiene i dettagli dell'account di archiviazione gestita Key Vault di "mystorageaccount" se le relative chiavi vengono gestite dal Vault "archivio dati"</span><span class="sxs-lookup"><span data-stu-id="14f5e-115">Gets the details of Key Vault managed Storage Account of 'mystorageaccount' if its keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="14f5e-116">Esempio 3: elencare tutti gli account di archiviazione gestiti Key Vault tramite filtro</span><span class="sxs-lookup"><span data-stu-id="14f5e-116">Example 3: List all Key Vault managed Storage Accounts using filtering</span></span>
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

<span data-ttu-id="14f5e-117">Elenca tutti gli account di cui le chiavi sono gestite dalla volta "Vault" che iniziano con "test"</span><span class="sxs-lookup"><span data-stu-id="14f5e-117">Lists all the accounts whose keys are managed by vault 'myvault' that start with "test"</span></span>

## <span data-ttu-id="14f5e-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="14f5e-118">PARAMETERS</span></span>

### <span data-ttu-id="14f5e-119">-AccountName</span><span class="sxs-lookup"><span data-stu-id="14f5e-119">-AccountName</span></span>
<span data-ttu-id="14f5e-120">Nome dell'account di archiviazione gestito Key Vault.</span><span class="sxs-lookup"><span data-stu-id="14f5e-120">Key Vault managed storage account name.</span></span> <span data-ttu-id="14f5e-121">Cmdlet crea l'FQDN di un nome di account di archiviazione gestito dal nome del Vault, dall'ambiente selezionato e dal nome dell'account di archiviazione modificato.</span><span class="sxs-lookup"><span data-stu-id="14f5e-121">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="14f5e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14f5e-122">-DefaultProfile</span></span>
<span data-ttu-id="14f5e-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="14f5e-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="14f5e-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14f5e-124">-InputObject</span></span>
<span data-ttu-id="14f5e-125">Oggetto Vault.</span><span class="sxs-lookup"><span data-stu-id="14f5e-125">Vault object.</span></span>

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

### <span data-ttu-id="14f5e-126">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="14f5e-126">-InRemovedState</span></span>
<span data-ttu-id="14f5e-127">Specifica se visualizzare gli account di archiviazione eliminati in precedenza nell'output.</span><span class="sxs-lookup"><span data-stu-id="14f5e-127">Specifies whether to show the previously deleted storage accounts in the output.</span></span>

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

### <span data-ttu-id="14f5e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14f5e-128">-ResourceId</span></span>
<span data-ttu-id="14f5e-129">ID risorsa del Vault.</span><span class="sxs-lookup"><span data-stu-id="14f5e-129">Vault resource id.</span></span>

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

### <span data-ttu-id="14f5e-130">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="14f5e-130">-VaultName</span></span>
<span data-ttu-id="14f5e-131">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="14f5e-131">Vault name.</span></span>
<span data-ttu-id="14f5e-132">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="14f5e-132">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="14f5e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14f5e-133">CommonParameters</span></span>
<span data-ttu-id="14f5e-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14f5e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14f5e-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14f5e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14f5e-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="14f5e-136">INPUTS</span></span>

### <span data-ttu-id="14f5e-137">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="14f5e-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="14f5e-138">System. String</span><span class="sxs-lookup"><span data-stu-id="14f5e-138">System.String</span></span>

## <span data-ttu-id="14f5e-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="14f5e-139">OUTPUTS</span></span>

### <span data-ttu-id="14f5e-140">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="14f5e-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="14f5e-141">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="14f5e-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

### <span data-ttu-id="14f5e-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="14f5e-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="14f5e-143">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="14f5e-143">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="14f5e-144">Note</span><span class="sxs-lookup"><span data-stu-id="14f5e-144">NOTES</span></span>

## <span data-ttu-id="14f5e-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="14f5e-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

