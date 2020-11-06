---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultCertificateRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultCertificateRemoval.md
ms.openlocfilehash: 91fee65a201de8babc7ef7aa09973f1e98f95cb9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521206"
---
# <span data-ttu-id="fbee0-101">Undo-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="fbee0-101">Undo-AzureKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="fbee0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fbee0-102">SYNOPSIS</span></span>
<span data-ttu-id="fbee0-103">Recuperare un certificato eliminato in un Vault chiave in uno stato attivo.</span><span class="sxs-lookup"><span data-stu-id="fbee0-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fbee0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fbee0-104">SYNTAX</span></span>

```
Undo-AzureKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbee0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fbee0-105">DESCRIPTION</span></span>
<span data-ttu-id="fbee0-106">Il cmdlet **Undo-AzureKeyVaultCertificateRemoval** recupererà un certificato eliminato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="fbee0-106">The **Undo-AzureKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="fbee0-107">Il certificato recuperato sarà attivo e potrà essere usato per tutte le operazioni.</span><span class="sxs-lookup"><span data-stu-id="fbee0-107">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="fbee0-108">Per eseguire questa operazione, il chiamante deve avere l'autorizzazione "Recupera".</span><span class="sxs-lookup"><span data-stu-id="fbee0-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="fbee0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fbee0-109">EXAMPLES</span></span>

### <span data-ttu-id="fbee0-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fbee0-110">Example 1</span></span>
```
PS C:\> Undo-AzureKeyVaultCertificateRemoval -VaultName 'MyKeyVault' -Name 'MyCertificate'
```

<span data-ttu-id="fbee0-111">Questo comando recupererà il certificato "certificato" eliminato in precedenza in uno stato attivo e utilizzabile.</span><span class="sxs-lookup"><span data-stu-id="fbee0-111">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="fbee0-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fbee0-112">PARAMETERS</span></span>

### <span data-ttu-id="fbee0-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="fbee0-113">-Name</span></span>
<span data-ttu-id="fbee0-114">Nome certificato.</span><span class="sxs-lookup"><span data-stu-id="fbee0-114">Certificate name.</span></span>
<span data-ttu-id="fbee0-115">Cmdlet costruisce il nome di dominio completo di un certificato dal nome del Vault, dall'ambiente selezionato e dall'attuale certificato.</span><span class="sxs-lookup"><span data-stu-id="fbee0-115">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbee0-116">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="fbee0-116">-VaultName</span></span>
<span data-ttu-id="fbee0-117">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="fbee0-117">Vault name.</span></span>
<span data-ttu-id="fbee0-118">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="fbee0-118">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="fbee0-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fbee0-119">-Confirm</span></span>
<span data-ttu-id="fbee0-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbee0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbee0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbee0-121">-WhatIf</span></span>
<span data-ttu-id="fbee0-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fbee0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbee0-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fbee0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbee0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbee0-124">-DefaultProfile</span></span>
<span data-ttu-id="fbee0-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fbee0-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fbee0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbee0-126">CommonParameters</span></span>
<span data-ttu-id="fbee0-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbee0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbee0-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbee0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbee0-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fbee0-129">INPUTS</span></span>

### <span data-ttu-id="fbee0-130">System. String</span><span class="sxs-lookup"><span data-stu-id="fbee0-130">System.String</span></span>

## <span data-ttu-id="fbee0-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fbee0-131">OUTPUTS</span></span>

### <span data-ttu-id="fbee0-132">Microsoft. Azure. Commands. Vault. Models. Certificate</span><span class="sxs-lookup"><span data-stu-id="fbee0-132">Microsoft.Azure.Commands.KeyVault.Models.Certificate</span></span>

## <span data-ttu-id="fbee0-133">Note</span><span class="sxs-lookup"><span data-stu-id="fbee0-133">NOTES</span></span>

## <span data-ttu-id="fbee0-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fbee0-134">RELATED LINKS</span></span>

[<span data-ttu-id="fbee0-135">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="fbee0-135">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)

[<span data-ttu-id="fbee0-136">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="fbee0-136">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)
