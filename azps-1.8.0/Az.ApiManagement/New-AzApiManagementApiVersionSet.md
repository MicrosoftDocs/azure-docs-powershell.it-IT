---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 58f9fda87bc24b22a68e98d60092b80002e74e4a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673602"
---
# <span data-ttu-id="195cf-101">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="195cf-101">New-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="195cf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="195cf-102">SYNOPSIS</span></span>
<span data-ttu-id="195cf-103">Crea un set di versioni dell'API.</span><span class="sxs-lookup"><span data-stu-id="195cf-103">Creates an API Version Set.</span></span>

## <span data-ttu-id="195cf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="195cf-104">SYNTAX</span></span>

```
New-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>] -Name <String>
 -Scheme <PsApiManagementVersioningScheme> [-HeaderName <String>] [-QueryName <String>] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="195cf-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="195cf-105">DESCRIPTION</span></span>
<span data-ttu-id="195cf-106">Il cmdlet **New-AzApiManagementApiVersionSet** crea un'entità set di versioni API nel contesto di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="195cf-106">The **New-AzApiManagementApiVersionSet** cmdlet creates an API Version set entity in the Azure API Management context.</span></span>

## <span data-ttu-id="195cf-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="195cf-107">EXAMPLES</span></span>

### <span data-ttu-id="195cf-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="195cf-108">Example 1</span></span>
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

<span data-ttu-id="195cf-109">Questo comando crea una versione dell'API che consente di impostare lo schema di controllo delle versioni `Query` e il parametro di query `api-version` .</span><span class="sxs-lookup"><span data-stu-id="195cf-109">This command creates an API Version Set which versioning scheme `Query` and Query parameter `api-version`.</span></span>

## <span data-ttu-id="195cf-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="195cf-110">PARAMETERS</span></span>

### <span data-ttu-id="195cf-111">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="195cf-111">-ApiVersionSetId</span></span>
<span data-ttu-id="195cf-112">Identificatore per il nuovo set di versioni API.</span><span class="sxs-lookup"><span data-stu-id="195cf-112">Identifier for new API Version Set.</span></span>
<span data-ttu-id="195cf-113">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="195cf-113">This parameter is optional.</span></span>
<span data-ttu-id="195cf-114">Se non viene specificato, verrà generato un identificatore.</span><span class="sxs-lookup"><span data-stu-id="195cf-114">If not specified an identifier will be generated.</span></span>

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

### <span data-ttu-id="195cf-115">-Contesto</span><span class="sxs-lookup"><span data-stu-id="195cf-115">-Context</span></span>
<span data-ttu-id="195cf-116">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="195cf-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="195cf-117">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="195cf-117">This parameter is required.</span></span>

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

### <span data-ttu-id="195cf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="195cf-118">-DefaultProfile</span></span>
<span data-ttu-id="195cf-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="195cf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="195cf-120">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="195cf-120">-Description</span></span>
<span data-ttu-id="195cf-121">Descrizione del set di versioni dell'API.</span><span class="sxs-lookup"><span data-stu-id="195cf-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="195cf-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="195cf-122">-HeaderName</span></span>
<span data-ttu-id="195cf-123">Il valore dell'intestazione che conterrà le informazioni sul controllo delle versioni.</span><span class="sxs-lookup"><span data-stu-id="195cf-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="195cf-124">Se l'intestazione dello schema di controllo delle versioni è choosen, questo valore deve essere specificato.</span><span class="sxs-lookup"><span data-stu-id="195cf-124">If versioning Scheme HEADER is choosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="195cf-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="195cf-125">-Name</span></span>
<span data-ttu-id="195cf-126">Il nome del set di ApiVersion.</span><span class="sxs-lookup"><span data-stu-id="195cf-126">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="195cf-127">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="195cf-127">This parameter is required.</span></span>

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

### <span data-ttu-id="195cf-128">-QueryName</span><span class="sxs-lookup"><span data-stu-id="195cf-128">-QueryName</span></span>
<span data-ttu-id="195cf-129">Il valore della query che conterrà le informazioni sul controllo delle versioni.</span><span class="sxs-lookup"><span data-stu-id="195cf-129">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="195cf-130">Se la query dello schema di controllo delle versioni è choosen, questo valore deve essere specificato.</span><span class="sxs-lookup"><span data-stu-id="195cf-130">If versioning Scheme Query is choosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="195cf-131">-Schema</span><span class="sxs-lookup"><span data-stu-id="195cf-131">-Scheme</span></span>
<span data-ttu-id="195cf-132">Schema di controllo delle versioni per selezionare il set di controllo delle versioni delle API.</span><span class="sxs-lookup"><span data-stu-id="195cf-132">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="195cf-133">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="195cf-133">This parameter is required.</span></span>

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

### <span data-ttu-id="195cf-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="195cf-134">-Confirm</span></span>
<span data-ttu-id="195cf-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="195cf-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="195cf-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="195cf-136">-WhatIf</span></span>
<span data-ttu-id="195cf-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="195cf-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="195cf-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="195cf-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="195cf-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="195cf-139">CommonParameters</span></span>
<span data-ttu-id="195cf-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="195cf-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="195cf-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="195cf-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="195cf-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="195cf-142">INPUTS</span></span>

### <span data-ttu-id="195cf-143">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="195cf-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="195cf-144">System. String</span><span class="sxs-lookup"><span data-stu-id="195cf-144">System.String</span></span>

### <span data-ttu-id="195cf-145">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementVersioningScheme</span><span class="sxs-lookup"><span data-stu-id="195cf-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="195cf-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="195cf-146">OUTPUTS</span></span>

### <span data-ttu-id="195cf-147">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="195cf-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="195cf-148">Note</span><span class="sxs-lookup"><span data-stu-id="195cf-148">NOTES</span></span>

## <span data-ttu-id="195cf-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="195cf-149">RELATED LINKS</span></span>

[<span data-ttu-id="195cf-150">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="195cf-150">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="195cf-151">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="195cf-151">Remove-AzApiManagementApiVersionSet</span></span>](./Remove-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="195cf-152">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="195cf-152">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)