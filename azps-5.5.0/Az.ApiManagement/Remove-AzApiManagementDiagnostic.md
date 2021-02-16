---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementDiagnostic.md
ms.openlocfilehash: 488f4082007c96a111483d7efac6a8b9a74dba8f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178054"
---
# <span data-ttu-id="ffd7a-101">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="ffd7a-101">Remove-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="ffd7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffd7a-102">SYNOPSIS</span></span>
<span data-ttu-id="ffd7a-103">Rimuovere l'entità di diagnostica dall'ambito a livello di API o globale.</span><span class="sxs-lookup"><span data-stu-id="ffd7a-103">Remove the Diagnostic entity from Global or API level scope.</span></span>

## <span data-ttu-id="ffd7a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ffd7a-104">SYNTAX</span></span>

### <span data-ttu-id="ffd7a-105">ByResourceIdParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="ffd7a-105">ByResourceIdParameterSet (Default)</span></span>
```
Remove-AzApiManagementDiagnostic -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffd7a-106">ExpandParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ffd7a-106">ExpandParameterSetName</span></span>
```
Remove-AzApiManagementDiagnostic -Context <PsApiManagementContext> [-ApiId <String>] -DiagnosticId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffd7a-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ffd7a-107">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffd7a-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ffd7a-108">DESCRIPTION</span></span>
<span data-ttu-id="ffd7a-109">Il cmdlet **Remove-AzApiManagementDiagnostic** rimuove l'entità di diagnostica specificata dall'ambito globale `DiagnosticId` o da un `ApiId` ambito</span><span class="sxs-lookup"><span data-stu-id="ffd7a-109">The cmdlet **Remove-AzApiManagementDiagnostic** removes the diagnostic entity specified by `DiagnosticId` from global scope or an `ApiId` scope</span></span>

## <span data-ttu-id="ffd7a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ffd7a-110">EXAMPLES</span></span>

### <span data-ttu-id="ffd7a-111">Esempio 1: Rimuovere l'entità di diagnostica</span><span class="sxs-lookup"><span data-stu-id="ffd7a-111">Example 1: Remove the Diagnostic entity</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementDiagnostic -Context $apimContext -DiagnosticId "applicationinsights"
```

<span data-ttu-id="ffd7a-112">Questo esempio rimuove la diagnostica `applicationinsights` dal servizio di gestione api.</span><span class="sxs-lookup"><span data-stu-id="ffd7a-112">This example remove the diagnostic `applicationinsights` from the Api Management service.</span></span>

## <span data-ttu-id="ffd7a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ffd7a-113">PARAMETERS</span></span>

### <span data-ttu-id="ffd7a-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="ffd7a-114">-ApiId</span></span>
<span data-ttu-id="ffd7a-115">Identificatore dell'API.</span><span class="sxs-lookup"><span data-stu-id="ffd7a-115">Identifier of the API.</span></span>
<span data-ttu-id="ffd7a-116">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="ffd7a-116">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffd7a-117">-Context</span><span class="sxs-lookup"><span data-stu-id="ffd7a-117">-Context</span></span>
<span data-ttu-id="ffd7a-118">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="ffd7a-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ffd7a-119">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="ffd7a-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ffd7a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffd7a-120">-DefaultProfile</span></span>
<span data-ttu-id="ffd7a-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ffd7a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffd7a-122">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="ffd7a-122">-DiagnosticId</span></span>
<span data-ttu-id="ffd7a-123">Identificatore del prodotto esistente.</span><span class="sxs-lookup"><span data-stu-id="ffd7a-123">Identifier of existing product.</span></span>
<span data-ttu-id="ffd7a-124">Se specificato restituirà criteri di ambito del prodotto.</span><span class="sxs-lookup"><span data-stu-id="ffd7a-124">If specified will return product-scope policy.</span></span>
<span data-ttu-id="ffd7a-125">Questi parametri sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="ffd7a-125">This parameters is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffd7a-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ffd7a-126">-InputObject</span></span>
<span data-ttu-id="ffd7a-127">Istanza di PsApiManagementDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="ffd7a-127">Instance of PsApiManagementDiagnostic.</span></span> <span data-ttu-id="ffd7a-128">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="ffd7a-128">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ffd7a-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ffd7a-129">-PassThru</span></span>
<span data-ttu-id="ffd7a-130">Se specificato, write true se l'operazione riesce.</span><span class="sxs-lookup"><span data-stu-id="ffd7a-130">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="ffd7a-131">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="ffd7a-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="ffd7a-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ffd7a-132">-ResourceId</span></span>
<span data-ttu-id="ffd7a-133">Arm ResourceId of Diagnostic.</span><span class="sxs-lookup"><span data-stu-id="ffd7a-133">Arm ResourceId of Diagnostic.</span></span> <span data-ttu-id="ffd7a-134">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="ffd7a-134">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffd7a-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ffd7a-135">-Confirm</span></span>
<span data-ttu-id="ffd7a-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ffd7a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffd7a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffd7a-137">-WhatIf</span></span>
<span data-ttu-id="ffd7a-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ffd7a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffd7a-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ffd7a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffd7a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffd7a-140">CommonParameters</span></span>
<span data-ttu-id="ffd7a-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffd7a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffd7a-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ffd7a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffd7a-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="ffd7a-143">INPUTS</span></span>

### <span data-ttu-id="ffd7a-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ffd7a-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ffd7a-145">System.String</span><span class="sxs-lookup"><span data-stu-id="ffd7a-145">System.String</span></span>

### <span data-ttu-id="ffd7a-146">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ffd7a-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ffd7a-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ffd7a-147">OUTPUTS</span></span>

### <span data-ttu-id="ffd7a-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ffd7a-148">System.Boolean</span></span>

## <span data-ttu-id="ffd7a-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="ffd7a-149">NOTES</span></span>

## <span data-ttu-id="ffd7a-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ffd7a-150">RELATED LINKS</span></span>

[<span data-ttu-id="ffd7a-151">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="ffd7a-151">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="ffd7a-152">New-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="ffd7a-152">New-AzApiManagementDiagnostic</span></span>](./New-AzApiManagementDiagnostic.md)

[<span data-ttu-id="ffd7a-153">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="ffd7a-153">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)