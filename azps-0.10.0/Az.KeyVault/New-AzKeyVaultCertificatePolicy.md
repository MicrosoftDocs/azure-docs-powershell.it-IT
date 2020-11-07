---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/new-AzKeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: 83eea8c8a030c5d22368bc0ede42c71e92df14a2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861282"
---
# <span data-ttu-id="24659-101">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="24659-101">New-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="24659-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="24659-102">SYNOPSIS</span></span>
<span data-ttu-id="24659-103">Crea un oggetto Criteri di certificato in memoria.</span><span class="sxs-lookup"><span data-stu-id="24659-103">Creates an in-memory certificate policy object.</span></span>

## <span data-ttu-id="24659-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="24659-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificatePolicy [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-SubjectName <String>] [-DnsNames <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] -IssuerName <String>
 [-CertificateType <String>] [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>]
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24659-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="24659-105">DESCRIPTION</span></span>
<span data-ttu-id="24659-106">Il cmdlet **New-AzKeyVaultCertificatePolicy** crea un oggetto Criteri di certificato in memoria per Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="24659-106">The **New-AzKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="24659-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="24659-107">EXAMPLES</span></span>

### <span data-ttu-id="24659-108">Esempio 1: creare un criterio di certificato</span><span class="sxs-lookup"><span data-stu-id="24659-108">Example 1: Create a certificate policy</span></span>
```
PS C:\>New-AzKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal
```

<span data-ttu-id="24659-109">Questo comando crea un criterio di certificato valido per sei mesi e riutilizza la chiave per rinnovare il certificato.</span><span class="sxs-lookup"><span data-stu-id="24659-109">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="24659-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="24659-110">PARAMETERS</span></span>

### <span data-ttu-id="24659-111">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="24659-111">-CertificateType</span></span>
<span data-ttu-id="24659-112">Specifica il tipo di certificato per l'emittente.</span><span class="sxs-lookup"><span data-stu-id="24659-112">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24659-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24659-113">-DefaultProfile</span></span>
<span data-ttu-id="24659-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="24659-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="24659-115">-Disabled</span><span class="sxs-lookup"><span data-stu-id="24659-115">-Disabled</span></span>
<span data-ttu-id="24659-116">Indica che il criterio di certificato è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="24659-116">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24659-117">-DnsNames</span><span class="sxs-lookup"><span data-stu-id="24659-117">-DnsNames</span></span>
<span data-ttu-id="24659-118">Specifica i nomi DNS nel certificato.</span><span class="sxs-lookup"><span data-stu-id="24659-118">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="24659-119">-EKU</span><span class="sxs-lookup"><span data-stu-id="24659-119">-Ekus</span></span>
<span data-ttu-id="24659-120">Specifica gli usi chiave avanzati (EKU) nel certificato.</span><span class="sxs-lookup"><span data-stu-id="24659-120">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="24659-121">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="24659-121">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="24659-122">Specifica il numero di giorni prima della scadenza in cui viene avviato il processo di notifica automatica.</span><span class="sxs-lookup"><span data-stu-id="24659-122">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="24659-123">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="24659-123">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="24659-124">Specifica la percentuale della durata dopo la quale inizia il processo automatico per la notifica.</span><span class="sxs-lookup"><span data-stu-id="24659-124">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="24659-125">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="24659-125">-IssuerName</span></span>
<span data-ttu-id="24659-126">Specifica il nome dell'autorità di certificazione per il certificato.</span><span class="sxs-lookup"><span data-stu-id="24659-126">Specifies the name of the issuer for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24659-127">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="24659-127">-KeyNotExportable</span></span>
<span data-ttu-id="24659-128">Indica che la chiave non è esportabile.</span><span class="sxs-lookup"><span data-stu-id="24659-128">Indicates that the key is not exportable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24659-129">-Tipo di digitare</span><span class="sxs-lookup"><span data-stu-id="24659-129">-KeyType</span></span>
<span data-ttu-id="24659-130">Specifica il tipo di chiave della chiave che consente di eseguire il backup del certificato.</span><span class="sxs-lookup"><span data-stu-id="24659-130">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="24659-131">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="24659-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="24659-132">RSA</span><span class="sxs-lookup"><span data-stu-id="24659-132">RSA</span></span>
- <span data-ttu-id="24659-133">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="24659-133">RSA-HSM</span></span>

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

### <span data-ttu-id="24659-134">-Utilizzo della sintassi</span><span class="sxs-lookup"><span data-stu-id="24659-134">-KeyUsage</span></span>
<span data-ttu-id="24659-135">Specifica gli usi chiave nel certificato.</span><span class="sxs-lookup"><span data-stu-id="24659-135">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="24659-136">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="24659-136">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="24659-137">Specifica il numero di giorni prima della scadenza in cui inizia il processo automatico per il rinnovo del certificato.</span><span class="sxs-lookup"><span data-stu-id="24659-137">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="24659-138">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="24659-138">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="24659-139">Specifica la percentuale della durata dopo la quale inizia il processo automatico per il rinnovo del certificato.</span><span class="sxs-lookup"><span data-stu-id="24659-139">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="24659-140">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="24659-140">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="24659-141">Indica che il certificato riutilizza la chiave durante il rinnovo.</span><span class="sxs-lookup"><span data-stu-id="24659-141">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24659-142">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="24659-142">-SecretContentType</span></span>
<span data-ttu-id="24659-143">Specifica il tipo di contenuto del nuovo segreto del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="24659-143">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="24659-144">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="24659-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="24659-145">applicazione/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="24659-145">application/x-pkcs12</span></span>
- <span data-ttu-id="24659-146">applicazione/x-Pem-file</span><span class="sxs-lookup"><span data-stu-id="24659-146">application/x-pem-file</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24659-147">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="24659-147">-SubjectName</span></span>
<span data-ttu-id="24659-148">Specifica il nome del soggetto del certificato.</span><span class="sxs-lookup"><span data-stu-id="24659-148">Specifies the subject name of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24659-149">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="24659-149">-ValidityInMonths</span></span>
<span data-ttu-id="24659-150">Specifica il numero di mesi in cui il certificato è valido.</span><span class="sxs-lookup"><span data-stu-id="24659-150">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="24659-151">-Confermare</span><span class="sxs-lookup"><span data-stu-id="24659-151">-Confirm</span></span>
<span data-ttu-id="24659-152">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24659-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24659-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24659-153">-WhatIf</span></span>
<span data-ttu-id="24659-154">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="24659-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24659-155">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="24659-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24659-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24659-156">CommonParameters</span></span>
<span data-ttu-id="24659-157">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24659-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24659-158">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24659-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24659-159">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="24659-159">INPUTS</span></span>

### <span data-ttu-id="24659-160">Nessuno</span><span class="sxs-lookup"><span data-stu-id="24659-160">None</span></span>
<span data-ttu-id="24659-161">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="24659-161">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="24659-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="24659-162">OUTPUTS</span></span>

### <span data-ttu-id="24659-163">Microsoft. Azure. Commands. Vault. Models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="24659-163">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="24659-164">Note</span><span class="sxs-lookup"><span data-stu-id="24659-164">NOTES</span></span>

## <span data-ttu-id="24659-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="24659-165">RELATED LINKS</span></span>

[<span data-ttu-id="24659-166">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="24659-166">Get-AzKeyVaultCertificatePolicy</span></span>](./Get-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="24659-167">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="24659-167">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

