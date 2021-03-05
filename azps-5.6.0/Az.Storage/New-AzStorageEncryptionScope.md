---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageencryptionscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageEncryptionScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageEncryptionScope.md
ms.openlocfilehash: ab2750bff8ccc3f53761671455bc50fe3ec154d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002461"
---
# <span data-ttu-id="6a378-101">New-AzStorageEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="6a378-101">New-AzStorageEncryptionScope</span></span>

## <span data-ttu-id="6a378-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a378-102">SYNOPSIS</span></span>
<span data-ttu-id="6a378-103">Crea un ambito di crittografia per un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="6a378-103">Creates an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="6a378-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6a378-104">SYNTAX</span></span>

### <span data-ttu-id="6a378-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6a378-105">AccountName (Default)</span></span>
```
New-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-StorageEncryption] [-RequireInfrastructureEncryption]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a378-106">AccountNameKeyVault</span><span class="sxs-lookup"><span data-stu-id="6a378-106">AccountNameKeyVault</span></span>
```
New-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-KeyvaultEncryption] -KeyUri <String> [-RequireInfrastructureEncryption]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a378-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="6a378-107">AccountObject</span></span>
```
New-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-StorageEncryption] [-RequireInfrastructureEncryption] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a378-108">AccountObjectKeyVault</span><span class="sxs-lookup"><span data-stu-id="6a378-108">AccountObjectKeyVault</span></span>
```
New-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-KeyvaultEncryption] -KeyUri <String> [-RequireInfrastructureEncryption]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a378-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6a378-109">DESCRIPTION</span></span>
<span data-ttu-id="6a378-110">Il cmdlet **New-AzStorageEncryptionScope** crea un ambito di crittografia per un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="6a378-110">The **New-AzStorageEncryptionScope** cmdlet creates an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="6a378-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6a378-111">EXAMPLES</span></span>

### <span data-ttu-id="6a378-112">Esempio 1: Creare un ambito di crittografia con Crittografia di archiviazione</span><span class="sxs-lookup"><span data-stu-id="6a378-112">Example 1: Create an encryption scope with Storage Encryption</span></span>
```
PS C:\> New-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -StorageEncryption

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri RequireInfrastructureEncryption                                         
----      -----    ------            -------------- -------------------------------                                         
testscope Enabled  Microsoft.Storage
```

<span data-ttu-id="6a378-113">Questo comando crea un ambito di crittografia con Crittografia archiviazione.</span><span class="sxs-lookup"><span data-stu-id="6a378-113">This command creates an encryption scope with Storage Encryption.</span></span>

### <span data-ttu-id="6a378-114">Esempio 2: Creare un ambito di crittografia con crittografia Keyvault e RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="6a378-114">Example 2: Create an encryption scope with Keyvault Encryption, and RequireInfrastructureEncryption</span></span>
```
PS C:\> New-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" `
    -EncryptionScopeName testscope -KeyvaultEncryption -KeyUri "https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57" `
    -RequireInfrastructureEncryption 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name         State   Source           KeyVaultKeyUri                                                                          RequireInfrastructureEncryption                                       
----         -----   ------             --------------                                                                        -------------------------------                                     
testscope Enabled  Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57  True 
```

<span data-ttu-id="6a378-115">Questo comando crea un ambito di crittografia con Crittografia Keyvault e RequireInfrastructureEncryption.</span><span class="sxs-lookup"><span data-stu-id="6a378-115">This command creates an encryption scope with Keyvault Encryption and RequireInfrastructureEncryption.</span></span>
<span data-ttu-id="6a378-116">L'identità dell'account di archiviazione deve avere autorizzazioni get, wrapkey e unwrapkey per la chiave keyvault.</span><span class="sxs-lookup"><span data-stu-id="6a378-116">The Storage account Identity need have get,wrapkey,unwrapkey permissions to the keyvault key.</span></span>

## <span data-ttu-id="6a378-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a378-117">PARAMETERS</span></span>

### <span data-ttu-id="6a378-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a378-118">-DefaultProfile</span></span>
<span data-ttu-id="6a378-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6a378-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a378-120">-EncryptionScopeName</span><span class="sxs-lookup"><span data-stu-id="6a378-120">-EncryptionScopeName</span></span>
<span data-ttu-id="6a378-121">Nome Azure Storage EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="6a378-121">Azure Storage EncryptionScope name</span></span>

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

### <span data-ttu-id="6a378-122">-KeyUri</span><span class="sxs-lookup"><span data-stu-id="6a378-122">-KeyUri</span></span>
<span data-ttu-id="6a378-123">URI chiave</span><span class="sxs-lookup"><span data-stu-id="6a378-123">The key Uri</span></span>

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

### <span data-ttu-id="6a378-124">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="6a378-124">-KeyvaultEncryption</span></span>
<span data-ttu-id="6a378-125">Creare un ambito di crittografia con keySource come Microsoft.Keyvault</span><span class="sxs-lookup"><span data-stu-id="6a378-125">Create encryption scope with keySource as Microsoft.Keyvault</span></span>

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

### <span data-ttu-id="6a378-126">-RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="6a378-126">-RequireInfrastructureEncryption</span></span>
<span data-ttu-id="6a378-127">L'ambito di crittografia applicherà un livello secondario di crittografia con chiavi gestite della piattaforma per i dati in archivio.</span><span class="sxs-lookup"><span data-stu-id="6a378-127">The encryption scope will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>

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

### <span data-ttu-id="6a378-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a378-128">-ResourceGroupName</span></span>
<span data-ttu-id="6a378-129">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6a378-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="6a378-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="6a378-130">-StorageAccount</span></span>
<span data-ttu-id="6a378-131">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="6a378-131">Storage account object</span></span>

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

### <span data-ttu-id="6a378-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6a378-132">-StorageAccountName</span></span>
<span data-ttu-id="6a378-133">Nome account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="6a378-133">Storage Account Name.</span></span>

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

### <span data-ttu-id="6a378-134">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="6a378-134">-StorageEncryption</span></span>
<span data-ttu-id="6a378-135">Creare un ambito di crittografia con keySource come Microsoft.Storage.</span><span class="sxs-lookup"><span data-stu-id="6a378-135">Create encryption scope with keySource as Microsoft.Storage.</span></span>

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

### <span data-ttu-id="6a378-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6a378-136">-Confirm</span></span>
<span data-ttu-id="6a378-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a378-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a378-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a378-138">-WhatIf</span></span>
<span data-ttu-id="6a378-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6a378-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a378-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6a378-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a378-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a378-141">CommonParameters</span></span>
<span data-ttu-id="6a378-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a378-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a378-143">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a378-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a378-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="6a378-144">INPUTS</span></span>

### <span data-ttu-id="6a378-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6a378-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="6a378-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6a378-146">OUTPUTS</span></span>

### <span data-ttu-id="6a378-147">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="6a378-147">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span></span>

## <span data-ttu-id="6a378-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="6a378-148">NOTES</span></span>

## <span data-ttu-id="6a378-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6a378-149">RELATED LINKS</span></span>
