---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: b9188e1bb4d5de4896bf0ca3b2844c7718593ca2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861309"
---
# <span data-ttu-id="f0792-101">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="f0792-101">Get-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="f0792-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f0792-102">SYNOPSIS</span></span>
<span data-ttu-id="f0792-103">Ottiene un emittente di certificati per un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="f0792-103">Gets a certificate issuer for a key vault.</span></span>

## <span data-ttu-id="f0792-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f0792-104">SYNTAX</span></span>

### <span data-ttu-id="f0792-105">ByVaultName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f0792-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultCertificateIssuer [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f0792-106">ByName</span><span class="sxs-lookup"><span data-stu-id="f0792-106">ByName</span></span>
```
Get-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0792-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f0792-107">DESCRIPTION</span></span>
<span data-ttu-id="f0792-108">Il cmdlet **Get-AzKeyVaultCertificateIssuer** ottiene un emittente di certificati specificato o tutti gli emittenti di certificati per un Vault chiave in Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="f0792-108">The **Get-AzKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="f0792-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f0792-109">EXAMPLES</span></span>

### <span data-ttu-id="f0792-110">Esempio 1: ottenere un emittente di certificati</span><span class="sxs-lookup"><span data-stu-id="f0792-110">Example 1: Get a certificate issuer</span></span>
```
PS C:\>Get-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"
Name                : TestIssuer01
IssuerProvider      : Test
AccountId           : 555
ApiKey              : 
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails
```

<span data-ttu-id="f0792-111">Questo comando consente di ottenere l'autorità di certificazione denominata TestIssuer01.</span><span class="sxs-lookup"><span data-stu-id="f0792-111">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="f0792-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f0792-112">PARAMETERS</span></span>

### <span data-ttu-id="f0792-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0792-113">-DefaultProfile</span></span>
<span data-ttu-id="f0792-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f0792-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f0792-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="f0792-115">-Name</span></span>
<span data-ttu-id="f0792-116">Specifica il nome dell'autorità emittente del certificato da ottenere.</span><span class="sxs-lookup"><span data-stu-id="f0792-116">Specifies the name of the certificate issuer to get.</span></span>

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

### <span data-ttu-id="f0792-117">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="f0792-117">-VaultName</span></span>
<span data-ttu-id="f0792-118">Specifica il nome di un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="f0792-118">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="f0792-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0792-119">CommonParameters</span></span>
<span data-ttu-id="f0792-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0792-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0792-121">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0792-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0792-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f0792-122">INPUTS</span></span>

### <span data-ttu-id="f0792-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f0792-123">None</span></span>
<span data-ttu-id="f0792-124">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="f0792-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f0792-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f0792-125">OUTPUTS</span></span>

### <span data-ttu-id="f0792-126">Elenco<Microsoft. Azure. Commands. Vault. Models. CertificateIssuerIdentityItem>, Microsoft. Azure. Commands. DataVault. Models. KeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="f0792-126">List<Microsoft.Azure.Commands.KeyVault.Models.CertificateIssuerIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="f0792-127">Note</span><span class="sxs-lookup"><span data-stu-id="f0792-127">NOTES</span></span>

## <span data-ttu-id="f0792-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f0792-128">RELATED LINKS</span></span>

[<span data-ttu-id="f0792-129">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="f0792-129">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="f0792-130">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="f0792-130">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


