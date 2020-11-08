---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiSchema.md
ms.openlocfilehash: ad931b574af8445947e9f3f4df12c35c2baa1bf7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020221"
---
# <span data-ttu-id="3efbc-101">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="3efbc-101">New-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="3efbc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3efbc-102">SYNOPSIS</span></span>
<span data-ttu-id="3efbc-103">Crea il nuovo schema API nel servizio ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3efbc-103">Creates the new API Schema in the ApiManagement service</span></span>

## <span data-ttu-id="3efbc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3efbc-104">SYNTAX</span></span>

### <span data-ttu-id="3efbc-105">SchemaDocumentInline (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3efbc-105">SchemaDocumentInline (Default)</span></span>
```
New-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 -SchemaDocumentContentType <String> -SchemaDocument <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3efbc-106">SchemaDocumentFromFile</span><span class="sxs-lookup"><span data-stu-id="3efbc-106">SchemaDocumentFromFile</span></span>
```
New-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 -SchemaDocumentContentType <String> -SchemaDocumentFilePath <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3efbc-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3efbc-107">DESCRIPTION</span></span>
<span data-ttu-id="3efbc-108">Crea il nuovo schema API dell'API.</span><span class="sxs-lookup"><span data-stu-id="3efbc-108">Creates the new API Schema of the API.</span></span>

## <span data-ttu-id="3efbc-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3efbc-109">EXAMPLES</span></span>

### <span data-ttu-id="3efbc-110">Esempio 1: creare un nuovo schema per l'API estesa petstore di spavalderia</span><span class="sxs-lookup"><span data-stu-id="3efbc-110">Example 1 : Create new Schema for Swagger Petstore Extensive API</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/resourceGroupName/providers/Microsoft.ApiManagement/service/sdktestapim4163
PS D:\github\azure-powershell> New-AzApiManagementApiSchema -Context $context -ApiId swagger-petstore-extensive -SchemaDocumentContentType swaggerdefinition -SchemaDocumentFilePath C:\Users\sasolank\Downloads\petstoreschema.json
Schema Id                            Api Id                     Schema ContentType
---------                            ------                     ------------------
3e8892eb-98e4-408d-b77a-f424185c1044 swagger-petstore-extensive swaggerdefinition
```

<span data-ttu-id="3efbc-111">Il cmdlet **New-AzApiManagementApiSchema** crea o aggiorna lo schema dell' `swagger-petstore-extensive` API.</span><span class="sxs-lookup"><span data-stu-id="3efbc-111">The cmdlet **New-AzApiManagementApiSchema** creates or updates the schema of the `swagger-petstore-extensive` aPI.</span></span>

## <span data-ttu-id="3efbc-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3efbc-112">PARAMETERS</span></span>

### <span data-ttu-id="3efbc-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="3efbc-113">-ApiId</span></span>
<span data-ttu-id="3efbc-114">Identificatore dell'API.</span><span class="sxs-lookup"><span data-stu-id="3efbc-114">Identifier of api.</span></span> <span data-ttu-id="3efbc-115">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="3efbc-115">This parameter is required.</span></span>

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

### <span data-ttu-id="3efbc-116">-Contesto</span><span class="sxs-lookup"><span data-stu-id="3efbc-116">-Context</span></span>
<span data-ttu-id="3efbc-117">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="3efbc-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="3efbc-118">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="3efbc-118">This parameter is required.</span></span>

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

### <span data-ttu-id="3efbc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3efbc-119">-DefaultProfile</span></span>
<span data-ttu-id="3efbc-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3efbc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3efbc-121">-SchemaDocument</span><span class="sxs-lookup"><span data-stu-id="3efbc-121">-SchemaDocument</span></span>
<span data-ttu-id="3efbc-122">Documento dello schema API come stringa.</span><span class="sxs-lookup"><span data-stu-id="3efbc-122">Api schema document as a string.</span></span> <span data-ttu-id="3efbc-123">Questo parametro è obbligatorio-SchemaDocumentFile non è specificato.</span><span class="sxs-lookup"><span data-stu-id="3efbc-123">This parameter is required is -SchemaDocumentFile is not specified.</span></span>

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

### <span data-ttu-id="3efbc-124">-SchemaDocumentContentType</span><span class="sxs-lookup"><span data-stu-id="3efbc-124">-SchemaDocumentContentType</span></span>
<span data-ttu-id="3efbc-125">ContentType dello schema API.</span><span class="sxs-lookup"><span data-stu-id="3efbc-125">ContentType of the api Schema.</span></span> <span data-ttu-id="3efbc-126">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="3efbc-126">This parameter is required.</span></span>

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

### <span data-ttu-id="3efbc-127">-SchemaDocumentFilePath</span><span class="sxs-lookup"><span data-stu-id="3efbc-127">-SchemaDocumentFilePath</span></span>
<span data-ttu-id="3efbc-128">Percorso file del documento dello schema API.</span><span class="sxs-lookup"><span data-stu-id="3efbc-128">Api schema document file path.</span></span> <span data-ttu-id="3efbc-129">Questo parametro è obbligatorio-SchemaDocument non è specificato.</span><span class="sxs-lookup"><span data-stu-id="3efbc-129">This parameter is required is -SchemaDocument is not specified.</span></span>

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

### <span data-ttu-id="3efbc-130">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="3efbc-130">-SchemaId</span></span>
<span data-ttu-id="3efbc-131">Identificatore del nuovo schema.</span><span class="sxs-lookup"><span data-stu-id="3efbc-131">Identifier of new schema.</span></span>
<span data-ttu-id="3efbc-132">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="3efbc-132">This parameter is optional.</span></span>
<span data-ttu-id="3efbc-133">Se non viene specificato verrà generato.</span><span class="sxs-lookup"><span data-stu-id="3efbc-133">If not specified will be generated.</span></span>

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

### <span data-ttu-id="3efbc-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3efbc-134">-Confirm</span></span>
<span data-ttu-id="3efbc-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3efbc-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3efbc-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3efbc-136">-WhatIf</span></span>
<span data-ttu-id="3efbc-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3efbc-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3efbc-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3efbc-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3efbc-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3efbc-139">CommonParameters</span></span>
<span data-ttu-id="3efbc-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3efbc-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3efbc-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3efbc-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3efbc-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3efbc-142">INPUTS</span></span>

### <span data-ttu-id="3efbc-143">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3efbc-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3efbc-144">System. String</span><span class="sxs-lookup"><span data-stu-id="3efbc-144">System.String</span></span>

## <span data-ttu-id="3efbc-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3efbc-145">OUTPUTS</span></span>

### <span data-ttu-id="3efbc-146">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="3efbc-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

## <span data-ttu-id="3efbc-147">Note</span><span class="sxs-lookup"><span data-stu-id="3efbc-147">NOTES</span></span>

## <span data-ttu-id="3efbc-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3efbc-148">RELATED LINKS</span></span>

[<span data-ttu-id="3efbc-149">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="3efbc-149">Get-AzApiManagementApiSchema</span></span>](./Get-AzApiManagementApiSchema.md)

[<span data-ttu-id="3efbc-150">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="3efbc-150">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

[<span data-ttu-id="3efbc-151">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="3efbc-151">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)
