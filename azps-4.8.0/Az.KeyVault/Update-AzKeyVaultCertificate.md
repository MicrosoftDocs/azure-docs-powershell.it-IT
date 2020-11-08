---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultCertificate.md
ms.openlocfilehash: ee613655f0a7838ba9e16c4b6331a30e9e1b9356
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189662"
---
# <span data-ttu-id="8a781-101">Update-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="8a781-101">Update-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="8a781-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8a781-102">SYNOPSIS</span></span>
<span data-ttu-id="8a781-103">Modifica gli attributi modificabili di un certificato.</span><span class="sxs-lookup"><span data-stu-id="8a781-103">Modifies editable attributes of a certificate.</span></span>

## <span data-ttu-id="8a781-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8a781-104">SYNTAX</span></span>

### <span data-ttu-id="8a781-105">ByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8a781-105">ByName (Default)</span></span>
```
Update-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a781-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8a781-106">ByInputObject</span></span>
```
Update-AzKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-Version] <String>]
 [-Enable <Boolean>] [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a781-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8a781-107">DESCRIPTION</span></span>
<span data-ttu-id="8a781-108">Il cmdlet **Update-AzKeyVaultCertificate** modifica gli attributi modificabili di un certificato.</span><span class="sxs-lookup"><span data-stu-id="8a781-108">The **Update-AzKeyVaultCertificate** cmdlet modifies the editable attributes of a certificate.</span></span>

## <span data-ttu-id="8a781-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8a781-109">EXAMPLES</span></span>

### <span data-ttu-id="8a781-110">Esempio 1: modificare i tag associati a un certificato</span><span class="sxs-lookup"><span data-stu-id="8a781-110">Example 1: Modify the tags associated with a certificate</span></span>
```powershell
PS C:\> $Tags = @{ "Team" = "Azure" ; "Role" = "Engg" }
PS C:\> Update-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01" -Tag $Tags -PassThru

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

<span data-ttu-id="8a781-111">Il primo comando assegna una matrice di coppie chiave/valore alla variabile $Tags.</span><span class="sxs-lookup"><span data-stu-id="8a781-111">The first command assigns an array of key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="8a781-112">Il secondo comando imposta il valore di tag del certificato denominato TestCert01 $Tags.</span><span class="sxs-lookup"><span data-stu-id="8a781-112">The second command sets the tags value of the certificate named TestCert01 to be $Tags.</span></span>

### <span data-ttu-id="8a781-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="8a781-113">Example 2</span></span>

<span data-ttu-id="8a781-114">Modifica gli attributi modificabili di un certificato.</span><span class="sxs-lookup"><span data-stu-id="8a781-114">Modifies editable attributes of a certificate.</span></span> <span data-ttu-id="8a781-115">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="8a781-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Update-AzKeyVaultCertificate -Enable $true -Name 'TestCert01' -VaultName 'ContosoKV01'
```

## <span data-ttu-id="8a781-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8a781-116">PARAMETERS</span></span>

### <span data-ttu-id="8a781-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a781-117">-DefaultProfile</span></span>
<span data-ttu-id="8a781-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8a781-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a781-119">-Enable</span><span class="sxs-lookup"><span data-stu-id="8a781-119">-Enable</span></span>
<span data-ttu-id="8a781-120">Se presente, abilitare un certificato se il valore è vero.</span><span class="sxs-lookup"><span data-stu-id="8a781-120">If present, enable a certificate if value is true.</span></span>
<span data-ttu-id="8a781-121">Disabilitare un certificato se il valore è false.</span><span class="sxs-lookup"><span data-stu-id="8a781-121">Disable a certificate if value is false.</span></span>
<span data-ttu-id="8a781-122">Se non specificato, il valore esistente dello stato abilitato/disabilitato del certificato rimane invariato.</span><span class="sxs-lookup"><span data-stu-id="8a781-122">If not specified, the existing value of the certificate's enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="8a781-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a781-123">-InputObject</span></span>
<span data-ttu-id="8a781-124">Oggetto certificato</span><span class="sxs-lookup"><span data-stu-id="8a781-124">Certificate object</span></span>

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

### <span data-ttu-id="8a781-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="8a781-125">-Name</span></span>
<span data-ttu-id="8a781-126">Nome certificato.</span><span class="sxs-lookup"><span data-stu-id="8a781-126">Certificate name.</span></span>
<span data-ttu-id="8a781-127">Cmdlet costruisce il nome di dominio completo di un segreto dal nome della volta, dall'ambiente selezionato e da quello segreto.</span><span class="sxs-lookup"><span data-stu-id="8a781-127">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="8a781-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8a781-128">-PassThru</span></span>
<span data-ttu-id="8a781-129">Cmdlet non restituisce Object per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="8a781-129">Cmdlet does not return object by default.</span></span>
<span data-ttu-id="8a781-130">Se questa opzione è specificata, restituire l'oggetto certificato.</span><span class="sxs-lookup"><span data-stu-id="8a781-130">If this switch is specified, return certificate object.</span></span>

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

### <span data-ttu-id="8a781-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="8a781-131">-Tag</span></span>
<span data-ttu-id="8a781-132">Hashtable che rappresenta i tag di certificato.</span><span class="sxs-lookup"><span data-stu-id="8a781-132">A hashtable representing certificate tags.</span></span>
<span data-ttu-id="8a781-133">Se non specificato, i tag esistenti di Sertificate rimarranno invariati.</span><span class="sxs-lookup"><span data-stu-id="8a781-133">If not specified, the existing tags of the sertificate remain unchanged.</span></span>
<span data-ttu-id="8a781-134">Rimuovere un contrassegno specificando una tabella hash vuota.</span><span class="sxs-lookup"><span data-stu-id="8a781-134">Remove a tag by specifying an empty Hashtable.</span></span>

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

### <span data-ttu-id="8a781-135">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="8a781-135">-VaultName</span></span>
<span data-ttu-id="8a781-136">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="8a781-136">Vault name.</span></span>
<span data-ttu-id="8a781-137">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="8a781-137">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="8a781-138">-Versione</span><span class="sxs-lookup"><span data-stu-id="8a781-138">-Version</span></span>
<span data-ttu-id="8a781-139">Versione del certificato.</span><span class="sxs-lookup"><span data-stu-id="8a781-139">Certificate version.</span></span>
<span data-ttu-id="8a781-140">Cmdlet costruisce l'FQDN di un certificato dal nome del Vault, l'ambiente attualmente selezionato, il nome del certificato e la versione del certificato.</span><span class="sxs-lookup"><span data-stu-id="8a781-140">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment, certificate name and certificate version.</span></span>

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

### <span data-ttu-id="8a781-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8a781-141">-Confirm</span></span>
<span data-ttu-id="8a781-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a781-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a781-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a781-143">-WhatIf</span></span>
<span data-ttu-id="8a781-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8a781-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a781-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8a781-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a781-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a781-146">CommonParameters</span></span>
<span data-ttu-id="8a781-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a781-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a781-148">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a781-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a781-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8a781-149">INPUTS</span></span>

### <span data-ttu-id="8a781-150">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="8a781-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="8a781-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8a781-151">OUTPUTS</span></span>

### <span data-ttu-id="8a781-152">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="8a781-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="8a781-153">Note</span><span class="sxs-lookup"><span data-stu-id="8a781-153">NOTES</span></span>

## <span data-ttu-id="8a781-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8a781-154">RELATED LINKS</span></span>