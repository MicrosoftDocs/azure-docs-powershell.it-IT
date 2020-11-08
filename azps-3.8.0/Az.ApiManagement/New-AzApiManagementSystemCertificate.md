---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsystemcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSystemCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSystemCertificate.md
ms.openlocfilehash: 657a1b729bfa5de8b62c58ed590b5cbf2cf7dca8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020166"
---
# <span data-ttu-id="6101e-101">New-AzApiManagementSystemCertificate</span><span class="sxs-lookup"><span data-stu-id="6101e-101">New-AzApiManagementSystemCertificate</span></span>

## <span data-ttu-id="6101e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6101e-102">SYNOPSIS</span></span>
<span data-ttu-id="6101e-103">Crea un'istanza di `PsApiManagementSystemCertificate` .</span><span class="sxs-lookup"><span data-stu-id="6101e-103">Creates an instance of `PsApiManagementSystemCertificate`.</span></span> <span data-ttu-id="6101e-104">Il certificato può essere emesso da una CA privata e verrà installato nel servizio di gestione delle API in `CertificateAuthority` o `Root` Store.</span><span class="sxs-lookup"><span data-stu-id="6101e-104">The certificate can be issued by private CA's and will be installed on the API Management service into `CertificateAuthority` or `Root` store.</span></span>

## <span data-ttu-id="6101e-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6101e-105">SYNTAX</span></span>

```
New-AzApiManagementSystemCertificate -StoreName <String> -PfxPath <String> [-PfxPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6101e-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6101e-106">DESCRIPTION</span></span>
<span data-ttu-id="6101e-107">Il cmdlet **New-AzApiManagementSystemCertificate** è un comando helper che crea un'istanza di **PsApiManagementSystemCertificate**.</span><span class="sxs-lookup"><span data-stu-id="6101e-107">The **New-AzApiManagementSystemCertificate** cmdlet is a helper command that creates an instance of **PsApiManagementSystemCertificate**.</span></span>
<span data-ttu-id="6101e-108">Questo comando viene usato con il cmdlet New-AzApiManagement e Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="6101e-108">This command is used with the New-AzApiManagement and Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="6101e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6101e-109">EXAMPLES</span></span>

### <span data-ttu-id="6101e-110">Esempio 1: creare e inizializzare un'istanza di PsApiManagementSystemCertificate usando un certificato SSL da un file</span><span class="sxs-lookup"><span data-stu-id="6101e-110">Example 1: Create and initialize an instance of PsApiManagementSystemCertificate using an Ssl Certificate from file</span></span>
```powershell
PS C:\>$rootCa = New-AzApiManagementSystemCertificate -StoreName "Root" -PfxPath "C:\contoso\certificates\privateCa.cer"
PS C:\>$systemCert = @($rootCa)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -SystemCertificateConfiguration $systemCert
```

<span data-ttu-id="6101e-111">Questo comando crea e Inizializza un'istanza di **PsApiManagementSystemCertificate** con un certificato della CA radice.</span><span class="sxs-lookup"><span data-stu-id="6101e-111">This command creates and initializes an instance of **PsApiManagementSystemCertificate** with a root CA certificate.</span></span> <span data-ttu-id="6101e-112">Crea quindi il servizio di gestione delle API che installa il certificato CA nell'archivio radice.</span><span class="sxs-lookup"><span data-stu-id="6101e-112">It then creates and API Management service which installs the CA cert to the Root store.</span></span>

## <span data-ttu-id="6101e-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6101e-113">PARAMETERS</span></span>

### <span data-ttu-id="6101e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6101e-114">-DefaultProfile</span></span>
<span data-ttu-id="6101e-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6101e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6101e-116">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="6101e-116">-PfxPassword</span></span>
<span data-ttu-id="6101e-117">Password per il file di certificato PFX.</span><span class="sxs-lookup"><span data-stu-id="6101e-117">Password for the .pfx certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6101e-118">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="6101e-118">-PfxPath</span></span>
<span data-ttu-id="6101e-119">Percorso di un file di certificato PFX.</span><span class="sxs-lookup"><span data-stu-id="6101e-119">Path to a .pfx certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6101e-120">-StoreName</span><span class="sxs-lookup"><span data-stu-id="6101e-120">-StoreName</span></span>
<span data-ttu-id="6101e-121">Certificato StoreName</span><span class="sxs-lookup"><span data-stu-id="6101e-121">Certificate StoreName</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: CertificateAuthority, Root

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6101e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6101e-122">CommonParameters</span></span>
<span data-ttu-id="6101e-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6101e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6101e-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6101e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6101e-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6101e-125">INPUTS</span></span>

### <span data-ttu-id="6101e-126">System. String</span><span class="sxs-lookup"><span data-stu-id="6101e-126">System.String</span></span>

### <span data-ttu-id="6101e-127">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="6101e-127">System.Security.SecureString</span></span>

## <span data-ttu-id="6101e-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6101e-128">OUTPUTS</span></span>

### <span data-ttu-id="6101e-129">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementSystemCertificate</span><span class="sxs-lookup"><span data-stu-id="6101e-129">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate</span></span>

## <span data-ttu-id="6101e-130">Note</span><span class="sxs-lookup"><span data-stu-id="6101e-130">NOTES</span></span>

## <span data-ttu-id="6101e-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6101e-131">RELATED LINKS</span></span>

[<span data-ttu-id="6101e-132">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="6101e-132">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="6101e-133">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="6101e-133">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)