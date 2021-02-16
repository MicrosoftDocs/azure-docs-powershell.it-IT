---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultmanagedstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccountKey.md
ms.openlocfilehash: b603cff68d2343a683718ca53e900aa5b667dc14
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185374"
---
# <span data-ttu-id="d3d3c-101">Update-AzKeyVaultManagedStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d3d3c-101">Update-AzKeyVaultManagedStorageAccountKey</span></span>

## <span data-ttu-id="d3d3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3d3c-102">SYNOPSIS</span></span>
<span data-ttu-id="d3d3c-103">Rigenera la chiave specificata dell'account di archiviazione di Azure gestito da Vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="d3d3c-103">Regenerates the specified key of Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="d3d3c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d3d3c-104">SYNTAX</span></span>

### <span data-ttu-id="d3d3c-105">ByDefinitionName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d3d3c-105">ByDefinitionName (Default)</span></span>
```
Update-AzKeyVaultManagedStorageAccountKey [-VaultName] <String> [-AccountName] <String> [-KeyName] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3d3c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d3d3c-106">ByInputObject</span></span>
```
Update-AzKeyVaultManagedStorageAccountKey [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-KeyName] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d3d3c-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d3d3c-107">DESCRIPTION</span></span>
<span data-ttu-id="d3d3c-108">Rigenera la chiave specificata dell'account di archiviazione di Azure gestito da Vault e la imposta come chiave attiva.</span><span class="sxs-lookup"><span data-stu-id="d3d3c-108">Regenerates the specified key of Key Vault managed Azure Storage Account and sets the key as the active key.</span></span> <span data-ttu-id="d3d3c-109">Il Vault chiave proxy la chiamata a Gestione risorse di Azure per rigenerare la chiave.</span><span class="sxs-lookup"><span data-stu-id="d3d3c-109">Key Vault proxies the call to Azure Resource Manager to regenerate the key.</span></span> <span data-ttu-id="d3d3c-110">Il chiamante deve avere le autorizzazioni per rigenerare le chiavi in un dato account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d3d3c-110">The caller must posses permissions to regenerate keys on given Azure Storage Account.</span></span>

## <span data-ttu-id="d3d3c-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d3d3c-111">EXAMPLES</span></span>

### <span data-ttu-id="d3d3c-112">Esempio 1: Rigenerare una chiave</span><span class="sxs-lookup"><span data-stu-id="d3d3c-112">Example 1: Regenerate a key</span></span>
```powershell
PS C:\> Update-AzKeyVaultManagedStorageAccountKey -VaultName 'myvault' -AccountName 'mystorageaccount' -KeyName 'key1'

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key1
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="d3d3c-113">Rigenera 'key1' dell'account 'mystorageaccount' e imposta 'key1' come attivo dell'account di archiviazione di Azure gestito dal Vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="d3d3c-113">Regenerates 'key1' of account 'mystorageaccount' and sets 'key1' as the active of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="d3d3c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3d3c-114">PARAMETERS</span></span>

### <span data-ttu-id="d3d3c-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d3d3c-115">-AccountName</span></span>
<span data-ttu-id="d3d3c-116">Nome dell'account di archiviazione gestito dal Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="d3d3c-116">Key Vault managed storage account name.</span></span> <span data-ttu-id="d3d3c-117">Il cmdlet crea l'FQDN di un account di archiviazione gestito dal nome del vault, dall'ambiente attualmente selezionato e dal nome dell'account di archiviazione gestito.</span><span class="sxs-lookup"><span data-stu-id="d3d3c-117">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="d3d3c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3d3c-118">-DefaultProfile</span></span>
<span data-ttu-id="d3d3c-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="d3d3c-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d3d3c-120">-Force</span><span class="sxs-lookup"><span data-stu-id="d3d3c-120">-Force</span></span>
<span data-ttu-id="d3d3c-121">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="d3d3c-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d3d3c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3d3c-122">-InputObject</span></span>
<span data-ttu-id="d3d3c-123">Oggetto ManagedStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="d3d3c-123">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="d3d3c-124">-KeyName</span><span class="sxs-lookup"><span data-stu-id="d3d3c-124">-KeyName</span></span>
<span data-ttu-id="d3d3c-125">Nome della chiave dell'account di archiviazione da rigenerare e rendere attiva.</span><span class="sxs-lookup"><span data-stu-id="d3d3c-125">Name of storage account key to regenerate and make active.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3d3c-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d3d3c-126">-PassThru</span></span>
<span data-ttu-id="d3d3c-127">Il cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="d3d3c-127">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="d3d3c-128">Se si specifica questa opzione, il cmdlet restituisce l'account di archiviazione gestito eliminato.</span><span class="sxs-lookup"><span data-stu-id="d3d3c-128">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="d3d3c-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="d3d3c-129">-VaultName</span></span>
<span data-ttu-id="d3d3c-130">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="d3d3c-130">Vault name.</span></span>
<span data-ttu-id="d3d3c-131">Il cmdlet crea l'FQDN di un vault in base al nome e all'ambiente attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="d3d3c-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="d3d3c-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d3d3c-132">-Confirm</span></span>
<span data-ttu-id="d3d3c-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3d3c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3d3c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3d3c-134">-WhatIf</span></span>
<span data-ttu-id="d3d3c-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d3d3c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3d3c-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d3d3c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3d3c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3d3c-137">CommonParameters</span></span>
<span data-ttu-id="d3d3c-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3d3c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3d3c-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d3d3c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3d3c-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="d3d3c-140">INPUTS</span></span>

### <span data-ttu-id="d3d3c-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="d3d3c-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="d3d3c-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d3d3c-142">OUTPUTS</span></span>

### <span data-ttu-id="d3d3c-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d3d3c-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="d3d3c-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="d3d3c-144">NOTES</span></span>

## <span data-ttu-id="d3d3c-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d3d3c-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

