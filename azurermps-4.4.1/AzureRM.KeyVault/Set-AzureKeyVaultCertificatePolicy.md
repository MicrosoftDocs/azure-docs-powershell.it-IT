---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: 94f8b6e136925956faf4402b583d80f6a675cca3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521215"
---
# <span data-ttu-id="57528-101">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="57528-101">Set-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="57528-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="57528-102">SYNOPSIS</span></span>
<span data-ttu-id="57528-103">Crea o aggiorna i criteri per un certificato in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="57528-103">Creates or updates the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57528-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="57528-104">SYNTAX</span></span>

### <span data-ttu-id="57528-105">Espanso (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="57528-105">Expanded (Default)</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-SecretContentType <String>]
 [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsNames <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>]
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [-KeyNotExportable] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="57528-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="57528-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [[-CertificatePolicy] <KeyVaultCertificatePolicy>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57528-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="57528-107">DESCRIPTION</span></span>
<span data-ttu-id="57528-108">Il cmdlet **set-AzureKeyVaultCertificatePolicy** crea o aggiorna i criteri per un certificato in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="57528-108">The **Set-AzureKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="57528-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="57528-109">EXAMPLES</span></span>

### <span data-ttu-id="57528-110">Esempio 1: impostare un criterio di certificato</span><span class="sxs-lookup"><span data-stu-id="57528-110">Example 1: Set a certificate policy</span></span>
```
PS C:\>Set-AzureKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True
```

<span data-ttu-id="57528-111">Questo comando imposta i criteri per il certificato TestCert01 nel Vault della chiave ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="57528-111">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="57528-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="57528-112">PARAMETERS</span></span>

### <span data-ttu-id="57528-113">-CertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="57528-113">-CertificatePolicy</span></span>
<span data-ttu-id="57528-114">Specifica i criteri di certificato.</span><span class="sxs-lookup"><span data-stu-id="57528-114">Specifies the certificate policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy
Parameter Sets: ByValue
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57528-115">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="57528-115">-CertificateType</span></span>
<span data-ttu-id="57528-116">Specifica il tipo di certificato per l'emittente.</span><span class="sxs-lookup"><span data-stu-id="57528-116">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57528-117">-Disabled</span><span class="sxs-lookup"><span data-stu-id="57528-117">-Disabled</span></span>
<span data-ttu-id="57528-118">Indica che il criterio di certificato è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="57528-118">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57528-119">-DnsNames</span><span class="sxs-lookup"><span data-stu-id="57528-119">-DnsNames</span></span>
<span data-ttu-id="57528-120">Specifica i nomi DNS nel certificato.</span><span class="sxs-lookup"><span data-stu-id="57528-120">Specifies the DNS names in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57528-121">-EKU</span><span class="sxs-lookup"><span data-stu-id="57528-121">-Ekus</span></span>
<span data-ttu-id="57528-122">Specifica gli usi chiave avanzati (EKU) nel certificato.</span><span class="sxs-lookup"><span data-stu-id="57528-122">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57528-123">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="57528-123">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="57528-124">Specifica il numero di giorni prima della scadenza in cui viene avviato il processo di notifica automatica.</span><span class="sxs-lookup"><span data-stu-id="57528-124">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="57528-125">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="57528-125">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="57528-126">Specifica la percentuale della durata dopo la quale inizia il processo automatico per la notifica.</span><span class="sxs-lookup"><span data-stu-id="57528-126">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="57528-127">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="57528-127">-IssuerName</span></span>
<span data-ttu-id="57528-128">Specifica il nome dell'autorità di certificazione per il certificato.</span><span class="sxs-lookup"><span data-stu-id="57528-128">Specifies the name of the issuer for this certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57528-129">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="57528-129">-KeyNotExportable</span></span>
<span data-ttu-id="57528-130">Indica che la chiave non è esportabile.</span><span class="sxs-lookup"><span data-stu-id="57528-130">Indicates that the key is not exportable.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57528-131">-Tipo di digitare</span><span class="sxs-lookup"><span data-stu-id="57528-131">-KeyType</span></span>
<span data-ttu-id="57528-132">Specifica il tipo di chiave della chiave che consente di eseguire il backup del certificato.</span><span class="sxs-lookup"><span data-stu-id="57528-132">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="57528-133">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="57528-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="57528-134">RSA</span><span class="sxs-lookup"><span data-stu-id="57528-134">RSA</span></span>
- <span data-ttu-id="57528-135">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="57528-135">RSA-HSM</span></span>

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

### <span data-ttu-id="57528-136">-Utilizzo della sintassi</span><span class="sxs-lookup"><span data-stu-id="57528-136">-KeyUsage</span></span>
<span data-ttu-id="57528-137">Specifica gli usi chiave nel certificato.</span><span class="sxs-lookup"><span data-stu-id="57528-137">Specifies the key usages in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57528-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="57528-138">-Name</span></span>
<span data-ttu-id="57528-139">Specifica il nome del certificato.</span><span class="sxs-lookup"><span data-stu-id="57528-139">Specifies the name of the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57528-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="57528-140">-PassThru</span></span>
<span data-ttu-id="57528-141">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="57528-141">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="57528-142">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="57528-142">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="57528-143">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="57528-143">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="57528-144">Specifica il numero di giorni prima della scadenza in cui inizia il processo automatico per il rinnovo del certificato.</span><span class="sxs-lookup"><span data-stu-id="57528-144">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57528-145">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="57528-145">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="57528-146">Specifica la percentuale della durata dopo la quale inizia il processo automatico per il rinnovo del certificato.</span><span class="sxs-lookup"><span data-stu-id="57528-146">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57528-147">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="57528-147">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="57528-148">Indica che il certificato riutilizza la chiave durante il rinnovo.</span><span class="sxs-lookup"><span data-stu-id="57528-148">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57528-149">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="57528-149">-SecretContentType</span></span>
<span data-ttu-id="57528-150">Specifica il tipo di contenuto del nuovo segreto del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="57528-150">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="57528-151">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="57528-151">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="57528-152">applicazione/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="57528-152">application/x-pkcs12</span></span>
- <span data-ttu-id="57528-153">applicazione/x-Pem-file</span><span class="sxs-lookup"><span data-stu-id="57528-153">application/x-pem-file</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57528-154">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="57528-154">-SubjectName</span></span>
<span data-ttu-id="57528-155">Specifica il nome del soggetto del certificato.</span><span class="sxs-lookup"><span data-stu-id="57528-155">Specifies the subject name of the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57528-156">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="57528-156">-ValidityInMonths</span></span>
<span data-ttu-id="57528-157">Specifica il numero di mesi in cui il certificato è valido.</span><span class="sxs-lookup"><span data-stu-id="57528-157">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57528-158">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="57528-158">-VaultName</span></span>
<span data-ttu-id="57528-159">Specifica il nome di un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="57528-159">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57528-160">-Confermare</span><span class="sxs-lookup"><span data-stu-id="57528-160">-Confirm</span></span>
<span data-ttu-id="57528-161">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57528-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57528-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57528-162">-WhatIf</span></span>
<span data-ttu-id="57528-163">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="57528-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57528-164">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="57528-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57528-165">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57528-165">-DefaultProfile</span></span>
<span data-ttu-id="57528-166">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="57528-166">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57528-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57528-167">CommonParameters</span></span>
<span data-ttu-id="57528-168">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57528-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57528-169">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57528-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57528-170">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="57528-170">INPUTS</span></span>

## <span data-ttu-id="57528-171">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="57528-171">OUTPUTS</span></span>

### <span data-ttu-id="57528-172">Microsoft. Azure. Commands. Vault. Models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="57528-172">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="57528-173">Note</span><span class="sxs-lookup"><span data-stu-id="57528-173">NOTES</span></span>

## <span data-ttu-id="57528-174">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="57528-174">RELATED LINKS</span></span>

[<span data-ttu-id="57528-175">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="57528-175">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="57528-176">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="57528-176">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)

