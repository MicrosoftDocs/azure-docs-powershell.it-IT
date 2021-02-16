---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementhttpmessagediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
ms.openlocfilehash: 10c84654bb5d074ee9f668062d1fa7a18d92f8b0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201310"
---
# <span data-ttu-id="41dc4-101">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="41dc4-101">New-AzApiManagementHttpMessageDiagnostic</span></span>

## <span data-ttu-id="41dc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41dc4-102">SYNOPSIS</span></span>
<span data-ttu-id="41dc4-103">Crea un'istanza di **PsApiManagementHttpMessageDiagnostic,** che è un'impostazione diagnostica del messaggio HTTP della diagnostica</span><span class="sxs-lookup"><span data-stu-id="41dc4-103">Creates an instance of **PsApiManagementHttpMessageDiagnostic** which is an Http Message diagnostic setting of the Diagnostic</span></span>

## <span data-ttu-id="41dc4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="41dc4-104">SYNTAX</span></span>

```
New-AzApiManagementHttpMessageDiagnostic [-HeadersToLog <String[]>] [-BodyBytesToLog <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41dc4-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="41dc4-105">DESCRIPTION</span></span>
<span data-ttu-id="41dc4-106">Il cmdlet **New-AzApiManagementHttpMessageDiagnostic** crea l'impostazione di diagnostica Http Message.</span><span class="sxs-lookup"><span data-stu-id="41dc4-106">The cmdlet **New-AzApiManagementHttpMessageDiagnostic** creates the Http Message diagnostic setting.</span></span>

## <span data-ttu-id="41dc4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="41dc4-107">EXAMPLES</span></span>

### <span data-ttu-id="41dc4-108">Esempio 1: Creare un'impostazione di diagnostica per messaggi Http di base</span><span class="sxs-lookup"><span data-stu-id="41dc4-108">Example 1: Create a Basic Http Message diagnostic Setting</span></span>
```powershell
PS C:\>  New-AzApiManagementHttpMessageDiagnostic -Headers 'Content-Type', 'UserAgent' -BodyBytes 100

Headers                   Body
-------                   ----
{Content-Type, UserAgent} Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBodyDiagnosticSetting
```

<span data-ttu-id="41dc4-109">Creare un'impostazione diagnostica per i messaggi http per registrare e intestazioni insieme a `Content-Type` `User-Agent` 100 byte di `body`</span><span class="sxs-lookup"><span data-stu-id="41dc4-109">Create a http message diagnostic setting to log `Content-Type` and `User-Agent` headers along with 100 bytes of `body`</span></span>

## <span data-ttu-id="41dc4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41dc4-110">PARAMETERS</span></span>

### <span data-ttu-id="41dc4-111">-BodyBytesToLog</span><span class="sxs-lookup"><span data-stu-id="41dc4-111">-BodyBytesToLog</span></span>
<span data-ttu-id="41dc4-112">Numero di byte del corpo della richiesta da registrare.</span><span class="sxs-lookup"><span data-stu-id="41dc4-112">Number of request body bytes to log.</span></span> <span data-ttu-id="41dc4-113">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="41dc4-113">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41dc4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41dc4-114">-DefaultProfile</span></span>
<span data-ttu-id="41dc4-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="41dc4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41dc4-116">-HeadersToLog</span><span class="sxs-lookup"><span data-stu-id="41dc4-116">-HeadersToLog</span></span>
<span data-ttu-id="41dc4-117">Matrice di intestazioni da registrare.</span><span class="sxs-lookup"><span data-stu-id="41dc4-117">The array of headers to log.</span></span> <span data-ttu-id="41dc4-118">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="41dc4-118">This parameter is optional.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41dc4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41dc4-119">CommonParameters</span></span>
<span data-ttu-id="41dc4-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41dc4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41dc4-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="41dc4-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41dc4-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="41dc4-122">INPUTS</span></span>

### <span data-ttu-id="41dc4-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="41dc4-123">None</span></span>

## <span data-ttu-id="41dc4-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="41dc4-124">OUTPUTS</span></span>

### <span data-ttu-id="41dc4-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="41dc4-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic</span></span>

## <span data-ttu-id="41dc4-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="41dc4-126">NOTES</span></span>

## <span data-ttu-id="41dc4-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="41dc4-127">RELATED LINKS</span></span>

[<span data-ttu-id="41dc4-128">New-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="41dc4-128">New-AzApiManagementDiagnostic</span></span>](./New-AzApiManagementDiagnostic.md)

[<span data-ttu-id="41dc4-129">New-AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="41dc4-129">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)