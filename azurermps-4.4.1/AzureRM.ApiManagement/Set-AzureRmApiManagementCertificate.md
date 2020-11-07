---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 12FC21EB-0B4E-4275-88FB-7FF42730A6A0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementCertificate.md
ms.openlocfilehash: ca9305b2d5863276c5d898e310dfab8be7488382
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687740"
---
# <span data-ttu-id="b9ade-101">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="b9ade-101">Set-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="b9ade-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b9ade-102">SYNOPSIS</span></span>
<span data-ttu-id="b9ade-103">Modifica un certificato di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="b9ade-103">Modifies an API Management certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9ade-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b9ade-104">SYNTAX</span></span>

### <span data-ttu-id="b9ade-105">Carica da file (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b9ade-105">Load from file (Default)</span></span>
```
Set-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 -PfxFilePath <String> -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b9ade-106">Non elaborate</span><span class="sxs-lookup"><span data-stu-id="b9ade-106">Raw</span></span>
```
Set-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 -PfxBytes <Byte[]> -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b9ade-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9ade-107">DESCRIPTION</span></span>
<span data-ttu-id="b9ade-108">Il cmdlet **set-AzureRmApiManagementCertificate** modifica un certificato di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="b9ade-108">The **Set-AzureRmApiManagementCertificate** cmdlet modifies an Azure API Management certificate.</span></span>

## <span data-ttu-id="b9ade-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b9ade-109">EXAMPLES</span></span>

### <span data-ttu-id="b9ade-110">Esempio 1: modificare un certificato</span><span class="sxs-lookup"><span data-stu-id="b9ade-110">Example 1: Modify a certificate</span></span>
```
PS C:\>Set-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -PfxFilePath "C:\contoso\certificates\apimanagementnew.pfx" -PfxPassword "2222"
```

<span data-ttu-id="b9ade-111">Questo comando modifica il certificato di gestione delle API specificato.</span><span class="sxs-lookup"><span data-stu-id="b9ade-111">This command modifies the specified API Management certificate.</span></span>

## <span data-ttu-id="b9ade-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b9ade-112">PARAMETERS</span></span>

### <span data-ttu-id="b9ade-113">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="b9ade-113">-CertificateId</span></span>
<span data-ttu-id="b9ade-114">Specifica l'ID del certificato da modificare.</span><span class="sxs-lookup"><span data-stu-id="b9ade-114">Specifies the ID of the certificate to modify.</span></span>

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

### <span data-ttu-id="b9ade-115">-Contesto</span><span class="sxs-lookup"><span data-stu-id="b9ade-115">-Context</span></span>
<span data-ttu-id="b9ade-116">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="b9ade-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b9ade-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b9ade-117">-PassThru</span></span>
<span data-ttu-id="b9ade-118">PassThru</span><span class="sxs-lookup"><span data-stu-id="b9ade-118">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9ade-119">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="b9ade-119">-PfxBytes</span></span>
<span data-ttu-id="b9ade-120">Specifica una matrice di byte del file di certificato in formato pfx.</span><span class="sxs-lookup"><span data-stu-id="b9ade-120">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="b9ade-121">Questo parametro è obbligatorio se non specifichi il parametro *PfxFilePath* .</span><span class="sxs-lookup"><span data-stu-id="b9ade-121">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

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

### <span data-ttu-id="b9ade-122">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="b9ade-122">-PfxFilePath</span></span>
<span data-ttu-id="b9ade-123">Specifica il percorso del file di certificato in formato pfx per creare e caricare.</span><span class="sxs-lookup"><span data-stu-id="b9ade-123">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="b9ade-124">Questo parametro è obbligatorio se non specifichi il parametro *PfxBytes* .</span><span class="sxs-lookup"><span data-stu-id="b9ade-124">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

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

### <span data-ttu-id="b9ade-125">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="b9ade-125">-PfxPassword</span></span>
<span data-ttu-id="b9ade-126">Specifica la password per il certificato.</span><span class="sxs-lookup"><span data-stu-id="b9ade-126">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="b9ade-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9ade-127">-DefaultProfile</span></span>
<span data-ttu-id="b9ade-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b9ade-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9ade-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9ade-129">CommonParameters</span></span>
<span data-ttu-id="b9ade-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9ade-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9ade-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9ade-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9ade-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b9ade-132">INPUTS</span></span>

## <span data-ttu-id="b9ade-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b9ade-133">OUTPUTS</span></span>

### <span data-ttu-id="b9ade-134">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="b9ade-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="b9ade-135">Note</span><span class="sxs-lookup"><span data-stu-id="b9ade-135">NOTES</span></span>

## <span data-ttu-id="b9ade-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b9ade-136">RELATED LINKS</span></span>

[<span data-ttu-id="b9ade-137">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="b9ade-137">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="b9ade-138">New-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="b9ade-138">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="b9ade-139">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="b9ade-139">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)


