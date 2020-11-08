---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: b0d690358fb5598b1a88ecb7fe169c8ef3d2718f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022839"
---
# <span data-ttu-id="56c98-101">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="56c98-101">New-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="56c98-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="56c98-102">SYNOPSIS</span></span>
<span data-ttu-id="56c98-103">Crea un oggetto Criteri di certificato in memoria.</span><span class="sxs-lookup"><span data-stu-id="56c98-103">Creates an in-memory certificate policy object.</span></span>

## <span data-ttu-id="56c98-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="56c98-104">SYNTAX</span></span>

### <span data-ttu-id="56c98-105">SubjectName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="56c98-105">SubjectName (Default)</span></span>
```
New-AzKeyVaultCertificatePolicy [-IssuerName] <String> [-SubjectName] <String>
 [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>]
 [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeySize <Int32>] [-KeyNotExportable] [-CertificateTransparency <Boolean>]
 [-Curve <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56c98-106">DNSNames</span><span class="sxs-lookup"><span data-stu-id="56c98-106">DNSNames</span></span>
```
New-AzKeyVaultCertificatePolicy [-IssuerName] <String> [[-SubjectName] <String>]
 [-DnsName] <System.Collections.Generic.List`1[System.String]> [-RenewAtNumberOfDaysBeforeExpiry <Int32>]
 [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeySize <Int32>] [-KeyNotExportable] [-CertificateTransparency <Boolean>]
 [-Curve <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56c98-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56c98-107">DESCRIPTION</span></span>
<span data-ttu-id="56c98-108">Il cmdlet **New-AzKeyVaultCertificatePolicy** crea un oggetto Criteri di certificato in memoria per Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="56c98-108">The **New-AzKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="56c98-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="56c98-109">EXAMPLES</span></span>

### <span data-ttu-id="56c98-110">Esempio 1: creare un criterio di certificato</span><span class="sxs-lookup"><span data-stu-id="56c98-110">Example 1: Create a certificate policy</span></span>
```powershell
PS C:\> New-AzKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal

