---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/undo-azkeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
ms.openlocfilehash: dc4c8925d4ddf00cc2e2739d3aa06285f628e423
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976990"
---
# <span data-ttu-id="a6070-101">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="a6070-101">Undo-AzKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="a6070-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6070-102">SYNOPSIS</span></span>
<span data-ttu-id="a6070-103">Recupera un segreto eliminato in uno stato attivo in un vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="a6070-103">Recovers a deleted secret in a key vault into an active state.</span></span>

## <span data-ttu-id="a6070-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a6070-104">SYNTAX</span></span>

### <span data-ttu-id="a6070-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a6070-105">Default (Default)</span></span>
```
Undo-AzKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6070-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a6070-106">InputObject</span></span>
```
Undo-AzKeyVaultSecretRemoval [-InputObject] <PSDeletedKeyVaultSecretIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6070-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a6070-107">DESCRIPTION</span></span>
<span data-ttu-id="a6070-108">Il cmdlet **Undo-AzKeyVaultSecretRemoval** recupera un segreto eliminato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="a6070-108">The **Undo-AzKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="a6070-109">Il segreto recuperato sarà attivo e può essere usato per tutte le normali operazioni segrete.</span><span class="sxs-lookup"><span data-stu-id="a6070-109">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="a6070-110">Per eseguire questa operazione, il chiamante deve avere l'autorizzazione di recupero.</span><span class="sxs-lookup"><span data-stu-id="a6070-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="a6070-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a6070-111">EXAMPLES</span></span>

### <span data-ttu-id="a6070-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a6070-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'

Vault Name   : MyKeyVault
Name         : MySecret
Version      : f622abc7b1394092812f1eb0f85dc91c
Id           : https://mykeyvault.vault.azure.net:443/secrets/mysecret/f622abc7b1394092812f1eb0f85dc91c
Enabled      : True
Expires      :
Not Before   :
Created      : 4/19/2018 5:56:02 PM
Updated      : 4/26/2018 7:48:40 PM
Content Type :
Tags         :
```

<span data-ttu-id="a6070-113">Questo comando recupera il segreto "MySecret" eliminato in precedenza, in uno stato attivo e utilizzabile.</span><span class="sxs-lookup"><span data-stu-id="a6070-113">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="a6070-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6070-114">PARAMETERS</span></span>

### <span data-ttu-id="a6070-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6070-115">-DefaultProfile</span></span>
<span data-ttu-id="a6070-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a6070-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a6070-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6070-117">-InputObject</span></span>
<span data-ttu-id="a6070-118">Oggetto segreto eliminato</span><span class="sxs-lookup"><span data-stu-id="a6070-118">Deleted secret object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6070-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a6070-119">-Name</span></span>
<span data-ttu-id="a6070-120">Nome segreto.</span><span class="sxs-lookup"><span data-stu-id="a6070-120">Secret name.</span></span>
<span data-ttu-id="a6070-121">Il cmdlet crea l'FQDN di un segreto dal nome del vault, l'ambiente attualmente selezionato e il nome del segreto.</span><span class="sxs-lookup"><span data-stu-id="a6070-121">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6070-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a6070-122">-VaultName</span></span>
<span data-ttu-id="a6070-123">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="a6070-123">Vault name.</span></span>
<span data-ttu-id="a6070-124">Il cmdlet crea l'FQDN di un vault in base al nome e all'ambiente attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="a6070-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="a6070-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6070-125">-Confirm</span></span>
<span data-ttu-id="a6070-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6070-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6070-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6070-127">-WhatIf</span></span>
<span data-ttu-id="a6070-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a6070-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6070-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a6070-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6070-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6070-130">CommonParameters</span></span>
<span data-ttu-id="a6070-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6070-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6070-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a6070-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6070-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="a6070-133">INPUTS</span></span>

### <span data-ttu-id="a6070-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="a6070-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="a6070-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a6070-135">OUTPUTS</span></span>

### <span data-ttu-id="a6070-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a6070-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="a6070-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="a6070-137">NOTES</span></span>

## <span data-ttu-id="a6070-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a6070-138">RELATED LINKS</span></span>

[<span data-ttu-id="a6070-139">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a6070-139">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="a6070-140">Add-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a6070-140">Add-AzKeyVaultSecret</span></span>](./Add-AzKeyVaultSecret.md)

[<span data-ttu-id="a6070-141">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a6070-141">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)
