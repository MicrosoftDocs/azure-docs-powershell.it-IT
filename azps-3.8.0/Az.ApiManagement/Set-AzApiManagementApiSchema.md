---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiSchema.md
ms.openlocfilehash: 23881baf47536db4fa694cf2165b8550b7f8cd62
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021821"
---
# <span data-ttu-id="8dfd6-101">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="8dfd6-101">Set-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="8dfd6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8dfd6-102">SYNOPSIS</span></span>
<span data-ttu-id="8dfd6-103">Modifica uno schema API</span><span class="sxs-lookup"><span data-stu-id="8dfd6-103">Modifies an API Schema</span></span>

## <span data-ttu-id="8dfd6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8dfd6-104">SYNTAX</span></span>

### <span data-ttu-id="8dfd6-105">ExpandedParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8dfd6-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> -SchemaId <String>
 [-SchemaDocumentContentType <String>] [-SchemaDocument <String>] [-SchemaDocumentFilePath <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dfd6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8dfd6-106">ByInputObject</span></span>
```
Set-AzApiManagementApiSchema -InputObject <PsApiManagementApiSchema> [-SchemaDocumentContentType <String>]
 [-SchemaDocument <String>] [-SchemaDocumentFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dfd6-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8dfd6-107">ByResourceId</span></span>
```
Set-AzApiManagementApiSchema -ResourceId <String> [-SchemaDocumentContentType <String>]
 [-SchemaDocument <String>] [-SchemaDocumentFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8dfd6-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8dfd6-108">DESCRIPTION</span></span>
<span data-ttu-id="8dfd6-109">Il cmdlet **set-AzApiManagementApiSchema** modifica uno schema API di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="8dfd6-109">The **Set-AzApiManagementApiSchema** cmdlet modifies an Azure API Management API Schema.</span></span>

## <span data-ttu-id="8dfd6-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8dfd6-110">EXAMPLES</span></span>

### <span data-ttu-id="8dfd6-111">Esempio 1: modifica uno schema API</span><span class="sxs-lookup"><span data-stu-id="8dfd6-111">Example 1 : Modifies an API Schema</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiSchema -Context $ApiMgmtContext -ApiId "echo-api" -SchemaId "2"
```

<span data-ttu-id="8dfd6-112">L'esempio aggiorna lo schema API</span><span class="sxs-lookup"><span data-stu-id="8dfd6-112">The example updates the Api Schema</span></span>

## <span data-ttu-id="8dfd6-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8dfd6-113">PARAMETERS</span></span>

### <span data-ttu-id="8dfd6-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="8dfd6-114">-ApiId</span></span>
<span data-ttu-id="8dfd6-115">Identificatore dell'API esistente.</span><span class="sxs-lookup"><span data-stu-id="8dfd6-115">Identifier of existing API.</span></span>
<span data-ttu-id="8dfd6-116">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="8dfd6-116">This parameter is required.</span></span>

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

### <span data-ttu-id="8dfd6-117">-Contesto</span><span class="sxs-lookup"><span data-stu-id="8dfd6-117">-Context</span></span>
<span data-ttu-id="8dfd6-118">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="8dfd6-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="8dfd6-119">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="8dfd6-119">This parameter is required.</span></span>

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

### <span data-ttu-id="8dfd6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dfd6-120">-DefaultProfile</span></span>
<span data-ttu-id="8dfd6-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8dfd6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8dfd6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8dfd6-122">-InputObject</span></span>
<span data-ttu-id="8dfd6-123">Istanza di PsApiManagementApiSchema.</span><span class="sxs-lookup"><span data-stu-id="8dfd6-123">Instance of PsApiManagementApiSchema.</span></span>
<span data-ttu-id="8dfd6-124">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="8dfd6-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8dfd6-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8dfd6-125">-PassThru</span></span>
<span data-ttu-id="8dfd6-126">Se specificato, l'istanza del tipo Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi che rappresenta l'API set.</span><span class="sxs-lookup"><span data-stu-id="8dfd6-126">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="8dfd6-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8dfd6-127">-ResourceId</span></span>
<span data-ttu-id="8dfd6-128">ResourceId ARM dello schema di diagnostica o API.</span><span class="sxs-lookup"><span data-stu-id="8dfd6-128">Arm ResourceId of Diagnostic or Api Schema.</span></span> <span data-ttu-id="8dfd6-129">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="8dfd6-129">This parameter is required.</span></span>

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

### <span data-ttu-id="8dfd6-130">-SchemaDocument</span><span class="sxs-lookup"><span data-stu-id="8dfd6-130">-SchemaDocument</span></span>
<span data-ttu-id="8dfd6-131">Documento dello schema API come stringa.</span><span class="sxs-lookup"><span data-stu-id="8dfd6-131">Api schema document as a string.</span></span> <span data-ttu-id="8dfd6-132">Questo parametro è obbligatorio-SchemaDocumentFile non è specificato.</span><span class="sxs-lookup"><span data-stu-id="8dfd6-132">This parameter is required is -SchemaDocumentFile is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dfd6-133">-SchemaDocumentContentType</span><span class="sxs-lookup"><span data-stu-id="8dfd6-133">-SchemaDocumentContentType</span></span>
<span data-ttu-id="8dfd6-134">ContentType dello schema API.</span><span class="sxs-lookup"><span data-stu-id="8dfd6-134">ContentType of the api Schema.</span></span> <span data-ttu-id="8dfd6-135">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="8dfd6-135">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dfd6-136">-SchemaDocumentFilePath</span><span class="sxs-lookup"><span data-stu-id="8dfd6-136">-SchemaDocumentFilePath</span></span>
<span data-ttu-id="8dfd6-137">Percorso file del documento dello schema API.</span><span class="sxs-lookup"><span data-stu-id="8dfd6-137">Api schema document file path.</span></span> <span data-ttu-id="8dfd6-138">Questo parametro è obbligatorio-SchemaDocument non è specificato.</span><span class="sxs-lookup"><span data-stu-id="8dfd6-138">This parameter is required is -SchemaDocument is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dfd6-139">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="8dfd6-139">-SchemaId</span></span>
<span data-ttu-id="8dfd6-140">Identificatore dello schema esistente.</span><span class="sxs-lookup"><span data-stu-id="8dfd6-140">Identifier of existing Schema.</span></span>
<span data-ttu-id="8dfd6-141">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="8dfd6-141">This parameter is required.</span></span>

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

### <span data-ttu-id="8dfd6-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8dfd6-142">-Confirm</span></span>
<span data-ttu-id="8dfd6-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8dfd6-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dfd6-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dfd6-144">-WhatIf</span></span>
<span data-ttu-id="8dfd6-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8dfd6-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8dfd6-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8dfd6-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dfd6-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dfd6-147">CommonParameters</span></span>
<span data-ttu-id="8dfd6-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dfd6-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dfd6-149">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8dfd6-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dfd6-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8dfd6-150">INPUTS</span></span>

### <span data-ttu-id="8dfd6-151">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8dfd6-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8dfd6-152">System. String</span><span class="sxs-lookup"><span data-stu-id="8dfd6-152">System.String</span></span>

### <span data-ttu-id="8dfd6-153">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="8dfd6-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

### <span data-ttu-id="8dfd6-154">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8dfd6-154">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8dfd6-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8dfd6-155">OUTPUTS</span></span>

### <span data-ttu-id="8dfd6-156">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8dfd6-156">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="8dfd6-157">Note</span><span class="sxs-lookup"><span data-stu-id="8dfd6-157">NOTES</span></span>

## <span data-ttu-id="8dfd6-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8dfd6-158">RELATED LINKS</span></span>

[<span data-ttu-id="8dfd6-159">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="8dfd6-159">Get-AzApiManagementApiSchema</span></span>](./Get-AzApiManagementApiSchema.md)

[<span data-ttu-id="8dfd6-160">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="8dfd6-160">New-AzApiManagementApiSchema</span></span>](./New-AzApiManagementApiSchema.md)

[<span data-ttu-id="8dfd6-161">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="8dfd6-161">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

