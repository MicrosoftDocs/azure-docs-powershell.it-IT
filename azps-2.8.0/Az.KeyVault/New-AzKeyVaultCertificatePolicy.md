---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 262c539d9ff97983494de0951c9a5d47510b0d28
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674143"
---
# <span data-ttu-id="abc4a-101">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="abc4a-101">New-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="abc4a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="abc4a-102">SYNOPSIS</span></span>
<span data-ttu-id="abc4a-103">Crea un oggetto Criteri di certificato in memoria.</span><span class="sxs-lookup"><span data-stu-id="abc4a-103">Creates an in-memory certificate policy object.</span></span>

## <span data-ttu-id="abc4a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="abc4a-104">SYNTAX</span></span>

### <span data-ttu-id="abc4a-105">SubjectName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="abc4a-105">SubjectName (Default)</span></span>
```
New-AzKeyVaultCertificatePolicy [-IssuerName] <String> [-SubjectName] <String>
 [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>]
 [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeySize <Int32>] [-KeyType <String>] [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="abc4a-106">DNSNames</span><span class="sxs-lookup"><span data-stu-id="abc4a-106">DNSNames</span></span>
```
New-AzKeyVaultCertificatePolicy [-IssuerName] <String> [[-SubjectName] <String>]
 [-DnsName] <System.Collections.Generic.List`1[System.String]> [-RenewAtNumberOfDaysBeforeExpiry <Int32>]
 [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeySize <Int32>] [-KeyType <String>] [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="abc4a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="abc4a-107">DESCRIPTION</span></span>
<span data-ttu-id="abc4a-108">Il cmdlet **New-AzKeyVaultCertificatePolicy** crea un oggetto Criteri di certificato in memoria per Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="abc4a-108">The **New-AzKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="abc4a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="abc4a-109">EXAMPLES</span></span>

### <span data-ttu-id="abc4a-110">Esempio 1: creare un criterio di certificato</span><span class="sxs-lookup"><span data-stu-id="abc4a-110">Example 1: Create a certificate policy</span></span>
```powershell
PS C:\> New-AzKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal

SecretContentType               : application/x-pkcs12
Kty                             :
KeySize                         : 2048
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

<span data-ttu-id="abc4a-111">Questo comando crea un criterio di certificato valido per sei mesi e riutilizza la chiave per rinnovare il certificato.</span><span class="sxs-lookup"><span data-stu-id="abc4a-111">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="abc4a-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="abc4a-112">PARAMETERS</span></span>

### <span data-ttu-id="abc4a-113">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="abc4a-113">-CertificateType</span></span>
<span data-ttu-id="abc4a-114">Specifica il tipo di certificato per l'emittente.</span><span class="sxs-lookup"><span data-stu-id="abc4a-114">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="abc4a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abc4a-115">-DefaultProfile</span></span>
<span data-ttu-id="abc4a-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="abc4a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="abc4a-117">-Disabled</span><span class="sxs-lookup"><span data-stu-id="abc4a-117">-Disabled</span></span>
<span data-ttu-id="abc4a-118">Indica che il criterio di certificato è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="abc4a-118">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="abc4a-119">-DnsName</span><span class="sxs-lookup"><span data-stu-id="abc4a-119">-DnsName</span></span>
<span data-ttu-id="abc4a-120">Specifica i nomi DNS nel certificato.</span><span class="sxs-lookup"><span data-stu-id="abc4a-120">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="abc4a-121">-EKU</span><span class="sxs-lookup"><span data-stu-id="abc4a-121">-Ekus</span></span>
<span data-ttu-id="abc4a-122">Specifica gli usi chiave avanzati (EKU) nel certificato.</span><span class="sxs-lookup"><span data-stu-id="abc4a-122">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="abc4a-123">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="abc4a-123">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="abc4a-124">Specifica il numero di giorni prima della scadenza in cui viene avviato il processo di notifica automatica.</span><span class="sxs-lookup"><span data-stu-id="abc4a-124">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="abc4a-125">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="abc4a-125">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="abc4a-126">Specifica la percentuale della durata dopo la quale inizia il processo automatico per la notifica.</span><span class="sxs-lookup"><span data-stu-id="abc4a-126">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="abc4a-127">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="abc4a-127">-IssuerName</span></span>
<span data-ttu-id="abc4a-128">Specifica il nome dell'autorità di certificazione per il certificato.</span><span class="sxs-lookup"><span data-stu-id="abc4a-128">Specifies the name of the issuer for the certificate.</span></span>

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

