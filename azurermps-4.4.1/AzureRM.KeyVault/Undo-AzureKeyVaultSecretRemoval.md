---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultSecretRemoval.md
ms.openlocfilehash: e71fa3098003f6fb713c90903eee6e97ca4f42ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687184"
---
# <span data-ttu-id="f1a20-101">Undo-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="f1a20-101">Undo-AzureKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="f1a20-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f1a20-102">SYNOPSIS</span></span>
<span data-ttu-id="f1a20-103">Recuperare un segreto eliminato in un Vault chiave in uno stato attivo.</span><span class="sxs-lookup"><span data-stu-id="f1a20-103">Recovers a deleted secret in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1a20-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f1a20-104">SYNTAX</span></span>

```
Undo-AzureKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1a20-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1a20-105">DESCRIPTION</span></span>
<span data-ttu-id="f1a20-106">Il cmdlet **Undo-AzureKeyVaultSecretRemoval** recupera un segreto eliminato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="f1a20-106">The **Undo-AzureKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="f1a20-107">Il segreto recuperato sarà attivo e può essere usato per tutte le normali operazioni segrete.</span><span class="sxs-lookup"><span data-stu-id="f1a20-107">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="f1a20-108">Per eseguire questa operazione, il chiamante deve avere l'autorizzazione "Recupera".</span><span class="sxs-lookup"><span data-stu-id="f1a20-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="f1a20-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f1a20-109">EXAMPLES</span></span>

### <span data-ttu-id="f1a20-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f1a20-110">Example 1</span></span>
```
PS C:\> Undo-AzureKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'
```

<span data-ttu-id="f1a20-111">Questo comando recupererà il segreto "segrete" che è stato eliminato in precedenza in uno stato attivo e utilizzabile.</span><span class="sxs-lookup"><span data-stu-id="f1a20-111">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="f1a20-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f1a20-112">PARAMETERS</span></span>

### <span data-ttu-id="f1a20-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="f1a20-113">-Name</span></span>
<span data-ttu-id="f1a20-114">Nome segreto.</span><span class="sxs-lookup"><span data-stu-id="f1a20-114">Secret name.</span></span>
<span data-ttu-id="f1a20-115">Cmdlet costruisce il nome di dominio completo di un segreto dal nome della volta, dall'ambiente selezionato e da quello segreto.</span><span class="sxs-lookup"><span data-stu-id="f1a20-115">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1a20-116">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="f1a20-116">-VaultName</span></span>
<span data-ttu-id="f1a20-117">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="f1a20-117">Vault name.</span></span>
<span data-ttu-id="f1a20-118">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="f1a20-118">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1a20-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f1a20-119">-Confirm</span></span>
<span data-ttu-id="f1a20-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1a20-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1a20-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1a20-121">-WhatIf</span></span>
<span data-ttu-id="f1a20-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f1a20-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1a20-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f1a20-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1a20-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1a20-124">-DefaultProfile</span></span>
<span data-ttu-id="f1a20-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f1a20-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1a20-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1a20-126">CommonParameters</span></span>
<span data-ttu-id="f1a20-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1a20-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1a20-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1a20-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1a20-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f1a20-129">INPUTS</span></span>

### <span data-ttu-id="f1a20-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f1a20-130">System.String</span></span>

## <span data-ttu-id="f1a20-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f1a20-131">OUTPUTS</span></span>

### <span data-ttu-id="f1a20-132">Microsoft. Azure. Commands. Vault. Models. Secret</span><span class="sxs-lookup"><span data-stu-id="f1a20-132">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="f1a20-133">Note</span><span class="sxs-lookup"><span data-stu-id="f1a20-133">NOTES</span></span>

## <span data-ttu-id="f1a20-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f1a20-134">RELATED LINKS</span></span>

[<span data-ttu-id="f1a20-135">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f1a20-135">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

[<span data-ttu-id="f1a20-136">Add-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f1a20-136">Add-AzureKeyVaultSecret</span></span>](./Add-AzureKeyVaultSecret.md)

[<span data-ttu-id="f1a20-137">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f1a20-137">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)
