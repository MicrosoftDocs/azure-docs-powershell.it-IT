---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
ms.openlocfilehash: 4f9e917f17037e5f47b52501007da5556bde1187
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401080"
---
# <span data-ttu-id="4908f-101">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="4908f-101">Get-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="4908f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4908f-102">SYNOPSIS</span></span>
<span data-ttu-id="4908f-103">Ottieni la versione api.</span><span class="sxs-lookup"><span data-stu-id="4908f-103">Get the API Release.</span></span>

## <span data-ttu-id="4908f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4908f-104">SYNTAX</span></span>

```
Get-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> [-ReleaseId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4908f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4908f-105">DESCRIPTION</span></span>
<span data-ttu-id="4908f-106">Il cmdlet **Get-AzApiManagementApiRelease** ottiene una o più versioni dell'API di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="4908f-106">The **Get-AzApiManagementApiRelease** cmdlet gets one or more releases of the Azure API Management API.</span></span>

## <span data-ttu-id="4908f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4908f-107">EXAMPLES</span></span>

### <span data-ttu-id="4908f-108">Esempio 1: Ottenere tutte le versioni dell'API</span><span class="sxs-lookup"><span data-stu-id="4908f-108">Example 1: Get all releases of the API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065
ReleaseId         : 5afccaf6b89fd067426d402e
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 12:21:12 AM
UpdatedDateTime   : 5/17/2018 12:21:12 AM
Notes             : creating a new release
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065/releases/5afccaf6b89fd067426d402e
ResourceGroupName : Api-Default-WestUS
ServiceName       : contos
```

<span data-ttu-id="4908f-109">Questo comando recupera tutte le versioni `echo-api` dell'API per il contesto specificato.</span><span class="sxs-lookup"><span data-stu-id="4908f-109">This command gets all of the releases of the `echo-api` API for the specified context.</span></span>

### <span data-ttu-id="4908f-110">Esempio 2: Ottenere le informazioni sulla versione della specifica versione dell'API</span><span class="sxs-lookup"><span data-stu-id="4908f-110">Example 2: Get the release information of the particular API release</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065 -ReleaseId 5afccaf6b89fd067426d402e
ReleaseId         : 5afccaf6b89fd067426d402e
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 12:21:12 AM
UpdatedDateTime   : 5/17/2018 12:21:12 AM
Notes             : creating a new release
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Mi
                    crosoft.ApiManagement/service/contos/apis/5adf6fbf0faadf3ad8558065/releases/5afccaf6b89fd067426d402
                    e
ResourceGroupName : Api-Default-WestUS
ServiceName       : contos
```

<span data-ttu-id="4908f-111">Questo comando ottiene le informazioni sul rilascio di una particolare API con il valore releaseId specificato.</span><span class="sxs-lookup"><span data-stu-id="4908f-111">This command gets the releases information of a particular API with the specified releaseId.</span></span>

## <span data-ttu-id="4908f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4908f-112">PARAMETERS</span></span>

### <span data-ttu-id="4908f-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="4908f-113">-ApiId</span></span>
<span data-ttu-id="4908f-114">Identificatore API da cercare.</span><span class="sxs-lookup"><span data-stu-id="4908f-114">API identifier to look for.</span></span>
<span data-ttu-id="4908f-115">Se specificato, tenterà di ottenere l'API con l'ID.</span><span class="sxs-lookup"><span data-stu-id="4908f-115">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="4908f-116">-Context</span><span class="sxs-lookup"><span data-stu-id="4908f-116">-Context</span></span>
<span data-ttu-id="4908f-117">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="4908f-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="4908f-118">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="4908f-118">This parameter is required.</span></span>

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

### <span data-ttu-id="4908f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4908f-119">-DefaultProfile</span></span>
<span data-ttu-id="4908f-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4908f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4908f-121">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="4908f-121">-ReleaseId</span></span>
<span data-ttu-id="4908f-122">L'identificatore del rilascio.</span><span class="sxs-lookup"><span data-stu-id="4908f-122">The identifier of the Release.</span></span>

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

### <span data-ttu-id="4908f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4908f-123">CommonParameters</span></span>
<span data-ttu-id="4908f-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4908f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4908f-125">Per altre informazioni, vedere about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4908f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4908f-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="4908f-126">INPUTS</span></span>

### <span data-ttu-id="4908f-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4908f-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4908f-128">System.String</span><span class="sxs-lookup"><span data-stu-id="4908f-128">System.String</span></span>

## <span data-ttu-id="4908f-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4908f-129">OUTPUTS</span></span>

### <span data-ttu-id="4908f-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="4908f-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="4908f-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="4908f-131">NOTES</span></span>

## <span data-ttu-id="4908f-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4908f-132">RELATED LINKS</span></span>

[<span data-ttu-id="4908f-133">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="4908f-133">New-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="4908f-134">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="4908f-134">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="4908f-135">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="4908f-135">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)