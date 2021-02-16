---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
ms.openlocfilehash: 7a3c418c5f55aa70b23972e5cd51065557335866
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187735"
---
# <span data-ttu-id="29cc1-101">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="29cc1-101">Get-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="29cc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29cc1-102">SYNOPSIS</span></span>
<span data-ttu-id="29cc1-103">Ottieni la versione api.</span><span class="sxs-lookup"><span data-stu-id="29cc1-103">Get the API Release.</span></span>

## <span data-ttu-id="29cc1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="29cc1-104">SYNTAX</span></span>

### <span data-ttu-id="29cc1-105">ContextParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="29cc1-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> [-ReleaseId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29cc1-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="29cc1-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiRelease -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="29cc1-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="29cc1-107">DESCRIPTION</span></span>
<span data-ttu-id="29cc1-108">Il cmdlet **Get-AzApiManagementApiRelease** ottiene una o più versioni dell'API di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="29cc1-108">The **Get-AzApiManagementApiRelease** cmdlet gets one or more releases of the Azure API Management API.</span></span>

## <span data-ttu-id="29cc1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="29cc1-109">EXAMPLES</span></span>

### <span data-ttu-id="29cc1-110">Esempio 1: Ottenere tutte le versioni dell'API</span><span class="sxs-lookup"><span data-stu-id="29cc1-110">Example 1: Get all releases of the API</span></span>
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
ServiceName       : contoso
```

<span data-ttu-id="29cc1-111">Questo comando recupera tutte le versioni `echo-api` dell'API per il contesto specificato.</span><span class="sxs-lookup"><span data-stu-id="29cc1-111">This command gets all of the releases of the `echo-api` API for the specified context.</span></span>

### <span data-ttu-id="29cc1-112">Esempio 2: Ottenere le informazioni sulla versione di una specifica API</span><span class="sxs-lookup"><span data-stu-id="29cc1-112">Example 2: Get the release information of the particular API release</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065 -ReleaseId 5afccaf6b89fd067426d402e
ReleaseId         : 5afccaf6b89fd067426d402e
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 12:21:12 AM
UpdatedDateTime   : 5/17/2018 12:21:12 AM
Notes             : creating a new release
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Mi
                    crosoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065/releases/5afccaf6b89fd067426d402
                    e
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="29cc1-113">Questo comando ottiene le informazioni sul rilascio di una particolare API con il valore releaseId specificato.</span><span class="sxs-lookup"><span data-stu-id="29cc1-113">This command gets the releases information of a particular API with the specified releaseId.</span></span>

## <span data-ttu-id="29cc1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29cc1-114">PARAMETERS</span></span>

### <span data-ttu-id="29cc1-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="29cc1-115">-ApiId</span></span>
<span data-ttu-id="29cc1-116">Identificatore API da cercare.</span><span class="sxs-lookup"><span data-stu-id="29cc1-116">API identifier to look for.</span></span>
<span data-ttu-id="29cc1-117">Se specificato, tenterà di ottenere l'API in base all'ID.</span><span class="sxs-lookup"><span data-stu-id="29cc1-117">If specified will try to get the API by the Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29cc1-118">-Context</span><span class="sxs-lookup"><span data-stu-id="29cc1-118">-Context</span></span>
<span data-ttu-id="29cc1-119">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="29cc1-119">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="29cc1-120">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="29cc1-120">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29cc1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29cc1-121">-DefaultProfile</span></span>
<span data-ttu-id="29cc1-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="29cc1-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29cc1-123">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="29cc1-123">-ReleaseId</span></span>
<span data-ttu-id="29cc1-124">L'identificatore del rilascio.</span><span class="sxs-lookup"><span data-stu-id="29cc1-124">The identifier of the Release.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29cc1-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29cc1-125">-ResourceId</span></span>
<span data-ttu-id="29cc1-126">Identificatore di risorsa Arm di una versione dell'Api.</span><span class="sxs-lookup"><span data-stu-id="29cc1-126">Arm Resource Identifier of a Api Release.</span></span> <span data-ttu-id="29cc1-127">Se specificato, tenterà di trovare il rilascio dell'API in base all'identificatore.</span><span class="sxs-lookup"><span data-stu-id="29cc1-127">If specified will try to find api release by the identifier.</span></span> <span data-ttu-id="29cc1-128">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="29cc1-128">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29cc1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29cc1-129">CommonParameters</span></span>
<span data-ttu-id="29cc1-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29cc1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29cc1-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="29cc1-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29cc1-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="29cc1-132">INPUTS</span></span>

### <span data-ttu-id="29cc1-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="29cc1-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="29cc1-134">System.String</span><span class="sxs-lookup"><span data-stu-id="29cc1-134">System.String</span></span>

## <span data-ttu-id="29cc1-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="29cc1-135">OUTPUTS</span></span>

### <span data-ttu-id="29cc1-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="29cc1-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="29cc1-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="29cc1-137">NOTES</span></span>

## <span data-ttu-id="29cc1-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="29cc1-138">RELATED LINKS</span></span>

[<span data-ttu-id="29cc1-139">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="29cc1-139">New-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="29cc1-140">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="29cc1-140">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="29cc1-141">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="29cc1-141">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)