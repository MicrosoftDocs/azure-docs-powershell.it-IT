---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 86b9e7574344e1b4724648ce55fa2e36aed6591b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490882"
---
# <span data-ttu-id="5e0a4-101">Get-AzsInfrastructureShare</span><span class="sxs-lookup"><span data-stu-id="5e0a4-101">Get-AzsInfrastructureShare</span></span>

## <span data-ttu-id="5e0a4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5e0a4-102">SYNOPSIS</span></span>
<span data-ttu-id="5e0a4-103">Restituisce un elenco di tutte le condivisioni di file fabric in una determinata posizione.</span><span class="sxs-lookup"><span data-stu-id="5e0a4-103">Returns a list of all fabric file shares at a certain location.</span></span>

## <span data-ttu-id="5e0a4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5e0a4-104">SYNTAX</span></span>

### <span data-ttu-id="5e0a4-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5e0a4-105">List (Default)</span></span>
```
Get-AzsInfrastructureShare [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="5e0a4-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="5e0a4-106">Get</span></span>
```
Get-AzsInfrastructureShare [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="5e0a4-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e0a4-107">ResourceId</span></span>
```
Get-AzsInfrastructureShare -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="5e0a4-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5e0a4-108">DESCRIPTION</span></span>
<span data-ttu-id="5e0a4-109">Restituisce un elenco di tutte le condivisioni di file fabric in una determinata posizione.</span><span class="sxs-lookup"><span data-stu-id="5e0a4-109">Returns a list of all fabric file shares at a certain location.</span></span>

## <span data-ttu-id="5e0a4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5e0a4-110">EXAMPLES</span></span>

### <span data-ttu-id="5e0a4-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5e0a4-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsInfrastructureShare
```

<span data-ttu-id="5e0a4-112">Restituisce un elenco di tutte le condivisioni file.</span><span class="sxs-lookup"><span data-stu-id="5e0a4-112">Returns a list of all file shares.</span></span>

### <span data-ttu-id="5e0a4-113">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="5e0a4-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsInfrastructureShare -Name Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare.Name
```

<span data-ttu-id="5e0a4-114">Restituisce una condivisione di file in base al nome.</span><span class="sxs-lookup"><span data-stu-id="5e0a4-114">Returns a file share based on name.</span></span>

## <span data-ttu-id="5e0a4-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5e0a4-115">PARAMETERS</span></span>

### <span data-ttu-id="5e0a4-116">-Filtro</span><span class="sxs-lookup"><span data-stu-id="5e0a4-116">-Filter</span></span>
<span data-ttu-id="5e0a4-117">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="5e0a4-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="5e0a4-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="5e0a4-118">-Location</span></span>
<span data-ttu-id="5e0a4-119">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="5e0a4-119">Location of the resource.</span></span>

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

### <span data-ttu-id="5e0a4-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="5e0a4-120">-Name</span></span>
<span data-ttu-id="5e0a4-121">Nome condivisione file in tessuto.</span><span class="sxs-lookup"><span data-stu-id="5e0a4-121">Fabric file share name.</span></span>

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

### <span data-ttu-id="5e0a4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e0a4-122">-ResourceGroupName</span></span>
<span data-ttu-id="5e0a4-123">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="5e0a4-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="5e0a4-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e0a4-124">-ResourceId</span></span>
<span data-ttu-id="5e0a4-125">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="5e0a4-125">The resource id.</span></span>

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

### <span data-ttu-id="5e0a4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e0a4-126">CommonParameters</span></span>
<span data-ttu-id="5e0a4-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e0a4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e0a4-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e0a4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e0a4-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5e0a4-129">INPUTS</span></span>

## <span data-ttu-id="5e0a4-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5e0a4-130">OUTPUTS</span></span>

### <span data-ttu-id="5e0a4-131">Microsoft. AzureStack. Management. Fabric. admin. Models. FileShare</span><span class="sxs-lookup"><span data-stu-id="5e0a4-131">Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare</span></span>

## <span data-ttu-id="5e0a4-132">Note</span><span class="sxs-lookup"><span data-stu-id="5e0a4-132">NOTES</span></span>

## <span data-ttu-id="5e0a4-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5e0a4-133">RELATED LINKS</span></span>
