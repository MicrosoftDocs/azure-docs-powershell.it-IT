---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5CBEDFF8-C441-44CC-B011-5F5AAFA2E5C6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCertificate.md
ms.openlocfilehash: f7ddfb327931fc7ebb9eac76cdd6818521332483
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514576"
---
# <span data-ttu-id="1614b-101">New-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="1614b-101">New-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="1614b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1614b-102">SYNOPSIS</span></span>
<span data-ttu-id="1614b-103">Crea un certificato di gestione API da usare durante l'autenticazione con backend.</span><span class="sxs-lookup"><span data-stu-id="1614b-103">Creates an API Management certificate to be used during Authentication with Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1614b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1614b-104">SYNTAX</span></span>

### <span data-ttu-id="1614b-105">LoadFromFile (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1614b-105">LoadFromFile (Default)</span></span>
```
New-AzureRmApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxFilePath <String> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1614b-106">Non elaborate</span><span class="sxs-lookup"><span data-stu-id="1614b-106">Raw</span></span>
```
New-AzureRmApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxBytes <Byte[]> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1614b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1614b-107">DESCRIPTION</span></span>
<span data-ttu-id="1614b-108">Il cmdlet **New-AzureRmApiManagementCertificate** crea un certificato di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="1614b-108">The **New-AzureRmApiManagementCertificate** cmdlet creates an Azure API Management certificate.</span></span>

## <span data-ttu-id="1614b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1614b-109">EXAMPLES</span></span>

### <span data-ttu-id="1614b-110">Esempio 1: creare e caricare un certificato</span><span class="sxs-lookup"><span data-stu-id="1614b-110">Example 1: Create and upload a certificate</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementCertificate -Context $ApiMgmtContext -PfxFilePath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111"
```

<span data-ttu-id="1614b-111">Questo comando carica un certificato per la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="1614b-111">This command uploads a certificate to Api Management.</span></span> <span data-ttu-id="1614b-112">Questo certificato può essere usato per l'autenticazione reciproca con backend usando i criteri.</span><span class="sxs-lookup"><span data-stu-id="1614b-112">This certificate can be used for mutual authentication with backend using policies.</span></span>

## <span data-ttu-id="1614b-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1614b-113">PARAMETERS</span></span>

### <span data-ttu-id="1614b-114">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="1614b-114">-CertificateId</span></span>
<span data-ttu-id="1614b-115">Specifica l'ID del certificato da creare.</span><span class="sxs-lookup"><span data-stu-id="1614b-115">Specifies the ID of the certificate to create.</span></span>
<span data-ttu-id="1614b-116">Se non specifichi questo parametro, viene generato un ID.</span><span class="sxs-lookup"><span data-stu-id="1614b-116">If you do not specify this parameter, an ID is generated for you.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1614b-117">-Contesto</span><span class="sxs-lookup"><span data-stu-id="1614b-117">-Context</span></span>
<span data-ttu-id="1614b-118">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="1614b-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1614b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1614b-119">-DefaultProfile</span></span>
<span data-ttu-id="1614b-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1614b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="1614b-121">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="1614b-121">-PfxBytes</span></span>
<span data-ttu-id="1614b-122">Specifica una matrice di byte del file di certificato in formato pfx.</span><span class="sxs-lookup"><span data-stu-id="1614b-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="1614b-123">Questo parametro è obbligatorio se non specifichi il parametro *PfxFilePath* .</span><span class="sxs-lookup"><span data-stu-id="1614b-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

```yaml
Type: Byte[]
Parameter Sets: Raw
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1614b-124">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="1614b-124">-PfxFilePath</span></span>
<span data-ttu-id="1614b-125">Specifica il percorso del file di certificato in formato pfx per creare e caricare.</span><span class="sxs-lookup"><span data-stu-id="1614b-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="1614b-126">Questo parametro è obbligatorio se non specifichi il parametro *PfxBytes* .</span><span class="sxs-lookup"><span data-stu-id="1614b-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

```yaml
Type: String
Parameter Sets: LoadFromFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1614b-127">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="1614b-127">-PfxPassword</span></span>
<span data-ttu-id="1614b-128">Specifica la password per il certificato.</span><span class="sxs-lookup"><span data-stu-id="1614b-128">Specifies the password for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1614b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1614b-129">CommonParameters</span></span>
<span data-ttu-id="1614b-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1614b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1614b-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1614b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1614b-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1614b-132">INPUTS</span></span>

### <span data-ttu-id="1614b-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1614b-133">None</span></span>
<span data-ttu-id="1614b-134">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="1614b-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1614b-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1614b-135">OUTPUTS</span></span>

### <span data-ttu-id="1614b-136">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="1614b-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="1614b-137">Note</span><span class="sxs-lookup"><span data-stu-id="1614b-137">NOTES</span></span>

## <span data-ttu-id="1614b-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1614b-138">RELATED LINKS</span></span>

[<span data-ttu-id="1614b-139">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="1614b-139">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="1614b-140">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="1614b-140">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="1614b-141">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="1614b-141">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)


