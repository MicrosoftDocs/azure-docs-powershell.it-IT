---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 48C143BE-3BF6-43E3-99B0-1A1D12A0A3F3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementApi.md
ms.openlocfilehash: a95aa5cf5d78d2540fe2816cfa4b044502c69b0f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517244"
---
# <span data-ttu-id="4ca10-101">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4ca10-101">Import-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="4ca10-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4ca10-102">SYNOPSIS</span></span>
<span data-ttu-id="4ca10-103">Importa un'API da un file o da un URL.</span><span class="sxs-lookup"><span data-stu-id="4ca10-103">Imports an API from a file or a URL.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ca10-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4ca10-104">SYNTAX</span></span>

### <span data-ttu-id="4ca10-105">Da file locale (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4ca10-105">From Local File (Default)</span></span>
```
Import-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationPath <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ca10-106">Da URL</span><span class="sxs-lookup"><span data-stu-id="4ca10-106">From URL</span></span>
```
Import-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationUrl <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ca10-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4ca10-107">DESCRIPTION</span></span>
<span data-ttu-id="4ca10-108">Il cmdlet **Import-AzureRmApiManagementApi** importa un'API di gestione delle API di Azure da un file o un URL nel linguaggio Wadl (Web Application Description Language), WSDL (Web Services Description Language) o in formato spavalderia.</span><span class="sxs-lookup"><span data-stu-id="4ca10-108">The **Import-AzureRmApiManagementApi** cmdlet imports an Azure API Management API from a file or a URL in Web Application Description Language (WADL), Web Services Description Language (WSDL), or Swagger format.</span></span>

## <span data-ttu-id="4ca10-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4ca10-109">EXAMPLES</span></span>

### <span data-ttu-id="4ca10-110">Esempio 1 importare un'API da un file WADL</span><span class="sxs-lookup"><span data-stu-id="4ca10-110">Example 1 Import an API from a WADL file</span></span>
```
PS C:\>Import-AzureRmApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationPath "C:\contoso\specifications\echoapi.wadl" -Path "apis"
```

<span data-ttu-id="4ca10-111">Questo comando importa un'API dal file WADL specificato.</span><span class="sxs-lookup"><span data-stu-id="4ca10-111">This command imports an API from the specified WADL file.</span></span>

### <span data-ttu-id="4ca10-112">Esempio 2 importare un'API da un file di spavalderia</span><span class="sxs-lookup"><span data-stu-id="4ca10-112">Example 2 Import an API from a Swagger file</span></span>
```
PS C:\>Import-AzureRmApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Swagger" -SpecificationPath "C:\contoso\specifications\echoapi.swagger" -Path "apis"
```

<span data-ttu-id="4ca10-113">Questo comando importa un'API dal file di spavalderia specificato.</span><span class="sxs-lookup"><span data-stu-id="4ca10-113">This command imports an API from the specified Swagger file.</span></span>

### <span data-ttu-id="4ca10-114">Esempio 3: importare un'API da un collegamento a WADL</span><span class="sxs-lookup"><span data-stu-id="4ca10-114">Example 3: Import an API from a WADL link</span></span>
```
PS C:\>Import-AzureRmApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationUrl "http://contoso.com/specifications/wadl/echoapi" -Path "apis"
```

<span data-ttu-id="4ca10-115">Questo comando importa un'API dal collegamento WADL specificato.</span><span class="sxs-lookup"><span data-stu-id="4ca10-115">This command imports an API from the specified WADL link.</span></span>

## <span data-ttu-id="4ca10-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4ca10-116">PARAMETERS</span></span>

### <span data-ttu-id="4ca10-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="4ca10-117">-ApiId</span></span>
<span data-ttu-id="4ca10-118">Specifica un ID per l'API da importare.</span><span class="sxs-lookup"><span data-stu-id="4ca10-118">Specifies an ID for the API to import.</span></span>
<span data-ttu-id="4ca10-119">Se non specifichi questo parametro, viene generato un ID.</span><span class="sxs-lookup"><span data-stu-id="4ca10-119">If you do not specify this parameter, an ID is generated for you.</span></span>

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

### <span data-ttu-id="4ca10-120">-ApiType</span><span class="sxs-lookup"><span data-stu-id="4ca10-120">-ApiType</span></span>
<span data-ttu-id="4ca10-121">Questo parametro è facoltativo con un valore predefinito di http.</span><span class="sxs-lookup"><span data-stu-id="4ca10-121">This parameter is optional with a default value of Http.</span></span> <span data-ttu-id="4ca10-122">L'opzione SOAP è applicabile solo quando si importano WSDL e si crea un'API passthrough SOAP.</span><span class="sxs-lookup"><span data-stu-id="4ca10-122">The Soap option is only applicable when importing WSDL and will create a SOAP Passthrough API.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiType]
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Soap

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ca10-123">-Contesto</span><span class="sxs-lookup"><span data-stu-id="4ca10-123">-Context</span></span>
<span data-ttu-id="4ca10-124">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="4ca10-124">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="4ca10-125">-Path</span><span class="sxs-lookup"><span data-stu-id="4ca10-125">-Path</span></span>
<span data-ttu-id="4ca10-126">Specifica un percorso dell'API Web come ultima parte dell'URL pubblico dell'API.</span><span class="sxs-lookup"><span data-stu-id="4ca10-126">Specifies a web API path as the last part of the API's public URL.</span></span>
<span data-ttu-id="4ca10-127">Questo URL viene usato dagli utenti dell'API per l'invio di richieste al servizio Web.</span><span class="sxs-lookup"><span data-stu-id="4ca10-127">This URL is used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="4ca10-128">Deve essere lunga da 1 a 400 caratteri.</span><span class="sxs-lookup"><span data-stu-id="4ca10-128">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="4ca10-129">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="4ca10-129">The default value is $Null.</span></span>

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

