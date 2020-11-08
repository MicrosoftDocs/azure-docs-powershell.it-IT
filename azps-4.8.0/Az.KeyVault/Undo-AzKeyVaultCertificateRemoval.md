---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultcertificateremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultCertificateRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultCertificateRemoval.md
ms.openlocfilehash: 7e9af7cd775726fc57b78f3fdead20f36dca13cb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189835"
---
# <span data-ttu-id="ab4b8-101">Undo-AzKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="ab4b8-101">Undo-AzKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="ab4b8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ab4b8-102">SYNOPSIS</span></span>
<span data-ttu-id="ab4b8-103">Recuperare un certificato eliminato in un Vault chiave in uno stato attivo.</span><span class="sxs-lookup"><span data-stu-id="ab4b8-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

## <span data-ttu-id="ab4b8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ab4b8-104">SYNTAX</span></span>

### <span data-ttu-id="ab4b8-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ab4b8-105">Default (Default)</span></span>
```
Undo-AzKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab4b8-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ab4b8-106">InputObject</span></span>
```
Undo-AzKeyVaultCertificateRemoval [-InputObject] <PSDeletedKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab4b8-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab4b8-107">DESCRIPTION</span></span>
<span data-ttu-id="ab4b8-108">Il cmdlet **Undo-AzKeyVaultCertificateRemoval** recupererà un certificato eliminato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="ab4b8-108">The **Undo-AzKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="ab4b8-109">Il certificato recuperato sarà attivo e potrà essere usato per tutte le operazioni.</span><span class="sxs-lookup"><span data-stu-id="ab4b8-109">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="ab4b8-110">Per eseguire questa operazione, il chiamante deve avere l'autorizzazione "Recupera".</span><span class="sxs-lookup"><span data-stu-id="ab4b8-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="ab4b8-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ab4b8-111">EXAMPLES</span></span>

### <span data-ttu-id="ab4b8-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ab4b8-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzKeyVaultCertificateRemoval -VaultName 'MyKeyVault' -Name 'MyCertificate'

Certificate   : [Subject]
                  CN=contoso.com

                [Issuer]
                  CN=contoso.com

                [Serial Number]
                  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

                [Not Before]
                  5/24/2018 10:58:13 AM

                [Not After]
                  11/24/2018 10:08:13 AM

                [Thumbprint]
                  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId         : https://mykeyvault.vault.azure.net:443/keys/mycertificate/7fe415d5518240c1a6fce89986b8d334
SecretId      : https://mykeyvault.vault.azure.net:443/secrets/mycertificate/7fe415d5518240c1a6fce89986b8d334
Thumbprint    : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
RecoveryLevel : Recoverable+Purgeable
Enabled       : True
Expires       : 11/24/2018 6:08:13 PM
NotBefore     : 5/24/2018 5:58:13 PM
Created       : 5/24/2018 6:08:13 PM
Updated       : 5/24/2018 6:08:13 PM
Tags          :
VaultName     : MyKeyVault
Name          : MyCertificate
Version       : 7fe415d5518240c1a6fce89986b8d334
Id            : https://mykeyvault.vault.azure.net:443/certificates/mycertificate/7fe415d5518240c1a6fce89986b8d334
```

<span data-ttu-id="ab4b8-113">Questo comando recupererà il certificato "certificato" eliminato in precedenza in uno stato attivo e utilizzabile.</span><span class="sxs-lookup"><span data-stu-id="ab4b8-113">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="ab4b8-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ab4b8-114">PARAMETERS</span></span>

### <span data-ttu-id="ab4b8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab4b8-115">-DefaultProfile</span></span>
<span data-ttu-id="ab4b8-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ab4b8-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ab4b8-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab4b8-117">-InputObject</span></span>
<span data-ttu-id="ab4b8-118">Oggetto certificato eliminato</span><span class="sxs-lookup"><span data-stu-id="ab4b8-118">Deleted Certificate object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab4b8-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="ab4b8-119">-Name</span></span>
<span data-ttu-id="ab4b8-120">Nome certificato.</span><span class="sxs-lookup"><span data-stu-id="ab4b8-120">Certificate name.</span></span>
<span data-ttu-id="ab4b8-121">Cmdlet costruisce il nome di dominio completo di un certificato dal nome del Vault, dall'ambiente selezionato e dall'attuale certificato.</span><span class="sxs-lookup"><span data-stu-id="ab4b8-121">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab4b8-122">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="ab4b8-122">-VaultName</span></span>
<span data-ttu-id="ab4b8-123">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="ab4b8-123">Vault name.</span></span>
<span data-ttu-id="ab4b8-124">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="ab4b8-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="ab4b8-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ab4b8-125">-Confirm</span></span>
<span data-ttu-id="ab4b8-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab4b8-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab4b8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab4b8-127">-WhatIf</span></span>
<span data-ttu-id="ab4b8-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ab4b8-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab4b8-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ab4b8-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab4b8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab4b8-130">CommonParameters</span></span>
<span data-ttu-id="ab4b8-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab4b8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab4b8-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab4b8-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab4b8-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ab4b8-133">INPUTS</span></span>

### <span data-ttu-id="ab4b8-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="ab4b8-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="ab4b8-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ab4b8-135">OUTPUTS</span></span>

### <span data-ttu-id="ab4b8-136">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="ab4b8-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="ab4b8-137">Note</span><span class="sxs-lookup"><span data-stu-id="ab4b8-137">NOTES</span></span>

## <span data-ttu-id="ab4b8-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ab4b8-138">RELATED LINKS</span></span>

[<span data-ttu-id="ab4b8-139">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="ab4b8-139">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="ab4b8-140">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="ab4b8-140">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)
