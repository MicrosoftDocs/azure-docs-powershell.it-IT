---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchService.md
ms.openlocfilehash: 9acd7be782d52e9b636b0445776defa95f83c1f9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854749"
---
# <span data-ttu-id="4ff19-101">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="4ff19-101">Get-AzSearchService</span></span>

## <span data-ttu-id="4ff19-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4ff19-102">SYNOPSIS</span></span>
<span data-ttu-id="4ff19-103">Ottiene un servizio di ricerca Azure.</span><span class="sxs-lookup"><span data-stu-id="4ff19-103">Gets an Azure Search service.</span></span>

## <span data-ttu-id="4ff19-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4ff19-104">SYNTAX</span></span>

### <span data-ttu-id="4ff19-105">ResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4ff19-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzSearchService [-ResourceGroupName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4ff19-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ff19-106">ResourceIdParameterSet</span></span>
```
Get-AzSearchService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ff19-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4ff19-107">DESCRIPTION</span></span>
<span data-ttu-id="4ff19-108">Il cmdlet **Get-AzSearchService** ottiene il servizio di ricerca Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="4ff19-108">The **Get-AzSearchService** cmdlet gets the specified Azure Search service.</span></span>

## <span data-ttu-id="4ff19-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4ff19-109">EXAMPLES</span></span>

### <span data-ttu-id="4ff19-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4ff19-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchService -ResourceGroupName felixwa-01


ResourceGroupName : felixwa-01
Name              : felixwa-basic-search
Location          : West US
Sku               : Basic
ReplicaCount      : 1
PartitionCount    : 1
HostingMode       : Default
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/felixwa-01/providers/Microsoft.Search/searchServices/felixwa-basic-search
```

<span data-ttu-id="4ff19-111">Ottenere un servizio di ricerca di Azure con parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="4ff19-111">Get an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="4ff19-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4ff19-112">PARAMETERS</span></span>

### <span data-ttu-id="4ff19-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ff19-113">-DefaultProfile</span></span>
<span data-ttu-id="4ff19-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4ff19-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ff19-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="4ff19-115">-Name</span></span>
<span data-ttu-id="4ff19-116">Nome del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="4ff19-116">Search Service name.</span></span>

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

### <span data-ttu-id="4ff19-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ff19-117">-ResourceGroupName</span></span>
<span data-ttu-id="4ff19-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4ff19-118">Resource Group name.</span></span>

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

### <span data-ttu-id="4ff19-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ff19-119">-ResourceId</span></span>
<span data-ttu-id="4ff19-120">ID risorsa del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="4ff19-120">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="4ff19-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ff19-121">CommonParameters</span></span>
<span data-ttu-id="4ff19-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ff19-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ff19-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ff19-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ff19-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4ff19-124">INPUTS</span></span>

### <span data-ttu-id="4ff19-125">System. String</span><span class="sxs-lookup"><span data-stu-id="4ff19-125">System.String</span></span>

## <span data-ttu-id="4ff19-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4ff19-126">OUTPUTS</span></span>

### <span data-ttu-id="4ff19-127">Microsoft. Azure. Commands. Management. search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="4ff19-127">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="4ff19-128">Note</span><span class="sxs-lookup"><span data-stu-id="4ff19-128">NOTES</span></span>

## <span data-ttu-id="4ff19-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4ff19-129">RELATED LINKS</span></span>

[<span data-ttu-id="4ff19-130">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="4ff19-130">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="4ff19-131">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="4ff19-131">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

[<span data-ttu-id="4ff19-132">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="4ff19-132">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)