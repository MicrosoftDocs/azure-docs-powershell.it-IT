---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 9859c6f17f393a5ca691c34e3ee144e24ab59fa8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686319"
---
# <span data-ttu-id="2291a-101">Remove-AzureKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="2291a-101">Remove-AzureKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="2291a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2291a-102">SYNOPSIS</span></span>
<span data-ttu-id="2291a-103">Consente di rimuovere una chiave di archiviazione delle definizioni SAS storage di Azure.</span><span class="sxs-lookup"><span data-stu-id="2291a-103">Removes a Key Vault managed Azure Storage SAS definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2291a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2291a-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2291a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2291a-105">DESCRIPTION</span></span>
<span data-ttu-id="2291a-106">Consente di rimuovere una chiave di archiviazione delle definizioni SAS storage di Azure.</span><span class="sxs-lookup"><span data-stu-id="2291a-106">Removes a Key Vault managed Azure Storage SAS definitions.</span></span> <span data-ttu-id="2291a-107">Viene inoltre rimosso il segreto usato per ottenere il token SAS per la definizione SAS.</span><span class="sxs-lookup"><span data-stu-id="2291a-107">This also removes the secret used to get the SAS token per this SAS definition.</span></span>

## <span data-ttu-id="2291a-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2291a-108">EXAMPLES</span></span>

### <span data-ttu-id="2291a-109">Esempio 1: rimuovere una definizione della chiave di archiviazione di Azure gestita da Key Vault.</span><span class="sxs-lookup"><span data-stu-id="2291a-109">Example 1: Remove a Key Vault managed Azure Storage SAS definition.</span></span>
```
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef'
```

<span data-ttu-id="2291a-110">Consente di rimuovere una definizione SAS di archiviazione gestita Key Vault mysasdef associata all'account "mystorageaccount" nel Vault "Vault".</span><span class="sxs-lookup"><span data-stu-id="2291a-110">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

### <span data-ttu-id="2291a-111">Esempio 2: rimuovere una definizione della chiave archiviata di Azure storage SAS senza la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="2291a-111">Example 2: Remove a Key Vault managed Azure Storage SAS definition without user confirmation.</span></span>
```
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef' -Force -Confirm:$False
```

<span data-ttu-id="2291a-112">Consente di rimuovere una definizione SAS di archiviazione gestita Key Vault mysasdef associata all'account "mystorageaccount" nel Vault "Vault".</span><span class="sxs-lookup"><span data-stu-id="2291a-112">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

## <span data-ttu-id="2291a-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2291a-113">PARAMETERS</span></span>

### <span data-ttu-id="2291a-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2291a-114">-AccountName</span></span>
<span data-ttu-id="2291a-115">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2291a-115">Storage account name.</span></span>
<span data-ttu-id="2291a-116">Cmdlet crea l'FQDN di un nome di account di archiviazione gestito dal nome del Vault, l'ambiente selezionato e il nome dell'account di archiviazione corrente.</span><span class="sxs-lookup"><span data-stu-id="2291a-116">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and storage account name.</span></span>

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

### <span data-ttu-id="2291a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2291a-117">-DefaultProfile</span></span>
<span data-ttu-id="2291a-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="2291a-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2291a-119">-Force</span><span class="sxs-lookup"><span data-stu-id="2291a-119">-Force</span></span>
<span data-ttu-id="2291a-120">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="2291a-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2291a-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="2291a-121">-Name</span></span>
<span data-ttu-id="2291a-122">Nome della definizione di archiviazione SAS.</span><span class="sxs-lookup"><span data-stu-id="2291a-122">Storage sas definition name.</span></span>
<span data-ttu-id="2291a-123">Cmdlet costruisce il nome di dominio completo di una definizione SAS di archiviazione dal nome della volta, dall'ambiente attualmente selezionato, dal nome dell'account di archiviazione e dalla definizione SAS.</span><span class="sxs-lookup"><span data-stu-id="2291a-123">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2291a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2291a-124">-PassThru</span></span>
<span data-ttu-id="2291a-125">Cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="2291a-125">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="2291a-126">Se questa opzione è specificata, cmdlet restituisce l'account di archiviazione gestita che è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="2291a-126">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="2291a-127">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="2291a-127">-VaultName</span></span>
<span data-ttu-id="2291a-128">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="2291a-128">Vault name.</span></span>
<span data-ttu-id="2291a-129">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="2291a-129">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="2291a-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2291a-130">-Confirm</span></span>
<span data-ttu-id="2291a-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2291a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2291a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2291a-132">-WhatIf</span></span>
<span data-ttu-id="2291a-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2291a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2291a-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2291a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2291a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2291a-135">CommonParameters</span></span>
<span data-ttu-id="2291a-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2291a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2291a-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2291a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2291a-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2291a-138">INPUTS</span></span>

### <span data-ttu-id="2291a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="2291a-139">System.String</span></span>

## <span data-ttu-id="2291a-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2291a-140">OUTPUTS</span></span>

### <span data-ttu-id="2291a-141">Microsoft. Azure. Commands. Vault. Models. ManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="2291a-141">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinition</span></span>

## <span data-ttu-id="2291a-142">Note</span><span class="sxs-lookup"><span data-stu-id="2291a-142">NOTES</span></span>

## <span data-ttu-id="2291a-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2291a-143">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)
