---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/update-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: b16ceeb2409c2709286b970f857fcb9079bf067a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512544"
---
# <span data-ttu-id="c6e76-101">Update-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c6e76-101">Update-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="c6e76-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c6e76-102">SYNOPSIS</span></span>
<span data-ttu-id="c6e76-103">Aggiornare gli attributi modificabili di un account di archiviazione di Azure Key Vault gestito.</span><span class="sxs-lookup"><span data-stu-id="c6e76-103">Update editable attributes of a Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6e76-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c6e76-104">SYNTAX</span></span>

```
Update-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-ActiveKeyName <String>] [-AutoRegenerateKey <Boolean>] [-RegenerationPeriod <TimeSpan>] [-Enable <Boolean>]
 [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c6e76-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c6e76-105">DESCRIPTION</span></span>
<span data-ttu-id="c6e76-106">Aggiornare gli attributi modificabili di un account di archiviazione di Azure Key Vault gestito.</span><span class="sxs-lookup"><span data-stu-id="c6e76-106">Update the editable attributes of a Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="c6e76-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c6e76-107">EXAMPLES</span></span>

### <span data-ttu-id="c6e76-108">Esempio 1: aggiornare la chiave attiva in "key2" in un account di archiviazione di Azure con chiave archiviata Key.</span><span class="sxs-lookup"><span data-stu-id="c6e76-108">Example 1:Update the active key to 'key2' on a Key Vault managed Azure Storage Account.</span></span>
```
PS C:\> Update-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -ActiveKeyName 'key2'
```

<span data-ttu-id="c6e76-109">Aggiorna la chiave attiva dell'account di archiviazione di Azure Key Vault in "key2".</span><span class="sxs-lookup"><span data-stu-id="c6e76-109">Updates the Key Vault managed Azure Storage Account active key to 'key2'.</span></span> <span data-ttu-id="c6e76-110">"key2" verrà usato per generare token SAS dopo questo aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="c6e76-110">'key2' will be used to generate SAS tokens after this update.</span></span>

## <span data-ttu-id="c6e76-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c6e76-111">PARAMETERS</span></span>

### <span data-ttu-id="c6e76-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c6e76-112">-AccountName</span></span>
<span data-ttu-id="c6e76-113">Nome dell'account di archiviazione gestito Key Vault.</span><span class="sxs-lookup"><span data-stu-id="c6e76-113">Key Vault managed storage account name.</span></span> <span data-ttu-id="c6e76-114">Cmdlet crea l'FQDN di un nome di account di archiviazione gestito dal nome del Vault, dall'ambiente selezionato e dal nome dell'account di archiviazione modificato.</span><span class="sxs-lookup"><span data-stu-id="c6e76-114">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="c6e76-115">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="c6e76-115">-ActiveKeyName</span></span>
<span data-ttu-id="c6e76-116">Nome chiave attiva.</span><span class="sxs-lookup"><span data-stu-id="c6e76-116">Active key name.</span></span>
<span data-ttu-id="c6e76-117">Se non specificato, il valore esistente del nome della chiave attiva dell'account di archiviazione gestito rimane invariato</span><span class="sxs-lookup"><span data-stu-id="c6e76-117">If not specified, the existing value of managed storage account's active key name remains unchanged</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6e76-118">-AutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="c6e76-118">-AutoRegenerateKey</span></span>
<span data-ttu-id="c6e76-119">Chiave di rigenerazione automatica.</span><span class="sxs-lookup"><span data-stu-id="c6e76-119">Auto regenerate key.</span></span>
<span data-ttu-id="c6e76-120">Se non specificato, il valore esistente della chiave di rigenerazione automatica dell'account di archiviazione gestita rimane invariato</span><span class="sxs-lookup"><span data-stu-id="c6e76-120">If not specified, the existing value of auto regenerate key of managed storage account remains unchanged</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6e76-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6e76-121">-DefaultProfile</span></span>
<span data-ttu-id="c6e76-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c6e76-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c6e76-123">-Enable</span><span class="sxs-lookup"><span data-stu-id="c6e76-123">-Enable</span></span>
<span data-ttu-id="c6e76-124">Se presente, Abilita l'uso di una chiave dell'account di archiviazione gestita per la generazione di token SAS se value è true.</span><span class="sxs-lookup"><span data-stu-id="c6e76-124">If present, enables a use of a managed storage account key for sas token generation if value is true.</span></span> <span data-ttu-id="c6e76-125">Disabilita l'uso di una chiave dell'account di archiviazione gestita per la generazione di token SAS se value è false.</span><span class="sxs-lookup"><span data-stu-id="c6e76-125">Disables use of a managed storage account key for sas token generation if value is false.</span></span> <span data-ttu-id="c6e76-126">Se non specificato, il valore esistente dello stato abilitato/disabilitato dell'account di archiviazione rimane invariato.</span><span class="sxs-lookup"><span data-stu-id="c6e76-126">If not specified, the existing value of the storage account's enabled/disabled state remains unchanged.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6e76-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c6e76-127">-PassThru</span></span>
<span data-ttu-id="c6e76-128">Cmdlet non restituisce Object per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="c6e76-128">Cmdlet does not return object by default.</span></span> <span data-ttu-id="c6e76-129">Se questa opzione è specificata, restituire l'oggetto account di archiviazione gestita.</span><span class="sxs-lookup"><span data-stu-id="c6e76-129">If this switch is specified, return managed storage account object.</span></span>

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

### <span data-ttu-id="c6e76-130">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="c6e76-130">-RegenerationPeriod</span></span>
<span data-ttu-id="c6e76-131">Periodo di rigenerazione.</span><span class="sxs-lookup"><span data-stu-id="c6e76-131">Regeneration period.</span></span> <span data-ttu-id="c6e76-132">Se la chiave di rigenerazione automatica è abilitata, questo valore specifica l'intervallo di valori TimeSpan dopo il quale il tasto inattivo dell'account di archiviazione gestito viene rigenerato automaticamente e diventa la chiave attiva.</span><span class="sxs-lookup"><span data-stu-id="c6e76-132">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the active key.</span></span> <span data-ttu-id="c6e76-133">Se non specificato, il valore esistente del periodo di rigenerazione delle chiavi dell'account di archiviazione gestita rimane invariato</span><span class="sxs-lookup"><span data-stu-id="c6e76-133">If not specified, the existing value of regeneration period of keys of managed storage account remains unchanged</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6e76-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="c6e76-134">-Tag</span></span>
<span data-ttu-id="c6e76-135">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="c6e76-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c6e76-136">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="c6e76-136">For example:</span></span>

<span data-ttu-id="c6e76-137">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="c6e76-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6e76-138">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="c6e76-138">-VaultName</span></span>
<span data-ttu-id="c6e76-139">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="c6e76-139">Vault name.</span></span>
<span data-ttu-id="c6e76-140">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="c6e76-140">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="c6e76-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c6e76-141">-Confirm</span></span>
<span data-ttu-id="c6e76-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6e76-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6e76-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6e76-143">-WhatIf</span></span>
<span data-ttu-id="c6e76-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c6e76-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6e76-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c6e76-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6e76-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6e76-146">CommonParameters</span></span>
<span data-ttu-id="c6e76-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6e76-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6e76-148">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6e76-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6e76-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c6e76-149">INPUTS</span></span>

### <span data-ttu-id="c6e76-150">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c6e76-150">None</span></span>
<span data-ttu-id="c6e76-151">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="c6e76-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c6e76-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c6e76-152">OUTPUTS</span></span>

### <span data-ttu-id="c6e76-153">Microsoft. Azure. Commands. Vault. Models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c6e76-153">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="c6e76-154">Note</span><span class="sxs-lookup"><span data-stu-id="c6e76-154">NOTES</span></span>

## <span data-ttu-id="c6e76-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c6e76-155">RELATED LINKS</span></span>

[<span data-ttu-id="c6e76-156">AzureRM. Vault</span><span class="sxs-lookup"><span data-stu-id="c6e76-156">AzureRM.KeyVault</span></span>](/powershell/module/azurerm.keyvault)
