---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurekeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: a77cd700064777c769d5499cb099cfa3f9a53ec0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685939"
---
# <span data-ttu-id="9cde4-101">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="9cde4-101">New-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="9cde4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9cde4-102">SYNOPSIS</span></span>
<span data-ttu-id="9cde4-103">Crea un oggetto Criteri di certificato in memoria.</span><span class="sxs-lookup"><span data-stu-id="9cde4-103">Creates an in-memory certificate policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9cde4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9cde4-104">SYNTAX</span></span>

### <span data-ttu-id="9cde4-105">SubjectName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9cde4-105">SubjectName (Default)</span></span>
```
New-AzureKeyVaultCertificatePolicy [-IssuerName] <String> [-SubjectName] <String>
 [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>]
 [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9cde4-106">DNSNames</span><span class="sxs-lookup"><span data-stu-id="9cde4-106">DNSNames</span></span>
```
New-AzureKeyVaultCertificatePolicy [-IssuerName] <String> [[-SubjectName] <String>]
 [-DnsName] <System.Collections.Generic.List`1[System.String]> [-RenewAtNumberOfDaysBeforeExpiry <Int32>]
 [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9cde4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9cde4-107">DESCRIPTION</span></span>
<span data-ttu-id="9cde4-108">Il cmdlet **New-AzureKeyVaultCertificatePolicy** crea un oggetto Criteri di certificato in memoria per Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="9cde4-108">The **New-AzureKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="9cde4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9cde4-109">EXAMPLES</span></span>

### <span data-ttu-id="9cde4-110">Esempio 1: creare un criterio di certificato</span><span class="sxs-lookup"><span data-stu-id="9cde4-110">Example 1: Create a certificate policy</span></span>
```powershell
PS C:\> New-AzureKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal

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

<span data-ttu-id="9cde4-111">Questo comando crea un criterio di certificato valido per sei mesi e riutilizza la chiave per rinnovare il certificato.</span><span class="sxs-lookup"><span data-stu-id="9cde4-111">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="9cde4-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9cde4-112">PARAMETERS</span></span>

### <span data-ttu-id="9cde4-113">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="9cde4-113">-CertificateType</span></span>
<span data-ttu-id="9cde4-114">Specifica il tipo di certificato per l'emittente.</span><span class="sxs-lookup"><span data-stu-id="9cde4-114">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="9cde4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cde4-115">-DefaultProfile</span></span>
<span data-ttu-id="9cde4-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9cde4-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9cde4-117">-Disabled</span><span class="sxs-lookup"><span data-stu-id="9cde4-117">-Disabled</span></span>
<span data-ttu-id="9cde4-118">Indica che il criterio di certificato è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="9cde4-118">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="9cde4-119">-DnsName</span><span class="sxs-lookup"><span data-stu-id="9cde4-119">-DnsName</span></span>
<span data-ttu-id="9cde4-120">Specifica i nomi DNS nel certificato.</span><span class="sxs-lookup"><span data-stu-id="9cde4-120">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="9cde4-121">-EKU</span><span class="sxs-lookup"><span data-stu-id="9cde4-121">-Ekus</span></span>
<span data-ttu-id="9cde4-122">Specifica gli usi chiave avanzati (EKU) nel certificato.</span><span class="sxs-lookup"><span data-stu-id="9cde4-122">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="9cde4-123">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="9cde4-123">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="9cde4-124">Specifica il numero di giorni prima della scadenza in cui viene avviato il processo di notifica automatica.</span><span class="sxs-lookup"><span data-stu-id="9cde4-124">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="9cde4-125">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="9cde4-125">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="9cde4-126">Specifica la percentuale della durata dopo la quale inizia il processo automatico per la notifica.</span><span class="sxs-lookup"><span data-stu-id="9cde4-126">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="9cde4-127">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="9cde4-127">-IssuerName</span></span>
<span data-ttu-id="9cde4-128">Specifica il nome dell'autorità di certificazione per il certificato.</span><span class="sxs-lookup"><span data-stu-id="9cde4-128">Specifies the name of the issuer for the certificate.</span></span>

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

