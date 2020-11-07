---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: e6ae1be8599869631698ddd886fa09184abfb867
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674106"
---
# <span data-ttu-id="f1e89-101">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="f1e89-101">Set-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="f1e89-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f1e89-102">SYNOPSIS</span></span>
<span data-ttu-id="f1e89-103">Crea o aggiorna i criteri per un certificato in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="f1e89-103">Creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="f1e89-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f1e89-104">SYNTAX</span></span>

### <span data-ttu-id="f1e89-105">ExpandedRenewPercentage (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f1e89-105">ExpandedRenewPercentage (Default)</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-RenewAtPercentageLifetime <Int32>]
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeySize <Int32>] [-KeyType <String>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1e89-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="f1e89-106">ByValue</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-InputObject] <PSKeyVaultCertificatePolicy> [-EmailAtNumberOfDaysBeforeExpiry <Int32>]
 [-EmailAtPercentageLifetime <Int32>] [-KeySize <Int32>] [-KeyType <String>] [-CertificateTransparency <Boolean>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1e89-107">ExpandedRenewNumber</span><span class="sxs-lookup"><span data-stu-id="f1e89-107">ExpandedRenewNumber</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> -RenewAtNumberOfDaysBeforeExpiry <Int32>
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.Security.Cryptography.X509Certificates.X509KeyUsageFlags]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeySize <Int32>] [-KeyType <String>] [-KeyNotExportable] [-CertificateTransparency <Boolean>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1e89-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1e89-108">DESCRIPTION</span></span>
<span data-ttu-id="f1e89-109">Il cmdlet **set-AzKeyVaultCertificatePolicy** crea o aggiorna i criteri per un certificato in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="f1e89-109">The **Set-AzKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="f1e89-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f1e89-110">EXAMPLES</span></span>

### <span data-ttu-id="f1e89-111">Esempio 1: impostare un criterio di certificato</span><span class="sxs-lookup"><span data-stu-id="f1e89-111">Example 1: Set a certificate policy</span></span>
```powershell
PS C:\> Set-AzKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True -PassThru

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

<span data-ttu-id="f1e89-112">Questo comando imposta i criteri per il certificato TestCert01 nel Vault della chiave ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="f1e89-112">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="f1e89-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f1e89-113">PARAMETERS</span></span>

### <span data-ttu-id="f1e89-114">-CertificateTransparency</span><span class="sxs-lookup"><span data-stu-id="f1e89-114">-CertificateTransparency</span></span>
<span data-ttu-id="f1e89-115">Indica se la trasparenza del certificato è abilitata per il certificato/emittente; Se non viene specificato, il valore predefinito è "true"</span><span class="sxs-lookup"><span data-stu-id="f1e89-115">Indicates whether certificate transparency is enabled for this certificate/issuer; if not specified, the default is 'true'</span></span>

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

### <span data-ttu-id="f1e89-116">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="f1e89-116">-CertificateType</span></span>
<span data-ttu-id="f1e89-117">Specifica il tipo di certificato per l'emittente.</span><span class="sxs-lookup"><span data-stu-id="f1e89-117">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="f1e89-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1e89-118">-DefaultProfile</span></span>
<span data-ttu-id="f1e89-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f1e89-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f1e89-120">-Disabled</span><span class="sxs-lookup"><span data-stu-id="f1e89-120">-Disabled</span></span>
<span data-ttu-id="f1e89-121">Indica che il criterio di certificato è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="f1e89-121">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="f1e89-122">-DnsName</span><span class="sxs-lookup"><span data-stu-id="f1e89-122">-DnsName</span></span>
<span data-ttu-id="f1e89-123">Specifica il nome del soggetto del certificato.</span><span class="sxs-lookup"><span data-stu-id="f1e89-123">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="f1e89-124">-EKU</span><span class="sxs-lookup"><span data-stu-id="f1e89-124">-Ekus</span></span>
<span data-ttu-id="f1e89-125">Specifica gli usi chiave avanzati (EKU) nel certificato.</span><span class="sxs-lookup"><span data-stu-id="f1e89-125">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="f1e89-126">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="f1e89-126">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="f1e89-127">Specifica il numero di giorni prima della scadenza quando deve iniziare il rinnovo automatico.</span><span class="sxs-lookup"><span data-stu-id="f1e89-127">Specifies the number of days before expiration when automatic renewal should start.</span></span>

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

### <span data-ttu-id="f1e89-128">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="f1e89-128">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="f1e89-129">Specifica la percentuale della durata dopo la quale inizia il processo automatico per la notifica.</span><span class="sxs-lookup"><span data-stu-id="f1e89-129">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="f1e89-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1e89-130">-InputObject</span></span>
<span data-ttu-id="f1e89-131">Specifica i criteri di certificato.</span><span class="sxs-lookup"><span data-stu-id="f1e89-131">Specifies the certificate policy.</span></span>

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

### <span data-ttu-id="f1e89-132">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="f1e89-132">-IssuerName</span></span>
<span data-ttu-id="f1e89-133">Specifica il nome dell'autorità di certificazione per il certificato.</span><span class="sxs-lookup"><span data-stu-id="f1e89-133">Specifies the name of the issuer for this certificate.</span></span>

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

### <span data-ttu-id="f1e89-134">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="f1e89-134">-KeyNotExportable</span></span>
<span data-ttu-id="f1e89-135">Indica che la chiave non è esportabile.</span><span class="sxs-lookup"><span data-stu-id="f1e89-135">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="f1e89-136">-KeySize</span><span class="sxs-lookup"><span data-stu-id="f1e89-136">-KeySize</span></span>
<span data-ttu-id="f1e89-137">Specifica la dimensione della chiave del certificato.</span><span class="sxs-lookup"><span data-stu-id="f1e89-137">Specifies the key size of the certificate.</span></span>
<span data-ttu-id="f1e89-138">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f1e89-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f1e89-139">2048</span><span class="sxs-lookup"><span data-stu-id="f1e89-139">2048</span></span>
- <span data-ttu-id="f1e89-140">3072</span><span class="sxs-lookup"><span data-stu-id="f1e89-140">3072</span></span>
- <span data-ttu-id="f1e89-141">4096</span><span class="sxs-lookup"><span data-stu-id="f1e89-141">4096</span></span>

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

### <span data-ttu-id="f1e89-142">-Tipo di digitare</span><span class="sxs-lookup"><span data-stu-id="f1e89-142">-KeyType</span></span>
<span data-ttu-id="f1e89-143">Specifica il tipo di chiave della chiave che consente di eseguire il backup del certificato.</span><span class="sxs-lookup"><span data-stu-id="f1e89-143">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="f1e89-144">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f1e89-144">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f1e89-145">RSA</span><span class="sxs-lookup"><span data-stu-id="f1e89-145">RSA</span></span>
- <span data-ttu-id="f1e89-146">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="f1e89-146">RSA-HSM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA, RSA-HSM

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1e89-147">-Utilizzo della sintassi</span><span class="sxs-lookup"><span data-stu-id="f1e89-147">-KeyUsage</span></span>
<span data-ttu-id="f1e89-148">Specifica gli usi chiave nel certificato.</span><span class="sxs-lookup"><span data-stu-id="f1e89-148">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="f1e89-149">-Nome</span><span class="sxs-lookup"><span data-stu-id="f1e89-149">-Name</span></span>
<span data-ttu-id="f1e89-150">Specifica il nome del certificato.</span><span class="sxs-lookup"><span data-stu-id="f1e89-150">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="f1e89-151">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1e89-151">-PassThru</span></span>
<span data-ttu-id="f1e89-152">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="f1e89-152">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f1e89-153">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="f1e89-153">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f1e89-154">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="f1e89-154">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="f1e89-155">Specifica il numero di giorni prima della scadenza in cui inizia il processo automatico per il rinnovo del certificato.</span><span class="sxs-lookup"><span data-stu-id="f1e89-155">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="f1e89-156">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="f1e89-156">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="f1e89-157">Specifica la percentuale della durata dopo la quale inizia il processo automatico per il rinnovo del certificato.</span><span class="sxs-lookup"><span data-stu-id="f1e89-157">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="f1e89-158">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="f1e89-158">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="f1e89-159">Indica che il certificato riutilizza la chiave durante il rinnovo.</span><span class="sxs-lookup"><span data-stu-id="f1e89-159">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="f1e89-160">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="f1e89-160">-SecretContentType</span></span>
<span data-ttu-id="f1e89-161">Specifica il tipo di contenuto del nuovo segreto del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="f1e89-161">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="f1e89-162">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f1e89-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f1e89-163">applicazione/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="f1e89-163">application/x-pkcs12</span></span>
- <span data-ttu-id="f1e89-164">applicazione/x-Pem-file</span><span class="sxs-lookup"><span data-stu-id="f1e89-164">application/x-pem-file</span></span>

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

### <span data-ttu-id="f1e89-165">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="f1e89-165">-SubjectName</span></span>
<span data-ttu-id="f1e89-166">Specifica il nome del soggetto del certificato.</span><span class="sxs-lookup"><span data-stu-id="f1e89-166">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="f1e89-167">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="f1e89-167">-ValidityInMonths</span></span>
<span data-ttu-id="f1e89-168">Specifica il numero di mesi in cui il certificato è valido.</span><span class="sxs-lookup"><span data-stu-id="f1e89-168">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="f1e89-169">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="f1e89-169">-VaultName</span></span>
<span data-ttu-id="f1e89-170">Specifica il nome di un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="f1e89-170">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="f1e89-171">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f1e89-171">-Confirm</span></span>
<span data-ttu-id="f1e89-172">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1e89-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1e89-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1e89-173">-WhatIf</span></span>
<span data-ttu-id="f1e89-174">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f1e89-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1e89-175">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f1e89-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1e89-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1e89-176">CommonParameters</span></span>
<span data-ttu-id="f1e89-177">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1e89-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1e89-178">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1e89-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1e89-179">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f1e89-179">INPUTS</span></span>

### <span data-ttu-id="f1e89-180">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="f1e89-180">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="f1e89-181">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f1e89-181">OUTPUTS</span></span>

### <span data-ttu-id="f1e89-182">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="f1e89-182">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="f1e89-183">Note</span><span class="sxs-lookup"><span data-stu-id="f1e89-183">NOTES</span></span>

## <span data-ttu-id="f1e89-184">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f1e89-184">RELATED LINKS</span></span>

[<span data-ttu-id="f1e89-185">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="f1e89-185">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="f1e89-186">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="f1e89-186">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

