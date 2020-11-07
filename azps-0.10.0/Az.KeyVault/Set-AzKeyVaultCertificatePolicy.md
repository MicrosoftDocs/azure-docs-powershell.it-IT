---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/set-AzKeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 160c98b141dbde36786404b58c694772dc86d323
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863014"
---
# <span data-ttu-id="91609-101">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="91609-101">Set-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="91609-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="91609-102">SYNOPSIS</span></span>
<span data-ttu-id="91609-103">Crea o aggiorna i criteri per un certificato in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="91609-103">Creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="91609-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="91609-104">SYNTAX</span></span>

### <span data-ttu-id="91609-105">Espanso (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="91609-105">Expanded (Default)</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-SecretContentType <String>]
 [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsNames <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>]
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [-KeyNotExportable] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="91609-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="91609-106">ByValue</span></span>
```
Set-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [[-CertificatePolicy] <KeyVaultCertificatePolicy>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91609-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91609-107">DESCRIPTION</span></span>
<span data-ttu-id="91609-108">Il cmdlet **set-AzKeyVaultCertificatePolicy** crea o aggiorna i criteri per un certificato in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="91609-108">The **Set-AzKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="91609-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="91609-109">EXAMPLES</span></span>

### <span data-ttu-id="91609-110">Esempio 1: impostare un criterio di certificato</span><span class="sxs-lookup"><span data-stu-id="91609-110">Example 1: Set a certificate policy</span></span>
```
PS C:\>Set-AzKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True
```

<span data-ttu-id="91609-111">Questo comando imposta i criteri per il certificato TestCert01 nel Vault della chiave ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="91609-111">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="91609-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="91609-112">PARAMETERS</span></span>

### <span data-ttu-id="91609-113">-CertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="91609-113">-CertificatePolicy</span></span>
<span data-ttu-id="91609-114">Specifica i criteri di certificato.</span><span class="sxs-lookup"><span data-stu-id="91609-114">Specifies the certificate policy.</span></span>

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

### <span data-ttu-id="91609-115">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="91609-115">-CertificateType</span></span>
<span data-ttu-id="91609-116">Specifica il tipo di certificato per l'emittente.</span><span class="sxs-lookup"><span data-stu-id="91609-116">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="91609-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91609-117">-DefaultProfile</span></span>
<span data-ttu-id="91609-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="91609-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91609-119">-Disabled</span><span class="sxs-lookup"><span data-stu-id="91609-119">-Disabled</span></span>
<span data-ttu-id="91609-120">Indica che il criterio di certificato è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="91609-120">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="91609-121">-DnsNames</span><span class="sxs-lookup"><span data-stu-id="91609-121">-DnsNames</span></span>
<span data-ttu-id="91609-122">Specifica i nomi DNS nel certificato.</span><span class="sxs-lookup"><span data-stu-id="91609-122">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="91609-123">-EKU</span><span class="sxs-lookup"><span data-stu-id="91609-123">-Ekus</span></span>
<span data-ttu-id="91609-124">Specifica gli usi chiave avanzati (EKU) nel certificato.</span><span class="sxs-lookup"><span data-stu-id="91609-124">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="91609-125">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="91609-125">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="91609-126">Specifica il numero di giorni prima della scadenza in cui viene avviato il processo di notifica automatica.</span><span class="sxs-lookup"><span data-stu-id="91609-126">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="91609-127">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="91609-127">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="91609-128">Specifica la percentuale della durata dopo la quale inizia il processo automatico per la notifica.</span><span class="sxs-lookup"><span data-stu-id="91609-128">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="91609-129">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="91609-129">-IssuerName</span></span>
<span data-ttu-id="91609-130">Specifica il nome dell'autorità di certificazione per il certificato.</span><span class="sxs-lookup"><span data-stu-id="91609-130">Specifies the name of the issuer for this certificate.</span></span>

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

### <span data-ttu-id="91609-131">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="91609-131">-KeyNotExportable</span></span>
<span data-ttu-id="91609-132">Indica che la chiave non è esportabile.</span><span class="sxs-lookup"><span data-stu-id="91609-132">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="91609-133">-Tipo di digitare</span><span class="sxs-lookup"><span data-stu-id="91609-133">-KeyType</span></span>
<span data-ttu-id="91609-134">Specifica il tipo di chiave della chiave che consente di eseguire il backup del certificato.</span><span class="sxs-lookup"><span data-stu-id="91609-134">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="91609-135">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="91609-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="91609-136">RSA</span><span class="sxs-lookup"><span data-stu-id="91609-136">RSA</span></span>
- <span data-ttu-id="91609-137">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="91609-137">RSA-HSM</span></span>

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

### <span data-ttu-id="91609-138">-Utilizzo della sintassi</span><span class="sxs-lookup"><span data-stu-id="91609-138">-KeyUsage</span></span>
<span data-ttu-id="91609-139">Specifica gli usi chiave nel certificato.</span><span class="sxs-lookup"><span data-stu-id="91609-139">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="91609-140">-Nome</span><span class="sxs-lookup"><span data-stu-id="91609-140">-Name</span></span>
<span data-ttu-id="91609-141">Specifica il nome del certificato.</span><span class="sxs-lookup"><span data-stu-id="91609-141">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="91609-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="91609-142">-PassThru</span></span>
<span data-ttu-id="91609-143">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="91609-143">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="91609-144">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="91609-144">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="91609-145">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="91609-145">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="91609-146">Specifica il numero di giorni prima della scadenza in cui inizia il processo automatico per il rinnovo del certificato.</span><span class="sxs-lookup"><span data-stu-id="91609-146">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="91609-147">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="91609-147">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="91609-148">Specifica la percentuale della durata dopo la quale inizia il processo automatico per il rinnovo del certificato.</span><span class="sxs-lookup"><span data-stu-id="91609-148">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="91609-149">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="91609-149">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="91609-150">Indica che il certificato riutilizza la chiave durante il rinnovo.</span><span class="sxs-lookup"><span data-stu-id="91609-150">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="91609-151">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="91609-151">-SecretContentType</span></span>
<span data-ttu-id="91609-152">Specifica il tipo di contenuto del nuovo segreto del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="91609-152">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="91609-153">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="91609-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="91609-154">applicazione/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="91609-154">application/x-pkcs12</span></span>
- <span data-ttu-id="91609-155">applicazione/x-Pem-file</span><span class="sxs-lookup"><span data-stu-id="91609-155">application/x-pem-file</span></span>

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

### <span data-ttu-id="91609-156">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="91609-156">-SubjectName</span></span>
<span data-ttu-id="91609-157">Specifica il nome del soggetto del certificato.</span><span class="sxs-lookup"><span data-stu-id="91609-157">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="91609-158">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="91609-158">-ValidityInMonths</span></span>
<span data-ttu-id="91609-159">Specifica il numero di mesi in cui il certificato è valido.</span><span class="sxs-lookup"><span data-stu-id="91609-159">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="91609-160">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="91609-160">-VaultName</span></span>
<span data-ttu-id="91609-161">Specifica il nome di un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="91609-161">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="91609-162">-Confermare</span><span class="sxs-lookup"><span data-stu-id="91609-162">-Confirm</span></span>
<span data-ttu-id="91609-163">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91609-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91609-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91609-164">-WhatIf</span></span>
<span data-ttu-id="91609-165">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="91609-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91609-166">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="91609-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91609-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91609-167">CommonParameters</span></span>
<span data-ttu-id="91609-168">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91609-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91609-169">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91609-169">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91609-170">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="91609-170">INPUTS</span></span>

### <span data-ttu-id="91609-171">Nessuno</span><span class="sxs-lookup"><span data-stu-id="91609-171">None</span></span>
<span data-ttu-id="91609-172">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="91609-172">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="91609-173">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="91609-173">OUTPUTS</span></span>

### <span data-ttu-id="91609-174">Microsoft. Azure. Commands. Vault. Models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="91609-174">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="91609-175">Note</span><span class="sxs-lookup"><span data-stu-id="91609-175">NOTES</span></span>

## <span data-ttu-id="91609-176">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="91609-176">RELATED LINKS</span></span>

[<span data-ttu-id="91609-177">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="91609-177">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="91609-178">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="91609-178">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

