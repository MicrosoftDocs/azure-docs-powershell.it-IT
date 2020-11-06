---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 0729687C-3104-4136-A80D-16BAEBD6B76C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificatepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificatePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificatePolicy.md
ms.openlocfilehash: 1317b35e957b46e6f39bfb0866e0429c01d35533
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512559"
---
# <span data-ttu-id="9d99c-101">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="9d99c-101">Get-AzureKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="9d99c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9d99c-102">SYNOPSIS</span></span>
<span data-ttu-id="9d99c-103">Ottiene i criteri per un certificato in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="9d99c-103">Gets the policy for a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d99c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9d99c-104">SYNTAX</span></span>

### <span data-ttu-id="9d99c-105">VaultAndCertName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9d99c-105">VaultAndCertName (Default)</span></span>
```
Get-AzureKeyVaultCertificatePolicy [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d99c-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="9d99c-106">InputObject</span></span>
```
Get-AzureKeyVaultCertificatePolicy [-InputObject] <PSKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d99c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9d99c-107">DESCRIPTION</span></span>
<span data-ttu-id="9d99c-108">Il cmdlet **Get-AzureKeyVaultCertificatePolicy** ottiene i criteri per un certificato in un Vault chiave in Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="9d99c-108">The **Get-AzureKeyVaultCertificatePolicy** cmdlet gets the policy for a certificate in a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="9d99c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9d99c-109">EXAMPLES</span></span>

### <span data-ttu-id="9d99c-110">Esempio 1: ottenere un criterio di certificato</span><span class="sxs-lookup"><span data-stu-id="9d99c-110">Example 1: Get a certificate policy</span></span>
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

<span data-ttu-id="9d99c-111">Questo comando consente di ottenere i criteri di certificato per il certificato TestCert01 nel caveau della chiave ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="9d99c-111">This command gets the certificate policy for TestCert01 certificate in the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="9d99c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9d99c-112">PARAMETERS</span></span>

### <span data-ttu-id="9d99c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d99c-113">-DefaultProfile</span></span>
<span data-ttu-id="9d99c-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9d99c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9d99c-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9d99c-115">-InputObject</span></span>
<span data-ttu-id="9d99c-116">Oggetto certificato.</span><span class="sxs-lookup"><span data-stu-id="9d99c-116">Certificate Object.</span></span>

```yaml
Type: PSKeyVaultCertificateIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d99c-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="9d99c-117">-Name</span></span>
<span data-ttu-id="9d99c-118">Specifica il nome di un certificato.</span><span class="sxs-lookup"><span data-stu-id="9d99c-118">Specifies the name of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: VaultAndCertName
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d99c-119">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="9d99c-119">-VaultName</span></span>
<span data-ttu-id="9d99c-120">Specifica il nome di un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="9d99c-120">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: VaultAndCertName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d99c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d99c-121">CommonParameters</span></span>
<span data-ttu-id="9d99c-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d99c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d99c-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d99c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d99c-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9d99c-124">INPUTS</span></span>

### <span data-ttu-id="9d99c-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="9d99c-125">None</span></span>
<span data-ttu-id="9d99c-126">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="9d99c-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9d99c-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9d99c-127">OUTPUTS</span></span>

### <span data-ttu-id="9d99c-128">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="9d99c-128">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="9d99c-129">Note</span><span class="sxs-lookup"><span data-stu-id="9d99c-129">NOTES</span></span>

## <span data-ttu-id="9d99c-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9d99c-130">RELATED LINKS</span></span>

[<span data-ttu-id="9d99c-131">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="9d99c-131">New-AzureKeyVaultCertificatePolicy</span></span>](./New-AzureKeyVaultCertificatePolicy.md)

[<span data-ttu-id="9d99c-132">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="9d99c-132">Set-AzureKeyVaultCertificatePolicy</span></span>](./Set-AzureKeyVaultCertificatePolicy.md)

