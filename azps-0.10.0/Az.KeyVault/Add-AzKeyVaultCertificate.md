---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificate.md
ms.openlocfilehash: 4984ce5dde65be9e715a7e34a10e5671902b53cc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863077"
---
# <span data-ttu-id="8130a-101">Add-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="8130a-101">Add-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="8130a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8130a-102">SYNOPSIS</span></span>
<span data-ttu-id="8130a-103">Aggiunge un certificato a un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="8130a-103">Adds a certificate to a key vault.</span></span>

## <span data-ttu-id="8130a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8130a-104">SYNTAX</span></span>

```
Add-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 [[-CertificatePolicy] <KeyVaultCertificatePolicy>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8130a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8130a-105">DESCRIPTION</span></span>
<span data-ttu-id="8130a-106">Il cmdlet **Add-AzKeyVaultCertificate** avvia il processo di registrazione di un certificato in un Vault chiave in Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="8130a-106">The **Add-AzKeyVaultCertificate** cmdlet starts the process of enrolling for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="8130a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8130a-107">EXAMPLES</span></span>

### <span data-ttu-id="8130a-108">Esempio 1: aggiungere un certificato</span><span class="sxs-lookup"><span data-stu-id="8130a-108">Example 1: Add a certificate</span></span>
```
PS C:\>$Policy = New-AzKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal
PS C:\> Add-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01" -CertificatePolicy $Policy

Status                    : inProgress
CancellationRequested     : False
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC73w3VRBOlgJ5Od1PjDh+2ytngNZp+ZP4fkuX8K1Ti5LA6Ih7eWx1fgAN/iTb6l
                            5K6LvAIJvsTNVePMNxfSdaEIJ70Inm45wVU4A/kf+UxQWAYVMsBrLtDFWxnVhzf6n7RGYke6HLBj3j5ASb9g+olSs6eON25ibF0t+u6JC+sIR0LmVGar9Q0eZys1rdfzJBIKq+laOM7z2pJijb5ANqve9
                            i7rH5mnhQk4V8WsRstOhYR9jgLqSSxokDoeaBClIOidSBYqVc1yNv4ASe1UWUCR7ZK6OQXiecNWSWPmgWEyawu6AR9eb1YotCr2ScheMOCxlm3103luitxrd8A7kMjAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAIHhsDJV37PKi8hor5eQf7+Tct1preIvSwqV0NF6Uo7O6
                            YnC9Py7Wp7CHfKzuqeptUk2Tsu7B5dHB+o9Ypeeqw8fWhTN0GFGRKO7WjZQlDqL+lRNcjlFSaP022oIP0kmvVhBcmZqRQlALXccAaxEclFA/3y/aNj2gwWeKpH/pwAkZ39zMEzpQCaRfnQk7e3l4MV8cf
                            eC2HPYdRWkXxAeDcNPxBuVmKy49AzYvly+APNVDU3v66gxl3fIKrGRsKi2Cp/nO5rBxG2h8t+0Za4l/HJ7ZWR9wKbd/xg7JhdZZFVBxMHYzw8KQ0ys13x8HY+PXU92Y7yD3uC2Rcj+zbAf+Kg==
ErrorCode                 :
ErrorMessage              : PS C:\>Get-AzKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01"
Status                    : completed
CancellationRequested     : False
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC73w3VRBOlgJ5Od1PjDh+2ytngNZp+ZP4fkuX8K1Ti5LA6Ih7eWx1fgAN/iTb6l
                            5K6LvAIJvsTNVePMNxfSdaEIJ70Inm45wVU4A/kf+UxQWAYVMsBrLtDFWxnVhzf6n7RGYke6HLBj3j5ASb9g+olSs6eON25ibF0t+u6JC+sIR0LmVGar9Q0eZys1rdfzJBIKq+laOM7z2pJijb5ANqve9
                            i7rH5mnhQk4V8WsRstOhYR9jgLqSSxokDoeaBClIOidSBYqVc1yNv4ASe1UWUCR7ZK6OQXiecNWSWPmgWEyawu6AR9eb1YotCr2ScheMOCxlm3103luitxrd8A7kMjAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAIHhsDJV37PKi8hor5eQf7+Tct1preIvSwqV0NF6Uo7O6
                            YnC9Py7Wp7CHfKzuqeptUk2Tsu7B5dHB+o9Ypeeqw8fWhTN0GFGRKO7WjZQlDqL+lRNcjlFSaP022oIP0kmvVhBcmZqRQlALXccAaxEclFA/3y/aNj2gwWeKpH/pwAkZ39zMEzpQCaRfnQk7e3l4MV8cf
                            eC2HPYdRWkXxAeDcNPxBuVmKy49AzYvly+APNVDU3v66gxl3fIKrGRsKi2Cp/nO5rBxG2h8t+0Za4l/HJ7ZWR9wKbd/xg7JhdZZFVBxMHYzw8KQ0ys13x8HY+PXU92Y7yD3uC2Rcj+zbAf+Kg==
