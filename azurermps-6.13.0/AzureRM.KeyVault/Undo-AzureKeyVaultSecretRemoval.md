---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultSecretRemoval.md
ms.openlocfilehash: ecc22deb6be4f8fe85b66454091f6bfbd01d3a80
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515188"
---
# <span data-ttu-id="753d0-101">Undo-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="753d0-101">Undo-AzureKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="753d0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="753d0-102">SYNOPSIS</span></span>
<span data-ttu-id="753d0-103">Recuperare un segreto eliminato in un Vault chiave in uno stato attivo.</span><span class="sxs-lookup"><span data-stu-id="753d0-103">Recovers a deleted secret in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="753d0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="753d0-104">SYNTAX</span></span>

### <span data-ttu-id="753d0-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="753d0-105">Default (Default)</span></span>
```
Undo-AzureKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="753d0-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="753d0-106">InputObject</span></span>
```
Undo-AzureKeyVaultSecretRemoval [-InputObject] <PSDeletedKeyVaultSecretIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="753d0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="753d0-107">DESCRIPTION</span></span>
<span data-ttu-id="753d0-108">Il cmdlet **Undo-AzureKeyVaultSecretRemoval** recupera un segreto eliminato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="753d0-108">The **Undo-AzureKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="753d0-109">Il segreto recuperato sarà attivo e può essere usato per tutte le normali operazioni segrete.</span><span class="sxs-lookup"><span data-stu-id="753d0-109">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="753d0-110">Per eseguire questa operazione, il chiamante deve avere l'autorizzazione "Recupera".</span><span class="sxs-lookup"><span data-stu-id="753d0-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="753d0-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="753d0-111">EXAMPLES</span></span>

### <span data-ttu-id="753d0-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="753d0-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzureKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'

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

<span data-ttu-id="753d0-113">Questo comando recupererà il segreto "segrete" che è stato eliminato in precedenza in uno stato attivo e utilizzabile.</span><span class="sxs-lookup"><span data-stu-id="753d0-113">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="753d0-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="753d0-114">PARAMETERS</span></span>

### <span data-ttu-id="753d0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="753d0-115">-DefaultProfile</span></span>
<span data-ttu-id="753d0-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="753d0-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="753d0-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="753d0-117">-InputObject</span></span>
<span data-ttu-id="753d0-118">Oggetto segreto eliminato</span><span class="sxs-lookup"><span data-stu-id="753d0-118">Deleted secret object</span></span>

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

### <span data-ttu-id="753d0-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="753d0-119">-Name</span></span>
<span data-ttu-id="753d0-120">Nome segreto.</span><span class="sxs-lookup"><span data-stu-id="753d0-120">Secret name.</span></span>
<span data-ttu-id="753d0-121">Cmdlet costruisce il nome di dominio completo di un segreto dal nome della volta, dall'ambiente selezionato e da quello segreto.</span><span class="sxs-lookup"><span data-stu-id="753d0-121">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="753d0-122">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="753d0-122">-VaultName</span></span>
<span data-ttu-id="753d0-123">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="753d0-123">Vault name.</span></span>
<span data-ttu-id="753d0-124">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="753d0-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="753d0-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="753d0-125">-Confirm</span></span>
<span data-ttu-id="753d0-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="753d0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="753d0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="753d0-127">-WhatIf</span></span>
<span data-ttu-id="753d0-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="753d0-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="753d0-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="753d0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="753d0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="753d0-130">CommonParameters</span></span>
<span data-ttu-id="753d0-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="753d0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="753d0-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="753d0-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="753d0-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="753d0-133">INPUTS</span></span>

### <span data-ttu-id="753d0-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="753d0-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>
<span data-ttu-id="753d0-135">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="753d0-135">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="753d0-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="753d0-136">OUTPUTS</span></span>

### <span data-ttu-id="753d0-137">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="753d0-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="753d0-138">Note</span><span class="sxs-lookup"><span data-stu-id="753d0-138">NOTES</span></span>

## <span data-ttu-id="753d0-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="753d0-139">RELATED LINKS</span></span>

[<span data-ttu-id="753d0-140">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="753d0-140">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

[<span data-ttu-id="753d0-141">Add-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="753d0-141">Add-AzureKeyVaultSecret</span></span>](./Add-AzureKeyVaultSecret.md)

[<span data-ttu-id="753d0-142">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="753d0-142">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)
