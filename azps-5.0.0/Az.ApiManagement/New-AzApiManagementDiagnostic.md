---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementDiagnostic.md
ms.openlocfilehash: f977b4dab003b3d1a1b83f1b81701a6089e1cefa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201339"
---
# <span data-ttu-id="d93bb-101">New-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d93bb-101">New-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="d93bb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d93bb-102">SYNOPSIS</span></span>
<span data-ttu-id="d93bb-103">Crea una nuova diagnostica nell'ambito globale o dell'ambito API.</span><span class="sxs-lookup"><span data-stu-id="d93bb-103">Creates a new diagnostics at the Global scope or Api Scope.</span></span>

## <span data-ttu-id="d93bb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d93bb-104">SYNTAX</span></span>

```
New-AzApiManagementDiagnostic -Context <PsApiManagementContext> -LoggerId <String> [-DiagnosticId <String>]
 [-AlwaysLog <String>] [-ApiId <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d93bb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d93bb-105">DESCRIPTION</span></span>
<span data-ttu-id="d93bb-106">Il cmdlet **New-AzApiManagementDiagnostic** crea un'entità di diagnostica in ambito globale o specifico.</span><span class="sxs-lookup"><span data-stu-id="d93bb-106">The cmdlet **New-AzApiManagementDiagnostic** creates a diagnostic entity either at Global scope or specific Api scope.</span></span>

## <span data-ttu-id="d93bb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d93bb-107">EXAMPLES</span></span>

### <span data-ttu-id="d93bb-108">Esempio 1: creare una nuova diagnostica di ambito globale</span><span class="sxs-lookup"><span data-stu-id="d93bb-108">Example 1: Create a new Global scope Diagnostic</span></span>
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

<span data-ttu-id="d93bb-109">Questo esempio crea un'entità di diagnostica nell'ambito globale.</span><span class="sxs-lookup"><span data-stu-id="d93bb-109">This example create a diagnostic entity at the Global Scope.</span></span>

### <span data-ttu-id="d93bb-110">Esempio 2: creare un ambito di diagnostica all'API</span><span class="sxs-lookup"><span data-stu-id="d93bb-110">Example 2: Create a diagnostic at Api scope</span></span>
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

<span data-ttu-id="d93bb-111">L'esempio precedente crea un sistema di diagnostica per l'API per `httpbin` registrare l'intestazione e i byte di 100 del corpo in `azuremonitor` logger.</span><span class="sxs-lookup"><span data-stu-id="d93bb-111">The example above create a diagnostic for the API `httpbin` to log the Header and 100 Bytes of Body to `azuremonitor` logger.</span></span>

## <span data-ttu-id="d93bb-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d93bb-112">PARAMETERS</span></span>

### <span data-ttu-id="d93bb-113">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="d93bb-113">-AlwaysLog</span></span>
<span data-ttu-id="d93bb-114">Specifica il tipo di messaggio che non deve essere applicato alle impostazioni di campionamento.</span><span class="sxs-lookup"><span data-stu-id="d93bb-114">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="d93bb-115">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d93bb-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="d93bb-116">-ApiId</span><span class="sxs-lookup"><span data-stu-id="d93bb-116">-ApiId</span></span>
<span data-ttu-id="d93bb-117">Identificatore dell'API esistente.</span><span class="sxs-lookup"><span data-stu-id="d93bb-117">Identifier of existing API.</span></span>
<span data-ttu-id="d93bb-118">Se specificato imposterà criteri per l'ambito API.</span><span class="sxs-lookup"><span data-stu-id="d93bb-118">If specified will set API-scope policy.</span></span>
<span data-ttu-id="d93bb-119">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="d93bb-119">This parameters is required.</span></span>

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

### <span data-ttu-id="d93bb-120">-BackendSetting</span><span class="sxs-lookup"><span data-stu-id="d93bb-120">-BackendSetting</span></span>
<span data-ttu-id="d93bb-121">Impostazione di diagnostica per i messaggi HTTP in arrivo/in uscita nel backend.</span><span class="sxs-lookup"><span data-stu-id="d93bb-121">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="d93bb-122">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d93bb-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="d93bb-123">-Contesto</span><span class="sxs-lookup"><span data-stu-id="d93bb-123">-Context</span></span>
<span data-ttu-id="d93bb-124">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d93bb-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d93bb-125">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="d93bb-125">This parameter is required.</span></span>

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

### <span data-ttu-id="d93bb-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d93bb-126">-DefaultProfile</span></span>
<span data-ttu-id="d93bb-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d93bb-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d93bb-128">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="d93bb-128">-DiagnosticId</span></span>
<span data-ttu-id="d93bb-129">Identificatore dell'entità di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="d93bb-129">Identifier of the diagnostics entity.</span></span>
<span data-ttu-id="d93bb-130">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d93bb-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="d93bb-131">-FrontEndSetting</span><span class="sxs-lookup"><span data-stu-id="d93bb-131">-FrontEndSetting</span></span>
<span data-ttu-id="d93bb-132">Impostazione di diagnostica per i messaggi HTTP in arrivo/in uscita nel gateway.</span><span class="sxs-lookup"><span data-stu-id="d93bb-132">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="d93bb-133">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d93bb-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="d93bb-134">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="d93bb-134">-LoggerId</span></span>
<span data-ttu-id="d93bb-135">Identificatore del logger in cui spingere la diagnostica.</span><span class="sxs-lookup"><span data-stu-id="d93bb-135">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="d93bb-136">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="d93bb-136">This parameter is required.</span></span>

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

### <span data-ttu-id="d93bb-137">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="d93bb-137">-SamplingSetting</span></span>
<span data-ttu-id="d93bb-138">Impostazione di campionamento della diagnostica.</span><span class="sxs-lookup"><span data-stu-id="d93bb-138">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="d93bb-139">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d93bb-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="d93bb-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d93bb-140">-Confirm</span></span>
<span data-ttu-id="d93bb-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d93bb-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d93bb-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d93bb-142">-WhatIf</span></span>
<span data-ttu-id="d93bb-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d93bb-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d93bb-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d93bb-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d93bb-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d93bb-145">CommonParameters</span></span>
<span data-ttu-id="d93bb-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d93bb-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d93bb-147">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d93bb-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d93bb-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d93bb-148">INPUTS</span></span>

### <span data-ttu-id="d93bb-149">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d93bb-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d93bb-150">System. String</span><span class="sxs-lookup"><span data-stu-id="d93bb-150">System.String</span></span>

### <span data-ttu-id="d93bb-151">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="d93bb-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="d93bb-152">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="d93bb-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="d93bb-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d93bb-153">OUTPUTS</span></span>

### <span data-ttu-id="d93bb-154">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d93bb-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="d93bb-155">Note</span><span class="sxs-lookup"><span data-stu-id="d93bb-155">NOTES</span></span>

## <span data-ttu-id="d93bb-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d93bb-156">RELATED LINKS</span></span>

[<span data-ttu-id="d93bb-157">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d93bb-157">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="d93bb-158">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d93bb-158">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="d93bb-159">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d93bb-159">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="d93bb-160">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d93bb-160">New-AzApiManagementHttpMessageDiagnostic</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)

[<span data-ttu-id="d93bb-161">New-AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="d93bb-161">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)