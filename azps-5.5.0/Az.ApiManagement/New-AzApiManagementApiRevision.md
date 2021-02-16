---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
ms.openlocfilehash: 833351c3abbf95eb898405f23241a20fe9affefa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190398"
---
# <span data-ttu-id="bc7fc-101">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="bc7fc-101">New-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="bc7fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc7fc-102">SYNOPSIS</span></span>
<span data-ttu-id="bc7fc-103">Crea una nuova revisione di un'API esistente.</span><span class="sxs-lookup"><span data-stu-id="bc7fc-103">Creates a new Revision of an Existing API.</span></span>

## <span data-ttu-id="bc7fc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bc7fc-104">SYNTAX</span></span>

```
New-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ApiRevisionDescription <String>] [-SourceApiRevision <String>] [-ServiceUrl <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc7fc-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bc7fc-105">DESCRIPTION</span></span>

<span data-ttu-id="bc7fc-106">Il cmdlet **New-AzApiManagementApiRevision** crea una revisione API per un'API esistente nel contesto di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="bc7fc-106">The **New-AzApiManagementApiRevision** cmdlet creates an API Revision for an existing an API in API Management context.</span></span>

## <span data-ttu-id="bc7fc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bc7fc-107">EXAMPLES</span></span>

### <span data-ttu-id="bc7fc-108">Esempio 1: Creare una revisione api vuota per un'API</span><span class="sxs-lookup"><span data-stu-id="bc7fc-108">Example 1: Create an empty API Revision for an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5"


New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5"
```

<span data-ttu-id="bc7fc-109">Questo comando crea una revisione api `2` `echo-api` dell'API.</span><span class="sxs-lookup"><span data-stu-id="bc7fc-109">This command creates an API Revision `2` of the `echo-api` API.</span></span>

### <span data-ttu-id="bc7fc-110">Esempio 2: Creare una revisione dell'API da un'API esistente e copiare tutte le operazioni, i tag e i criteri</span><span class="sxs-lookup"><span data-stu-id="bc7fc-110">Example 2: Create an API Revision from an Existing Api and copy All operations, tags and Policies</span></span>
```powershell
PS C:\>$context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5" -SourceApiRevision "1" -ServiceUrl "https://echoapi.cloudapp.net/rev4"


ApiId                         : echo-api;rev=5
Name                          : Echo API
Description                   :
ServiceUrl                    : http://echoapi.cloudapp.net/api
Path                          : echo
ApiType                       : http
Protocols                     : {Https}
AuthorizationServerId         :
AuthorizationScope            :
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 5
ApiVersion                    :
IsCurrent                     : False
IsOnline                      : False
SubscriptionRequired          : True
ApiRevisionDescription        :
ApiVersionSetDescription      :
ApiVersionSetId               :
Id                            : /subscriptions/subid/resourceGroups/apimService1/providers/Microsoft.ApiManagement/service/sdktestapim4163/apis/echo-api;rev=5
ResourceGroupName             : apimService1
ServiceName                   : sdktestapim4163
```

<span data-ttu-id="bc7fc-111">Questo comando crea una revisione API `5` `echo-api` dell'API.</span><span class="sxs-lookup"><span data-stu-id="bc7fc-111">This command creates an API Revision `5` of the `echo-api` API.</span></span>

## <span data-ttu-id="bc7fc-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc7fc-112">PARAMETERS</span></span>

### <span data-ttu-id="bc7fc-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="bc7fc-113">-ApiId</span></span>
<span data-ttu-id="bc7fc-114">Identificatore per l'API di cui deve essere creata la revisione.</span><span class="sxs-lookup"><span data-stu-id="bc7fc-114">Identifier for API whose Revision is to be created.</span></span>

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

### <span data-ttu-id="bc7fc-115">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="bc7fc-115">-ApiRevision</span></span>
<span data-ttu-id="bc7fc-116">Identificatore di revisione dell'API.</span><span class="sxs-lookup"><span data-stu-id="bc7fc-116">Revision Identifier of the Api.</span></span>

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

### <span data-ttu-id="bc7fc-117">-ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="bc7fc-117">-ApiRevisionDescription</span></span>
<span data-ttu-id="bc7fc-118">Descrizione della revisione api.</span><span class="sxs-lookup"><span data-stu-id="bc7fc-118">Api Revision Description.</span></span> <span data-ttu-id="bc7fc-119">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="bc7fc-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="bc7fc-120">-Context</span><span class="sxs-lookup"><span data-stu-id="bc7fc-120">-Context</span></span>
<span data-ttu-id="bc7fc-121">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="bc7fc-121">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="bc7fc-122">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="bc7fc-122">This parameter is required.</span></span>

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

### <span data-ttu-id="bc7fc-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc7fc-123">-DefaultProfile</span></span>
<span data-ttu-id="bc7fc-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bc7fc-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc7fc-125">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="bc7fc-125">-ServiceUrl</span></span>
<span data-ttu-id="bc7fc-126">URL del servizio Web che espone l'API nel servizio Back-end.</span><span class="sxs-lookup"><span data-stu-id="bc7fc-126">A URL of the web service exposing the API in the Backend service.</span></span> <span data-ttu-id="bc7fc-127">Questo URL verrà usato solo da Gestione API di Azure e non verrà reso pubblico.</span><span class="sxs-lookup"><span data-stu-id="bc7fc-127">This URL will be used by Azure API Management only, and will not be made public.</span></span> <span data-ttu-id="bc7fc-128">Deve contenere da 1 a 2000 caratteri.</span><span class="sxs-lookup"><span data-stu-id="bc7fc-128">Must be 1 to 2000 characters long.</span></span> <span data-ttu-id="bc7fc-129">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="bc7fc-129">This parameter is required.</span></span>

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

### <span data-ttu-id="bc7fc-130">-SourceApiRevision</span><span class="sxs-lookup"><span data-stu-id="bc7fc-130">-SourceApiRevision</span></span>
<span data-ttu-id="bc7fc-131">Identificatore di revisione API dell'API di origine.</span><span class="sxs-lookup"><span data-stu-id="bc7fc-131">Api Revision identifier of the source API.</span></span> <span data-ttu-id="bc7fc-132">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="bc7fc-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="bc7fc-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bc7fc-133">-Confirm</span></span>
<span data-ttu-id="bc7fc-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc7fc-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc7fc-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc7fc-135">-WhatIf</span></span>
<span data-ttu-id="bc7fc-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bc7fc-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bc7fc-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bc7fc-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc7fc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc7fc-138">CommonParameters</span></span>
<span data-ttu-id="bc7fc-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc7fc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc7fc-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bc7fc-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc7fc-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="bc7fc-141">INPUTS</span></span>

### <span data-ttu-id="bc7fc-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="bc7fc-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="bc7fc-143">System.String</span><span class="sxs-lookup"><span data-stu-id="bc7fc-143">System.String</span></span>

## <span data-ttu-id="bc7fc-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bc7fc-144">OUTPUTS</span></span>

### <span data-ttu-id="bc7fc-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="bc7fc-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="bc7fc-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="bc7fc-146">NOTES</span></span>

## <span data-ttu-id="bc7fc-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bc7fc-147">RELATED LINKS</span></span>

[<span data-ttu-id="bc7fc-148">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="bc7fc-148">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="bc7fc-149">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="bc7fc-149">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="bc7fc-150">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="bc7fc-150">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)
