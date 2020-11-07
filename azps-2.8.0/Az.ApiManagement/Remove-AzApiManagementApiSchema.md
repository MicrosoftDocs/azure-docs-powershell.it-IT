---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiSchema.md
ms.openlocfilehash: 4fa05a0c3568d8d787a7b269cd0f26c0adc82d0f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675958"
---
# <span data-ttu-id="9d1b9-101">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="9d1b9-101">Remove-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="9d1b9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9d1b9-102">SYNOPSIS</span></span>
<span data-ttu-id="9d1b9-103">Rimuove lo schema API dall'API.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-103">Removes the API Schema from the API.</span></span>

## <span data-ttu-id="9d1b9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9d1b9-104">SYNTAX</span></span>

### <span data-ttu-id="9d1b9-105">ByApiSchemaId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9d1b9-105">ByApiSchemaId (Default)</span></span>
```
Remove-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> -SchemaId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d1b9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9d1b9-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiSchema -InputObject <PsApiManagementApiSchema> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d1b9-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d1b9-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementApiSchema -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d1b9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9d1b9-108">DESCRIPTION</span></span>
<span data-ttu-id="9d1b9-109">Cmdlet **Remove-AzApiManagementSchema** dall'API.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-109">The cmdlet **Remove-AzApiManagementSchema** from the Api.</span></span>

## <span data-ttu-id="9d1b9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9d1b9-110">EXAMPLES</span></span>

### <span data-ttu-id="9d1b9-111">Esempio 1: rimuove lo schema API dall'API</span><span class="sxs-lookup"><span data-stu-id="9d1b9-111">Example 1 : Removes the Api Schema from the API</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzAzureRmApiManagementApiSchema -Context $apimContext -ApiId "echo-api" -SchemaId "2"
```

<span data-ttu-id="9d1b9-112">Lo script rimuove lo schema `2` dall'API `echo-api` se non viene fatto riferimento.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-112">The script removes the Schema `2` from the Api `echo-api` if it is not referenced.</span></span>

## <span data-ttu-id="9d1b9-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9d1b9-113">PARAMETERS</span></span>

### <span data-ttu-id="9d1b9-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="9d1b9-114">-ApiId</span></span>
<span data-ttu-id="9d1b9-115">Identificatore dell'API.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-115">Identifier of the API.</span></span>
<span data-ttu-id="9d1b9-116">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-116">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiSchemaId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d1b9-117">-Contesto</span><span class="sxs-lookup"><span data-stu-id="9d1b9-117">-Context</span></span>
<span data-ttu-id="9d1b9-118">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="9d1b9-119">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ByApiSchemaId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d1b9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d1b9-120">-DefaultProfile</span></span>
<span data-ttu-id="9d1b9-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d1b9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9d1b9-122">-InputObject</span></span>
<span data-ttu-id="9d1b9-123">Istanza di PsApiManagementApiSchema.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-123">Instance of PsApiManagementApiSchema.</span></span>
<span data-ttu-id="9d1b9-124">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-124">This parameter is required.</span></span>

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

### <span data-ttu-id="9d1b9-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9d1b9-125">-PassThru</span></span>
<span data-ttu-id="9d1b9-126">Se specificato scriverà true nel caso in cui l'operazione venga eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="9d1b9-127">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="9d1b9-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d1b9-128">-ResourceId</span></span>
<span data-ttu-id="9d1b9-129">ResourceId ARM di ApiSchema.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-129">Arm ResourceId of ApiSchema.</span></span> <span data-ttu-id="9d1b9-130">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-130">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d1b9-131">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="9d1b9-131">-SchemaId</span></span>
<span data-ttu-id="9d1b9-132">Identificatore dello schema API.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-132">Identifier of the API Schema.</span></span>
<span data-ttu-id="9d1b9-133">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-133">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiSchemaId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d1b9-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9d1b9-134">-Confirm</span></span>
<span data-ttu-id="9d1b9-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d1b9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d1b9-136">-WhatIf</span></span>
<span data-ttu-id="9d1b9-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d1b9-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d1b9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d1b9-139">CommonParameters</span></span>
<span data-ttu-id="9d1b9-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d1b9-141">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9d1b9-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d1b9-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9d1b9-142">INPUTS</span></span>

### <span data-ttu-id="9d1b9-143">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9d1b9-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9d1b9-144">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="9d1b9-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

### <span data-ttu-id="9d1b9-145">System. String</span><span class="sxs-lookup"><span data-stu-id="9d1b9-145">System.String</span></span>

## <span data-ttu-id="9d1b9-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9d1b9-146">OUTPUTS</span></span>

### <span data-ttu-id="9d1b9-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9d1b9-147">System.Boolean</span></span>

## <span data-ttu-id="9d1b9-148">Note</span><span class="sxs-lookup"><span data-stu-id="9d1b9-148">NOTES</span></span>

## <span data-ttu-id="9d1b9-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9d1b9-149">RELATED LINKS</span></span>

[<span data-ttu-id="9d1b9-150">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="9d1b9-150">Get-AzApiManagementApiSchema</span></span>](./Get-AzApiManagementApiSchema.md)

[<span data-ttu-id="9d1b9-151">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="9d1b9-151">New-AzApiManagementApiSchema</span></span>](./New-AzApiManagementApiSchema.md)

[<span data-ttu-id="9d1b9-152">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="9d1b9-152">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)
