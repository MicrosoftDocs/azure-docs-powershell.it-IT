---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: D4188DC6-A8AB-4B45-9781-94B74C338C63
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/import-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Import-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Import-AzureKeyVaultCertificate.md
ms.openlocfilehash: 37befa1434d18241b2f4721523de0ab48bebfd0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688460"
---
# <span data-ttu-id="63f5e-101">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="63f5e-101">Import-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="63f5e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="63f5e-102">SYNOPSIS</span></span>
<span data-ttu-id="63f5e-103">Importa un certificato in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="63f5e-103">Imports a certificate to a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63f5e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="63f5e-104">SYNTAX</span></span>

### <span data-ttu-id="63f5e-105">ImportCertificateFromFile (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="63f5e-105">ImportCertificateFromFile (Default)</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> -FilePath <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="63f5e-106">ImportWithPrivateKeyFromString</span><span class="sxs-lookup"><span data-stu-id="63f5e-106">ImportWithPrivateKeyFromString</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> -CertificateString <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="63f5e-107">ImportWithPrivateKeyFromCollection</span><span class="sxs-lookup"><span data-stu-id="63f5e-107">ImportWithPrivateKeyFromCollection</span></span>
```
Import-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 [-CertificateCollection] <X509Certificate2Collection> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63f5e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="63f5e-108">DESCRIPTION</span></span>
<span data-ttu-id="63f5e-109">Il cmdlet **Import-AzureKeyVaultCertificate** importa un certificato in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="63f5e-109">The **Import-AzureKeyVaultCertificate** cmdlet imports a certificate into a key vault.</span></span>

<span data-ttu-id="63f5e-110">Puoi creare il certificato da importare usando uno dei metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="63f5e-110">You can create the certificate to import by using one of the following methods:</span></span>

- <span data-ttu-id="63f5e-111">Utilizzare il cmdlet New-AzureKeyVaultCertificateSigningRequest per creare una richiesta di firma del certificato e inviarla a un'autorità di certificazione.</span><span class="sxs-lookup"><span data-stu-id="63f5e-111">Use the New-AzureKeyVaultCertificateSigningRequest cmdlet to create a certificate signing request and submit it to a certificate authority.</span></span>
- <span data-ttu-id="63f5e-112">Usare un file di pacchetto di certificati esistente, ad esempio un file con estensione pfx o P12, che contiene sia il certificato che la chiave privata.</span><span class="sxs-lookup"><span data-stu-id="63f5e-112">Use an existing certificate package file, such as a .pfx or .p12 file, which contains both the certificate and private key.</span></span>

## <span data-ttu-id="63f5e-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="63f5e-113">EXAMPLES</span></span>

### <span data-ttu-id="63f5e-114">Esempio 1: importare un certificato della volta chiave</span><span class="sxs-lookup"><span data-stu-id="63f5e-114">Example 1: Import a key vault certificate</span></span>
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

<span data-ttu-id="63f5e-115">Il primo comando usa il cmdlet ConvertTo-SecureString per creare una password sicura e quindi la archivia nella variabile $Password.</span><span class="sxs-lookup"><span data-stu-id="63f5e-115">The first command uses the ConvertTo-SecureString cmdlet to create a secure password, and then stores it in the $Password variable.</span></span>

<span data-ttu-id="63f5e-116">Il secondo comando importa il certificato denominato ImportCert01 nel caveau della chiave CosotosoKV01.</span><span class="sxs-lookup"><span data-stu-id="63f5e-116">The second command imports the certificate named ImportCert01 into the CosotosoKV01 key vault.</span></span>

## <span data-ttu-id="63f5e-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="63f5e-117">PARAMETERS</span></span>

### <span data-ttu-id="63f5e-118">-Certificate</span><span class="sxs-lookup"><span data-stu-id="63f5e-118">-CertificateCollection</span></span>
<span data-ttu-id="63f5e-119">Specifica la raccolta di certificati da aggiungere a un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="63f5e-119">Specifies the certificate collection to add to a key vault.</span></span>

```yaml
Type: X509Certificate2Collection
Parameter Sets: ImportWithPrivateKeyFromCollection
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63f5e-120">-CertificateString</span><span class="sxs-lookup"><span data-stu-id="63f5e-120">-CertificateString</span></span>
<span data-ttu-id="63f5e-121">Specifica una stringa di certificato.</span><span class="sxs-lookup"><span data-stu-id="63f5e-121">Specifies a certificate string.</span></span>

