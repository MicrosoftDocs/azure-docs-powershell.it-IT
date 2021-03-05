---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementDiagnostic.md
ms.openlocfilehash: a330aa6df0da0be08de925d59e72018a028e7d82
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988579"
---
# <span data-ttu-id="c424b-101">New-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="c424b-101">New-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="c424b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c424b-102">SYNOPSIS</span></span>
<span data-ttu-id="c424b-103">Crea una nuova diagnostica con ambito globale o ambito API.</span><span class="sxs-lookup"><span data-stu-id="c424b-103">Creates a new diagnostics at the Global scope or Api Scope.</span></span>

## <span data-ttu-id="c424b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c424b-104">SYNTAX</span></span>

```
New-AzApiManagementDiagnostic -Context <PsApiManagementContext> -LoggerId <String> [-DiagnosticId <String>]
 [-AlwaysLog <String>] [-ApiId <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c424b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c424b-105">DESCRIPTION</span></span>
<span data-ttu-id="c424b-106">Il cmdlet **New-AzApiManagementDiagnostic** crea un'entità di diagnostica nell'ambito globale o in un ambito API specifico.</span><span class="sxs-lookup"><span data-stu-id="c424b-106">The cmdlet **New-AzApiManagementDiagnostic** creates a diagnostic entity either at Global scope or specific Api scope.</span></span>

## <span data-ttu-id="c424b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c424b-107">EXAMPLES</span></span>

### <span data-ttu-id="c424b-108">Esempio 1: Creare un nuovo ambito globale - Diagnostica</span><span class="sxs-lookup"><span data-stu-id="c424b-108">Example 1: Create a new Global scope Diagnostic</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS D:\github\azure-powershell> $logger = Get-AzApiManagementLogger -Context $context -LoggerId "backendapisachinc"
PS D:\github\azure-powershell> $samplingsetting = New-AzApiManagementSamplingSetting -SamplingType fixed -SamplingPercentage 100
PS D:\github\azure-powershell> New-AzApiManagementDiagnostic -LoggerId $logger.LoggerId -Context $context -AlwaysLog allErrors -SamplingSetting $samplingSetting  -DiagnosticId "applicationinsights"

DiagnosticId                 : applicationinsights
ApiId                        :
AlwaysLog                    : allErrors
LoggerId                     : backendapisachinc
EnableHttpCorrelationHeaders : True
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              :
BackendSetting               :
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUs/providers/Microsoft.ApiManagement/service/contoso/diagnostics/applicationinsights
ResourceGroupName            : Api-Default-WestUs
ServiceName                  : contoso
```

<span data-ttu-id="c424b-109">Questo esempio crea un'entità di diagnostica nell'ambito globale.</span><span class="sxs-lookup"><span data-stu-id="c424b-109">This example create a diagnostic entity at the Global Scope.</span></span>

### <span data-ttu-id="c424b-110">Esempio 2: Creare una diagnostica con ambito Api</span><span class="sxs-lookup"><span data-stu-id="c424b-110">Example 2: Create a diagnostic at Api scope</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS D:\github\azure-powershell> $logger = Get-AzApiManagementLogger -Context $context -LoggerId azuremonitor
PS D:\github\azure-powershell> $samplingsetting = New-AzApiManagementSamplingSetting -SamplingType fixed -SamplingPercentage 100
PS D:\github\azure-powershell> $httpMessageDiagnostic = New-AzApiManagementHttpMessageDiagnostic -HeadersToLog 'Content-Type', 'User-Agent' -BodyBytesToLog 100
PS D:\github\azure-powershell> $pipelineDiagnostic = New-AzApiManagementPipelineDiagnosticSetting -Request $httpMessageDiagnostic -Response $httpMessageDiagnostic
PS D:\github\azure-powershell> New-AzApiManagementDiagnostic -LoggerId $logger.LoggerId -Context $context -ApiId httpbin -AlwaysLog allErrors -SamplingSetting $samplingsetting -FrontEndSetting $pipelineDiagnostic -BackendSetting $pipelineDiagnostic -DiagnosticId azuremonitor

