---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 370662b1d24f9b5b71653506be7a3add5a3801f8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189688"
---
# <span data-ttu-id="993ea-101">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="993ea-101">New-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="993ea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="993ea-102">SYNOPSIS</span></span>
<span data-ttu-id="993ea-103">Crea un oggetto Criteri di certificato in memoria.</span><span class="sxs-lookup"><span data-stu-id="993ea-103">Creates an in-memory certificate policy object.</span></span>

## <span data-ttu-id="993ea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="993ea-104">SYNTAX</span></span>

### <span data-ttu-id="993ea-105">SubjectName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="993ea-105">SubjectName (Default)</span></span>
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

### <span data-ttu-id="993ea-106">DNSNames</span><span class="sxs-lookup"><span data-stu-id="993ea-106">DNSNames</span></span>
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

## <span data-ttu-id="993ea-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="993ea-107">DESCRIPTION</span></span>
<span data-ttu-id="993ea-108">Il cmdlet **New-AzKeyVaultCertificatePolicy** crea un oggetto Criteri di certificato in memoria per Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="993ea-108">The **New-AzKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="993ea-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="993ea-109">EXAMPLES</span></span>

### <span data-ttu-id="993ea-110">Esempio 1: creare un criterio di certificato</span><span class="sxs-lookup"><span data-stu-id="993ea-110">Example 1: Create a certificate policy</span></span>
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

<span data-ttu-id="993ea-111">Questo comando crea un criterio di certificato valido per sei mesi e riutilizza la chiave per rinnovare il certificato.</span><span class="sxs-lookup"><span data-stu-id="993ea-111">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

### <span data-ttu-id="993ea-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="993ea-112">Example 2</span></span>

<span data-ttu-id="993ea-113">Crea un oggetto Criteri di certificato in memoria.</span><span class="sxs-lookup"><span data-stu-id="993ea-113">Creates an in-memory certificate policy object.</span></span> <span data-ttu-id="993ea-114">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="993ea-114">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzKeyVaultCertificatePolicy -IssuerName 'Self' -KeyType RSA -RenewAtNumberOfDaysBeforeExpiry <Int32> -SecretContentType application/x-pkcs12 -SubjectName 'CN=contoso.com' -ValidityInMonths 6
```

### <span data-ttu-id="993ea-115">Esempio 3: creare un certificato di nome alternativo soggetto (o SAN)</span><span class="sxs-lookup"><span data-stu-id="993ea-115">Example 3: Create a Subject Alternate Name (or SAN) certificate</span></span>

```powershell
PS C:\> New-AzKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -DnsName "contoso.com","support.contoso.com","docs.contoso.com" -IssuerName "Self"

SecretContentType               : application/x-pkcs12
Kty                             : RSA
KeySize                         : 2048
Curve                           :
Exportable                      :
ReuseKeyOnRenewal               : False
SubjectName                     : CN=contoso.com
DnsNames                        : {contoso.com, support.contoso.com, docs.contoso.com}
KeyUsage                        :
Ekus                            :
ValidityInMonths                :
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

<span data-ttu-id="993ea-116">Questo esempio crea un certificato SAN con 3 nomi DNS.</span><span class="sxs-lookup"><span data-stu-id="993ea-116">This example creates a SAN certificate with 3 DNS names.</span></span>

## <span data-ttu-id="993ea-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="993ea-117">PARAMETERS</span></span>

### <span data-ttu-id="993ea-118">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="993ea-118">-CertificateTransparency</span></span>
<span data-ttu-id="993ea-119">Indica se la trasparenza del certificato è abilitata per il certificato/emittente; Se non viene specificato, il valore predefinito è "true"</span><span class="sxs-lookup"><span data-stu-id="993ea-119">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

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

### <span data-ttu-id="993ea-120">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="993ea-120">-CertificateType</span></span>
<span data-ttu-id="993ea-121">Specifica il tipo di certificato per l'emittente.</span><span class="sxs-lookup"><span data-stu-id="993ea-121">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="993ea-122">-Curva</span><span class="sxs-lookup"><span data-stu-id="993ea-122">-Curve</span></span>
<span data-ttu-id="993ea-123">Specifica il nome della curva ellittica della chiave del certificato.</span><span class="sxs-lookup"><span data-stu-id="993ea-123">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="993ea-124">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="993ea-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="993ea-125">P-256</span><span class="sxs-lookup"><span data-stu-id="993ea-125">P-256</span></span>
- <span data-ttu-id="993ea-126">P-384</span><span class="sxs-lookup"><span data-stu-id="993ea-126">P-384</span></span>
- <span data-ttu-id="993ea-127">P-521</span><span class="sxs-lookup"><span data-stu-id="993ea-127">P-521</span></span>
- <span data-ttu-id="993ea-128">P-256K</span><span class="sxs-lookup"><span data-stu-id="993ea-128">P-256K</span></span>
- <span data-ttu-id="993ea-129">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="993ea-129">SECP256K1</span></span>

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

