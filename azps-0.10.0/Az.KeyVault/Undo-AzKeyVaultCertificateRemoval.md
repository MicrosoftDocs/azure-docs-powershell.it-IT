---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/undo-AzKeyvaultcertificateremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultCertificateRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultCertificateRemoval.md
ms.openlocfilehash: 5757a9fb050d69cdf0ef0e648b0d446de1e3ee24
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861242"
---
# <span data-ttu-id="37c0b-101">Undo-AzKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="37c0b-101">Undo-AzKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="37c0b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="37c0b-102">SYNOPSIS</span></span>
<span data-ttu-id="37c0b-103">Recuperare un certificato eliminato in un Vault chiave in uno stato attivo.</span><span class="sxs-lookup"><span data-stu-id="37c0b-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

## <span data-ttu-id="37c0b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="37c0b-104">SYNTAX</span></span>

```
Undo-AzKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37c0b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="37c0b-105">DESCRIPTION</span></span>
<span data-ttu-id="37c0b-106">Il cmdlet **Undo-AzKeyVaultCertificateRemoval** recupererà un certificato eliminato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="37c0b-106">The **Undo-AzKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="37c0b-107">Il certificato recuperato sarà attivo e potrà essere usato per tutte le operazioni.</span><span class="sxs-lookup"><span data-stu-id="37c0b-107">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="37c0b-108">Per eseguire questa operazione, il chiamante deve avere l'autorizzazione "Recupera".</span><span class="sxs-lookup"><span data-stu-id="37c0b-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="37c0b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="37c0b-109">EXAMPLES</span></span>

### <span data-ttu-id="37c0b-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="37c0b-110">Example 1</span></span>
```
PS C:\> Undo-AzKeyVaultCertificateRemoval -VaultName 'MyKeyVault' -Name 'MyCertificate'
```

<span data-ttu-id="37c0b-111">Questo comando recupererà il certificato "certificato" eliminato in precedenza in uno stato attivo e utilizzabile.</span><span class="sxs-lookup"><span data-stu-id="37c0b-111">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="37c0b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="37c0b-112">PARAMETERS</span></span>

### <span data-ttu-id="37c0b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37c0b-113">-DefaultProfile</span></span>
<span data-ttu-id="37c0b-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="37c0b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37c0b-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="37c0b-115">-Name</span></span>
<span data-ttu-id="37c0b-116">Nome certificato.</span><span class="sxs-lookup"><span data-stu-id="37c0b-116">Certificate name.</span></span>
<span data-ttu-id="37c0b-117">Cmdlet costruisce il nome di dominio completo di un certificato dal nome del Vault, dall'ambiente selezionato e dall'attuale certificato.</span><span class="sxs-lookup"><span data-stu-id="37c0b-117">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

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

### <span data-ttu-id="37c0b-118">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="37c0b-118">-VaultName</span></span>
<span data-ttu-id="37c0b-119">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="37c0b-119">Vault name.</span></span>
<span data-ttu-id="37c0b-120">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="37c0b-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="37c0b-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="37c0b-121">-Confirm</span></span>
<span data-ttu-id="37c0b-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37c0b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37c0b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37c0b-123">-WhatIf</span></span>
<span data-ttu-id="37c0b-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="37c0b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37c0b-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="37c0b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37c0b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37c0b-126">CommonParameters</span></span>
<span data-ttu-id="37c0b-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37c0b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37c0b-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37c0b-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37c0b-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="37c0b-129">INPUTS</span></span>

### <span data-ttu-id="37c0b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="37c0b-130">System.String</span></span>

## <span data-ttu-id="37c0b-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="37c0b-131">OUTPUTS</span></span>

### <span data-ttu-id="37c0b-132">Microsoft. Azure. Commands. Vault. Models. Certificate</span><span class="sxs-lookup"><span data-stu-id="37c0b-132">Microsoft.Azure.Commands.KeyVault.Models.Certificate</span></span>

## <span data-ttu-id="37c0b-133">Note</span><span class="sxs-lookup"><span data-stu-id="37c0b-133">NOTES</span></span>

## <span data-ttu-id="37c0b-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="37c0b-134">RELATED LINKS</span></span>

[<span data-ttu-id="37c0b-135">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="37c0b-135">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="37c0b-136">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="37c0b-136">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)
