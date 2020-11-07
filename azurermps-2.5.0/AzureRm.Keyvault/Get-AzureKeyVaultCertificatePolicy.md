---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificatepolicy
schema: 2.0.0
ms.openlocfilehash: 692c639ac42d0a8f2dc2bf121321dfc116ebce1b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866522"
---
# <span data-ttu-id="6fad4-101">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="6fad4-101">Get-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="6fad4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6fad4-102">SYNOPSIS</span></span>
<span data-ttu-id="6fad4-103">Ottiene i criteri per un certificato in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="6fad4-103">Gets the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6fad4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6fad4-104">SYNTAX</span></span>

```
Get-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fad4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6fad4-105">DESCRIPTION</span></span>
<span data-ttu-id="6fad4-106">Il cmdlet **Get-AzureKeyVaultCertificatePolicy** ottiene i criteri per un certificato in un Vault chiave in Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="6fad4-106">The **Get-AzureKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="6fad4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6fad4-107">EXAMPLES</span></span>

### <span data-ttu-id="6fad4-108">Esempio 1: ottenere un criterio di certificato</span><span class="sxs-lookup"><span data-stu-id="6fad4-108">Example 1: Get a certificate policy</span></span>
```
PS C:\>Get-AzureKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01"
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

<span data-ttu-id="6fad4-109">Questo comando consente di ottenere i criteri di certificato per il certificato TestCert01 nel caveau della chiave ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="6fad4-109">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="6fad4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6fad4-110">PARAMETERS</span></span>

### <span data-ttu-id="6fad4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fad4-111">-DefaultProfile</span></span>
<span data-ttu-id="6fad4-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6fad4-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6fad4-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="6fad4-113">-Name</span></span>
<span data-ttu-id="6fad4-114">Specifica il nome di un certificato.</span><span class="sxs-lookup"><span data-stu-id="6fad4-114">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="6fad4-115">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="6fad4-115">-VaultName</span></span>
<span data-ttu-id="6fad4-116">Specifica il nome di un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="6fad4-116">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="6fad4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fad4-117">CommonParameters</span></span>
<span data-ttu-id="6fad4-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fad4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fad4-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fad4-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fad4-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6fad4-120">INPUTS</span></span>

## <span data-ttu-id="6fad4-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6fad4-121">OUTPUTS</span></span>

### <span data-ttu-id="6fad4-122">Microsoft. Azure. Commands. Vault. Models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="6fad4-122">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="6fad4-123">Note</span><span class="sxs-lookup"><span data-stu-id="6fad4-123">NOTES</span></span>

## <span data-ttu-id="6fad4-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6fad4-124">RELATED LINKS</span></span>

[<span data-ttu-id="6fad4-125">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="6fad4-125">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="6fad4-126">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="6fad4-126">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)