### <span data-ttu-id="993ea-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="993ea-130">-DefaultProfile</span></span>
<span data-ttu-id="993ea-131">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="993ea-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="993ea-132">-Disabled</span><span class="sxs-lookup"><span data-stu-id="993ea-132">-Disabled</span></span>
<span data-ttu-id="993ea-133">Indica che il criterio di certificato è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="993ea-133">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="993ea-134">-DnsName</span><span class="sxs-lookup"><span data-stu-id="993ea-134">-DnsName</span></span>
<span data-ttu-id="993ea-135">Specifica i nomi DNS nel certificato.</span><span class="sxs-lookup"><span data-stu-id="993ea-135">Specifies the DNS names in the certificate.</span></span> <span data-ttu-id="993ea-136">I nomi alternativi oggetto (SANs) possono essere specificati come nomi DNS.</span><span class="sxs-lookup"><span data-stu-id="993ea-136">Subject Alternative Names (SANs) can be specified as DNS names.</span></span>

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

### <span data-ttu-id="993ea-137">-EKU</span><span class="sxs-lookup"><span data-stu-id="993ea-137">-Ekus</span></span>
<span data-ttu-id="993ea-138">Specifica gli usi chiave avanzati (EKU) nel certificato.</span><span class="sxs-lookup"><span data-stu-id="993ea-138">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="993ea-139">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="993ea-139">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="993ea-140">Specifica il numero di giorni prima della scadenza in cui viene avviato il processo di notifica automatica.</span><span class="sxs-lookup"><span data-stu-id="993ea-140">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="993ea-141">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="993ea-141">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="993ea-142">Specifica la percentuale della durata dopo la quale inizia il processo automatico per la notifica.</span><span class="sxs-lookup"><span data-stu-id="993ea-142">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="993ea-143">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="993ea-143">-IssuerName</span></span>
<span data-ttu-id="993ea-144">Specifica il nome dell'autorità di certificazione per il certificato.</span><span class="sxs-lookup"><span data-stu-id="993ea-144">Specifies the name of the issuer for the certificate.</span></span>

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

### <span data-ttu-id="993ea-145">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="993ea-145">-KeyNotExportable</span></span>
<span data-ttu-id="993ea-146">Indica che la chiave non è esportabile.</span><span class="sxs-lookup"><span data-stu-id="993ea-146">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="993ea-147">-KeySize</span><span class="sxs-lookup"><span data-stu-id="993ea-147">-KeySize</span></span>
<span data-ttu-id="993ea-148">Specifica la dimensione della chiave del certificato.</span><span class="sxs-lookup"><span data-stu-id="993ea-148">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="993ea-149">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="993ea-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="993ea-150">2048</span><span class="sxs-lookup"><span data-stu-id="993ea-150">2048</span></span>
- <span data-ttu-id="993ea-151">3072</span><span class="sxs-lookup"><span data-stu-id="993ea-151">3072</span></span>
- <span data-ttu-id="993ea-152">4096</span><span class="sxs-lookup"><span data-stu-id="993ea-152">4096</span></span>
- <span data-ttu-id="993ea-153">256</span><span class="sxs-lookup"><span data-stu-id="993ea-153">256</span></span>
- <span data-ttu-id="993ea-154">384</span><span class="sxs-lookup"><span data-stu-id="993ea-154">384</span></span>
- <span data-ttu-id="993ea-155">521</span><span class="sxs-lookup"><span data-stu-id="993ea-155">521</span></span>

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

### <span data-ttu-id="993ea-156">-Tipo di digitare</span><span class="sxs-lookup"><span data-stu-id="993ea-156">-KeyType</span></span>
<span data-ttu-id="993ea-157">Specifica il tipo di chiave della chiave che consente di eseguire il backup del certificato.</span><span class="sxs-lookup"><span data-stu-id="993ea-157">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="993ea-158">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="993ea-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="993ea-159">RSA</span><span class="sxs-lookup"><span data-stu-id="993ea-159">RSA</span></span>
- <span data-ttu-id="993ea-160">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="993ea-160">RSA-HSM</span></span>
- <span data-ttu-id="993ea-161">CE</span><span class="sxs-lookup"><span data-stu-id="993ea-161">EC</span></span>
- <span data-ttu-id="993ea-162">EC-HSM</span><span class="sxs-lookup"><span data-stu-id="993ea-162">EC-HSM</span></span>

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