DiagnosticId                 : azuremonitor
ApiId                        : httpbin
AlwaysLog                    : allErrors
LoggerId                     : azuremonitor
EnableHttpCorrelationHeaders :
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
BackendSetting               : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/httpbin/diagnostics/azuremonitor      
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso
```

<span data-ttu-id="c424b-111">Nell'esempio precedente viene creata una diagnostica per l'API per registrare l'intestazione e `httpbin` 100 byte del corpo `azuremonitor` da sempre.</span><span class="sxs-lookup"><span data-stu-id="c424b-111">The example above create a diagnostic for the API `httpbin` to log the Header and 100 Bytes of Body to `azuremonitor` logger.</span></span>

## <span data-ttu-id="c424b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c424b-112">PARAMETERS</span></span>

### <span data-ttu-id="c424b-113">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="c424b-113">-AlwaysLog</span></span>
<span data-ttu-id="c424b-114">Specifica il tipo di impostazioni di campionamento dei messaggi da non applicare.</span><span class="sxs-lookup"><span data-stu-id="c424b-114">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="c424b-115">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c424b-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="c424b-116">-ApiId</span><span class="sxs-lookup"><span data-stu-id="c424b-116">-ApiId</span></span>
<span data-ttu-id="c424b-117">Identificatore dell'API esistente.</span><span class="sxs-lookup"><span data-stu-id="c424b-117">Identifier of existing API.</span></span>
<span data-ttu-id="c424b-118">Se specificato, verrà impostato il criterio di ambito API.</span><span class="sxs-lookup"><span data-stu-id="c424b-118">If specified will set API-scope policy.</span></span>
<span data-ttu-id="c424b-119">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="c424b-119">This parameters is required.</span></span>

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

### <span data-ttu-id="c424b-120">-BackendSetting</span><span class="sxs-lookup"><span data-stu-id="c424b-120">-BackendSetting</span></span>
<span data-ttu-id="c424b-121">Impostazione diagnostica per i messaggi Http in arrivo/in uscita nel back-end.</span><span class="sxs-lookup"><span data-stu-id="c424b-121">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="c424b-122">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c424b-122">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c424b-123">-Context</span><span class="sxs-lookup"><span data-stu-id="c424b-123">-Context</span></span>
<span data-ttu-id="c424b-124">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c424b-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c424b-125">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="c424b-125">This parameter is required.</span></span>

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

### <span data-ttu-id="c424b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c424b-126">-DefaultProfile</span></span>
<span data-ttu-id="c424b-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c424b-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c424b-128">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="c424b-128">-DiagnosticId</span></span>
<span data-ttu-id="c424b-129">Identificatore dell'entità di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="c424b-129">Identifier of the diagnostics entity.</span></span>
<span data-ttu-id="c424b-130">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c424b-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="c424b-131">-FrontEndSetting</span><span class="sxs-lookup"><span data-stu-id="c424b-131">-FrontEndSetting</span></span>
<span data-ttu-id="c424b-132">Impostazione di diagnostica per i messaggi Http in arrivo/in uscita al gateway.</span><span class="sxs-lookup"><span data-stu-id="c424b-132">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="c424b-133">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c424b-133">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c424b-134">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="c424b-134">-LoggerId</span></span>
<span data-ttu-id="c424b-135">Identificatore del registro in cui eseguire il push della diagnostica.</span><span class="sxs-lookup"><span data-stu-id="c424b-135">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="c424b-136">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="c424b-136">This parameter is required.</span></span>

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

### <span data-ttu-id="c424b-137">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="c424b-137">-SamplingSetting</span></span>
<span data-ttu-id="c424b-138">Campionamento dell'impostazione della diagnostica.</span><span class="sxs-lookup"><span data-stu-id="c424b-138">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="c424b-139">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c424b-139">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c424b-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c424b-140">-Confirm</span></span>
<span data-ttu-id="c424b-141">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c424b-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c424b-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c424b-142">-WhatIf</span></span>
<span data-ttu-id="c424b-143">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c424b-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c424b-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c424b-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c424b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c424b-145">CommonParameters</span></span>
<span data-ttu-id="c424b-146">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c424b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c424b-147">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c424b-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c424b-148">INPUT</span><span class="sxs-lookup"><span data-stu-id="c424b-148">INPUTS</span></span>

### <span data-ttu-id="c424b-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c424b-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c424b-150">System.String</span><span class="sxs-lookup"><span data-stu-id="c424b-150">System.String</span></span>

### <span data-ttu-id="c424b-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="c424b-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="c424b-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="c424b-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="c424b-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c424b-153">OUTPUTS</span></span>

### <span data-ttu-id="c424b-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="c424b-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="c424b-155">NOTE</span><span class="sxs-lookup"><span data-stu-id="c424b-155">NOTES</span></span>

## <span data-ttu-id="c424b-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c424b-156">RELATED LINKS</span></span>

[<span data-ttu-id="c424b-157">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="c424b-157">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="c424b-158">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="c424b-158">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="c424b-159">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="c424b-159">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="c424b-160">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="c424b-160">New-AzApiManagementHttpMessageDiagnostic</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)

[<span data-ttu-id="c424b-161">New-AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="c424b-161">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)