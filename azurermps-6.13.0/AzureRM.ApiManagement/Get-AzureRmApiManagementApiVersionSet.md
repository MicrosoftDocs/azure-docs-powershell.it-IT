---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApiVersionSet.md
ms.openlocfilehash: 60a811aaa097ccc95f8dd57fa105ba4b1388b060
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517707"
---
# <span data-ttu-id="9f520-101">Get-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="9f520-101">Get-AzureRmApiManagementApiVersionSet</span></span>

## <span data-ttu-id="9f520-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9f520-102">SYNOPSIS</span></span>
<span data-ttu-id="9f520-103">Ottenere i dettagli dei set di versioni dell'API</span><span class="sxs-lookup"><span data-stu-id="9f520-103">Get the details of the API Version Sets</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f520-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9f520-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f520-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9f520-105">DESCRIPTION</span></span>
<span data-ttu-id="9f520-106">Il cmdlet **Get-AzureRmApiManagementApiVersionSet** ottiene i dettagli dei set di versioni dell'API configurati in un contesto di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="9f520-106">The **Get-AzureRmApiManagementApiVersionSet** cmdlet gets the details of the API Version Sets configured in an API Management context.</span></span>

## <span data-ttu-id="9f520-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9f520-107">EXAMPLES</span></span>

### <span data-ttu-id="9f520-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9f520-108">Example 1</span></span>

### <span data-ttu-id="9f520-109">Esempio 1: ottenere tutti i set di versioni dell'API</span><span class="sxs-lookup"><span data-stu-id="9f520-109">Example 1: Get all API Version Sets</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApiVersionSet -Context $ApiMgmtContext

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

<span data-ttu-id="9f520-110">Questo comando ottiene tutti i set di versioni dell'API per il contesto specificato.</span><span class="sxs-lookup"><span data-stu-id="9f520-110">This command gets all of the API Version sets for the specified context.</span></span>

### <span data-ttu-id="9f520-111">Esempio 2: ottenere una versione dell'API impostata da ID</span><span class="sxs-lookup"><span data-stu-id="9f520-111">Example 2: Get a API Version Set by ID</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApiVersionSet -Context $ApiMgmtContext -ApiVersionSetId $ApiVersionSetId

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

<span data-ttu-id="9f520-112">Questo comando ottiene il set di versioni dell'API con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="9f520-112">This command gets the API Version Set with the specified ID.</span></span>

## <span data-ttu-id="9f520-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9f520-113">PARAMETERS</span></span>

### <span data-ttu-id="9f520-114">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="9f520-114">-ApiVersionSetId</span></span>
<span data-ttu-id="9f520-115">Identificatore API da cercare.</span><span class="sxs-lookup"><span data-stu-id="9f520-115">API identifier to look for.</span></span>
<span data-ttu-id="9f520-116">Se specificato cercherà di ottenere l'API dall'ID.</span><span class="sxs-lookup"><span data-stu-id="9f520-116">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="9f520-117">-Contesto</span><span class="sxs-lookup"><span data-stu-id="9f520-117">-Context</span></span>
<span data-ttu-id="9f520-118">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="9f520-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="9f520-119">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="9f520-119">This parameter is required.</span></span>

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

### <span data-ttu-id="9f520-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f520-120">-DefaultProfile</span></span>
<span data-ttu-id="9f520-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9f520-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f520-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f520-122">CommonParameters</span></span>
<span data-ttu-id="9f520-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f520-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f520-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f520-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f520-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9f520-125">INPUTS</span></span>

### <span data-ttu-id="9f520-126">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9f520-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9f520-127">System. String</span><span class="sxs-lookup"><span data-stu-id="9f520-127">System.String</span></span>

## <span data-ttu-id="9f520-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9f520-128">OUTPUTS</span></span>

### <span data-ttu-id="9f520-129">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="9f520-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="9f520-130">Note</span><span class="sxs-lookup"><span data-stu-id="9f520-130">NOTES</span></span>

## <span data-ttu-id="9f520-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9f520-131">RELATED LINKS</span></span>

[<span data-ttu-id="9f520-132">New-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="9f520-132">New-AzureRmApiManagementApiVersionSet</span></span>](./New-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="9f520-133">Remove-AzureRmApiManagementApiSet</span><span class="sxs-lookup"><span data-stu-id="9f520-133">Remove-AzureRmApiManagementApiSet</span></span>](./Remove-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="9f520-134">Set-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="9f520-134">Set-AzureRmApiManagementApiVersionSet</span></span>](./Set-AzureRmApiManagementApiSet.md)
