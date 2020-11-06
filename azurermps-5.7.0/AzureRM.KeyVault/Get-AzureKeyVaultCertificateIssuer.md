---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: f19fa119bf307724fb318e0a1d9a390190523bd1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512571"
---
# <span data-ttu-id="8ea1d-101">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="8ea1d-101">Get-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="8ea1d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8ea1d-102">SYNOPSIS</span></span>
<span data-ttu-id="8ea1d-103">Ottiene un emittente di certificati per un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="8ea1d-103">Gets a certificate issuer for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ea1d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8ea1d-104">SYNTAX</span></span>

### <span data-ttu-id="8ea1d-105">ByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8ea1d-105">ByName (Default)</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-VaultName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ea1d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8ea1d-106">ByInputObject</span></span>
```
Get-AzureKeyVaultCertificateIssuer [-InputObject] <PSKeyVault> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ea1d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8ea1d-107">DESCRIPTION</span></span>
<span data-ttu-id="8ea1d-108">Il cmdlet **Get-AzureKeyVaultCertificateIssuer** ottiene un emittente di certificati specificato o tutti gli emittenti di certificati per un Vault chiave in Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="8ea1d-108">The **Get-AzureKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="8ea1d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8ea1d-109">EXAMPLES</span></span>

### <span data-ttu-id="8ea1d-110">Esempio 1: ottenere un emittente di certificati</span><span class="sxs-lookup"><span data-stu-id="8ea1d-110">Example 1: Get a certificate issuer</span></span>
```
PS C:\>Get-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"
Name                : TestIssuer01
IssuerProvider      : Test
AccountId           : 555
ApiKey              : 
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails
```

<span data-ttu-id="8ea1d-111">Questo comando consente di ottenere l'autorità di certificazione denominata TestIssuer01.</span><span class="sxs-lookup"><span data-stu-id="8ea1d-111">This command gets the certificate issuer named TestIssuer01.</span></span>

## <span data-ttu-id="8ea1d-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8ea1d-112">PARAMETERS</span></span>

### <span data-ttu-id="8ea1d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ea1d-113">-DefaultProfile</span></span>
<span data-ttu-id="8ea1d-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8ea1d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8ea1d-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ea1d-115">-InputObject</span></span>
<span data-ttu-id="8ea1d-116">Oggetto di Vault.</span><span class="sxs-lookup"><span data-stu-id="8ea1d-116">KeyVault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ea1d-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="8ea1d-117">-Name</span></span>
<span data-ttu-id="8ea1d-118">Specifica il nome dell'autorità emittente del certificato da ottenere.</span><span class="sxs-lookup"><span data-stu-id="8ea1d-118">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IssuerName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ea1d-119">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="8ea1d-119">-VaultName</span></span>
<span data-ttu-id="8ea1d-120">Specifica il nome di un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="8ea1d-120">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ea1d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ea1d-121">CommonParameters</span></span>
<span data-ttu-id="8ea1d-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ea1d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ea1d-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ea1d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ea1d-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8ea1d-124">INPUTS</span></span>

### <span data-ttu-id="8ea1d-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8ea1d-125">None</span></span>
<span data-ttu-id="8ea1d-126">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="8ea1d-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8ea1d-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8ea1d-127">OUTPUTS</span></span>

### <span data-ttu-id="8ea1d-128">Elenco<Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificateIssuerIdentityItem>, Microsoft. Azure. Commands. DataVault. Models. PSKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="8ea1d-128">List<Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="8ea1d-129">Note</span><span class="sxs-lookup"><span data-stu-id="8ea1d-129">NOTES</span></span>

## <span data-ttu-id="8ea1d-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8ea1d-130">RELATED LINKS</span></span>

[<span data-ttu-id="8ea1d-131">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="8ea1d-131">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="8ea1d-132">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="8ea1d-132">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


