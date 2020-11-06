---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: D4188DC6-A8AB-4B45-9781-94B74C338C63
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Import-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Import-AzureKeyVaultCertificate.md
ms.openlocfilehash: b97dc509ad6508c2cbec79d6ba1db27508f94c34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510583"
---
# <span data-ttu-id="cd3f2-101">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="cd3f2-101">Import-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="cd3f2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cd3f2-102">SYNOPSIS</span></span>
<span data-ttu-id="cd3f2-103">Importa un certificato in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="cd3f2-103">Imports a certificate to a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd3f2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cd3f2-104">SYNTAX</span></span>

### <span data-ttu-id="cd3f2-105">ImportCertificateFromFile (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cd3f2-105">ImportCertificateFromFile (Default)</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> -FilePath <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd3f2-106">ImportWithPrivateKeyFromFile</span><span class="sxs-lookup"><span data-stu-id="cd3f2-106">ImportWithPrivateKeyFromFile</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> -FilePath <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cd3f2-107">ImportWithPrivateKeyFromString</span><span class="sxs-lookup"><span data-stu-id="cd3f2-107">ImportWithPrivateKeyFromString</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> -CertificateString <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cd3f2-108">ImportWithPrivateKeyFromCollection</span><span class="sxs-lookup"><span data-stu-id="cd3f2-108">ImportWithPrivateKeyFromCollection</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 -CertificateCollection <X509Certificate2Collection> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd3f2-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd3f2-109">DESCRIPTION</span></span>
<span data-ttu-id="cd3f2-110">Il cmdlet **Import-AzureKeyVaultCertificate** importa un certificato in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="cd3f2-110">The **Import-AzureKeyVaultCertificate** cmdlet imports a certificate into a key vault.</span></span>

<span data-ttu-id="cd3f2-111">Puoi creare il certificato da importare usando uno dei metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="cd3f2-111">You can create the certificate to import by using one of the following methods:</span></span>

- <span data-ttu-id="cd3f2-112">Utilizzare il cmdlet New-AzureKeyVaultCertificateSigningRequest per creare una richiesta di firma del certificato e inviarla a un'autorità di certificazione.</span><span class="sxs-lookup"><span data-stu-id="cd3f2-112">Use the New-AzureKeyVaultCertificateSigningRequest cmdlet to create a certificate signing request and submit it to a certificate authority.</span></span>
- <span data-ttu-id="cd3f2-113">Usare un file di pacchetto di certificati esistente, ad esempio un file con estensione pfx o P12, che contiene sia il certificato che la chiave privata.</span><span class="sxs-lookup"><span data-stu-id="cd3f2-113">Use an existing certificate package file, such as a .pfx or .p12 file, which contains both the certificate and private key.</span></span>

## <span data-ttu-id="cd3f2-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cd3f2-114">EXAMPLES</span></span>

### <span data-ttu-id="cd3f2-115">Esempio 1: importare un certificato della volta chiave</span><span class="sxs-lookup"><span data-stu-id="cd3f2-115">Example 1: Import a key vault certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS C:\> Import-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "ImportCert01" -FilePath "C:\Users\contosoUser\Desktop\import.pfx" -Password $Password
Name        : importCert01
Certificate : [Subject]
                CN=contoso.com

              [Issuer]
                CN=contoso.com

              [Serial Number]
                05979C5A2F0741D5A3B6F97673E8A118

              [Not Before]
                2/8/2016 3:11:45 PM

              [Not After]
                8/8/2016 4:21:45 PM

              [Thumbprint]
                3E9B6848AD1834284157D68B060F748037F663C8

