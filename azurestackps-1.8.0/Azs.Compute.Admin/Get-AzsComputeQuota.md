---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 819cdc45e75c15c38c9ae28c583ac3c73e54f4ac
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "93859061"
---
# <span data-ttu-id="7f98c-101">Get-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="7f98c-101">Get-AzsComputeQuota</span></span>

## <span data-ttu-id="7f98c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7f98c-102">SYNOPSIS</span></span>
<span data-ttu-id="7f98c-103">Restituisce le quote che specificano i limiti di quota per gli oggetti COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="7f98c-103">Returns quotas specifying the quota limits for compute objects.</span></span>

## <span data-ttu-id="7f98c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7f98c-104">SYNTAX</span></span>

### <span data-ttu-id="7f98c-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7f98c-105">List (Default)</span></span>
```
Get-AzsComputeQuota [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="7f98c-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="7f98c-106">Get</span></span>
```
Get-AzsComputeQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="7f98c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f98c-107">ResourceId</span></span>
```
Get-AzsComputeQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="7f98c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f98c-108">DESCRIPTION</span></span>
<span data-ttu-id="7f98c-109">Ottenere un elenco di quote esistenti.</span><span class="sxs-lookup"><span data-stu-id="7f98c-109">Get a list of existing quotas.</span></span>

## <span data-ttu-id="7f98c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7f98c-110">EXAMPLES</span></span>

### <span data-ttu-id="7f98c-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7f98c-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsComputeQuota -Location 'local'
```

<span data-ttu-id="7f98c-112">Ottenere tutte le quote di calcolo nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="7f98c-112">Get all compute quotas at the specified location.</span></span>

### <span data-ttu-id="7f98c-113">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="7f98c-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsComputeQuota 'Default Quota'
```

<span data-ttu-id="7f98c-114">Ottenere una quota di calcolo specifica.</span><span class="sxs-lookup"><span data-stu-id="7f98c-114">Get a specific compute quota.</span></span>

## <span data-ttu-id="7f98c-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7f98c-115">PARAMETERS</span></span>

### <span data-ttu-id="7f98c-116">-Posizione</span><span class="sxs-lookup"><span data-stu-id="7f98c-116">-Location</span></span>
<span data-ttu-id="7f98c-117">{{Fill Location Description}}</span><span class="sxs-lookup"><span data-stu-id="7f98c-117">{{Fill Location Description}}</span></span>

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

### <span data-ttu-id="7f98c-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="7f98c-118">-Name</span></span>
<span data-ttu-id="7f98c-119">Nome della quota.</span><span class="sxs-lookup"><span data-stu-id="7f98c-119">Name of the quota.</span></span>

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

### <span data-ttu-id="7f98c-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f98c-120">-ResourceId</span></span>
<span data-ttu-id="7f98c-121">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="7f98c-121">The resource id.</span></span>

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

### <span data-ttu-id="7f98c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f98c-122">CommonParameters</span></span>
<span data-ttu-id="7f98c-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f98c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f98c-124">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f98c-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f98c-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7f98c-125">INPUTS</span></span>

## <span data-ttu-id="7f98c-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7f98c-126">OUTPUTS</span></span>

### <span data-ttu-id="7f98c-127">ComputeQuotaObject</span><span class="sxs-lookup"><span data-stu-id="7f98c-127">ComputeQuotaObject</span></span>

## <span data-ttu-id="7f98c-128">Note</span><span class="sxs-lookup"><span data-stu-id="7f98c-128">NOTES</span></span>

## <span data-ttu-id="7f98c-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7f98c-129">RELATED LINKS</span></span>

