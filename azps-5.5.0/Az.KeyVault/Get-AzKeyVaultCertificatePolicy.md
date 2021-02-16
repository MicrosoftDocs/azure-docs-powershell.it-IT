---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificatePolicy.md
ms.openlocfilehash: d6e2225cc7441d4c370d990aa45c9b2c2bb40457
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209339"
---
# <span data-ttu-id="0c2ca-101">Get-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="0c2ca-101">Get-AzKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="0c2ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c2ca-102">SYNOPSIS</span></span>
<span data-ttu-id="0c2ca-103">Ottiene i criteri per un certificato in un vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="0c2ca-103">Gets the policy for a certificate in a key vault.</span></span>

## <span data-ttu-id="0c2ca-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0c2ca-104">SYNTAX</span></span>

### <span data-ttu-id="0c2ca-105">VaultAndCertName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0c2ca-105">VaultAndCertName (Default)</span></span>
```
Get-AzKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c2ca-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="0c2ca-106">InputObject</span></span>
```
Get-AzKeyVaultCertificatePolicy [-InputObject] <PSKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c2ca-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0c2ca-107">DESCRIPTION</span></span>
<span data-ttu-id="0c2ca-108">Il cmdlet **Get-AzKeyVaultCertificatePolicy** ottiene i criteri per un certificato in un vault delle chiavi nel Vault delle chiavi di Azure.</span><span class="sxs-lookup"><span data-stu-id="0c2ca-108">The **Get-AzKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="0c2ca-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0c2ca-109">EXAMPLES</span></span>

### <span data-ttu-id="0c2ca-110">Esempio 1: Ottenere un criterio di certificato</span><span class="sxs-lookup"><span data-stu-id="0c2ca-110">Example 1: Get a certificate policy</span></span>
```powershell
PS C:\ >Get-AzKeyVaultCertificatePolicy -VaultName "ContosoKV01" -Name "TestCert01"

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
CertificateType                 :
RenewAtNumberOfDaysBeforeExpiry : 
RenewAtPercentageLifetime       : 80
EmailAtNumberOfDaysBeforeExpiry :
EmailAtPercentageLifetime       :
Enabled                         : True
Created                         : 2/8/2016 11:10:29 PM
Updated                         : 2/8/2016 11:10:29 PM
```

<span data-ttu-id="0c2ca-111">Questo comando recupera i criteri di certificato per il certificato TestCert01 nell'vault delle chiavi ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="0c2ca-111">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="0c2ca-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c2ca-112">PARAMETERS</span></span>

### <span data-ttu-id="0c2ca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c2ca-113">-DefaultProfile</span></span>
<span data-ttu-id="0c2ca-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="0c2ca-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c2ca-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c2ca-115">-InputObject</span></span>
<span data-ttu-id="0c2ca-116">Oggetto certificato.</span><span class="sxs-lookup"><span data-stu-id="0c2ca-116">Certificate Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c2ca-117">-Name</span><span class="sxs-lookup"><span data-stu-id="0c2ca-117">-Name</span></span>
<span data-ttu-id="0c2ca-118">Specifica il nome di un certificato.</span><span class="sxs-lookup"><span data-stu-id="0c2ca-118">Specifies the name of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: VaultAndCertName
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c2ca-119">-VaultName</span><span class="sxs-lookup"><span data-stu-id="0c2ca-119">-VaultName</span></span>
<span data-ttu-id="0c2ca-120">Specifica il nome di un vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="0c2ca-120">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: VaultAndCertName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c2ca-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c2ca-121">CommonParameters</span></span>
<span data-ttu-id="0c2ca-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c2ca-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c2ca-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0c2ca-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c2ca-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="0c2ca-124">INPUTS</span></span>

### <span data-ttu-id="0c2ca-125">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="0c2ca-125">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="0c2ca-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0c2ca-126">OUTPUTS</span></span>

### <span data-ttu-id="0c2ca-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="0c2ca-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="0c2ca-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="0c2ca-128">NOTES</span></span>

## <span data-ttu-id="0c2ca-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0c2ca-129">RELATED LINKS</span></span>

[<span data-ttu-id="0c2ca-130">New-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="0c2ca-130">New-AzKeyVaultCertificatePolicy</span></span>](./New-AzKeyVaultCertificatePolicy.md)

[<span data-ttu-id="0c2ca-131">Set-AzKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="0c2ca-131">Set-AzKeyVaultCertificatePolicy</span></span>](./Set-AzKeyVaultCertificatePolicy.md)

