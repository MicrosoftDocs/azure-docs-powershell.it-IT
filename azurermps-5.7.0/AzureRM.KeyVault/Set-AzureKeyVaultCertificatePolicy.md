---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 28BC1B99-946C-4A8D-9581-4D5CC0BCEF8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: e960aa211b53c79087e67e2bd86504e597a718d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521435"
---
# <span data-ttu-id="0827d-101">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="0827d-101">Set-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="0827d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0827d-102">SYNOPSIS</span></span>
<span data-ttu-id="0827d-103">Crea o aggiorna i criteri per un certificato in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="0827d-103">Creates or updates the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0827d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0827d-104">SYNTAX</span></span>

### <span data-ttu-id="0827d-105">ExpandedRenewPercentage (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0827d-105">ExpandedRenewPercentage (Default)</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String> [-RenewAtPercentageLifetime <Int32>]
 [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>] [-Disabled] [-SubjectName <String>]
 [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0827d-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="0827d-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-InputObject] <PSKeyVaultCertificatePolicy> [-EmailAtNumberOfDaysBeforeExpiry <Int32>]
 [-EmailAtPercentageLifetime <Int32>] [-KeyType <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0827d-107">ExpandedRenewNumber</span><span class="sxs-lookup"><span data-stu-id="0827d-107">ExpandedRenewNumber</span></span>
```
Set-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 -RenewAtNumberOfDaysBeforeExpiry <Int32> [-SecretContentType <String>] [-ReuseKeyOnRenewal <Boolean>]
 [-Disabled] [-SubjectName <String>] [-DnsName <System.Collections.Generic.List`1[System.String]>]
 [-KeyUsage <System.Collections.Generic.List`1[System.String]>]
 [-Ekus <System.Collections.Generic.List`1[System.String]>] [-ValidityInMonths <Int32>] [-IssuerName <String>]
 [-CertificateType <String>] [-EmailAtNumberOfDaysBeforeExpiry <Int32>] [-EmailAtPercentageLifetime <Int32>]
 [-KeyType <String>] [-KeyNotExportable] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0827d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0827d-108">DESCRIPTION</span></span>
<span data-ttu-id="0827d-109">Il cmdlet **set-AzureKeyVaultCertificatePolicy** crea o aggiorna i criteri per un certificato in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="0827d-109">The **Set-AzureKeyVaultCertificatePolicy** cmdlet creates or updates the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="0827d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0827d-110">EXAMPLES</span></span>

### <span data-ttu-id="0827d-111">Esempio 1: impostare un criterio di certificato</span><span class="sxs-lookup"><span data-stu-id="0827d-111">Example 1: Set a certificate policy</span></span>
```
PS C:\>Set-AzureKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01" -SecretContentType "application/x-pkcs12" -SubjectName "CN=contoso.com" -IssuerName "Self" -ValidityInMonths 6 -ReuseKeyOnRenewal $True
```

<span data-ttu-id="0827d-112">Questo comando imposta i criteri per il certificato TestCert01 nel Vault della chiave ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="0827d-112">This command sets the policy for the TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="0827d-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0827d-113">PARAMETERS</span></span>

### <span data-ttu-id="0827d-114">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="0827d-114">-CertificateType</span></span>
<span data-ttu-id="0827d-115">Specifica il tipo di certificato per l'emittente.</span><span class="sxs-lookup"><span data-stu-id="0827d-115">Specifies the type of certificate to the issuer.</span></span>

```yaml
Type: String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0827d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0827d-116">-DefaultProfile</span></span>
<span data-ttu-id="0827d-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0827d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0827d-118">-Disabled</span><span class="sxs-lookup"><span data-stu-id="0827d-118">-Disabled</span></span>
<span data-ttu-id="0827d-119">Indica che il criterio di certificato è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="0827d-119">Indicates that the certificate policy is disabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0827d-120">-DnsName</span><span class="sxs-lookup"><span data-stu-id="0827d-120">-DnsName</span></span>
<span data-ttu-id="0827d-121">Specifica il nome del soggetto del certificato.</span><span class="sxs-lookup"><span data-stu-id="0827d-121">Specifies the subject name of the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases: DnsNames

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0827d-122">-EKU</span><span class="sxs-lookup"><span data-stu-id="0827d-122">-Ekus</span></span>
<span data-ttu-id="0827d-123">Specifica gli usi chiave avanzati (EKU) nel certificato.</span><span class="sxs-lookup"><span data-stu-id="0827d-123">Specifies the enhanced key usages (EKUs) in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0827d-124">-EmailAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="0827d-124">-EmailAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="0827d-125">Specifica il numero di giorni prima della scadenza quando deve iniziare il rinnovo automatico.</span><span class="sxs-lookup"><span data-stu-id="0827d-125">Specifies the number of days before expiration when automatic renewal should start.</span></span>

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

### <span data-ttu-id="0827d-126">-EmailAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="0827d-126">-EmailAtPercentageLifetime</span></span>
<span data-ttu-id="0827d-127">Specifica la percentuale della durata dopo la quale inizia il processo automatico per la notifica.</span><span class="sxs-lookup"><span data-stu-id="0827d-127">Specifies the percentage of the lifetime after which the automatic process for the notification begins.</span></span>

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

### <span data-ttu-id="0827d-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0827d-128">-InputObject</span></span>
<span data-ttu-id="0827d-129">Specifica i criteri di certificato.</span><span class="sxs-lookup"><span data-stu-id="0827d-129">Specifies the certificate policy.</span></span>

```yaml
Type: PSKeyVaultCertificatePolicy
Parameter Sets: ByValue
Aliases: CertificatePolicy

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0827d-130">-IssuerName</span><span class="sxs-lookup"><span data-stu-id="0827d-130">-IssuerName</span></span>
<span data-ttu-id="0827d-131">Specifica il nome dell'autorità di certificazione per il certificato.</span><span class="sxs-lookup"><span data-stu-id="0827d-131">Specifies the name of the issuer for this certificate.</span></span>

```yaml
Type: String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0827d-132">-KeyNotExportable</span><span class="sxs-lookup"><span data-stu-id="0827d-132">-KeyNotExportable</span></span>
<span data-ttu-id="0827d-133">Indica che la chiave non è esportabile.</span><span class="sxs-lookup"><span data-stu-id="0827d-133">Indicates that the key is not exportable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0827d-134">-Tipo di digitare</span><span class="sxs-lookup"><span data-stu-id="0827d-134">-KeyType</span></span>
<span data-ttu-id="0827d-135">Specifica il tipo di chiave della chiave che consente di eseguire il backup del certificato.</span><span class="sxs-lookup"><span data-stu-id="0827d-135">Specifies the key type of the key that backs the certificate.</span></span>
<span data-ttu-id="0827d-136">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="0827d-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0827d-137">RSA</span><span class="sxs-lookup"><span data-stu-id="0827d-137">RSA</span></span>
- <span data-ttu-id="0827d-138">RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="0827d-138">RSA-HSM</span></span>

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

### <span data-ttu-id="0827d-139">-Utilizzo della sintassi</span><span class="sxs-lookup"><span data-stu-id="0827d-139">-KeyUsage</span></span>
<span data-ttu-id="0827d-140">Specifica gli usi chiave nel certificato.</span><span class="sxs-lookup"><span data-stu-id="0827d-140">Specifies the key usages in the certificate.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0827d-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="0827d-141">-Name</span></span>
<span data-ttu-id="0827d-142">Specifica il nome del certificato.</span><span class="sxs-lookup"><span data-stu-id="0827d-142">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="0827d-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0827d-143">-PassThru</span></span>
<span data-ttu-id="0827d-144">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="0827d-144">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0827d-145">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="0827d-145">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0827d-146">-RenewAtNumberOfDaysBeforeExpiry</span><span class="sxs-lookup"><span data-stu-id="0827d-146">-RenewAtNumberOfDaysBeforeExpiry</span></span>
<span data-ttu-id="0827d-147">Specifica il numero di giorni prima della scadenza in cui inizia il processo automatico per il rinnovo del certificato.</span><span class="sxs-lookup"><span data-stu-id="0827d-147">Specifies the number of days before expiry after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: Int32
Parameter Sets: ExpandedRenewNumber
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0827d-148">-RenewAtPercentageLifetime</span><span class="sxs-lookup"><span data-stu-id="0827d-148">-RenewAtPercentageLifetime</span></span>
<span data-ttu-id="0827d-149">Specifica la percentuale della durata dopo la quale inizia il processo automatico per il rinnovo del certificato.</span><span class="sxs-lookup"><span data-stu-id="0827d-149">Specifies the percentage of the lifetime after which the automatic process for certificate renewal begins.</span></span>

```yaml
Type: Int32
Parameter Sets: ExpandedRenewPercentage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0827d-150">-ReuseKeyOnRenewal</span><span class="sxs-lookup"><span data-stu-id="0827d-150">-ReuseKeyOnRenewal</span></span>
<span data-ttu-id="0827d-151">Indica che il certificato riutilizza la chiave durante il rinnovo.</span><span class="sxs-lookup"><span data-stu-id="0827d-151">Indicates that the certificate reuse the key during renewal.</span></span>

```yaml
Type: Boolean
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0827d-152">-SecretContentType</span><span class="sxs-lookup"><span data-stu-id="0827d-152">-SecretContentType</span></span>
<span data-ttu-id="0827d-153">Specifica il tipo di contenuto del nuovo segreto del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="0827d-153">Specifies the content type of the new key vault secret.</span></span>
<span data-ttu-id="0827d-154">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="0827d-154">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0827d-155">applicazione/x-PKCS12</span><span class="sxs-lookup"><span data-stu-id="0827d-155">application/x-pkcs12</span></span>
- <span data-ttu-id="0827d-156">applicazione/x-Pem-file</span><span class="sxs-lookup"><span data-stu-id="0827d-156">application/x-pem-file</span></span>

```yaml
Type: String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:
Accepted values: application/x-pkcs12, application/x-pem-file

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0827d-157">-SubjectName</span><span class="sxs-lookup"><span data-stu-id="0827d-157">-SubjectName</span></span>
<span data-ttu-id="0827d-158">Specifica il nome del soggetto del certificato.</span><span class="sxs-lookup"><span data-stu-id="0827d-158">Specifies the subject name of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0827d-159">-ValidityInMonths</span><span class="sxs-lookup"><span data-stu-id="0827d-159">-ValidityInMonths</span></span>
<span data-ttu-id="0827d-160">Specifica il numero di mesi in cui il certificato è valido.</span><span class="sxs-lookup"><span data-stu-id="0827d-160">Specifies the number of months the certificate is valid.</span></span>

```yaml
Type: Int32
Parameter Sets: ExpandedRenewPercentage, ExpandedRenewNumber
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0827d-161">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="0827d-161">-VaultName</span></span>
<span data-ttu-id="0827d-162">Specifica il nome di un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="0827d-162">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="0827d-163">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0827d-163">-Confirm</span></span>
<span data-ttu-id="0827d-164">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0827d-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0827d-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0827d-165">-WhatIf</span></span>
<span data-ttu-id="0827d-166">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0827d-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0827d-167">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0827d-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0827d-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0827d-168">CommonParameters</span></span>
<span data-ttu-id="0827d-169">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0827d-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0827d-170">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0827d-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0827d-171">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0827d-171">INPUTS</span></span>

### <span data-ttu-id="0827d-172">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0827d-172">None</span></span>
<span data-ttu-id="0827d-173">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="0827d-173">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0827d-174">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0827d-174">OUTPUTS</span></span>

### <span data-ttu-id="0827d-175">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="0827d-175">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="0827d-176">Note</span><span class="sxs-lookup"><span data-stu-id="0827d-176">NOTES</span></span>

## <span data-ttu-id="0827d-177">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0827d-177">RELATED LINKS</span></span>

[<span data-ttu-id="0827d-178">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="0827d-178">Get-AzureKeyVaultCertificatePolicy</span></span>](./Get-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="0827d-179">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="0827d-179">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)

