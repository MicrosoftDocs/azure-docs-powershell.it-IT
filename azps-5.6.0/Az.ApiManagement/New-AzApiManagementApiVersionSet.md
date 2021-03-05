---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 126f30e732bc9c55c78c94d6c802b05a18ce29db
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993088"
---
# <span data-ttu-id="26b8a-101">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="26b8a-101">New-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="26b8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26b8a-102">SYNOPSIS</span></span>
<span data-ttu-id="26b8a-103">Crea un set di versioni dell'API.</span><span class="sxs-lookup"><span data-stu-id="26b8a-103">Creates an API Version Set.</span></span>

## <span data-ttu-id="26b8a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="26b8a-104">SYNTAX</span></span>

```
New-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>] -Name <String>
 -Scheme <PsApiManagementVersioningScheme> [-HeaderName <String>] [-QueryName <String>] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26b8a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="26b8a-105">DESCRIPTION</span></span>
<span data-ttu-id="26b8a-106">Il cmdlet **New-AzApiManagementApiVersionSet** crea un'entità set di versioni API nel contesto Gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="26b8a-106">The **New-AzApiManagementApiVersionSet** cmdlet creates an API Version set entity in the Azure API Management context.</span></span>

## <span data-ttu-id="26b8a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="26b8a-107">EXAMPLES</span></span>

### <span data-ttu-id="26b8a-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="26b8a-108">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> New-AzApiManagementApiVersionSet -Context $ApiMgmtContext  -Name "newversion" -Scheme Header -HeaderName "x-ms-version" -Description "version by xmsversion"

ApiVersionSetId   : ea9a87cd-a699-4a75-bf7d-909846b91268
Description       : version by xmsversion
VersionQueryName  :
VersionHeaderName : x-ms-version
DisplayName       : newversion
VersioningScheme  : Header
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/ea9a87cd-a699-4a75-bf7d-909846b91268
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="26b8a-109">Questo comando crea un set di versioni API per lo schema di controllo delle versioni `Query` e il parametro di `api-version` query.</span><span class="sxs-lookup"><span data-stu-id="26b8a-109">This command creates an API Version Set which versioning scheme `Query` and Query parameter `api-version`.</span></span>

## <span data-ttu-id="26b8a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26b8a-110">PARAMETERS</span></span>

### <span data-ttu-id="26b8a-111">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="26b8a-111">-ApiVersionSetId</span></span>
<span data-ttu-id="26b8a-112">Identificatore del nuovo set di versioni dell'API.</span><span class="sxs-lookup"><span data-stu-id="26b8a-112">Identifier for new API Version Set.</span></span>
<span data-ttu-id="26b8a-113">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="26b8a-113">This parameter is optional.</span></span>
<span data-ttu-id="26b8a-114">Se non è specificato, verrà generato un identificatore.</span><span class="sxs-lookup"><span data-stu-id="26b8a-114">If not specified an identifier will be generated.</span></span>

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

### <span data-ttu-id="26b8a-115">-Context</span><span class="sxs-lookup"><span data-stu-id="26b8a-115">-Context</span></span>
<span data-ttu-id="26b8a-116">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="26b8a-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="26b8a-117">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="26b8a-117">This parameter is required.</span></span>

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

### <span data-ttu-id="26b8a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26b8a-118">-DefaultProfile</span></span>
<span data-ttu-id="26b8a-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="26b8a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26b8a-120">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="26b8a-120">-Description</span></span>
<span data-ttu-id="26b8a-121">Descrizione del set di versioni dell'Api.</span><span class="sxs-lookup"><span data-stu-id="26b8a-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="26b8a-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="26b8a-122">-HeaderName</span></span>
<span data-ttu-id="26b8a-123">Valore dell'intestazione che conterrà le informazioni sul controllo delle versioni.</span><span class="sxs-lookup"><span data-stu-id="26b8a-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="26b8a-124">Se si sceglie INTESTAZIONE dello schema di controllo delle versioni, è necessario specificare questo valore.</span><span class="sxs-lookup"><span data-stu-id="26b8a-124">If versioning Scheme HEADER is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="26b8a-125">-Name</span><span class="sxs-lookup"><span data-stu-id="26b8a-125">-Name</span></span>
<span data-ttu-id="26b8a-126">Nome del set ApiVersion.</span><span class="sxs-lookup"><span data-stu-id="26b8a-126">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="26b8a-127">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="26b8a-127">This parameter is required.</span></span>

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

### <span data-ttu-id="26b8a-128">-QueryName</span><span class="sxs-lookup"><span data-stu-id="26b8a-128">-QueryName</span></span>
<span data-ttu-id="26b8a-129">Valore della query che conterrà le informazioni sul controllo delle versioni.</span><span class="sxs-lookup"><span data-stu-id="26b8a-129">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="26b8a-130">Se si sceglie la query dello schema di controllo delle versioni, è necessario specificare questo valore.</span><span class="sxs-lookup"><span data-stu-id="26b8a-130">If versioning Scheme Query is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="26b8a-131">-Schema</span><span class="sxs-lookup"><span data-stu-id="26b8a-131">-Scheme</span></span>
<span data-ttu-id="26b8a-132">Schema di controllo delle versioni da selezionare per il set di controllo delle versioni Api.</span><span class="sxs-lookup"><span data-stu-id="26b8a-132">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="26b8a-133">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="26b8a-133">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme
Parameter Sets: (All)
Aliases:
Accepted values: Segment, Query, Header

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26b8a-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="26b8a-134">-Confirm</span></span>
<span data-ttu-id="26b8a-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26b8a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26b8a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26b8a-136">-WhatIf</span></span>
<span data-ttu-id="26b8a-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="26b8a-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26b8a-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="26b8a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26b8a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26b8a-139">CommonParameters</span></span>
<span data-ttu-id="26b8a-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26b8a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26b8a-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="26b8a-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26b8a-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="26b8a-142">INPUTS</span></span>

### <span data-ttu-id="26b8a-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="26b8a-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="26b8a-144">System.String</span><span class="sxs-lookup"><span data-stu-id="26b8a-144">System.String</span></span>

### <span data-ttu-id="26b8a-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span><span class="sxs-lookup"><span data-stu-id="26b8a-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="26b8a-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="26b8a-146">OUTPUTS</span></span>

### <span data-ttu-id="26b8a-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="26b8a-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="26b8a-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="26b8a-148">NOTES</span></span>

## <span data-ttu-id="26b8a-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="26b8a-149">RELATED LINKS</span></span>

[<span data-ttu-id="26b8a-150">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="26b8a-150">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="26b8a-151">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="26b8a-151">Remove-AzApiManagementApiVersionSet</span></span>](./Remove-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="26b8a-152">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="26b8a-152">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)