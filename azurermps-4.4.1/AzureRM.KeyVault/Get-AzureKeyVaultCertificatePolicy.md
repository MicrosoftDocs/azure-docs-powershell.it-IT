---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: a6b8b4f07d4ac589a0bb700e6303c384e38966fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688015"
---
# <span data-ttu-id="f2795-101">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="f2795-101">Get-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="f2795-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f2795-102">SYNOPSIS</span></span>
<span data-ttu-id="f2795-103">Ottiene i criteri per un certificato in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="f2795-103">Gets the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2795-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f2795-104">SYNTAX</span></span>

```
Get-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2795-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f2795-105">DESCRIPTION</span></span>
<span data-ttu-id="f2795-106">Il cmdlet **Get-AzureKeyVaultCertificatePolicy** ottiene i criteri per un certificato in un Vault chiave in Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="f2795-106">The **Get-AzureKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="f2795-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f2795-107">EXAMPLES</span></span>

### <span data-ttu-id="f2795-108">Esempio 1: ottenere un criterio di certificato</span><span class="sxs-lookup"><span data-stu-id="f2795-108">Example 1: Get a certificate policy</span></span>
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

<span data-ttu-id="f2795-109">Questo comando consente di ottenere i criteri di certificato per il certificato TestCert01 nel caveau della chiave ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="f2795-109">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="f2795-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f2795-110">PARAMETERS</span></span>

### <span data-ttu-id="f2795-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="f2795-111">-Name</span></span>
<span data-ttu-id="f2795-112">Specifica il nome di un certificato.</span><span class="sxs-lookup"><span data-stu-id="f2795-112">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="f2795-113">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="f2795-113">-VaultName</span></span>
<span data-ttu-id="f2795-114">Specifica il nome di un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="f2795-114">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="f2795-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2795-115">-DefaultProfile</span></span>
<span data-ttu-id="f2795-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f2795-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2795-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2795-117">CommonParameters</span></span>
<span data-ttu-id="f2795-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2795-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2795-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2795-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2795-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f2795-120">INPUTS</span></span>

## <span data-ttu-id="f2795-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f2795-121">OUTPUTS</span></span>

### <span data-ttu-id="f2795-122">Microsoft. Azure. Commands. Vault. Models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="f2795-122">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="f2795-123">Note</span><span class="sxs-lookup"><span data-stu-id="f2795-123">NOTES</span></span>

## <span data-ttu-id="f2795-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f2795-124">RELATED LINKS</span></span>

[<span data-ttu-id="f2795-125">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="f2795-125">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="f2795-126">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="f2795-126">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)