### <span data-ttu-id="4ca10-130">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="4ca10-130">-SpecificationFormat</span></span>
<span data-ttu-id="4ca10-131">Specifica il formato della specifica.</span><span class="sxs-lookup"><span data-stu-id="4ca10-131">Specifies the specification format.</span></span>
<span data-ttu-id="4ca10-132">psdx_paramvalues Wadl, WSDL e spavalderia.</span><span class="sxs-lookup"><span data-stu-id="4ca10-132">psdx_paramvalues Wadl, Wsdl, and Swagger.</span></span>

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

### <span data-ttu-id="4ca10-133">-SpecificationPath</span><span class="sxs-lookup"><span data-stu-id="4ca10-133">-SpecificationPath</span></span>
<span data-ttu-id="4ca10-134">Specifica il percorso del file delle specifiche.</span><span class="sxs-lookup"><span data-stu-id="4ca10-134">Specifies the specification file path.</span></span>

```yaml
Type: System.String
Parameter Sets: From Local File
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ca10-135">-SpecificationUrl</span><span class="sxs-lookup"><span data-stu-id="4ca10-135">-SpecificationUrl</span></span>
<span data-ttu-id="4ca10-136">Specifica l'URL della specifica.</span><span class="sxs-lookup"><span data-stu-id="4ca10-136">Specifies the specification URL.</span></span>

```yaml
Type: System.String
Parameter Sets: From URL
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ca10-137">-WsdlEndpointName</span><span class="sxs-lookup"><span data-stu-id="4ca10-137">-WsdlEndpointName</span></span>
<span data-ttu-id="4ca10-138">Nome locale dell'endpoint WSDL (porta) da importare.</span><span class="sxs-lookup"><span data-stu-id="4ca10-138">Local name of WSDL Endpoint (port) to be imported.</span></span> <span data-ttu-id="4ca10-139">Deve essere lunga da 1 a 400 caratteri.</span><span class="sxs-lookup"><span data-stu-id="4ca10-139">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="4ca10-140">Questo parametro è facoltativo e necessario solo per l'importazione di WSDL.</span><span class="sxs-lookup"><span data-stu-id="4ca10-140">This parameter is optional and only required for importing Wsdl.</span></span> <span data-ttu-id="4ca10-141">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="4ca10-141">Default value is $null.</span></span>

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

### <span data-ttu-id="4ca10-142">-WsdlServiceName</span><span class="sxs-lookup"><span data-stu-id="4ca10-142">-WsdlServiceName</span></span>
<span data-ttu-id="4ca10-143">Nome locale del servizio WSDL da importare.</span><span class="sxs-lookup"><span data-stu-id="4ca10-143">Local name of WSDL Service to be imported.</span></span> <span data-ttu-id="4ca10-144">Deve essere lunga da 1 a 400 caratteri.</span><span class="sxs-lookup"><span data-stu-id="4ca10-144">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="4ca10-145">Questo parametro è facoltativo e necessario solo per l'importazione di WSDL.</span><span class="sxs-lookup"><span data-stu-id="4ca10-145">This parameter is optional and only required for importing Wsdl .</span></span> <span data-ttu-id="4ca10-146">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="4ca10-146">Default value is $null.</span></span>

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

### <span data-ttu-id="4ca10-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ca10-147">-DefaultProfile</span></span>
<span data-ttu-id="4ca10-148">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4ca10-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ca10-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ca10-149">CommonParameters</span></span>
<span data-ttu-id="4ca10-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ca10-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ca10-151">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ca10-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ca10-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4ca10-152">INPUTS</span></span>

## <span data-ttu-id="4ca10-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4ca10-153">OUTPUTS</span></span>

### <span data-ttu-id="4ca10-154">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4ca10-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>
<span data-ttu-id="4ca10-155">Questo cmdlet restituisce l'API importata come oggetto **PsApiManagementApi** .</span><span class="sxs-lookup"><span data-stu-id="4ca10-155">This cmdlet returns the imported API as a **PsApiManagementApi** object.</span></span>

## <span data-ttu-id="4ca10-156">Note</span><span class="sxs-lookup"><span data-stu-id="4ca10-156">NOTES</span></span>

## <span data-ttu-id="4ca10-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4ca10-157">RELATED LINKS</span></span>

[<span data-ttu-id="4ca10-158">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4ca10-158">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="4ca10-159">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4ca10-159">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="4ca10-160">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4ca10-160">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="4ca10-161">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4ca10-161">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="4ca10-162">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4ca10-162">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


