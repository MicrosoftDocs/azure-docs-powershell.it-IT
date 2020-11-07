---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 70ee1aaf9fb082819c626c43ba5c08ad01f0f1d6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863045"
---
# <span data-ttu-id="82c4c-101">Get-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="82c4c-101">Get-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="82c4c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="82c4c-102">SYNOPSIS</span></span>
<span data-ttu-id="82c4c-103">Ottiene gli account di archiviazione Azure gestiti Key Vault.</span><span class="sxs-lookup"><span data-stu-id="82c4c-103">Gets Key Vault managed Azure Storage Accounts.</span></span>

## <span data-ttu-id="82c4c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="82c4c-104">SYNTAX</span></span>

### <span data-ttu-id="82c4c-105">ByVaultName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="82c4c-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="82c4c-106">ByAccountName</span><span class="sxs-lookup"><span data-stu-id="82c4c-106">ByAccountName</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82c4c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82c4c-107">DESCRIPTION</span></span>
<span data-ttu-id="82c4c-108">Ottiene un account di archiviazione di Azure Key Vault gestito se viene specificato il nome dell'account e le chiavi dell'account sono gestite dall'archivio specificato.</span><span class="sxs-lookup"><span data-stu-id="82c4c-108">Gets a Key Vault managed Azure Storage Account if the name of the account is specified and the account keys are managed by the specified vault.</span></span> <span data-ttu-id="82c4c-109">Se il nome dell'account non è specificato, verranno elencati tutti gli account le cui chiavi sono gestite da Vault specificato.</span><span class="sxs-lookup"><span data-stu-id="82c4c-109">If the account name is not specified, then all the accounts whose keys are managed by specified vault are listed.</span></span>

## <span data-ttu-id="82c4c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="82c4c-110">EXAMPLES</span></span>

### <span data-ttu-id="82c4c-111">Esempio 1: elenca tutti gli account di archiviazione gestiti Key Vault</span><span class="sxs-lookup"><span data-stu-id="82c4c-111">Example 1: List all Key Vault managed Storage Accounts</span></span>
```
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault'
```

<span data-ttu-id="82c4c-112">Elenca tutti gli account le cui chiavi sono gestite dalla volta "archivio"</span><span class="sxs-lookup"><span data-stu-id="82c4c-112">Lists all the accounts whose keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="82c4c-113">Esempio 2: ottenere un account di archiviazione gestito Key Vault</span><span class="sxs-lookup"><span data-stu-id="82c4c-113">Example 2: Get a Key Vault managed Storage Account</span></span>
```
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -Name 'mystorageaccount'
```

<span data-ttu-id="82c4c-114">Ottiene i dettagli dell'account di archiviazione gestita Key Vault di "mystorageaccount" se le relative chiavi vengono gestite dal Vault "archivio dati"</span><span class="sxs-lookup"><span data-stu-id="82c4c-114">Gets the details of Key Vault managed Storage Account of 'mystorageaccount' if its keys are managed by vault 'myvault'</span></span>

## <span data-ttu-id="82c4c-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="82c4c-115">PARAMETERS</span></span>

### <span data-ttu-id="82c4c-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="82c4c-116">-AccountName</span></span>
<span data-ttu-id="82c4c-117">Nome dell'account di archiviazione gestito Key Vault.</span><span class="sxs-lookup"><span data-stu-id="82c4c-117">Key Vault managed storage account name.</span></span> <span data-ttu-id="82c4c-118">Cmdlet crea l'FQDN di un nome di account di archiviazione gestito dal nome del Vault, dall'ambiente selezionato e dal nome dell'account di archiviazione modificato.</span><span class="sxs-lookup"><span data-stu-id="82c4c-118">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: String
Parameter Sets: ByAccountName
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82c4c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82c4c-119">-DefaultProfile</span></span>
<span data-ttu-id="82c4c-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="82c4c-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="82c4c-121">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="82c4c-121">-VaultName</span></span>
<span data-ttu-id="82c4c-122">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="82c4c-122">Vault name.</span></span>
<span data-ttu-id="82c4c-123">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="82c4c-123">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="82c4c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82c4c-124">CommonParameters</span></span>
<span data-ttu-id="82c4c-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82c4c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82c4c-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82c4c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82c4c-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="82c4c-127">INPUTS</span></span>

### <span data-ttu-id="82c4c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="82c4c-128">System.String</span></span>

## <span data-ttu-id="82c4c-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="82c4c-129">OUTPUTS</span></span>

### <span data-ttu-id="82c4c-130">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. Vault. Models. ManagedStorageAccount, Microsoft. Azure. Commands. Vault, Version = 2.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="82c4c-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount, Microsoft.Azure.Commands.KeyVault, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="82c4c-131">Microsoft. Azure. Commands. Vault. Models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="82c4c-131">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="82c4c-132">Note</span><span class="sxs-lookup"><span data-stu-id="82c4c-132">NOTES</span></span>

## <span data-ttu-id="82c4c-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="82c4c-133">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

