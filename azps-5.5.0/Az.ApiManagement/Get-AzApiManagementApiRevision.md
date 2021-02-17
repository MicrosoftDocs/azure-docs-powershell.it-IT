---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRevision.md
ms.openlocfilehash: 16c108d4f62d9bcc44176fce7ede9a7e56d98687
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192558"
---
# <span data-ttu-id="c059b-101">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="c059b-101">Get-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="c059b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c059b-102">SYNOPSIS</span></span>
<span data-ttu-id="c059b-103">Recupera i dettagli di tutte le revisioni delle API di un'API</span><span class="sxs-lookup"><span data-stu-id="c059b-103">Gets details of all the API Revisions of an API</span></span>

## <span data-ttu-id="c059b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c059b-104">SYNTAX</span></span>

```
Get-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c059b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c059b-105">DESCRIPTION</span></span>
<span data-ttu-id="c059b-106">Il cmdlet **Get-AzApiManagementApiRevision** ottiene i dettagli di tutte le revisioni di un'API</span><span class="sxs-lookup"><span data-stu-id="c059b-106">The **Get-AzApiManagementApiRevision** cmdlet gets the details of all revisions of an API</span></span>

## <span data-ttu-id="c059b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c059b-107">EXAMPLES</span></span>

### <span data-ttu-id="c059b-108">Esempio 1: Ottenere tutte le revisioni delle API di un'API</span><span class="sxs-lookup"><span data-stu-id="c059b-108">Example 1: Get all API Revisions of an API</span></span>
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

<span data-ttu-id="c059b-109">Questo comando recupera tutta la revisione dell'API specificata per un particolare contesto ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="c059b-109">This command gets all of the API revision of specified API for particular ApiManagement Context.</span></span>

## <span data-ttu-id="c059b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c059b-110">PARAMETERS</span></span>

### <span data-ttu-id="c059b-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="c059b-111">-ApiId</span></span>
<span data-ttu-id="c059b-112">Identificatore API di cui elencare le revisioni.</span><span class="sxs-lookup"><span data-stu-id="c059b-112">API identifier whose revisions we want to list.</span></span>
<span data-ttu-id="c059b-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="c059b-113">This parameter is required.</span></span>

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

### <span data-ttu-id="c059b-114">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="c059b-114">-ApiRevision</span></span>
<span data-ttu-id="c059b-115">Identificatore di revisione della specifica revisione api.</span><span class="sxs-lookup"><span data-stu-id="c059b-115">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="c059b-116">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c059b-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="c059b-117">-Context</span><span class="sxs-lookup"><span data-stu-id="c059b-117">-Context</span></span>
<span data-ttu-id="c059b-118">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c059b-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c059b-119">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="c059b-119">This parameter is required.</span></span>

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

### <span data-ttu-id="c059b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c059b-120">-DefaultProfile</span></span>
<span data-ttu-id="c059b-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c059b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c059b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c059b-122">CommonParameters</span></span>
<span data-ttu-id="c059b-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c059b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c059b-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c059b-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c059b-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="c059b-125">INPUTS</span></span>

### <span data-ttu-id="c059b-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c059b-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c059b-127">System.String</span><span class="sxs-lookup"><span data-stu-id="c059b-127">System.String</span></span>

## <span data-ttu-id="c059b-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c059b-128">OUTPUTS</span></span>

### <span data-ttu-id="c059b-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="c059b-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRevision</span></span>

## <span data-ttu-id="c059b-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="c059b-130">NOTES</span></span>

## <span data-ttu-id="c059b-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c059b-131">RELATED LINKS</span></span>
