---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApiRelease.md
ms.openlocfilehash: 880d96ba0e9eff053084517452c03ffb018b72a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685590"
---
# <span data-ttu-id="4e4f1-101">Get-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="4e4f1-101">Get-AzureRmApiManagementApiRelease</span></span>

## <span data-ttu-id="4e4f1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4e4f1-102">SYNOPSIS</span></span>
<span data-ttu-id="4e4f1-103">Ottenere la versione dell'API.</span><span class="sxs-lookup"><span data-stu-id="4e4f1-103">Get the API Release.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e4f1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4e4f1-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> [-ReleaseId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e4f1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4e4f1-105">DESCRIPTION</span></span>
<span data-ttu-id="4e4f1-106">Il cmdlet **Get-AzureRmApiManagementApiRelease** ottiene una o più versioni dell'API di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="4e4f1-106">The **Get-AzureRmApiManagementApiRelease** cmdlet gets one or more releases of the Azure API Management API.</span></span>

## <span data-ttu-id="4e4f1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4e4f1-107">EXAMPLES</span></span>

### <span data-ttu-id="4e4f1-108">Esempio 1: ottenere tutte le versioni dell'API</span><span class="sxs-lookup"><span data-stu-id="4e4f1-108">Example 1: Get all releases of the API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065
ReleaseId         : 5afccaf6b89fd067426d402e
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 12:21:12 AM
UpdatedDateTime   : 5/17/2018 12:21:12 AM
Notes             : creating a new release
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065/releases/5afccaf6b89fd067426d402e
ResourceGroupName : Api-Default-WestUS
ServiceName       : contos
```

<span data-ttu-id="4e4f1-109">Questo comando consente di ottenere tutte le versioni dell' `echo-api` API per il contesto specificato.</span><span class="sxs-lookup"><span data-stu-id="4e4f1-109">This command gets all of the releases of the `echo-api` API for the specified context.</span></span>

### <span data-ttu-id="4e4f1-110">Esempio 2: ottenere le informazioni sulla versione della versione specifica dell'API</span><span class="sxs-lookup"><span data-stu-id="4e4f1-110">Example 2: Get the release information of the particular API release</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065 -ReleaseId 5afccaf6b89fd067426d402e
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

<span data-ttu-id="4e4f1-111">Questo comando consente di ottenere le informazioni sulle versioni di una specifica API con il releaseId specificato.</span><span class="sxs-lookup"><span data-stu-id="4e4f1-111">This command gets the releases information of a particular API with the specified releaseId.</span></span>

## <span data-ttu-id="4e4f1-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4e4f1-112">PARAMETERS</span></span>

### <span data-ttu-id="4e4f1-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="4e4f1-113">-ApiId</span></span>
<span data-ttu-id="4e4f1-114">Identificatore API da cercare.</span><span class="sxs-lookup"><span data-stu-id="4e4f1-114">API identifier to look for.</span></span>
<span data-ttu-id="4e4f1-115">Se specificato cercherà di ottenere l'API dall'ID.</span><span class="sxs-lookup"><span data-stu-id="4e4f1-115">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="4e4f1-116">-Contesto</span><span class="sxs-lookup"><span data-stu-id="4e4f1-116">-Context</span></span>
<span data-ttu-id="4e4f1-117">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="4e4f1-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="4e4f1-118">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="4e4f1-118">This parameter is required.</span></span>

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

### <span data-ttu-id="4e4f1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e4f1-119">-DefaultProfile</span></span>
<span data-ttu-id="4e4f1-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4e4f1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e4f1-121">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="4e4f1-121">-ReleaseId</span></span>
<span data-ttu-id="4e4f1-122">Identificatore della versione.</span><span class="sxs-lookup"><span data-stu-id="4e4f1-122">The identifier of the Release.</span></span>

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

### <span data-ttu-id="4e4f1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e4f1-123">CommonParameters</span></span>
<span data-ttu-id="4e4f1-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e4f1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e4f1-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e4f1-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e4f1-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4e4f1-126">INPUTS</span></span>

### <span data-ttu-id="4e4f1-127">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4e4f1-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4e4f1-128">System. String</span><span class="sxs-lookup"><span data-stu-id="4e4f1-128">System.String</span></span>

## <span data-ttu-id="4e4f1-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4e4f1-129">OUTPUTS</span></span>

### <span data-ttu-id="4e4f1-130">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="4e4f1-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="4e4f1-131">Note</span><span class="sxs-lookup"><span data-stu-id="4e4f1-131">NOTES</span></span>

## <span data-ttu-id="4e4f1-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4e4f1-132">RELATED LINKS</span></span>

[<span data-ttu-id="4e4f1-133">New-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="4e4f1-133">New-AzureRmApiManagementApiRelease</span></span>](./Get-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="4e4f1-134">Remove-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="4e4f1-134">Remove-AzureRmApiManagementApiRelease</span></span>](./Remove-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="4e4f1-135">Set-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="4e4f1-135">Set-AzureRmApiManagementApiRelease</span></span>](./Set-AzureRmApiManagementApiRelease.md)
