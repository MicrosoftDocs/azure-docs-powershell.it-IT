---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
ms.openlocfilehash: e6b9122481e5e506fc02a13a61b7ebeb71372e96
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366155"
---
# <span data-ttu-id="07000-101">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="07000-101">Get-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="07000-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="07000-102">SYNOPSIS</span></span>
<span data-ttu-id="07000-103">Ottenere i dettagli dei set di versioni dell'API</span><span class="sxs-lookup"><span data-stu-id="07000-103">Get the details of the API Version Sets</span></span>

## <span data-ttu-id="07000-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="07000-104">SYNTAX</span></span>

### <span data-ttu-id="07000-105">ContextParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="07000-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07000-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="07000-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07000-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07000-107">DESCRIPTION</span></span>
<span data-ttu-id="07000-108">Il cmdlet **Get-AzApiManagementApiVersionSet** ottiene i dettagli dei set di versioni dell'API configurati in un contesto di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="07000-108">The **Get-AzApiManagementApiVersionSet** cmdlet gets the details of the API Version Sets configured in an API Management context.</span></span>

## <span data-ttu-id="07000-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="07000-109">EXAMPLES</span></span>

### <span data-ttu-id="07000-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="07000-110">Example 1</span></span>

### <span data-ttu-id="07000-111">Esempio 2: ottenere tutti i set di versioni delle API</span><span class="sxs-lookup"><span data-stu-id="07000-111">Example 2: Get all API Version Sets</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiVersionSet -Context $ApiMgmtContext

ApiVersionSetId   : a93316c8-8b88-46cc-8260-380789a5d598
Description       :
VersionQueryName  :
VersionHeaderName :
DisplayName       : Echo API
VersioningScheme  : Segment
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/a916c8-8b88-46cc-8260-380789a5d598
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso

ApiVersionSetId   : 4cbdfa34-25f3-4a93-a9b6-76b6eade7562
Description       :
VersionQueryName  : api-version
VersionHeaderName :
DisplayName       : getproduct old
VersioningScheme  : Query
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/4cbdfa34-25f3-4a93-a9b6-76b6eade7562
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso


ApiVersionSetId   : 8c441e0e-a0cd-47d8-8d88-f944a83b41bd
Description       :
VersionQueryName  :
VersionHeaderName : Api-Version
DisplayName       : ordersapi
VersioningScheme  : Header
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/8c441e0e-a0cd-47d8-8d88-f944a83b41bd
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="07000-112">Questo comando ottiene tutti i set di versioni dell'API per il contesto specificato.</span><span class="sxs-lookup"><span data-stu-id="07000-112">This command gets all of the API Version sets for the specified context.</span></span>

### <span data-ttu-id="07000-113">Esempio 3: ottenere una versione dell'API impostata da ID</span><span class="sxs-lookup"><span data-stu-id="07000-113">Example 3: Get a API Version Set by ID</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiVersionSet -Context $ApiMgmtContext -ApiVersionSetId $ApiVersionSetId

ApiVersionSetId   : 8c441e0e-a0cd-47d8-8d88-f944a83b41bd
Description       :
VersionQueryName  :
VersionHeaderName : Api-Version
DisplayName       : ordersapi
VersioningScheme  : Header
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/8c441e0e-a0cd-47d8-8d88-f944a83b41bd
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="07000-114">Questo comando ottiene il set di versioni dell'API con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="07000-114">This command gets the API Version Set with the specified ID.</span></span>

## <span data-ttu-id="07000-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="07000-115">PARAMETERS</span></span>

### <span data-ttu-id="07000-116">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="07000-116">-ApiVersionSetId</span></span>
<span data-ttu-id="07000-117">Identificatore API da cercare.</span><span class="sxs-lookup"><span data-stu-id="07000-117">API identifier to look for.</span></span>
<span data-ttu-id="07000-118">Se specificato cercherà di ottenere l'API dall'ID.</span><span class="sxs-lookup"><span data-stu-id="07000-118">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="07000-119">-Contesto</span><span class="sxs-lookup"><span data-stu-id="07000-119">-Context</span></span>
<span data-ttu-id="07000-120">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="07000-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="07000-121">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="07000-121">This parameter is required.</span></span>

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

### <span data-ttu-id="07000-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07000-122">-DefaultProfile</span></span>
<span data-ttu-id="07000-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="07000-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07000-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="07000-124">-ResourceId</span></span>
<span data-ttu-id="07000-125">Identificatore delle risorse ARM della ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="07000-125">Arm Resource Identifier of the ApiVersionSet.</span></span> <span data-ttu-id="07000-126">Se specificato cercherà di trovare apiVersionSet dall'identificatore.</span><span class="sxs-lookup"><span data-stu-id="07000-126">If specified will try to find apiVersionSet by the identifier.</span></span> <span data-ttu-id="07000-127">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="07000-127">This parameter is required.</span></span>

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

### <span data-ttu-id="07000-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07000-128">CommonParameters</span></span>
<span data-ttu-id="07000-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07000-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07000-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="07000-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07000-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="07000-131">INPUTS</span></span>

### <span data-ttu-id="07000-132">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="07000-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="07000-133">System. String</span><span class="sxs-lookup"><span data-stu-id="07000-133">System.String</span></span>

## <span data-ttu-id="07000-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="07000-134">OUTPUTS</span></span>

### <span data-ttu-id="07000-135">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="07000-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="07000-136">Note</span><span class="sxs-lookup"><span data-stu-id="07000-136">NOTES</span></span>

## <span data-ttu-id="07000-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="07000-137">RELATED LINKS</span></span>

[<span data-ttu-id="07000-138">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="07000-138">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="07000-139">Remove-AzApiManagementApiSet</span><span class="sxs-lookup"><span data-stu-id="07000-139">Remove-AzApiManagementApiSet</span></span>](./Remove-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="07000-140">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="07000-140">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)
