---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 48C143BE-3BF6-43E3-99B0-1A1D12A0A3F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/import-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Import-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Import-AzApiManagementApi.md
ms.openlocfilehash: 690ebbfb1bb3cca6de8feb1f199068510e41f1d5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673616"
---
# <span data-ttu-id="d8870-101">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d8870-101">Import-AzApiManagementApi</span></span>

## <span data-ttu-id="d8870-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d8870-102">SYNOPSIS</span></span>
<span data-ttu-id="d8870-103">Importa un'API da un file o da un URL.</span><span class="sxs-lookup"><span data-stu-id="d8870-103">Imports an API from a file or a URL.</span></span>

## <span data-ttu-id="d8870-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d8870-104">SYNTAX</span></span>

### <span data-ttu-id="d8870-105">ImportFromLocalFile (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d8870-105">ImportFromLocalFile (Default)</span></span>
```
Import-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationPath <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8870-106">ImportFromUrl</span><span class="sxs-lookup"><span data-stu-id="d8870-106">ImportFromUrl</span></span>
```
Import-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationUrl <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8870-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d8870-107">DESCRIPTION</span></span>
<span data-ttu-id="d8870-108">Il cmdlet **Import-AzApiManagementApi** importa un'API di gestione delle API di Azure da un file o un URL nel linguaggio Wadl (Web Application Description Language), WSDL (Web Services Description Language) o in formato spavalderia.</span><span class="sxs-lookup"><span data-stu-id="d8870-108">The **Import-AzApiManagementApi** cmdlet imports an Azure API Management API from a file or a URL in Web Application Description Language (WADL), Web Services Description Language (WSDL), or Swagger format.</span></span>

## <span data-ttu-id="d8870-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d8870-109">EXAMPLES</span></span>

### <span data-ttu-id="d8870-110">Esempio 1 importare un'API da un file WADL</span><span class="sxs-lookup"><span data-stu-id="d8870-110">Example 1 Import an API from a WADL file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationPath "C:\contoso\specifications\echoapi.wadl" -Path "apis"
```

<span data-ttu-id="d8870-111">Questo comando importa un'API dal file WADL specificato.</span><span class="sxs-lookup"><span data-stu-id="d8870-111">This command imports an API from the specified WADL file.</span></span>

### <span data-ttu-id="d8870-112">Esempio 2 importare un'API da un file di spavalderia</span><span class="sxs-lookup"><span data-stu-id="d8870-112">Example 2 Import an API from a Swagger file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Swagger" -SpecificationPath "C:\contoso\specifications\echoapi.swagger" -Path "apis"
```

<span data-ttu-id="d8870-113">Questo comando importa un'API dal file di spavalderia specificato.</span><span class="sxs-lookup"><span data-stu-id="d8870-113">This command imports an API from the specified Swagger file.</span></span>

