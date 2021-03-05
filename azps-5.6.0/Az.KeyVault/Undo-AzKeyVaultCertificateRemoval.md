---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/undo-azkeyvaultcertificateremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultCertificateRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultCertificateRemoval.md
ms.openlocfilehash: e514ded413eaca5ae5992e452a6b35f78ab6532b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991085"
---
# <span data-ttu-id="8599b-101">Undo-AzKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="8599b-101">Undo-AzKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="8599b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8599b-102">SYNOPSIS</span></span>
<span data-ttu-id="8599b-103">Recupera un certificato eliminato in uno stato attivo in un vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="8599b-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

## <span data-ttu-id="8599b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8599b-104">SYNTAX</span></span>

### <span data-ttu-id="8599b-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8599b-105">Default (Default)</span></span>
```
Undo-AzKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8599b-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="8599b-106">InputObject</span></span>
```
Undo-AzKeyVaultCertificateRemoval [-InputObject] <PSDeletedKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8599b-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8599b-107">DESCRIPTION</span></span>
<span data-ttu-id="8599b-108">Il cmdlet **Undo-AzKeyVaultCertificateRemoval** recupera un certificato eliminato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="8599b-108">The **Undo-AzKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="8599b-109">Il certificato recuperato sarà attivo e può essere usato per tutte le operazioni.</span><span class="sxs-lookup"><span data-stu-id="8599b-109">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="8599b-110">Per eseguire questa operazione, il chiamante deve avere l'autorizzazione di recupero.</span><span class="sxs-lookup"><span data-stu-id="8599b-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="8599b-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8599b-111">EXAMPLES</span></span>

### <span data-ttu-id="8599b-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8599b-112">Example 1</span></span>
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

<span data-ttu-id="8599b-113">Questo comando recupererà il certificato 'MyCertificate' eliminato in precedenza, in uno stato attivo e utilizzabile.</span><span class="sxs-lookup"><span data-stu-id="8599b-113">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="8599b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8599b-114">PARAMETERS</span></span>

### <span data-ttu-id="8599b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8599b-115">-DefaultProfile</span></span>
<span data-ttu-id="8599b-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8599b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8599b-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8599b-117">-InputObject</span></span>
<span data-ttu-id="8599b-118">Oggetto Certificato eliminato</span><span class="sxs-lookup"><span data-stu-id="8599b-118">Deleted Certificate object</span></span>

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

### <span data-ttu-id="8599b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="8599b-119">-Name</span></span>
<span data-ttu-id="8599b-120">Nome certificato.</span><span class="sxs-lookup"><span data-stu-id="8599b-120">Certificate name.</span></span>
<span data-ttu-id="8599b-121">Il cmdlet crea l'FQDN di un certificato dal nome del vault, l'ambiente attualmente selezionato e il nome del certificato.</span><span class="sxs-lookup"><span data-stu-id="8599b-121">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

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

### <span data-ttu-id="8599b-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8599b-122">-VaultName</span></span>
<span data-ttu-id="8599b-123">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="8599b-123">Vault name.</span></span>
<span data-ttu-id="8599b-124">Il cmdlet crea l'FQDN di un vault in base al nome e all'ambiente attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="8599b-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="8599b-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8599b-125">-Confirm</span></span>
<span data-ttu-id="8599b-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8599b-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8599b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8599b-127">-WhatIf</span></span>
<span data-ttu-id="8599b-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8599b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8599b-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8599b-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8599b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8599b-130">CommonParameters</span></span>
<span data-ttu-id="8599b-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8599b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8599b-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8599b-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8599b-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="8599b-133">INPUTS</span></span>

### <span data-ttu-id="8599b-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="8599b-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="8599b-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8599b-135">OUTPUTS</span></span>

### <span data-ttu-id="8599b-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="8599b-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="8599b-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="8599b-137">NOTES</span></span>

## <span data-ttu-id="8599b-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8599b-138">RELATED LINKS</span></span>

[<span data-ttu-id="8599b-139">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="8599b-139">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="8599b-140">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="8599b-140">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)
