---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/get-azurermsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchService.md
ms.openlocfilehash: 57b09ea3267447f16ceadf4d1eae51f997c53a82
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511444"
---
# <span data-ttu-id="7a301-101">Get-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="7a301-101">Get-AzureRmSearchService</span></span>

## <span data-ttu-id="7a301-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7a301-102">SYNOPSIS</span></span>
<span data-ttu-id="7a301-103">Ottiene un servizio di ricerca Azure.</span><span class="sxs-lookup"><span data-stu-id="7a301-103">Gets an Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a301-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7a301-104">SYNTAX</span></span>

### <span data-ttu-id="7a301-105">ResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7a301-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmSearchService [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a301-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a301-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmSearchService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a301-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a301-107">DESCRIPTION</span></span>
<span data-ttu-id="7a301-108">Il cmdlet **Get-AzureRmSearchService** ottiene il servizio di ricerca Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="7a301-108">The **Get-AzureRmSearchService** cmdlet gets the specified Azure Search service.</span></span>

## <span data-ttu-id="7a301-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7a301-109">EXAMPLES</span></span>

### <span data-ttu-id="7a301-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7a301-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSearchService -ResourceGroupName felixwa-01


ResourceGroupName : felixwa-01
Name              : felixwa-basic-search
Location          : West US
Sku               : Basic
ReplicaCount      : 1
PartitionCount    : 1
HostingMode       : Default
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/felixwa-01/providers/Microsoft.Search/searchServices/felixwa-basic-search
```

<span data-ttu-id="7a301-111">Ottenere un servizio di ricerca di Azure con parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="7a301-111">Get an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="7a301-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7a301-112">PARAMETERS</span></span>

### <span data-ttu-id="7a301-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a301-113">-DefaultProfile</span></span>
<span data-ttu-id="7a301-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7a301-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a301-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="7a301-115">-Name</span></span>
<span data-ttu-id="7a301-116">Nome del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="7a301-116">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a301-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a301-117">-ResourceGroupName</span></span>
<span data-ttu-id="7a301-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7a301-118">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a301-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a301-119">-ResourceId</span></span>
<span data-ttu-id="7a301-120">ID risorsa del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="7a301-120">Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a301-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a301-121">CommonParameters</span></span>
<span data-ttu-id="7a301-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a301-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a301-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a301-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a301-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7a301-124">INPUTS</span></span>

### <span data-ttu-id="7a301-125">System. String</span><span class="sxs-lookup"><span data-stu-id="7a301-125">System.String</span></span>

## <span data-ttu-id="7a301-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7a301-126">OUTPUTS</span></span>

### <span data-ttu-id="7a301-127">Microsoft. Azure. Commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="7a301-127">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="7a301-128">Note</span><span class="sxs-lookup"><span data-stu-id="7a301-128">NOTES</span></span>

## <span data-ttu-id="7a301-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7a301-129">RELATED LINKS</span></span>

[<span data-ttu-id="7a301-130">New-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="7a301-130">New-AzureRmSearchService</span></span>](./New-AzureRmSearchService.md)

[<span data-ttu-id="7a301-131">Set-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="7a301-131">Set-AzureRmSearchService</span></span>](./Set-AzureRmSearchService.md)

[<span data-ttu-id="7a301-132">Remove-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="7a301-132">Remove-AzureRmSearchService</span></span>](./Remove-AzureRmSearchService.md)
