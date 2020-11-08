---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementDiagnostic.md
ms.openlocfilehash: c31c3d23e8e5ed160aff55a3599137454f1c638c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019896"
---
# <span data-ttu-id="b5c43-101">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="b5c43-101">Get-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="b5c43-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b5c43-102">SYNOPSIS</span></span>
<span data-ttu-id="b5c43-103">Ottenere informazioni dettagliate sulla diagnostica configurata a livello di servizio o API.</span><span class="sxs-lookup"><span data-stu-id="b5c43-103">Get details of the Diagnostic configured at the service level or the Api Level.</span></span> <span data-ttu-id="b5c43-104">La diagnostica viene usata per registrare le richieste e le risposte dal gateway di gestione API.</span><span class="sxs-lookup"><span data-stu-id="b5c43-104">Diagnostics are used to log requests/responses from Api Management gateway.</span></span>

## <span data-ttu-id="b5c43-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b5c43-105">SYNTAX</span></span>

### <span data-ttu-id="b5c43-106">ContextParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b5c43-106">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementDiagnostic -Context <PsApiManagementContext> [-DiagnosticId <String>] [-ApiId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5c43-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5c43-107">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementDiagnostic -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b5c43-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b5c43-108">DESCRIPTION</span></span>
<span data-ttu-id="b5c43-109">**Get-AzApiManagementDiagnostic** ottiene i dettagli della diagnostica configurata nel servizio di gestione delle API in un ambito specifico.</span><span class="sxs-lookup"><span data-stu-id="b5c43-109">The **Get-AzApiManagementDiagnostic** gets details of the diagnostics configured in the Api management service at a given scope.</span></span>

## <span data-ttu-id="b5c43-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b5c43-110">EXAMPLES</span></span>

### <span data-ttu-id="b5c43-111">Esempio 1: ottenere tutta la diagnostica configurata nell'ambito del tenant.</span><span class="sxs-lookup"><span data-stu-id="b5c43-111">Example 1: Get all the diagnostic configured at the tenant scope.</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementDiagnostic -Context $apimContext

DiagnosticId                 : applicationinsights
ApiId                        :
AlwaysLog                    : allErrors
LoggerId                     : backendapisachinc
EnableHttpCorrelationHeaders : True
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              :
BackendSetting               :
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/diagnostics/applicationinsights
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso

DiagnosticId                 : azuremonitor
ApiId                        :
AlwaysLog                    :
LoggerId                     : azuremonitor
EnableHttpCorrelationHeaders :
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              :
BackendSetting               : 
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/diagnostics/azuremonitor
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso
```

<span data-ttu-id="b5c43-112">Questo comando consente di ottenere tutte le diagnostica configurate nel servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="b5c43-112">This command gets all the diagnostics configured in the Api Management service.</span></span>

### <span data-ttu-id="b5c43-113">Esempio 2: ottenere tutte le diagnostica configurate nell'ambito dell'API</span><span class="sxs-lookup"><span data-stu-id="b5c43-113">Example 2: Get all the diagnostics configured at the Api scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementDiagnostic -Context $apimContext -ApiId "echo-api"

DiagnosticId                 : applicationinsights
ApiId                        : echo-api
AlwaysLog                    : allErrors
LoggerId                     : backendapisachinc
EnableHttpCorrelationHeaders : True
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
BackendSetting               : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/diagnostics/applicationinsights
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso
```

<span data-ttu-id="b5c43-114">Questo comando consente di ottenere tutte le diagnostica configurate nell' `echo-api` ambito dell'API</span><span class="sxs-lookup"><span data-stu-id="b5c43-114">This command gets all the diagnostics configured at the `echo-api` Api scope</span></span>

### <span data-ttu-id="b5c43-115">Esempio 3: ottenere il sistema di diagnostica dell'ambito API specificato da un ID</span><span class="sxs-lookup"><span data-stu-id="b5c43-115">Example 3: Get the API-scope diagnostic specified by an Id</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementDiagnostic -Context $apimContext -ApiId "echo-api" -DiagnosticId "applicationinsights"

DiagnosticId                 : applicationinsights
ApiId                        : echo-api
AlwaysLog                    : allErrors
LoggerId                     : backendapisachinc
EnableHttpCorrelationHeaders : True
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              :
BackendSetting               :
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/diagnostics/applicationinsights
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso
```

<span data-ttu-id="b5c43-116">Questo comando ottiene la `applicationinsights` diagnostica configurata in API `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="b5c43-116">This command gets the `applicationinsights` diagnostics configured in api `echo-api`.</span></span>

## <span data-ttu-id="b5c43-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b5c43-117">PARAMETERS</span></span>

### <span data-ttu-id="b5c43-118">-ApiId</span><span class="sxs-lookup"><span data-stu-id="b5c43-118">-ApiId</span></span>
<span data-ttu-id="b5c43-119">Identificatore dell'API esistente.</span><span class="sxs-lookup"><span data-stu-id="b5c43-119">Identifier of existing API.</span></span>
<span data-ttu-id="b5c43-120">Se specificato restituirà la diagnostica per l'ambito API.</span><span class="sxs-lookup"><span data-stu-id="b5c43-120">If specified will return API-scope diagnostic.</span></span>
<span data-ttu-id="b5c43-121">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="b5c43-121">This parameters is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5c43-122">-Contesto</span><span class="sxs-lookup"><span data-stu-id="b5c43-122">-Context</span></span>
<span data-ttu-id="b5c43-123">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b5c43-123">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b5c43-124">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="b5c43-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5c43-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5c43-125">-DefaultProfile</span></span>
<span data-ttu-id="b5c43-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b5c43-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5c43-127">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="b5c43-127">-DiagnosticId</span></span>
<span data-ttu-id="b5c43-128">Identificatore della diagnostica esistente.</span><span class="sxs-lookup"><span data-stu-id="b5c43-128">Identifier of existing diagnostic.</span></span>
<span data-ttu-id="b5c43-129">Se specificato restituirà criteri per l'ambito prodotto.</span><span class="sxs-lookup"><span data-stu-id="b5c43-129">If specified will return product-scope policy.</span></span>
<span data-ttu-id="b5c43-130">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b5c43-130">This parameters is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5c43-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5c43-131">-ResourceId</span></span>
<span data-ttu-id="b5c43-132">Identificatore delle risorse ARM di un sistema diagnostico o diagnostico API.</span><span class="sxs-lookup"><span data-stu-id="b5c43-132">Arm Resource Identifier of a Diagnostic or Api Diagnostic.</span></span> <span data-ttu-id="b5c43-133">Se specificato cercherà di trovare la diagnostica dall'identificatore.</span><span class="sxs-lookup"><span data-stu-id="b5c43-133">If specified will try to find diagnostic by the identifier.</span></span> <span data-ttu-id="b5c43-134">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="b5c43-134">This parameter is required.</span></span>

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

### <span data-ttu-id="b5c43-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5c43-135">CommonParameters</span></span>
<span data-ttu-id="b5c43-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5c43-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5c43-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b5c43-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5c43-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b5c43-138">INPUTS</span></span>

### <span data-ttu-id="b5c43-139">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b5c43-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b5c43-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b5c43-140">System.String</span></span>

## <span data-ttu-id="b5c43-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b5c43-141">OUTPUTS</span></span>

### <span data-ttu-id="b5c43-142">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="b5c43-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="b5c43-143">Note</span><span class="sxs-lookup"><span data-stu-id="b5c43-143">NOTES</span></span>

## <span data-ttu-id="b5c43-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b5c43-144">RELATED LINKS</span></span>
