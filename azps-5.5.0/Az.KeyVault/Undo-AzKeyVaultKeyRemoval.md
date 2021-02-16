---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
ms.openlocfilehash: d6637b8c180dd2ef25bdba5326f0a42a364bc8ab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185454"
---
# <span data-ttu-id="607a1-101">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="607a1-101">Undo-AzKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="607a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="607a1-102">SYNOPSIS</span></span>
<span data-ttu-id="607a1-103">Recupera una chiave eliminata di un vault chiave in stato attivo.</span><span class="sxs-lookup"><span data-stu-id="607a1-103">Recovers a deleted key in a key vault into an active state.</span></span>

## <span data-ttu-id="607a1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="607a1-104">SYNTAX</span></span>

### <span data-ttu-id="607a1-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="607a1-105">Default (Default)</span></span>
```
Undo-AzKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="607a1-106">HsmInteractive</span><span class="sxs-lookup"><span data-stu-id="607a1-106">HsmInteractive</span></span>
```
Undo-AzKeyVaultKeyRemoval -HsmName <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="607a1-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="607a1-107">InputObject</span></span>
```
Undo-AzKeyVaultKeyRemoval [-InputObject] <PSDeletedKeyVaultKeyIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="607a1-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="607a1-108">DESCRIPTION</span></span>
<span data-ttu-id="607a1-109">Il cmdlet **Undo-AzKeyVaultKeyRemoval** recupera una chiave eliminata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="607a1-109">The **Undo-AzKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="607a1-110">La chiave recuperata sarà attiva e può essere usata per tutte le normali operazioni chiave.</span><span class="sxs-lookup"><span data-stu-id="607a1-110">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="607a1-111">Per eseguire questa operazione, il chiamante deve avere l'autorizzazione di recupero.</span><span class="sxs-lookup"><span data-stu-id="607a1-111">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="607a1-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="607a1-112">EXAMPLES</span></span>

### <span data-ttu-id="607a1-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="607a1-113">Example 1</span></span>
```powershell
PS C:\> Undo-AzKeyVaultKeyRemoval -VaultName 'MyKeyVault' -Name 'MyKey'

Vault Name     : MyKeyVault
Name           : MyKey
Version        : 1af807cc331a49d0b52b7c75e1b2366e
Id             : https://mykeybault.vault.azure.net:443/keys/mykey/1af807cc331a49d0b52b7c75e1b2366e
Enabled        : True
Expires        :
Not Before     :
Created        : 5/24/2018 8:32:27 PM
Updated        : 5/24/2018 8:32:27 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="607a1-114">Questo comando recupera la chiave "MyKey" eliminata in precedenza, in uno stato attivo e utilizzabile.</span><span class="sxs-lookup"><span data-stu-id="607a1-114">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="607a1-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="607a1-115">PARAMETERS</span></span>

### <span data-ttu-id="607a1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="607a1-116">-DefaultProfile</span></span>
<span data-ttu-id="607a1-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="607a1-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="607a1-118">-HsmName</span><span class="sxs-lookup"><span data-stu-id="607a1-118">-HsmName</span></span>
<span data-ttu-id="607a1-119">Nome HSM.</span><span class="sxs-lookup"><span data-stu-id="607a1-119">HSM name.</span></span> <span data-ttu-id="607a1-120">Il cmdlet crea l'FQDN di un servizio HSM gestito in base al nome e all'ambiente attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="607a1-120">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmInteractive
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="607a1-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="607a1-121">-InputObject</span></span>
<span data-ttu-id="607a1-122">Oggetto chiave eliminato</span><span class="sxs-lookup"><span data-stu-id="607a1-122">Deleted key object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="607a1-123">-Name</span><span class="sxs-lookup"><span data-stu-id="607a1-123">-Name</span></span>
<span data-ttu-id="607a1-124">Nome della chiave.</span><span class="sxs-lookup"><span data-stu-id="607a1-124">Key name.</span></span>
<span data-ttu-id="607a1-125">Il cmdlet crea l'FQDN di una chiave dal nome del vault, l'ambiente attualmente selezionato e il nome della chiave.</span><span class="sxs-lookup"><span data-stu-id="607a1-125">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, HsmInteractive
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="607a1-126">-VaultName</span><span class="sxs-lookup"><span data-stu-id="607a1-126">-VaultName</span></span>
<span data-ttu-id="607a1-127">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="607a1-127">Vault name.</span></span>
<span data-ttu-id="607a1-128">Il cmdlet crea l'FQDN di un vault in base al nome e all'ambiente attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="607a1-128">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="607a1-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="607a1-129">-Confirm</span></span>
<span data-ttu-id="607a1-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="607a1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="607a1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="607a1-131">-WhatIf</span></span>
<span data-ttu-id="607a1-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="607a1-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="607a1-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="607a1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="607a1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="607a1-134">CommonParameters</span></span>
<span data-ttu-id="607a1-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="607a1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="607a1-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="607a1-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="607a1-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="607a1-137">INPUTS</span></span>

### <span data-ttu-id="607a1-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="607a1-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="607a1-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="607a1-139">OUTPUTS</span></span>

### <span data-ttu-id="607a1-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="607a1-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="607a1-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="607a1-141">NOTES</span></span>

## <span data-ttu-id="607a1-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="607a1-142">RELATED LINKS</span></span>

[<span data-ttu-id="607a1-143">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="607a1-143">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="607a1-144">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="607a1-144">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="607a1-145">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="607a1-145">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

