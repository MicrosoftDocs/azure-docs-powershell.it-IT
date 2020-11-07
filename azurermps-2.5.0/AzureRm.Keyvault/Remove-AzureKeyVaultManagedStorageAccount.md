---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
ms.openlocfilehash: 438d36a5c9081da3124c0ef5ee03c7eb9ad8f634
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865794"
---
# <span data-ttu-id="901cd-101">Remove-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="901cd-101">Remove-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="901cd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="901cd-102">SYNOPSIS</span></span>
<span data-ttu-id="901cd-103">Consente di rimuovere un account di archiviazione di Azure Key Vault gestito e tutte le definizioni SAS associate.</span><span class="sxs-lookup"><span data-stu-id="901cd-103">Removes a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="901cd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="901cd-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="901cd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="901cd-105">DESCRIPTION</span></span>
<span data-ttu-id="901cd-106">Dissocia un account di archiviazione di Azure da Key Vault.</span><span class="sxs-lookup"><span data-stu-id="901cd-106">Disassociates an Azure Storage Account from Key Vault.</span></span> <span data-ttu-id="901cd-107">In questo modo non viene rimosso un account di archiviazione di Azure, ma i tasti account vengono rimossi dall'archivio chiavi di Azure.</span><span class="sxs-lookup"><span data-stu-id="901cd-107">This does not remove an Azure Storage Account but removes the account keys from being managed by Azure Key Vault.</span></span> <span data-ttu-id="901cd-108">Vengono rimosse anche tutte le definizioni di archiviazione gestite di Key Vault associate.</span><span class="sxs-lookup"><span data-stu-id="901cd-108">All associated Key Vault managed Storage SAS definitions are also removed.</span></span>

## <span data-ttu-id="901cd-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="901cd-109">EXAMPLES</span></span>

### <span data-ttu-id="901cd-110">Esempio 1: rimuovere un account di archiviazione di Azure Key Vault gestito e tutte le definizioni SAS associate.</span><span class="sxs-lookup"><span data-stu-id="901cd-110">Example 1: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>
```
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount'
```

<span data-ttu-id="901cd-111">Annulla l'associazione dell'account di archiviazione di Azure "mystorageaccount" dal Vault Key "Vault" e interrompe la gestione delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="901cd-111">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="901cd-112">L'account "mystorageaccount" non verrà rimosso.</span><span class="sxs-lookup"><span data-stu-id="901cd-112">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="901cd-113">Verranno rimosse tutte le definizioni SAS di archiviazione gestite di Key Vault associate a questo account.</span><span class="sxs-lookup"><span data-stu-id="901cd-113">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="901cd-114">Esempio 2: rimuovere un account di archiviazione di Azure Key Vault gestito e tutte le definizioni SAS associate senza la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="901cd-114">Example 2: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions without user confirmation.</span></span>
```
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Force -Confirm:$False
```

<span data-ttu-id="901cd-115">Annulla l'associazione dell'account di archiviazione di Azure "mystorageaccount" dal Vault Key "Vault" e interrompe la gestione delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="901cd-115">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="901cd-116">L'account "mystorageaccount" non verrà rimosso.</span><span class="sxs-lookup"><span data-stu-id="901cd-116">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="901cd-117">Verranno rimosse tutte le definizioni SAS di archiviazione gestite di Key Vault associate a questo account.</span><span class="sxs-lookup"><span data-stu-id="901cd-117">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

## <span data-ttu-id="901cd-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="901cd-118">PARAMETERS</span></span>

### <span data-ttu-id="901cd-119">-AccountName</span><span class="sxs-lookup"><span data-stu-id="901cd-119">-AccountName</span></span>
<span data-ttu-id="901cd-120">Nome dell'account di archiviazione gestito Key Vault.</span><span class="sxs-lookup"><span data-stu-id="901cd-120">Key Vault managed storage account name.</span></span> <span data-ttu-id="901cd-121">Cmdlet crea l'FQDN di un nome di account di archiviazione gestito dal nome del Vault, dall'ambiente selezionato e dal nome dell'account di archiviazione modificato.</span><span class="sxs-lookup"><span data-stu-id="901cd-121">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="901cd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="901cd-122">-DefaultProfile</span></span>
<span data-ttu-id="901cd-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="901cd-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="901cd-124">-Force</span><span class="sxs-lookup"><span data-stu-id="901cd-124">-Force</span></span>
<span data-ttu-id="901cd-125">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="901cd-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="901cd-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="901cd-126">-PassThru</span></span>
<span data-ttu-id="901cd-127">Cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="901cd-127">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="901cd-128">Se questa opzione è specificata, cmdlet restituisce l'account di archiviazione gestita che è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="901cd-128">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="901cd-129">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="901cd-129">-VaultName</span></span>
<span data-ttu-id="901cd-130">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="901cd-130">Vault name.</span></span>
<span data-ttu-id="901cd-131">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="901cd-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="901cd-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="901cd-132">-Confirm</span></span>
<span data-ttu-id="901cd-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="901cd-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="901cd-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="901cd-134">-WhatIf</span></span>
<span data-ttu-id="901cd-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="901cd-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="901cd-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="901cd-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="901cd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="901cd-137">CommonParameters</span></span>
<span data-ttu-id="901cd-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="901cd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="901cd-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="901cd-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="901cd-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="901cd-140">INPUTS</span></span>

### <span data-ttu-id="901cd-141">System. String</span><span class="sxs-lookup"><span data-stu-id="901cd-141">System.String</span></span>

## <span data-ttu-id="901cd-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="901cd-142">OUTPUTS</span></span>

### <span data-ttu-id="901cd-143">Microsoft. Azure. Commands. Vault. Models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="901cd-143">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="901cd-144">Note</span><span class="sxs-lookup"><span data-stu-id="901cd-144">NOTES</span></span>

## <span data-ttu-id="901cd-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="901cd-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

