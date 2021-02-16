---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: D4188DC6-A8AB-4B45-9781-94B74C338C63
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/import-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultCertificate.md
ms.openlocfilehash: 6a687f67741a8d4925e3253c9f787532501ad186
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209314"
---
# <span data-ttu-id="014f5-101">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="014f5-101">Import-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="014f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="014f5-102">SYNOPSIS</span></span>
<span data-ttu-id="014f5-103">Importa un certificato in un vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="014f5-103">Imports a certificate to a key vault.</span></span>

## <span data-ttu-id="014f5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="014f5-104">SYNTAX</span></span>

### <span data-ttu-id="014f5-105">ImportCertificateFromFile (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="014f5-105">ImportCertificateFromFile (Default)</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> -FilePath <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="014f5-106">ImportWithPrivateKeyFromString</span><span class="sxs-lookup"><span data-stu-id="014f5-106">ImportWithPrivateKeyFromString</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> -CertificateString <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="014f5-107">ImportWithPrivateKeyFromCollection</span><span class="sxs-lookup"><span data-stu-id="014f5-107">ImportWithPrivateKeyFromCollection</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 [-CertificateCollection] <X509Certificate2Collection> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="014f5-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="014f5-108">DESCRIPTION</span></span>
<span data-ttu-id="014f5-109">Il cmdlet **Import-AzKeyVaultCertificate** importa un certificato in un vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="014f5-109">The **Import-AzKeyVaultCertificate** cmdlet imports a certificate into a key vault.</span></span>
<span data-ttu-id="014f5-110">È possibile creare il certificato da importare usando uno dei metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="014f5-110">You can create the certificate to import by using one of the following methods:</span></span>
- <span data-ttu-id="014f5-111">Consente `Add-AzKeyVaultCertificate` di creare una richiesta di firma del certificato e inviarla a un'autorità di certificazione.</span><span class="sxs-lookup"><span data-stu-id="014f5-111">Use `Add-AzKeyVaultCertificate` to create a certificate signing request and submit it to a certificate authority.</span></span> <span data-ttu-id="014f5-112">Vedi https://docs.microsoft.com/en-us/azure/key-vault/certificates/create-certificate-signing-request</span><span class="sxs-lookup"><span data-stu-id="014f5-112">See https://docs.microsoft.com/en-us/azure/key-vault/certificates/create-certificate-signing-request</span></span>
- <span data-ttu-id="014f5-113">Usare un file del pacchetto di certificati esistente, ad esempio un file PFX o P12, che contiene sia il certificato che la chiave privata.</span><span class="sxs-lookup"><span data-stu-id="014f5-113">Use an existing certificate package file, such as a .pfx or .p12 file, which contains both the certificate and private key.</span></span>

## <span data-ttu-id="014f5-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="014f5-114">EXAMPLES</span></span>

### <span data-ttu-id="014f5-115">Esempio 1: Importare un certificato vault chiave</span><span class="sxs-lookup"><span data-stu-id="014f5-115">Example 1: Import a key vault certificate</span></span>
```powershell
PS C:\> $Password = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS C:\> Import-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "ImportCert01" -FilePath "C:\Users\contosoUser\Desktop\import.pfx" -Password $Password

Name        : importCert01
Certificate : [Subject]
                CN=contoso.com

              [Issuer]
                CN=contoso.com

              [Serial Number]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

              [Not Before]
                2/8/2016 3:11:45 PM

              [Not After]
                8/8/2016 4:21:45 PM

              [Thumbprint]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

Thumbprint  : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Tags        :
Enabled     : True
Created     : 2/8/2016 11:50:43 PM
Updated     : 2/8/2016 11:50:43 PM
```

<span data-ttu-id="014f5-116">Il primo comando usa il cmdlet ConvertTo-SecureString per creare una password sicura e quindi la archivia nella $Password variabile.</span><span class="sxs-lookup"><span data-stu-id="014f5-116">The first command uses the ConvertTo-SecureString cmdlet to create a secure password, and then stores it in the $Password variable.</span></span>
<span data-ttu-id="014f5-117">Il secondo comando importa il certificato denominato ImportCert01 nel vault delle chiavi di CosotosoKV01.</span><span class="sxs-lookup"><span data-stu-id="014f5-117">The second command imports the certificate named ImportCert01 into the CosotosoKV01 key vault.</span></span>

## <span data-ttu-id="014f5-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="014f5-118">PARAMETERS</span></span>

