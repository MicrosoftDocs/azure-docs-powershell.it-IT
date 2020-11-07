---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: d57f672ef440515e69535503f006e08b4c924646
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861254"
---
# <span data-ttu-id="18202-101">Remove-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="18202-101">Remove-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="18202-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="18202-102">SYNOPSIS</span></span>
<span data-ttu-id="18202-103">Consente di rimuovere un account di archiviazione di Azure Key Vault gestito e tutte le definizioni SAS associate.</span><span class="sxs-lookup"><span data-stu-id="18202-103">Removes a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>

## <span data-ttu-id="18202-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="18202-104">SYNTAX</span></span>

```
Remove-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18202-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18202-105">DESCRIPTION</span></span>
<span data-ttu-id="18202-106">Dissocia un account di archiviazione di Azure da Key Vault.</span><span class="sxs-lookup"><span data-stu-id="18202-106">Disassociates an Azure Storage Account from Key Vault.</span></span> <span data-ttu-id="18202-107">In questo modo non viene rimosso un account di archiviazione di Azure, ma i tasti account vengono rimossi dall'archivio chiavi di Azure.</span><span class="sxs-lookup"><span data-stu-id="18202-107">This does not remove an Azure Storage Account but removes the account keys from being managed by Azure Key Vault.</span></span> <span data-ttu-id="18202-108">Vengono rimosse anche tutte le definizioni di archiviazione gestite di Key Vault associate.</span><span class="sxs-lookup"><span data-stu-id="18202-108">All associated Key Vault managed Storage SAS definitions are also removed.</span></span>

## <span data-ttu-id="18202-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="18202-109">EXAMPLES</span></span>

### <span data-ttu-id="18202-110">Esempio 1: rimuovere un account di archiviazione di Azure Key Vault gestito e tutte le definizioni SAS associate.</span><span class="sxs-lookup"><span data-stu-id="18202-110">Example 1: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>
```
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount'
```

<span data-ttu-id="18202-111">Annulla l'associazione dell'account di archiviazione di Azure "mystorageaccount" dal Vault Key "Vault" e interrompe la gestione delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="18202-111">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="18202-112">L'account "mystorageaccount" non verrà rimosso.</span><span class="sxs-lookup"><span data-stu-id="18202-112">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="18202-113">Verranno rimosse tutte le definizioni SAS di archiviazione gestite di Key Vault associate a questo account.</span><span class="sxs-lookup"><span data-stu-id="18202-113">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="18202-114">Esempio 2: rimuovere un account di archiviazione di Azure Key Vault gestito e tutte le definizioni SAS associate senza la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="18202-114">Example 2: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions without user confirmation.</span></span>
```
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Force -Confirm:$False
```

<span data-ttu-id="18202-115">Annulla l'associazione dell'account di archiviazione di Azure "mystorageaccount" dal Vault Key "Vault" e interrompe la gestione delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="18202-115">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="18202-116">L'account "mystorageaccount" non verrà rimosso.</span><span class="sxs-lookup"><span data-stu-id="18202-116">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="18202-117">Verranno rimosse tutte le definizioni SAS di archiviazione gestite di Key Vault associate a questo account.</span><span class="sxs-lookup"><span data-stu-id="18202-117">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

## <span data-ttu-id="18202-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="18202-118">PARAMETERS</span></span>

### <span data-ttu-id="18202-119">-AccountName</span><span class="sxs-lookup"><span data-stu-id="18202-119">-AccountName</span></span>
<span data-ttu-id="18202-120">Nome dell'account di archiviazione gestito Key Vault.</span><span class="sxs-lookup"><span data-stu-id="18202-120">Key Vault managed storage account name.</span></span> <span data-ttu-id="18202-121">Cmdlet crea l'FQDN di un nome di account di archiviazione gestito dal nome del Vault, dall'ambiente selezionato e dal nome dell'account di archiviazione modificato.</span><span class="sxs-lookup"><span data-stu-id="18202-121">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18202-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18202-122">-DefaultProfile</span></span>
<span data-ttu-id="18202-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="18202-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="18202-124">-Force</span><span class="sxs-lookup"><span data-stu-id="18202-124">-Force</span></span>
<span data-ttu-id="18202-125">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="18202-125">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18202-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="18202-126">-PassThru</span></span>
<span data-ttu-id="18202-127">Cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="18202-127">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="18202-128">Se questa opzione è specificata, cmdlet restituisce l'account di archiviazione gestita che è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="18202-128">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18202-129">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="18202-129">-VaultName</span></span>
<span data-ttu-id="18202-130">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="18202-130">Vault name.</span></span>
<span data-ttu-id="18202-131">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="18202-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="18202-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="18202-132">-Confirm</span></span>
<span data-ttu-id="18202-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18202-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18202-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18202-134">-WhatIf</span></span>
<span data-ttu-id="18202-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="18202-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18202-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="18202-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18202-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18202-137">CommonParameters</span></span>
<span data-ttu-id="18202-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18202-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18202-139">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18202-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18202-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="18202-140">INPUTS</span></span>

### <span data-ttu-id="18202-141">System. String</span><span class="sxs-lookup"><span data-stu-id="18202-141">System.String</span></span>

## <span data-ttu-id="18202-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="18202-142">OUTPUTS</span></span>

### <span data-ttu-id="18202-143">Microsoft. Azure. Commands. Vault. Models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="18202-143">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="18202-144">Note</span><span class="sxs-lookup"><span data-stu-id="18202-144">NOTES</span></span>

## <span data-ttu-id="18202-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="18202-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

