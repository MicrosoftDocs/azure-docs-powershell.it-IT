---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/undo-AzKeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
ms.openlocfilehash: e65bef4119c51b989287bbf0db2e7587fef50271
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862989"
---
# <span data-ttu-id="e29f2-101">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="e29f2-101">Undo-AzKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="e29f2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e29f2-102">SYNOPSIS</span></span>
<span data-ttu-id="e29f2-103">Recuperare un segreto eliminato in un Vault chiave in uno stato attivo.</span><span class="sxs-lookup"><span data-stu-id="e29f2-103">Recovers a deleted secret in a key vault into an active state.</span></span>

## <span data-ttu-id="e29f2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e29f2-104">SYNTAX</span></span>

```
Undo-AzKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e29f2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e29f2-105">DESCRIPTION</span></span>
<span data-ttu-id="e29f2-106">Il cmdlet **Undo-AzKeyVaultSecretRemoval** recupera un segreto eliminato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="e29f2-106">The **Undo-AzKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="e29f2-107">Il segreto recuperato sarà attivo e può essere usato per tutte le normali operazioni segrete.</span><span class="sxs-lookup"><span data-stu-id="e29f2-107">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="e29f2-108">Per eseguire questa operazione, il chiamante deve avere l'autorizzazione "Recupera".</span><span class="sxs-lookup"><span data-stu-id="e29f2-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="e29f2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e29f2-109">EXAMPLES</span></span>

### <span data-ttu-id="e29f2-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e29f2-110">Example 1</span></span>
```
PS C:\> Undo-AzKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'
```

<span data-ttu-id="e29f2-111">Questo comando recupererà il segreto "segrete" che è stato eliminato in precedenza in uno stato attivo e utilizzabile.</span><span class="sxs-lookup"><span data-stu-id="e29f2-111">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="e29f2-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e29f2-112">PARAMETERS</span></span>

### <span data-ttu-id="e29f2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e29f2-113">-DefaultProfile</span></span>
<span data-ttu-id="e29f2-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e29f2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e29f2-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="e29f2-115">-Name</span></span>
<span data-ttu-id="e29f2-116">Nome segreto.</span><span class="sxs-lookup"><span data-stu-id="e29f2-116">Secret name.</span></span>
<span data-ttu-id="e29f2-117">Cmdlet costruisce il nome di dominio completo di un segreto dal nome della volta, dall'ambiente selezionato e da quello segreto.</span><span class="sxs-lookup"><span data-stu-id="e29f2-117">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="e29f2-118">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="e29f2-118">-VaultName</span></span>
<span data-ttu-id="e29f2-119">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="e29f2-119">Vault name.</span></span>
<span data-ttu-id="e29f2-120">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="e29f2-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="e29f2-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e29f2-121">-Confirm</span></span>
<span data-ttu-id="e29f2-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e29f2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e29f2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e29f2-123">-WhatIf</span></span>
<span data-ttu-id="e29f2-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e29f2-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e29f2-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e29f2-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e29f2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e29f2-126">CommonParameters</span></span>
<span data-ttu-id="e29f2-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e29f2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e29f2-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e29f2-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e29f2-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e29f2-129">INPUTS</span></span>

### <span data-ttu-id="e29f2-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e29f2-130">System.String</span></span>

## <span data-ttu-id="e29f2-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e29f2-131">OUTPUTS</span></span>

### <span data-ttu-id="e29f2-132">Microsoft. Azure. Commands. Vault. Models. Secret</span><span class="sxs-lookup"><span data-stu-id="e29f2-132">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="e29f2-133">Note</span><span class="sxs-lookup"><span data-stu-id="e29f2-133">NOTES</span></span>

## <span data-ttu-id="e29f2-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e29f2-134">RELATED LINKS</span></span>

[<span data-ttu-id="e29f2-135">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e29f2-135">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="e29f2-136">Add-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e29f2-136">Add-AzKeyVaultSecret</span></span>](./Add-AzKeyVaultSecret.md)

[<span data-ttu-id="e29f2-137">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e29f2-137">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)
