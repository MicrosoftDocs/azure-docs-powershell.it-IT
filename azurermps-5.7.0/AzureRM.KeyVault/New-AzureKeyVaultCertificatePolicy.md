---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 25E0F0E9-BF8C-49DF-87BA-31E2103A29A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurekeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: caa0961c1b7aebd5fd2f9883831d733a0fa69f1b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520446"
---
# <span data-ttu-id="5b21c-101">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="5b21c-101">New-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="5b21c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5b21c-102">SYNOPSIS</span></span>
<span data-ttu-id="5b21c-103">Crea un oggetto Criteri di certificato in memoria.</span><span class="sxs-lookup"><span data-stu-id="5b21c-103">Creates an in-memory certificate policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b21c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5b21c-104">SYNTAX</span></span>

### <span data-ttu-id="5b21c-105">SubjectName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5b21c-105">SubjectName (Default)</span></span>
```
New-AzureKeyVaultCertificatePolicy [-IssuerName] <String> [-SubjectName] <String>
 [-RenewAtNumberOfDaysBeforeExpiry <Int32>] [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>]
 [-ReuseKeyOnRenewal] [-Disabled] [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5b21c-106">DNSNames</span><span class="sxs-lookup"><span data-stu-id="5b21c-106">DNSNames</span></span>
```
New-AzureKeyVaultCertificatePolicy [-IssuerName] <String> [[-SubjectName] <String>]
 [-DnsName] <System.Collections.Generic.List`1[System.String]> [-RenewAtNumberOfDaysBeforeExpiry <Int32>]
 [-RenewAtPercentageLifetime <Int32>] [-SecretContentType <String>] [-ReuseKeyOnRenewal] [-Disabled]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5b21c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5b21c-107">DESCRIPTION</span></span>
<span data-ttu-id="5b21c-108">Il cmdlet **New-AzureKeyVaultCertificatePolicy** crea un oggetto Criteri di certificato in memoria per Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="5b21c-108">The **New-AzureKeyVaultCertificatePolicy** cmdlet creates an in-memory certificate policy object for Azure Key Vault.</span></span>

## <span data-ttu-id="5b21c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5b21c-109">EXAMPLES</span></span>

### <span data-ttu-id="5b21c-110">Esempio 1: creare un criterio di certificato</span><span class="sxs-lookup"><span data-stu-id="5b21c-110">Example 1: Create a certificate policy</span></span>
```
PS C:\>New-AzureKeyVaultCertificatePolicy -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal
```

<span data-ttu-id="5b21c-111">Questo comando crea un criterio di certificato valido per sei mesi e riutilizza la chiave per rinnovare il certificato.</span><span class="sxs-lookup"><span data-stu-id="5b21c-111">This command creates a certificate policy that is valid for six months and reuses the key to renew the certificate.</span></span>

## <span data-ttu-id="5b21c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5b21c-112">PARAMETERS</span></span>

### <span data-ttu-id="5b21c-113">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="5b21c-113">-CertificateType</span></span>
<span data-ttu-id="5b21c-114">Specifica il tipo di certificato per l'emittente.</span><span class="sxs-lookup"><span data-stu-id="5b21c-114">Specifies the type of certificate to the issuer.</span></span>

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

### <span data-ttu-id="5b21c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b21c-115">-DefaultProfile</span></span>
<span data-ttu-id="5b21c-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5b21c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5b21c-117">-Disabled</span><span class="sxs-lookup"><span data-stu-id="5b21c-117">-Disabled</span></span>
<span data-ttu-id="5b21c-118">Indica che il criterio di certificato è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="5b21c-118">Indicates that the certificate policy is disabled.</span></span>

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

### <span data-ttu-id="5b21c-119">-DnsName</span><span class="sxs-lookup"><span data-stu-id="5b21c-119">-DnsName</span></span>
<span data-ttu-id="5b21c-120">Specifica i nomi DNS nel certificato.</span><span class="sxs-lookup"><span data-stu-id="5b21c-120">Specifies the DNS names in the certificate.</span></span>

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

### <span data-ttu-id="5b21c-121">-EKU</span><span class="sxs-lookup"><span data-stu-id="5b21c-121">-Ekus</span></span>
<span data-ttu-id="5b21c-122">Specifica gli usi chiave avanzati (EKU) nel certificato.</span><span class="sxs-lookup"><span data-stu-id="5b21c-122">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

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

### <span data-ttu-id="5b21c-123">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="5b21c-123">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="5b21c-124">Specifica il numero di giorni prima della scadenza in cui viene avviato il processo di notifica automatica.</span><span class="sxs-lookup"><span data-stu-id="5b21c-124">Specifies how many days before expiry the automatic notification process begins.</span></span>

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

### <span data-ttu-id="5b21c-125">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="5b21c-125">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="5b21c-126">Specifica la percentuale della durata dopo la quale inizia il processo automatico per la notifica.</span><span class="sxs-lookup"><span data-stu-id="5b21c-126">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="5b21c-127">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="5b21c-127">-IssuerName</span></span>
<span data-ttu-id="5b21c-128">Specifica il nome dell'autorità di certificazione per il certificato.</span><span class="sxs-lookup"><span data-stu-id="5b21c-128">Specifies the name of the issuer for the certificate.</span></span>

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

### <span data-ttu-id="5b21c-129">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="5b21c-129">-KeyNotExportable</span></span>
<span data-ttu-id="5b21c-130">Indica che la chiave non è esportabile.</span><span class="sxs-lookup"><span data-stu-id="5b21c-130">Indicates that the key is not exportable.</span></span>

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

### <span data-ttu-id="5b21c-131">-Tipo di digitare</span><span class="sxs-lookup"><span data-stu-id="5b21c-131">-KeyType</span></span>
<span data-ttu-id="5b21c-132">Specifica il tipo di chiave della chiave che consente di eseguire il backup del certificato.</span><span class="sxs-lookup"><span data-stu-id="5b21c-132">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="5b21c-133">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="5b21c-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5b21c-134">RSA</span><span class="sxs-lookup"><span data-stu-id="5b21c-134">RSA</span></span>
- <span data-ttu-id="5b21c-135">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="5b21c-135">RSA-HSM</span></span>

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

### <span data-ttu-id="5b21c-136">-Utilizzo della sintassi</span><span class="sxs-lookup"><span data-stu-id="5b21c-136">-KeyUsage</span></span>
<span data-ttu-id="5b21c-137">Specifica gli usi chiave nel certificato.</span><span class="sxs-lookup"><span data-stu-id="5b21c-137">Specifies the key usages in the certificate.</span></span>

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

### <span data-ttu-id="5b21c-138">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="5b21c-138">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="5b21c-139">Specifica il numero di giorni prima della scadenza in cui inizia il processo automatico per il rinnovo del certificato.</span><span class="sxs-lookup"><span data-stu-id="5b21c-139">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="5b21c-140">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="5b21c-140">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="5b21c-141">Specifica la percentuale della durata dopo la quale inizia il processo automatico per il rinnovo del certificato.</span><span class="sxs-lookup"><span data-stu-id="5b21c-141">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

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

### <span data-ttu-id="5b21c-142">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="5b21c-142">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="5b21c-143">Indica che il certificato riutilizza la chiave durante il rinnovo.</span><span class="sxs-lookup"><span data-stu-id="5b21c-143">Indicates that the certificate reuse the key during renewal.</span></span>

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

### <span data-ttu-id="5b21c-144">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="5b21c-144">-SecretContentType</span></span>
<span data-ttu-id="5b21c-145">Specifica il tipo di contenuto del nuovo segreto del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="5b21c-145">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="5b21c-146">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="5b21c-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5b21c-147">applicazione/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="5b21c-147">application/x-pkcs12</span></span>
- <span data-ttu-id="5b21c-148">applicazione/x-Pem-file</span><span class="sxs-lookup"><span data-stu-id="5b21c-148">application/x-pem-file</span></span>

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

### <span data-ttu-id="5b21c-149">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="5b21c-149">-SubjectName</span></span>
<span data-ttu-id="5b21c-150">Specifica il nome del soggetto del certificato.</span><span class="sxs-lookup"><span data-stu-id="5b21c-150">Specifies the subject name of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: SubjectName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: DNSNames
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b21c-151">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="5b21c-151">-ValidityInMonths</span></span>
<span data-ttu-id="5b21c-152">Specifica il numero di mesi in cui il certificato è valido.</span><span class="sxs-lookup"><span data-stu-id="5b21c-152">Specifies the number of months the certificate is valid.</span></span>

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

### <span data-ttu-id="5b21c-153">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5b21c-153">-Confirm</span></span>
<span data-ttu-id="5b21c-154">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b21c-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b21c-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b21c-155">-WhatIf</span></span>
<span data-ttu-id="5b21c-156">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5b21c-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b21c-157">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5b21c-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b21c-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b21c-158">CommonParameters</span></span>
<span data-ttu-id="5b21c-159">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b21c-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b21c-160">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b21c-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b21c-161">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5b21c-161">INPUTS</span></span>

### <span data-ttu-id="5b21c-162">Nessuno</span><span class="sxs-lookup"><span data-stu-id="5b21c-162">None</span></span>
<span data-ttu-id="5b21c-163">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="5b21c-163">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5b21c-164">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5b21c-164">OUTPUTS</span></span>

### <span data-ttu-id="5b21c-165">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="5b21c-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="5b21c-166">Note</span><span class="sxs-lookup"><span data-stu-id="5b21c-166">NOTES</span></span>

## <span data-ttu-id="5b21c-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5b21c-167">RELATED LINKS</span></span>

[<span data-ttu-id="5b21c-168">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="5b21c-168">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="5b21c-169">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="5b21c-169">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)