```yaml
Type: String
Parameter Sets: ImportWithPrivateKeyFromString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63f5e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63f5e-122">-DefaultProfile</span></span>
<span data-ttu-id="63f5e-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="63f5e-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="63f5e-124">-FilePath</span><span class="sxs-lookup"><span data-stu-id="63f5e-124">-FilePath</span></span>
<span data-ttu-id="63f5e-125">Specifica il percorso del file di certificato importato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63f5e-125">Specifies the path of the certificate file that this cmdlet imports.</span></span>

```yaml
Type: String
Parameter Sets: ImportCertificateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63f5e-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="63f5e-126">-Name</span></span>
<span data-ttu-id="63f5e-127">Specifica il nome del certificato.</span><span class="sxs-lookup"><span data-stu-id="63f5e-127">Specifies the certificate name.</span></span> <span data-ttu-id="63f5e-128">Questo cmdlet costruisce il nome di dominio completo (FQDN) di un certificato dal nome del Vault chiave, dall'ambiente attualmente selezionato e dal nome del certificato.</span><span class="sxs-lookup"><span data-stu-id="63f5e-128">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate from key vault name, currently selected environment, and certificate name.</span></span>

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

### <span data-ttu-id="63f5e-129">-Password</span><span class="sxs-lookup"><span data-stu-id="63f5e-129">-Password</span></span>
<span data-ttu-id="63f5e-130">Specifica la password per un file di certificato.</span><span class="sxs-lookup"><span data-stu-id="63f5e-130">Specifies the password for a certificate file.</span></span>

```yaml
Type: SecureString
Parameter Sets: ImportCertificateFromFile, ImportWithPrivateKeyFromString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63f5e-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="63f5e-131">-Tag</span></span>
<span data-ttu-id="63f5e-132">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="63f5e-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="63f5e-133">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="63f5e-133">For example:</span></span>

<span data-ttu-id="63f5e-134">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="63f5e-134">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63f5e-135">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="63f5e-135">-VaultName</span></span>
<span data-ttu-id="63f5e-136">Specifica il nome del Vault chiave in cui questo cmdlet importa i certificati.</span><span class="sxs-lookup"><span data-stu-id="63f5e-136">Specifies the key vault name into which this cmdlet imports certificates.</span></span>
<span data-ttu-id="63f5e-137">Questo cmdlet costruisce il nome di dominio completo (FQDN) di un Vault chiave in base al nome e all'ambiente attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="63f5e-137">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="63f5e-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="63f5e-138">-Confirm</span></span>
<span data-ttu-id="63f5e-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63f5e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63f5e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63f5e-140">-WhatIf</span></span>
<span data-ttu-id="63f5e-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="63f5e-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63f5e-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="63f5e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63f5e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63f5e-143">CommonParameters</span></span>
<span data-ttu-id="63f5e-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63f5e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63f5e-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63f5e-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63f5e-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="63f5e-146">INPUTS</span></span>

### <span data-ttu-id="63f5e-147">Nessuno</span><span class="sxs-lookup"><span data-stu-id="63f5e-147">None</span></span>
<span data-ttu-id="63f5e-148">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="63f5e-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="63f5e-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="63f5e-149">OUTPUTS</span></span>

### <span data-ttu-id="63f5e-150">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="63f5e-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="63f5e-151">Note</span><span class="sxs-lookup"><span data-stu-id="63f5e-151">NOTES</span></span>

## <span data-ttu-id="63f5e-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="63f5e-152">RELATED LINKS</span></span>

[<span data-ttu-id="63f5e-153">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="63f5e-153">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)
