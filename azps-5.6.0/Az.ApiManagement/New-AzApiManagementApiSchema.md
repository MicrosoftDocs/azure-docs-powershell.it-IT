---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiSchema.md
ms.openlocfilehash: 7ac8d0b243f70d9e0f02c620febc7062f0c2e3ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962509"
---
# <span data-ttu-id="29352-101">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="29352-101">New-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="29352-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29352-102">SYNOPSIS</span></span>
<span data-ttu-id="29352-103">Crea il nuovo schema API nel servizio ApiManagement</span><span class="sxs-lookup"><span data-stu-id="29352-103">Creates the new API Schema in the ApiManagement service</span></span>

## <span data-ttu-id="29352-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="29352-104">SYNTAX</span></span>

### <span data-ttu-id="29352-105">SchemaDocumentInline (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="29352-105">SchemaDocumentInline (Default)</span></span>
```
New-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 -SchemaDocumentContentType <String> -SchemaDocument <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29352-106">SchemaDocumentFromFile</span><span class="sxs-lookup"><span data-stu-id="29352-106">SchemaDocumentFromFile</span></span>
```
New-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 -SchemaDocumentContentType <String> -SchemaDocumentFilePath <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29352-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="29352-107">DESCRIPTION</span></span>
<span data-ttu-id="29352-108">Crea il nuovo schema API dell'API.</span><span class="sxs-lookup"><span data-stu-id="29352-108">Creates the new API Schema of the API.</span></span>

## <span data-ttu-id="29352-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="29352-109">EXAMPLES</span></span>

### <span data-ttu-id="29352-110">Esempio 1: Creare un nuovo schema per l'API Swagger Petstore Extensive</span><span class="sxs-lookup"><span data-stu-id="29352-110">Example 1: Create new Schema for Swagger Petstore Extensive API</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/resourceGroupName/providers/Microsoft.ApiManagement/service/sdktestapim4163
PS D:\github\azure-powershell> New-AzApiManagementApiSchema -Context $context -ApiId swagger-petstore-extensive -SchemaDocumentContentType swaggerdefinition -SchemaDocumentFilePath C:\Users\sasolank\Downloads\petstoreschema.json
Schema Id                            Api Id                     Schema ContentType
---------                            ------                     ------------------
3e8892eb-98e4-408d-b77a-f424185c1044 swagger-petstore-extensive swaggerdefinition
```

<span data-ttu-id="29352-111">Il cmdlet **New-AzApiManagementApiSchema** crea o aggiorna lo schema `swagger-petstore-extensive` dell'aPI.</span><span class="sxs-lookup"><span data-stu-id="29352-111">The cmdlet **New-AzApiManagementApiSchema** creates or updates the schema of the `swagger-petstore-extensive` aPI.</span></span>

## <span data-ttu-id="29352-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29352-112">PARAMETERS</span></span>

### <span data-ttu-id="29352-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="29352-113">-ApiId</span></span>
<span data-ttu-id="29352-114">Identificatore dell'api.</span><span class="sxs-lookup"><span data-stu-id="29352-114">Identifier of api.</span></span> <span data-ttu-id="29352-115">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="29352-115">This parameter is required.</span></span>

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

### <span data-ttu-id="29352-116">-Context</span><span class="sxs-lookup"><span data-stu-id="29352-116">-Context</span></span>
<span data-ttu-id="29352-117">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="29352-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="29352-118">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="29352-118">This parameter is required.</span></span>

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

### <span data-ttu-id="29352-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29352-119">-DefaultProfile</span></span>
<span data-ttu-id="29352-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="29352-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29352-121">-SchemaDocument</span><span class="sxs-lookup"><span data-stu-id="29352-121">-SchemaDocument</span></span>
<span data-ttu-id="29352-122">Api schema document as a string.</span><span class="sxs-lookup"><span data-stu-id="29352-122">Api schema document as a string.</span></span> <span data-ttu-id="29352-123">Questo parametro è obbligatorio: SchemaDocumentFile non è specificato.</span><span class="sxs-lookup"><span data-stu-id="29352-123">This parameter is required is -SchemaDocumentFile is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SchemaDocumentInline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29352-124">-SchemaDocumentContentType</span><span class="sxs-lookup"><span data-stu-id="29352-124">-SchemaDocumentContentType</span></span>
<span data-ttu-id="29352-125">ContentType dello schema api.</span><span class="sxs-lookup"><span data-stu-id="29352-125">ContentType of the api Schema.</span></span> <span data-ttu-id="29352-126">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="29352-126">This parameter is required.</span></span>

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

### <span data-ttu-id="29352-127">-SchemaDocumentFilePath</span><span class="sxs-lookup"><span data-stu-id="29352-127">-SchemaDocumentFilePath</span></span>
<span data-ttu-id="29352-128">Percorso del file del documento dello schema API.</span><span class="sxs-lookup"><span data-stu-id="29352-128">Api schema document file path.</span></span> <span data-ttu-id="29352-129">Questo parametro è obbligatorio. SchemaDocument non è specificato.</span><span class="sxs-lookup"><span data-stu-id="29352-129">This parameter is required is -SchemaDocument is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SchemaDocumentFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29352-130">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="29352-130">-SchemaId</span></span>
<span data-ttu-id="29352-131">Identificatore del nuovo schema.</span><span class="sxs-lookup"><span data-stu-id="29352-131">Identifier of new schema.</span></span>
<span data-ttu-id="29352-132">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="29352-132">This parameter is optional.</span></span>
<span data-ttu-id="29352-133">Se non viene specificato, verrà generato.</span><span class="sxs-lookup"><span data-stu-id="29352-133">If not specified will be generated.</span></span>

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

### <span data-ttu-id="29352-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="29352-134">-Confirm</span></span>
<span data-ttu-id="29352-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29352-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29352-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29352-136">-WhatIf</span></span>
<span data-ttu-id="29352-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="29352-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29352-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="29352-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29352-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29352-139">CommonParameters</span></span>
<span data-ttu-id="29352-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29352-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29352-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="29352-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29352-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="29352-142">INPUTS</span></span>

### <span data-ttu-id="29352-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="29352-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="29352-144">System.String</span><span class="sxs-lookup"><span data-stu-id="29352-144">System.String</span></span>

## <span data-ttu-id="29352-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="29352-145">OUTPUTS</span></span>

### <span data-ttu-id="29352-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="29352-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

## <span data-ttu-id="29352-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="29352-147">NOTES</span></span>

## <span data-ttu-id="29352-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="29352-148">RELATED LINKS</span></span>

[<span data-ttu-id="29352-149">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="29352-149">Get-AzApiManagementApiSchema</span></span>](./Get-AzApiManagementApiSchema.md)

[<span data-ttu-id="29352-150">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="29352-150">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

[<span data-ttu-id="29352-151">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="29352-151">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)
