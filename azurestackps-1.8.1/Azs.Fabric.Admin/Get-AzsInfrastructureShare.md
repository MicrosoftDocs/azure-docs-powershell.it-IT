---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4e39a2d9e314a29eaf273e4ef20e71d96293f1f7
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859653"
---
# <span data-ttu-id="24def-101">Get-AzsInfrastructureShare</span><span class="sxs-lookup"><span data-stu-id="24def-101">Get-AzsInfrastructureShare</span></span>

## <span data-ttu-id="24def-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="24def-102">SYNOPSIS</span></span>
<span data-ttu-id="24def-103">Restituisce un elenco di tutte le condivisioni di file fabric in una determinata posizione.</span><span class="sxs-lookup"><span data-stu-id="24def-103">Returns a list of all fabric file shares at a certain location.</span></span>

## <span data-ttu-id="24def-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="24def-104">SYNTAX</span></span>

### <span data-ttu-id="24def-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="24def-105">List (Default)</span></span>
```
Get-AzsInfrastructureShare [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="24def-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="24def-106">Get</span></span>
```
Get-AzsInfrastructureShare [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="24def-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="24def-107">ResourceId</span></span>
```
Get-AzsInfrastructureShare -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="24def-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="24def-108">DESCRIPTION</span></span>
<span data-ttu-id="24def-109">Restituisce un elenco di tutte le condivisioni di file fabric in una determinata posizione.</span><span class="sxs-lookup"><span data-stu-id="24def-109">Returns a list of all fabric file shares at a certain location.</span></span>

## <span data-ttu-id="24def-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="24def-110">EXAMPLES</span></span>

### <span data-ttu-id="24def-111">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="24def-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureShare
```

<span data-ttu-id="24def-112">Restituisce un elenco di tutte le condivisioni file.</span><span class="sxs-lookup"><span data-stu-id="24def-112">Returns a list of all file shares.</span></span>

### <span data-ttu-id="24def-113">ESEMPIO 2</span><span class="sxs-lookup"><span data-stu-id="24def-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureShare -Name Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare.Name
```

<span data-ttu-id="24def-114">Restituisce una condivisione di file in base al nome.</span><span class="sxs-lookup"><span data-stu-id="24def-114">Returns a file share based on name.</span></span>

## <span data-ttu-id="24def-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="24def-115">PARAMETERS</span></span>

### <span data-ttu-id="24def-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="24def-116">-Name</span></span>
<span data-ttu-id="24def-117">Nome condivisione file in tessuto.</span><span class="sxs-lookup"><span data-stu-id="24def-117">Fabric file share name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24def-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="24def-118">-Location</span></span>
<span data-ttu-id="24def-119">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="24def-119">Location of the resource.</span></span>

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

### <span data-ttu-id="24def-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24def-120">-ResourceGroupName</span></span>
<span data-ttu-id="24def-121">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="24def-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="24def-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24def-122">-ResourceId</span></span>
<span data-ttu-id="24def-123">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="24def-123">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24def-124">-Filtro</span><span class="sxs-lookup"><span data-stu-id="24def-124">-Filter</span></span>
<span data-ttu-id="24def-125">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="24def-125">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24def-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24def-126">CommonParameters</span></span>
<span data-ttu-id="24def-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24def-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24def-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24def-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24def-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="24def-129">INPUTS</span></span>

## <span data-ttu-id="24def-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="24def-130">OUTPUTS</span></span>

### <span data-ttu-id="24def-131">Microsoft. AzureStack. Management. Fabric. admin. Models. FileShare</span><span class="sxs-lookup"><span data-stu-id="24def-131">Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare</span></span>

## <span data-ttu-id="24def-132">Note</span><span class="sxs-lookup"><span data-stu-id="24def-132">NOTES</span></span>

## <span data-ttu-id="24def-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="24def-133">RELATED LINKS</span></span>
