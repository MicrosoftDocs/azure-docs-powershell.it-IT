---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5CBEDFF8-C441-44CC-B011-5F5AAFA2E5C6
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCertificate.md
ms.openlocfilehash: 1fe178b80a39d4587a97207b6bd2d8cf6f4c9731
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93685136"
---
# <span data-ttu-id="910e3-101">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="910e3-101">New-AzApiManagementCertificate</span></span>

## <span data-ttu-id="910e3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="910e3-102">SYNOPSIS</span></span>
<span data-ttu-id="910e3-103">Crea un certificato di gestione API da usare durante l'autenticazione con backend.</span><span class="sxs-lookup"><span data-stu-id="910e3-103">Creates an API Management certificate to be used during Authentication with Backend.</span></span>

## <span data-ttu-id="910e3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="910e3-104">SYNTAX</span></span>

### <span data-ttu-id="910e3-105">LoadFromFile (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="910e3-105">LoadFromFile (Default)</span></span>
```
New-AzApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxFilePath <String> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="910e3-106">Non elaborate</span><span class="sxs-lookup"><span data-stu-id="910e3-106">Raw</span></span>
```
New-AzApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>] -PfxBytes <Byte[]>
 -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="910e3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="910e3-107">DESCRIPTION</span></span>
<span data-ttu-id="910e3-108">Il cmdlet **New-AzApiManagementCertificate** crea un certificato di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="910e3-108">The **New-AzApiManagementCertificate** cmdlet creates an Azure API Management certificate.</span></span>

## <span data-ttu-id="910e3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="910e3-109">EXAMPLES</span></span>

### <span data-ttu-id="910e3-110">Esempio 1: creare e caricare un certificato</span><span class="sxs-lookup"><span data-stu-id="910e3-110">Example 1: Create and upload a certificate</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementCertificate -Context $ApiMgmtContext -PfxFilePath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111"
```

<span data-ttu-id="910e3-111">Questo comando carica un certificato per la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="910e3-111">This command uploads a certificate to Api Management.</span></span> <span data-ttu-id="910e3-112">Questo certificato può essere usato per l'autenticazione reciproca con backend usando i criteri.</span><span class="sxs-lookup"><span data-stu-id="910e3-112">This certificate can be used for mutual authentication with backend using policies.</span></span>

## <span data-ttu-id="910e3-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="910e3-113">PARAMETERS</span></span>

### <span data-ttu-id="910e3-114">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="910e3-114">-CertificateId</span></span>
<span data-ttu-id="910e3-115">Specifica l'ID del certificato da creare.</span><span class="sxs-lookup"><span data-stu-id="910e3-115">Specifies the ID of the certificate to create.</span></span>
<span data-ttu-id="910e3-116">Se non specifichi questo parametro, viene generato un ID.</span><span class="sxs-lookup"><span data-stu-id="910e3-116">If you do not specify this parameter, an ID is generated for you.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="910e3-117">-Contesto</span><span class="sxs-lookup"><span data-stu-id="910e3-117">-Context</span></span>
<span data-ttu-id="910e3-118">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="910e3-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="910e3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="910e3-119">-DefaultProfile</span></span>
<span data-ttu-id="910e3-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="910e3-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="910e3-121">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="910e3-121">-PfxBytes</span></span>
<span data-ttu-id="910e3-122">Specifica una matrice di byte del file di certificato in formato pfx.</span><span class="sxs-lookup"><span data-stu-id="910e3-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="910e3-123">Questo parametro è obbligatorio se non specifichi il parametro *PfxFilePath* .</span><span class="sxs-lookup"><span data-stu-id="910e3-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: Raw
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="910e3-124">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="910e3-124">-PfxFilePath</span></span>
<span data-ttu-id="910e3-125">Specifica il percorso del file di certificato in formato pfx per creare e caricare.</span><span class="sxs-lookup"><span data-stu-id="910e3-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="910e3-126">Questo parametro è obbligatorio se non specifichi il parametro *PfxBytes* .</span><span class="sxs-lookup"><span data-stu-id="910e3-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: LoadFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="910e3-127">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="910e3-127">-PfxPassword</span></span>
<span data-ttu-id="910e3-128">Specifica la password per il certificato.</span><span class="sxs-lookup"><span data-stu-id="910e3-128">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="910e3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="910e3-129">CommonParameters</span></span>
<span data-ttu-id="910e3-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="910e3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="910e3-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="910e3-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="910e3-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="910e3-132">INPUTS</span></span>

### <span data-ttu-id="910e3-133">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="910e3-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="910e3-134">System. String</span><span class="sxs-lookup"><span data-stu-id="910e3-134">System.String</span></span>

### <span data-ttu-id="910e3-135">System. Byte []</span><span class="sxs-lookup"><span data-stu-id="910e3-135">System.Byte[]</span></span>

## <span data-ttu-id="910e3-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="910e3-136">OUTPUTS</span></span>

### <span data-ttu-id="910e3-137">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="910e3-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="910e3-138">Note</span><span class="sxs-lookup"><span data-stu-id="910e3-138">NOTES</span></span>

## <span data-ttu-id="910e3-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="910e3-139">RELATED LINKS</span></span>

[<span data-ttu-id="910e3-140">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="910e3-140">Get-AzApiManagementCertificate</span></span>](./Get-AzApiManagementCertificate.md)

[<span data-ttu-id="910e3-141">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="910e3-141">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)

[<span data-ttu-id="910e3-142">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="910e3-142">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)


