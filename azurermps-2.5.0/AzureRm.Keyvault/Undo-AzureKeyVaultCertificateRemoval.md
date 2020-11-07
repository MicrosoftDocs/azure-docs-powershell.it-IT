---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultcertificateremoval
schema: 2.0.0
ms.openlocfilehash: 493d4bcd641e8132bffd49100a04732759ce7e91
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866329"
---
# <span data-ttu-id="b03a1-101">Undo-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="b03a1-101">Undo-AzureKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="b03a1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b03a1-102">SYNOPSIS</span></span>
<span data-ttu-id="b03a1-103">Recuperare un certificato eliminato in un Vault chiave in uno stato attivo.</span><span class="sxs-lookup"><span data-stu-id="b03a1-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b03a1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b03a1-104">SYNTAX</span></span>

```
Undo-AzureKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b03a1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b03a1-105">DESCRIPTION</span></span>
<span data-ttu-id="b03a1-106">Il cmdlet **Undo-AzureKeyVaultCertificateRemoval** recupererà un certificato eliminato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="b03a1-106">The **Undo-AzureKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="b03a1-107">Il certificato recuperato sarà attivo e potrà essere usato per tutte le operazioni.</span><span class="sxs-lookup"><span data-stu-id="b03a1-107">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="b03a1-108">Per eseguire questa operazione, il chiamante deve avere l'autorizzazione "Recupera".</span><span class="sxs-lookup"><span data-stu-id="b03a1-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="b03a1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b03a1-109">EXAMPLES</span></span>

### <span data-ttu-id="b03a1-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b03a1-110">Example 1</span></span>
```
PS C:\> Undo-AzureKeyVaultCertificateRemoval -VaultName 'MyKeyVault' -Name 'MyCertificate'
```

<span data-ttu-id="b03a1-111">Questo comando recupererà il certificato "certificato" eliminato in precedenza in uno stato attivo e utilizzabile.</span><span class="sxs-lookup"><span data-stu-id="b03a1-111">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="b03a1-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b03a1-112">PARAMETERS</span></span>

### <span data-ttu-id="b03a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b03a1-113">-DefaultProfile</span></span>
<span data-ttu-id="b03a1-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b03a1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b03a1-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="b03a1-115">-Name</span></span>
<span data-ttu-id="b03a1-116">Nome certificato.</span><span class="sxs-lookup"><span data-stu-id="b03a1-116">Certificate name.</span></span>
<span data-ttu-id="b03a1-117">Cmdlet costruisce il nome di dominio completo di un certificato dal nome del Vault, dall'ambiente selezionato e dall'attuale certificato.</span><span class="sxs-lookup"><span data-stu-id="b03a1-117">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b03a1-118">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="b03a1-118">-VaultName</span></span>
<span data-ttu-id="b03a1-119">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="b03a1-119">Vault name.</span></span>
<span data-ttu-id="b03a1-120">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="b03a1-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="b03a1-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b03a1-121">-Confirm</span></span>
<span data-ttu-id="b03a1-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b03a1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b03a1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b03a1-123">-WhatIf</span></span>
<span data-ttu-id="b03a1-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b03a1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b03a1-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b03a1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b03a1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b03a1-126">CommonParameters</span></span>
<span data-ttu-id="b03a1-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b03a1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b03a1-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b03a1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b03a1-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b03a1-129">INPUTS</span></span>

### <span data-ttu-id="b03a1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b03a1-130">System.String</span></span>

## <span data-ttu-id="b03a1-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b03a1-131">OUTPUTS</span></span>

### <span data-ttu-id="b03a1-132">Microsoft. Azure. Commands. Vault. Models. Certificate</span><span class="sxs-lookup"><span data-stu-id="b03a1-132">Microsoft.Azure.Commands.KeyVault.Models.Certificate</span></span>

## <span data-ttu-id="b03a1-133">Note</span><span class="sxs-lookup"><span data-stu-id="b03a1-133">NOTES</span></span>

## <span data-ttu-id="b03a1-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b03a1-134">RELATED LINKS</span></span>

[<span data-ttu-id="b03a1-135">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b03a1-135">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)

[<span data-ttu-id="b03a1-136">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b03a1-136">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)
