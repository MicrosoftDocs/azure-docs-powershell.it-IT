---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
ms.openlocfilehash: c646e7f39b5149803161bfc7b97ed64b5517dd9e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210307"
---
# <span data-ttu-id="9027d-101">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="9027d-101">Set-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="9027d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9027d-102">SYNOPSIS</span></span>
<span data-ttu-id="9027d-103">Modifica una diagnostica di gestione DELLE API nell'ambito Globale o API.</span><span class="sxs-lookup"><span data-stu-id="9027d-103">Modifies an API Management diagnostic at the Global or Api scope.</span></span>

## <span data-ttu-id="9027d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9027d-104">SYNTAX</span></span>

### <span data-ttu-id="9027d-105">ExpandedParameter (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9027d-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementDiagnostic -Context <PsApiManagementContext> -DiagnosticId <String> [-ApiId <String>]
 [-LoggerId <String>] [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9027d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9027d-106">ByInputObject</span></span>
```
Set-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-LoggerId <String>]
 [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9027d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9027d-107">ByResourceId</span></span>
```
Set-AzApiManagementDiagnostic -ResourceId <String> [-LoggerId <String>] [-AlwaysLog <String>]
 [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9027d-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9027d-108">DESCRIPTION</span></span>
<span data-ttu-id="9027d-109">Il cmdlet **Set-AzApiManagementDiagnostic** aggiorna la diagnostica configurata in base all'ambito globale o api.</span><span class="sxs-lookup"><span data-stu-id="9027d-109">The cmdlet **Set-AzApiManagementDiagnostic** updates the diagnostics which is configured at the Global or Api Scope.</span></span>

## <span data-ttu-id="9027d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9027d-110">EXAMPLES</span></span>

### <span data-ttu-id="9027d-111">Esempio 1: Modificare una diagnostica nell'ambito globale</span><span class="sxs-lookup"><span data-stu-id="9027d-111">Example 1: Modify a diagnostic at the Global scope</span></span>
```powershell
PS c:\> $context =New-AzApiManagementContext -ResourceGroupName Api-Default-WestUS -ServiceName contoso
PS c:\> $diagnostic=Get-AzApiManagementDiagnostic -Context $context -DiagnosticId "applicationinsights"
PS c:\> $diagnostic

DiagnosticId      : applicationinsights
AlwaysLog         : allErrors
LoggerId          : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/loggers/backendapisachinc
Sampling          : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
Frontend          :
Backend           :
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/diagnostics/applicationinsights
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso


PS c:\> $diagnostic.Sampling

SamplingType Percentage
------------ ----------
fixed               100

PS c:\> $diagnostic.Sampling.Percentage = 50
PS c:\> $diagnostic.Sampling

SamplingType Percentage
------------ ----------
fixed                50

PS c:\> Set-AzApiManagementDiagnostic -InputObject $diagnostic
```

<span data-ttu-id="9027d-112">Questo comando modifica la percentuale di campionamento diagnostica specificata dal 100 al 50%</span><span class="sxs-lookup"><span data-stu-id="9027d-112">This command modifies the specified diagnostic Sampling Percentage from 100 to 50%</span></span>

### <span data-ttu-id="9027d-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9027d-113">Example 2</span></span>

<span data-ttu-id="9027d-114">Modifica una diagnostica di gestione DELLE API nell'ambito Globale o API.</span><span class="sxs-lookup"><span data-stu-id="9027d-114">Modifies an API Management diagnostic at the Global or Api scope.</span></span> <span data-ttu-id="9027d-115">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="9027d-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzApiManagementDiagnostic -AlwaysLog allErrors -ApiId '0001' -Context <PsApiManagementContext> -DiagnosticId 'applicationinsights' -LoggerId 'Logger123' -SamplingSetting <PsApiManagementSamplingSetting>
```

## <span data-ttu-id="9027d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9027d-116">PARAMETERS</span></span>

### <span data-ttu-id="9027d-117">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="9027d-117">-AlwaysLog</span></span>
<span data-ttu-id="9027d-118">Specifica il tipo di impostazioni di campionamento dei messaggi da non applicare.</span><span class="sxs-lookup"><span data-stu-id="9027d-118">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="9027d-119">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="9027d-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="9027d-120">-ApiId</span><span class="sxs-lookup"><span data-stu-id="9027d-120">-ApiId</span></span>
<span data-ttu-id="9027d-121">Identificatore dell'API esistente.</span><span class="sxs-lookup"><span data-stu-id="9027d-121">Identifier of existing API.</span></span>
<span data-ttu-id="9027d-122">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="9027d-122">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9027d-123">-BackendSetting</span><span class="sxs-lookup"><span data-stu-id="9027d-123">-BackendSetting</span></span>
<span data-ttu-id="9027d-124">Impostazione diagnostica per i messaggi Http in arrivo/in uscita nel back-end.</span><span class="sxs-lookup"><span data-stu-id="9027d-124">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="9027d-125">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="9027d-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="9027d-126">-Context</span><span class="sxs-lookup"><span data-stu-id="9027d-126">-Context</span></span>
<span data-ttu-id="9027d-127">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="9027d-127">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="9027d-128">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="9027d-128">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9027d-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9027d-129">-DefaultProfile</span></span>
<span data-ttu-id="9027d-130">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9027d-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9027d-131">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="9027d-131">-DiagnosticId</span></span>
<span data-ttu-id="9027d-132">Identificatore della diagnostica esistente.</span><span class="sxs-lookup"><span data-stu-id="9027d-132">Identifier of existing Diagnostic.</span></span>
<span data-ttu-id="9027d-133">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="9027d-133">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9027d-134">-FrontEndSetting</span><span class="sxs-lookup"><span data-stu-id="9027d-134">-FrontEndSetting</span></span>
<span data-ttu-id="9027d-135">Impostazione diagnostica per i messaggi Http in ingresso/in uscita al gateway.</span><span class="sxs-lookup"><span data-stu-id="9027d-135">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="9027d-136">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="9027d-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="9027d-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9027d-137">-InputObject</span></span>
<span data-ttu-id="9027d-138">Istanza di PsApiManagementDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="9027d-138">Instance of PsApiManagementDiagnostic.</span></span>
<span data-ttu-id="9027d-139">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="9027d-139">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9027d-140">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="9027d-140">-LoggerId</span></span>
<span data-ttu-id="9027d-141">Identificatore del registro in cui eseguire il push della diagnostica.</span><span class="sxs-lookup"><span data-stu-id="9027d-141">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="9027d-142">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="9027d-142">This parameter is required.</span></span>

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

### <span data-ttu-id="9027d-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9027d-143">-PassThru</span></span>
<span data-ttu-id="9027d-144">Se si specifica l'istanza di Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic che rappresenta l'insieme Diagnostic.</span><span class="sxs-lookup"><span data-stu-id="9027d-144">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic type representing the set Diagnostic.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9027d-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9027d-145">-ResourceId</span></span>
<span data-ttu-id="9027d-146">Arm ResourceId of Diagnostic or Api Diagnostic.</span><span class="sxs-lookup"><span data-stu-id="9027d-146">Arm ResourceId of Diagnostic or Api Diagnostic.</span></span> <span data-ttu-id="9027d-147">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="9027d-147">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9027d-148">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="9027d-148">-SamplingSetting</span></span>
<span data-ttu-id="9027d-149">Campionamento dell'impostazione della diagnostica.</span><span class="sxs-lookup"><span data-stu-id="9027d-149">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="9027d-150">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="9027d-150">This parameter is optional.</span></span>

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

### <span data-ttu-id="9027d-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9027d-151">-Confirm</span></span>
<span data-ttu-id="9027d-152">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9027d-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9027d-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9027d-153">-WhatIf</span></span>
<span data-ttu-id="9027d-154">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9027d-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9027d-155">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9027d-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9027d-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9027d-156">CommonParameters</span></span>
<span data-ttu-id="9027d-157">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9027d-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9027d-158">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9027d-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9027d-159">INPUT</span><span class="sxs-lookup"><span data-stu-id="9027d-159">INPUTS</span></span>

### <span data-ttu-id="9027d-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9027d-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9027d-161">System.String</span><span class="sxs-lookup"><span data-stu-id="9027d-161">System.String</span></span>

### <span data-ttu-id="9027d-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="9027d-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

### <span data-ttu-id="9027d-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="9027d-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="9027d-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="9027d-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

### <span data-ttu-id="9027d-165">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9027d-165">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9027d-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9027d-166">OUTPUTS</span></span>

### <span data-ttu-id="9027d-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="9027d-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="9027d-168">NOTE</span><span class="sxs-lookup"><span data-stu-id="9027d-168">NOTES</span></span>

## <span data-ttu-id="9027d-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9027d-169">RELATED LINKS</span></span>
