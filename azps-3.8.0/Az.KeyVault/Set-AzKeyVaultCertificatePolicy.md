---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 5a6b88ce85b8b9296d9666955a93d1240b631634
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020500"
---
# <span data-ttu-id="f159b-101">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="f159b-101">Set-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="f159b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f159b-102">SYNOPSIS</span></span>
<span data-ttu-id="f159b-103">Crea o aggiorna i criteri per un certificato in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="f159b-103">Creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="f159b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f159b-104">SYNTAX</span></span>

### <span data-ttu-id="f159b-105">ExpandedRenewPercentage (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f159b-105">ExpandedRenewPercentage (Default)</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-RenewAtPercentageLifetime <Int32>]
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeySize <Int32>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-Curve <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f159b-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="f159b-106">ByValue</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-InputObject] <PSKeyVaultCertificatePolicy> [-EmailAtNumberOfDaysBeforeExpiry <Int32>]
 [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>] [-KeySize <Int32>]
 [-CertificateTransparency <Boolean>] [-PassThru] [-Curve <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f159b-107">ExpandedRenewNumber</span><span class="sxs-lookup"><span data-stu-id="f159b-107">ExpandedRenewNumber</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> -RenewAtNumberOfDaysBeforeExpiry <Int32>
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeySize <Int32>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-Curve <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f159b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f159b-108">DESCRIPTION</span></span>
<span data-ttu-id="f159b-109">Il cmdlet **set-AzKeyVaultCertificatePolicy** crea o aggiorna i criteri per un certificato in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="f159b-109">The **Set-AzKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="f159b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f159b-110">EXAMPLES</span></span>

### <span data-ttu-id="f159b-111">Esempio 1: impostare un criterio di certificato</span><span class="sxs-lookup"><span data-stu-id="f159b-111">Example 1: Set a certificate policy</span></span>
```powershell
PS C:\> Set-AzKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True -PassThru

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

<span data-ttu-id="f159b-112">Questo comando imposta i criteri per il certificato TestCert01 nel Vault della chiave ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="f159b-112">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="f159b-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f159b-113">PARAMETERS</span></span>

### <span data-ttu-id="f159b-114">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="f159b-114">-CertificateTransparency</span></span>
<span data-ttu-id="f159b-115">Indica se la trasparenza del certificato è abilitata per il certificato/emittente; Se non viene specificato, il valore predefinito è "true"</span><span class="sxs-lookup"><span data-stu-id="f159b-115">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

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

### <span data-ttu-id="f159b-116">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="f159b-116">-CertificateType</span></span>
<span data-ttu-id="f159b-117">Specifica il tipo di certificato per l'emittente.</span><span class="sxs-lookup"><span data-stu-id="f159b-117">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f159b-118">-Curva</span><span class="sxs-lookup"><span data-stu-id="f159b-118">-Curve</span></span>
<span data-ttu-id="f159b-119">Specifica il nome della curva ellittica della chiave del certificato.</span><span class="sxs-lookup"><span data-stu-id="f159b-119">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="f159b-120">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f159b-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f159b-121">P-256</span><span class="sxs-lookup"><span data-stu-id="f159b-121">P-256</span></span>
- <span data-ttu-id="f159b-122">P-384</span><span class="sxs-lookup"><span data-stu-id="f159b-122">P-384</span></span>
- <span data-ttu-id="f159b-123">P-521</span><span class="sxs-lookup"><span data-stu-id="f159b-123">P-521</span></span>
- <span data-ttu-id="f159b-124">P-256K</span><span class="sxs-lookup"><span data-stu-id="f159b-124">P-256K</span></span>
- <span data-ttu-id="f159b-125">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="f159b-125">SECP256K1</span></span>

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

### <span data-ttu-id="f159b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f159b-126">-DefaultProfile</span></span>
<span data-ttu-id="f159b-127">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f159b-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f159b-128">-Disabled</span><span class="sxs-lookup"><span data-stu-id="f159b-128">-Disabled</span></span>
<span data-ttu-id="f159b-129">Indica che il criterio di certificato è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="f159b-129">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f159b-130">-DnsName</span><span class="sxs-lookup"><span data-stu-id="f159b-130">-DnsName</span></span>
<span data-ttu-id="f159b-131">Specifica il nome del soggetto del certificato.</span><span class="sxs-lookup"><span data-stu-id="f159b-131">Specifies the subject name of the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases: DnsNames

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f159b-132">-EKU</span><span class="sxs-lookup"><span data-stu-id="f159b-132">-Ekus</span></span>
<span data-ttu-id="f159b-133">Specifica gli usi chiave avanzati (EKU) nel certificato.</span><span class="sxs-lookup"><span data-stu-id="f159b-133">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f159b-134">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="f159b-134">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="f159b-135">Specifica il numero di giorni prima della scadenza quando deve iniziare il rinnovo automatico.</span><span class="sxs-lookup"><span data-stu-id="f159b-135">Specifies the number of days before expiration when automatic renewal should start.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f159b-136">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="f159b-136">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="f159b-137">Specifica la percentuale della durata dopo la quale inizia il processo automatico per la notifica.</span><span class="sxs-lookup"><span data-stu-id="f159b-137">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f159b-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f159b-138">-InputObject</span></span>
<span data-ttu-id="f159b-139">Specifica i criteri di certificato.</span><span class="sxs-lookup"><span data-stu-id="f159b-139">Specifies the certificate policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy
Parameter Sets: ByValue
Aliases: CertificatePolicy

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f159b-140">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="f159b-140">-IssuerName</span></span>
<span data-ttu-id="f159b-141">Specifica il nome dell'autorità di certificazione per il certificato.</span><span class="sxs-lookup"><span data-stu-id="f159b-141">Specifies the name of the issuer for this certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f159b-142">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="f159b-142">-KeyNotExportable</span></span>
<span data-ttu-id="f159b-143">Indica che la chiave non è esportabile.</span><span class="sxs-lookup"><span data-stu-id="f159b-143">Indicates that the key is not exportable.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f159b-144">-KeySize</span><span class="sxs-lookup"><span data-stu-id="f159b-144">-KeySize</span></span>
<span data-ttu-id="f159b-145">Specifica la dimensione della chiave del certificato.</span><span class="sxs-lookup"><span data-stu-id="f159b-145">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="f159b-146">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f159b-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f159b-147">2048</span><span class="sxs-lookup"><span data-stu-id="f159b-147">2048</span></span>
- <span data-ttu-id="f159b-148">3072</span><span class="sxs-lookup"><span data-stu-id="f159b-148">3072</span></span>
- <span data-ttu-id="f159b-149">4096</span><span class="sxs-lookup"><span data-stu-id="f159b-149">4096</span></span>
- <span data-ttu-id="f159b-150">256</span><span class="sxs-lookup"><span data-stu-id="f159b-150">256</span></span>
- <span data-ttu-id="f159b-151">384</span><span class="sxs-lookup"><span data-stu-id="f159b-151">384</span></span>
- <span data-ttu-id="f159b-152">521</span><span class="sxs-lookup"><span data-stu-id="f159b-152">521</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:
Accepted values: 2048, 3072, 4096, 256, 384, 521

Required: False
Position: Named
Default value: 2048
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f159b-153">-Tipo di digitare</span><span class="sxs-lookup"><span data-stu-id="f159b-153">-KeyType</span></span>
<span data-ttu-id="f159b-154">Specifica il tipo di chiave della chiave che consente di eseguire il backup del certificato.</span><span class="sxs-lookup"><span data-stu-id="f159b-154">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="f159b-155">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f159b-155">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f159b-156">RSA</span><span class="sxs-lookup"><span data-stu-id="f159b-156">RSA</span></span>
- <span data-ttu-id="f159b-157">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="f159b-157">RSA-HSM</span></span>
- <span data-ttu-id="f159b-158">CE</span><span class="sxs-lookup"><span data-stu-id="f159b-158">EC</span></span>
- <span data-ttu-id="f159b-159">EC-HSM</span><span class="sxs-lookup"><span data-stu-id="f159b-159">EC-HSM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA, RSA-HSM, EC, EC-HSM

Required: False
Position: Named
Default value: RSA
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f159b-160">-Utilizzo della sintassi</span><span class="sxs-lookup"><span data-stu-id="f159b-160">-KeyUsage</span></span>
<span data-ttu-id="f159b-161">Specifica gli usi chiave nel certificato.</span><span class="sxs-lookup"><span data-stu-id="f159b-161">Specifies the key usages in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:
Accepted values: None, EncipherOnly, CrlSign, KeyCertSign, KeyAgreement, DataEncipherment, KeyEncipherment, NonRepudiation, DigitalSignature, DecipherOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f159b-162">-Nome</span><span class="sxs-lookup"><span data-stu-id="f159b-162">-Name</span></span>
<span data-ttu-id="f159b-163">Specifica il nome del certificato.</span><span class="sxs-lookup"><span data-stu-id="f159b-163">Specifies the name of the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f159b-164">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f159b-164">-PassThru</span></span>
<span data-ttu-id="f159b-165">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="f159b-165">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f159b-166">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="f159b-166">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f159b-167">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="f159b-167">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="f159b-168">Specifica il numero di giorni prima della scadenza in cui inizia il processo automatico per il rinnovo del certificato.</span><span class="sxs-lookup"><span data-stu-id="f159b-168">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ExpandedRenewNumber
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f159b-169">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="f159b-169">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="f159b-170">Specifica la percentuale della durata dopo la quale inizia il processo automatico per il rinnovo del certificato.</span><span class="sxs-lookup"><span data-stu-id="f159b-170">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ExpandedRenewPercentage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f159b-171">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="f159b-171">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="f159b-172">Indica che il certificato riutilizza la chiave durante il rinnovo.</span><span class="sxs-lookup"><span data-stu-id="f159b-172">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f159b-173">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="f159b-173">-SecretContentType</span></span>
<span data-ttu-id="f159b-174">Specifica il tipo di contenuto del nuovo segreto del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="f159b-174">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="f159b-175">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f159b-175">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f159b-176">applicazione/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="f159b-176">application/x-pkcs12</span></span>
- <span data-ttu-id="f159b-177">applicazione/x-Pem-file</span><span class="sxs-lookup"><span data-stu-id="f159b-177">application/x-pem-file</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f159b-178">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="f159b-178">-SubjectName</span></span>
<span data-ttu-id="f159b-179">Specifica il nome del soggetto del certificato.</span><span class="sxs-lookup"><span data-stu-id="f159b-179">Specifies the subject name of the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f159b-180">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="f159b-180">-ValidityInMonths</span></span>
<span data-ttu-id="f159b-181">Specifica il numero di mesi in cui il certificato è valido.</span><span class="sxs-lookup"><span data-stu-id="f159b-181">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f159b-182">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="f159b-182">-VaultName</span></span>
<span data-ttu-id="f159b-183">Specifica il nome di un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="f159b-183">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f159b-184">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f159b-184">-Confirm</span></span>
<span data-ttu-id="f159b-185">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f159b-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f159b-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f159b-186">-WhatIf</span></span>
<span data-ttu-id="f159b-187">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f159b-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f159b-188">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f159b-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f159b-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f159b-189">CommonParameters</span></span>
<span data-ttu-id="f159b-190">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f159b-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f159b-191">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f159b-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f159b-192">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f159b-192">INPUTS</span></span>

### <span data-ttu-id="f159b-193">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="f159b-193">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="f159b-194">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f159b-194">OUTPUTS</span></span>

### <span data-ttu-id="f159b-195">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="f159b-195">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="f159b-196">Note</span><span class="sxs-lookup"><span data-stu-id="f159b-196">NOTES</span></span>

## <span data-ttu-id="f159b-197">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f159b-197">RELATED LINKS</span></span>

[<span data-ttu-id="f159b-198">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="f159b-198">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="f159b-199">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="f159b-199">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

