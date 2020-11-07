---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsystemcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSystemCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSystemCertificate.md
ms.openlocfilehash: 834a713e5fb7cc6bfcf24244bbb376eb0f01a8de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675978"
---
# <span data-ttu-id="f43c0-101">New-AzApiManagementSystemCertificate</span><span class="sxs-lookup"><span data-stu-id="f43c0-101">New-AzApiManagementSystemCertificate</span></span>

## <span data-ttu-id="f43c0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f43c0-102">SYNOPSIS</span></span>
<span data-ttu-id="f43c0-103">Crea un'istanza di `PsApiManagementSystemCertificate` .</span><span class="sxs-lookup"><span data-stu-id="f43c0-103">Creates an instance of `PsApiManagementSystemCertificate`.</span></span> <span data-ttu-id="f43c0-104">Il certificato può essere emesso da una CA privata e verrà installato nel servizio di gestione delle API in `CertificateAuthority` o `Root` Store.</span><span class="sxs-lookup"><span data-stu-id="f43c0-104">The certificate can be issued by private CA's and will be installed on the API Management service into `CertificateAuthority` or `Root` store.</span></span>

## <span data-ttu-id="f43c0-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f43c0-105">SYNTAX</span></span>

```
New-AzApiManagementSystemCertificate -StoreName <String> -PfxPath <String> [-PfxPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f43c0-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f43c0-106">DESCRIPTION</span></span>
<span data-ttu-id="f43c0-107">Il cmdlet **New-AzApiManagementSystemCertificate** è un comando helper che crea un'istanza di **PsApiManagementSystemCertificate**.</span><span class="sxs-lookup"><span data-stu-id="f43c0-107">The **New-AzApiManagementSystemCertificate** cmdlet is a helper command that creates an instance of **PsApiManagementSystemCertificate**.</span></span>
<span data-ttu-id="f43c0-108">Questo comando viene usato con il cmdlet New-AzApiManagement e Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="f43c0-108">This command is used with the New-AzApiManagement and Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="f43c0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f43c0-109">EXAMPLES</span></span>

### <span data-ttu-id="f43c0-110">Esempio 1: creare e inizializzare un'istanza di PsApiManagementSystemCertificate usando un certificato SSL da un file</span><span class="sxs-lookup"><span data-stu-id="f43c0-110">Example 1: Create and initialize an instance of PsApiManagementSystemCertificate using an Ssl Certificate from file</span></span>
```powershell
PS C:\>$rootCa = New-AzApiManagementSystemCertificate -StoreName "Root" -PfxPath "C:\contoso\certificates\privateCa.cer"
PS C:\>$systemCert = @($rootCa)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -SystemCertificateConfiguration $systemCert
```

<span data-ttu-id="f43c0-111">Questo comando crea e Inizializza un'istanza di **PsApiManagementSystemCertificate** con un certificato della CA radice.</span><span class="sxs-lookup"><span data-stu-id="f43c0-111">This command creates and initializes an instance of **PsApiManagementSystemCertificate** with a root CA certificate.</span></span> <span data-ttu-id="f43c0-112">Crea quindi il servizio di gestione delle API che installa il certificato CA nell'archivio radice.</span><span class="sxs-lookup"><span data-stu-id="f43c0-112">It then creates and API Management service which installs the CA cert to the Root store.</span></span>

## <span data-ttu-id="f43c0-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f43c0-113">PARAMETERS</span></span>

### <span data-ttu-id="f43c0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f43c0-114">-DefaultProfile</span></span>
<span data-ttu-id="f43c0-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f43c0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f43c0-116">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="f43c0-116">-PfxPassword</span></span>
<span data-ttu-id="f43c0-117">Password per il file di certificato PFX.</span><span class="sxs-lookup"><span data-stu-id="f43c0-117">Password for the .pfx certificate file.</span></span>

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

### <span data-ttu-id="f43c0-118">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="f43c0-118">-PfxPath</span></span>
<span data-ttu-id="f43c0-119">Percorso di un file di certificato PFX.</span><span class="sxs-lookup"><span data-stu-id="f43c0-119">Path to a .pfx certificate file.</span></span>

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

### <span data-ttu-id="f43c0-120">-StoreName</span><span class="sxs-lookup"><span data-stu-id="f43c0-120">-StoreName</span></span>
<span data-ttu-id="f43c0-121">Certificato StoreName</span><span class="sxs-lookup"><span data-stu-id="f43c0-121">Certificate StoreName</span></span>

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

### <span data-ttu-id="f43c0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f43c0-122">CommonParameters</span></span>
<span data-ttu-id="f43c0-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f43c0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f43c0-124">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f43c0-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f43c0-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f43c0-125">INPUTS</span></span>

### <span data-ttu-id="f43c0-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f43c0-126">System.String</span></span>

### <span data-ttu-id="f43c0-127">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="f43c0-127">System.Security.SecureString</span></span>

## <span data-ttu-id="f43c0-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f43c0-128">OUTPUTS</span></span>

### <span data-ttu-id="f43c0-129">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementSystemCertificate</span><span class="sxs-lookup"><span data-stu-id="f43c0-129">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate</span></span>

## <span data-ttu-id="f43c0-130">Note</span><span class="sxs-lookup"><span data-stu-id="f43c0-130">NOTES</span></span>

## <span data-ttu-id="f43c0-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f43c0-131">RELATED LINKS</span></span>

[<span data-ttu-id="f43c0-132">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="f43c0-132">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="f43c0-133">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="f43c0-133">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)