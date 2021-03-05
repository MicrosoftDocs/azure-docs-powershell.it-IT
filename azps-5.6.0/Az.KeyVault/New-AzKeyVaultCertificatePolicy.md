---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/powershell/module/az.keyvault/new-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: af35cef768c668663b68cfd4a21e473109883aec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001310"
---
# <span data-ttu-id="fb5a3-101">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="fb5a3-101">New-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="fb5a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb5a3-102">SYNOPSIS</span></span>
<span data-ttu-id="fb5a3-103">Crea un oggetto criterio certificato in memoria.</span><span class="sxs-lookup"><span data-stu-id="fb5a3-103">Creates an in-memory certificate policy object.</span></span>

## <span data-ttu-id="fb5a3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fb5a3-104">SYNTAX</span></span>

### <span data-ttu-id="fb5a3-105">SubjectName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fb5a3-105">SubjectName (Default)</span></span>
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

### <span data-ttu-id="fb5a3-106">DNSNames</span><span class="sxs-lookup"><span data-stu-id="fb5a3-106">DNSNames</span></span>
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

## <span data-ttu-id="fb5a3-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fb5a3-107">DESCRIPTION</span></span>
<span data-ttu-id="fb5a3-108">Il cmdlet **New-AzKeyVaultCertificatePolicy** crea un oggetto criteri certificato in memoria per il Vault delle chiavi di Azure.</span><span class="sxs-lookup"><span data-stu-id="fb5a3-108">The **New-AzKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="fb5a3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fb5a3-109">EXAMPLES</span></span>

### <span data-ttu-id="fb5a3-110">Esempio 1: Creare criteri di certificato</span><span class="sxs-lookup"><span data-stu-id="fb5a3-110">Example 1: Create a certificate policy</span></span>
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

<span data-ttu-id="fb5a3-111">Questo comando crea un criterio di certificato valido per sei mesi e riutilizza la chiave per rinnovare il certificato.</span><span class="sxs-lookup"><span data-stu-id="fb5a3-111">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

### <span data-ttu-id="fb5a3-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="fb5a3-112">Example 2</span></span>

