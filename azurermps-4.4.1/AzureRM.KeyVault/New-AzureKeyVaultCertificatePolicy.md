---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: 381ce302a8404c0bb643db0fc82e392fe53d956a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510567"
---
# <span data-ttu-id="61a6a-101">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="61a6a-101">New-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="61a6a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="61a6a-102">SYNOPSIS</span></span>
<span data-ttu-id="61a6a-103">Crea un oggetto Criteri di certificato in memoria.</span><span class="sxs-lookup"><span data-stu-id="61a6a-103">Creates an in-memory certificate policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61a6a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="61a6a-104">SYNTAX</span></span>

```
New-AzureKeyVaultCertificatePolicy [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-SubjectName <String>] [-DnsNames <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] -IssuerName <String>
 [-CertificateType <String>] [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>]
 [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>]
 [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61a6a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61a6a-105">DESCRIPTION</span></span>
<span data-ttu-id="61a6a-106">Il cmdlet **New-AzureKeyVaultCertificatePolicy** crea un oggetto Criteri di certificato in memoria per Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="61a6a-106">The **New-AzureKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="61a6a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="61a6a-107">EXAMPLES</span></span>

### <span data-ttu-id="61a6a-108">Esempio 1: creare un criterio di certificato</span><span class="sxs-lookup"><span data-stu-id="61a6a-108">Example 1: Create a certificate policy</span></span>
```
PS C:\>New-AzureKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal
```

<span data-ttu-id="61a6a-109">Questo comando crea un criterio di certificato valido per sei mesi e riutilizza la chiave per rinnovare il certificato.</span><span class="sxs-lookup"><span data-stu-id="61a6a-109">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="61a6a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="61a6a-110">PARAMETERS</span></span>

### <span data-ttu-id="61a6a-111">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="61a6a-111">-CertificateType</span></span>
<span data-ttu-id="61a6a-112">Specifica il tipo di certificato per l'emittente.</span><span class="sxs-lookup"><span data-stu-id="61a6a-112">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="61a6a-113">-Disabled</span><span class="sxs-lookup"><span data-stu-id="61a6a-113">-Disabled</span></span>
<span data-ttu-id="61a6a-114">Indica che il criterio di certificato è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="61a6a-114">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="61a6a-115">-DnsNames</span><span class="sxs-lookup"><span data-stu-id="61a6a-115">-DnsNames</span></span>
<span data-ttu-id="61a6a-116">Specifica i nomi DNS nel certificato.</span><span class="sxs-lookup"><span data-stu-id="61a6a-116">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="61a6a-117">-EKU</span><span class="sxs-lookup"><span data-stu-id="61a6a-117">-Ekus</span></span>
<span data-ttu-id="61a6a-118">Specifica gli usi chiave avanzati (EKU) nel certificato.</span><span class="sxs-lookup"><span data-stu-id="61a6a-118">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="61a6a-119">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="61a6a-119">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="61a6a-120">Specifica il numero di giorni prima della scadenza in cui viene avviato il processo di notifica automatica.</span><span class="sxs-lookup"><span data-stu-id="61a6a-120">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="61a6a-121">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="61a6a-121">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="61a6a-122">Specifica la percentuale della durata dopo la quale inizia il processo automatico per la notifica.</span><span class="sxs-lookup"><span data-stu-id="61a6a-122">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="61a6a-123">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="61a6a-123">-IssuerName</span></span>
<span data-ttu-id="61a6a-124">Specifica il nome dell'autorità di certificazione per il certificato.</span><span class="sxs-lookup"><span data-stu-id="61a6a-124">Specifies the name of the issuer for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61a6a-125">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="61a6a-125">-KeyNotExportable</span></span>
<span data-ttu-id="61a6a-126">Indica che la chiave non è esportabile.</span><span class="sxs-lookup"><span data-stu-id="61a6a-126">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="61a6a-127">-Tipo di digitare</span><span class="sxs-lookup"><span data-stu-id="61a6a-127">-KeyType</span></span>
<span data-ttu-id="61a6a-128">Specifica il tipo di chiave della chiave che consente di eseguire il backup del certificato.</span><span class="sxs-lookup"><span data-stu-id="61a6a-128">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="61a6a-129">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="61a6a-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="61a6a-130">RSA</span><span class="sxs-lookup"><span data-stu-id="61a6a-130">RSA</span></span>
- <span data-ttu-id="61a6a-131">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="61a6a-131">RSA-HSM</span></span>

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

### <span data-ttu-id="61a6a-132">-Utilizzo della sintassi</span><span class="sxs-lookup"><span data-stu-id="61a6a-132">-KeyUsage</span></span>
<span data-ttu-id="61a6a-133">Specifica gli usi chiave nel certificato.</span><span class="sxs-lookup"><span data-stu-id="61a6a-133">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="61a6a-134">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="61a6a-134">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="61a6a-135">Specifica il numero di giorni prima della scadenza in cui inizia il processo automatico per il rinnovo del certificato.</span><span class="sxs-lookup"><span data-stu-id="61a6a-135">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="61a6a-136">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="61a6a-136">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="61a6a-137">Specifica la percentuale della durata dopo la quale inizia il processo automatico per il rinnovo del certificato.</span><span class="sxs-lookup"><span data-stu-id="61a6a-137">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="61a6a-138">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="61a6a-138">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="61a6a-139">Indica che il certificato riutilizza la chiave durante il rinnovo.</span><span class="sxs-lookup"><span data-stu-id="61a6a-139">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="61a6a-140">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="61a6a-140">-SecretContentType</span></span>
<span data-ttu-id="61a6a-141">Specifica il tipo di contenuto del nuovo segreto del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="61a6a-141">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="61a6a-142">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="61a6a-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="61a6a-143">applicazione/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="61a6a-143">application/x-pkcs12</span></span>
- <span data-ttu-id="61a6a-144">applicazione/x-Pem-file</span><span class="sxs-lookup"><span data-stu-id="61a6a-144">application/x-pem-file</span></span>

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

### <span data-ttu-id="61a6a-145">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="61a6a-145">-SubjectName</span></span>
<span data-ttu-id="61a6a-146">Specifica il nome del soggetto del certificato.</span><span class="sxs-lookup"><span data-stu-id="61a6a-146">Specifies the subject name of the certificate.</span></span>

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

### <span data-ttu-id="61a6a-147">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="61a6a-147">-ValidityInMonths</span></span>
<span data-ttu-id="61a6a-148">Specifica il numero di mesi in cui il certificato è valido.</span><span class="sxs-lookup"><span data-stu-id="61a6a-148">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="61a6a-149">-Confermare</span><span class="sxs-lookup"><span data-stu-id="61a6a-149">-Confirm</span></span>
<span data-ttu-id="61a6a-150">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61a6a-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61a6a-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61a6a-151">-WhatIf</span></span>
<span data-ttu-id="61a6a-152">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="61a6a-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61a6a-153">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="61a6a-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61a6a-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61a6a-154">-DefaultProfile</span></span>
<span data-ttu-id="61a6a-155">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="61a6a-155">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61a6a-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61a6a-156">CommonParameters</span></span>
<span data-ttu-id="61a6a-157">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61a6a-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61a6a-158">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61a6a-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61a6a-159">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="61a6a-159">INPUTS</span></span>

## <span data-ttu-id="61a6a-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="61a6a-160">OUTPUTS</span></span>

### <span data-ttu-id="61a6a-161">Microsoft. Azure. Commands. Vault. Models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="61a6a-161">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="61a6a-162">Note</span><span class="sxs-lookup"><span data-stu-id="61a6a-162">NOTES</span></span>

## <span data-ttu-id="61a6a-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="61a6a-163">RELATED LINKS</span></span>

[<span data-ttu-id="61a6a-164">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="61a6a-164">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="61a6a-165">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="61a6a-165">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)

