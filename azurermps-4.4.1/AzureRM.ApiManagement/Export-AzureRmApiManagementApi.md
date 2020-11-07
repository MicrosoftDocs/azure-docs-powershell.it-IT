---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 2BA76B02-B786-4A77-86E0-E7D4191120B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Export-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Export-AzureRmApiManagementApi.md
ms.openlocfilehash: 09400d3111ffb3fda232e1cbb71fd0aac063a74c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686876"
---
# <span data-ttu-id="237d7-101">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="237d7-101">Export-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="237d7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="237d7-102">SYNOPSIS</span></span>
<span data-ttu-id="237d7-103">Esporta un'API in un file.</span><span class="sxs-lookup"><span data-stu-id="237d7-103">Exports an API to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="237d7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="237d7-104">SYNTAX</span></span>

### <span data-ttu-id="237d7-105">Esporta in pipeline (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="237d7-105">Export to pipeline (Default)</span></span>
```
Export-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String>
 -SpecificationFormat <PsApiManagementApiFormat> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="237d7-106">Esporta in un file</span><span class="sxs-lookup"><span data-stu-id="237d7-106">Export to File</span></span>
```
Export-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String>
 -SpecificationFormat <PsApiManagementApiFormat> -SaveAs <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="237d7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="237d7-107">DESCRIPTION</span></span>
<span data-ttu-id="237d7-108">Il cmdlet **Export-AzureRmApiManagementApi** Esporta un'API di gestione API di Azure in un file in uno dei formati supportati.</span><span class="sxs-lookup"><span data-stu-id="237d7-108">The **Export-AzureRmApiManagementApi** cmdlet exports an Azure API Management API to a file in one of the supported formats.</span></span>

## <span data-ttu-id="237d7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="237d7-109">EXAMPLES</span></span>

### <span data-ttu-id="237d7-110">Esempio 1: esportare un'API nel formato WADL (Web Application Description Language)</span><span class="sxs-lookup"><span data-stu-id="237d7-110">Example 1: Export an API in Web Application Description Language (WADL) format</span></span>
```
PS C:\>Export-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789" -SpecificationFormat "Wadl" -SaveAs "C:\contoso\specifications\0123456789.wadl"
```

<span data-ttu-id="237d7-111">Questo comando Esporta un'API in un file WADL.</span><span class="sxs-lookup"><span data-stu-id="237d7-111">This command exports an API to a WADL file.</span></span>

## <span data-ttu-id="237d7-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="237d7-112">PARAMETERS</span></span>

### <span data-ttu-id="237d7-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="237d7-113">-ApiId</span></span>
<span data-ttu-id="237d7-114">Specifica l'ID dell'API da esportare.</span><span class="sxs-lookup"><span data-stu-id="237d7-114">Specifies the ID of the API to export.</span></span>

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

### <span data-ttu-id="237d7-115">-Contesto</span><span class="sxs-lookup"><span data-stu-id="237d7-115">-Context</span></span>
<span data-ttu-id="237d7-116">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="237d7-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="237d7-117">-Force</span><span class="sxs-lookup"><span data-stu-id="237d7-117">-Force</span></span>
<span data-ttu-id="237d7-118">Indica che questa operazione sovrascrive il file con lo stesso nome se esiste già.</span><span class="sxs-lookup"><span data-stu-id="237d7-118">Indicates that this operation overwrites the file of the same name if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Export to File
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="237d7-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="237d7-119">-PassThru</span></span>
<span data-ttu-id="237d7-120">Indica che questa operazione restituisce $True se l'API viene esportata correttamente o $False in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="237d7-120">Indicates that this operation returns $True if the API is exported successfully, or $False otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Export to File
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="237d7-121">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="237d7-121">-SaveAs</span></span>
<span data-ttu-id="237d7-122">Specifica il percorso del file in cui salvare l'API esportata.</span><span class="sxs-lookup"><span data-stu-id="237d7-122">Specifies the file path to which to save the exported API.</span></span>

```yaml
Type: System.String
Parameter Sets: Export to File
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="237d7-123">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="237d7-123">-SpecificationFormat</span></span>
<span data-ttu-id="237d7-124">Specifica il formato dell'API.</span><span class="sxs-lookup"><span data-stu-id="237d7-124">Specifies the API format.</span></span>
<span data-ttu-id="237d7-125">psdx_paramvalues Wadl e spavalderia.</span><span class="sxs-lookup"><span data-stu-id="237d7-125">psdx_paramvalues Wadl and Swagger.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat
Parameter Sets: (All)
Aliases: 
Accepted values: Wadl, Swagger, Wsdl

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="237d7-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="237d7-126">-Confirm</span></span>
<span data-ttu-id="237d7-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="237d7-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="237d7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="237d7-128">-WhatIf</span></span>
<span data-ttu-id="237d7-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="237d7-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="237d7-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="237d7-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="237d7-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="237d7-131">-DefaultProfile</span></span>
<span data-ttu-id="237d7-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="237d7-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="237d7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="237d7-133">CommonParameters</span></span>
<span data-ttu-id="237d7-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="237d7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="237d7-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="237d7-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="237d7-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="237d7-136">INPUTS</span></span>

## <span data-ttu-id="237d7-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="237d7-137">OUTPUTS</span></span>

### <span data-ttu-id="237d7-138">Stringa</span><span class="sxs-lookup"><span data-stu-id="237d7-138">String</span></span>
<span data-ttu-id="237d7-139">Questo cmdlet restituisce il contenuto dell'API esportato come stringa.</span><span class="sxs-lookup"><span data-stu-id="237d7-139">This cmdlet returns the exported API content as a string.</span></span>

## <span data-ttu-id="237d7-140">Note</span><span class="sxs-lookup"><span data-stu-id="237d7-140">NOTES</span></span>

## <span data-ttu-id="237d7-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="237d7-141">RELATED LINKS</span></span>

[<span data-ttu-id="237d7-142">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="237d7-142">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="237d7-143">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="237d7-143">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="237d7-144">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="237d7-144">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="237d7-145">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="237d7-145">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="237d7-146">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="237d7-146">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


