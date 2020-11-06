---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/update-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultCertificate.md
ms.openlocfilehash: 732d8dc7cfe3c0f8a3bec6eb3157b65bc8437e44
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515183"
---
# <span data-ttu-id="f0992-101">Update-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="f0992-101">Update-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="f0992-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f0992-102">SYNOPSIS</span></span>
<span data-ttu-id="f0992-103">Modifica gli attributi modificabili di un certificato.</span><span class="sxs-lookup"><span data-stu-id="f0992-103">Modifies editable attributes of a certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0992-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f0992-104">SYNTAX</span></span>

### <span data-ttu-id="f0992-105">ByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f0992-105">ByName (Default)</span></span>
```
Update-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0992-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f0992-106">ByInputObject</span></span>
```
Update-AzureKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-Version] <String>]
 [-Enable <Boolean>] [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0992-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f0992-107">DESCRIPTION</span></span>
<span data-ttu-id="f0992-108">Il cmdlet **Update-AzureKeyVaultCertificate** modifica gli attributi modificabili di un certificato.</span><span class="sxs-lookup"><span data-stu-id="f0992-108">The **Update-AzureKeyVaultCertificate** cmdlet modifies the editable attributes of a certificate.</span></span>

## <span data-ttu-id="f0992-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f0992-109">EXAMPLES</span></span>

### <span data-ttu-id="f0992-110">Esempio 1: modificare i tag associati a un certificato</span><span class="sxs-lookup"><span data-stu-id="f0992-110">Example 1: Modify the tags associated with a certificate</span></span>
```powershell
PS C:\> $Tags = @{ "Team" = "Azure" ; "Role" = "Engg" }
PS C:\> Update-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01" -Tag $Tags -PassThru

Name        : TestCert01
Certificate : [Subject]
                CN=AZURE

              [Issuer]
                CN=AZURE

              [Serial Number]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

              [Not Before]
                7/27/2016 6:50:01 PM

              [Not After]
                7/27/2018 7:00:01 PM

              [Thumbprint]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

Id          : https://ContosoKV01.vault.azure.net:443/certificates/TestCert01
KeyId       : https://ContosoKV01.vault.azure.net:443/keys/TestCert01
SecretId    : https://ContosoKV01.vault.azure.net:443/secrets/TestCert01
Thumbprint  : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Tags        : {[Role, Engg], [Team, Azure]}
Enabled     : True
Created     : 7/28/2016 2:00:01 AM
Updated     : 8/1/2016 5:37:48 PM
```

<span data-ttu-id="f0992-111">Il primo comando assegna una matrice di coppie chiave/valore alla variabile $Tags.</span><span class="sxs-lookup"><span data-stu-id="f0992-111">The first command assigns an array of key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="f0992-112">Il secondo comando imposta il valore di tag del certificato denominato TestCert01 $Tags.</span><span class="sxs-lookup"><span data-stu-id="f0992-112">The second command sets the tags value of the certificate named TestCert01 to be $Tags.</span></span>

## <span data-ttu-id="f0992-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f0992-113">PARAMETERS</span></span>

### <span data-ttu-id="f0992-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0992-114">-DefaultProfile</span></span>
<span data-ttu-id="f0992-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f0992-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0992-116">-Enable</span><span class="sxs-lookup"><span data-stu-id="f0992-116">-Enable</span></span>
<span data-ttu-id="f0992-117">Se presente, abilitare un certificato se il valore è vero.</span><span class="sxs-lookup"><span data-stu-id="f0992-117">If present, enable a certificate if value is true.</span></span>
<span data-ttu-id="f0992-118">Disabilitare un certificato se il valore è false.</span><span class="sxs-lookup"><span data-stu-id="f0992-118">Disable a certificate if value is false.</span></span>
<span data-ttu-id="f0992-119">Se non specificato, il valore esistente dello stato abilitato/disabilitato del certificato rimane invariato.</span><span class="sxs-lookup"><span data-stu-id="f0992-119">If not specified, the existing value of the certificate's enabled/disabled state remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0992-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0992-120">-InputObject</span></span>
<span data-ttu-id="f0992-121">Oggetto certificato</span><span class="sxs-lookup"><span data-stu-id="f0992-121">Certificate object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0992-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="f0992-122">-Name</span></span>
<span data-ttu-id="f0992-123">Nome certificato.</span><span class="sxs-lookup"><span data-stu-id="f0992-123">Certificate name.</span></span>
<span data-ttu-id="f0992-124">Cmdlet costruisce il nome di dominio completo di un segreto dal nome della volta, dall'ambiente selezionato e da quello segreto.</span><span class="sxs-lookup"><span data-stu-id="f0992-124">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0992-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0992-125">-PassThru</span></span>
<span data-ttu-id="f0992-126">Cmdlet non restituisce Object per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="f0992-126">Cmdlet does not return object by default.</span></span>
<span data-ttu-id="f0992-127">Se questa opzione è specificata, restituire l'oggetto certificato.</span><span class="sxs-lookup"><span data-stu-id="f0992-127">If this switch is specified, return certificate object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0992-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="f0992-128">-Tag</span></span>
<span data-ttu-id="f0992-129">Hashtable che rappresenta i tag di certificato.</span><span class="sxs-lookup"><span data-stu-id="f0992-129">A hashtable representing certificate tags.</span></span>
<span data-ttu-id="f0992-130">Se non specificato, i tag esistenti di Sertificate rimarranno invariati.</span><span class="sxs-lookup"><span data-stu-id="f0992-130">If not specified, the existing tags of the sertificate remain unchanged.</span></span>
<span data-ttu-id="f0992-131">Rimuovere un contrassegno specificando una tabella hash vuota.</span><span class="sxs-lookup"><span data-stu-id="f0992-131">Remove a tag by specifying an empty Hashtable.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0992-132">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="f0992-132">-VaultName</span></span>
<span data-ttu-id="f0992-133">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="f0992-133">Vault name.</span></span>
<span data-ttu-id="f0992-134">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="f0992-134">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0992-135">-Versione</span><span class="sxs-lookup"><span data-stu-id="f0992-135">-Version</span></span>
<span data-ttu-id="f0992-136">Versione del certificato.</span><span class="sxs-lookup"><span data-stu-id="f0992-136">Certificate version.</span></span>
<span data-ttu-id="f0992-137">Cmdlet costruisce l'FQDN di un certificato dal nome del Vault, l'ambiente attualmente selezionato, il nome del certificato e la versione del certificato.</span><span class="sxs-lookup"><span data-stu-id="f0992-137">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment, certificate name and certificate version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0992-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f0992-138">-Confirm</span></span>
<span data-ttu-id="f0992-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0992-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0992-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0992-140">-WhatIf</span></span>
<span data-ttu-id="f0992-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f0992-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0992-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f0992-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0992-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0992-143">CommonParameters</span></span>
<span data-ttu-id="f0992-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0992-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0992-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0992-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0992-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f0992-146">INPUTS</span></span>

### <span data-ttu-id="f0992-147">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="f0992-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>
<span data-ttu-id="f0992-148">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f0992-148">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="f0992-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f0992-149">OUTPUTS</span></span>

### <span data-ttu-id="f0992-150">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="f0992-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="f0992-151">Note</span><span class="sxs-lookup"><span data-stu-id="f0992-151">NOTES</span></span>

## <span data-ttu-id="f0992-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f0992-152">RELATED LINKS</span></span>
