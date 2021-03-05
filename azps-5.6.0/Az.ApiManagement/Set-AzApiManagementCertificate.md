---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 12FC21EB-0B4E-4275-88FB-7FF42730A6A0
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementCertificate.md
ms.openlocfilehash: bb60ce1fc2cb20a24d1b445cf4a3729bf26747ce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965438"
---
# <span data-ttu-id="e190e-101">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="e190e-101">Set-AzApiManagementCertificate</span></span>

## <span data-ttu-id="e190e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e190e-102">SYNOPSIS</span></span>
<span data-ttu-id="e190e-103">Modifica un certificato di gestione API configurato per l'autenticazione reciproca con back-end.</span><span class="sxs-lookup"><span data-stu-id="e190e-103">Modifies an API Management certificate which is configured for mutual authentication with backend.</span></span>

## <span data-ttu-id="e190e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e190e-104">SYNTAX</span></span>

### <span data-ttu-id="e190e-105">LoadFromFile (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e190e-105">LoadFromFile (Default)</span></span>
```
Set-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> -PfxFilePath <String>
 -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e190e-106">Non elaborati</span><span class="sxs-lookup"><span data-stu-id="e190e-106">Raw</span></span>
```
Set-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> -PfxBytes <Byte[]>
 -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e190e-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e190e-107">DESCRIPTION</span></span>
<span data-ttu-id="e190e-108">Il **cmdlet Set-AzApiManagementCertificate** modifica un certificato di Gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="e190e-108">The **Set-AzApiManagementCertificate** cmdlet modifies an Azure API Management certificate.</span></span>

## <span data-ttu-id="e190e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e190e-109">EXAMPLES</span></span>

### <span data-ttu-id="e190e-110">Esempio 1: Modificare un certificato</span><span class="sxs-lookup"><span data-stu-id="e190e-110">Example 1: Modify a certificate</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -PfxFilePath "C:\contoso\certificates\apimanagementnew.pfx" -PfxPassword "2222"
```

<span data-ttu-id="e190e-111">Questo comando modifica il certificato di gestione API specificato.</span><span class="sxs-lookup"><span data-stu-id="e190e-111">This command modifies the specified API Management certificate.</span></span>

## <span data-ttu-id="e190e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e190e-112">PARAMETERS</span></span>

### <span data-ttu-id="e190e-113">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="e190e-113">-CertificateId</span></span>
<span data-ttu-id="e190e-114">Specifica l'ID del certificato da modificare.</span><span class="sxs-lookup"><span data-stu-id="e190e-114">Specifies the ID of the certificate to modify.</span></span>

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

### <span data-ttu-id="e190e-115">-Context</span><span class="sxs-lookup"><span data-stu-id="e190e-115">-Context</span></span>
<span data-ttu-id="e190e-116">Specifica un **oggetto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="e190e-116">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e190e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e190e-117">-DefaultProfile</span></span>
<span data-ttu-id="e190e-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e190e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e190e-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e190e-119">-PassThru</span></span>
<span data-ttu-id="e190e-120">passthru</span><span class="sxs-lookup"><span data-stu-id="e190e-120">passthru</span></span>

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

### <span data-ttu-id="e190e-121">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="e190e-121">-PfxBytes</span></span>
<span data-ttu-id="e190e-122">Specifica una matrice di byte del file di certificato in formato PFX.</span><span class="sxs-lookup"><span data-stu-id="e190e-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="e190e-123">Questo parametro è obbligatorio se non si specifica il *parametro PfxFilePath.*</span><span class="sxs-lookup"><span data-stu-id="e190e-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

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

### <span data-ttu-id="e190e-124">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="e190e-124">-PfxFilePath</span></span>
<span data-ttu-id="e190e-125">Specifica il percorso del file del certificato in formato PFX da creare e caricare.</span><span class="sxs-lookup"><span data-stu-id="e190e-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="e190e-126">Questo parametro è obbligatorio se non si specifica il *parametro PfxBytes.*</span><span class="sxs-lookup"><span data-stu-id="e190e-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

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

### <span data-ttu-id="e190e-127">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="e190e-127">-PfxPassword</span></span>
<span data-ttu-id="e190e-128">Specifica la password per il certificato.</span><span class="sxs-lookup"><span data-stu-id="e190e-128">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="e190e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e190e-129">CommonParameters</span></span>
<span data-ttu-id="e190e-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e190e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e190e-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e190e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e190e-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="e190e-132">INPUTS</span></span>

### <span data-ttu-id="e190e-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e190e-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e190e-134">System.String</span><span class="sxs-lookup"><span data-stu-id="e190e-134">System.String</span></span>

### <span data-ttu-id="e190e-135">System.Byte[]</span><span class="sxs-lookup"><span data-stu-id="e190e-135">System.Byte[]</span></span>

### <span data-ttu-id="e190e-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e190e-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e190e-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e190e-137">OUTPUTS</span></span>

### <span data-ttu-id="e190e-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="e190e-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="e190e-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="e190e-139">NOTES</span></span>

## <span data-ttu-id="e190e-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e190e-140">RELATED LINKS</span></span>

[<span data-ttu-id="e190e-141">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="e190e-141">Get-AzApiManagementCertificate</span></span>](./Get-AzApiManagementCertificate.md)

[<span data-ttu-id="e190e-142">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="e190e-142">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="e190e-143">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="e190e-143">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)


