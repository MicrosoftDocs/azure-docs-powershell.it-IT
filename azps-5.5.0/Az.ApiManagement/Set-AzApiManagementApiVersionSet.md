---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiVersionSet.md
ms.openlocfilehash: d85d480adc5d6c588c7da2f03c514258dc96a9e8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205611"
---
# <span data-ttu-id="2b903-101">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="2b903-101">Set-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="2b903-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b903-102">SYNOPSIS</span></span>
<span data-ttu-id="2b903-103">Aggiorna un set di versioni dell'API nel contesto di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="2b903-103">Updates an API Version Set in the API Management Context.</span></span>

## <span data-ttu-id="2b903-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2b903-104">SYNTAX</span></span>

### <span data-ttu-id="2b903-105">ExpandedParameter (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2b903-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2b903-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2b903-106">ByInputObject</span></span>
```
Set-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2b903-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2b903-107">DESCRIPTION</span></span>

<span data-ttu-id="2b903-108">Il cmdlet **Set-AzApiManagementApiVersionSet** modifica un set di versioni dell'API Di gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="2b903-108">The **Set-AzApiManagementApiVersionSet** cmdlet modifies an Azure API Management API Version Set.</span></span>

## <span data-ttu-id="2b903-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2b903-109">EXAMPLES</span></span>

### <span data-ttu-id="2b903-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2b903-110">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiVersionSet -Context $ApiMgmtContext -ApiVersionSetId "query-verion-set" -Scheme Header -HeaderName "api-version" -Description "Azure version header string"
```

<span data-ttu-id="2b903-111">Questo comando aggiorna un set di versioni dell'API esistente con lo schema di controllo delle versioni `Header` e il parametro `api-version` Header.</span><span class="sxs-lookup"><span data-stu-id="2b903-111">This command updates an existing API Version Set with versioning scheme `Header` and Header parameter `api-version`.</span></span>

## <span data-ttu-id="2b903-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2b903-112">PARAMETERS</span></span>

### <span data-ttu-id="2b903-113">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="2b903-113">-ApiVersionSetId</span></span>
<span data-ttu-id="2b903-114">Identificatore del nuovo set di versioni dell'API.</span><span class="sxs-lookup"><span data-stu-id="2b903-114">Identifier for new API Version Set.</span></span>

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

### <span data-ttu-id="2b903-115">-Context</span><span class="sxs-lookup"><span data-stu-id="2b903-115">-Context</span></span>
<span data-ttu-id="2b903-116">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="2b903-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="2b903-117">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="2b903-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b903-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b903-118">-DefaultProfile</span></span>
<span data-ttu-id="2b903-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2b903-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b903-120">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b903-120">-Description</span></span>
<span data-ttu-id="2b903-121">Descrizione del set di versioni dell'Api.</span><span class="sxs-lookup"><span data-stu-id="2b903-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="2b903-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="2b903-122">-HeaderName</span></span>
<span data-ttu-id="2b903-123">Valore dell'intestazione che conterrà le informazioni sul controllo delle versioni.</span><span class="sxs-lookup"><span data-stu-id="2b903-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="2b903-124">Se si sceglie HEADER dello schema di controllo delle versioni, è necessario specificare questo valore.</span><span class="sxs-lookup"><span data-stu-id="2b903-124">If versioning Scheme HEADER is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="2b903-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b903-125">-InputObject</span></span>
<span data-ttu-id="2b903-126">Istanza di PsApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="2b903-126">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="2b903-127">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="2b903-127">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b903-128">-Name</span><span class="sxs-lookup"><span data-stu-id="2b903-128">-Name</span></span>
<span data-ttu-id="2b903-129">Nome del set ApiVersion.</span><span class="sxs-lookup"><span data-stu-id="2b903-129">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="2b903-130">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="2b903-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="2b903-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2b903-131">-PassThru</span></span>
<span data-ttu-id="2b903-132">Se si specifica, nell'output verrà scritta l'istanza di Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet che rappresenta il set di apiVersionSet modificato.</span><span class="sxs-lookup"><span data-stu-id="2b903-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet type  representing the modified apiVersionSet will be written to output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b903-133">-QueryName</span><span class="sxs-lookup"><span data-stu-id="2b903-133">-QueryName</span></span>
<span data-ttu-id="2b903-134">Valore della query che conterrà le informazioni sul controllo delle versioni.</span><span class="sxs-lookup"><span data-stu-id="2b903-134">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="2b903-135">Se si sceglie la query dello schema di controllo delle versioni, è necessario specificare questo valore.</span><span class="sxs-lookup"><span data-stu-id="2b903-135">If versioning Scheme Query is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="2b903-136">-Schema</span><span class="sxs-lookup"><span data-stu-id="2b903-136">-Scheme</span></span>
<span data-ttu-id="2b903-137">Schema di controllo delle versioni da selezionare per il set di controllo delle versioni Api.</span><span class="sxs-lookup"><span data-stu-id="2b903-137">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="2b903-138">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="2b903-138">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme
Parameter Sets: (All)
Aliases:
Accepted values: Segment, Query, Header

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b903-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2b903-139">-Confirm</span></span>
<span data-ttu-id="2b903-140">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b903-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b903-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b903-141">-WhatIf</span></span>
<span data-ttu-id="2b903-142">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2b903-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2b903-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2b903-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b903-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b903-144">CommonParameters</span></span>
<span data-ttu-id="2b903-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b903-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b903-146">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2b903-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b903-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="2b903-147">INPUTS</span></span>

### <span data-ttu-id="2b903-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2b903-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2b903-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="2b903-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="2b903-150">System.String</span><span class="sxs-lookup"><span data-stu-id="2b903-150">System.String</span></span>

### <span data-ttu-id="2b903-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span><span class="sxs-lookup"><span data-stu-id="2b903-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="2b903-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2b903-152">OUTPUTS</span></span>

### <span data-ttu-id="2b903-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="2b903-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="2b903-154">NOTE</span><span class="sxs-lookup"><span data-stu-id="2b903-154">NOTES</span></span>

## <span data-ttu-id="2b903-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2b903-155">RELATED LINKS</span></span>

[<span data-ttu-id="2b903-156">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="2b903-156">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="2b903-157">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="2b903-157">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="2b903-158">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="2b903-158">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)
