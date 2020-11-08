---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 963a7005e95941a644b35a57f80b558f02e2d6a0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189845"
---
# <span data-ttu-id="0a2b2-101">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="0a2b2-101">Set-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="0a2b2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0a2b2-102">SYNOPSIS</span></span>
<span data-ttu-id="0a2b2-103">Crea o aggiorna i criteri per un certificato in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="0a2b2-103">Creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="0a2b2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0a2b2-104">SYNTAX</span></span>

### <span data-ttu-id="0a2b2-105">ExpandedRenewPercentage (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0a2b2-105">ExpandedRenewPercentage (Default)</span></span>
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

### <span data-ttu-id="0a2b2-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="0a2b2-106">ByValue</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-InputObject] <PSKeyVaultCertificatePolicy> [-EmailAtNumberOfDaysBeforeExpiry <Int32>]
 [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>] [-KeySize <Int32>]
 [-CertificateTransparency <Boolean>] [-PassThru] [-Curve <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a2b2-107">ExpandedRenewNumber</span><span class="sxs-lookup"><span data-stu-id="0a2b2-107">ExpandedRenewNumber</span></span>
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

## <span data-ttu-id="0a2b2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0a2b2-108">DESCRIPTION</span></span>
<span data-ttu-id="0a2b2-109">Il cmdlet **set-AzKeyVaultCertificatePolicy** crea o aggiorna i criteri per un certificato in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="0a2b2-109">The **Set-AzKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="0a2b2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0a2b2-110">EXAMPLES</span></span>

### <span data-ttu-id="0a2b2-111">Esempio 1: impostare un criterio di certificato</span><span class="sxs-lookup"><span data-stu-id="0a2b2-111">Example 1: Set a certificate policy</span></span>
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

<span data-ttu-id="0a2b2-112">Questo comando imposta i criteri per il certificato TestCert01 nel Vault della chiave ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="0a2b2-112">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="0a2b2-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0a2b2-113">PARAMETERS</span></span>

### <span data-ttu-id="0a2b2-114">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="0a2b2-114">-CertificateTransparency</span></span>
<span data-ttu-id="0a2b2-115">Indica se la trasparenza del certificato è abilitata per il certificato/emittente; Se non viene specificato, il valore predefinito è "true".</span><span class="sxs-lookup"><span data-stu-id="0a2b2-115">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'.</span></span>
<span data-ttu-id="0a2b2-116">`-IssuerName` deve essere specificato durante l'impostazione di questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="0a2b2-116">`-IssuerName` needs to be specified when setting this property.</span></span>

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

### <span data-ttu-id="0a2b2-117">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="0a2b2-117">-CertificateType</span></span>
<span data-ttu-id="0a2b2-118">Specifica il tipo di certificato per l'emittente.</span><span class="sxs-lookup"><span data-stu-id="0a2b2-118">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="0a2b2-119">-Curva</span><span class="sxs-lookup"><span data-stu-id="0a2b2-119">-Curve</span></span>
<span data-ttu-id="0a2b2-120">Specifica il nome della curva ellittica della chiave del certificato.</span><span class="sxs-lookup"><span data-stu-id="0a2b2-120">Specifies the elliptic curve name of the key of the certificate.</span></span>
<span data-ttu-id="0a2b2-121">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="0a2b2-121">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0a2b2-122">P-256</span><span class="sxs-lookup"><span data-stu-id="0a2b2-122">P-256</span></span>
- <span data-ttu-id="0a2b2-123">P-384</span><span class="sxs-lookup"><span data-stu-id="0a2b2-123">P-384</span></span>
- <span data-ttu-id="0a2b2-124">P-521</span><span class="sxs-lookup"><span data-stu-id="0a2b2-124">P-521</span></span>
- <span data-ttu-id="0a2b2-125">P-256K</span><span class="sxs-lookup"><span data-stu-id="0a2b2-125">P-256K</span></span>
- <span data-ttu-id="0a2b2-126">SECP256K1</span><span class="sxs-lookup"><span data-stu-id="0a2b2-126">SECP256K1</span></span>

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

### <span data-ttu-id="0a2b2-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a2b2-127">-DefaultProfile</span></span>
<span data-ttu-id="0a2b2-128">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0a2b2-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0a2b2-129">-Disabled</span><span class="sxs-lookup"><span data-stu-id="0a2b2-129">-Disabled</span></span>
<span data-ttu-id="0a2b2-130">Indica che il criterio di certificato è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="0a2b2-130">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="0a2b2-131">-DnsName</span><span class="sxs-lookup"><span data-stu-id="0a2b2-131">-DnsName</span></span>
<span data-ttu-id="0a2b2-132">Specifica il nome del soggetto del certificato.</span><span class="sxs-lookup"><span data-stu-id="0a2b2-132">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="0a2b2-133">-EKU</span><span class="sxs-lookup"><span data-stu-id="0a2b2-133">-Ekus</span></span>
<span data-ttu-id="0a2b2-134">Specifica gli usi chiave avanzati (EKU) nel certificato.</span><span class="sxs-lookup"><span data-stu-id="0a2b2-134">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="0a2b2-135">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="0a2b2-135">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="0a2b2-136">Specifica il numero di giorni prima della scadenza quando deve iniziare il rinnovo automatico.</span><span class="sxs-lookup"><span data-stu-id="0a2b2-136">Specifies the number of days before expiration when automatic renewal should start.</span></span>

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

### <span data-ttu-id="0a2b2-137">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="0a2b2-137">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="0a2b2-138">Specifica la percentuale della durata dopo la quale inizia il processo automatico per la notifica.</span><span class="sxs-lookup"><span data-stu-id="0a2b2-138">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="0a2b2-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a2b2-139">-InputObject</span></span>
<span data-ttu-id="0a2b2-140">Specifica i criteri di certificato.</span><span class="sxs-lookup"><span data-stu-id="0a2b2-140">Specifies the certificate policy.</span></span>

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

### <span data-ttu-id="0a2b2-141">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="0a2b2-141">-IssuerName</span></span>
<span data-ttu-id="0a2b2-142">Specifica il nome dell'autorità di certificazione per il certificato.</span><span class="sxs-lookup"><span data-stu-id="0a2b2-142">Specifies the name of the issuer for this certificate.</span></span>

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

### <span data-ttu-id="0a2b2-143">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="0a2b2-143">-KeyNotExportable</span></span>
<span data-ttu-id="0a2b2-144">Indica che la chiave non è esportabile.</span><span class="sxs-lookup"><span data-stu-id="0a2b2-144">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="0a2b2-145">-KeySize</span><span class="sxs-lookup"><span data-stu-id="0a2b2-145">-KeySize</span></span>
<span data-ttu-id="0a2b2-146">Specifica la dimensione della chiave del certificato.</span><span class="sxs-lookup"><span data-stu-id="0a2b2-146">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="0a2b2-147">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="0a2b2-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0a2b2-148">2048</span><span class="sxs-lookup"><span data-stu-id="0a2b2-148">2048</span></span>
- <span data-ttu-id="0a2b2-149">3072</span><span class="sxs-lookup"><span data-stu-id="0a2b2-149">3072</span></span>
- <span data-ttu-id="0a2b2-150">4096</span><span class="sxs-lookup"><span data-stu-id="0a2b2-150">4096</span></span>
- <span data-ttu-id="0a2b2-151">256</span><span class="sxs-lookup"><span data-stu-id="0a2b2-151">256</span></span>
- <span data-ttu-id="0a2b2-152">384</span><span class="sxs-lookup"><span data-stu-id="0a2b2-152">384</span></span>
- <span data-ttu-id="0a2b2-153">521</span><span class="sxs-lookup"><span data-stu-id="0a2b2-153">521</span></span>

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

### <span data-ttu-id="0a2b2-154">-Tipo di digitare</span><span class="sxs-lookup"><span data-stu-id="0a2b2-154">-KeyType</span></span>
<span data-ttu-id="0a2b2-155">Specifica il tipo di chiave della chiave che consente di eseguire il backup del certificato.</span><span class="sxs-lookup"><span data-stu-id="0a2b2-155">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="0a2b2-156">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="0a2b2-156">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0a2b2-157">RSA</span><span class="sxs-lookup"><span data-stu-id="0a2b2-157">RSA</span></span>
- <span data-ttu-id="0a2b2-158">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="0a2b2-158">RSA-HSM</span></span>
- <span data-ttu-id="0a2b2-159">CE</span><span class="sxs-lookup"><span data-stu-id="0a2b2-159">EC</span></span>
- <span data-ttu-id="0a2b2-160">EC-HSM</span><span class="sxs-lookup"><span data-stu-id="0a2b2-160">EC-HSM</span></span>

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

### <span data-ttu-id="0a2b2-161">-Utilizzo della sintassi</span><span class="sxs-lookup"><span data-stu-id="0a2b2-161">-KeyUsage</span></span>
<span data-ttu-id="0a2b2-162">Specifica gli usi chiave nel certificato.</span><span class="sxs-lookup"><span data-stu-id="0a2b2-162">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="0a2b2-163">-Nome</span><span class="sxs-lookup"><span data-stu-id="0a2b2-163">-Name</span></span>
<span data-ttu-id="0a2b2-164">Specifica il nome del certificato.</span><span class="sxs-lookup"><span data-stu-id="0a2b2-164">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="0a2b2-165">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0a2b2-165">-PassThru</span></span>
<span data-ttu-id="0a2b2-166">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="0a2b2-166">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0a2b2-167">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="0a2b2-167">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0a2b2-168">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="0a2b2-168">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="0a2b2-169">Specifica il numero di giorni prima della scadenza in cui inizia il processo automatico per il rinnovo del certificato.</span><span class="sxs-lookup"><span data-stu-id="0a2b2-169">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="0a2b2-170">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="0a2b2-170">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="0a2b2-171">Specifica la percentuale della durata dopo la quale inizia il processo automatico per il rinnovo del certificato.</span><span class="sxs-lookup"><span data-stu-id="0a2b2-171">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="0a2b2-172">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="0a2b2-172">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="0a2b2-173">Indica che il certificato riutilizza la chiave durante il rinnovo.</span><span class="sxs-lookup"><span data-stu-id="0a2b2-173">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="0a2b2-174">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="0a2b2-174">-SecretContentType</span></span>
<span data-ttu-id="0a2b2-175">Specifica il tipo di contenuto del nuovo segreto del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="0a2b2-175">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="0a2b2-176">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="0a2b2-176">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0a2b2-177">applicazione/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="0a2b2-177">application/x-pkcs12</span></span>
- <span data-ttu-id="0a2b2-178">applicazione/x-Pem-file</span><span class="sxs-lookup"><span data-stu-id="0a2b2-178">application/x-pem-file</span></span>

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

### <span data-ttu-id="0a2b2-179">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="0a2b2-179">-SubjectName</span></span>
<span data-ttu-id="0a2b2-180">Specifica il nome del soggetto del certificato.</span><span class="sxs-lookup"><span data-stu-id="0a2b2-180">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="0a2b2-181">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="0a2b2-181">-ValidityInMonths</span></span>
<span data-ttu-id="0a2b2-182">Specifica il numero di mesi in cui il certificato è valido.</span><span class="sxs-lookup"><span data-stu-id="0a2b2-182">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="0a2b2-183">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="0a2b2-183">-VaultName</span></span>
<span data-ttu-id="0a2b2-184">Specifica il nome di un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="0a2b2-184">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="0a2b2-185">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0a2b2-185">-Confirm</span></span>
<span data-ttu-id="0a2b2-186">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a2b2-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a2b2-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a2b2-187">-WhatIf</span></span>
<span data-ttu-id="0a2b2-188">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0a2b2-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a2b2-189">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0a2b2-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a2b2-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a2b2-190">CommonParameters</span></span>
<span data-ttu-id="0a2b2-191">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a2b2-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a2b2-192">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0a2b2-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a2b2-193">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0a2b2-193">INPUTS</span></span>

### <span data-ttu-id="0a2b2-194">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="0a2b2-194">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="0a2b2-195">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0a2b2-195">OUTPUTS</span></span>

### <span data-ttu-id="0a2b2-196">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="0a2b2-196">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="0a2b2-197">Note</span><span class="sxs-lookup"><span data-stu-id="0a2b2-197">NOTES</span></span>

## <span data-ttu-id="0a2b2-198">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0a2b2-198">RELATED LINKS</span></span>

[<span data-ttu-id="0a2b2-199">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="0a2b2-199">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="0a2b2-200">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="0a2b2-200">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)
