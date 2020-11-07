---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultmanagedstoragesasdefinition
schema: 2.0.0
ms.openlocfilehash: 6a1994979cc6521cee083b07f336a76a54dd7cb7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866511"
---
# <span data-ttu-id="8288c-101">Get-AzureKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="8288c-101">Get-AzureKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="8288c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8288c-102">SYNOPSIS</span></span>
<span data-ttu-id="8288c-103">Ottiene le definizioni SAS di archiviazione Managed Key Vault.</span><span class="sxs-lookup"><span data-stu-id="8288c-103">Gets Key Vault managed Storage SAS Definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8288c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8288c-104">SYNTAX</span></span>

### <span data-ttu-id="8288c-105">ByAccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8288c-105">ByAccountName (Default)</span></span>
```
Get-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8288c-106">ByDefinitionName</span><span class="sxs-lookup"><span data-stu-id="8288c-106">ByDefinitionName</span></span>
```
Get-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8288c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8288c-107">DESCRIPTION</span></span>
<span data-ttu-id="8288c-108">Ottiene una definizione della chiave di archiviazione gestita di SAS se il nome della definizione è specificato.</span><span class="sxs-lookup"><span data-stu-id="8288c-108">Gets a Key Vault managed Storage SAS Definition if the name of the definition is specified.</span></span> <span data-ttu-id="8288c-109">Se il nome della definizione non viene specificato, verranno elencate tutte le definizioni SAS associate all'account di archiviazione gestita Key Vault specificato nel Vault.</span><span class="sxs-lookup"><span data-stu-id="8288c-109">If the definition name is not specified, then all the SAS definitions associated with the specified Key Vault managed Storage Account in the vault are listed.</span></span>

## <span data-ttu-id="8288c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8288c-110">EXAMPLES</span></span>

### <span data-ttu-id="8288c-111">Esempio 1: elencare tutte le definizioni di archiviazione SAS Key Vault Managed</span><span class="sxs-lookup"><span data-stu-id="8288c-111">Example 1: List all Key Vault managed Storage SAS Definitions</span></span>
```
PS C:\> Get-AzureKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount'
```

<span data-ttu-id="8288c-112">Elenca tutte le definizioni SAS associate all'account di archiviazione gestita Key Vault ' mystorageaccount ' gestito dal Vault ' Vault '</span><span class="sxs-lookup"><span data-stu-id="8288c-112">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'</span></span>

### <span data-ttu-id="8288c-113">Esempio 2: ottenere un account di archiviazione gestito Key Vault</span><span class="sxs-lookup"><span data-stu-id="8288c-113">Example 2: Get a Key Vault managed Storage Account</span></span>
```
PS C:\> Get-AzureKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasDef'
```

<span data-ttu-id="8288c-114">Ottiene i dettagli della definizione SAS "mysasDef" associata all'account di archiviazione gestita Key Vault "mystorageaccount" gestito dal Vault "archivio dati".</span><span class="sxs-lookup"><span data-stu-id="8288c-114">Gets the details of SAS Definition 'mysasDef' associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'.</span></span>

## <span data-ttu-id="8288c-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8288c-115">PARAMETERS</span></span>

### <span data-ttu-id="8288c-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8288c-116">-AccountName</span></span>
<span data-ttu-id="8288c-117">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="8288c-117">Vault name.</span></span>
<span data-ttu-id="8288c-118">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="8288c-118">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8288c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8288c-119">-DefaultProfile</span></span>
<span data-ttu-id="8288c-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8288c-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8288c-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="8288c-121">-Name</span></span>
<span data-ttu-id="8288c-122">Nome della definizione di archiviazione SAS.</span><span class="sxs-lookup"><span data-stu-id="8288c-122">Storage sas definition name.</span></span>
<span data-ttu-id="8288c-123">Cmdlet costruisce il nome di dominio completo di una definizione SAS di archiviazione dal nome della volta, dall'ambiente attualmente selezionato, dal nome dell'account di archiviazione e dalla definizione SAS.</span><span class="sxs-lookup"><span data-stu-id="8288c-123">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: String
Parameter Sets: ByDefinitionName
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8288c-124">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="8288c-124">-VaultName</span></span>
<span data-ttu-id="8288c-125">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="8288c-125">Vault name.</span></span>
<span data-ttu-id="8288c-126">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="8288c-126">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="8288c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8288c-127">CommonParameters</span></span>
<span data-ttu-id="8288c-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8288c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8288c-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8288c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8288c-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8288c-130">INPUTS</span></span>

### <span data-ttu-id="8288c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="8288c-131">System.String</span></span>

## <span data-ttu-id="8288c-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8288c-132">OUTPUTS</span></span>

### <span data-ttu-id="8288c-133">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. Vault. Models. ManagedStorageSasDefinitionListItem, Microsoft. Azure. Commands. Vault, Version = 2.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="8288c-133">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinitionListItem, Microsoft.Azure.Commands.KeyVault, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="8288c-134">Microsoft. Azure. Commands. Vault. Models. ManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="8288c-134">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinition</span></span>

## <span data-ttu-id="8288c-135">Note</span><span class="sxs-lookup"><span data-stu-id="8288c-135">NOTES</span></span>

## <span data-ttu-id="8288c-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8288c-136">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

