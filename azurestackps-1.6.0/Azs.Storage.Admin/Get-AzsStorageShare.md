---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cc6e2adff73e4b7c81a401bb98e9ab625005ae3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93685199"
---
# <span data-ttu-id="92d3f-101">Get-AzsStorageShare</span><span class="sxs-lookup"><span data-stu-id="92d3f-101">Get-AzsStorageShare</span></span>

## <span data-ttu-id="92d3f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="92d3f-102">SYNOPSIS</span></span>
<span data-ttu-id="92d3f-103">Restituisce un elenco di condivisioni di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="92d3f-103">Returns a list of storage shares.</span></span>

## <span data-ttu-id="92d3f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="92d3f-104">SYNTAX</span></span>

### <span data-ttu-id="92d3f-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="92d3f-105">List (Default)</span></span>
```
Get-AzsStorageShare -FarmName <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="92d3f-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="92d3f-106">Get</span></span>
```
Get-AzsStorageShare -FarmName <String> -Name <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="92d3f-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="92d3f-107">ResourceId</span></span>
```
Get-AzsStorageShare -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="92d3f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="92d3f-108">DESCRIPTION</span></span>
<span data-ttu-id="92d3f-109">Restituisce un elenco di condivisioni di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="92d3f-109">Returns a list of storage shares.</span></span>

## <span data-ttu-id="92d3f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="92d3f-110">EXAMPLES</span></span>

### <span data-ttu-id="92d3f-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="92d3f-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageShare -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="92d3f-112">Ottenere l'elenco delle condivisioni di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="92d3f-112">Get the list of storage shares.</span></span>

## <span data-ttu-id="92d3f-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="92d3f-113">PARAMETERS</span></span>

### <span data-ttu-id="92d3f-114">-Farmname</span><span class="sxs-lookup"><span data-stu-id="92d3f-114">-FarmName</span></span>
<span data-ttu-id="92d3f-115">ID farm.</span><span class="sxs-lookup"><span data-stu-id="92d3f-115">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92d3f-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="92d3f-116">-Name</span></span>
<span data-ttu-id="92d3f-117">Condividi nome.</span><span class="sxs-lookup"><span data-stu-id="92d3f-117">Share name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92d3f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92d3f-118">-ResourceGroupName</span></span>
<span data-ttu-id="92d3f-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="92d3f-119">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92d3f-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92d3f-120">-ResourceId</span></span>
<span data-ttu-id="92d3f-121">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="92d3f-121">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92d3f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92d3f-122">CommonParameters</span></span>
<span data-ttu-id="92d3f-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92d3f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92d3f-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92d3f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92d3f-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="92d3f-125">INPUTS</span></span>

## <span data-ttu-id="92d3f-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="92d3f-126">OUTPUTS</span></span>

### <span data-ttu-id="92d3f-127">Microsoft. AzureStack. Management. storage. admin. Models. Share</span><span class="sxs-lookup"><span data-stu-id="92d3f-127">Microsoft.AzureStack.Management.Storage.Admin.Models.Share</span></span>

## <span data-ttu-id="92d3f-128">Note</span><span class="sxs-lookup"><span data-stu-id="92d3f-128">NOTES</span></span>

## <span data-ttu-id="92d3f-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="92d3f-129">RELATED LINKS</span></span>