### <span data-ttu-id="9cde4-129">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="9cde4-129">-KeyNotExportable</span></span>
<span data-ttu-id="9cde4-130">Indica che la chiave non è esportabile.</span><span class="sxs-lookup"><span data-stu-id="9cde4-130">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="9cde4-131">-Tipo di digitare</span><span class="sxs-lookup"><span data-stu-id="9cde4-131">-KeyType</span></span>
<span data-ttu-id="9cde4-132">Specifica il tipo di chiave della chiave che consente di eseguire il backup del certificato.</span><span class="sxs-lookup"><span data-stu-id="9cde4-132">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="9cde4-133">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="9cde4-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9cde4-134">RSA</span><span class="sxs-lookup"><span data-stu-id="9cde4-134">RSA</span></span>
- <span data-ttu-id="9cde4-135">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="9cde4-135">RSA-HSM</span></span>

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

### <span data-ttu-id="9cde4-136">-Utilizzo della sintassi</span><span class="sxs-lookup"><span data-stu-id="9cde4-136">-KeyUsage</span></span>
<span data-ttu-id="9cde4-137">Specifica gli usi chiave nel certificato.</span><span class="sxs-lookup"><span data-stu-id="9cde4-137">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="9cde4-138">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="9cde4-138">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="9cde4-139">Specifica il numero di giorni prima della scadenza in cui inizia il processo automatico per il rinnovo del certificato.</span><span class="sxs-lookup"><span data-stu-id="9cde4-139">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="9cde4-140">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="9cde4-140">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="9cde4-141">Specifica la percentuale della durata dopo la quale inizia il processo automatico per il rinnovo del certificato.</span><span class="sxs-lookup"><span data-stu-id="9cde4-141">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="9cde4-142">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="9cde4-142">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="9cde4-143">Indica che il certificato riutilizza la chiave durante il rinnovo.</span><span class="sxs-lookup"><span data-stu-id="9cde4-143">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="9cde4-144">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="9cde4-144">-SecretContentType</span></span>
<span data-ttu-id="9cde4-145">Specifica il tipo di contenuto del nuovo segreto del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="9cde4-145">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="9cde4-146">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="9cde4-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9cde4-147">applicazione/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="9cde4-147">application/x-pkcs12</span></span>
- <span data-ttu-id="9cde4-148">applicazione/x-Pem-file</span><span class="sxs-lookup"><span data-stu-id="9cde4-148">application/x-pem-file</span></span>

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

### <span data-ttu-id="9cde4-149">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="9cde4-149">-SubjectName</span></span>
<span data-ttu-id="9cde4-150">Specifica il nome del soggetto del certificato.</span><span class="sxs-lookup"><span data-stu-id="9cde4-150">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="9cde4-151">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="9cde4-151">-ValidityInMonths</span></span>
<span data-ttu-id="9cde4-152">Specifica il numero di mesi in cui il certificato è valido.</span><span class="sxs-lookup"><span data-stu-id="9cde4-152">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="9cde4-153">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9cde4-153">-Confirm</span></span>
<span data-ttu-id="9cde4-154">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9cde4-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cde4-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cde4-155">-WhatIf</span></span>
<span data-ttu-id="9cde4-156">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9cde4-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cde4-157">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9cde4-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cde4-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cde4-158">CommonParameters</span></span>
<span data-ttu-id="9cde4-159">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cde4-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cde4-160">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cde4-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cde4-161">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9cde4-161">INPUTS</span></span>

### <span data-ttu-id="9cde4-162">System. String</span><span class="sxs-lookup"><span data-stu-id="9cde4-162">System.String</span></span>

### <span data-ttu-id="9cde4-163">System. Collections. Generic. list ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="9cde4-163">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="9cde4-164">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="9cde4-164">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="9cde4-165">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9cde4-165">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="9cde4-166">System. Collections. Generic. list ' 1 [[System. Security. Cryptography. X509Certificates. X509KeyUsageFlags, System, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="9cde4-166">System.Collections.Generic.List\`1[[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags, System, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="9cde4-167">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9cde4-167">OUTPUTS</span></span>

### <span data-ttu-id="9cde4-168">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="9cde4-168">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="9cde4-169">Note</span><span class="sxs-lookup"><span data-stu-id="9cde4-169">NOTES</span></span>

## <span data-ttu-id="9cde4-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9cde4-170">RELATED LINKS</span></span>

[<span data-ttu-id="9cde4-171">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="9cde4-171">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="9cde4-172">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="9cde4-172">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)
