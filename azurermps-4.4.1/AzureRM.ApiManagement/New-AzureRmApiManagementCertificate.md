---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5CBEDFF8-C441-44CC-B011-5F5AAFA2E5C6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCertificate.md
ms.openlocfilehash: 55b95cec3e699872688fad5daeb0d2f7e89059c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517211"
---
# <span data-ttu-id="32676-101">New-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="32676-101">New-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="32676-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="32676-102">SYNOPSIS</span></span>
<span data-ttu-id="32676-103">Crea un certificato di gestione API da usare durante l'autenticazione con backend.</span><span class="sxs-lookup"><span data-stu-id="32676-103">Creates an API Management certificate to be used during Authentication with Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32676-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="32676-104">SYNTAX</span></span>

### <span data-ttu-id="32676-105">Carica da file (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="32676-105">Load from file (Default)</span></span>
```
New-AzureRmApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxFilePath <String> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32676-106">Non elaborate</span><span class="sxs-lookup"><span data-stu-id="32676-106">Raw</span></span>
```
New-AzureRmApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxBytes <Byte[]> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32676-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32676-107">DESCRIPTION</span></span>
<span data-ttu-id="32676-108">Il cmdlet **New-AzureRmApiManagementCertificate** crea un certificato di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="32676-108">The **New-AzureRmApiManagementCertificate** cmdlet creates an Azure API Management certificate.</span></span>

## <span data-ttu-id="32676-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="32676-109">EXAMPLES</span></span>

### <span data-ttu-id="32676-110">Esempio 1: creare e caricare un certificato</span><span class="sxs-lookup"><span data-stu-id="32676-110">Example 1: Create and upload a certificate</span></span>
```
PS C:\>New-AzureRmApiManagementCertificate -Context $ApiMgmtContext -PfxFilePath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111"
```

<span data-ttu-id="32676-111">Questo comando crea un certificato di gestione delle API e lo carica.</span><span class="sxs-lookup"><span data-stu-id="32676-111">This command creates an API Management certificate and uploads it.</span></span>

## <span data-ttu-id="32676-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="32676-112">PARAMETERS</span></span>

### <span data-ttu-id="32676-113">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="32676-113">-CertificateId</span></span>
<span data-ttu-id="32676-114">Specifica l'ID del certificato da creare.</span><span class="sxs-lookup"><span data-stu-id="32676-114">Specifies the ID of the certificate to create.</span></span>
<span data-ttu-id="32676-115">Se non specifichi questo parametro, viene generato un ID.</span><span class="sxs-lookup"><span data-stu-id="32676-115">If you do not specify this parameter, an ID is generated for you.</span></span>

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

### <span data-ttu-id="32676-116">-Contesto</span><span class="sxs-lookup"><span data-stu-id="32676-116">-Context</span></span>
<span data-ttu-id="32676-117">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="32676-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="32676-118">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="32676-118">-PfxBytes</span></span>
<span data-ttu-id="32676-119">Specifica una matrice di byte del file di certificato in formato pfx.</span><span class="sxs-lookup"><span data-stu-id="32676-119">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="32676-120">Questo parametro è obbligatorio se non specifichi il parametro *PfxFilePath* .</span><span class="sxs-lookup"><span data-stu-id="32676-120">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

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

### <span data-ttu-id="32676-121">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="32676-121">-PfxFilePath</span></span>
<span data-ttu-id="32676-122">Specifica il percorso del file di certificato in formato pfx per creare e caricare.</span><span class="sxs-lookup"><span data-stu-id="32676-122">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="32676-123">Questo parametro è obbligatorio se non specifichi il parametro *PfxBytes* .</span><span class="sxs-lookup"><span data-stu-id="32676-123">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Load from file
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32676-124">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="32676-124">-PfxPassword</span></span>
<span data-ttu-id="32676-125">Specifica la password per il certificato.</span><span class="sxs-lookup"><span data-stu-id="32676-125">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="32676-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32676-126">-DefaultProfile</span></span>
<span data-ttu-id="32676-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="32676-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32676-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32676-128">CommonParameters</span></span>
<span data-ttu-id="32676-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32676-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32676-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32676-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32676-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="32676-131">INPUTS</span></span>

## <span data-ttu-id="32676-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="32676-132">OUTPUTS</span></span>

### <span data-ttu-id="32676-133">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="32676-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="32676-134">Note</span><span class="sxs-lookup"><span data-stu-id="32676-134">NOTES</span></span>

## <span data-ttu-id="32676-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="32676-135">RELATED LINKS</span></span>

[<span data-ttu-id="32676-136">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="32676-136">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="32676-137">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="32676-137">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="32676-138">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="32676-138">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)


