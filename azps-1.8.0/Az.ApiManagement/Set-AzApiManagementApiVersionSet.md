---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 32279f3f87ec3653fe4d9aab25a98c90f7642b3b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852401"
---
# <span data-ttu-id="b1c6f-101">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b1c6f-101">Set-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="b1c6f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b1c6f-102">SYNOPSIS</span></span>
<span data-ttu-id="b1c6f-103">Aggiorna una versione dell'API impostata nel contesto di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="b1c6f-103">Updates an API Version Set in the API Management Context.</span></span>

## <span data-ttu-id="b1c6f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b1c6f-104">SYNTAX</span></span>

### <span data-ttu-id="b1c6f-105">ExpandedParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b1c6f-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b1c6f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b1c6f-106">ByInputObject</span></span>
```
Set-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b1c6f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1c6f-107">DESCRIPTION</span></span>

<span data-ttu-id="b1c6f-108">Il cmdlet **set-AzApiManagementApiVersionSet** modifica un set di versioni dell'API di gestione di Azure API.</span><span class="sxs-lookup"><span data-stu-id="b1c6f-108">The **Set-AzApiManagementApiVersionSet** cmdlet modifies an Azure API Management API Version Set.</span></span>

## <span data-ttu-id="b1c6f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b1c6f-109">EXAMPLES</span></span>

### <span data-ttu-id="b1c6f-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b1c6f-110">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiVersionSet -Context $ApiMgmtContext -ApiVersionSetId "query-verion-set" -Scheme Header -HeaderName "api-version" -Description "Azure version header string"
```

<span data-ttu-id="b1c6f-111">Questo comando aggiorna un set di versioni dell'API esistente con il parametro di intestazione e lo schema di controllo delle versioni `Header` `api-version` .</span><span class="sxs-lookup"><span data-stu-id="b1c6f-111">This command updates an existing API Version Set with versioning scheme `Header` and Header parameter `api-version`.</span></span>

## <span data-ttu-id="b1c6f-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b1c6f-112">PARAMETERS</span></span>

### <span data-ttu-id="b1c6f-113">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="b1c6f-113">-ApiVersionSetId</span></span>
<span data-ttu-id="b1c6f-114">Identificatore per il nuovo set di versioni API.</span><span class="sxs-lookup"><span data-stu-id="b1c6f-114">Identifier for new API Version Set.</span></span>

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

### <span data-ttu-id="b1c6f-115">-Contesto</span><span class="sxs-lookup"><span data-stu-id="b1c6f-115">-Context</span></span>
<span data-ttu-id="b1c6f-116">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b1c6f-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b1c6f-117">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="b1c6f-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1c6f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1c6f-118">-DefaultProfile</span></span>
<span data-ttu-id="b1c6f-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b1c6f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1c6f-120">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1c6f-120">-Description</span></span>
<span data-ttu-id="b1c6f-121">Descrizione del set di versioni dell'API.</span><span class="sxs-lookup"><span data-stu-id="b1c6f-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="b1c6f-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="b1c6f-122">-HeaderName</span></span>
<span data-ttu-id="b1c6f-123">Il valore dell'intestazione che conterrà le informazioni sul controllo delle versioni.</span><span class="sxs-lookup"><span data-stu-id="b1c6f-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="b1c6f-124">Se l'intestazione dello schema di controllo delle versioni è choosen, questo valore deve essere specificato.</span><span class="sxs-lookup"><span data-stu-id="b1c6f-124">If versioning Scheme HEADER is choosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="b1c6f-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1c6f-125">-InputObject</span></span>
<span data-ttu-id="b1c6f-126">Istanza di PsApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="b1c6f-126">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="b1c6f-127">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="b1c6f-127">This parameter is required.</span></span>

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

### <span data-ttu-id="b1c6f-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="b1c6f-128">-Name</span></span>
<span data-ttu-id="b1c6f-129">Il nome del set di ApiVersion.</span><span class="sxs-lookup"><span data-stu-id="b1c6f-129">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="b1c6f-130">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b1c6f-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="b1c6f-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b1c6f-131">-PassThru</span></span>
<span data-ttu-id="b1c6f-132">Se specificato, viene scritta in output l'istanza del tipo Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiVersionSet che rappresenta il apiVersionSet modificato.</span><span class="sxs-lookup"><span data-stu-id="b1c6f-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet type  representing the modified apiVersionSet will be written to output.</span></span>

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

### <span data-ttu-id="b1c6f-133">-QueryName</span><span class="sxs-lookup"><span data-stu-id="b1c6f-133">-QueryName</span></span>
<span data-ttu-id="b1c6f-134">Il valore della query che conterrà le informazioni sul controllo delle versioni.</span><span class="sxs-lookup"><span data-stu-id="b1c6f-134">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="b1c6f-135">Se la query dello schema di controllo delle versioni è choosen, questo valore deve essere specificato.</span><span class="sxs-lookup"><span data-stu-id="b1c6f-135">If versioning Scheme Query is choosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="b1c6f-136">-Schema</span><span class="sxs-lookup"><span data-stu-id="b1c6f-136">-Scheme</span></span>
<span data-ttu-id="b1c6f-137">Schema di controllo delle versioni per selezionare il set di controllo delle versioni delle API.</span><span class="sxs-lookup"><span data-stu-id="b1c6f-137">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="b1c6f-138">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b1c6f-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="b1c6f-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b1c6f-139">-Confirm</span></span>
<span data-ttu-id="b1c6f-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1c6f-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1c6f-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1c6f-141">-WhatIf</span></span>
<span data-ttu-id="b1c6f-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b1c6f-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b1c6f-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b1c6f-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1c6f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1c6f-144">CommonParameters</span></span>
<span data-ttu-id="b1c6f-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1c6f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1c6f-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1c6f-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1c6f-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b1c6f-147">INPUTS</span></span>

### <span data-ttu-id="b1c6f-148">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b1c6f-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b1c6f-149">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b1c6f-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="b1c6f-150">System. String</span><span class="sxs-lookup"><span data-stu-id="b1c6f-150">System.String</span></span>

### <span data-ttu-id="b1c6f-151">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementVersioningScheme</span><span class="sxs-lookup"><span data-stu-id="b1c6f-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="b1c6f-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b1c6f-152">OUTPUTS</span></span>

### <span data-ttu-id="b1c6f-153">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b1c6f-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="b1c6f-154">Note</span><span class="sxs-lookup"><span data-stu-id="b1c6f-154">NOTES</span></span>

## <span data-ttu-id="b1c6f-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b1c6f-155">RELATED LINKS</span></span>

[<span data-ttu-id="b1c6f-156">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b1c6f-156">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="b1c6f-157">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b1c6f-157">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="b1c6f-158">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b1c6f-158">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)
