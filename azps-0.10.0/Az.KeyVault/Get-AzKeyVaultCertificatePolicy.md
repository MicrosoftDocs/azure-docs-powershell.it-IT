---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: d525a47dde9551e5d48c7c316cf6844323b75e81
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861297"
---
# <span data-ttu-id="79c01-101">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="79c01-101">Get-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="79c01-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="79c01-102">SYNOPSIS</span></span>
<span data-ttu-id="79c01-103">Ottiene i criteri per un certificato in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="79c01-103">Gets the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="79c01-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="79c01-104">SYNTAX</span></span>

```
Get-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79c01-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="79c01-105">DESCRIPTION</span></span>
<span data-ttu-id="79c01-106">Il cmdlet **Get-AzKeyVaultCertificatePolicy** ottiene i criteri per un certificato in un Vault chiave in Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="79c01-106">The **Get-AzKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="79c01-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="79c01-107">EXAMPLES</span></span>

### <span data-ttu-id="79c01-108">Esempio 1: ottenere un criterio di certificato</span><span class="sxs-lookup"><span data-stu-id="79c01-108">Example 1: Get a certificate policy</span></span>
```
PS C:\>Get-AzKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01"
SecretContentType               : application/x-pkcs12
Kty                             : RSA
KeySize                         : 2048
Exportable                      : True
ReuseKeyOnRenewal               : True
SubjectName                     : CN=contoso.com
DnsNames                        : 
Ekus                            : {1.3.6.1.5.5.7.3.1, 1.3.6.1.5.5.7.3.2}
ValidityInMonths                : 6
IssuerName                      : Self
RenewAtNumberOfDaysBeforeExpiry : 
RenewAtPercentageLifetime       : 80
EmailOnly                       : False
Enabled                         : True
Created                         : 2/8/2016 11:10:29 PM
Updated                         : 2/8/2016 11:10:29 PM
```

<span data-ttu-id="79c01-109">Questo comando consente di ottenere i criteri di certificato per il certificato TestCert01 nel caveau della chiave ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="79c01-109">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="79c01-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="79c01-110">PARAMETERS</span></span>

### <span data-ttu-id="79c01-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79c01-111">-DefaultProfile</span></span>
<span data-ttu-id="79c01-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="79c01-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79c01-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="79c01-113">-Name</span></span>
<span data-ttu-id="79c01-114">Specifica il nome di un certificato.</span><span class="sxs-lookup"><span data-stu-id="79c01-114">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="79c01-115">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="79c01-115">-VaultName</span></span>
<span data-ttu-id="79c01-116">Specifica il nome di un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="79c01-116">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="79c01-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79c01-117">CommonParameters</span></span>
<span data-ttu-id="79c01-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79c01-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79c01-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79c01-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79c01-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="79c01-120">INPUTS</span></span>

### <span data-ttu-id="79c01-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="79c01-121">None</span></span>
<span data-ttu-id="79c01-122">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="79c01-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="79c01-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="79c01-123">OUTPUTS</span></span>

### <span data-ttu-id="79c01-124">Microsoft. Azure. Commands. Vault. Models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="79c01-124">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="79c01-125">Note</span><span class="sxs-lookup"><span data-stu-id="79c01-125">NOTES</span></span>

## <span data-ttu-id="79c01-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="79c01-126">RELATED LINKS</span></span>

[<span data-ttu-id="79c01-127">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="79c01-127">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="79c01-128">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="79c01-128">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

