---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementDiagnostic.md
ms.openlocfilehash: 2201a1ed8b09ae57f7595d22ee3565cb0d39483f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004989"
---
# <span data-ttu-id="01086-101">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="01086-101">Get-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="01086-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01086-102">SYNOPSIS</span></span>
<span data-ttu-id="01086-103">Ottenere i dettagli della diagnostica configurata a livello di servizio o a livello di API.</span><span class="sxs-lookup"><span data-stu-id="01086-103">Get details of the Diagnostic configured at the service level or the Api Level.</span></span> <span data-ttu-id="01086-104">La diagnostica viene usata per registrare le richieste/risposte da Gateway di gestione API.</span><span class="sxs-lookup"><span data-stu-id="01086-104">Diagnostics are used to log requests/responses from Api Management gateway.</span></span>

## <span data-ttu-id="01086-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="01086-105">SYNTAX</span></span>

### <span data-ttu-id="01086-106">ContextParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="01086-106">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementDiagnostic -Context <PsApiManagementContext> [-DiagnosticId <String>] [-ApiId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01086-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="01086-107">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementDiagnostic -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="01086-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="01086-108">DESCRIPTION</span></span>
<span data-ttu-id="01086-109">**Get-AzApiManagementDiagnostic** ottiene i dettagli della diagnostica configurata nel servizio di gestione api in un determinato ambito.</span><span class="sxs-lookup"><span data-stu-id="01086-109">The **Get-AzApiManagementDiagnostic** gets details of the diagnostics configured in the Api management service at a given scope.</span></span>

## <span data-ttu-id="01086-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="01086-110">EXAMPLES</span></span>

### <span data-ttu-id="01086-111">Esempio 1: Configurare tutta la diagnostica nell'ambito tenant.</span><span class="sxs-lookup"><span data-stu-id="01086-111">Example 1: Get all the diagnostic configured at the tenant scope.</span></span>
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

<span data-ttu-id="01086-112">Questo comando consente di ottenere tutte le funzionalità di diagnostica configurate nel servizio di gestione api.</span><span class="sxs-lookup"><span data-stu-id="01086-112">This command gets all the diagnostics configured in the Api Management service.</span></span>

### <span data-ttu-id="01086-113">Esempio 2: Configurare tutta la diagnostica con l'ambito API</span><span class="sxs-lookup"><span data-stu-id="01086-113">Example 2: Get all the diagnostics configured at the Api scope</span></span>
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

<span data-ttu-id="01086-114">Questo comando recupera tutta la diagnostica configurata con `echo-api` l'ambito Api</span><span class="sxs-lookup"><span data-stu-id="01086-114">This command gets all the diagnostics configured at the `echo-api` Api scope</span></span>

### <span data-ttu-id="01086-115">Esempio 3: Ottenere la diagnostica dell'ambito API specificata da un ID</span><span class="sxs-lookup"><span data-stu-id="01086-115">Example 3: Get the API-scope diagnostic specified by an Id</span></span>
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

<span data-ttu-id="01086-116">Questo comando consente di configurare `applicationinsights` la diagnostica nell'api. `echo-api`</span><span class="sxs-lookup"><span data-stu-id="01086-116">This command gets the `applicationinsights` diagnostics configured in api `echo-api`.</span></span>

## <span data-ttu-id="01086-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01086-117">PARAMETERS</span></span>

### <span data-ttu-id="01086-118">-ApiId</span><span class="sxs-lookup"><span data-stu-id="01086-118">-ApiId</span></span>
<span data-ttu-id="01086-119">Identificatore dell'API esistente.</span><span class="sxs-lookup"><span data-stu-id="01086-119">Identifier of existing API.</span></span>
<span data-ttu-id="01086-120">Se specificato restituirà la diagnostica dell'ambito API.</span><span class="sxs-lookup"><span data-stu-id="01086-120">If specified will return API-scope diagnostic.</span></span>
<span data-ttu-id="01086-121">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="01086-121">This parameters is required.</span></span>

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

### <span data-ttu-id="01086-122">-Context</span><span class="sxs-lookup"><span data-stu-id="01086-122">-Context</span></span>
<span data-ttu-id="01086-123">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="01086-123">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="01086-124">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="01086-124">This parameter is required.</span></span>

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

### <span data-ttu-id="01086-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01086-125">-DefaultProfile</span></span>
<span data-ttu-id="01086-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="01086-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01086-127">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="01086-127">-DiagnosticId</span></span>
<span data-ttu-id="01086-128">Identificatore della diagnostica esistente.</span><span class="sxs-lookup"><span data-stu-id="01086-128">Identifier of existing diagnostic.</span></span>
<span data-ttu-id="01086-129">Se specificato restituirà criteri di ambito del prodotto.</span><span class="sxs-lookup"><span data-stu-id="01086-129">If specified will return product-scope policy.</span></span>
<span data-ttu-id="01086-130">Questi parametri sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="01086-130">This parameters is optional.</span></span>

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

### <span data-ttu-id="01086-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="01086-131">-ResourceId</span></span>
<span data-ttu-id="01086-132">Arm Resource Identifier of a Diagnostic or Api Diagnostic.</span><span class="sxs-lookup"><span data-stu-id="01086-132">Arm Resource Identifier of a Diagnostic or Api Diagnostic.</span></span> <span data-ttu-id="01086-133">Se specificato, tenterà di trovare la diagnostica in base all'identificatore.</span><span class="sxs-lookup"><span data-stu-id="01086-133">If specified will try to find diagnostic by the identifier.</span></span> <span data-ttu-id="01086-134">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="01086-134">This parameter is required.</span></span>

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

### <span data-ttu-id="01086-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01086-135">CommonParameters</span></span>
<span data-ttu-id="01086-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01086-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01086-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="01086-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01086-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="01086-138">INPUTS</span></span>

### <span data-ttu-id="01086-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="01086-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="01086-140">System.String</span><span class="sxs-lookup"><span data-stu-id="01086-140">System.String</span></span>

## <span data-ttu-id="01086-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="01086-141">OUTPUTS</span></span>

### <span data-ttu-id="01086-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="01086-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="01086-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="01086-143">NOTES</span></span>

## <span data-ttu-id="01086-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="01086-144">RELATED LINKS</span></span>
