---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2BA76B02-B786-4A77-86E0-E7D4191120B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/export-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
ms.openlocfilehash: 7b4163b18905fd0676543de1b0ead26d11c7096a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676094"
---
# <span data-ttu-id="204ce-101">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="204ce-101">Export-AzApiManagementApi</span></span>

## <span data-ttu-id="204ce-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="204ce-102">SYNOPSIS</span></span>
<span data-ttu-id="204ce-103">Esporta un'API in un file.</span><span class="sxs-lookup"><span data-stu-id="204ce-103">Exports an API to a file.</span></span>

## <span data-ttu-id="204ce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="204ce-104">SYNTAX</span></span>

### <span data-ttu-id="204ce-105">ExportToPipeline (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="204ce-105">ExportToPipeline (Default)</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="204ce-106">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="204ce-106">ExportToFile</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SaveAs <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="204ce-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="204ce-107">DESCRIPTION</span></span>
<span data-ttu-id="204ce-108">Il cmdlet **Export-AzApiManagementApi** Esporta un'API di gestione API di Azure in un file in uno dei formati supportati.</span><span class="sxs-lookup"><span data-stu-id="204ce-108">The **Export-AzApiManagementApi** cmdlet exports an Azure API Management API to a file in one of the supported formats.</span></span>

## <span data-ttu-id="204ce-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="204ce-109">EXAMPLES</span></span>

### <span data-ttu-id="204ce-110">Esempio 1: esportare un'API nel formato WADL (Web Application Description Language)</span><span class="sxs-lookup"><span data-stu-id="204ce-110">Example 1: Export an API in Web Application Description Language (WADL) format</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Export-AzApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789" -SpecificationFormat "Wadl" -SaveAs "C:\contoso\specifications\0123456789.wadl"
```

<span data-ttu-id="204ce-111">Questo comando Esporta un'API in un file WADL.</span><span class="sxs-lookup"><span data-stu-id="204ce-111">This command exports an API to a WADL file.</span></span>

## <span data-ttu-id="204ce-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="204ce-112">PARAMETERS</span></span>

### <span data-ttu-id="204ce-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="204ce-113">-ApiId</span></span>
<span data-ttu-id="204ce-114">Specifica l'ID dell'API da esportare.</span><span class="sxs-lookup"><span data-stu-id="204ce-114">Specifies the ID of the API to export.</span></span>

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

### <span data-ttu-id="204ce-115">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="204ce-115">-ApiRevision</span></span>
<span data-ttu-id="204ce-116">Identificatore della revisione API.</span><span class="sxs-lookup"><span data-stu-id="204ce-116">Identifier of API Revision.</span></span> <span data-ttu-id="204ce-117">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="204ce-117">This parameter is optional.</span></span> <span data-ttu-id="204ce-118">Se non specificato, l'esportazione verrà eseguita per la revisione API attualmente attiva.</span><span class="sxs-lookup"><span data-stu-id="204ce-118">If not specified, the export will be done for the currently active api revision.</span></span>

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

### <span data-ttu-id="204ce-119">-Contesto</span><span class="sxs-lookup"><span data-stu-id="204ce-119">-Context</span></span>
<span data-ttu-id="204ce-120">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="204ce-120">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="204ce-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="204ce-121">-DefaultProfile</span></span>
<span data-ttu-id="204ce-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="204ce-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="204ce-123">-Force</span><span class="sxs-lookup"><span data-stu-id="204ce-123">-Force</span></span>
<span data-ttu-id="204ce-124">Indica che questa operazione sovrascrive il file con lo stesso nome se esiste già.</span><span class="sxs-lookup"><span data-stu-id="204ce-124">Indicates that this operation overwrites the file of the same name if it already exists.</span></span>

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

### <span data-ttu-id="204ce-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="204ce-125">-PassThru</span></span>
<span data-ttu-id="204ce-126">Indica che questa operazione restituisce $True se l'API viene esportata correttamente o $False in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="204ce-126">Indicates that this operation returns $True if the API is exported successfully, or $False otherwise.</span></span>

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

### <span data-ttu-id="204ce-127">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="204ce-127">-SaveAs</span></span>
<span data-ttu-id="204ce-128">Specifica il percorso del file in cui salvare l'API esportata.</span><span class="sxs-lookup"><span data-stu-id="204ce-128">Specifies the file path to which to save the exported API.</span></span>

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

### <span data-ttu-id="204ce-129">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="204ce-129">-SpecificationFormat</span></span>
<span data-ttu-id="204ce-130">Specifica il formato dell'API.</span><span class="sxs-lookup"><span data-stu-id="204ce-130">Specifies the API format.</span></span>
<span data-ttu-id="204ce-131">psdx_paramvalues Wadl e spavalderia.</span><span class="sxs-lookup"><span data-stu-id="204ce-131">psdx_paramvalues Wadl and Swagger.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat
Parameter Sets: (All)
Aliases:
Accepted values: Wadl, Swagger, Wsdl, OpenApi

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="204ce-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="204ce-132">-Confirm</span></span>
<span data-ttu-id="204ce-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="204ce-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="204ce-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="204ce-134">-WhatIf</span></span>
<span data-ttu-id="204ce-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="204ce-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="204ce-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="204ce-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="204ce-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="204ce-137">CommonParameters</span></span>
<span data-ttu-id="204ce-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="204ce-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="204ce-139">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="204ce-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="204ce-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="204ce-140">INPUTS</span></span>

### <span data-ttu-id="204ce-141">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="204ce-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="204ce-142">System. String</span><span class="sxs-lookup"><span data-stu-id="204ce-142">System.String</span></span>

### <span data-ttu-id="204ce-143">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="204ce-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="204ce-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="204ce-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="204ce-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="204ce-145">OUTPUTS</span></span>

### <span data-ttu-id="204ce-146">System. String</span><span class="sxs-lookup"><span data-stu-id="204ce-146">System.String</span></span>

## <span data-ttu-id="204ce-147">Note</span><span class="sxs-lookup"><span data-stu-id="204ce-147">NOTES</span></span>

## <span data-ttu-id="204ce-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="204ce-148">RELATED LINKS</span></span>

[<span data-ttu-id="204ce-149">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="204ce-149">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="204ce-150">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="204ce-150">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="204ce-151">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="204ce-151">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="204ce-152">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="204ce-152">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="204ce-153">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="204ce-153">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)

