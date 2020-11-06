---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 84c6df195b0d24e5096748a4a5e3fd8360665831
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510564"
---
# <span data-ttu-id="9db34-101">Update-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9db34-101">Update-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="9db34-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9db34-102">SYNOPSIS</span></span>
<span data-ttu-id="9db34-103">Aggiornare gli attributi modificabili di un account di archiviazione di Azure Key Vault gestito.</span><span class="sxs-lookup"><span data-stu-id="9db34-103">Update editable attributes of a Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9db34-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9db34-104">SYNTAX</span></span>

```
Update-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-ActiveKeyName <String>] [-AutoRegenerateKey <Boolean>] [-RegenerationPeriod <TimeSpan>] [-Enable <Boolean>]
 [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9db34-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9db34-105">DESCRIPTION</span></span>
<span data-ttu-id="9db34-106">Aggiornare gli attributi modificabili di un account di archiviazione di Azure Key Vault gestito.</span><span class="sxs-lookup"><span data-stu-id="9db34-106">Update the editable attributes of a Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="9db34-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9db34-107">EXAMPLES</span></span>

### <span data-ttu-id="9db34-108">Esempio 1: aggiornare la chiave attiva in "key2" in un account di archiviazione di Azure con chiave archiviata Key.</span><span class="sxs-lookup"><span data-stu-id="9db34-108">Example 1:Update the active key to 'key2' on a Key Vault managed Azure Storage Account.</span></span>
```
PS C:\> Update-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -ActiveKeyName 'key2'
```

<span data-ttu-id="9db34-109">Aggiorna la chiave attiva dell'account di archiviazione di Azure Key Vault in "key2".</span><span class="sxs-lookup"><span data-stu-id="9db34-109">Updates the Key Vault managed Azure Storage Account active key to 'key2'.</span></span> <span data-ttu-id="9db34-110">"key2" verrà usato per generare token SAS dopo questo aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="9db34-110">'key2' will be used to generate SAS tokens after this update.</span></span>

## <span data-ttu-id="9db34-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9db34-111">PARAMETERS</span></span>

### <span data-ttu-id="9db34-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9db34-112">-AccountName</span></span>
<span data-ttu-id="9db34-113">Nome dell'account di archiviazione gestito Key Vault.</span><span class="sxs-lookup"><span data-stu-id="9db34-113">Key Vault managed storage account name.</span></span> <span data-ttu-id="9db34-114">Cmdlet crea l'FQDN di un nome di account di archiviazione gestito dal nome del Vault, dall'ambiente selezionato e dal nome dell'account di archiviazione modificato.</span><span class="sxs-lookup"><span data-stu-id="9db34-114">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9db34-115">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="9db34-115">-ActiveKeyName</span></span>
<span data-ttu-id="9db34-116">Nome chiave attiva.</span><span class="sxs-lookup"><span data-stu-id="9db34-116">Active key name.</span></span>
<span data-ttu-id="9db34-117">Se non specificato, il valore esistente del nome della chiave attiva dell'account di archiviazione gestito rimane invariato</span><span class="sxs-lookup"><span data-stu-id="9db34-117">If not specified, the existing value of managed storage account's active key name remains unchanged</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9db34-118">-AutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="9db34-118">-AutoRegenerateKey</span></span>
<span data-ttu-id="9db34-119">Chiave di rigenerazione automatica.</span><span class="sxs-lookup"><span data-stu-id="9db34-119">Auto regenerate key.</span></span>
<span data-ttu-id="9db34-120">Se non specificato, il valore esistente della chiave di rigenerazione automatica dell'account di archiviazione gestita rimane invariato</span><span class="sxs-lookup"><span data-stu-id="9db34-120">If not specified, the existing value of auto regenerate key of managed storage account remains unchanged</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9db34-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9db34-121">-Confirm</span></span>
<span data-ttu-id="9db34-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9db34-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9db34-123">-Enable</span><span class="sxs-lookup"><span data-stu-id="9db34-123">-Enable</span></span>
<span data-ttu-id="9db34-124">Se presente, Abilita l'uso di una chiave dell'account di archiviazione gestita per la generazione di token SAS se value è true.</span><span class="sxs-lookup"><span data-stu-id="9db34-124">If present, enables a use of a managed storage account key for sas token generation if value is true.</span></span> <span data-ttu-id="9db34-125">Disabilita l'uso di una chiave dell'account di archiviazione gestita per la generazione di token SAS se value è false.</span><span class="sxs-lookup"><span data-stu-id="9db34-125">Disables use of a managed storage account key for sas token generation if value is false.</span></span> <span data-ttu-id="9db34-126">Se non specificato, il valore esistente dello stato abilitato/disabilitato dell'account di archiviazione rimane invariato.</span><span class="sxs-lookup"><span data-stu-id="9db34-126">If not specified, the existing value of the storage account's enabled/disabled state remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9db34-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9db34-127">-PassThru</span></span>
<span data-ttu-id="9db34-128">Cmdlet non restituisce Object per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="9db34-128">Cmdlet does not return object by default.</span></span> <span data-ttu-id="9db34-129">Se questa opzione è specificata, restituire l'oggetto account di archiviazione gestita.</span><span class="sxs-lookup"><span data-stu-id="9db34-129">If this switch is specified, return managed storage account object.</span></span>

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

### <span data-ttu-id="9db34-130">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="9db34-130">-RegenerationPeriod</span></span>
<span data-ttu-id="9db34-131">Periodo di rigenerazione.</span><span class="sxs-lookup"><span data-stu-id="9db34-131">Regeneration period.</span></span> <span data-ttu-id="9db34-132">Se la chiave di rigenerazione automatica è abilitata, questo valore specifica l'intervallo di valori TimeSpan dopo il quale il tasto inattivo dell'account di archiviazione gestito viene rigenerato automaticamente e diventa la chiave attiva.</span><span class="sxs-lookup"><span data-stu-id="9db34-132">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the active key.</span></span> <span data-ttu-id="9db34-133">Se non specificato, il valore esistente del periodo di rigenerazione delle chiavi dell'account di archiviazione gestita rimane invariato</span><span class="sxs-lookup"><span data-stu-id="9db34-133">If not specified, the existing value of regeneration period of keys of managed storage account remains unchanged</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9db34-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="9db34-134">-Tag</span></span>
<span data-ttu-id="9db34-135">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="9db34-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9db34-136">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="9db34-136">For example:</span></span>

<span data-ttu-id="9db34-137">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="9db34-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9db34-138">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="9db34-138">-VaultName</span></span>
<span data-ttu-id="9db34-139">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="9db34-139">Vault name.</span></span>
<span data-ttu-id="9db34-140">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="9db34-140">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9db34-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9db34-141">-WhatIf</span></span>
<span data-ttu-id="9db34-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9db34-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9db34-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9db34-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9db34-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9db34-144">-DefaultProfile</span></span>
<span data-ttu-id="9db34-145">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9db34-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9db34-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9db34-146">CommonParameters</span></span>
<span data-ttu-id="9db34-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9db34-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9db34-148">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9db34-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9db34-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9db34-149">INPUTS</span></span>

## <span data-ttu-id="9db34-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9db34-150">OUTPUTS</span></span>

### <span data-ttu-id="9db34-151">Microsoft. Azure. Commands. Vault. Models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9db34-151">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="9db34-152">Note</span><span class="sxs-lookup"><span data-stu-id="9db34-152">NOTES</span></span>

## <span data-ttu-id="9db34-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9db34-153">RELATED LINKS</span></span>

[<span data-ttu-id="9db34-154">AzureRM. Vault</span><span class="sxs-lookup"><span data-stu-id="9db34-154">AzureRM.KeyVault</span></span>](/powershell/module/azurerm.keyvault)
