---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApiRevision.md
ms.openlocfilehash: 2ee3954569067000d445ecd7dab034db41734829
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512055"
---
# <span data-ttu-id="b835e-101">New-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="b835e-101">New-AzureRmApiManagementApiRevision</span></span>

## <span data-ttu-id="b835e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b835e-102">SYNOPSIS</span></span>
<span data-ttu-id="b835e-103">Crea una nuova revisione di un'API esistente.</span><span class="sxs-lookup"><span data-stu-id="b835e-103">Creates a new Revision of an Existing API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b835e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b835e-104">SYNTAX</span></span>

```
New-AzureRmApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b835e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b835e-105">DESCRIPTION</span></span>

<span data-ttu-id="b835e-106">Il cmdlet **New-AzureRmApiManagementApiRevision** crea una revisione API per un'API esistente nel contesto di gestione API.</span><span class="sxs-lookup"><span data-stu-id="b835e-106">The **New-AzureRmApiManagementApiRevision** cmdlet creates an API Revision for an existing an API in API Management context.</span></span>

## <span data-ttu-id="b835e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b835e-107">EXAMPLES</span></span>

### <span data-ttu-id="b835e-108">Esempio 1: creare una revisione API per un'API</span><span class="sxs-lookup"><span data-stu-id="b835e-108">Example 1: Create an API Revision for an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementApiRevision -Context $ApiMgmtContext  -ApiId 5adf6fbf0faadf3ad8558065 -ApiRevision 6


ApiId                         : 5adf6fbf0faadf3ad8558065;rev=6
Name                          : httpbin.org
Description                   : API Management facade for a very handy and free online HTTP tool.
ServiceUrl                    : https://httpbin.org/
Path                          : httpbin
ApiType                       : http
Protocols                     : {Http, Https}
AuthorizationServerId         : contoso-oauth
AuthorizationScope            : contoso-oauth
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 6
ApiVersion                    : v1
IsCurrent                     : False
IsOnline                      : False
Id                            : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065;rev=6
ResourceGroupName             : Api-Default-WestUS
ServiceName                   : contoso
```

<span data-ttu-id="b835e-109">Questo comando crea una revisione API `2` dell' `echo-api` API.</span><span class="sxs-lookup"><span data-stu-id="b835e-109">This command creates an API Revision `2` of the `echo-api` API.</span></span>

## <span data-ttu-id="b835e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b835e-110">PARAMETERS</span></span>

### <span data-ttu-id="b835e-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="b835e-111">-ApiId</span></span>
<span data-ttu-id="b835e-112">Identificatore per l'API di cui deve essere creata la revisione.</span><span class="sxs-lookup"><span data-stu-id="b835e-112">Identifier for API whose Revision is to be created.</span></span>

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

### <span data-ttu-id="b835e-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="b835e-113">-ApiRevision</span></span>
<span data-ttu-id="b835e-114">Identificatore di revisione dell'API.</span><span class="sxs-lookup"><span data-stu-id="b835e-114">Revision Identifier of the Api.</span></span>

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

### <span data-ttu-id="b835e-115">-Contesto</span><span class="sxs-lookup"><span data-stu-id="b835e-115">-Context</span></span>
<span data-ttu-id="b835e-116">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b835e-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b835e-117">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="b835e-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b835e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b835e-118">-DefaultProfile</span></span>
<span data-ttu-id="b835e-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b835e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b835e-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b835e-120">-Confirm</span></span>
<span data-ttu-id="b835e-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b835e-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b835e-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b835e-122">-WhatIf</span></span>
<span data-ttu-id="b835e-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b835e-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b835e-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b835e-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b835e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b835e-125">CommonParameters</span></span>
<span data-ttu-id="b835e-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b835e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b835e-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b835e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b835e-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b835e-128">INPUTS</span></span>

### <span data-ttu-id="b835e-129">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b835e-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>
<span data-ttu-id="b835e-130">Parameters: Context (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b835e-130">Parameters: Context (ByValue)</span></span>

### <span data-ttu-id="b835e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b835e-131">System.String</span></span>

## <span data-ttu-id="b835e-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b835e-132">OUTPUTS</span></span>

### <span data-ttu-id="b835e-133">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="b835e-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="b835e-134">Note</span><span class="sxs-lookup"><span data-stu-id="b835e-134">NOTES</span></span>

## <span data-ttu-id="b835e-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b835e-135">RELATED LINKS</span></span>

[<span data-ttu-id="b835e-136">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="b835e-136">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="b835e-137">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="b835e-137">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="b835e-138">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="b835e-138">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)
