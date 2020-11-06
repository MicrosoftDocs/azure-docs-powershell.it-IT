---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultSecretRemoval.md
ms.openlocfilehash: 07c62b1b106453cf9b19610867be39458943bcab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518088"
---
# <span data-ttu-id="26095-101">Undo-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="26095-101">Undo-AzureKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="26095-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="26095-102">SYNOPSIS</span></span>
<span data-ttu-id="26095-103">Recuperare un segreto eliminato in un Vault chiave in uno stato attivo.</span><span class="sxs-lookup"><span data-stu-id="26095-103">Recovers a deleted secret in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26095-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="26095-104">SYNTAX</span></span>

### <span data-ttu-id="26095-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="26095-105">Default (Default)</span></span>
```
Undo-AzureKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26095-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="26095-106">InputObject</span></span>
```
Undo-AzureKeyVaultSecretRemoval [-InputObject] <PSDeletedKeyVaultSecretIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26095-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26095-107">DESCRIPTION</span></span>
<span data-ttu-id="26095-108">Il cmdlet **Undo-AzureKeyVaultSecretRemoval** recupera un segreto eliminato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="26095-108">The **Undo-AzureKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="26095-109">Il segreto recuperato sarà attivo e può essere usato per tutte le normali operazioni segrete.</span><span class="sxs-lookup"><span data-stu-id="26095-109">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="26095-110">Per eseguire questa operazione, il chiamante deve avere l'autorizzazione "Recupera".</span><span class="sxs-lookup"><span data-stu-id="26095-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="26095-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="26095-111">EXAMPLES</span></span>

### <span data-ttu-id="26095-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="26095-112">Example 1</span></span>
```
PS C:\> Undo-AzureKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'
```

<span data-ttu-id="26095-113">Questo comando recupererà il segreto "segrete" che è stato eliminato in precedenza in uno stato attivo e utilizzabile.</span><span class="sxs-lookup"><span data-stu-id="26095-113">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="26095-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="26095-114">PARAMETERS</span></span>

### <span data-ttu-id="26095-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26095-115">-DefaultProfile</span></span>
<span data-ttu-id="26095-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="26095-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26095-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26095-117">-InputObject</span></span>
<span data-ttu-id="26095-118">Oggetto segreto eliminato</span><span class="sxs-lookup"><span data-stu-id="26095-118">Deleted secret object</span></span>

```yaml
Type: PSDeletedKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26095-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="26095-119">-Name</span></span>
<span data-ttu-id="26095-120">Nome segreto.</span><span class="sxs-lookup"><span data-stu-id="26095-120">Secret name.</span></span>
<span data-ttu-id="26095-121">Cmdlet costruisce il nome di dominio completo di un segreto dal nome della volta, dall'ambiente selezionato e da quello segreto.</span><span class="sxs-lookup"><span data-stu-id="26095-121">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26095-122">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="26095-122">-VaultName</span></span>
<span data-ttu-id="26095-123">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="26095-123">Vault name.</span></span>
<span data-ttu-id="26095-124">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="26095-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26095-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="26095-125">-Confirm</span></span>
<span data-ttu-id="26095-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26095-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26095-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26095-127">-WhatIf</span></span>
<span data-ttu-id="26095-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="26095-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26095-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="26095-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26095-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26095-130">CommonParameters</span></span>
<span data-ttu-id="26095-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26095-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26095-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26095-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26095-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="26095-133">INPUTS</span></span>

### <span data-ttu-id="26095-134">System. String</span><span class="sxs-lookup"><span data-stu-id="26095-134">System.String</span></span>

## <span data-ttu-id="26095-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="26095-135">OUTPUTS</span></span>

### <span data-ttu-id="26095-136">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="26095-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="26095-137">Note</span><span class="sxs-lookup"><span data-stu-id="26095-137">NOTES</span></span>

## <span data-ttu-id="26095-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="26095-138">RELATED LINKS</span></span>

[<span data-ttu-id="26095-139">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="26095-139">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

[<span data-ttu-id="26095-140">Add-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="26095-140">Add-AzureKeyVaultSecret</span></span>](./Add-AzureKeyVaultSecret.md)

[<span data-ttu-id="26095-141">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="26095-141">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)
