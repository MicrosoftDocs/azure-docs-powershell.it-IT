---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApiVersionSet.md
ms.openlocfilehash: 5d9bc89eb2d4188b7b2903bee7a8b0a44bec1216
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517672"
---
# <span data-ttu-id="158b9-101">Set-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="158b9-101">Set-AzureRmApiManagementApiVersionSet</span></span>

## <span data-ttu-id="158b9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="158b9-102">SYNOPSIS</span></span>
<span data-ttu-id="158b9-103">Aggiorna una versione dell'API impostata nel contesto di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="158b9-103">Updates an API Version Set in the API Management Context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="158b9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="158b9-104">SYNTAX</span></span>

### <span data-ttu-id="158b9-105">ExpandedParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="158b9-105">ExpandedParameter (Default)</span></span>
```
Set-AzureRmApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String>
 [-Name <String>] [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="158b9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="158b9-106">ByInputObject</span></span>
```
Set-AzureRmApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="158b9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="158b9-107">DESCRIPTION</span></span>

<span data-ttu-id="158b9-108">Il cmdlet **set-AzureRmApiManagementApiVersionSet** modifica un set di versioni dell'API di gestione di Azure API.</span><span class="sxs-lookup"><span data-stu-id="158b9-108">The **Set-AzureRmApiManagementApiVersionSet** cmdlet modifies an Azure API Management API Version Set.</span></span>

## <span data-ttu-id="158b9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="158b9-109">EXAMPLES</span></span>

### <span data-ttu-id="158b9-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="158b9-110">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementApiVersionSet -Context $ApiMgmtContext -ApiVersionSetId "query-verion-set" -Scheme Header -HeaderName "api-version" -Description "Azure version header string"
```

<span data-ttu-id="158b9-111">Questo comando aggiorna un set di versioni dell'API esistente con il parametro di intestazione e lo schema di controllo delle versioni `Header` `api-version` .</span><span class="sxs-lookup"><span data-stu-id="158b9-111">This command updates an existing API Version Set with versioning scheme `Header` and Header parameter `api-version`.</span></span>

## <span data-ttu-id="158b9-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="158b9-112">PARAMETERS</span></span>

### <span data-ttu-id="158b9-113">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="158b9-113">-ApiVersionSetId</span></span>
<span data-ttu-id="158b9-114">Identificatore per il nuovo set di versioni API.</span><span class="sxs-lookup"><span data-stu-id="158b9-114">Identifier for new API Version Set.</span></span>

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

### <span data-ttu-id="158b9-115">-Contesto</span><span class="sxs-lookup"><span data-stu-id="158b9-115">-Context</span></span>
<span data-ttu-id="158b9-116">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="158b9-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="158b9-117">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="158b9-117">This parameter is required.</span></span>

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

### <span data-ttu-id="158b9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="158b9-118">-DefaultProfile</span></span>
<span data-ttu-id="158b9-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="158b9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="158b9-120">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="158b9-120">-Description</span></span>
<span data-ttu-id="158b9-121">Descrizione del set di versioni dell'API.</span><span class="sxs-lookup"><span data-stu-id="158b9-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="158b9-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="158b9-122">-HeaderName</span></span>
<span data-ttu-id="158b9-123">Il valore dell'intestazione che conterrà le informazioni sul controllo delle versioni.</span><span class="sxs-lookup"><span data-stu-id="158b9-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="158b9-124">Se l'intestazione dello schema di controllo delle versioni è choosen, questo valore deve essere specificato.</span><span class="sxs-lookup"><span data-stu-id="158b9-124">If versioning Scheme HEADER is choosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="158b9-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="158b9-125">-InputObject</span></span>
<span data-ttu-id="158b9-126">Istanza di PsApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="158b9-126">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="158b9-127">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="158b9-127">This parameter is required.</span></span>

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

### <span data-ttu-id="158b9-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="158b9-128">-Name</span></span>
<span data-ttu-id="158b9-129">Il nome del set di ApiVersion.</span><span class="sxs-lookup"><span data-stu-id="158b9-129">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="158b9-130">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="158b9-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="158b9-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="158b9-131">-PassThru</span></span>
<span data-ttu-id="158b9-132">Se specificato, viene scritta in output l'istanza del tipo Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiVersionSet che rappresenta il apiVersionSet modificato.</span><span class="sxs-lookup"><span data-stu-id="158b9-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet type  representing the modified apiVersionSet will be written to output.</span></span>

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

### <span data-ttu-id="158b9-133">-QueryName</span><span class="sxs-lookup"><span data-stu-id="158b9-133">-QueryName</span></span>
<span data-ttu-id="158b9-134">Il valore della query che conterrà le informazioni sul controllo delle versioni.</span><span class="sxs-lookup"><span data-stu-id="158b9-134">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="158b9-135">Se la query dello schema di controllo delle versioni è choosen, questo valore deve essere specificato.</span><span class="sxs-lookup"><span data-stu-id="158b9-135">If versioning Scheme Query is choosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="158b9-136">-Schema</span><span class="sxs-lookup"><span data-stu-id="158b9-136">-Scheme</span></span>
<span data-ttu-id="158b9-137">Schema di controllo delle versioni per selezionare il set di controllo delle versioni delle API.</span><span class="sxs-lookup"><span data-stu-id="158b9-137">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="158b9-138">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="158b9-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="158b9-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="158b9-139">-Confirm</span></span>
<span data-ttu-id="158b9-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="158b9-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="158b9-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="158b9-141">-WhatIf</span></span>
<span data-ttu-id="158b9-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="158b9-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="158b9-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="158b9-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="158b9-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="158b9-144">CommonParameters</span></span>
<span data-ttu-id="158b9-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="158b9-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="158b9-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="158b9-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="158b9-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="158b9-147">INPUTS</span></span>

### <span data-ttu-id="158b9-148">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="158b9-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="158b9-149">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="158b9-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>
<span data-ttu-id="158b9-150">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="158b9-150">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="158b9-151">System. String</span><span class="sxs-lookup"><span data-stu-id="158b9-151">System.String</span></span>

### <span data-ttu-id="158b9-152">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementVersioningScheme</span><span class="sxs-lookup"><span data-stu-id="158b9-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="158b9-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="158b9-153">OUTPUTS</span></span>

### <span data-ttu-id="158b9-154">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="158b9-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="158b9-155">Note</span><span class="sxs-lookup"><span data-stu-id="158b9-155">NOTES</span></span>

## <span data-ttu-id="158b9-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="158b9-156">RELATED LINKS</span></span>

[<span data-ttu-id="158b9-157">Get-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="158b9-157">Get-AzureRmApiManagementApiVersionSet</span></span>](./Get-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="158b9-158">New-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="158b9-158">New-AzureRmApiManagementApiVersionSet</span></span>](./New-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="158b9-159">Set-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="158b9-159">Set-AzureRmApiManagementApiVersionSet</span></span>](./Set-AzureRmApiManagementApiVersionSet.md)
