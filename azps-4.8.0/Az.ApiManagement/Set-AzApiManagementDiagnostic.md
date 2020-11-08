---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
ms.openlocfilehash: c646e7f39b5149803161bfc7b97ed64b5517dd9e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031997"
---
# <span data-ttu-id="8ed54-101">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8ed54-101">Set-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="8ed54-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8ed54-102">SYNOPSIS</span></span>
<span data-ttu-id="8ed54-103">Modifica un sistema diagnostico di gestione delle API nell'ambito globale o delle API.</span><span class="sxs-lookup"><span data-stu-id="8ed54-103">Modifies an API Management diagnostic at the Global or Api scope.</span></span>

## <span data-ttu-id="8ed54-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8ed54-104">SYNTAX</span></span>

### <span data-ttu-id="8ed54-105">ExpandedParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8ed54-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementDiagnostic -Context <PsApiManagementContext> -DiagnosticId <String> [-ApiId <String>]
 [-LoggerId <String>] [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ed54-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8ed54-106">ByInputObject</span></span>
```
Set-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-LoggerId <String>]
 [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ed54-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8ed54-107">ByResourceId</span></span>
```
Set-AzApiManagementDiagnostic -ResourceId <String> [-LoggerId <String>] [-AlwaysLog <String>]
 [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ed54-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8ed54-108">DESCRIPTION</span></span>
<span data-ttu-id="8ed54-109">Il cmdlet **set-AzApiManagementDiagnostic** aggiorna la diagnostica configurata nell'ambito globale o delle API.</span><span class="sxs-lookup"><span data-stu-id="8ed54-109">The cmdlet **Set-AzApiManagementDiagnostic** updates the diagnostics which is configured at the Global or Api Scope.</span></span>

## <span data-ttu-id="8ed54-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8ed54-110">EXAMPLES</span></span>

### <span data-ttu-id="8ed54-111">Esempio 1: modificare una diagnostica nell'ambito globale</span><span class="sxs-lookup"><span data-stu-id="8ed54-111">Example 1: Modify a diagnostic at the Global scope</span></span>
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

<span data-ttu-id="8ed54-112">Questo comando modifica la percentuale di campionamento diagnostico specificata da 100 a 50%</span><span class="sxs-lookup"><span data-stu-id="8ed54-112">This command modifies the specified diagnostic Sampling Percentage from 100 to 50%</span></span>

### <span data-ttu-id="8ed54-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="8ed54-113">Example 2</span></span>

<span data-ttu-id="8ed54-114">Modifica un sistema diagnostico di gestione delle API nell'ambito globale o delle API.</span><span class="sxs-lookup"><span data-stu-id="8ed54-114">Modifies an API Management diagnostic at the Global or Api scope.</span></span> <span data-ttu-id="8ed54-115">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="8ed54-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzApiManagementDiagnostic -AlwaysLog allErrors -ApiId '0001' -Context <PsApiManagementContext> -DiagnosticId 'applicationinsights' -LoggerId 'Logger123' -SamplingSetting <PsApiManagementSamplingSetting>
```

## <span data-ttu-id="8ed54-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8ed54-116">PARAMETERS</span></span>

### <span data-ttu-id="8ed54-117">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="8ed54-117">-AlwaysLog</span></span>
<span data-ttu-id="8ed54-118">Specifica il tipo di messaggio che non deve essere applicato alle impostazioni di campionamento.</span><span class="sxs-lookup"><span data-stu-id="8ed54-118">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="8ed54-119">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="8ed54-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="8ed54-120">-ApiId</span><span class="sxs-lookup"><span data-stu-id="8ed54-120">-ApiId</span></span>
<span data-ttu-id="8ed54-121">Identificatore dell'API esistente.</span><span class="sxs-lookup"><span data-stu-id="8ed54-121">Identifier of existing API.</span></span>
<span data-ttu-id="8ed54-122">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="8ed54-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="8ed54-123">-BackendSetting</span><span class="sxs-lookup"><span data-stu-id="8ed54-123">-BackendSetting</span></span>
<span data-ttu-id="8ed54-124">Impostazione di diagnostica per i messaggi HTTP in arrivo/in uscita nel backend.</span><span class="sxs-lookup"><span data-stu-id="8ed54-124">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="8ed54-125">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="8ed54-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="8ed54-126">-Contesto</span><span class="sxs-lookup"><span data-stu-id="8ed54-126">-Context</span></span>
<span data-ttu-id="8ed54-127">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="8ed54-127">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="8ed54-128">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="8ed54-128">This parameter is required.</span></span>

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

### <span data-ttu-id="8ed54-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ed54-129">-DefaultProfile</span></span>
<span data-ttu-id="8ed54-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8ed54-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ed54-131">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="8ed54-131">-DiagnosticId</span></span>
<span data-ttu-id="8ed54-132">Identificatore della diagnostica esistente.</span><span class="sxs-lookup"><span data-stu-id="8ed54-132">Identifier of existing Diagnostic.</span></span>
<span data-ttu-id="8ed54-133">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="8ed54-133">This parameter is required.</span></span>

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

### <span data-ttu-id="8ed54-134">-FrontEndSetting</span><span class="sxs-lookup"><span data-stu-id="8ed54-134">-FrontEndSetting</span></span>
<span data-ttu-id="8ed54-135">Impostazione di diagnostica per i messaggi HTTP in arrivo/in uscita nel gateway.</span><span class="sxs-lookup"><span data-stu-id="8ed54-135">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="8ed54-136">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="8ed54-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="8ed54-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ed54-137">-InputObject</span></span>
<span data-ttu-id="8ed54-138">Istanza di PsApiManagementDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="8ed54-138">Instance of PsApiManagementDiagnostic.</span></span>
<span data-ttu-id="8ed54-139">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="8ed54-139">This parameter is required.</span></span>

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

### <span data-ttu-id="8ed54-140">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="8ed54-140">-LoggerId</span></span>
<span data-ttu-id="8ed54-141">Identificatore del logger in cui spingere la diagnostica.</span><span class="sxs-lookup"><span data-stu-id="8ed54-141">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="8ed54-142">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="8ed54-142">This parameter is required.</span></span>

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

### <span data-ttu-id="8ed54-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8ed54-143">-PassThru</span></span>
<span data-ttu-id="8ed54-144">Se specificato, quindi istanza del tipo Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementDiagnostic che rappresenta la diagnostica set.</span><span class="sxs-lookup"><span data-stu-id="8ed54-144">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic type representing the set Diagnostic.</span></span>

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

### <span data-ttu-id="8ed54-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ed54-145">-ResourceId</span></span>
<span data-ttu-id="8ed54-146">ARM ResourceId di diagnostica o API Diagnostic.</span><span class="sxs-lookup"><span data-stu-id="8ed54-146">Arm ResourceId of Diagnostic or Api Diagnostic.</span></span> <span data-ttu-id="8ed54-147">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="8ed54-147">This parameter is required.</span></span>

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

### <span data-ttu-id="8ed54-148">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="8ed54-148">-SamplingSetting</span></span>
<span data-ttu-id="8ed54-149">Impostazione di campionamento della diagnostica.</span><span class="sxs-lookup"><span data-stu-id="8ed54-149">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="8ed54-150">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="8ed54-150">This parameter is optional.</span></span>

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

### <span data-ttu-id="8ed54-151">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8ed54-151">-Confirm</span></span>
<span data-ttu-id="8ed54-152">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ed54-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ed54-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ed54-153">-WhatIf</span></span>
<span data-ttu-id="8ed54-154">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8ed54-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8ed54-155">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8ed54-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ed54-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ed54-156">CommonParameters</span></span>
<span data-ttu-id="8ed54-157">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ed54-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ed54-158">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8ed54-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ed54-159">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8ed54-159">INPUTS</span></span>

### <span data-ttu-id="8ed54-160">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8ed54-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8ed54-161">System. String</span><span class="sxs-lookup"><span data-stu-id="8ed54-161">System.String</span></span>

### <span data-ttu-id="8ed54-162">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8ed54-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

### <span data-ttu-id="8ed54-163">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="8ed54-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="8ed54-164">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="8ed54-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

### <span data-ttu-id="8ed54-165">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8ed54-165">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8ed54-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8ed54-166">OUTPUTS</span></span>

### <span data-ttu-id="8ed54-167">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8ed54-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="8ed54-168">Note</span><span class="sxs-lookup"><span data-stu-id="8ed54-168">NOTES</span></span>

## <span data-ttu-id="8ed54-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8ed54-169">RELATED LINKS</span></span>
