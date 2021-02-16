---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 72d23725f537df4f3e2244e799437394496bf434
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185375"
---
# <span data-ttu-id="78581-101">Update-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="78581-101">Update-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="78581-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78581-102">SYNOPSIS</span></span>
<span data-ttu-id="78581-103">Aggiornare gli attributi modificabili di un account di archiviazione di Azure gestito da Vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="78581-103">Update editable attributes of a Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="78581-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="78581-104">SYNTAX</span></span>

### <span data-ttu-id="78581-105">ByDefinitionName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="78581-105">ByDefinitionName (Default)</span></span>
```
Update-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-ActiveKeyName <String>]
 [-AutoRegenerateKey <Boolean>] [-RegenerationPeriod <TimeSpan>] [-Enable <Boolean>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78581-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="78581-106">ByInputObject</span></span>
```
Update-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-ActiveKeyName <String>] [-AutoRegenerateKey <Boolean>] [-RegenerationPeriod <TimeSpan>] [-Enable <Boolean>]
 [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="78581-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="78581-107">DESCRIPTION</span></span>
<span data-ttu-id="78581-108">Aggiornare gli attributi modificabili di un account di archiviazione di Azure gestito da Vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="78581-108">Update the editable attributes of a Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="78581-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="78581-109">EXAMPLES</span></span>

### <span data-ttu-id="78581-110">Esempio 1: Aggiornare la chiave attiva a "chiave2" in un account di archiviazione di Azure gestito da Vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="78581-110">Example 1: Update the active key to 'key2' on a Key Vault managed Azure Storage Account.</span></span>
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

<span data-ttu-id="78581-111">Aggiorna la chiave attiva dell'account di archiviazione di Azure gestita da Vault della chiave a "chiave2".</span><span class="sxs-lookup"><span data-stu-id="78581-111">Updates the Key Vault managed Azure Storage Account active key to 'key2'.</span></span> <span data-ttu-id="78581-112">'key2' verrà usato per generare token di firma di accesso condiviso dopo questo aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="78581-112">'key2' will be used to generate SAS tokens after this update.</span></span>

### <span data-ttu-id="78581-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="78581-113">Example 2</span></span>

<span data-ttu-id="78581-114">Aggiornare gli attributi modificabili di un account di archiviazione di Azure gestito da Vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="78581-114">Update editable attributes of a Key Vault managed Azure Storage Account.</span></span> <span data-ttu-id="78581-115">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="78581-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Update-AzKeyVaultManagedStorageAccount -AccountName 'mystorageaccount' -AutoRegenerateKey $false -RegenerationPeriod $regenerationPeriod -VaultName 'myvault'
```

## <span data-ttu-id="78581-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78581-116">PARAMETERS</span></span>

### <span data-ttu-id="78581-117">-AccountName</span><span class="sxs-lookup"><span data-stu-id="78581-117">-AccountName</span></span>
<span data-ttu-id="78581-118">Nome dell'account di archiviazione gestito dal Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="78581-118">Key Vault managed storage account name.</span></span> <span data-ttu-id="78581-119">Il cmdlet crea l'FQDN di un account di archiviazione gestito dal nome del vault, dall'ambiente attualmente selezionato e dal nome dell'account di archiviazione gestito.</span><span class="sxs-lookup"><span data-stu-id="78581-119">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="78581-120">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="78581-120">-ActiveKeyName</span></span>
<span data-ttu-id="78581-121">Nome della chiave attiva.</span><span class="sxs-lookup"><span data-stu-id="78581-121">Active key name.</span></span>
<span data-ttu-id="78581-122">Se non viene specificato, il valore esistente del nome della chiave attiva dell'account di archiviazione gestito rimane invariato</span><span class="sxs-lookup"><span data-stu-id="78581-122">If not specified, the existing value of managed storage account's active key name remains unchanged</span></span>

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

### <span data-ttu-id="78581-123">-AutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="78581-123">-AutoRegenerateKey</span></span>
<span data-ttu-id="78581-124">Chiave di rigenerazione automatica.</span><span class="sxs-lookup"><span data-stu-id="78581-124">Auto regenerate key.</span></span>
<span data-ttu-id="78581-125">Se non viene specificato, il valore esistente della chiave di rigenerazione automatica dell'account di archiviazione gestita rimane invariato</span><span class="sxs-lookup"><span data-stu-id="78581-125">If not specified, the existing value of auto regenerate key of managed storage account remains unchanged</span></span>

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

### <span data-ttu-id="78581-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78581-126">-DefaultProfile</span></span>
<span data-ttu-id="78581-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="78581-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78581-128">-Enable</span><span class="sxs-lookup"><span data-stu-id="78581-128">-Enable</span></span>
<span data-ttu-id="78581-129">Se presente, consente l'uso di una chiave dell'account di archiviazione gestita per la generazione di token sas se il valore è vero.</span><span class="sxs-lookup"><span data-stu-id="78581-129">If present, enables a use of a managed storage account key for sas token generation if value is true.</span></span> <span data-ttu-id="78581-130">Disabilita l'uso di una chiave dell'account di archiviazione gestita per la generazione di token sas se il valore è false.</span><span class="sxs-lookup"><span data-stu-id="78581-130">Disables use of a managed storage account key for sas token generation if value is false.</span></span> <span data-ttu-id="78581-131">Se non viene specificato, il valore esistente dello stato abilitato/disabilitato dell'account di archiviazione rimane invariato.</span><span class="sxs-lookup"><span data-stu-id="78581-131">If not specified, the existing value of the storage account's enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="78581-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78581-132">-InputObject</span></span>
<span data-ttu-id="78581-133">Oggetto ManagedStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="78581-133">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="78581-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="78581-134">-PassThru</span></span>
<span data-ttu-id="78581-135">Il cmdlet non restituisce l'oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="78581-135">Cmdlet does not return object by default.</span></span> <span data-ttu-id="78581-136">Se questa opzione è specificata, restituire l'oggetto account di archiviazione gestito.</span><span class="sxs-lookup"><span data-stu-id="78581-136">If this switch is specified, return managed storage account object.</span></span>

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

### <span data-ttu-id="78581-137">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="78581-137">-RegenerationPeriod</span></span>
<span data-ttu-id="78581-138">Periodo di rigenerazione.</span><span class="sxs-lookup"><span data-stu-id="78581-138">Regeneration period.</span></span> <span data-ttu-id="78581-139">Se la chiave di rigenerazione automatica è abilitata, questo valore specifica l'intervallo di tempo dopo il quale le chiavi inattive dell'account di archiviazione gestito vengono rigenerate automaticamente e diventano la chiave attiva.</span><span class="sxs-lookup"><span data-stu-id="78581-139">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the active key.</span></span> <span data-ttu-id="78581-140">Se non viene specificato, il valore esistente del periodo di rigenerazione delle chiavi dell'account di archiviazione gestita rimane invariato</span><span class="sxs-lookup"><span data-stu-id="78581-140">If not specified, the existing value of regeneration period of keys of managed storage account remains unchanged</span></span>

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

### <span data-ttu-id="78581-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="78581-141">-Tag</span></span>
<span data-ttu-id="78581-142">Coppie chiave-valore sotto forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="78581-142">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="78581-143">Ad esempio: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="78581-143">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="78581-144">-VaultName</span><span class="sxs-lookup"><span data-stu-id="78581-144">-VaultName</span></span>
<span data-ttu-id="78581-145">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="78581-145">Vault name.</span></span>
<span data-ttu-id="78581-146">Il cmdlet crea l'FQDN di un vault in base al nome e all'ambiente attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="78581-146">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="78581-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="78581-147">-Confirm</span></span>
<span data-ttu-id="78581-148">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78581-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78581-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78581-149">-WhatIf</span></span>
<span data-ttu-id="78581-150">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="78581-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78581-151">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="78581-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78581-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78581-152">CommonParameters</span></span>
<span data-ttu-id="78581-153">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78581-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78581-154">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="78581-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78581-155">INPUT</span><span class="sxs-lookup"><span data-stu-id="78581-155">INPUTS</span></span>

### <span data-ttu-id="78581-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="78581-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="78581-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="78581-157">OUTPUTS</span></span>

### <span data-ttu-id="78581-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="78581-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="78581-159">NOTE</span><span class="sxs-lookup"><span data-stu-id="78581-159">NOTES</span></span>

## <span data-ttu-id="78581-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="78581-160">RELATED LINKS</span></span>

[<span data-ttu-id="78581-161">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="78581-161">Az.KeyVault</span></span>](/powershell/module/az.keyvault)
