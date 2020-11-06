---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 2BA76B02-B786-4A77-86E0-E7D4191120B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/export-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Export-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Export-AzureRmApiManagementApi.md
ms.openlocfilehash: 3985f393e642645ddf9f023756e78db20074c214
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93522095"
---
# <span data-ttu-id="cef79-101">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cef79-101">Export-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="cef79-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cef79-102">SYNOPSIS</span></span>
<span data-ttu-id="cef79-103">Esporta un'API in un file.</span><span class="sxs-lookup"><span data-stu-id="cef79-103">Exports an API to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cef79-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cef79-104">SYNTAX</span></span>

### <span data-ttu-id="cef79-105">ExportToPipeline (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cef79-105">ExportToPipeline (Default)</span></span>
```
Export-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String>
 -SpecificationFormat <PsApiManagementApiFormat> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cef79-106">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="cef79-106">ExportToFile</span></span>
```
Export-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String>
 -SpecificationFormat <PsApiManagementApiFormat> -SaveAs <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cef79-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cef79-107">DESCRIPTION</span></span>
<span data-ttu-id="cef79-108">Il cmdlet **Export-AzureRmApiManagementApi** Esporta un'API di gestione API di Azure in un file in uno dei formati supportati.</span><span class="sxs-lookup"><span data-stu-id="cef79-108">The **Export-AzureRmApiManagementApi** cmdlet exports an Azure API Management API to a file in one of the supported formats.</span></span>

## <span data-ttu-id="cef79-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cef79-109">EXAMPLES</span></span>

### <span data-ttu-id="cef79-110">Esempio 1: esportare un'API nel formato WADL (Web Application Description Language)</span><span class="sxs-lookup"><span data-stu-id="cef79-110">Example 1: Export an API in Web Application Description Language (WADL) format</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Export-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789" -SpecificationFormat "Wadl" -SaveAs "C:\contoso\specifications\0123456789.wadl"
```

<span data-ttu-id="cef79-111">Questo comando Esporta un'API in un file WADL.</span><span class="sxs-lookup"><span data-stu-id="cef79-111">This command exports an API to a WADL file.</span></span>

## <span data-ttu-id="cef79-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cef79-112">PARAMETERS</span></span>

### <span data-ttu-id="cef79-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="cef79-113">-ApiId</span></span>
<span data-ttu-id="cef79-114">Specifica l'ID dell'API da esportare.</span><span class="sxs-lookup"><span data-stu-id="cef79-114">Specifies the ID of the API to export.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cef79-115">-Contesto</span><span class="sxs-lookup"><span data-stu-id="cef79-115">-Context</span></span>
<span data-ttu-id="cef79-116">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="cef79-116">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cef79-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cef79-117">-DefaultProfile</span></span>
<span data-ttu-id="cef79-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cef79-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef79-119">-Force</span><span class="sxs-lookup"><span data-stu-id="cef79-119">-Force</span></span>
<span data-ttu-id="cef79-120">Indica che questa operazione sovrascrive il file con lo stesso nome se esiste già.</span><span class="sxs-lookup"><span data-stu-id="cef79-120">Indicates that this operation overwrites the file of the same name if it already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ExportToFile
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cef79-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cef79-121">-PassThru</span></span>
<span data-ttu-id="cef79-122">Indica che questa operazione restituisce $True se l'API viene esportata correttamente o $False in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="cef79-122">Indicates that this operation returns $True if the API is exported successfully, or $False otherwise.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ExportToFile
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cef79-123">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="cef79-123">-SaveAs</span></span>
<span data-ttu-id="cef79-124">Specifica il percorso del file in cui salvare l'API esportata.</span><span class="sxs-lookup"><span data-stu-id="cef79-124">Specifies the file path to which to save the exported API.</span></span>

```yaml
Type: String
Parameter Sets: ExportToFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cef79-125">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="cef79-125">-SpecificationFormat</span></span>
<span data-ttu-id="cef79-126">Specifica il formato dell'API.</span><span class="sxs-lookup"><span data-stu-id="cef79-126">Specifies the API format.</span></span>
<span data-ttu-id="cef79-127">psdx_paramvalues Wadl e spavalderia.</span><span class="sxs-lookup"><span data-stu-id="cef79-127">psdx_paramvalues Wadl and Swagger.</span></span>

```yaml
Type: PsApiManagementApiFormat
Parameter Sets: (All)
Aliases: 
Accepted values: Wadl, Swagger, Wsdl

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cef79-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cef79-128">-Confirm</span></span>
<span data-ttu-id="cef79-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cef79-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef79-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cef79-130">-WhatIf</span></span>
<span data-ttu-id="cef79-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cef79-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cef79-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cef79-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef79-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cef79-133">CommonParameters</span></span>
<span data-ttu-id="cef79-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cef79-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cef79-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cef79-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cef79-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cef79-136">INPUTS</span></span>

### <span data-ttu-id="cef79-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="cef79-137">None</span></span>
<span data-ttu-id="cef79-138">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="cef79-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cef79-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cef79-139">OUTPUTS</span></span>

### <span data-ttu-id="cef79-140">Stringa</span><span class="sxs-lookup"><span data-stu-id="cef79-140">String</span></span>
<span data-ttu-id="cef79-141">Questo cmdlet restituisce il contenuto dell'API esportato come stringa.</span><span class="sxs-lookup"><span data-stu-id="cef79-141">This cmdlet returns the exported API content as a string.</span></span>

## <span data-ttu-id="cef79-142">Note</span><span class="sxs-lookup"><span data-stu-id="cef79-142">NOTES</span></span>

## <span data-ttu-id="cef79-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cef79-143">RELATED LINKS</span></span>

[<span data-ttu-id="cef79-144">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cef79-144">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="cef79-145">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cef79-145">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="cef79-146">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cef79-146">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="cef79-147">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cef79-147">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="cef79-148">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cef79-148">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


