---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/undo-AzKeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
ms.openlocfilehash: 9c240d3902aeba38af4281ba31bacea76bad0a58
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399091"
---
# <span data-ttu-id="70878-101">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="70878-101">Undo-AzKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="70878-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70878-102">SYNOPSIS</span></span>
<span data-ttu-id="70878-103">Recupera un segreto eliminato in un vault della chiave in stato attivo.</span><span class="sxs-lookup"><span data-stu-id="70878-103">Recovers a deleted secret in a key vault into an active state.</span></span>

## <span data-ttu-id="70878-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="70878-104">SYNTAX</span></span>

```
Undo-AzKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70878-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="70878-105">DESCRIPTION</span></span>
<span data-ttu-id="70878-106">Il cmdlet **Undo-AzKeyVaultSecretRemoval** recupera un segreto eliminato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="70878-106">The **Undo-AzKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="70878-107">Il segreto recuperato sarà attivo e può essere usato per tutte le normali operazioni segrete.</span><span class="sxs-lookup"><span data-stu-id="70878-107">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="70878-108">Per eseguire questa operazione, il chiamante deve avere l'autorizzazione di recupero.</span><span class="sxs-lookup"><span data-stu-id="70878-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="70878-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="70878-109">EXAMPLES</span></span>

### <span data-ttu-id="70878-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="70878-110">Example 1</span></span>
```
PS C:\> Undo-AzKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'
```

<span data-ttu-id="70878-111">Questo comando recupera il segreto "MySecret" eliminato in precedenza, in uno stato attivo e utilizzabile.</span><span class="sxs-lookup"><span data-stu-id="70878-111">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="70878-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70878-112">PARAMETERS</span></span>

### <span data-ttu-id="70878-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70878-113">-DefaultProfile</span></span>
<span data-ttu-id="70878-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="70878-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70878-115">-Name</span><span class="sxs-lookup"><span data-stu-id="70878-115">-Name</span></span>
<span data-ttu-id="70878-116">Nome segreto.</span><span class="sxs-lookup"><span data-stu-id="70878-116">Secret name.</span></span>
<span data-ttu-id="70878-117">Il cmdlet crea l'FQDN di un segreto dal nome del vault, l'ambiente attualmente selezionato e il nome del segreto.</span><span class="sxs-lookup"><span data-stu-id="70878-117">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70878-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="70878-118">-VaultName</span></span>
<span data-ttu-id="70878-119">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="70878-119">Vault name.</span></span>
<span data-ttu-id="70878-120">Il cmdlet crea l'FQDN di un vault in base al nome e all'ambiente attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="70878-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70878-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="70878-121">-Confirm</span></span>
<span data-ttu-id="70878-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70878-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70878-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70878-123">-WhatIf</span></span>
<span data-ttu-id="70878-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="70878-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70878-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="70878-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70878-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70878-126">CommonParameters</span></span>
<span data-ttu-id="70878-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70878-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70878-128">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70878-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70878-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="70878-129">INPUTS</span></span>

### <span data-ttu-id="70878-130">System.String</span><span class="sxs-lookup"><span data-stu-id="70878-130">System.String</span></span>

## <span data-ttu-id="70878-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="70878-131">OUTPUTS</span></span>

### <span data-ttu-id="70878-132">Microsoft.Azure.Commands.KeyVault.Models.Secret</span><span class="sxs-lookup"><span data-stu-id="70878-132">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="70878-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="70878-133">NOTES</span></span>

## <span data-ttu-id="70878-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="70878-134">RELATED LINKS</span></span>

[<span data-ttu-id="70878-135">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="70878-135">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)


[<span data-ttu-id="70878-136">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="70878-136">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)
