---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: d089cf44e14e70be8b377de310ab4a332ae2d1a1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476207"
---
# <span data-ttu-id="23630-101">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="23630-101">Get-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="23630-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="23630-102">SYNOPSIS</span></span>
<span data-ttu-id="23630-103">Ottiene un emittente di certificati per un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="23630-103">Gets a certificate issuer for a key vault.</span></span>

## <span data-ttu-id="23630-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="23630-104">SYNTAX</span></span>

### <span data-ttu-id="23630-105">ByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="23630-105">ByName (Default)</span></span>
```
Get-AzKeyVaultCertificateIssuer [-VaultName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23630-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="23630-106">ByInputObject</span></span>
```
Get-AzKeyVaultCertificateIssuer [-InputObject] <PSKeyVault> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23630-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="23630-107">ByResourceId</span></span>
```
Get-AzKeyVaultCertificateIssuer [-ResourceId] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23630-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="23630-108">DESCRIPTION</span></span>
<span data-ttu-id="23630-109">Il cmdlet **Get-AzKeyVaultCertificateIssuer** ottiene un emittente di certificati specificato o tutti gli emittenti di certificati per un Vault chiave in Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="23630-109">The **Get-AzKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="23630-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="23630-110">EXAMPLES</span></span>

### <span data-ttu-id="23630-111">Esempio 1: ottenere un emittente di certificati</span><span class="sxs-lookup"><span data-stu-id="23630-111">Example 1: Get a certificate issuer</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="23630-112">Questo comando consente di ottenere l'autorità di certificazione denominata TestIssuer01.</span><span class="sxs-lookup"><span data-stu-id="23630-112">This command gets the certificate issuer named TestIssuer01.</span></span>

### <span data-ttu-id="23630-113">Esempio 2: elenco degli emittenti di certificati tramite filtro</span><span class="sxs-lookup"><span data-stu-id="23630-113">Example 2: List certificate issuers using filtering</span></span>
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

<span data-ttu-id="23630-114">Questo comando consente di ottenere gli emittenti di certificati che iniziano con "test".</span><span class="sxs-lookup"><span data-stu-id="23630-114">This command gets the certificate issuers that start with "test".</span></span>

## <span data-ttu-id="23630-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="23630-115">PARAMETERS</span></span>

### <span data-ttu-id="23630-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23630-116">-DefaultProfile</span></span>
<span data-ttu-id="23630-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="23630-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23630-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23630-118">-InputObject</span></span>
<span data-ttu-id="23630-119">Oggetto di Vault.</span><span class="sxs-lookup"><span data-stu-id="23630-119">KeyVault object.</span></span>

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

### <span data-ttu-id="23630-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="23630-120">-Name</span></span>
<span data-ttu-id="23630-121">Specifica il nome dell'autorità emittente del certificato da ottenere.</span><span class="sxs-lookup"><span data-stu-id="23630-121">Specifies the name of the certificate issuer to get.</span></span>

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

### <span data-ttu-id="23630-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="23630-122">-ResourceId</span></span>
<span data-ttu-id="23630-123">ID risorsa di un Vault.</span><span class="sxs-lookup"><span data-stu-id="23630-123">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="23630-124">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="23630-124">-VaultName</span></span>
<span data-ttu-id="23630-125">Specifica il nome di un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="23630-125">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="23630-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23630-126">CommonParameters</span></span>
<span data-ttu-id="23630-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23630-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23630-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23630-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23630-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="23630-129">INPUTS</span></span>

### <span data-ttu-id="23630-130">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="23630-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="23630-131">System. String</span><span class="sxs-lookup"><span data-stu-id="23630-131">System.String</span></span>

## <span data-ttu-id="23630-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="23630-132">OUTPUTS</span></span>

### <span data-ttu-id="23630-133">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="23630-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

### <span data-ttu-id="23630-134">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="23630-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="23630-135">Note</span><span class="sxs-lookup"><span data-stu-id="23630-135">NOTES</span></span>

## <span data-ttu-id="23630-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="23630-136">RELATED LINKS</span></span>

[<span data-ttu-id="23630-137">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="23630-137">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="23630-138">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="23630-138">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


