---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCache.md
ms.openlocfilehash: fee978a1500c0fc472ec8015a3e8dbbbdc8015bd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189950"
---
# <span data-ttu-id="e73e2-101">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="e73e2-101">Get-AzApiManagementCache</span></span>

## <span data-ttu-id="e73e2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e73e2-102">SYNOPSIS</span></span>
<span data-ttu-id="e73e2-103">Ottenere i dettagli della cache.</span><span class="sxs-lookup"><span data-stu-id="e73e2-103">Get the details of the Cache.</span></span>

## <span data-ttu-id="e73e2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e73e2-104">SYNTAX</span></span>

### <span data-ttu-id="e73e2-105">ContextParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e73e2-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementCache -Context <PsApiManagementContext> [-CacheId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e73e2-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e73e2-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementCache -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e73e2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e73e2-107">DESCRIPTION</span></span>
<span data-ttu-id="e73e2-108">Ottenere i dettagli della cache configurata nel servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="e73e2-108">Get the details of the Cache configured in Api Management service.</span></span>

## <span data-ttu-id="e73e2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e73e2-109">EXAMPLES</span></span>

### <span data-ttu-id="e73e2-110">Esempio 1: ottenere tutte le cache</span><span class="sxs-lookup"><span data-stu-id="e73e2-110">Example 1: Get all Caches</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCache -Context $apimContext
```

```
CacheId           : westus
Description       : apim.redis.cache.windows.net
ConnectionString  : {{5cc1848125a3f724dcf9a928}}
ResourceId        : https://management.azure.com/subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.Cache/Redis/apim
Id                : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/caches/westus
ResourceGroupName : Api-Default-West-US
ServiceName       : contoso
```

<span data-ttu-id="e73e2-111">Ottiene un elenco di tutte le cache configurate nel servizio di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="e73e2-111">Gets a list of all the Caches configured in the Api Management service.</span></span>

### <span data-ttu-id="e73e2-112">Esempio 2: ottenere la cache specificata dall'identificatore westus</span><span class="sxs-lookup"><span data-stu-id="e73e2-112">Example 2: Get the Cache specified by the Identifier westus</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCache -Context $apimContext -cacheId westus
```

```
CacheId           : westus
Description       : apim.redis.cache.windows.net
ConnectionString  : {{5cc1848125a3f724dcf9a928}}
ResourceId        : https://management.azure.com/subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.Cache/Redis/apim
Id                : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/caches/westus
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="e73e2-113">Ottenere i dettagli della cache specificata configurata per westus</span><span class="sxs-lookup"><span data-stu-id="e73e2-113">Get the details of the specified Cache configured for westus</span></span>

## <span data-ttu-id="e73e2-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e73e2-114">PARAMETERS</span></span>

### <span data-ttu-id="e73e2-115">-CacheId</span><span class="sxs-lookup"><span data-stu-id="e73e2-115">-CacheId</span></span>
<span data-ttu-id="e73e2-116">Identificatore di una cache.</span><span class="sxs-lookup"><span data-stu-id="e73e2-116">Identifier of a cache.</span></span>
<span data-ttu-id="e73e2-117">Se specificato cercherà di trovare la cache in base all'identificatore.</span><span class="sxs-lookup"><span data-stu-id="e73e2-117">If specified will try to find cache by the identifier.</span></span>
<span data-ttu-id="e73e2-118">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e73e2-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="e73e2-119">-Contesto</span><span class="sxs-lookup"><span data-stu-id="e73e2-119">-Context</span></span>
<span data-ttu-id="e73e2-120">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="e73e2-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e73e2-121">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="e73e2-121">This parameter is required.</span></span>

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

### <span data-ttu-id="e73e2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e73e2-122">-DefaultProfile</span></span>
<span data-ttu-id="e73e2-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e73e2-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e73e2-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e73e2-124">-ResourceId</span></span>
<span data-ttu-id="e73e2-125">Identificatore delle risorse ARM di una cache.</span><span class="sxs-lookup"><span data-stu-id="e73e2-125">Arm Resource Identifier of a cache.</span></span> <span data-ttu-id="e73e2-126">Se specificato cercherà di trovare la cache in base all'identificatore.</span><span class="sxs-lookup"><span data-stu-id="e73e2-126">If specified will try to find cache by the identifier.</span></span> <span data-ttu-id="e73e2-127">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="e73e2-127">This parameter is required.</span></span>

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

### <span data-ttu-id="e73e2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e73e2-128">CommonParameters</span></span>
<span data-ttu-id="e73e2-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e73e2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e73e2-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e73e2-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e73e2-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e73e2-131">INPUTS</span></span>

### <span data-ttu-id="e73e2-132">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e73e2-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e73e2-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e73e2-133">System.String</span></span>

## <span data-ttu-id="e73e2-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e73e2-134">OUTPUTS</span></span>

### <span data-ttu-id="e73e2-135">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="e73e2-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="e73e2-136">Note</span><span class="sxs-lookup"><span data-stu-id="e73e2-136">NOTES</span></span>

## <span data-ttu-id="e73e2-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e73e2-137">RELATED LINKS</span></span>

[<span data-ttu-id="e73e2-138">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="e73e2-138">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="e73e2-139">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="e73e2-139">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)

[<span data-ttu-id="e73e2-140">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="e73e2-140">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)
