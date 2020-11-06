---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: 66c5e949cca8a6f53fdbac89e2745ac7697e14ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520523"
---
# <span data-ttu-id="d9084-101">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="d9084-101">Get-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="d9084-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d9084-102">SYNOPSIS</span></span>
<span data-ttu-id="d9084-103">Ottiene un emittente di certificati per un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="d9084-103">Gets a certificate issuer for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9084-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d9084-104">SYNTAX</span></span>

### <span data-ttu-id="d9084-105">ByVaultName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d9084-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d9084-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d9084-106">ByName</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9084-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d9084-107">DESCRIPTION</span></span>
<span data-ttu-id="d9084-108">Il cmdlet **Get-AzureKeyVaultCertificateIssuer** ottiene un emittente di certificati specificato o tutti gli emittenti di certificati per un Vault chiave in Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="d9084-108">The **Get-AzureKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="d9084-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d9084-109">EXAMPLES</span></span>

### <span data-ttu-id="d9084-110">Esempio 1: ottenere un emittente di certificati</span><span class="sxs-lookup"><span data-stu-id="d9084-110">Example 1: Get a certificate issuer</span></span>
```
PS C:\>Get-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"
Name                : TestIssuer01
IssuerProvider      : Test
AccountId           : 555
ApiKey              : 
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails
```

<span data-ttu-id="d9084-111">Questo comando consente di ottenere l'autorità di certificazione denominata TestIssuer01.</span><span class="sxs-lookup"><span data-stu-id="d9084-111">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="d9084-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d9084-112">PARAMETERS</span></span>

### <span data-ttu-id="d9084-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="d9084-113">-Name</span></span>
<span data-ttu-id="d9084-114">Specifica il nome dell'autorità emittente del certificato da ottenere.</span><span class="sxs-lookup"><span data-stu-id="d9084-114">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: IssuerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9084-115">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="d9084-115">-VaultName</span></span>
<span data-ttu-id="d9084-116">Specifica il nome di un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="d9084-116">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="d9084-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9084-117">-DefaultProfile</span></span>
<span data-ttu-id="d9084-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d9084-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9084-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9084-119">CommonParameters</span></span>
<span data-ttu-id="d9084-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9084-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9084-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9084-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9084-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d9084-122">INPUTS</span></span>

## <span data-ttu-id="d9084-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d9084-123">OUTPUTS</span></span>

### <span data-ttu-id="d9084-124">Elenco<Microsoft. Azure. Commands. Vault. Models. CertificateIssuerIdentityItem>, Microsoft. Azure. Commands. DataVault. Models. KeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="d9084-124">List<Microsoft.Azure.Commands.KeyVault.Models.CertificateIssuerIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="d9084-125">Note</span><span class="sxs-lookup"><span data-stu-id="d9084-125">NOTES</span></span>

## <span data-ttu-id="d9084-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d9084-126">RELATED LINKS</span></span>

[<span data-ttu-id="d9084-127">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="d9084-127">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="d9084-128">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="d9084-128">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


