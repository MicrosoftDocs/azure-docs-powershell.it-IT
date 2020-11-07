---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificateissuer
schema: 2.0.0
ms.openlocfilehash: fcbb19936bb9924f95aa3a20fa026a9c8c723033
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866524"
---
# <span data-ttu-id="ba243-101">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="ba243-101">Get-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="ba243-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ba243-102">SYNOPSIS</span></span>
<span data-ttu-id="ba243-103">Ottiene un emittente di certificati per un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="ba243-103">Gets a certificate issuer for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba243-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ba243-104">SYNTAX</span></span>

### <span data-ttu-id="ba243-105">ByVaultName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ba243-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ba243-106">ByName</span><span class="sxs-lookup"><span data-stu-id="ba243-106">ByName</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba243-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ba243-107">DESCRIPTION</span></span>
<span data-ttu-id="ba243-108">Il cmdlet **Get-AzureKeyVaultCertificateIssuer** ottiene un emittente di certificati specificato o tutti gli emittenti di certificati per un Vault chiave in Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="ba243-108">The **Get-AzureKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="ba243-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ba243-109">EXAMPLES</span></span>

### <span data-ttu-id="ba243-110">Esempio 1: ottenere un emittente di certificati</span><span class="sxs-lookup"><span data-stu-id="ba243-110">Example 1: Get a certificate issuer</span></span>
```
PS C:\>Get-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"
Name                : TestIssuer01
IssuerProvider      : Test
AccountId           : 555
ApiKey              : 
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails
```

<span data-ttu-id="ba243-111">Questo comando consente di ottenere l'autorità di certificazione denominata TestIssuer01.</span><span class="sxs-lookup"><span data-stu-id="ba243-111">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="ba243-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ba243-112">PARAMETERS</span></span>

### <span data-ttu-id="ba243-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba243-113">-DefaultProfile</span></span>
<span data-ttu-id="ba243-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ba243-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba243-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="ba243-115">-Name</span></span>
<span data-ttu-id="ba243-116">Specifica il nome dell'autorità emittente del certificato da ottenere.</span><span class="sxs-lookup"><span data-stu-id="ba243-116">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba243-117">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="ba243-117">-VaultName</span></span>
<span data-ttu-id="ba243-118">Specifica il nome di un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="ba243-118">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="ba243-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba243-119">CommonParameters</span></span>
<span data-ttu-id="ba243-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba243-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba243-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba243-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba243-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ba243-122">INPUTS</span></span>

## <span data-ttu-id="ba243-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ba243-123">OUTPUTS</span></span>

### <span data-ttu-id="ba243-124">Elenco<Microsoft. Azure. Commands. Vault. Models. CertificateIssuerIdentityItem>, Microsoft. Azure. Commands. DataVault. Models. KeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="ba243-124">List<Microsoft.Azure.Commands.KeyVault.Models.CertificateIssuerIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="ba243-125">Note</span><span class="sxs-lookup"><span data-stu-id="ba243-125">NOTES</span></span>

## <span data-ttu-id="ba243-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ba243-126">RELATED LINKS</span></span>

[<span data-ttu-id="ba243-127">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="ba243-127">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="ba243-128">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="ba243-128">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


