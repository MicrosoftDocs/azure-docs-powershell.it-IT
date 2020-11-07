---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/get-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Get-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Get-AzHealthcareApisService.md
ms.openlocfilehash: d1a6edc3365631f93d2bc3b7a0e153ec360c2611
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864326"
---
# <span data-ttu-id="3905a-101">Get-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="3905a-101">Get-AzHealthcareApisService</span></span>

## <span data-ttu-id="3905a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3905a-102">SYNOPSIS</span></span>
<span data-ttu-id="3905a-103">Ottenere i metadati di un'istanza di servizio.</span><span class="sxs-lookup"><span data-stu-id="3905a-103">Get the metadata of a service instance.</span></span>

## <span data-ttu-id="3905a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3905a-104">SYNTAX</span></span>

### <span data-ttu-id="3905a-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3905a-105">ListParameterSet (Default)</span></span>
```
Get-AzHealthcareApisService [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3905a-106">ServiceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3905a-106">ServiceNameParameterSet</span></span>
```
Get-AzHealthcareApisService -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3905a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3905a-107">ResourceIdParameterSet</span></span>
```
Get-AzHealthcareApisService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3905a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3905a-108">DESCRIPTION</span></span>
<span data-ttu-id="3905a-109">Ottiene gli account di servizio di healthcareApis Fhir esistenti creati nell'abbonamento specificato o in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3905a-109">Gets existing healthcareApis fhir service accounts created within the specified subscription or a resource group.</span></span>

## <span data-ttu-id="3905a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3905a-110">EXAMPLES</span></span>

### <span data-ttu-id="3905a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3905a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzHealthcareApisService -Name "MyService" -ResourceGroupName "MyResourceGroup"

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False
```

### <span data-ttu-id="3905a-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3905a-112">Example 2</span></span>

<span data-ttu-id="3905a-113">Ottiene i metadati per tutti i servizi di HealthcareApis nel gruppo di risorse fornito.</span><span class="sxs-lookup"><span data-stu-id="3905a-113">Gets the metadata for all HealthcareApis services in the provided Resource Group.</span></span>

```powershell
PS C:\> Get-AzHealthcareApisService -ResourceGroupName "MyResourceGroup"

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db48
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db478
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService1
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService1
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False
```

### <span data-ttu-id="3905a-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="3905a-114">Example 3</span></span>

<span data-ttu-id="3905a-115">Ottiene i metadati per tutti i servizi di HealthcareApis nella sottoscrizione specificata</span><span class="sxs-lookup"><span data-stu-id="3905a-115">Gets the metadata for all HealthcareApis services in the given subscription</span></span>

```powershell
PS C:\> Get-AzHealthcareApisService

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db48
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db478
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService1
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService1
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False
```

## <span data-ttu-id="3905a-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3905a-116">PARAMETERS</span></span>

### <span data-ttu-id="3905a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3905a-117">-DefaultProfile</span></span>
<span data-ttu-id="3905a-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3905a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3905a-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="3905a-119">-Name</span></span>
<span data-ttu-id="3905a-120">Nome servizio HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="3905a-120">HealthcareApis Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases: HealthcareApisName, FhirServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3905a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3905a-121">-ResourceGroupName</span></span>
<span data-ttu-id="3905a-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3905a-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3905a-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3905a-123">-ResourceId</span></span>
<span data-ttu-id="3905a-124">Nome ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="3905a-124">Resource Id Name.</span></span>

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

### <span data-ttu-id="3905a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3905a-125">CommonParameters</span></span>
<span data-ttu-id="3905a-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3905a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3905a-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3905a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3905a-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3905a-128">INPUTS</span></span>

### <span data-ttu-id="3905a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="3905a-129">System.String</span></span>

## <span data-ttu-id="3905a-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3905a-130">OUTPUTS</span></span>

### <span data-ttu-id="3905a-131">Microsoft. Azure. Commands. HealthcareApisService. Models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="3905a-131">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="3905a-132">Note</span><span class="sxs-lookup"><span data-stu-id="3905a-132">NOTES</span></span>

## <span data-ttu-id="3905a-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3905a-133">RELATED LINKS</span></span>
