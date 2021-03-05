---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRevision.md
ms.openlocfilehash: e653053264baaa343b474f534f30915d725e5553
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990609"
---
# <span data-ttu-id="47da5-101">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="47da5-101">Get-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="47da5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47da5-102">SYNOPSIS</span></span>
<span data-ttu-id="47da5-103">Recupera i dettagli di tutte le revisioni delle API di un'API</span><span class="sxs-lookup"><span data-stu-id="47da5-103">Gets details of all the API Revisions of an API</span></span>

## <span data-ttu-id="47da5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="47da5-104">SYNTAX</span></span>

```
Get-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47da5-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="47da5-105">DESCRIPTION</span></span>
<span data-ttu-id="47da5-106">Il cmdlet **Get-AzApiManagementApiRevision** ottiene i dettagli di tutte le revisioni di un'API</span><span class="sxs-lookup"><span data-stu-id="47da5-106">The **Get-AzApiManagementApiRevision** cmdlet gets the details of all revisions of an API</span></span>

## <span data-ttu-id="47da5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="47da5-107">EXAMPLES</span></span>

### <span data-ttu-id="47da5-108">Esempio 1: Ottenere tutte le revisioni delle API di un'API</span><span class="sxs-lookup"><span data-stu-id="47da5-108">Example 1: Get all API Revisions of an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiRevision -Context $ApiMgmtContext -ApiId "5adf6fbf0faadf3ad8558065"

ApiId           : /apis/5adf6fbf0faadf3ad8558065;rev=3
ApiRevision     : 3
CreatedDateTime : 4/26/2018 10:57:42 PM
UpdatedDateTime : 4/26/2018 10:57:42 PM
Description     : ddsds
PrivateUrl      : /httpbin/v1;rev=3
IsOnline        : True
IsCurrent       : False

ApiId           : /apis/5adf6fbf0faadf3ad8558065;rev=2
ApiRevision     : 2
CreatedDateTime : 4/26/2018 10:57:33 PM
UpdatedDateTime : 4/26/2018 10:57:33 PM
Description     : AA
PrivateUrl      : /httpbin/v1
IsOnline        : True
IsCurrent       : True

ApiId           : /apis/5adf6fbf0faadf3ad8558065;rev=1
ApiRevision     : 1
CreatedDateTime : 4/24/2018 5:56:17 PM
UpdatedDateTime : 5/9/2018 9:29:06 PM
Description     :
PrivateUrl      : /httpbin/v1;rev=1
IsOnline        : True
IsCurrent       : False
```

<span data-ttu-id="47da5-109">Questo comando recupera tutta la revisione dell'API specificata per uno specifico contesto ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="47da5-109">This command gets all of the API revision of specified API for particular ApiManagement Context.</span></span>

## <span data-ttu-id="47da5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47da5-110">PARAMETERS</span></span>

### <span data-ttu-id="47da5-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="47da5-111">-ApiId</span></span>
<span data-ttu-id="47da5-112">Identificatore API di cui si vogliono elencare le revisioni.</span><span class="sxs-lookup"><span data-stu-id="47da5-112">API identifier whose revisions we want to list.</span></span>
<span data-ttu-id="47da5-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="47da5-113">This parameter is required.</span></span>

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

### <span data-ttu-id="47da5-114">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="47da5-114">-ApiRevision</span></span>
<span data-ttu-id="47da5-115">Identificatore di revisione della specifica revisione api.</span><span class="sxs-lookup"><span data-stu-id="47da5-115">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="47da5-116">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="47da5-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="47da5-117">-Context</span><span class="sxs-lookup"><span data-stu-id="47da5-117">-Context</span></span>
<span data-ttu-id="47da5-118">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="47da5-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="47da5-119">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="47da5-119">This parameter is required.</span></span>

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

### <span data-ttu-id="47da5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47da5-120">-DefaultProfile</span></span>
<span data-ttu-id="47da5-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="47da5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47da5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47da5-122">CommonParameters</span></span>
<span data-ttu-id="47da5-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47da5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47da5-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="47da5-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47da5-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="47da5-125">INPUTS</span></span>

### <span data-ttu-id="47da5-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="47da5-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="47da5-127">System.String</span><span class="sxs-lookup"><span data-stu-id="47da5-127">System.String</span></span>

## <span data-ttu-id="47da5-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="47da5-128">OUTPUTS</span></span>

### <span data-ttu-id="47da5-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="47da5-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRevision</span></span>

## <span data-ttu-id="47da5-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="47da5-130">NOTES</span></span>

## <span data-ttu-id="47da5-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="47da5-131">RELATED LINKS</span></span>
