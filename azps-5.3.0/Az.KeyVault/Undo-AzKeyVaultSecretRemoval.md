---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
ms.openlocfilehash: 1eca5a380dc71a5bd801c21bb7e7f556fcff0d35
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486960"
---
# <span data-ttu-id="7a910-101">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="7a910-101">Undo-AzKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="7a910-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7a910-102">SYNOPSIS</span></span>
<span data-ttu-id="7a910-103">Recuperare un segreto eliminato in un Vault chiave in uno stato attivo.</span><span class="sxs-lookup"><span data-stu-id="7a910-103">Recovers a deleted secret in a key vault into an active state.</span></span>

## <span data-ttu-id="7a910-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7a910-104">SYNTAX</span></span>

### <span data-ttu-id="7a910-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7a910-105">Default (Default)</span></span>
```
Undo-AzKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a910-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="7a910-106">InputObject</span></span>
```
Undo-AzKeyVaultSecretRemoval [-InputObject] <PSDeletedKeyVaultSecretIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a910-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a910-107">DESCRIPTION</span></span>
<span data-ttu-id="7a910-108">Il cmdlet **Undo-AzKeyVaultSecretRemoval** recupera un segreto eliminato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="7a910-108">The **Undo-AzKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="7a910-109">Il segreto recuperato sarà attivo e può essere usato per tutte le normali operazioni segrete.</span><span class="sxs-lookup"><span data-stu-id="7a910-109">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="7a910-110">Per eseguire questa operazione, il chiamante deve avere l'autorizzazione "Recupera".</span><span class="sxs-lookup"><span data-stu-id="7a910-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="7a910-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7a910-111">EXAMPLES</span></span>

### <span data-ttu-id="7a910-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7a910-112">Example 1</span></span>
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

<span data-ttu-id="7a910-113">Questo comando recupererà il segreto "segrete" che è stato eliminato in precedenza in uno stato attivo e utilizzabile.</span><span class="sxs-lookup"><span data-stu-id="7a910-113">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="7a910-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7a910-114">PARAMETERS</span></span>

### <span data-ttu-id="7a910-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a910-115">-DefaultProfile</span></span>
<span data-ttu-id="7a910-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7a910-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a910-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a910-117">-InputObject</span></span>
<span data-ttu-id="7a910-118">Oggetto segreto eliminato</span><span class="sxs-lookup"><span data-stu-id="7a910-118">Deleted secret object</span></span>

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

### <span data-ttu-id="7a910-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="7a910-119">-Name</span></span>
<span data-ttu-id="7a910-120">Nome segreto.</span><span class="sxs-lookup"><span data-stu-id="7a910-120">Secret name.</span></span>
<span data-ttu-id="7a910-121">Cmdlet costruisce il nome di dominio completo di un segreto dal nome della volta, dall'ambiente selezionato e da quello segreto.</span><span class="sxs-lookup"><span data-stu-id="7a910-121">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="7a910-122">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="7a910-122">-VaultName</span></span>
<span data-ttu-id="7a910-123">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="7a910-123">Vault name.</span></span>
<span data-ttu-id="7a910-124">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="7a910-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="7a910-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7a910-125">-Confirm</span></span>
<span data-ttu-id="7a910-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a910-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a910-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a910-127">-WhatIf</span></span>
<span data-ttu-id="7a910-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7a910-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a910-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7a910-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a910-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a910-130">CommonParameters</span></span>
<span data-ttu-id="7a910-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a910-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a910-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7a910-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a910-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7a910-133">INPUTS</span></span>

### <span data-ttu-id="7a910-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="7a910-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="7a910-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7a910-135">OUTPUTS</span></span>

### <span data-ttu-id="7a910-136">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7a910-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="7a910-137">Note</span><span class="sxs-lookup"><span data-stu-id="7a910-137">NOTES</span></span>

## <span data-ttu-id="7a910-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7a910-138">RELATED LINKS</span></span>

[<span data-ttu-id="7a910-139">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7a910-139">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="7a910-140">Add-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7a910-140">Add-AzKeyVaultSecret</span></span>](./Add-AzKeyVaultSecret.md)

[<span data-ttu-id="7a910-141">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7a910-141">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)
