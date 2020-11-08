---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: D4188DC6-A8AB-4B45-9781-94B74C338C63
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/import-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultCertificate.md
ms.openlocfilehash: 4d78e325908cf7863177b6bb3e1ebed67f4b36de
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018643"
---
# <span data-ttu-id="e0855-101">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e0855-101">Import-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="e0855-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e0855-102">SYNOPSIS</span></span>
<span data-ttu-id="e0855-103">Importa un certificato in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="e0855-103">Imports a certificate to a key vault.</span></span>

## <span data-ttu-id="e0855-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e0855-104">SYNTAX</span></span>

### <span data-ttu-id="e0855-105">ImportCertificateFromFile (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e0855-105">ImportCertificateFromFile (Default)</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> -FilePath <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e0855-106">ImportWithPrivateKeyFromString</span><span class="sxs-lookup"><span data-stu-id="e0855-106">ImportWithPrivateKeyFromString</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> -CertificateString <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e0855-107">ImportWithPrivateKeyFromCollection</span><span class="sxs-lookup"><span data-stu-id="e0855-107">ImportWithPrivateKeyFromCollection</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 [-CertificateCollection] <X509Certificate2Collection> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0855-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e0855-108">DESCRIPTION</span></span>
<span data-ttu-id="e0855-109">Il cmdlet **Import-AzKeyVaultCertificate** importa un certificato in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="e0855-109">The **Import-AzKeyVaultCertificate** cmdlet imports a certificate into a key vault.</span></span>
<span data-ttu-id="e0855-110">Puoi creare il certificato da importare usando uno dei metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="e0855-110">You can create the certificate to import by using one of the following methods:</span></span>
- <span data-ttu-id="e0855-111">Utilizzare il cmdlet New-AzKeyVaultCertificateSigningRequest per creare una richiesta di firma del certificato e inviarla a un'autorità di certificazione.</span><span class="sxs-lookup"><span data-stu-id="e0855-111">Use the New-AzKeyVaultCertificateSigningRequest cmdlet to create a certificate signing request and submit it to a certificate authority.</span></span>
- <span data-ttu-id="e0855-112">Usare un file di pacchetto di certificati esistente, ad esempio un file con estensione pfx o P12, che contiene sia il certificato che la chiave privata.</span><span class="sxs-lookup"><span data-stu-id="e0855-112">Use an existing certificate package file, such as a .pfx or .p12 file, which contains both the certificate and private key.</span></span>

## <span data-ttu-id="e0855-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e0855-113">EXAMPLES</span></span>

### <span data-ttu-id="e0855-114">Esempio 1: importare un certificato della volta chiave</span><span class="sxs-lookup"><span data-stu-id="e0855-114">Example 1: Import a key vault certificate</span></span>
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

<span data-ttu-id="e0855-115">Il primo comando usa il cmdlet ConvertTo-SecureString per creare una password sicura e quindi la archivia nella variabile $Password.</span><span class="sxs-lookup"><span data-stu-id="e0855-115">The first command uses the ConvertTo-SecureString cmdlet to create a secure password, and then stores it in the $Password variable.</span></span>
<span data-ttu-id="e0855-116">Il secondo comando importa il certificato denominato ImportCert01 nel caveau della chiave CosotosoKV01.</span><span class="sxs-lookup"><span data-stu-id="e0855-116">The second command imports the certificate named ImportCert01 into the CosotosoKV01 key vault.</span></span>

## <span data-ttu-id="e0855-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e0855-117">PARAMETERS</span></span>

### <span data-ttu-id="e0855-118">-Certificate</span><span class="sxs-lookup"><span data-stu-id="e0855-118">-CertificateCollection</span></span>
<span data-ttu-id="e0855-119">Specifica la raccolta di certificati da aggiungere a un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="e0855-119">Specifies the certificate collection to add to a key vault.</span></span>

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

### <span data-ttu-id="e0855-120">-CertificateString</span><span class="sxs-lookup"><span data-stu-id="e0855-120">-CertificateString</span></span>
<span data-ttu-id="e0855-121">Specifica una stringa di certificato.</span><span class="sxs-lookup"><span data-stu-id="e0855-121">Specifies a certificate string.</span></span>

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

### <span data-ttu-id="e0855-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0855-122">-DefaultProfile</span></span>
<span data-ttu-id="e0855-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e0855-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0855-124">-FilePath</span><span class="sxs-lookup"><span data-stu-id="e0855-124">-FilePath</span></span>
<span data-ttu-id="e0855-125">Specifica il percorso del file di certificato importato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0855-125">Specifies the path of the certificate file that this cmdlet imports.</span></span>

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

### <span data-ttu-id="e0855-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="e0855-126">-Name</span></span>
<span data-ttu-id="e0855-127">Specifica il nome del certificato.</span><span class="sxs-lookup"><span data-stu-id="e0855-127">Specifies the certificate name.</span></span> <span data-ttu-id="e0855-128">Questo cmdlet costruisce il nome di dominio completo (FQDN) di un certificato dal nome del Vault chiave, dall'ambiente attualmente selezionato e dal nome del certificato.</span><span class="sxs-lookup"><span data-stu-id="e0855-128">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate from key vault name, currently selected environment, and certificate name.</span></span>

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

### <span data-ttu-id="e0855-129">-Password</span><span class="sxs-lookup"><span data-stu-id="e0855-129">-Password</span></span>
<span data-ttu-id="e0855-130">Specifica la password per un file di certificato.</span><span class="sxs-lookup"><span data-stu-id="e0855-130">Specifies the password for a certificate file.</span></span>

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

### <span data-ttu-id="e0855-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="e0855-131">-Tag</span></span>
<span data-ttu-id="e0855-132">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="e0855-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e0855-133">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="e0855-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e0855-134">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="e0855-134">-VaultName</span></span>
<span data-ttu-id="e0855-135">Specifica il nome del Vault chiave in cui questo cmdlet importa i certificati.</span><span class="sxs-lookup"><span data-stu-id="e0855-135">Specifies the key vault name into which this cmdlet imports certificates.</span></span>
<span data-ttu-id="e0855-136">Questo cmdlet costruisce il nome di dominio completo (FQDN) di un Vault chiave in base al nome e all'ambiente attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="e0855-136">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="e0855-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e0855-137">-Confirm</span></span>
<span data-ttu-id="e0855-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0855-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0855-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0855-139">-WhatIf</span></span>
<span data-ttu-id="e0855-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e0855-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0855-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e0855-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0855-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0855-142">CommonParameters</span></span>
<span data-ttu-id="e0855-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0855-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0855-144">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0855-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0855-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e0855-145">INPUTS</span></span>

### <span data-ttu-id="e0855-146">System. String</span><span class="sxs-lookup"><span data-stu-id="e0855-146">System.String</span></span>

### <span data-ttu-id="e0855-147">System. Security. Cryptography. X509Certificates. X509Certificate2collection</span><span class="sxs-lookup"><span data-stu-id="e0855-147">System.Security.Cryptography.X509Certificates.X509Certificate2Collection</span></span>

### <span data-ttu-id="e0855-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e0855-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e0855-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e0855-149">OUTPUTS</span></span>

### <span data-ttu-id="e0855-150">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e0855-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="e0855-151">Note</span><span class="sxs-lookup"><span data-stu-id="e0855-151">NOTES</span></span>

## <span data-ttu-id="e0855-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e0855-152">RELATED LINKS</span></span>

[<span data-ttu-id="e0855-153">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e0855-153">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)
