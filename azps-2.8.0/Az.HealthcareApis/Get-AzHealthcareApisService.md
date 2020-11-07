---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/get-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Get-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Get-AzHealthcareApisService.md
ms.openlocfilehash: 0f5aff6cfe499d9d0ef37d299babb178b437c2e0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674272"
---
# <span data-ttu-id="11f00-101">Get-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="11f00-101">Get-AzHealthcareApisService</span></span>

## <span data-ttu-id="11f00-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="11f00-102">SYNOPSIS</span></span>
<span data-ttu-id="11f00-103">Ottenere i metadati di un'istanza di servizio.</span><span class="sxs-lookup"><span data-stu-id="11f00-103">Get the metadata of a service instance.</span></span>

## <span data-ttu-id="11f00-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="11f00-104">SYNTAX</span></span>

### <span data-ttu-id="11f00-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="11f00-105">ListParameterSet (Default)</span></span>
```
Get-AzHealthcareApisService [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="11f00-106">ServiceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="11f00-106">ServiceNameParameterSet</span></span>
```
Get-AzHealthcareApisService -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11f00-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="11f00-107">ResourceIdParameterSet</span></span>
```
Get-AzHealthcareApisService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="11f00-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="11f00-108">DESCRIPTION</span></span>
<span data-ttu-id="11f00-109">Ottiene gli account di servizio di healthcareApis Fhir esistenti creati nell'abbonamento specificato o in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="11f00-109">Gets existing healthcareApis fhir service accounts created within the specified subscription or a resource group.</span></span>

## <span data-ttu-id="11f00-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="11f00-110">EXAMPLES</span></span>

### <span data-ttu-id="11f00-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="11f00-111">Example 1</span></span>
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

### <span data-ttu-id="11f00-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="11f00-112">Example 2</span></span>

<span data-ttu-id="11f00-113">Ottiene i metadati per tutti i servizi di HealthcareApis nel gruppo di risorse fornito.</span><span class="sxs-lookup"><span data-stu-id="11f00-113">Gets the metadata for all HealthcareApis services in the provided Resource Group.</span></span>

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

### <span data-ttu-id="11f00-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="11f00-114">Example 3</span></span>

<span data-ttu-id="11f00-115">Ottiene i metadati per tutti i servizi di HealthcareApis nella sottoscrizione specificata</span><span class="sxs-lookup"><span data-stu-id="11f00-115">Gets the metadata for all HealthcareApis services in the given subscription</span></span>

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

## <span data-ttu-id="11f00-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="11f00-116">PARAMETERS</span></span>

### <span data-ttu-id="11f00-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11f00-117">-DefaultProfile</span></span>
<span data-ttu-id="11f00-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="11f00-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11f00-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="11f00-119">-Name</span></span>
<span data-ttu-id="11f00-120">Nome servizio HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="11f00-120">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="11f00-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11f00-121">-ResourceGroupName</span></span>
<span data-ttu-id="11f00-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="11f00-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="11f00-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11f00-123">-ResourceId</span></span>
<span data-ttu-id="11f00-124">Nome ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="11f00-124">Resource Id Name.</span></span>

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

### <span data-ttu-id="11f00-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11f00-125">CommonParameters</span></span>
<span data-ttu-id="11f00-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11f00-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11f00-127">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="11f00-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11f00-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="11f00-128">INPUTS</span></span>

### <span data-ttu-id="11f00-129">System. String</span><span class="sxs-lookup"><span data-stu-id="11f00-129">System.String</span></span>

## <span data-ttu-id="11f00-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="11f00-130">OUTPUTS</span></span>

### <span data-ttu-id="11f00-131">Microsoft. Azure. Commands. HealthcareApisService. Models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="11f00-131">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="11f00-132">Note</span><span class="sxs-lookup"><span data-stu-id="11f00-132">NOTES</span></span>

## <span data-ttu-id="11f00-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="11f00-133">RELATED LINKS</span></span>
