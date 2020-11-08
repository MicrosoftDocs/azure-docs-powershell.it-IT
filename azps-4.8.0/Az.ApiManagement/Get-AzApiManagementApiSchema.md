---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiSchema.md
ms.openlocfilehash: 837494b8f042d3ea788eda69d47845b02859c805
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190631"
---
# <span data-ttu-id="83b2d-101">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="83b2d-101">Get-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="83b2d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="83b2d-102">SYNOPSIS</span></span>
<span data-ttu-id="83b2d-103">Ottenere i dettagli dello schema API</span><span class="sxs-lookup"><span data-stu-id="83b2d-103">Get the details of the API Schema</span></span>

## <span data-ttu-id="83b2d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="83b2d-104">SYNTAX</span></span>

### <span data-ttu-id="83b2d-105">ContextParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="83b2d-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83b2d-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="83b2d-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiSchema -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="83b2d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="83b2d-107">DESCRIPTION</span></span>
<span data-ttu-id="83b2d-108">Il cmdlet **Get-AzApiManagementApiSchema** ottiene i dettagli dello schema API</span><span class="sxs-lookup"><span data-stu-id="83b2d-108">The **Get-AzApiManagementApiSchema** cmdlet gets the details of the API Schema</span></span>

## <span data-ttu-id="83b2d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="83b2d-109">EXAMPLES</span></span>

### <span data-ttu-id="83b2d-110">Esempio 1: ottenere i dettagli di tutti gli schemi API di un'API</span><span class="sxs-lookup"><span data-stu-id="83b2d-110">Example 1: Get the details of all the Api Schema of an Api</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/resourceGroupName/providers/Microsoft.ApiManagement/service/sdktestapim4163
PS D:\github\azure-powershell> Get-AzApiManagementApiSchema -Context $context -ApiId wsdlapitest

SchemaId           : 2a03e1b4-1826-4e59-b372-4711f575db28
Api Id             : wsdlapitest
Schema ContentType : xsdschema
Schema Document    : <s:schema elementFormDefault="qualified"....

SchemaId           : b6e5497d-f65a-4851-9f5b-b5684cdae688
Api Id             : wsdlapitest
Schema ContentType : xsdschema
Schema Document    : <?xml version=""1.0"" encoding=""UTF-8""....
```

<span data-ttu-id="83b2d-111">Questo comando consente di ottenere tutti gli schemi API associati a un'API `swagger-petstore-extensive` per un contesto ApiManagement specifico.</span><span class="sxs-lookup"><span data-stu-id="83b2d-111">This command gets all the API schemas associated with an Api `swagger-petstore-extensive` for particular ApiManagement Context.</span></span>

### <span data-ttu-id="83b2d-112">Esempio 2: ottenere lo schema specifico associato a un'API</span><span class="sxs-lookup"><span data-stu-id="83b2d-112">Example 2: Get the specific schema associated with an Api</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/resourceGroupName/providers/Microsoft.ApiManagement/service/sdktestapim4163
PS D:\github\azure-powershell> Get-AzApiManagementApiSchema -Context $context -ApiId swagger-petstore-extensive -SchemaId 5cc9cf67e6ed3b1154e638bd

SchemaId           : 5cc9cf67e6ed3b1154e638bd
Api Id             : swagger-petstore-extensive
Schema ContentType : swaggerdefinition
Schema Document    : {
                       "definitions": {
                         "pet": {
                        ....
```

<span data-ttu-id="83b2d-113">Questo comando ottiene lo schema API `5cc9cf67e6ed3b1154e638bd` associato a un'API `swagger-petstore-extensive` per un contesto ApiManagement specifico.</span><span class="sxs-lookup"><span data-stu-id="83b2d-113">This command gets the API schema `5cc9cf67e6ed3b1154e638bd` associated with an Api `swagger-petstore-extensive` for particular ApiManagement Context.</span></span>

## <span data-ttu-id="83b2d-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="83b2d-114">PARAMETERS</span></span>

### <span data-ttu-id="83b2d-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="83b2d-115">-ApiId</span></span>
<span data-ttu-id="83b2d-116">Identificatore API da cercare.</span><span class="sxs-lookup"><span data-stu-id="83b2d-116">API identifier to look for.</span></span>
<span data-ttu-id="83b2d-117">Se specificato cercherà di ottenere l'API dall'ID.</span><span class="sxs-lookup"><span data-stu-id="83b2d-117">If specified will try to get the API by the Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83b2d-118">-Contesto</span><span class="sxs-lookup"><span data-stu-id="83b2d-118">-Context</span></span>
<span data-ttu-id="83b2d-119">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="83b2d-119">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="83b2d-120">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="83b2d-120">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83b2d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83b2d-121">-DefaultProfile</span></span>
<span data-ttu-id="83b2d-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="83b2d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83b2d-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="83b2d-123">-ResourceId</span></span>
<span data-ttu-id="83b2d-124">Identificatore delle risorse ARM di uno schema API.</span><span class="sxs-lookup"><span data-stu-id="83b2d-124">Arm Resource Identifier of a Api Schema.</span></span> <span data-ttu-id="83b2d-125">Se specificato cercherà di trovare lo schema API dall'identificatore.</span><span class="sxs-lookup"><span data-stu-id="83b2d-125">If specified will try to find api schema by the identifier.</span></span> <span data-ttu-id="83b2d-126">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="83b2d-126">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83b2d-127">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="83b2d-127">-SchemaId</span></span>
<span data-ttu-id="83b2d-128">Identificatore dello schema.</span><span class="sxs-lookup"><span data-stu-id="83b2d-128">The identifier of the Schema.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83b2d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83b2d-129">CommonParameters</span></span>
<span data-ttu-id="83b2d-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83b2d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83b2d-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="83b2d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83b2d-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="83b2d-132">INPUTS</span></span>

### <span data-ttu-id="83b2d-133">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="83b2d-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="83b2d-134">System. String</span><span class="sxs-lookup"><span data-stu-id="83b2d-134">System.String</span></span>

## <span data-ttu-id="83b2d-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="83b2d-135">OUTPUTS</span></span>

### <span data-ttu-id="83b2d-136">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="83b2d-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

## <span data-ttu-id="83b2d-137">Note</span><span class="sxs-lookup"><span data-stu-id="83b2d-137">NOTES</span></span>

## <span data-ttu-id="83b2d-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="83b2d-138">RELATED LINKS</span></span>

[<span data-ttu-id="83b2d-139">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="83b2d-139">New-AzApiManagementApiSchema</span></span>](./New-AzApiManagementApiSchema.md)

[<span data-ttu-id="83b2d-140">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="83b2d-140">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

[<span data-ttu-id="83b2d-141">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="83b2d-141">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)