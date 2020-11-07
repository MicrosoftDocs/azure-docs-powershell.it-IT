---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultcertificateremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultCertificateRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultCertificateRemoval.md
ms.openlocfilehash: 33024ce7002975848a98ff8bdfd6188196a96e6f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687910"
---
# <span data-ttu-id="0a661-101">Undo-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="0a661-101">Undo-AzureKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="0a661-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0a661-102">SYNOPSIS</span></span>
<span data-ttu-id="0a661-103">Recuperare un certificato eliminato in un Vault chiave in uno stato attivo.</span><span class="sxs-lookup"><span data-stu-id="0a661-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a661-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0a661-104">SYNTAX</span></span>

### <span data-ttu-id="0a661-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0a661-105">Default (Default)</span></span>
```
Undo-AzureKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a661-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="0a661-106">InputObject</span></span>
```
Undo-AzureKeyVaultCertificateRemoval [-InputObject] <PSDeletedKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a661-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0a661-107">DESCRIPTION</span></span>
<span data-ttu-id="0a661-108">Il cmdlet **Undo-AzureKeyVaultCertificateRemoval** recupererà un certificato eliminato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="0a661-108">The **Undo-AzureKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="0a661-109">Il certificato recuperato sarà attivo e potrà essere usato per tutte le operazioni.</span><span class="sxs-lookup"><span data-stu-id="0a661-109">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="0a661-110">Per eseguire questa operazione, il chiamante deve avere l'autorizzazione "Recupera".</span><span class="sxs-lookup"><span data-stu-id="0a661-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="0a661-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0a661-111">EXAMPLES</span></span>

### <span data-ttu-id="0a661-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0a661-112">Example 1</span></span>
```
PS C:\> Undo-AzureKeyVaultCertificateRemoval -VaultName 'MyKeyVault' -Name 'MyCertificate'
```

<span data-ttu-id="0a661-113">Questo comando recupererà il certificato "certificato" eliminato in precedenza in uno stato attivo e utilizzabile.</span><span class="sxs-lookup"><span data-stu-id="0a661-113">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="0a661-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0a661-114">PARAMETERS</span></span>

### <span data-ttu-id="0a661-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a661-115">-DefaultProfile</span></span>
<span data-ttu-id="0a661-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0a661-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0a661-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a661-117">-InputObject</span></span>
<span data-ttu-id="0a661-118">Oggetto certificato eliminato</span><span class="sxs-lookup"><span data-stu-id="0a661-118">Deleted Certificate object</span></span>

```yaml
Type: PSDeletedKeyVaultCertificateIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a661-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="0a661-119">-Name</span></span>
<span data-ttu-id="0a661-120">Nome certificato.</span><span class="sxs-lookup"><span data-stu-id="0a661-120">Certificate name.</span></span>
<span data-ttu-id="0a661-121">Cmdlet costruisce il nome di dominio completo di un certificato dal nome del Vault, dall'ambiente selezionato e dall'attuale certificato.</span><span class="sxs-lookup"><span data-stu-id="0a661-121">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a661-122">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="0a661-122">-VaultName</span></span>
<span data-ttu-id="0a661-123">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="0a661-123">Vault name.</span></span>
<span data-ttu-id="0a661-124">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="0a661-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="0a661-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0a661-125">-Confirm</span></span>
<span data-ttu-id="0a661-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a661-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a661-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a661-127">-WhatIf</span></span>
<span data-ttu-id="0a661-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0a661-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a661-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0a661-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a661-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a661-130">CommonParameters</span></span>
<span data-ttu-id="0a661-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a661-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a661-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a661-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a661-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0a661-133">INPUTS</span></span>

### <span data-ttu-id="0a661-134">System. String</span><span class="sxs-lookup"><span data-stu-id="0a661-134">System.String</span></span>

## <span data-ttu-id="0a661-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0a661-135">OUTPUTS</span></span>

### <span data-ttu-id="0a661-136">Microsoft. Azure. Commands. Vault. Models. CertificateBundle</span><span class="sxs-lookup"><span data-stu-id="0a661-136">Microsoft.Azure.Commands.KeyVault.Models.CertificateBundle</span></span>

## <span data-ttu-id="0a661-137">Note</span><span class="sxs-lookup"><span data-stu-id="0a661-137">NOTES</span></span>

## <span data-ttu-id="0a661-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0a661-138">RELATED LINKS</span></span>

[<span data-ttu-id="0a661-139">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="0a661-139">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)

[<span data-ttu-id="0a661-140">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="0a661-140">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)