ErrorCode                 :
ErrorMessage              : PS C:\>Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
Name        : testCert01
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
Created     : 2/8/2016 11:21:45 PM
Updated     : 2/8/2016 11:21:45 PM
```

<span data-ttu-id="8130a-109">Il primo comando usa il cmdlet New-AzKeyVaultCertificatePolicy per creare un criterio di certificato e lo archivia nella variabile $Policy.</span><span class="sxs-lookup"><span data-stu-id="8130a-109">The first command uses the New-AzKeyVaultCertificatePolicy cmdlet to create a certificate policy, and then stores it in the $Policy variable.</span></span>

<span data-ttu-id="8130a-110">Il secondo comando USA **Add-AzKeyVaultCertificate** per avviare il processo per creare un certificato.</span><span class="sxs-lookup"><span data-stu-id="8130a-110">The second command uses **Add-AzKeyVaultCertificate** to start the process to create a certificate.</span></span>

<span data-ttu-id="8130a-111">Il terzo comando usa il cmdlet Get-AzKeyVaultCertificateOperation per eseguire il polling dell'operazione per verificare che sia completa.</span><span class="sxs-lookup"><span data-stu-id="8130a-111">The third command uses the Get-AzKeyVaultCertificateOperation cmdlet to poll the operation to verify that it's complete.</span></span>

<span data-ttu-id="8130a-112">Il comando finale usa il cmdlet Get-AzKeyVaultCertificate per ottenere il certificato.</span><span class="sxs-lookup"><span data-stu-id="8130a-112">The final command uses the Get-AzKeyVaultCertificate cmdlet to get the certificate.</span></span>

## <span data-ttu-id="8130a-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8130a-113">PARAMETERS</span></span>

### <span data-ttu-id="8130a-114">-CertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="8130a-114">-CertificatePolicy</span></span>
<span data-ttu-id="8130a-115">Specifica un oggetto **KeyVaultCertificatePolicy** .</span><span class="sxs-lookup"><span data-stu-id="8130a-115">Specifies a **KeyVaultCertificatePolicy** object.</span></span>

```yaml
Type: KeyVaultCertificatePolicy
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8130a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8130a-116">-DefaultProfile</span></span>
<span data-ttu-id="8130a-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8130a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8130a-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="8130a-118">-Name</span></span>
<span data-ttu-id="8130a-119">Specifica il nome del certificato da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="8130a-119">Specifies the name of the certificate to add.</span></span>

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

### <span data-ttu-id="8130a-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="8130a-120">-Tag</span></span>
<span data-ttu-id="8130a-121">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="8130a-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8130a-122">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="8130a-122">For example:</span></span>

<span data-ttu-id="8130a-123">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="8130a-123">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8130a-124">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="8130a-124">-VaultName</span></span>
<span data-ttu-id="8130a-125">Specifica il nome di un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="8130a-125">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="8130a-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8130a-126">-Confirm</span></span>
<span data-ttu-id="8130a-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8130a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8130a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8130a-128">-WhatIf</span></span>
<span data-ttu-id="8130a-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8130a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8130a-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8130a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8130a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8130a-131">CommonParameters</span></span>
<span data-ttu-id="8130a-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8130a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8130a-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8130a-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8130a-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8130a-134">INPUTS</span></span>

### <span data-ttu-id="8130a-135">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8130a-135">None</span></span>
<span data-ttu-id="8130a-136">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="8130a-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8130a-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8130a-137">OUTPUTS</span></span>

### <span data-ttu-id="8130a-138">Microsoft. Azure. Commands. Vault. Models. KeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="8130a-138">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOperation</span></span>

## <span data-ttu-id="8130a-139">Note</span><span class="sxs-lookup"><span data-stu-id="8130a-139">NOTES</span></span>

## <span data-ttu-id="8130a-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8130a-140">RELATED LINKS</span></span>

[<span data-ttu-id="8130a-141">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="8130a-141">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)

[<span data-ttu-id="8130a-142">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="8130a-142">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="8130a-143">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="8130a-143">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)
