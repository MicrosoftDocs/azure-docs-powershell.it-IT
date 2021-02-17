---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: d089cf44e14e70be8b377de310ab4a332ae2d1a1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188182"
---
# <span data-ttu-id="24857-101">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="24857-101">Get-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="24857-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24857-102">SYNOPSIS</span></span>
<span data-ttu-id="24857-103">Ottiene un'autorità di certificazione per un vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="24857-103">Gets a certificate issuer for a key vault.</span></span>

## <span data-ttu-id="24857-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="24857-104">SYNTAX</span></span>

### <span data-ttu-id="24857-105">ByName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="24857-105">ByName (Default)</span></span>
```
Get-AzKeyVaultCertificateIssuer [-VaultName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24857-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="24857-106">ByInputObject</span></span>
```
Get-AzKeyVaultCertificateIssuer [-InputObject] <PSKeyVault> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24857-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="24857-107">ByResourceId</span></span>
```
Get-AzKeyVaultCertificateIssuer [-ResourceId] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24857-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="24857-108">DESCRIPTION</span></span>
<span data-ttu-id="24857-109">Il cmdlet **Get-AzKeyVaultCertificateIss cmdlet** ottiene un'autorità di certificazione specificata o tutte le autorità di certificazione per un vault delle chiavi nel Vault delle chiavi di Azure.</span><span class="sxs-lookup"><span data-stu-id="24857-109">The **Get-AzKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="24857-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="24857-110">EXAMPLES</span></span>

### <span data-ttu-id="24857-111">Esempio 1: Ottenere un'autorità di certificazione</span><span class="sxs-lookup"><span data-stu-id="24857-111">Example 1: Get a certificate issuer</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="24857-112">Questo comando recupera l'autorità di certificazione denominata TestIssuer01.</span><span class="sxs-lookup"><span data-stu-id="24857-112">This command gets the certificate issuer named TestIssuer01.</span></span>

### <span data-ttu-id="24857-113">Esempio 2: Elencare le autorità di certificazione mediante il filtro</span><span class="sxs-lookup"><span data-stu-id="24857-113">Example 2: List certificate issuers using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "test*"

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer02
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="24857-114">Questo comando recupera le autorità di certificazione che iniziano con "test".</span><span class="sxs-lookup"><span data-stu-id="24857-114">This command gets the certificate issuers that start with "test".</span></span>

## <span data-ttu-id="24857-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24857-115">PARAMETERS</span></span>

### <span data-ttu-id="24857-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24857-116">-DefaultProfile</span></span>
<span data-ttu-id="24857-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="24857-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="24857-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24857-118">-InputObject</span></span>
<span data-ttu-id="24857-119">Oggetto KeyVault.</span><span class="sxs-lookup"><span data-stu-id="24857-119">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24857-120">-Name</span><span class="sxs-lookup"><span data-stu-id="24857-120">-Name</span></span>
<span data-ttu-id="24857-121">Specifica il nome dell'autorità di certificazione da ottenere.</span><span class="sxs-lookup"><span data-stu-id="24857-121">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IssuerName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="24857-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24857-122">-ResourceId</span></span>
<span data-ttu-id="24857-123">ID risorsa KeyVault.</span><span class="sxs-lookup"><span data-stu-id="24857-123">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24857-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="24857-124">-VaultName</span></span>
<span data-ttu-id="24857-125">Specifica il nome di un vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="24857-125">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24857-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24857-126">CommonParameters</span></span>
<span data-ttu-id="24857-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24857-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24857-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="24857-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24857-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="24857-129">INPUTS</span></span>

### <span data-ttu-id="24857-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="24857-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="24857-131">System.String</span><span class="sxs-lookup"><span data-stu-id="24857-131">System.String</span></span>

## <span data-ttu-id="24857-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="24857-132">OUTPUTS</span></span>

### <span data-ttu-id="24857-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="24857-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

### <span data-ttu-id="24857-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="24857-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="24857-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="24857-135">NOTES</span></span>

## <span data-ttu-id="24857-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="24857-136">RELATED LINKS</span></span>

[<span data-ttu-id="24857-137">Remove-AzKeyVaultCertificateIsssburg</span><span class="sxs-lookup"><span data-stu-id="24857-137">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="24857-138">Set-AzKeyVaultCertificateIsssburg</span><span class="sxs-lookup"><span data-stu-id="24857-138">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