<span data-ttu-id="fb5a3-113">Crea un oggetto criterio certificato in memoria.</span><span class="sxs-lookup"><span data-stu-id="fb5a3-113">Creates an in-memory certificate policy object.</span></span> <span data-ttu-id="fb5a3-114">(autogenerati)</span><span class="sxs-lookup"><span data-stu-id="fb5a3-114">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzKeyVaultCertificatePolicy -IssuerName 'Self' -KeyType RSA -RenewAtNumberOfDaysBeforeExpiry <Int32> -SecretContentType application/x-pkcs12 -SubjectName 'CN=contoso.com' -ValidityInMonths 6
```

### <span data-ttu-id="fb5a3-115">Esempio 3: Creare un certificato SAN (Subject Alternate Name)</span><span class="sxs-lookup"><span data-stu-id="fb5a3-115">Example 3: Create a Subject Alternate Name (or SAN) certificate</span></span>

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

<span data-ttu-id="fb5a3-116">Questo esempio crea un certificato SAN con 3 nomi DNS.</span><span class="sxs-lookup"><span data-stu-id="fb5a3-116">This example creates a SAN certificate with 3 DNS names.</span></span>

## <span data-ttu-id="fb5a3-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb5a3-117">PARAMETERS</span></span>

### <span data-ttu-id="fb5a3-118">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="fb5a3-118">-CertificateTransparency</span></span>
<span data-ttu-id="fb5a3-119">Indica se la trasparenza del certificato è abilitata per questo certificato/autorità di certificazione; se non viene specificato, il valore predefinito è "true"</span><span class="sxs-lookup"><span data-stu-id="fb5a3-119">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

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

### <span data-ttu-id="fb5a3-120">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="fb5a3-120">-CertificateType</span></span>
<span data-ttu-id="fb5a3-121">Specifica il tipo di certificato per l'autorità di certificazione.</span><span class="sxs-lookup"><span data-stu-id="fb5a3-121">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="fb5a3-122">-Curva</span><span class="sxs-lookup"><span data-stu-id="fb5a3-122">-Curve</span></span>
<span data-ttu-id="fb5a3-123">Specifica il nome della curva ellittico della chiave del certificato.</span><span class="sxs-lookup"><span data-stu-id="fb5a3-123">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="fb5a3-124">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="fb5a3-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fb5a3-125">P-256</span><span class="sxs-lookup"><span data-stu-id="fb5a3-125">P-256</span></span>
- <span data-ttu-id="fb5a3-126">P-384</span><span class="sxs-lookup"><span data-stu-id="fb5a3-126">P-384</span></span>
- <span data-ttu-id="fb5a3-127">P-521</span><span class="sxs-lookup"><span data-stu-id="fb5a3-127">P-521</span></span>
- <span data-ttu-id="fb5a3-128">P-256K</span><span class="sxs-lookup"><span data-stu-id="fb5a3-128">P-256K</span></span>
- <span data-ttu-id="fb5a3-129">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="fb5a3-129">SECP256K1</span></span>

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

### <span data-ttu-id="fb5a3-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb5a3-130">-DefaultProfile</span></span>
<span data-ttu-id="fb5a3-131">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="fb5a3-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb5a3-132">-Disabled</span><span class="sxs-lookup"><span data-stu-id="fb5a3-132">-Disabled</span></span>
<span data-ttu-id="fb5a3-133">Indica che il criterio di certificato è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="fb5a3-133">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="fb5a3-134">-DnsName</span><span class="sxs-lookup"><span data-stu-id="fb5a3-134">-DnsName</span></span>
<span data-ttu-id="fb5a3-135">Specifica i nomi DNS nel certificato.</span><span class="sxs-lookup"><span data-stu-id="fb5a3-135">Specifies the DNS names in the certificate.</span></span> <span data-ttu-id="fb5a3-136">I nomi alternativi dell'oggetto possono essere specificati come nomi DNS.</span><span class="sxs-lookup"><span data-stu-id="fb5a3-136">Subject Alternative Names (SANs) can be specified as DNS names.</span></span>

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

### <span data-ttu-id="fb5a3-137">-Ekus</span><span class="sxs-lookup"><span data-stu-id="fb5a3-137">-Ekus</span></span>
<span data-ttu-id="fb5a3-138">Specifica l'utilizzo avanzato delle chiavi (EKU) nel certificato.</span><span class="sxs-lookup"><span data-stu-id="fb5a3-138">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="fb5a3-139">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="fb5a3-139">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="fb5a3-140">Specifica quanti giorni prima della scadenza inizia il processo di notifica automatica.</span><span class="sxs-lookup"><span data-stu-id="fb5a3-140">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="fb5a3-141">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="fb5a3-141">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="fb5a3-142">Specifica la percentuale di durata dopo la quale ha inizio il processo automatico per la notifica.</span><span class="sxs-lookup"><span data-stu-id="fb5a3-142">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="fb5a3-143">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="fb5a3-143">-IssuerName</span></span>
<span data-ttu-id="fb5a3-144">Specifica il nome dell'autorità di certificazione per il certificato.</span><span class="sxs-lookup"><span data-stu-id="fb5a3-144">Specifies the name of the issuer for the certificate.</span></span>

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

### <span data-ttu-id="fb5a3-145">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="fb5a3-145">-KeyNotExportable</span></span>
<span data-ttu-id="fb5a3-146">Indica che la chiave non è esportabile.</span><span class="sxs-lookup"><span data-stu-id="fb5a3-146">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="fb5a3-147">-KeySize</span><span class="sxs-lookup"><span data-stu-id="fb5a3-147">-KeySize</span></span>
<span data-ttu-id="fb5a3-148">Specifica la dimensione chiave del certificato.</span><span class="sxs-lookup"><span data-stu-id="fb5a3-148">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="fb5a3-149">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="fb5a3-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fb5a3-150">2048</span><span class="sxs-lookup"><span data-stu-id="fb5a3-150">2048</span></span>
- <span data-ttu-id="fb5a3-151">3072</span><span class="sxs-lookup"><span data-stu-id="fb5a3-151">3072</span></span>
- <span data-ttu-id="fb5a3-152">4096</span><span class="sxs-lookup"><span data-stu-id="fb5a3-152">4096</span></span>
- <span data-ttu-id="fb5a3-153">256</span><span class="sxs-lookup"><span data-stu-id="fb5a3-153">256</span></span>
- <span data-ttu-id="fb5a3-154">384</span><span class="sxs-lookup"><span data-stu-id="fb5a3-154">384</span></span>
- <span data-ttu-id="fb5a3-155">521</span><span class="sxs-lookup"><span data-stu-id="fb5a3-155">521</span></span>

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

### <span data-ttu-id="fb5a3-156">-KeyType</span><span class="sxs-lookup"><span data-stu-id="fb5a3-156">-KeyType</span></span>
<span data-ttu-id="fb5a3-157">Specifica il tipo di chiave della chiave che contiene il certificato.</span><span class="sxs-lookup"><span data-stu-id="fb5a3-157">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="fb5a3-158">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="fb5a3-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fb5a3-159">RSA</span><span class="sxs-lookup"><span data-stu-id="fb5a3-159">RSA</span></span>
- <span data-ttu-id="fb5a3-160">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="fb5a3-160">RSA-HSM</span></span>
- <span data-ttu-id="fb5a3-161">Ec</span><span class="sxs-lookup"><span data-stu-id="fb5a3-161">EC</span></span>
- <span data-ttu-id="fb5a3-162">EC-HSM</span><span class="sxs-lookup"><span data-stu-id="fb5a3-162">EC-HSM</span></span>

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

### <span data-ttu-id="fb5a3-163">-KeyUsage</span><span class="sxs-lookup"><span data-stu-id="fb5a3-163">-KeyUsage</span></span>
<span data-ttu-id="fb5a3-164">Specifica gli utilizzi delle chiavi nel certificato.</span><span class="sxs-lookup"><span data-stu-id="fb5a3-164">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="fb5a3-165">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="fb5a3-165">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="fb5a3-166">Specifica il numero di giorni prima della scadenza dopo il quale ha inizio il processo automatico di rinnovo del certificato.</span><span class="sxs-lookup"><span data-stu-id="fb5a3-166">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="fb5a3-167">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="fb5a3-167">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="fb5a3-168">Specifica la percentuale di durata dopo la quale ha inizio il processo automatico di rinnovo del certificato.</span><span class="sxs-lookup"><span data-stu-id="fb5a3-168">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="fb5a3-169">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="fb5a3-169">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="fb5a3-170">Indica che il certificato viene riutilizzato durante il rinnovo.</span><span class="sxs-lookup"><span data-stu-id="fb5a3-170">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="fb5a3-171">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="fb5a3-171">-SecretContentType</span></span>
<span data-ttu-id="fb5a3-172">Specifica il tipo di contenuto del nuovo segreto vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="fb5a3-172">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="fb5a3-173">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="fb5a3-173">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fb5a3-174">application/x-pkcs12</span><span class="sxs-lookup"><span data-stu-id="fb5a3-174">application/x-pkcs12</span></span>
- <span data-ttu-id="fb5a3-175">application/x-pem-file</span><span class="sxs-lookup"><span data-stu-id="fb5a3-175">application/x-pem-file</span></span>

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

### <span data-ttu-id="fb5a3-176">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="fb5a3-176">-SubjectName</span></span>
<span data-ttu-id="fb5a3-177">Specifica il nome dell'oggetto del certificato.</span><span class="sxs-lookup"><span data-stu-id="fb5a3-177">Specifies the subject name of the certificate.</span></span> 

> [!NOTE]
> <span data-ttu-id="fb5a3-178">Se è necessario usare una virgola (,) o un punto (.) all'interno di una proprietà nel parametro, è necessario racchiudere il campo della proprietà `SubjectName` tra virgolette.</span><span class="sxs-lookup"><span data-stu-id="fb5a3-178">If you must use a comma (,) or a period (.) within a property in the `SubjectName` parameter, you must enclose the property field in quotation marks.</span></span> <span data-ttu-id="fb5a3-179">Ad esempio, è possibile usare O="Contoso, Ltd."</span><span class="sxs-lookup"><span data-stu-id="fb5a3-179">For example, you may use O="Contoso, Ltd."</span></span> <span data-ttu-id="fb5a3-180">nel campo Nome organizzazione.</span><span class="sxs-lookup"><span data-stu-id="fb5a3-180">in the Organization Name field.</span></span>

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

### <span data-ttu-id="fb5a3-181">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="fb5a3-181">-ValidityInMonths</span></span>
<span data-ttu-id="fb5a3-182">Specifica il numero di mesi per cui il certificato è valido.</span><span class="sxs-lookup"><span data-stu-id="fb5a3-182">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="fb5a3-183">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fb5a3-183">-Confirm</span></span>
<span data-ttu-id="fb5a3-184">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb5a3-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb5a3-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb5a3-185">-WhatIf</span></span>
<span data-ttu-id="fb5a3-186">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fb5a3-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb5a3-187">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fb5a3-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb5a3-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb5a3-188">CommonParameters</span></span>
<span data-ttu-id="fb5a3-189">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb5a3-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb5a3-190">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fb5a3-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb5a3-191">INPUT</span><span class="sxs-lookup"><span data-stu-id="fb5a3-191">INPUTS</span></span>

### <span data-ttu-id="fb5a3-192">System.String</span><span class="sxs-lookup"><span data-stu-id="fb5a3-192">System.String</span></span>

### <span data-ttu-id="fb5a3-193">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fb5a3-193">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="fb5a3-194">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fb5a3-194">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="fb5a3-195">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fb5a3-195">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="fb5a3-196">System.Collections.Generic.List'1[[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags, System.Security.Cryptography.X509Certificates, Version=4.2.1.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a]]</span><span class="sxs-lookup"><span data-stu-id="fb5a3-196">System.Collections.Generic.List\`1[[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags, System.Security.Cryptography.X509Certificates, Version=4.2.1.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a]]</span></span>

## <span data-ttu-id="fb5a3-197">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fb5a3-197">OUTPUTS</span></span>

### <span data-ttu-id="fb5a3-198">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="fb5a3-198">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="fb5a3-199">NOTE</span><span class="sxs-lookup"><span data-stu-id="fb5a3-199">NOTES</span></span>

## <span data-ttu-id="fb5a3-200">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fb5a3-200">RELATED LINKS</span></span>

[<span data-ttu-id="fb5a3-201">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="fb5a3-201">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="fb5a3-202">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="fb5a3-202">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

