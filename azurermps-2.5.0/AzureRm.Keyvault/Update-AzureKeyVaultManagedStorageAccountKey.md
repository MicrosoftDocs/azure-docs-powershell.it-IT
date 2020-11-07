---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/update-azurekeyvaultmanagedstorageaccountkey
schema: 2.0.0
ms.openlocfilehash: d7bd1e776cc0593f57a17e8d83ecde3f6981973b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866325"
---
# <span data-ttu-id="b2ec6-101">Update-AzureKeyVaultManagedStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="b2ec6-101">Update-AzureKeyVaultManagedStorageAccountKey</span></span>

## <span data-ttu-id="b2ec6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b2ec6-102">SYNOPSIS</span></span>
<span data-ttu-id="b2ec6-103">Rigenera la chiave specificata dell'account di archiviazione di Azure con chiave Key Vault.</span><span class="sxs-lookup"><span data-stu-id="b2ec6-103">Regenerates the specified key of Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2ec6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b2ec6-104">SYNTAX</span></span>

```
Update-AzureKeyVaultManagedStorageAccountKey [-VaultName] <String> [-AccountName] <String> [-KeyName] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2ec6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2ec6-105">DESCRIPTION</span></span>
<span data-ttu-id="b2ec6-106">Rigenera la chiave specificata di un account di archiviazione di Azure con chiave Key Vault e imposta la chiave come chiave attiva.</span><span class="sxs-lookup"><span data-stu-id="b2ec6-106">Regenerates the specified key of Key Vault managed Azure Storage Account and sets the key as the active key.</span></span> <span data-ttu-id="b2ec6-107">Key Vault inoltra la chiamata a Azure Resource Manager per rigenerare la chiave.</span><span class="sxs-lookup"><span data-stu-id="b2ec6-107">Key Vault proxies the call to Azure Resource Manager to regenerate the key.</span></span> <span data-ttu-id="b2ec6-108">Il chiamante deve possedere le autorizzazioni per rigenerare le chiavi in un account di archiviazione di Azure specifico.</span><span class="sxs-lookup"><span data-stu-id="b2ec6-108">The caller must posses permissions to regenerate keys on given Azure Storage Account.</span></span>

## <span data-ttu-id="b2ec6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b2ec6-109">EXAMPLES</span></span>

### <span data-ttu-id="b2ec6-110">Esempio 1: rigenerare una chiave</span><span class="sxs-lookup"><span data-stu-id="b2ec6-110">Example 1: Regenerate a key</span></span>
```
PS C:\> Update-AzureKeyVaultManagedStorageAccountKey -VaultName 'myvault' -AccountName 'mystorageaccount' -KeyName 'key1'
```

<span data-ttu-id="b2ec6-111">Rigenera "Key1" dell'account "mystorageaccount" e imposta "Key1" come attivo dell'account di archiviazione di Azure Key.</span><span class="sxs-lookup"><span data-stu-id="b2ec6-111">Regenerates 'key1' of account 'mystorageaccount' and sets 'key1' as the active of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="b2ec6-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b2ec6-112">PARAMETERS</span></span>

### <span data-ttu-id="b2ec6-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b2ec6-113">-AccountName</span></span>
<span data-ttu-id="b2ec6-114">Nome dell'account di archiviazione gestito Key Vault.</span><span class="sxs-lookup"><span data-stu-id="b2ec6-114">Key Vault managed storage account name.</span></span> <span data-ttu-id="b2ec6-115">Cmdlet crea l'FQDN di un nome di account di archiviazione gestito dal nome del Vault, dall'ambiente selezionato e dal nome dell'account di archiviazione modificato.</span><span class="sxs-lookup"><span data-stu-id="b2ec6-115">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="b2ec6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2ec6-116">-DefaultProfile</span></span>
<span data-ttu-id="b2ec6-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b2ec6-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2ec6-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b2ec6-118">-Force</span></span>
<span data-ttu-id="b2ec6-119">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="b2ec6-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b2ec6-120">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="b2ec6-120">-KeyName</span></span>
<span data-ttu-id="b2ec6-121">Nome della chiave dell'account di archiviazione per rigenerare e rendere attivo.</span><span class="sxs-lookup"><span data-stu-id="b2ec6-121">Name of storage account key to regenerate and make active.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2ec6-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b2ec6-122">-PassThru</span></span>
<span data-ttu-id="b2ec6-123">Cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="b2ec6-123">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="b2ec6-124">Se questa opzione è specificata, cmdlet restituisce l'account di archiviazione gestita che è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="b2ec6-124">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="b2ec6-125">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="b2ec6-125">-VaultName</span></span>
<span data-ttu-id="b2ec6-126">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="b2ec6-126">Vault name.</span></span>
<span data-ttu-id="b2ec6-127">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="b2ec6-127">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="b2ec6-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b2ec6-128">-Confirm</span></span>
<span data-ttu-id="b2ec6-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2ec6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2ec6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2ec6-130">-WhatIf</span></span>
<span data-ttu-id="b2ec6-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b2ec6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2ec6-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b2ec6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2ec6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2ec6-133">CommonParameters</span></span>
<span data-ttu-id="b2ec6-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2ec6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2ec6-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2ec6-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2ec6-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b2ec6-136">INPUTS</span></span>

### <span data-ttu-id="b2ec6-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b2ec6-137">System.String</span></span>

## <span data-ttu-id="b2ec6-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b2ec6-138">OUTPUTS</span></span>

### <span data-ttu-id="b2ec6-139">Microsoft. Azure. Commands. Vault. Models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b2ec6-139">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="b2ec6-140">Note</span><span class="sxs-lookup"><span data-stu-id="b2ec6-140">NOTES</span></span>

## <span data-ttu-id="b2ec6-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b2ec6-141">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

