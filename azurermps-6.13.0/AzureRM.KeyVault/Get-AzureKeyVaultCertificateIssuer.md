---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: 83e81e479807c3eada25456d53521dfcecd81f40
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687314"
---
# <span data-ttu-id="0a597-101">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="0a597-101">Get-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="0a597-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0a597-102">SYNOPSIS</span></span>
<span data-ttu-id="0a597-103">Ottiene un emittente di certificati per un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="0a597-103">Gets a certificate issuer for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a597-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0a597-104">SYNTAX</span></span>

### <span data-ttu-id="0a597-105">ByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0a597-105">ByName (Default)</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a597-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0a597-106">ByInputObject</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-InputObject] <PSKeyVault> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a597-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0a597-107">ByResourceId</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-ResourceId] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a597-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0a597-108">DESCRIPTION</span></span>
<span data-ttu-id="0a597-109">Il cmdlet **Get-AzureKeyVaultCertificateIssuer** ottiene un emittente di certificati specificato o tutti gli emittenti di certificati per un Vault chiave in Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="0a597-109">The **Get-AzureKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="0a597-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0a597-110">EXAMPLES</span></span>

### <span data-ttu-id="0a597-111">Esempio 1: ottenere un emittente di certificati</span><span class="sxs-lookup"><span data-stu-id="0a597-111">Example 1: Get a certificate issuer</span></span>
```powershell
PS C:\> Get-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="0a597-112">Questo comando consente di ottenere l'autorità di certificazione denominata TestIssuer01.</span><span class="sxs-lookup"><span data-stu-id="0a597-112">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="0a597-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0a597-113">PARAMETERS</span></span>

### <span data-ttu-id="0a597-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a597-114">-DefaultProfile</span></span>
<span data-ttu-id="0a597-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0a597-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0a597-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a597-116">-InputObject</span></span>
<span data-ttu-id="0a597-117">Oggetto di Vault.</span><span class="sxs-lookup"><span data-stu-id="0a597-117">KeyVault object.</span></span>

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

### <span data-ttu-id="0a597-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="0a597-118">-Name</span></span>
<span data-ttu-id="0a597-119">Specifica il nome dell'autorità emittente del certificato da ottenere.</span><span class="sxs-lookup"><span data-stu-id="0a597-119">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IssuerName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a597-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a597-120">-ResourceId</span></span>
<span data-ttu-id="0a597-121">ID risorsa di un Vault.</span><span class="sxs-lookup"><span data-stu-id="0a597-121">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="0a597-122">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="0a597-122">-VaultName</span></span>
<span data-ttu-id="0a597-123">Specifica il nome di un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="0a597-123">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="0a597-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a597-124">CommonParameters</span></span>
<span data-ttu-id="0a597-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a597-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a597-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a597-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a597-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0a597-127">INPUTS</span></span>

### <span data-ttu-id="0a597-128">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="0a597-128">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="0a597-129">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0a597-129">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="0a597-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0a597-130">System.String</span></span>

## <span data-ttu-id="0a597-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0a597-131">OUTPUTS</span></span>

### <span data-ttu-id="0a597-132">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="0a597-132">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

### <span data-ttu-id="0a597-133">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="0a597-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="0a597-134">Note</span><span class="sxs-lookup"><span data-stu-id="0a597-134">NOTES</span></span>

## <span data-ttu-id="0a597-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0a597-135">RELATED LINKS</span></span>

[<span data-ttu-id="0a597-136">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="0a597-136">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="0a597-137">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="0a597-137">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


