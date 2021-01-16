---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageencryptionscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageEncryptionScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageEncryptionScope.md
ms.openlocfilehash: 6c8f07cbdb70b84d235afa7ce953da0bac477f55
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375952"
---
# <span data-ttu-id="3ce08-101">Update-AzStorageEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="3ce08-101">Update-AzStorageEncryptionScope</span></span>

## <span data-ttu-id="3ce08-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3ce08-102">SYNOPSIS</span></span>
<span data-ttu-id="3ce08-103">Modificare un ambito di crittografia per un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3ce08-103">Modify an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="3ce08-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3ce08-104">SYNTAX</span></span>

### <span data-ttu-id="3ce08-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3ce08-105">AccountName (Default)</span></span>
```
Update-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-StorageEncryption] [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ce08-106">AccountNameKeyVault</span><span class="sxs-lookup"><span data-stu-id="3ce08-106">AccountNameKeyVault</span></span>
```
Update-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-KeyvaultEncryption] -KeyUri <String> [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ce08-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="3ce08-107">AccountObject</span></span>
```
Update-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-StorageEncryption] [-State <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3ce08-108">AccountObjectKeyVault</span><span class="sxs-lookup"><span data-stu-id="3ce08-108">AccountObjectKeyVault</span></span>
```
Update-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-KeyvaultEncryption] -KeyUri <String> [-State <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ce08-109">EncryptionScopeObject</span><span class="sxs-lookup"><span data-stu-id="3ce08-109">EncryptionScopeObject</span></span>
```
Update-AzStorageEncryptionScope -InputObject <PSEncryptionScope> [-StorageEncryption] [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ce08-110">EncryptionScopeObjectKeyVault</span><span class="sxs-lookup"><span data-stu-id="3ce08-110">EncryptionScopeObjectKeyVault</span></span>
```
Update-AzStorageEncryptionScope -InputObject <PSEncryptionScope> [-KeyvaultEncryption] -KeyUri <String>
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ce08-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ce08-111">DESCRIPTION</span></span>
<span data-ttu-id="3ce08-112">Il cmdlet **Update-AzStorageEncryptionScope** modifica un ambito di crittografia per un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3ce08-112">The **Update-AzStorageEncryptionScope** cmdlet modifies an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="3ce08-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3ce08-113">EXAMPLES</span></span>

### <span data-ttu-id="3ce08-114">Esempio 1: disabilitare un ambito di crittografia</span><span class="sxs-lookup"><span data-stu-id="3ce08-114">Example 1: Disable an encryption scope</span></span>
```
PS C:\> Update-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -State Disabled 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri                                                                          
----      -----    ------            --------------                                                                          
testscope Disabled Microsoft.Storage
```

<span data-ttu-id="3ce08-115">Questo comando Disabilita un ambito di crittografia.</span><span class="sxs-lookup"><span data-stu-id="3ce08-115">This command disables an encryption scope.</span></span>

### <span data-ttu-id="3ce08-116">Esempio 2: abilitare un ambito di crittografia</span><span class="sxs-lookup"><span data-stu-id="3ce08-116">Example 2: Enable an encryption scope</span></span>
```
PS C:\> Update-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -State Enabled 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri                                                                          
----      -----    ------            --------------                                                                          
testscope Enabled  Microsoft.Storage
```

<span data-ttu-id="3ce08-117">Questo comando consente di abilitare un ambito di crittografia.</span><span class="sxs-lookup"><span data-stu-id="3ce08-117">This command enables an encryption scope.</span></span>

### <span data-ttu-id="3ce08-118">Esempio 3: aggiornare un ambito di crittografia per usare la crittografia dello spazio di archiviazione</span><span class="sxs-lookup"><span data-stu-id="3ce08-118">Example 3: Update an encryption scope to use Storage Encryption</span></span>
```
PS C:\> Update-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -StorageEncryption

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri                                         
----      -----    ------            --------------                                         
testscope Enabled  Microsoft.Storage
```

<span data-ttu-id="3ce08-119">Questo comando aggiorna un ambito di crittografia per l'uso della crittografia dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3ce08-119">This command updates an encryption scope to use Storage Encryption.</span></span>

### <span data-ttu-id="3ce08-120">Esempio 4: aggiornare un ambito di crittografia per l'uso della crittografia con il Vault</span><span class="sxs-lookup"><span data-stu-id="3ce08-120">Example 4: Update an encryption scope to use Keyvault Encryption</span></span>
```
PS C:\> Update-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EncryptionScopeName testscope -KeyvaultEncryption -KeyUri "https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                         
----      -----    ------             --------------                                         
testscope Enabled  Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57
```

<span data-ttu-id="3ce08-121">Questo comando updtaes un ambito di crittografia per l'uso della crittografia con il Vault.</span><span class="sxs-lookup"><span data-stu-id="3ce08-121">This command updtaes an encryption scope to use Keyvault Encryption.</span></span>
<span data-ttu-id="3ce08-122">L'identità dell'account di archiviazione deve avere le autorizzazioni Get, wrapkey, unwrapkey per la chiave del Vault.</span><span class="sxs-lookup"><span data-stu-id="3ce08-122">The Storage account Identity need have get,wrapkey,unwrapkey permissions to the keyvault key.</span></span>

## <span data-ttu-id="3ce08-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3ce08-123">PARAMETERS</span></span>

### <span data-ttu-id="3ce08-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ce08-124">-DefaultProfile</span></span>
<span data-ttu-id="3ce08-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3ce08-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ce08-126">-EncryptionScopeName</span><span class="sxs-lookup"><span data-stu-id="3ce08-126">-EncryptionScopeName</span></span>
<span data-ttu-id="3ce08-127">Nome EncryptionScope di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="3ce08-127">Azure Storage EncryptionScope name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameKeyVault, AccountObject, AccountObjectKeyVault
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce08-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ce08-128">-InputObject</span></span>
<span data-ttu-id="3ce08-129">Oggetto EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="3ce08-129">EncryptionScope object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope
Parameter Sets: EncryptionScopeObject, EncryptionScopeObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ce08-130">-KeyUri</span><span class="sxs-lookup"><span data-stu-id="3ce08-130">-KeyUri</span></span>
<span data-ttu-id="3ce08-131">URI chiave</span><span class="sxs-lookup"><span data-stu-id="3ce08-131">The key Uri</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameKeyVault, AccountObjectKeyVault, EncryptionScopeObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce08-132">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="3ce08-132">-KeyvaultEncryption</span></span>
<span data-ttu-id="3ce08-133">Creare un ambito di crittografia con la sorgente di origine come Microsoft. Vault</span><span class="sxs-lookup"><span data-stu-id="3ce08-133">Create encryption scope with keySource as Microsoft.Keyvault</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountNameKeyVault, AccountObjectKeyVault, EncryptionScopeObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce08-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ce08-134">-ResourceGroupName</span></span>
<span data-ttu-id="3ce08-135">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3ce08-135">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameKeyVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce08-136">-Stato</span><span class="sxs-lookup"><span data-stu-id="3ce08-136">-State</span></span>
<span data-ttu-id="3ce08-137">Aggiornare lo stato dell'ambito di crittografia, i possibili valori includono:' Enabled ',' disabled '.</span><span class="sxs-lookup"><span data-stu-id="3ce08-137">Update encryption scope State, Possible values include: 'Enabled', 'Disabled'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce08-138">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="3ce08-138">-StorageAccount</span></span>
<span data-ttu-id="3ce08-139">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="3ce08-139">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject, AccountObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ce08-140">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3ce08-140">-StorageAccountName</span></span>
<span data-ttu-id="3ce08-141">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3ce08-141">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameKeyVault
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce08-142">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="3ce08-142">-StorageEncryption</span></span>
<span data-ttu-id="3ce08-143">Creare l'ambito di crittografia con la fonte di risorse come Microsoft. storage.</span><span class="sxs-lookup"><span data-stu-id="3ce08-143">Create encryption scope with keySource as Microsoft.Storage.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountName, AccountObject, EncryptionScopeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ce08-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3ce08-144">-Confirm</span></span>
<span data-ttu-id="3ce08-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ce08-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ce08-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ce08-146">-WhatIf</span></span>
<span data-ttu-id="3ce08-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3ce08-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ce08-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3ce08-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ce08-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ce08-149">CommonParameters</span></span>
<span data-ttu-id="3ce08-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ce08-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ce08-151">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ce08-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ce08-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3ce08-152">INPUTS</span></span>

### <span data-ttu-id="3ce08-153">Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3ce08-153">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="3ce08-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3ce08-154">OUTPUTS</span></span>

### <span data-ttu-id="3ce08-155">Microsoft. Azure. Commands. Management. storage. Models. PSEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="3ce08-155">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span></span>

## <span data-ttu-id="3ce08-156">Note</span><span class="sxs-lookup"><span data-stu-id="3ce08-156">NOTES</span></span>

## <span data-ttu-id="3ce08-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3ce08-157">RELATED LINKS</span></span>
