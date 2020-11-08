---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2BA76B02-B786-4A77-86E0-E7D4191120B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/export-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
ms.openlocfilehash: 3981d1fd0a921f467007afc85c00b726b6037fad
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019917"
---
# <span data-ttu-id="dd25d-101">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="dd25d-101">Export-AzApiManagementApi</span></span>

## <span data-ttu-id="dd25d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dd25d-102">SYNOPSIS</span></span>
<span data-ttu-id="dd25d-103">Esporta un'API in un file.</span><span class="sxs-lookup"><span data-stu-id="dd25d-103">Exports an API to a file.</span></span>

## <span data-ttu-id="dd25d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dd25d-104">SYNTAX</span></span>

### <span data-ttu-id="dd25d-105">ExportToPipeline (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dd25d-105">ExportToPipeline (Default)</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd25d-106">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="dd25d-106">ExportToFile</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SaveAs <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd25d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dd25d-107">DESCRIPTION</span></span>
<span data-ttu-id="dd25d-108">Il cmdlet **Export-AzApiManagementApi** Esporta un'API di gestione API di Azure in un file in uno dei formati supportati.</span><span class="sxs-lookup"><span data-stu-id="dd25d-108">The **Export-AzApiManagementApi** cmdlet exports an Azure API Management API to a file in one of the supported formats.</span></span>

## <span data-ttu-id="dd25d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dd25d-109">EXAMPLES</span></span>

### <span data-ttu-id="dd25d-110">Esempio 1: esportare un'API nel formato WADL (Web Application Description Language)</span><span class="sxs-lookup"><span data-stu-id="dd25d-110">Example 1: Export an API in Web Application Description Language (WADL) format</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Export-AzApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789" -SpecificationFormat "Wadl" -SaveAs "C:\contoso\specifications\0123456789.wadl"
```

<span data-ttu-id="dd25d-111">Questo comando Esporta un'API in un file WADL.</span><span class="sxs-lookup"><span data-stu-id="dd25d-111">This command exports an API to a WADL file.</span></span>

### <span data-ttu-id="dd25d-112">Esempio 2: esportare un'API nel formato di specifica di OpenApi 3,0 come documento JSON</span><span class="sxs-lookup"><span data-stu-id="dd25d-112">Example 2: Export an API in OpenApi 3.0 Specification Format as Json Document</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Export-AzApiManagementApi -Context $context -ApiId swagger-petstore -SpecificationFormat OpenApiJson -SaveAs D:\github\petstore.json
```

<span data-ttu-id="dd25d-113">Questo comando Esporta le definizioni delle API in formato API aperto come documento JSON</span><span class="sxs-lookup"><span data-stu-id="dd25d-113">This command exports an API definitions in Open Api format as Json document</span></span>

## <span data-ttu-id="dd25d-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dd25d-114">PARAMETERS</span></span>

### <span data-ttu-id="dd25d-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="dd25d-115">-ApiId</span></span>
<span data-ttu-id="dd25d-116">Specifica l'ID dell'API da esportare.</span><span class="sxs-lookup"><span data-stu-id="dd25d-116">Specifies the ID of the API to export.</span></span>

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

### <span data-ttu-id="dd25d-117">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="dd25d-117">-ApiRevision</span></span>
<span data-ttu-id="dd25d-118">Identificatore della revisione API.</span><span class="sxs-lookup"><span data-stu-id="dd25d-118">Identifier of API Revision.</span></span> <span data-ttu-id="dd25d-119">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="dd25d-119">This parameter is optional.</span></span> <span data-ttu-id="dd25d-120">Se non specificato, l'esportazione verrà eseguita per la revisione API attualmente attiva.</span><span class="sxs-lookup"><span data-stu-id="dd25d-120">If not specified, the export will be done for the currently active api revision.</span></span>

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

### <span data-ttu-id="dd25d-121">-Contesto</span><span class="sxs-lookup"><span data-stu-id="dd25d-121">-Context</span></span>
<span data-ttu-id="dd25d-122">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="dd25d-122">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd25d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd25d-123">-DefaultProfile</span></span>
<span data-ttu-id="dd25d-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dd25d-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd25d-125">-Force</span><span class="sxs-lookup"><span data-stu-id="dd25d-125">-Force</span></span>
<span data-ttu-id="dd25d-126">Indica che questa operazione sovrascrive il file con lo stesso nome se esiste già.</span><span class="sxs-lookup"><span data-stu-id="dd25d-126">Indicates that this operation overwrites the file of the same name if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExportToFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd25d-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd25d-127">-PassThru</span></span>
<span data-ttu-id="dd25d-128">Indica che questa operazione restituisce $True se l'API viene esportata correttamente o $False in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="dd25d-128">Indicates that this operation returns $True if the API is exported successfully, or $False otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExportToFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd25d-129">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="dd25d-129">-SaveAs</span></span>
<span data-ttu-id="dd25d-130">Specifica il percorso del file in cui salvare l'API esportata.</span><span class="sxs-lookup"><span data-stu-id="dd25d-130">Specifies the file path to which to save the exported API.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportToFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd25d-131">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="dd25d-131">-SpecificationFormat</span></span>
<span data-ttu-id="dd25d-132">Specifica il formato dell'API.</span><span class="sxs-lookup"><span data-stu-id="dd25d-132">Specifies the API format.</span></span>
<span data-ttu-id="dd25d-133">psdx_paramvalues Wadl, WSDL, spavalderia, OpenApi e OpenApiJson</span><span class="sxs-lookup"><span data-stu-id="dd25d-133">psdx_paramvalues Wadl, Wsdl, Swagger, OpenApi and OpenApiJson</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat
Parameter Sets: (All)
Aliases:
Accepted values: Wadl, Swagger, Wsdl, OpenApi, OpenApiJson

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd25d-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dd25d-134">-Confirm</span></span>
<span data-ttu-id="dd25d-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd25d-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd25d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd25d-136">-WhatIf</span></span>
<span data-ttu-id="dd25d-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dd25d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd25d-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dd25d-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd25d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd25d-139">CommonParameters</span></span>
<span data-ttu-id="dd25d-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd25d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd25d-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd25d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd25d-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dd25d-142">INPUTS</span></span>

### <span data-ttu-id="dd25d-143">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="dd25d-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="dd25d-144">System. String</span><span class="sxs-lookup"><span data-stu-id="dd25d-144">System.String</span></span>

### <span data-ttu-id="dd25d-145">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="dd25d-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="dd25d-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="dd25d-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="dd25d-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dd25d-147">OUTPUTS</span></span>

### <span data-ttu-id="dd25d-148">System. String</span><span class="sxs-lookup"><span data-stu-id="dd25d-148">System.String</span></span>

## <span data-ttu-id="dd25d-149">Note</span><span class="sxs-lookup"><span data-stu-id="dd25d-149">NOTES</span></span>

## <span data-ttu-id="dd25d-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dd25d-150">RELATED LINKS</span></span>

[<span data-ttu-id="dd25d-151">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="dd25d-151">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="dd25d-152">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="dd25d-152">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="dd25d-153">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="dd25d-153">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="dd25d-154">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="dd25d-154">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="dd25d-155">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="dd25d-155">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