### <span data-ttu-id="014f5-119">-CertificateCollection</span><span class="sxs-lookup"><span data-stu-id="014f5-119">-CertificateCollection</span></span>
<span data-ttu-id="014f5-120">Specifica la raccolta di certificati da aggiungere a un vault chiave.</span><span class="sxs-lookup"><span data-stu-id="014f5-120">Specifies the certificate collection to add to a key vault.</span></span>

```yaml
Type: System.Security.Cryptography.X509Certificates.X509Certificate2Collection
Parameter Sets: ImportWithPrivateKeyFromCollection
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="014f5-121">-CertificateString</span><span class="sxs-lookup"><span data-stu-id="014f5-121">-CertificateString</span></span>
<span data-ttu-id="014f5-122">Specifica una stringa di certificato.</span><span class="sxs-lookup"><span data-stu-id="014f5-122">Specifies a certificate string.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportWithPrivateKeyFromString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="014f5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="014f5-123">-DefaultProfile</span></span>
<span data-ttu-id="014f5-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="014f5-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="014f5-125">-FilePath</span><span class="sxs-lookup"><span data-stu-id="014f5-125">-FilePath</span></span>
<span data-ttu-id="014f5-126">Specifica il percorso del file di certificato importato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="014f5-126">Specifies the path of the certificate file that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportCertificateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="014f5-127">-Name</span><span class="sxs-lookup"><span data-stu-id="014f5-127">-Name</span></span>
<span data-ttu-id="014f5-128">Specifica il nome del certificato.</span><span class="sxs-lookup"><span data-stu-id="014f5-128">Specifies the certificate name.</span></span> <span data-ttu-id="014f5-129">Questo cmdlet crea il nome di dominio completo (FQDN) di un certificato dal nome vault della chiave, l'ambiente attualmente selezionato e il nome del certificato.</span><span class="sxs-lookup"><span data-stu-id="014f5-129">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate from key vault name, currently selected environment, and certificate name.</span></span>

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

### <span data-ttu-id="014f5-130">-Password</span><span class="sxs-lookup"><span data-stu-id="014f5-130">-Password</span></span>
<span data-ttu-id="014f5-131">Specifica la password per un file di certificato.</span><span class="sxs-lookup"><span data-stu-id="014f5-131">Specifies the password for a certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ImportCertificateFromFile, ImportWithPrivateKeyFromString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="014f5-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="014f5-132">-Tag</span></span>
<span data-ttu-id="014f5-133">Coppie chiave-valore sotto forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="014f5-133">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="014f5-134">Ad esempio: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="014f5-134">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="014f5-135">-VaultName</span><span class="sxs-lookup"><span data-stu-id="014f5-135">-VaultName</span></span>
<span data-ttu-id="014f5-136">Specifica il nome vault della chiave in cui questo cmdlet importa i certificati.</span><span class="sxs-lookup"><span data-stu-id="014f5-136">Specifies the key vault name into which this cmdlet imports certificates.</span></span>
<span data-ttu-id="014f5-137">Questo cmdlet crea il nome di dominio completo (FQDN) di un vault delle chiavi in base al nome e all'ambiente attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="014f5-137">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="014f5-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="014f5-138">-Confirm</span></span>
<span data-ttu-id="014f5-139">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="014f5-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="014f5-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="014f5-140">-WhatIf</span></span>
<span data-ttu-id="014f5-141">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="014f5-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="014f5-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="014f5-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="014f5-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="014f5-143">CommonParameters</span></span>
<span data-ttu-id="014f5-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="014f5-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="014f5-145">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="014f5-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="014f5-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="014f5-146">INPUTS</span></span>

### <span data-ttu-id="014f5-147">System.String</span><span class="sxs-lookup"><span data-stu-id="014f5-147">System.String</span></span>

### <span data-ttu-id="014f5-148">System.Security.Cryptography.X509Certificates.X509Certificate2Collection</span><span class="sxs-lookup"><span data-stu-id="014f5-148">System.Security.Cryptography.X509Certificates.X509Certificate2Collection</span></span>

### <span data-ttu-id="014f5-149">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="014f5-149">System.Collections.Hashtable</span></span>

## <span data-ttu-id="014f5-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="014f5-150">OUTPUTS</span></span>

### <span data-ttu-id="014f5-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="014f5-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="014f5-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="014f5-152">NOTES</span></span>

## <span data-ttu-id="014f5-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="014f5-153">RELATED LINKS</span></span>

[<span data-ttu-id="014f5-154">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="014f5-154">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="014f5-155">Creazione e unione di CSR nel Vault delle chiavi</span><span class="sxs-lookup"><span data-stu-id="014f5-155">Creating and merging CSR in Key Vault</span></span>](https://docs.microsoft.com/en-us/azure/key-vault/certificates/create-certificate-signing-request)