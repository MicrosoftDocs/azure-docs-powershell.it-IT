---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 183618058d6400798dc2af74975fd45a0a397b16
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674082"
---
# <span data-ttu-id="0b2c2-101">Update-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0b2c2-101">Update-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="0b2c2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0b2c2-102">SYNOPSIS</span></span>
<span data-ttu-id="0b2c2-103">Aggiornare gli attributi modificabili di un account di archiviazione di Azure Key Vault gestito.</span><span class="sxs-lookup"><span data-stu-id="0b2c2-103">Update editable attributes of a Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="0b2c2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0b2c2-104">SYNTAX</span></span>

### <span data-ttu-id="0b2c2-105">ByDefinitionName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0b2c2-105">ByDefinitionName (Default)</span></span>
```
Update-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-ActiveKeyName <String>]
 [-AutoRegenerateKey <Boolean>] [-RegenerationPeriod <TimeSpan>] [-Enable <Boolean>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b2c2-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0b2c2-106">ByInputObject</span></span>
```
Update-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-ActiveKeyName <String>] [-AutoRegenerateKey <Boolean>] [-RegenerationPeriod <TimeSpan>] [-Enable <Boolean>]
 [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0b2c2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b2c2-107">DESCRIPTION</span></span>
<span data-ttu-id="0b2c2-108">Aggiornare gli attributi modificabili di un account di archiviazione di Azure Key Vault gestito.</span><span class="sxs-lookup"><span data-stu-id="0b2c2-108">Update the editable attributes of a Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="0b2c2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0b2c2-109">EXAMPLES</span></span>

### <span data-ttu-id="0b2c2-110">Esempio 1: aggiornare la chiave attiva in "key2" in un account di archiviazione di Azure con chiave archiviata Key.</span><span class="sxs-lookup"><span data-stu-id="0b2c2-110">Example 1: Update the active key to 'key2' on a Key Vault managed Azure Storage Account.</span></span>
```powershell
PS C:\> Update-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -ActiveKeyName 'key2'

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key2
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="0b2c2-111">Aggiorna la chiave attiva dell'account di archiviazione di Azure Key Vault in "key2".</span><span class="sxs-lookup"><span data-stu-id="0b2c2-111">Updates the Key Vault managed Azure Storage Account active key to 'key2'.</span></span> <span data-ttu-id="0b2c2-112">"key2" verrà usato per generare token SAS dopo questo aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="0b2c2-112">'key2' will be used to generate SAS tokens after this update.</span></span>

## <span data-ttu-id="0b2c2-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0b2c2-113">PARAMETERS</span></span>

### <span data-ttu-id="0b2c2-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0b2c2-114">-AccountName</span></span>
<span data-ttu-id="0b2c2-115">Nome dell'account di archiviazione gestito Key Vault.</span><span class="sxs-lookup"><span data-stu-id="0b2c2-115">Key Vault managed storage account name.</span></span> <span data-ttu-id="0b2c2-116">Cmdlet crea l'FQDN di un nome di account di archiviazione gestito dal nome del Vault, dall'ambiente selezionato e dal nome dell'account di archiviazione modificato.</span><span class="sxs-lookup"><span data-stu-id="0b2c2-116">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b2c2-117">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="0b2c2-117">-ActiveKeyName</span></span>
<span data-ttu-id="0b2c2-118">Nome chiave attiva.</span><span class="sxs-lookup"><span data-stu-id="0b2c2-118">Active key name.</span></span>
<span data-ttu-id="0b2c2-119">Se non specificato, il valore esistente del nome della chiave attiva dell'account di archiviazione gestito rimane invariato</span><span class="sxs-lookup"><span data-stu-id="0b2c2-119">If not specified, the existing value of managed storage account's active key name remains unchanged</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b2c2-120">-AutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="0b2c2-120">-AutoRegenerateKey</span></span>
<span data-ttu-id="0b2c2-121">Chiave di rigenerazione automatica.</span><span class="sxs-lookup"><span data-stu-id="0b2c2-121">Auto regenerate key.</span></span>
<span data-ttu-id="0b2c2-122">Se non specificato, il valore esistente della chiave di rigenerazione automatica dell'account di archiviazione gestita rimane invariato</span><span class="sxs-lookup"><span data-stu-id="0b2c2-122">If not specified, the existing value of auto regenerate key of managed storage account remains unchanged</span></span>

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

### <span data-ttu-id="0b2c2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b2c2-123">-DefaultProfile</span></span>
<span data-ttu-id="0b2c2-124">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0b2c2-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b2c2-125">-Enable</span><span class="sxs-lookup"><span data-stu-id="0b2c2-125">-Enable</span></span>
<span data-ttu-id="0b2c2-126">Se presente, Abilita l'uso di una chiave dell'account di archiviazione gestita per la generazione di token SAS se value è true.</span><span class="sxs-lookup"><span data-stu-id="0b2c2-126">If present, enables a use of a managed storage account key for sas token generation if value is true.</span></span> <span data-ttu-id="0b2c2-127">Disabilita l'uso di una chiave dell'account di archiviazione gestita per la generazione di token SAS se value è false.</span><span class="sxs-lookup"><span data-stu-id="0b2c2-127">Disables use of a managed storage account key for sas token generation if value is false.</span></span> <span data-ttu-id="0b2c2-128">Se non specificato, il valore esistente dello stato abilitato/disabilitato dell'account di archiviazione rimane invariato.</span><span class="sxs-lookup"><span data-stu-id="0b2c2-128">If not specified, the existing value of the storage account's enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="0b2c2-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0b2c2-129">-InputObject</span></span>
<span data-ttu-id="0b2c2-130">Oggetto ManagedStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="0b2c2-130">ManagedStorageAccount object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b2c2-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0b2c2-131">-PassThru</span></span>
<span data-ttu-id="0b2c2-132">Cmdlet non restituisce Object per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="0b2c2-132">Cmdlet does not return object by default.</span></span> <span data-ttu-id="0b2c2-133">Se questa opzione è specificata, restituire l'oggetto account di archiviazione gestita.</span><span class="sxs-lookup"><span data-stu-id="0b2c2-133">If this switch is specified, return managed storage account object.</span></span>

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

### <span data-ttu-id="0b2c2-134">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="0b2c2-134">-RegenerationPeriod</span></span>
<span data-ttu-id="0b2c2-135">Periodo di rigenerazione.</span><span class="sxs-lookup"><span data-stu-id="0b2c2-135">Regeneration period.</span></span> <span data-ttu-id="0b2c2-136">Se la chiave di rigenerazione automatica è abilitata, questo valore specifica l'intervallo di valori TimeSpan dopo il quale il tasto inattivo dell'account di archiviazione gestito viene rigenerato automaticamente e diventa la chiave attiva.</span><span class="sxs-lookup"><span data-stu-id="0b2c2-136">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the active key.</span></span> <span data-ttu-id="0b2c2-137">Se non specificato, il valore esistente del periodo di rigenerazione delle chiavi dell'account di archiviazione gestita rimane invariato</span><span class="sxs-lookup"><span data-stu-id="0b2c2-137">If not specified, the existing value of regeneration period of keys of managed storage account remains unchanged</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b2c2-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="0b2c2-138">-Tag</span></span>
<span data-ttu-id="0b2c2-139">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="0b2c2-139">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0b2c2-140">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="0b2c2-140">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b2c2-141">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="0b2c2-141">-VaultName</span></span>
<span data-ttu-id="0b2c2-142">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="0b2c2-142">Vault name.</span></span>
<span data-ttu-id="0b2c2-143">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="0b2c2-143">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b2c2-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0b2c2-144">-Confirm</span></span>
<span data-ttu-id="0b2c2-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b2c2-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b2c2-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b2c2-146">-WhatIf</span></span>
<span data-ttu-id="0b2c2-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0b2c2-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b2c2-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0b2c2-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b2c2-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b2c2-149">CommonParameters</span></span>
<span data-ttu-id="0b2c2-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b2c2-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b2c2-151">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b2c2-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b2c2-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0b2c2-152">INPUTS</span></span>

### <span data-ttu-id="0b2c2-153">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="0b2c2-153">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="0b2c2-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0b2c2-154">OUTPUTS</span></span>

### <span data-ttu-id="0b2c2-155">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0b2c2-155">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="0b2c2-156">Note</span><span class="sxs-lookup"><span data-stu-id="0b2c2-156">NOTES</span></span>

## <span data-ttu-id="0b2c2-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0b2c2-157">RELATED LINKS</span></span>

[<span data-ttu-id="0b2c2-158">AZ. Vault</span><span class="sxs-lookup"><span data-stu-id="0b2c2-158">Az.KeyVault</span></span>](/powershell/module/az.keyvault)
