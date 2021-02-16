---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultRemoval.md
ms.openlocfilehash: 98a3a023564c2c61f1398856e8a089276aeae7bc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185431"
---
# <span data-ttu-id="58471-101">Undo-AzKeyVaultRemoval</span><span class="sxs-lookup"><span data-stu-id="58471-101">Undo-AzKeyVaultRemoval</span></span>

## <span data-ttu-id="58471-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58471-102">SYNOPSIS</span></span>
<span data-ttu-id="58471-103">Recupera un vault chiave eliminato in stato attivo.</span><span class="sxs-lookup"><span data-stu-id="58471-103">Recovers a deleted key vault into an active state.</span></span>

## <span data-ttu-id="58471-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="58471-104">SYNTAX</span></span>

### <span data-ttu-id="58471-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="58471-105">Default (Default)</span></span>
```
Undo-AzKeyVaultRemoval [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58471-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="58471-106">InputObject</span></span>
```
Undo-AzKeyVaultRemoval [-InputObject] <PSDeletedKeyVault> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58471-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="58471-107">DESCRIPTION</span></span>
<span data-ttu-id="58471-108">Il cmdlet **Undo-AzKeyVaultRemoval** recupera un vault delle chiavi eliminato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="58471-108">The **Undo-AzKeyVaultRemoval** cmdlet will recover a previously deleted key vault.</span></span> <span data-ttu-id="58471-109">Il vault recuperato sarà attivo dopo il ripristino</span><span class="sxs-lookup"><span data-stu-id="58471-109">The recovered vault will be active after recovery</span></span>

## <span data-ttu-id="58471-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="58471-110">EXAMPLES</span></span>

### <span data-ttu-id="58471-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="58471-111">Example 1</span></span>
```powershell
PS C:\> Undo-AzKeyVaultRemoval -VaultName 'MyKeyVault' -ResourceGroupName 'MyResourceGroup' -Location 'eastus2' -Tag @{"x"= "y"}

Vault Name                       : MyKeyVault
Resource Group Name              : MyResourceGroup
Location                         : eastus2
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers
                                   /Microsoft.KeyVault/vaults/mykeyvault
Vault URI                        : https://mykeyvault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : True
Enabled For Disk Encryption?     : True
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : get, create, delete, list, update,
                                   import, backup, restore, recover
                                   Permissions to Secrets                     : get, list, set, delete, backup,
                                   restore, recover
                                   Permissions to Certificates                : get, delete, list, create, import,
                                   update, deleteissuers, getissuers, listissuers, managecontacts, manageissuers,
                                   setissuers, recover
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update

Tags                             :
                                   Name  Value
                                   ====  =====
                                   x     y
```

<span data-ttu-id="58471-112">Questo comando recupera il vault della chiave "MyKeyVault" eliminato in precedenza dall'area estus2 e dal gruppo di risorse "MyResourceGroup" in uno stato attivo e utilizzabile.</span><span class="sxs-lookup"><span data-stu-id="58471-112">This command will recover the key vault 'MyKeyVault' that was previously deleted from eastus2 region and 'MyResourceGroup' resource group, into an active and usable state.</span></span> <span data-ttu-id="58471-113">Sostituisce inoltre i tag con un nuovo contrassegno.</span><span class="sxs-lookup"><span data-stu-id="58471-113">It also replaces the tags with new tag.</span></span>

## <span data-ttu-id="58471-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58471-114">PARAMETERS</span></span>

### <span data-ttu-id="58471-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58471-115">-DefaultProfile</span></span>
<span data-ttu-id="58471-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="58471-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="58471-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58471-117">-InputObject</span></span>
<span data-ttu-id="58471-118">Oggetto vault eliminato</span><span class="sxs-lookup"><span data-stu-id="58471-118">Deleted vault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58471-119">-Location</span><span class="sxs-lookup"><span data-stu-id="58471-119">-Location</span></span>
<span data-ttu-id="58471-120">Specifica l'area Azure originale del vault eliminato.</span><span class="sxs-lookup"><span data-stu-id="58471-120">Specifies the deleted vault original Azure region.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58471-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58471-121">-ResourceGroupName</span></span>
<span data-ttu-id="58471-122">Specifica il nome di un gruppo di risorse esistente in cui creare il vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="58471-122">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58471-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="58471-123">-Tag</span></span>
<span data-ttu-id="58471-124">Coppie chiave-valore sotto forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="58471-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="58471-125">Ad esempio: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="58471-125">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58471-126">-VaultName</span><span class="sxs-lookup"><span data-stu-id="58471-126">-VaultName</span></span>
<span data-ttu-id="58471-127">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="58471-127">Vault name.</span></span>
<span data-ttu-id="58471-128">Il cmdlet crea l'FQDN di un vault in base al nome e all'ambiente attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="58471-128">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58471-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="58471-129">-Confirm</span></span>
<span data-ttu-id="58471-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58471-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58471-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58471-131">-WhatIf</span></span>
<span data-ttu-id="58471-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="58471-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="58471-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="58471-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58471-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58471-134">CommonParameters</span></span>
<span data-ttu-id="58471-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58471-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58471-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="58471-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58471-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="58471-137">INPUTS</span></span>

### <span data-ttu-id="58471-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span><span class="sxs-lookup"><span data-stu-id="58471-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span></span>

## <span data-ttu-id="58471-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="58471-139">OUTPUTS</span></span>

### <span data-ttu-id="58471-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="58471-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="58471-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="58471-141">NOTES</span></span>

## <span data-ttu-id="58471-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="58471-142">RELATED LINKS</span></span>

[<span data-ttu-id="58471-143">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="58471-143">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)

[<span data-ttu-id="58471-144">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="58471-144">New-AzKeyVault</span></span>](./New-AzKeyVault.md)

[<span data-ttu-id="58471-145">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="58471-145">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)
