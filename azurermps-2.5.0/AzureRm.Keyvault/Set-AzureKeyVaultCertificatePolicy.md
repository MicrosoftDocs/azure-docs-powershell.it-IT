---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificatepolicy
schema: 2.0.0
ms.openlocfilehash: 7a9356952f2ea8b4113f5df0fe364e9647e2c733
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866509"
---
# <span data-ttu-id="bf13b-101">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="bf13b-101">Set-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="bf13b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bf13b-102">SYNOPSIS</span></span>
<span data-ttu-id="bf13b-103">Crea o aggiorna i criteri per un certificato in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="bf13b-103">Creates or updates the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf13b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bf13b-104">SYNTAX</span></span>

### <span data-ttu-id="bf13b-105">Espanso (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bf13b-105">Expanded (Default)</span></span>
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

### <span data-ttu-id="bf13b-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="bf13b-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [[-CertificatePolicy] <KeyVaultCertificatePolicy>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf13b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bf13b-107">DESCRIPTION</span></span>
<span data-ttu-id="bf13b-108">Il cmdlet **set-AzureKeyVaultCertificatePolicy** crea o aggiorna i criteri per un certificato in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="bf13b-108">The **Set-AzureKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="bf13b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bf13b-109">EXAMPLES</span></span>

### <span data-ttu-id="bf13b-110">Esempio 1: impostare un criterio di certificato</span><span class="sxs-lookup"><span data-stu-id="bf13b-110">Example 1: Set a certificate policy</span></span>
```
PS C:\>Set-AzureKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True
```

<span data-ttu-id="bf13b-111">Questo comando imposta i criteri per il certificato TestCert01 nel Vault della chiave ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="bf13b-111">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="bf13b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bf13b-112">PARAMETERS</span></span>

### <span data-ttu-id="bf13b-113">-CertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="bf13b-113">-CertificatePolicy</span></span>
<span data-ttu-id="bf13b-114">Specifica i criteri di certificato.</span><span class="sxs-lookup"><span data-stu-id="bf13b-114">Specifies the certificate policy.</span></span>

