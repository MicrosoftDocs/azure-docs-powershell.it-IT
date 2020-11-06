---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementsystemcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSystemCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSystemCertificate.md
ms.openlocfilehash: fa64e9bade3a6cd8ec4edc8e04956c97306328ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507768"
---
# <span data-ttu-id="ddf49-101">New-AzureRmApiManagementSystemCertificate</span><span class="sxs-lookup"><span data-stu-id="ddf49-101">New-AzureRmApiManagementSystemCertificate</span></span>

## <span data-ttu-id="ddf49-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ddf49-102">SYNOPSIS</span></span>
<span data-ttu-id="ddf49-103">Crea un'istanza di `PsApiManagementSystemCertificate` .</span><span class="sxs-lookup"><span data-stu-id="ddf49-103">Creates an instance of `PsApiManagementSystemCertificate`.</span></span> <span data-ttu-id="ddf49-104">Il certificato può essere emesso da una CA privata e verrà installato nel servizio di gestione delle API in `CertificateAuthority` o `Root` Store.</span><span class="sxs-lookup"><span data-stu-id="ddf49-104">The certificate can be issued by private CA's and will be installed on the API Management service into `CertificateAuthority` or `Root` store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ddf49-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ddf49-105">SYNTAX</span></span>

```
New-AzureRmApiManagementSystemCertificate -StoreName <String> -PfxPath <String> [-PfxPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ddf49-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ddf49-106">DESCRIPTION</span></span>
<span data-ttu-id="ddf49-107">Il cmdlet **New-AzureRmApiManagementSystemCertificate** è un comando helper che crea un'istanza di **PsApiManagementSystemCertificate**.</span><span class="sxs-lookup"><span data-stu-id="ddf49-107">The **New-AzureRmApiManagementSystemCertificate** cmdlet is a helper command that creates an instance of **PsApiManagementSystemCertificate**.</span></span>
<span data-ttu-id="ddf49-108">Questo comando viene usato con il cmdlet New-AzureRmApiManagement e Set-AzureRmApiManagement.</span><span class="sxs-lookup"><span data-stu-id="ddf49-108">This command is used with the New-AzureRmApiManagement and Set-AzureRmApiManagement cmdlet.</span></span>

## <span data-ttu-id="ddf49-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ddf49-109">EXAMPLES</span></span>

### <span data-ttu-id="ddf49-110">Esempio 1: creare e inizializzare un'istanza di PsApiManagementSystemCertificate usando un certificato SSL da un file</span><span class="sxs-lookup"><span data-stu-id="ddf49-110">Example 1: Create and initialize an instance of PsApiManagementSystemCertificate using an Ssl Certificate from file</span></span>
```powershell
PS C:\>$rootCa = New-AzureRmApiManagementSystemCertificate -StoreName "Root" -PfxPath "C:\contoso\certificates\privateCa.cer"
PS C:\>$systemCert = @($rootCa)
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -SystemCertificateConfiguration $systemCert
```

<span data-ttu-id="ddf49-111">Questo comando crea e Inizializza un'istanza di **PsApiManagementSystemCertificate** con un certificato della CA radice.</span><span class="sxs-lookup"><span data-stu-id="ddf49-111">This command creates and initializes an instance of **PsApiManagementSystemCertificate** with a root CA certificate.</span></span> <span data-ttu-id="ddf49-112">Crea quindi il servizio di gestione delle API che installa il certificato CA nell'archivio radice.</span><span class="sxs-lookup"><span data-stu-id="ddf49-112">It then creates and API Management service which installs the CA cert to the Root store.</span></span>

## <span data-ttu-id="ddf49-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ddf49-113">PARAMETERS</span></span>

### <span data-ttu-id="ddf49-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddf49-114">-DefaultProfile</span></span>
<span data-ttu-id="ddf49-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ddf49-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddf49-116">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="ddf49-116">-PfxPassword</span></span>
<span data-ttu-id="ddf49-117">Password per il file di certificato PFX.</span><span class="sxs-lookup"><span data-stu-id="ddf49-117">Password for the .pfx certificate file.</span></span>

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

### <span data-ttu-id="ddf49-118">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="ddf49-118">-PfxPath</span></span>
<span data-ttu-id="ddf49-119">Percorso di un file di certificato PFX.</span><span class="sxs-lookup"><span data-stu-id="ddf49-119">Path to a .pfx certificate file.</span></span>

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

### <span data-ttu-id="ddf49-120">-StoreName</span><span class="sxs-lookup"><span data-stu-id="ddf49-120">-StoreName</span></span>
<span data-ttu-id="ddf49-121">Certificato StoreName</span><span class="sxs-lookup"><span data-stu-id="ddf49-121">Certificate StoreName</span></span>

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

### <span data-ttu-id="ddf49-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddf49-122">CommonParameters</span></span>
<span data-ttu-id="ddf49-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddf49-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddf49-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddf49-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddf49-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ddf49-125">INPUTS</span></span>

### <span data-ttu-id="ddf49-126">System. String</span><span class="sxs-lookup"><span data-stu-id="ddf49-126">System.String</span></span>

### <span data-ttu-id="ddf49-127">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="ddf49-127">System.Security.SecureString</span></span>

## <span data-ttu-id="ddf49-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ddf49-128">OUTPUTS</span></span>

### <span data-ttu-id="ddf49-129">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementSystemCertificate</span><span class="sxs-lookup"><span data-stu-id="ddf49-129">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate</span></span>

## <span data-ttu-id="ddf49-130">Note</span><span class="sxs-lookup"><span data-stu-id="ddf49-130">NOTES</span></span>

## <span data-ttu-id="ddf49-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ddf49-131">RELATED LINKS</span></span>

[<span data-ttu-id="ddf49-132">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="ddf49-132">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="ddf49-133">Set-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="ddf49-133">Set-AzureRmApiManagement</span></span>](./Set-AzureRmApiManagement.md)
