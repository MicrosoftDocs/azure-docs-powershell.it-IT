---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/get-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Get-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Get-AzHealthcareApisService.md
ms.openlocfilehash: 6d9c099457c25831d0ce97786b8d710cf4c0dc98
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200150"
---
# <span data-ttu-id="d60b9-101">Get-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="d60b9-101">Get-AzHealthcareApisService</span></span>

## <span data-ttu-id="d60b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d60b9-102">SYNOPSIS</span></span>
<span data-ttu-id="d60b9-103">Ottenere i metadati di un'istanza del servizio.</span><span class="sxs-lookup"><span data-stu-id="d60b9-103">Get the metadata of a service instance.</span></span>

## <span data-ttu-id="d60b9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d60b9-104">SYNTAX</span></span>

### <span data-ttu-id="d60b9-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d60b9-105">ListParameterSet (Default)</span></span>
```
Get-AzHealthcareApisService [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d60b9-106">ServiceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d60b9-106">ServiceNameParameterSet</span></span>
```
Get-AzHealthcareApisService -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d60b9-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d60b9-107">ResourceIdParameterSet</span></span>
```
Get-AzHealthcareApisService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d60b9-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d60b9-108">DESCRIPTION</span></span>
<span data-ttu-id="d60b9-109">Ottiene gli account del servizio healthcareApis esistenti creati nella sottoscrizione specificata o in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d60b9-109">Gets existing healthcareApis fhir service accounts created within the specified subscription or a resource group.</span></span>

## <span data-ttu-id="d60b9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d60b9-110">EXAMPLES</span></span>

### <span data-ttu-id="d60b9-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d60b9-111">Example 1</span></span>
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
CosmosDbKeyVaultKeyUri  :
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

### <span data-ttu-id="d60b9-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="d60b9-112">Example 2</span></span>

<span data-ttu-id="d60b9-113">Recupera i metadati per tutti i servizi HealthcareApis nel gruppo di risorse fornito.</span><span class="sxs-lookup"><span data-stu-id="d60b9-113">Gets the metadata for all HealthcareApis services in the provided Resource Group.</span></span>

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
CosmosDbKeyVaultKeyUri  :
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
CosmosDbKeyVaultKeyUri  :
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

### <span data-ttu-id="d60b9-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="d60b9-114">Example 3</span></span>

<span data-ttu-id="d60b9-115">Recupera i metadati per tutti i servizi HealthcareApis nella sottoscrizione specificata</span><span class="sxs-lookup"><span data-stu-id="d60b9-115">Gets the metadata for all HealthcareApis services in the given subscription</span></span>

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
CosmosDbKeyVaultKeyUri  :
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
CosmosDbKeyVaultKeyUri  :
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

## <span data-ttu-id="d60b9-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d60b9-116">PARAMETERS</span></span>

### <span data-ttu-id="d60b9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d60b9-117">-DefaultProfile</span></span>
<span data-ttu-id="d60b9-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d60b9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d60b9-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d60b9-119">-Name</span></span>
<span data-ttu-id="d60b9-120">Nome del servizio HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="d60b9-120">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="d60b9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d60b9-121">-ResourceGroupName</span></span>
<span data-ttu-id="d60b9-122">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d60b9-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="d60b9-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d60b9-123">-ResourceId</span></span>
<span data-ttu-id="d60b9-124">Nome ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="d60b9-124">Resource Id Name.</span></span>

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

### <span data-ttu-id="d60b9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d60b9-125">CommonParameters</span></span>
<span data-ttu-id="d60b9-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d60b9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d60b9-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d60b9-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d60b9-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="d60b9-128">INPUTS</span></span>

### <span data-ttu-id="d60b9-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d60b9-129">System.String</span></span>

## <span data-ttu-id="d60b9-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d60b9-130">OUTPUTS</span></span>

### <span data-ttu-id="d60b9-131">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="d60b9-131">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="d60b9-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="d60b9-132">NOTES</span></span>

## <span data-ttu-id="d60b9-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d60b9-133">RELATED LINKS</span></span>