### <span data-ttu-id="d8870-114">Esempio 3: importare un'API da un collegamento a WADL</span><span class="sxs-lookup"><span data-stu-id="d8870-114">Example 3: Import an API from a WADL link</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationUrl "http://contoso.com/specifications/wadl/echoapi" -Path "apis"
```

<span data-ttu-id="d8870-115">Questo comando importa un'API dal collegamento WADL specificato.</span><span class="sxs-lookup"><span data-stu-id="d8870-115">This command imports an API from the specified WADL link.</span></span>

## <span data-ttu-id="d8870-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d8870-116">PARAMETERS</span></span>

### <span data-ttu-id="d8870-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="d8870-117">-ApiId</span></span>
<span data-ttu-id="d8870-118">Specifica un ID per l'API da importare.</span><span class="sxs-lookup"><span data-stu-id="d8870-118">Specifies an ID for the API to import.</span></span>
<span data-ttu-id="d8870-119">Se non specifichi questo parametro, viene generato un ID.</span><span class="sxs-lookup"><span data-stu-id="d8870-119">If you do not specify this parameter, an ID is generated for you.</span></span>

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

### <span data-ttu-id="d8870-120">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="d8870-120">-ApiRevision</span></span>
<span data-ttu-id="d8870-121">Identificatore della revisione API.</span><span class="sxs-lookup"><span data-stu-id="d8870-121">Identifier of API Revision.</span></span> <span data-ttu-id="d8870-122">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d8870-122">This parameter is optional.</span></span> <span data-ttu-id="d8870-123">Se non specificato, l'importazione verrà eseguita nella revisione attualmente attiva o in una nuova API.</span><span class="sxs-lookup"><span data-stu-id="d8870-123">If not specified, the import will be done onto the currently active revision or a new api.</span></span>

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

### <span data-ttu-id="d8870-124">-ApiType</span><span class="sxs-lookup"><span data-stu-id="d8870-124">-ApiType</span></span>
<span data-ttu-id="d8870-125">Questo parametro è facoltativo con un valore predefinito di http.</span><span class="sxs-lookup"><span data-stu-id="d8870-125">This parameter is optional with a default value of Http.</span></span> <span data-ttu-id="d8870-126">L'opzione SOAP è applicabile solo quando si importano WSDL e si crea un'API passthrough SOAP.</span><span class="sxs-lookup"><span data-stu-id="d8870-126">The Soap option is only applicable when importing WSDL and will create a SOAP Passthrough API.</span></span>

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

### <span data-ttu-id="d8870-127">-Contesto</span><span class="sxs-lookup"><span data-stu-id="d8870-127">-Context</span></span>
<span data-ttu-id="d8870-128">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="d8870-128">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d8870-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8870-129">-DefaultProfile</span></span>
<span data-ttu-id="d8870-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d8870-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8870-131">-Path</span><span class="sxs-lookup"><span data-stu-id="d8870-131">-Path</span></span>
<span data-ttu-id="d8870-132">Specifica un percorso dell'API Web come ultima parte dell'URL pubblico dell'API.</span><span class="sxs-lookup"><span data-stu-id="d8870-132">Specifies a web API path as the last part of the API's public URL.</span></span>
<span data-ttu-id="d8870-133">Questo URL viene usato dagli utenti dell'API per l'invio di richieste al servizio Web.</span><span class="sxs-lookup"><span data-stu-id="d8870-133">This URL is used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="d8870-134">Deve essere lunga da 1 a 400 caratteri.</span><span class="sxs-lookup"><span data-stu-id="d8870-134">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="d8870-135">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="d8870-135">The default value is $Null.</span></span>

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

### <span data-ttu-id="d8870-136">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="d8870-136">-SpecificationFormat</span></span>
<span data-ttu-id="d8870-137">Specifica il formato della specifica.</span><span class="sxs-lookup"><span data-stu-id="d8870-137">Specifies the specification format.</span></span>
<span data-ttu-id="d8870-138">psdx_paramvalues Wadl, WSDL e spavalderia.</span><span class="sxs-lookup"><span data-stu-id="d8870-138">psdx_paramvalues Wadl, Wsdl, and Swagger.</span></span>

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

### <span data-ttu-id="d8870-139">-SpecificationPath</span><span class="sxs-lookup"><span data-stu-id="d8870-139">-SpecificationPath</span></span>
<span data-ttu-id="d8870-140">Specifica il percorso del file delle specifiche.</span><span class="sxs-lookup"><span data-stu-id="d8870-140">Specifies the specification file path.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportFromLocalFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8870-141">-SpecificationUrl</span><span class="sxs-lookup"><span data-stu-id="d8870-141">-SpecificationUrl</span></span>
<span data-ttu-id="d8870-142">Specifica l'URL della specifica.</span><span class="sxs-lookup"><span data-stu-id="d8870-142">Specifies the specification URL.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportFromUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8870-143">-WsdlEndpointName</span><span class="sxs-lookup"><span data-stu-id="d8870-143">-WsdlEndpointName</span></span>
<span data-ttu-id="d8870-144">Nome locale dell'endpoint WSDL (porta) da importare.</span><span class="sxs-lookup"><span data-stu-id="d8870-144">Local name of WSDL Endpoint (port) to be imported.</span></span> <span data-ttu-id="d8870-145">Deve essere lunga da 1 a 400 caratteri.</span><span class="sxs-lookup"><span data-stu-id="d8870-145">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="d8870-146">Questo parametro è facoltativo e necessario solo per l'importazione di WSDL.</span><span class="sxs-lookup"><span data-stu-id="d8870-146">This parameter is optional and only required for importing Wsdl.</span></span> <span data-ttu-id="d8870-147">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="d8870-147">Default value is $null.</span></span>

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

### <span data-ttu-id="d8870-148">-WsdlServiceName</span><span class="sxs-lookup"><span data-stu-id="d8870-148">-WsdlServiceName</span></span>
<span data-ttu-id="d8870-149">Nome locale del servizio WSDL da importare.</span><span class="sxs-lookup"><span data-stu-id="d8870-149">Local name of WSDL Service to be imported.</span></span> <span data-ttu-id="d8870-150">Deve essere lunga da 1 a 400 caratteri.</span><span class="sxs-lookup"><span data-stu-id="d8870-150">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="d8870-151">Questo parametro è facoltativo e necessario solo per l'importazione di WSDL.</span><span class="sxs-lookup"><span data-stu-id="d8870-151">This parameter is optional and only required for importing Wsdl .</span></span> <span data-ttu-id="d8870-152">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="d8870-152">Default value is $null.</span></span>

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

### <span data-ttu-id="d8870-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8870-153">CommonParameters</span></span>
<span data-ttu-id="d8870-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8870-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8870-155">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8870-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8870-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d8870-156">INPUTS</span></span>

### <span data-ttu-id="d8870-157">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d8870-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d8870-158">System. String</span><span class="sxs-lookup"><span data-stu-id="d8870-158">System.String</span></span>

### <span data-ttu-id="d8870-159">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="d8870-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="d8870-160">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiType, Microsoft. Azure. PowerShell. Cmdlets. ApiManagement. ServiceManagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d8870-160">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiType, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d8870-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d8870-161">OUTPUTS</span></span>

### <span data-ttu-id="d8870-162">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d8870-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="d8870-163">Note</span><span class="sxs-lookup"><span data-stu-id="d8870-163">NOTES</span></span>

## <span data-ttu-id="d8870-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d8870-164">RELATED LINKS</span></span>

[<span data-ttu-id="d8870-165">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d8870-165">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="d8870-166">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d8870-166">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="d8870-167">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d8870-167">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="d8870-168">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d8870-168">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="d8870-169">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d8870-169">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


