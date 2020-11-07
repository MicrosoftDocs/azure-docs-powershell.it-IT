---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiSchema.md
ms.openlocfilehash: 02091c1a207bc10fbdb539fb9a301d002b631827
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675907"
---
# <span data-ttu-id="3b923-101">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="3b923-101">Set-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="3b923-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3b923-102">SYNOPSIS</span></span>
<span data-ttu-id="3b923-103">Modifica uno schema API</span><span class="sxs-lookup"><span data-stu-id="3b923-103">Modifies an API Schema</span></span>

## <span data-ttu-id="3b923-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3b923-104">SYNTAX</span></span>

### <span data-ttu-id="3b923-105">ExpandedParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3b923-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> -SchemaId <String>
 [-SchemaDocumentContentType <String>] [-SchemaDocument <String>] [-SchemaDocumentFilePath <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b923-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3b923-106">ByInputObject</span></span>
```
Set-AzApiManagementApiSchema -InputObject <PsApiManagementApiSchema> [-SchemaDocumentContentType <String>]
 [-SchemaDocument <String>] [-SchemaDocumentFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b923-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3b923-107">ByResourceId</span></span>
```
Set-AzApiManagementApiSchema -ResourceId <String> [-SchemaDocumentContentType <String>]
 [-SchemaDocument <String>] [-SchemaDocumentFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b923-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3b923-108">DESCRIPTION</span></span>
<span data-ttu-id="3b923-109">Il cmdlet **set-AzApiManagementApiSchema** modifica uno schema API di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="3b923-109">The **Set-AzApiManagementApiSchema** cmdlet modifies an Azure API Management API Schema.</span></span>

## <span data-ttu-id="3b923-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3b923-110">EXAMPLES</span></span>

### <span data-ttu-id="3b923-111">Esempio 1: modifica uno schema API</span><span class="sxs-lookup"><span data-stu-id="3b923-111">Example 1 : Modifies an API Schema</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiSchema -Context $ApiMgmtContext -ApiId "echo-api" -SchemaId "2"
```

<span data-ttu-id="3b923-112">L'esempio aggiorna lo schema API</span><span class="sxs-lookup"><span data-stu-id="3b923-112">The example updates the Api Schema</span></span>

## <span data-ttu-id="3b923-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3b923-113">PARAMETERS</span></span>

### <span data-ttu-id="3b923-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="3b923-114">-ApiId</span></span>
<span data-ttu-id="3b923-115">Identificatore dell'API esistente.</span><span class="sxs-lookup"><span data-stu-id="3b923-115">Identifier of existing API.</span></span>
<span data-ttu-id="3b923-116">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="3b923-116">This parameter is required.</span></span>

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

### <span data-ttu-id="3b923-117">-Contesto</span><span class="sxs-lookup"><span data-stu-id="3b923-117">-Context</span></span>
<span data-ttu-id="3b923-118">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="3b923-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="3b923-119">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="3b923-119">This parameter is required.</span></span>

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

### <span data-ttu-id="3b923-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b923-120">-DefaultProfile</span></span>
<span data-ttu-id="3b923-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3b923-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b923-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b923-122">-InputObject</span></span>
<span data-ttu-id="3b923-123">Istanza di PsApiManagementApiSchema.</span><span class="sxs-lookup"><span data-stu-id="3b923-123">Instance of PsApiManagementApiSchema.</span></span>
<span data-ttu-id="3b923-124">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="3b923-124">This parameter is required.</span></span>

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

### <span data-ttu-id="3b923-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3b923-125">-PassThru</span></span>
<span data-ttu-id="3b923-126">Se specificato, l'istanza del tipo Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi che rappresenta l'API set.</span><span class="sxs-lookup"><span data-stu-id="3b923-126">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="3b923-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b923-127">-ResourceId</span></span>
<span data-ttu-id="3b923-128">ResourceId ARM dello schema di diagnostica o API.</span><span class="sxs-lookup"><span data-stu-id="3b923-128">Arm ResourceId of Diagnostic or Api Schema.</span></span> <span data-ttu-id="3b923-129">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="3b923-129">This parameter is required.</span></span>

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

### <span data-ttu-id="3b923-130">-SchemaDocument</span><span class="sxs-lookup"><span data-stu-id="3b923-130">-SchemaDocument</span></span>
<span data-ttu-id="3b923-131">Documento dello schema API come stringa.</span><span class="sxs-lookup"><span data-stu-id="3b923-131">Api schema document as a string.</span></span> <span data-ttu-id="3b923-132">Questo parametro è obbligatorio-SchemaDocumentFile non è specificato.</span><span class="sxs-lookup"><span data-stu-id="3b923-132">This parameter is required is -SchemaDocumentFile is not specified.</span></span>

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

### <span data-ttu-id="3b923-133">-SchemaDocumentContentType</span><span class="sxs-lookup"><span data-stu-id="3b923-133">-SchemaDocumentContentType</span></span>
<span data-ttu-id="3b923-134">ContentType dello schema API.</span><span class="sxs-lookup"><span data-stu-id="3b923-134">ContentType of the api Schema.</span></span> <span data-ttu-id="3b923-135">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="3b923-135">This parameter is optional.</span></span>

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

### <span data-ttu-id="3b923-136">-SchemaDocumentFilePath</span><span class="sxs-lookup"><span data-stu-id="3b923-136">-SchemaDocumentFilePath</span></span>
<span data-ttu-id="3b923-137">Percorso file del documento dello schema API.</span><span class="sxs-lookup"><span data-stu-id="3b923-137">Api schema document file path.</span></span> <span data-ttu-id="3b923-138">Questo parametro è obbligatorio-SchemaDocument non è specificato.</span><span class="sxs-lookup"><span data-stu-id="3b923-138">This parameter is required is -SchemaDocument is not specified.</span></span>

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

### <span data-ttu-id="3b923-139">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="3b923-139">-SchemaId</span></span>
<span data-ttu-id="3b923-140">Identificatore dello schema esistente.</span><span class="sxs-lookup"><span data-stu-id="3b923-140">Identifier of existing Schema.</span></span>
<span data-ttu-id="3b923-141">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="3b923-141">This parameter is required.</span></span>

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

### <span data-ttu-id="3b923-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3b923-142">-Confirm</span></span>
<span data-ttu-id="3b923-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b923-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b923-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b923-144">-WhatIf</span></span>
<span data-ttu-id="3b923-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3b923-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3b923-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3b923-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b923-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b923-147">CommonParameters</span></span>
<span data-ttu-id="3b923-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b923-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b923-149">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3b923-149">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b923-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3b923-150">INPUTS</span></span>

### <span data-ttu-id="3b923-151">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3b923-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3b923-152">System. String</span><span class="sxs-lookup"><span data-stu-id="3b923-152">System.String</span></span>

### <span data-ttu-id="3b923-153">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="3b923-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

### <span data-ttu-id="3b923-154">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3b923-154">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3b923-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3b923-155">OUTPUTS</span></span>

### <span data-ttu-id="3b923-156">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="3b923-156">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="3b923-157">Note</span><span class="sxs-lookup"><span data-stu-id="3b923-157">NOTES</span></span>

## <span data-ttu-id="3b923-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3b923-158">RELATED LINKS</span></span>

[<span data-ttu-id="3b923-159">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="3b923-159">Get-AzApiManagementApiSchema</span></span>](./Get-AzApiManagementApiSchema.md)

[<span data-ttu-id="3b923-160">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="3b923-160">New-AzApiManagementApiSchema</span></span>](./New-AzApiManagementApiSchema.md)

[<span data-ttu-id="3b923-161">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="3b923-161">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