SecretContentType               : application/x-pkcs12
Kty                             :
KeySize                         : 2048
Curve                           :
Exportable                      :
ReuseKeyOnRenewal               : True
SubjectName                     : CN=contoso.com
DnsNames                        :
KeyUsage                        :
Ekus                            :
ValidityInMonths                : 6
IssuerName                      : Self
CertificateType                 :
RenewAtNumberOfDaysBeforeExpiry :
RenewAtPercentageLifetime       :
EmailAtNumberOfDaysBeforeExpiry :
EmailAtPercentageLifetime       :
CertificateTransparency         :
Enabled                         : True
Created                         :
Updated                         :
```

<span data-ttu-id="56c98-111">Questo comando crea un criterio di certificato valido per sei mesi e riutilizza la chiave per rinnovare il certificato.</span><span class="sxs-lookup"><span data-stu-id="56c98-111">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="56c98-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="56c98-112">PARAMETERS</span></span>

### <span data-ttu-id="56c98-113">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="56c98-113">-CertificateTransparency</span></span>
<span data-ttu-id="56c98-114">Indica se la trasparenza del certificato è abilitata per il certificato/emittente; Se non viene specificato, il valore predefinito è "true"</span><span class="sxs-lookup"><span data-stu-id="56c98-114">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56c98-115">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="56c98-115">-CertificateType</span></span>
<span data-ttu-id="56c98-116">Specifica il tipo di certificato per l'emittente.</span><span class="sxs-lookup"><span data-stu-id="56c98-116">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56c98-117">-Curva</span><span class="sxs-lookup"><span data-stu-id="56c98-117">-Curve</span></span>
<span data-ttu-id="56c98-118">Specifica il nome della curva ellittica della chiave del certificato.</span><span class="sxs-lookup"><span data-stu-id="56c98-118">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="56c98-119">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="56c98-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="56c98-120">P-256</span><span class="sxs-lookup"><span data-stu-id="56c98-120">P-256</span></span>
- <span data-ttu-id="56c98-121">P-384</span><span class="sxs-lookup"><span data-stu-id="56c98-121">P-384</span></span>
- <span data-ttu-id="56c98-122">P-521</span><span class="sxs-lookup"><span data-stu-id="56c98-122">P-521</span></span>
- <span data-ttu-id="56c98-123">P-256K</span><span class="sxs-lookup"><span data-stu-id="56c98-123">P-256K</span></span>
- <span data-ttu-id="56c98-124">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="56c98-124">SECP256K1</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: P-256, P-384, P-521, P-256K, SECP256K1

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56c98-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56c98-125">-DefaultProfile</span></span>
<span data-ttu-id="56c98-126">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="56c98-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="56c98-127">-Disabled</span><span class="sxs-lookup"><span data-stu-id="56c98-127">-Disabled</span></span>
<span data-ttu-id="56c98-128">Indica che il criterio di certificato è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="56c98-128">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56c98-129">-DnsName</span><span class="sxs-lookup"><span data-stu-id="56c98-129">-DnsName</span></span>
<span data-ttu-id="56c98-130">Specifica i nomi DNS nel certificato.</span><span class="sxs-lookup"><span data-stu-id="56c98-130">Specifies the DNS names in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: DNSNames
Aliases: DnsNames

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56c98-131">-EKU</span><span class="sxs-lookup"><span data-stu-id="56c98-131">-Ekus</span></span>
<span data-ttu-id="56c98-132">Specifica gli usi chiave avanzati (EKU) nel certificato.</span><span class="sxs-lookup"><span data-stu-id="56c98-132">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56c98-133">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="56c98-133">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="56c98-134">Specifica il numero di giorni prima della scadenza in cui viene avviato il processo di notifica automatica.</span><span class="sxs-lookup"><span data-stu-id="56c98-134">Specifies how many days before expiry the automatic notification process begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56c98-135">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="56c98-135">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="56c98-136">Specifica la percentuale della durata dopo la quale inizia il processo automatico per la notifica.</span><span class="sxs-lookup"><span data-stu-id="56c98-136">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56c98-137">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="56c98-137">-IssuerName</span></span>
<span data-ttu-id="56c98-138">Specifica il nome dell'autorità di certificazione per il certificato.</span><span class="sxs-lookup"><span data-stu-id="56c98-138">Specifies the name of the issuer for the certificate.</span></span>

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

### <span data-ttu-id="56c98-139">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="56c98-139">-KeyNotExportable</span></span>
<span data-ttu-id="56c98-140">Indica che la chiave non è esportabile.</span><span class="sxs-lookup"><span data-stu-id="56c98-140">Indicates that the key is not exportable.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56c98-141">-KeySize</span><span class="sxs-lookup"><span data-stu-id="56c98-141">-KeySize</span></span>
<span data-ttu-id="56c98-142">Specifica la dimensione della chiave del certificato.</span><span class="sxs-lookup"><span data-stu-id="56c98-142">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="56c98-143">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="56c98-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="56c98-144">2048</span><span class="sxs-lookup"><span data-stu-id="56c98-144">2048</span></span>
- <span data-ttu-id="56c98-145">3072</span><span class="sxs-lookup"><span data-stu-id="56c98-145">3072</span></span>
- <span data-ttu-id="56c98-146">4096</span><span class="sxs-lookup"><span data-stu-id="56c98-146">4096</span></span>
- <span data-ttu-id="56c98-147">256</span><span class="sxs-lookup"><span data-stu-id="56c98-147">256</span></span>
- <span data-ttu-id="56c98-148">384</span><span class="sxs-lookup"><span data-stu-id="56c98-148">384</span></span>
- <span data-ttu-id="56c98-149">521</span><span class="sxs-lookup"><span data-stu-id="56c98-149">521</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:
Accepted values: 2048, 3072, 4096, 256, 384, 521

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56c98-150">-Tipo di digitare</span><span class="sxs-lookup"><span data-stu-id="56c98-150">-KeyType</span></span>
<span data-ttu-id="56c98-151">Specifica il tipo di chiave della chiave che consente di eseguire il backup del certificato.</span><span class="sxs-lookup"><span data-stu-id="56c98-151">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="56c98-152">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="56c98-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="56c98-153">RSA</span><span class="sxs-lookup"><span data-stu-id="56c98-153">RSA</span></span>
- <span data-ttu-id="56c98-154">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="56c98-154">RSA-HSM</span></span>
- <span data-ttu-id="56c98-155">CE</span><span class="sxs-lookup"><span data-stu-id="56c98-155">EC</span></span>
- <span data-ttu-id="56c98-156">EC-HSM</span><span class="sxs-lookup"><span data-stu-id="56c98-156">EC-HSM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA, RSA-HSM, EC, EC-HSM

Required: False
Position: Named
Default value: RSA
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56c98-157">-Utilizzo della sintassi</span><span class="sxs-lookup"><span data-stu-id="56c98-157">-KeyUsage</span></span>
<span data-ttu-id="56c98-158">Specifica gli usi chiave nel certificato.</span><span class="sxs-lookup"><span data-stu-id="56c98-158">Specifies the key usages in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]
Parameter Sets: (All)
Aliases:
Accepted values: None, EncipherOnly, CrlSign, KeyCertSign, KeyAgreement, DataEncipherment, KeyEncipherment, NonRepudiation, DigitalSignature, DecipherOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56c98-159">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="56c98-159">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="56c98-160">Specifica il numero di giorni prima della scadenza in cui inizia il processo automatico per il rinnovo del certificato.</span><span class="sxs-lookup"><span data-stu-id="56c98-160">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56c98-161">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="56c98-161">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="56c98-162">Specifica la percentuale della durata dopo la quale inizia il processo automatico per il rinnovo del certificato.</span><span class="sxs-lookup"><span data-stu-id="56c98-162">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56c98-163">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="56c98-163">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="56c98-164">Indica che il certificato riutilizza la chiave durante il rinnovo.</span><span class="sxs-lookup"><span data-stu-id="56c98-164">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56c98-165">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="56c98-165">-SecretContentType</span></span>
<span data-ttu-id="56c98-166">Specifica il tipo di contenuto del nuovo segreto del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="56c98-166">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="56c98-167">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="56c98-167">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="56c98-168">applicazione/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="56c98-168">application/x-pkcs12</span></span>
- <span data-ttu-id="56c98-169">applicazione/x-Pem-file</span><span class="sxs-lookup"><span data-stu-id="56c98-169">application/x-pem-file</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56c98-170">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="56c98-170">-SubjectName</span></span>
<span data-ttu-id="56c98-171">Specifica il nome del soggetto del certificato.</span><span class="sxs-lookup"><span data-stu-id="56c98-171">Specifies the subject name of the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: SubjectName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DNSNames
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56c98-172">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="56c98-172">-ValidityInMonths</span></span>
<span data-ttu-id="56c98-173">Specifica il numero di mesi in cui il certificato è valido.</span><span class="sxs-lookup"><span data-stu-id="56c98-173">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56c98-174">-Confermare</span><span class="sxs-lookup"><span data-stu-id="56c98-174">-Confirm</span></span>
<span data-ttu-id="56c98-175">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56c98-175">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56c98-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56c98-176">-WhatIf</span></span>
<span data-ttu-id="56c98-177">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="56c98-177">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56c98-178">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="56c98-178">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56c98-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56c98-179">CommonParameters</span></span>
<span data-ttu-id="56c98-180">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56c98-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56c98-181">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56c98-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56c98-182">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="56c98-182">INPUTS</span></span>

### <span data-ttu-id="56c98-183">System. String</span><span class="sxs-lookup"><span data-stu-id="56c98-183">System.String</span></span>

### <span data-ttu-id="56c98-184">System. Collections. Generic. list ' 1 [[System. String, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="56c98-184">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="56c98-185">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="56c98-185">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="56c98-186">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="56c98-186">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="56c98-187">System. Collections. Generic. list ' 1 [[System. Security. Cryptography. X509Certificates. X509KeyUsageFlags, System. Security. Cryptography. X509Certificates, Version = 4.2.1.0, Culture = neutral, PublicKeyToken = b03f5f7f11d50a3a]]</span><span class="sxs-lookup"><span data-stu-id="56c98-187">System.Collections.Generic.List\`1[[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags, System.Security.Cryptography.X509Certificates, Version=4.2.1.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a]]</span></span>

## <span data-ttu-id="56c98-188">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="56c98-188">OUTPUTS</span></span>

### <span data-ttu-id="56c98-189">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="56c98-189">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="56c98-190">Note</span><span class="sxs-lookup"><span data-stu-id="56c98-190">NOTES</span></span>

## <span data-ttu-id="56c98-191">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="56c98-191">RELATED LINKS</span></span>

[<span data-ttu-id="56c98-192">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="56c98-192">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="56c98-193">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="56c98-193">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

