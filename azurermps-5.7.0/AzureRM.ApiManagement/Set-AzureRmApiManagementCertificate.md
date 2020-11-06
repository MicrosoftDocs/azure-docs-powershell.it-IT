---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 12FC21EB-0B4E-4275-88FB-7FF42730A6A0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementCertificate.md
ms.openlocfilehash: 1b1f16c8d48debb04ad1f38c03aa58e65f9953a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515839"
---
# <span data-ttu-id="55165-101">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="55165-101">Set-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="55165-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="55165-102">SYNOPSIS</span></span>
<span data-ttu-id="55165-103">Modifica un certificato di gestione delle API configurato per l'autenticazione reciproca con backend.</span><span class="sxs-lookup"><span data-stu-id="55165-103">Modifies an API Management certificate which is configured for mutual authentication with backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55165-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="55165-104">SYNTAX</span></span>

### <span data-ttu-id="55165-105">LoadFromFile (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="55165-105">LoadFromFile (Default)</span></span>
```
Set-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 -PfxFilePath <String> -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="55165-106">Non elaborate</span><span class="sxs-lookup"><span data-stu-id="55165-106">Raw</span></span>
```
Set-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 -PfxBytes <Byte[]> -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="55165-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="55165-107">DESCRIPTION</span></span>
<span data-ttu-id="55165-108">Il cmdlet **set-AzureRmApiManagementCertificate** modifica un certificato di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="55165-108">The **Set-AzureRmApiManagementCertificate** cmdlet modifies an Azure API Management certificate.</span></span>

## <span data-ttu-id="55165-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="55165-109">EXAMPLES</span></span>

### <span data-ttu-id="55165-110">Esempio 1: modificare un certificato</span><span class="sxs-lookup"><span data-stu-id="55165-110">Example 1: Modify a certificate</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -PfxFilePath "C:\contoso\certificates\apimanagementnew.pfx" -PfxPassword "2222"
```

<span data-ttu-id="55165-111">Questo comando modifica il certificato di gestione delle API specificato.</span><span class="sxs-lookup"><span data-stu-id="55165-111">This command modifies the specified API Management certificate.</span></span>

## <span data-ttu-id="55165-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="55165-112">PARAMETERS</span></span>

### <span data-ttu-id="55165-113">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="55165-113">-CertificateId</span></span>
<span data-ttu-id="55165-114">Specifica l'ID del certificato da modificare.</span><span class="sxs-lookup"><span data-stu-id="55165-114">Specifies the ID of the certificate to modify.</span></span>

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

### <span data-ttu-id="55165-115">-Contesto</span><span class="sxs-lookup"><span data-stu-id="55165-115">-Context</span></span>
<span data-ttu-id="55165-116">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="55165-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="55165-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55165-117">-DefaultProfile</span></span>
<span data-ttu-id="55165-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="55165-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="55165-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="55165-119">-PassThru</span></span>
<span data-ttu-id="55165-120">PassThru</span><span class="sxs-lookup"><span data-stu-id="55165-120">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55165-121">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="55165-121">-PfxBytes</span></span>
<span data-ttu-id="55165-122">Specifica una matrice di byte del file di certificato in formato pfx.</span><span class="sxs-lookup"><span data-stu-id="55165-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="55165-123">Questo parametro è obbligatorio se non specifichi il parametro *PfxFilePath* .</span><span class="sxs-lookup"><span data-stu-id="55165-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

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

### <span data-ttu-id="55165-124">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="55165-124">-PfxFilePath</span></span>
<span data-ttu-id="55165-125">Specifica il percorso del file di certificato in formato pfx per creare e caricare.</span><span class="sxs-lookup"><span data-stu-id="55165-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="55165-126">Questo parametro è obbligatorio se non specifichi il parametro *PfxBytes* .</span><span class="sxs-lookup"><span data-stu-id="55165-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

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

### <span data-ttu-id="55165-127">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="55165-127">-PfxPassword</span></span>
<span data-ttu-id="55165-128">Specifica la password per il certificato.</span><span class="sxs-lookup"><span data-stu-id="55165-128">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="55165-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55165-129">CommonParameters</span></span>
<span data-ttu-id="55165-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55165-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55165-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55165-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55165-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="55165-132">INPUTS</span></span>

### <span data-ttu-id="55165-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="55165-133">None</span></span>
<span data-ttu-id="55165-134">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="55165-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="55165-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="55165-135">OUTPUTS</span></span>

### <span data-ttu-id="55165-136">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="55165-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="55165-137">Note</span><span class="sxs-lookup"><span data-stu-id="55165-137">NOTES</span></span>

## <span data-ttu-id="55165-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="55165-138">RELATED LINKS</span></span>

[<span data-ttu-id="55165-139">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="55165-139">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="55165-140">New-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="55165-140">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="55165-141">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="55165-141">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)


