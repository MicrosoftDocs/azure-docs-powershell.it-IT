---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiVersionSet.md
ms.openlocfilehash: a29713e91027ee6ca6e3cbc6390d63829fbb612c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675906"
---
# <span data-ttu-id="e4955-101">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="e4955-101">Set-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="e4955-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e4955-102">SYNOPSIS</span></span>
<span data-ttu-id="e4955-103">Aggiorna una versione dell'API impostata nel contesto di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="e4955-103">Updates an API Version Set in the API Management Context.</span></span>

## <span data-ttu-id="e4955-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e4955-104">SYNTAX</span></span>

### <span data-ttu-id="e4955-105">ExpandedParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e4955-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e4955-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e4955-106">ByInputObject</span></span>
```
Set-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e4955-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e4955-107">DESCRIPTION</span></span>

<span data-ttu-id="e4955-108">Il cmdlet **set-AzApiManagementApiVersionSet** modifica un set di versioni dell'API di gestione di Azure API.</span><span class="sxs-lookup"><span data-stu-id="e4955-108">The **Set-AzApiManagementApiVersionSet** cmdlet modifies an Azure API Management API Version Set.</span></span>

## <span data-ttu-id="e4955-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e4955-109">EXAMPLES</span></span>

### <span data-ttu-id="e4955-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e4955-110">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiVersionSet -Context $ApiMgmtContext -ApiVersionSetId "query-verion-set" -Scheme Header -HeaderName "api-version" -Description "Azure version header string"
```

<span data-ttu-id="e4955-111">Questo comando aggiorna un set di versioni dell'API esistente con il parametro di intestazione e lo schema di controllo delle versioni `Header` `api-version` .</span><span class="sxs-lookup"><span data-stu-id="e4955-111">This command updates an existing API Version Set with versioning scheme `Header` and Header parameter `api-version`.</span></span>

## <span data-ttu-id="e4955-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e4955-112">PARAMETERS</span></span>

### <span data-ttu-id="e4955-113">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="e4955-113">-ApiVersionSetId</span></span>
<span data-ttu-id="e4955-114">Identificatore per il nuovo set di versioni API.</span><span class="sxs-lookup"><span data-stu-id="e4955-114">Identifier for new API Version Set.</span></span>

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

### <span data-ttu-id="e4955-115">-Contesto</span><span class="sxs-lookup"><span data-stu-id="e4955-115">-Context</span></span>
<span data-ttu-id="e4955-116">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="e4955-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e4955-117">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="e4955-117">This parameter is required.</span></span>

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

### <span data-ttu-id="e4955-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4955-118">-DefaultProfile</span></span>
<span data-ttu-id="e4955-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e4955-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4955-120">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="e4955-120">-Description</span></span>
<span data-ttu-id="e4955-121">Descrizione del set di versioni dell'API.</span><span class="sxs-lookup"><span data-stu-id="e4955-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="e4955-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="e4955-122">-HeaderName</span></span>
<span data-ttu-id="e4955-123">Il valore dell'intestazione che conterrà le informazioni sul controllo delle versioni.</span><span class="sxs-lookup"><span data-stu-id="e4955-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="e4955-124">Se si sceglie l'intestazione dello schema di controllo, questo valore deve essere specificato.</span><span class="sxs-lookup"><span data-stu-id="e4955-124">If versioning Scheme HEADER is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="e4955-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4955-125">-InputObject</span></span>
<span data-ttu-id="e4955-126">Istanza di PsApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="e4955-126">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="e4955-127">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="e4955-127">This parameter is required.</span></span>

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

### <span data-ttu-id="e4955-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="e4955-128">-Name</span></span>
<span data-ttu-id="e4955-129">Il nome del set di ApiVersion.</span><span class="sxs-lookup"><span data-stu-id="e4955-129">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="e4955-130">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e4955-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="e4955-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e4955-131">-PassThru</span></span>
<span data-ttu-id="e4955-132">Se specificato, viene scritta in output l'istanza del tipo Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiVersionSet che rappresenta il apiVersionSet modificato.</span><span class="sxs-lookup"><span data-stu-id="e4955-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet type  representing the modified apiVersionSet will be written to output.</span></span>

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

### <span data-ttu-id="e4955-133">-QueryName</span><span class="sxs-lookup"><span data-stu-id="e4955-133">-QueryName</span></span>
<span data-ttu-id="e4955-134">Il valore della query che conterrà le informazioni sul controllo delle versioni.</span><span class="sxs-lookup"><span data-stu-id="e4955-134">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="e4955-135">Se viene scelta la query dello schema di controllo delle versioni, questo valore deve essere specificato.</span><span class="sxs-lookup"><span data-stu-id="e4955-135">If versioning Scheme Query is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="e4955-136">-Schema</span><span class="sxs-lookup"><span data-stu-id="e4955-136">-Scheme</span></span>
<span data-ttu-id="e4955-137">Schema di controllo delle versioni per selezionare il set di controllo delle versioni delle API.</span><span class="sxs-lookup"><span data-stu-id="e4955-137">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="e4955-138">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e4955-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="e4955-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e4955-139">-Confirm</span></span>
<span data-ttu-id="e4955-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4955-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4955-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4955-141">-WhatIf</span></span>
<span data-ttu-id="e4955-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e4955-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e4955-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e4955-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4955-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4955-144">CommonParameters</span></span>
<span data-ttu-id="e4955-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4955-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4955-146">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e4955-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4955-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e4955-147">INPUTS</span></span>

### <span data-ttu-id="e4955-148">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e4955-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e4955-149">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="e4955-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="e4955-150">System. String</span><span class="sxs-lookup"><span data-stu-id="e4955-150">System.String</span></span>

### <span data-ttu-id="e4955-151">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementVersioningScheme</span><span class="sxs-lookup"><span data-stu-id="e4955-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="e4955-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e4955-152">OUTPUTS</span></span>

### <span data-ttu-id="e4955-153">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="e4955-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="e4955-154">Note</span><span class="sxs-lookup"><span data-stu-id="e4955-154">NOTES</span></span>

## <span data-ttu-id="e4955-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e4955-155">RELATED LINKS</span></span>

[<span data-ttu-id="e4955-156">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="e4955-156">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="e4955-157">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="e4955-157">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="e4955-158">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="e4955-158">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)