### <span data-ttu-id="993ea-163">-Utilizzo della sintassi</span><span class="sxs-lookup"><span data-stu-id="993ea-163">-KeyUsage</span></span>
<span data-ttu-id="993ea-164">Specifica gli usi chiave nel certificato.</span><span class="sxs-lookup"><span data-stu-id="993ea-164">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="993ea-165">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="993ea-165">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="993ea-166">Specifica il numero di giorni prima della scadenza in cui inizia il processo automatico per il rinnovo del certificato.</span><span class="sxs-lookup"><span data-stu-id="993ea-166">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="993ea-167">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="993ea-167">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="993ea-168">Specifica la percentuale della durata dopo la quale inizia il processo automatico per il rinnovo del certificato.</span><span class="sxs-lookup"><span data-stu-id="993ea-168">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="993ea-169">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="993ea-169">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="993ea-170">Indica che il certificato riutilizza la chiave durante il rinnovo.</span><span class="sxs-lookup"><span data-stu-id="993ea-170">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="993ea-171">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="993ea-171">-SecretContentType</span></span>
<span data-ttu-id="993ea-172">Specifica il tipo di contenuto del nuovo segreto del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="993ea-172">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="993ea-173">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="993ea-173">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="993ea-174">applicazione/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="993ea-174">application/x-pkcs12</span></span>
- <span data-ttu-id="993ea-175">applicazione/x-Pem-file</span><span class="sxs-lookup"><span data-stu-id="993ea-175">application/x-pem-file</span></span>

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

### <span data-ttu-id="993ea-176">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="993ea-176">-SubjectName</span></span>
<span data-ttu-id="993ea-177">Specifica il nome del soggetto del certificato.</span><span class="sxs-lookup"><span data-stu-id="993ea-177">Specifies the subject name of the certificate.</span></span> 

> [!NOTE]
> <span data-ttu-id="993ea-178">Se è necessario usare una virgola (,) o un punto (.) all'interno di una proprietà nel `SubjectName` parametro, è necessario racchiudere il campo delle proprietà tra virgolette.</span><span class="sxs-lookup"><span data-stu-id="993ea-178">If you must use a comma (,) or a period (.) within a property in the `SubjectName` parameter, you must enclose the property field in quotation marks.</span></span> <span data-ttu-id="993ea-179">Ad esempio, è possibile usare O = "contoso, Ltd."</span><span class="sxs-lookup"><span data-stu-id="993ea-179">For example, you may use O="Contoso, Ltd."</span></span> <span data-ttu-id="993ea-180">nel campo nome organizzazione.</span><span class="sxs-lookup"><span data-stu-id="993ea-180">in the Organization Name field.</span></span>

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

### <span data-ttu-id="993ea-181">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="993ea-181">-ValidityInMonths</span></span>
<span data-ttu-id="993ea-182">Specifica il numero di mesi in cui il certificato è valido.</span><span class="sxs-lookup"><span data-stu-id="993ea-182">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="993ea-183">-Confermare</span><span class="sxs-lookup"><span data-stu-id="993ea-183">-Confirm</span></span>
<span data-ttu-id="993ea-184">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="993ea-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="993ea-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="993ea-185">-WhatIf</span></span>
<span data-ttu-id="993ea-186">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="993ea-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="993ea-187">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="993ea-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="993ea-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="993ea-188">CommonParameters</span></span>
<span data-ttu-id="993ea-189">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="993ea-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="993ea-190">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="993ea-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="993ea-191">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="993ea-191">INPUTS</span></span>

### <span data-ttu-id="993ea-192">System. String</span><span class="sxs-lookup"><span data-stu-id="993ea-192">System.String</span></span>

### <span data-ttu-id="993ea-193">System. Collections. Generic. list ' 1 [[System. String, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="993ea-193">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="993ea-194">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="993ea-194">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="993ea-195">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="993ea-195">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="993ea-196">System. Collections. Generic. list ' 1 [[System. Security. Cryptography. X509Certificates. X509KeyUsageFlags, System. Security. Cryptography. X509Certificates, Version = 4.2.1.0, Culture = neutral, PublicKeyToken = b03f5f7f11d50a3a]]</span><span class="sxs-lookup"><span data-stu-id="993ea-196">System.Collections.Generic.List\`1[[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags, System.Security.Cryptography.X509Certificates, Version=4.2.1.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a]]</span></span>

## <span data-ttu-id="993ea-197">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="993ea-197">OUTPUTS</span></span>

### <span data-ttu-id="993ea-198">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="993ea-198">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="993ea-199">Note</span><span class="sxs-lookup"><span data-stu-id="993ea-199">NOTES</span></span>

## <span data-ttu-id="993ea-200">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="993ea-200">RELATED LINKS</span></span>

[<span data-ttu-id="993ea-201">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="993ea-201">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="993ea-202">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="993ea-202">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