### <span data-ttu-id="abc4a-129">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="abc4a-129">-KeyNotExportable</span></span>
<span data-ttu-id="abc4a-130">Indica che la chiave non è esportabile.</span><span class="sxs-lookup"><span data-stu-id="abc4a-130">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="abc4a-131">-KeySize</span><span class="sxs-lookup"><span data-stu-id="abc4a-131">-KeySize</span></span>
<span data-ttu-id="abc4a-132">Specifica la dimensione della chiave del certificato.</span><span class="sxs-lookup"><span data-stu-id="abc4a-132">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="abc4a-133">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="abc4a-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="abc4a-134">2048</span><span class="sxs-lookup"><span data-stu-id="abc4a-134">2048</span></span>
- <span data-ttu-id="abc4a-135">3072</span><span class="sxs-lookup"><span data-stu-id="abc4a-135">3072</span></span>
- <span data-ttu-id="abc4a-136">4096</span><span class="sxs-lookup"><span data-stu-id="abc4a-136">4096</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:
Accepted values: 2048, 3072, 4096

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abc4a-137">-Tipo di digitare</span><span class="sxs-lookup"><span data-stu-id="abc4a-137">-KeyType</span></span>
<span data-ttu-id="abc4a-138">Specifica il tipo di chiave della chiave che consente di eseguire il backup del certificato.</span><span class="sxs-lookup"><span data-stu-id="abc4a-138">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="abc4a-139">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="abc4a-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="abc4a-140">RSA</span><span class="sxs-lookup"><span data-stu-id="abc4a-140">RSA</span></span>
- <span data-ttu-id="abc4a-141">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="abc4a-141">RSA-HSM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA, RSA-HSM

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abc4a-142">-Utilizzo della sintassi</span><span class="sxs-lookup"><span data-stu-id="abc4a-142">-KeyUsage</span></span>
<span data-ttu-id="abc4a-143">Specifica gli usi chiave nel certificato.</span><span class="sxs-lookup"><span data-stu-id="abc4a-143">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="abc4a-144">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="abc4a-144">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="abc4a-145">Specifica il numero di giorni prima della scadenza in cui inizia il processo automatico per il rinnovo del certificato.</span><span class="sxs-lookup"><span data-stu-id="abc4a-145">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="abc4a-146">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="abc4a-146">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="abc4a-147">Specifica la percentuale della durata dopo la quale inizia il processo automatico per il rinnovo del certificato.</span><span class="sxs-lookup"><span data-stu-id="abc4a-147">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="abc4a-148">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="abc4a-148">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="abc4a-149">Indica che il certificato riutilizza la chiave durante il rinnovo.</span><span class="sxs-lookup"><span data-stu-id="abc4a-149">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="abc4a-150">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="abc4a-150">-SecretContentType</span></span>
<span data-ttu-id="abc4a-151">Specifica il tipo di contenuto del nuovo segreto del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="abc4a-151">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="abc4a-152">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="abc4a-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="abc4a-153">applicazione/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="abc4a-153">application/x-pkcs12</span></span>
- <span data-ttu-id="abc4a-154">applicazione/x-Pem-file</span><span class="sxs-lookup"><span data-stu-id="abc4a-154">application/x-pem-file</span></span>

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

### <span data-ttu-id="abc4a-155">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="abc4a-155">-SubjectName</span></span>
<span data-ttu-id="abc4a-156">Specifica il nome del soggetto del certificato.</span><span class="sxs-lookup"><span data-stu-id="abc4a-156">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="abc4a-157">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="abc4a-157">-ValidityInMonths</span></span>
<span data-ttu-id="abc4a-158">Specifica il numero di mesi in cui il certificato è valido.</span><span class="sxs-lookup"><span data-stu-id="abc4a-158">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="abc4a-159">-Confermare</span><span class="sxs-lookup"><span data-stu-id="abc4a-159">-Confirm</span></span>
<span data-ttu-id="abc4a-160">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="abc4a-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abc4a-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abc4a-161">-WhatIf</span></span>
<span data-ttu-id="abc4a-162">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="abc4a-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abc4a-163">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="abc4a-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abc4a-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abc4a-164">CommonParameters</span></span>
<span data-ttu-id="abc4a-165">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abc4a-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abc4a-166">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abc4a-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abc4a-167">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="abc4a-167">INPUTS</span></span>

### <span data-ttu-id="abc4a-168">System. String</span><span class="sxs-lookup"><span data-stu-id="abc4a-168">System.String</span></span>

### <span data-ttu-id="abc4a-169">System. Collections. Generic. list ' 1 [[System. String, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="abc4a-169">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="abc4a-170">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="abc4a-170">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="abc4a-171">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="abc4a-171">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="abc4a-172">System. Collections. Generic. list ' 1 [[System. Security. Cryptography. X509Certificates. X509KeyUsageFlags, System. Security. Cryptography. X509Certificates, Version = 4.2.1.0, Culture = neutral, PublicKeyToken = b03f5f7f11d50a3a]]</span><span class="sxs-lookup"><span data-stu-id="abc4a-172">System.Collections.Generic.List\`1[[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags, System.Security.Cryptography.X509Certificates, Version=4.2.1.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a]]</span></span>

## <span data-ttu-id="abc4a-173">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="abc4a-173">OUTPUTS</span></span>

### <span data-ttu-id="abc4a-174">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="abc4a-174">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="abc4a-175">Note</span><span class="sxs-lookup"><span data-stu-id="abc4a-175">NOTES</span></span>

## <span data-ttu-id="abc4a-176">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="abc4a-176">RELATED LINKS</span></span>

[<span data-ttu-id="abc4a-177">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="abc4a-177">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="abc4a-178">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="abc4a-178">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