```yaml
Type: KeyVaultCertificatePolicy
Parameter Sets: ByValue
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf13b-115">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="bf13b-115">-CertificateType</span></span>
<span data-ttu-id="bf13b-116">Specifica il tipo di certificato per l'emittente.</span><span class="sxs-lookup"><span data-stu-id="bf13b-116">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf13b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf13b-117">-DefaultProfile</span></span>
<span data-ttu-id="bf13b-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="bf13b-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf13b-119">-Disabled</span><span class="sxs-lookup"><span data-stu-id="bf13b-119">-Disabled</span></span>
<span data-ttu-id="bf13b-120">Indica che il criterio di certificato è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="bf13b-120">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf13b-121">-DnsNames</span><span class="sxs-lookup"><span data-stu-id="bf13b-121">-DnsNames</span></span>
<span data-ttu-id="bf13b-122">Specifica i nomi DNS nel certificato.</span><span class="sxs-lookup"><span data-stu-id="bf13b-122">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="bf13b-123">-EKU</span><span class="sxs-lookup"><span data-stu-id="bf13b-123">-Ekus</span></span>
<span data-ttu-id="bf13b-124">Specifica gli usi chiave avanzati (EKU) nel certificato.</span><span class="sxs-lookup"><span data-stu-id="bf13b-124">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="bf13b-125">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="bf13b-125">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="bf13b-126">Specifica il numero di giorni prima della scadenza in cui viene avviato il processo di notifica automatica.</span><span class="sxs-lookup"><span data-stu-id="bf13b-126">Specifies how many days before expiry the automatic notification process begins.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf13b-127">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="bf13b-127">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="bf13b-128">Specifica la percentuale della durata dopo la quale inizia il processo automatico per la notifica.</span><span class="sxs-lookup"><span data-stu-id="bf13b-128">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf13b-129">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="bf13b-129">-IssuerName</span></span>
<span data-ttu-id="bf13b-130">Specifica il nome dell'autorità di certificazione per il certificato.</span><span class="sxs-lookup"><span data-stu-id="bf13b-130">Specifies the name of the issuer for this certificate.</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf13b-131">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="bf13b-131">-KeyNotExportable</span></span>
<span data-ttu-id="bf13b-132">Indica che la chiave non è esportabile.</span><span class="sxs-lookup"><span data-stu-id="bf13b-132">Indicates that the key is not exportable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf13b-133">-Tipo di digitare</span><span class="sxs-lookup"><span data-stu-id="bf13b-133">-KeyType</span></span>
<span data-ttu-id="bf13b-134">Specifica il tipo di chiave della chiave che consente di eseguire il backup del certificato.</span><span class="sxs-lookup"><span data-stu-id="bf13b-134">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="bf13b-135">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="bf13b-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bf13b-136">RSA</span><span class="sxs-lookup"><span data-stu-id="bf13b-136">RSA</span></span>
- <span data-ttu-id="bf13b-137">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="bf13b-137">RSA-HSM</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: RSA, RSA-HSM

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf13b-138">-Utilizzo della sintassi</span><span class="sxs-lookup"><span data-stu-id="bf13b-138">-KeyUsage</span></span>
<span data-ttu-id="bf13b-139">Specifica gli usi chiave nel certificato.</span><span class="sxs-lookup"><span data-stu-id="bf13b-139">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="bf13b-140">-Nome</span><span class="sxs-lookup"><span data-stu-id="bf13b-140">-Name</span></span>
<span data-ttu-id="bf13b-141">Specifica il nome del certificato.</span><span class="sxs-lookup"><span data-stu-id="bf13b-141">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="bf13b-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bf13b-142">-PassThru</span></span>
<span data-ttu-id="bf13b-143">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="bf13b-143">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="bf13b-144">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="bf13b-144">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf13b-145">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="bf13b-145">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="bf13b-146">Specifica il numero di giorni prima della scadenza in cui inizia il processo automatico per il rinnovo del certificato.</span><span class="sxs-lookup"><span data-stu-id="bf13b-146">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: Int32
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf13b-147">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="bf13b-147">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="bf13b-148">Specifica la percentuale della durata dopo la quale inizia il processo automatico per il rinnovo del certificato.</span><span class="sxs-lookup"><span data-stu-id="bf13b-148">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: Int32
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf13b-149">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="bf13b-149">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="bf13b-150">Indica che il certificato riutilizza la chiave durante il rinnovo.</span><span class="sxs-lookup"><span data-stu-id="bf13b-150">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: Boolean
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf13b-151">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="bf13b-151">-SecretContentType</span></span>
<span data-ttu-id="bf13b-152">Specifica il tipo di contenuto del nuovo segreto del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="bf13b-152">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="bf13b-153">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="bf13b-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bf13b-154">applicazione/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="bf13b-154">application/x-pkcs12</span></span>
- <span data-ttu-id="bf13b-155">applicazione/x-Pem-file</span><span class="sxs-lookup"><span data-stu-id="bf13b-155">application/x-pem-file</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases: 
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf13b-156">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="bf13b-156">-SubjectName</span></span>
<span data-ttu-id="bf13b-157">Specifica il nome del soggetto del certificato.</span><span class="sxs-lookup"><span data-stu-id="bf13b-157">Specifies the subject name of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf13b-158">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="bf13b-158">-ValidityInMonths</span></span>
<span data-ttu-id="bf13b-159">Specifica il numero di mesi in cui il certificato è valido.</span><span class="sxs-lookup"><span data-stu-id="bf13b-159">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: Int32
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf13b-160">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="bf13b-160">-VaultName</span></span>
<span data-ttu-id="bf13b-161">Specifica il nome di un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="bf13b-161">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="bf13b-162">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bf13b-162">-Confirm</span></span>
<span data-ttu-id="bf13b-163">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf13b-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf13b-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf13b-164">-WhatIf</span></span>
<span data-ttu-id="bf13b-165">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bf13b-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf13b-166">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bf13b-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf13b-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf13b-167">CommonParameters</span></span>
<span data-ttu-id="bf13b-168">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf13b-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf13b-169">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf13b-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf13b-170">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bf13b-170">INPUTS</span></span>

## <span data-ttu-id="bf13b-171">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bf13b-171">OUTPUTS</span></span>

### <span data-ttu-id="bf13b-172">Microsoft. Azure. Commands. Vault. Models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="bf13b-172">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="bf13b-173">Note</span><span class="sxs-lookup"><span data-stu-id="bf13b-173">NOTES</span></span>

## <span data-ttu-id="bf13b-174">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bf13b-174">RELATED LINKS</span></span>

[<span data-ttu-id="bf13b-175">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="bf13b-175">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="bf13b-176">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="bf13b-176">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)

