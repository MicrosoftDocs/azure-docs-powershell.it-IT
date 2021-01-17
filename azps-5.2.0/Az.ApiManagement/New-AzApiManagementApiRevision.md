---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
ms.openlocfilehash: 833351c3abbf95eb898405f23241a20fe9affefa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353572"
---
# <span data-ttu-id="fbbb9-101">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="fbbb9-101">New-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="fbbb9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fbbb9-102">SYNOPSIS</span></span>
<span data-ttu-id="fbbb9-103">Crea una nuova revisione di un'API esistente.</span><span class="sxs-lookup"><span data-stu-id="fbbb9-103">Creates a new Revision of an Existing API.</span></span>

## <span data-ttu-id="fbbb9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fbbb9-104">SYNTAX</span></span>

```
New-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ApiRevisionDescription <String>] [-SourceApiRevision <String>] [-ServiceUrl <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbbb9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fbbb9-105">DESCRIPTION</span></span>

<span data-ttu-id="fbbb9-106">Il cmdlet **New-AzApiManagementApiRevision** crea una revisione API per un'API esistente nel contesto di gestione API.</span><span class="sxs-lookup"><span data-stu-id="fbbb9-106">The **New-AzApiManagementApiRevision** cmdlet creates an API Revision for an existing an API in API Management context.</span></span>

## <span data-ttu-id="fbbb9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fbbb9-107">EXAMPLES</span></span>

### <span data-ttu-id="fbbb9-108">Esempio 1: creare una revisione API vuota per un'API</span><span class="sxs-lookup"><span data-stu-id="fbbb9-108">Example 1: Create an empty API Revision for an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5"


New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5"
```

<span data-ttu-id="fbbb9-109">Questo comando crea una revisione API `2` dell' `echo-api` API.</span><span class="sxs-lookup"><span data-stu-id="fbbb9-109">This command creates an API Revision `2` of the `echo-api` API.</span></span>

### <span data-ttu-id="fbbb9-110">Esempio 2: creare una revisione API da un'API esistente e copiare tutte le operazioni, i tag e i criteri</span><span class="sxs-lookup"><span data-stu-id="fbbb9-110">Example 2: Create an API Revision from an Existing Api and copy All operations, tags and Policies</span></span>
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

<span data-ttu-id="fbbb9-111">Questo comando crea una revisione API `5` dell' `echo-api` API.</span><span class="sxs-lookup"><span data-stu-id="fbbb9-111">This command creates an API Revision `5` of the `echo-api` API.</span></span>

## <span data-ttu-id="fbbb9-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fbbb9-112">PARAMETERS</span></span>

### <span data-ttu-id="fbbb9-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="fbbb9-113">-ApiId</span></span>
<span data-ttu-id="fbbb9-114">Identificatore per l'API di cui deve essere creata la revisione.</span><span class="sxs-lookup"><span data-stu-id="fbbb9-114">Identifier for API whose Revision is to be created.</span></span>

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

### <span data-ttu-id="fbbb9-115">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="fbbb9-115">-ApiRevision</span></span>
<span data-ttu-id="fbbb9-116">Identificatore di revisione dell'API.</span><span class="sxs-lookup"><span data-stu-id="fbbb9-116">Revision Identifier of the Api.</span></span>

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

### <span data-ttu-id="fbbb9-117">-ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="fbbb9-117">-ApiRevisionDescription</span></span>
<span data-ttu-id="fbbb9-118">Descrizione della revisione API.</span><span class="sxs-lookup"><span data-stu-id="fbbb9-118">Api Revision Description.</span></span> <span data-ttu-id="fbbb9-119">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fbbb9-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="fbbb9-120">-Contesto</span><span class="sxs-lookup"><span data-stu-id="fbbb9-120">-Context</span></span>
<span data-ttu-id="fbbb9-121">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="fbbb9-121">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="fbbb9-122">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="fbbb9-122">This parameter is required.</span></span>

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

### <span data-ttu-id="fbbb9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbbb9-123">-DefaultProfile</span></span>
<span data-ttu-id="fbbb9-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fbbb9-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbbb9-125">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="fbbb9-125">-ServiceUrl</span></span>
<span data-ttu-id="fbbb9-126">URL del servizio Web che espone l'API nel servizio back-end.</span><span class="sxs-lookup"><span data-stu-id="fbbb9-126">A URL of the web service exposing the API in the Backend service.</span></span> <span data-ttu-id="fbbb9-127">Questo URL verrà usato solo dalla gestione delle API di Azure e non verrà reso pubblico.</span><span class="sxs-lookup"><span data-stu-id="fbbb9-127">This URL will be used by Azure API Management only, and will not be made public.</span></span> <span data-ttu-id="fbbb9-128">Deve essere lunga da 1 a 2000 caratteri.</span><span class="sxs-lookup"><span data-stu-id="fbbb9-128">Must be 1 to 2000 characters long.</span></span> <span data-ttu-id="fbbb9-129">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="fbbb9-129">This parameter is required.</span></span>

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

### <span data-ttu-id="fbbb9-130">-SourceApiRevision</span><span class="sxs-lookup"><span data-stu-id="fbbb9-130">-SourceApiRevision</span></span>
<span data-ttu-id="fbbb9-131">Identificatore di revisione API dell'API di origine.</span><span class="sxs-lookup"><span data-stu-id="fbbb9-131">Api Revision identifier of the source API.</span></span> <span data-ttu-id="fbbb9-132">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fbbb9-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="fbbb9-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fbbb9-133">-Confirm</span></span>
<span data-ttu-id="fbbb9-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbbb9-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbbb9-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbbb9-135">-WhatIf</span></span>
<span data-ttu-id="fbbb9-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fbbb9-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fbbb9-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fbbb9-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbbb9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbbb9-138">CommonParameters</span></span>
<span data-ttu-id="fbbb9-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbbb9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbbb9-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fbbb9-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbbb9-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fbbb9-141">INPUTS</span></span>

### <span data-ttu-id="fbbb9-142">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="fbbb9-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="fbbb9-143">System. String</span><span class="sxs-lookup"><span data-stu-id="fbbb9-143">System.String</span></span>

## <span data-ttu-id="fbbb9-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fbbb9-144">OUTPUTS</span></span>

### <span data-ttu-id="fbbb9-145">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="fbbb9-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="fbbb9-146">Note</span><span class="sxs-lookup"><span data-stu-id="fbbb9-146">NOTES</span></span>

## <span data-ttu-id="fbbb9-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fbbb9-147">RELATED LINKS</span></span>

[<span data-ttu-id="fbbb9-148">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="fbbb9-148">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="fbbb9-149">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="fbbb9-149">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="fbbb9-150">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="fbbb9-150">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)