Thumbprint  : 3E9B6848AD1834284157D68B060F748037F663C8
Tags        :
Enabled     : True
Created     : 2/8/2016 11:50:43 PM
Updated     : 2/8/2016 11:50:43 PM
```

<span data-ttu-id="cd3f2-116">Il primo comando usa il cmdlet ConvertTo-SecureString per creare una password sicura e quindi la archivia nella variabile $Password.</span><span class="sxs-lookup"><span data-stu-id="cd3f2-116">The first command uses the ConvertTo-SecureString cmdlet to create a secure password, and then stores it in the $Password variable.</span></span>

<span data-ttu-id="cd3f2-117">Il secondo comando importa il certificato denominato ImportCert01 nel caveau della chiave CosotosoKV01.</span><span class="sxs-lookup"><span data-stu-id="cd3f2-117">The second command imports the certificate named ImportCert01 into the CosotosoKV01 key vault.</span></span>

## <span data-ttu-id="cd3f2-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cd3f2-118">PARAMETERS</span></span>

### <span data-ttu-id="cd3f2-119">-Certificate</span><span class="sxs-lookup"><span data-stu-id="cd3f2-119">-CertificateCollection</span></span>
<span data-ttu-id="cd3f2-120">Specifica la raccolta di certificati da aggiungere a un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="cd3f2-120">Specifies the certificate collection to add to a key vault.</span></span>

```yaml
Type: System.Security.Cryptography.X509Certificates.X509Certificate2Collection
Parameter Sets: ImportWithPrivateKeyFromCollection
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd3f2-121">-CertificateString</span><span class="sxs-lookup"><span data-stu-id="cd3f2-121">-CertificateString</span></span>
<span data-ttu-id="cd3f2-122">Specifica una stringa di certificato.</span><span class="sxs-lookup"><span data-stu-id="cd3f2-122">Specifies a certificate string.</span></span>

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

### <span data-ttu-id="cd3f2-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cd3f2-123">-Confirm</span></span>
<span data-ttu-id="cd3f2-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd3f2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd3f2-125">-FilePath</span><span class="sxs-lookup"><span data-stu-id="cd3f2-125">-FilePath</span></span>
<span data-ttu-id="cd3f2-126">Specifica il percorso del file di certificato importato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd3f2-126">Specifies the path of the certificate file that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportCertificateFromFile, ImportWithPrivateKeyFromFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd3f2-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="cd3f2-127">-Name</span></span>
<span data-ttu-id="cd3f2-128">Specifica il nome del certificato.</span><span class="sxs-lookup"><span data-stu-id="cd3f2-128">Specifies the certificate name.</span></span> <span data-ttu-id="cd3f2-129">Questo cmdlet costruisce il nome di dominio completo (FQDN) di un certificato dal nome del Vault chiave, dall'ambiente attualmente selezionato e dal nome del certificato.</span><span class="sxs-lookup"><span data-stu-id="cd3f2-129">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate from key vault name, currently selected environment, and certificate name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd3f2-130">-Password</span><span class="sxs-lookup"><span data-stu-id="cd3f2-130">-Password</span></span>
<span data-ttu-id="cd3f2-131">Specifica la password per un file di certificato.</span><span class="sxs-lookup"><span data-stu-id="cd3f2-131">Specifies the password for a certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ImportWithPrivateKeyFromFile, ImportWithPrivateKeyFromString
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd3f2-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="cd3f2-132">-Tag</span></span>
<span data-ttu-id="cd3f2-133">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="cd3f2-133">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="cd3f2-134">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="cd3f2-134">For example:</span></span>

<span data-ttu-id="cd3f2-135">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="cd3f2-135">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="cd3f2-136">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="cd3f2-136">-VaultName</span></span>
<span data-ttu-id="cd3f2-137">Specifica il nome del Vault chiave in cui questo cmdlet importa i certificati.</span><span class="sxs-lookup"><span data-stu-id="cd3f2-137">Specifies the key vault name into which this cmdlet imports certificates.</span></span>
<span data-ttu-id="cd3f2-138">Questo cmdlet costruisce il nome di dominio completo (FQDN) di un Vault chiave in base al nome e all'ambiente attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="cd3f2-138">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd3f2-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd3f2-139">-WhatIf</span></span>
<span data-ttu-id="cd3f2-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd3f2-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd3f2-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd3f2-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd3f2-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd3f2-142">-DefaultProfile</span></span>
<span data-ttu-id="cd3f2-143">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cd3f2-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd3f2-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd3f2-144">CommonParameters</span></span>
<span data-ttu-id="cd3f2-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd3f2-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd3f2-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd3f2-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd3f2-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cd3f2-147">INPUTS</span></span>

## <span data-ttu-id="cd3f2-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cd3f2-148">OUTPUTS</span></span>

### <span data-ttu-id="cd3f2-149">Microsoft. Azure. Commands. Vault. Models. CertificateBundle</span><span class="sxs-lookup"><span data-stu-id="cd3f2-149">Microsoft.Azure.Commands.KeyVault.Models.CertificateBundle</span></span>

## <span data-ttu-id="cd3f2-150">Note</span><span class="sxs-lookup"><span data-stu-id="cd3f2-150">NOTES</span></span>

## <span data-ttu-id="cd3f2-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cd3f2-151">RELATED LINKS</span></span>

[<span data-ttu-id="cd3f2-152">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="cd3f2-152">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)
