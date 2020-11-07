---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
ms.openlocfilehash: 44a19d16cb5328f185370dcc407182a20a77bcfc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675899"
---
# <span data-ttu-id="e254c-101">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="e254c-101">Set-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="e254c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e254c-102">SYNOPSIS</span></span>
<span data-ttu-id="e254c-103">Modifica un sistema diagnostico di gestione delle API nell'ambito globale o delle API.</span><span class="sxs-lookup"><span data-stu-id="e254c-103">Modifies an API Management diagnostic at the Global or Api scope.</span></span>

## <span data-ttu-id="e254c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e254c-104">SYNTAX</span></span>

### <span data-ttu-id="e254c-105">ExpandedParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e254c-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementDiagnostic -Context <PsApiManagementContext> -DiagnosticId <String> [-ApiId <String>]
 [-LoggerId <String>] [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e254c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e254c-106">ByInputObject</span></span>
```
Set-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-LoggerId <String>]
 [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e254c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e254c-107">ByResourceId</span></span>
```
Set-AzApiManagementDiagnostic -ResourceId <String> [-LoggerId <String>] [-AlwaysLog <String>]
 [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e254c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e254c-108">DESCRIPTION</span></span>
<span data-ttu-id="e254c-109">Il cmdlet **set-AzApiManagementDiagnostic** aggiorna la diagnostica configurata nell'ambito globale o delle API.</span><span class="sxs-lookup"><span data-stu-id="e254c-109">The cmdlet **Set-AzApiManagementDiagnostic** updates the diagnostics which is configured at the Global or Api Scope.</span></span>

## <span data-ttu-id="e254c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e254c-110">EXAMPLES</span></span>

### <span data-ttu-id="e254c-111">Esempio 1: modificare una diagnostica nell'ambito globale</span><span class="sxs-lookup"><span data-stu-id="e254c-111">Example 1: Modify a diagnostic at the Global scope</span></span>
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

<span data-ttu-id="e254c-112">Questo comando modifica la percentuale di campionamento diagnostico specificata da 100 a 50%</span><span class="sxs-lookup"><span data-stu-id="e254c-112">This command modifies the specified diagnostic Sampling Percentage from 100 to 50%</span></span>

## <span data-ttu-id="e254c-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e254c-113">PARAMETERS</span></span>

### <span data-ttu-id="e254c-114">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="e254c-114">-AlwaysLog</span></span>
<span data-ttu-id="e254c-115">Specifica il tipo di messaggio che non deve essere applicato alle impostazioni di campionamento.</span><span class="sxs-lookup"><span data-stu-id="e254c-115">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="e254c-116">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e254c-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="e254c-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="e254c-117">-ApiId</span></span>
<span data-ttu-id="e254c-118">Identificatore dell'API esistente.</span><span class="sxs-lookup"><span data-stu-id="e254c-118">Identifier of existing API.</span></span>
<span data-ttu-id="e254c-119">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e254c-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="e254c-120">-BackendSetting</span><span class="sxs-lookup"><span data-stu-id="e254c-120">-BackendSetting</span></span>
<span data-ttu-id="e254c-121">Impostazione di diagnostica per i messaggi HTTP in arrivo/in uscita nel backend.</span><span class="sxs-lookup"><span data-stu-id="e254c-121">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="e254c-122">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e254c-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="e254c-123">-Contesto</span><span class="sxs-lookup"><span data-stu-id="e254c-123">-Context</span></span>
<span data-ttu-id="e254c-124">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="e254c-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e254c-125">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="e254c-125">This parameter is required.</span></span>

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

### <span data-ttu-id="e254c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e254c-126">-DefaultProfile</span></span>
<span data-ttu-id="e254c-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e254c-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e254c-128">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="e254c-128">-DiagnosticId</span></span>
<span data-ttu-id="e254c-129">Identificatore della diagnostica esistente.</span><span class="sxs-lookup"><span data-stu-id="e254c-129">Identifier of existing Diagnostic.</span></span>
<span data-ttu-id="e254c-130">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="e254c-130">This parameter is required.</span></span>

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

### <span data-ttu-id="e254c-131">-FrontEndSetting</span><span class="sxs-lookup"><span data-stu-id="e254c-131">-FrontEndSetting</span></span>
<span data-ttu-id="e254c-132">Impostazione di diagnostica per i messaggi HTTP in arrivo/in uscita nel gateway.</span><span class="sxs-lookup"><span data-stu-id="e254c-132">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="e254c-133">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e254c-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="e254c-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e254c-134">-InputObject</span></span>
<span data-ttu-id="e254c-135">Istanza di PsApiManagementDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="e254c-135">Instance of PsApiManagementDiagnostic.</span></span>
<span data-ttu-id="e254c-136">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="e254c-136">This parameter is required.</span></span>

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

### <span data-ttu-id="e254c-137">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="e254c-137">-LoggerId</span></span>
<span data-ttu-id="e254c-138">Identificatore del logger in cui spingere la diagnostica.</span><span class="sxs-lookup"><span data-stu-id="e254c-138">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="e254c-139">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="e254c-139">This parameter is required.</span></span>

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

### <span data-ttu-id="e254c-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e254c-140">-PassThru</span></span>
<span data-ttu-id="e254c-141">Se specificato, quindi istanza del tipo Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementDiagnostic che rappresenta la diagnostica set.</span><span class="sxs-lookup"><span data-stu-id="e254c-141">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic type representing the set Diagnostic.</span></span>

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

### <span data-ttu-id="e254c-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e254c-142">-ResourceId</span></span>
<span data-ttu-id="e254c-143">ARM ResourceId di diagnostica o API Diagnostic.</span><span class="sxs-lookup"><span data-stu-id="e254c-143">Arm ResourceId of Diagnostic or Api Diagnostic.</span></span> <span data-ttu-id="e254c-144">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="e254c-144">This parameter is required.</span></span>

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

### <span data-ttu-id="e254c-145">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="e254c-145">-SamplingSetting</span></span>
<span data-ttu-id="e254c-146">Impostazione di campionamento della diagnostica.</span><span class="sxs-lookup"><span data-stu-id="e254c-146">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="e254c-147">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e254c-147">This parameter is optional.</span></span>

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

### <span data-ttu-id="e254c-148">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e254c-148">-Confirm</span></span>
<span data-ttu-id="e254c-149">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e254c-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e254c-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e254c-150">-WhatIf</span></span>
<span data-ttu-id="e254c-151">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e254c-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e254c-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e254c-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e254c-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e254c-153">CommonParameters</span></span>
<span data-ttu-id="e254c-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e254c-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e254c-155">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e254c-155">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e254c-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e254c-156">INPUTS</span></span>

### <span data-ttu-id="e254c-157">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e254c-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e254c-158">System. String</span><span class="sxs-lookup"><span data-stu-id="e254c-158">System.String</span></span>

### <span data-ttu-id="e254c-159">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="e254c-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

### <span data-ttu-id="e254c-160">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="e254c-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="e254c-161">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="e254c-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

### <span data-ttu-id="e254c-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e254c-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e254c-163">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e254c-163">OUTPUTS</span></span>

### <span data-ttu-id="e254c-164">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="e254c-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="e254c-165">Note</span><span class="sxs-lookup"><span data-stu-id="e254c-165">NOTES</span></span>

## <span data-ttu-id="e254c-166">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e254c-166">RELATED LINKS</span></span>
