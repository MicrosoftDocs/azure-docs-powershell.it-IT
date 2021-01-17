---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageencryptionscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageEncryptionScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageEncryptionScope.md
ms.openlocfilehash: 011bdd96d69ae73ca62145b85f6e636751f8eb9f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474678"
---
# <span data-ttu-id="67219-101">New-AzStorageEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="67219-101">New-AzStorageEncryptionScope</span></span>

## <span data-ttu-id="67219-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="67219-102">SYNOPSIS</span></span>
<span data-ttu-id="67219-103">Crea un ambito di crittografia per un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="67219-103">Creates an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="67219-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="67219-104">SYNTAX</span></span>

### <span data-ttu-id="67219-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="67219-105">AccountName (Default)</span></span>
```
New-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-StorageEncryption] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67219-106">AccountNameKeyVault</span><span class="sxs-lookup"><span data-stu-id="67219-106">AccountNameKeyVault</span></span>
```
New-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-KeyvaultEncryption] -KeyUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67219-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="67219-107">AccountObject</span></span>
```
New-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-StorageEncryption] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67219-108">AccountObjectKeyVault</span><span class="sxs-lookup"><span data-stu-id="67219-108">AccountObjectKeyVault</span></span>
```
New-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-KeyvaultEncryption] -KeyUri <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="67219-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="67219-109">DESCRIPTION</span></span>
<span data-ttu-id="67219-110">Il cmdlet **New-AzStorageEncryptionScope** crea un ambito di crittografia per un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="67219-110">The **New-AzStorageEncryptionScope** cmdlet creates an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="67219-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="67219-111">EXAMPLES</span></span>

### <span data-ttu-id="67219-112">Esempio 1: creare un ambito di crittografia con la crittografia dello spazio di archiviazione</span><span class="sxs-lookup"><span data-stu-id="67219-112">Example 1: Create an encryption scope with Storage Encryption</span></span>
```
PS C:\> New-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -StorageEncryption

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri                                         
----      -----    ------            --------------                                         
testscope Enabled  Microsoft.Storage
```

<span data-ttu-id="67219-113">Questo comando crea un ambito di crittografia con crittografia dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="67219-113">This command creates an encryption scope with Storage Encryption.</span></span>

### <span data-ttu-id="67219-114">Esempio 2: creare un ambito di crittografia con la crittografia di un Vault</span><span class="sxs-lookup"><span data-stu-id="67219-114">Example 2: Create an encryption scope with Keyvault Encryption</span></span>
```
PS C:\> New-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EncryptionScopeName testscope -KeyvaultEncryption -KeyUri "https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                         
----      -----    ------             --------------                                         
testscope Enabled  Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57
```

<span data-ttu-id="67219-115">Questo comando crea un ambito di crittografia con la crittografia di un Vault.</span><span class="sxs-lookup"><span data-stu-id="67219-115">This command creates an encryption scope with Keyvault Encryption.</span></span>
<span data-ttu-id="67219-116">L'identità dell'account di archiviazione deve avere le autorizzazioni Get, wrapkey, unwrapkey per la chiave del Vault.</span><span class="sxs-lookup"><span data-stu-id="67219-116">The Storage account Identity need have get,wrapkey,unwrapkey permissions to the keyvault key.</span></span>

## <span data-ttu-id="67219-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="67219-117">PARAMETERS</span></span>

### <span data-ttu-id="67219-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67219-118">-DefaultProfile</span></span>
<span data-ttu-id="67219-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="67219-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67219-120">-EncryptionScopeName</span><span class="sxs-lookup"><span data-stu-id="67219-120">-EncryptionScopeName</span></span>
<span data-ttu-id="67219-121">Nome EncryptionScope di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="67219-121">Azure Storage EncryptionScope name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67219-122">-KeyUri</span><span class="sxs-lookup"><span data-stu-id="67219-122">-KeyUri</span></span>
<span data-ttu-id="67219-123">URI chiave</span><span class="sxs-lookup"><span data-stu-id="67219-123">The key Uri</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameKeyVault, AccountObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67219-124">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="67219-124">-KeyvaultEncryption</span></span>
<span data-ttu-id="67219-125">Creare un ambito di crittografia con la sorgente di origine come Microsoft. Vault</span><span class="sxs-lookup"><span data-stu-id="67219-125">Create encryption scope with keySource as Microsoft.Keyvault</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountNameKeyVault, AccountObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67219-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67219-126">-ResourceGroupName</span></span>
<span data-ttu-id="67219-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="67219-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="67219-128">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="67219-128">-StorageAccount</span></span>
<span data-ttu-id="67219-129">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="67219-129">Storage account object</span></span>

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

### <span data-ttu-id="67219-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="67219-130">-StorageAccountName</span></span>
<span data-ttu-id="67219-131">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="67219-131">Storage Account Name.</span></span>

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

### <span data-ttu-id="67219-132">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="67219-132">-StorageEncryption</span></span>
<span data-ttu-id="67219-133">Creare l'ambito di crittografia con la fonte di risorse come Microsoft. storage.</span><span class="sxs-lookup"><span data-stu-id="67219-133">Create encryption scope with keySource as Microsoft.Storage.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountName, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67219-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="67219-134">-Confirm</span></span>
<span data-ttu-id="67219-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67219-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67219-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67219-136">-WhatIf</span></span>
<span data-ttu-id="67219-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="67219-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67219-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="67219-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67219-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67219-139">CommonParameters</span></span>
<span data-ttu-id="67219-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67219-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67219-141">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67219-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67219-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="67219-142">INPUTS</span></span>

### <span data-ttu-id="67219-143">Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="67219-143">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="67219-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="67219-144">OUTPUTS</span></span>

### <span data-ttu-id="67219-145">Microsoft. Azure. Commands. Management. storage. Models. PSEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="67219-145">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span></span>

## <span data-ttu-id="67219-146">Note</span><span class="sxs-lookup"><span data-stu-id="67219-146">NOTES</span></span>

## <span data-ttu-id="67219-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="67219-147">RELATED LINKS</span></span>
