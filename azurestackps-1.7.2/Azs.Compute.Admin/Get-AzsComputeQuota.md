---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 30a1bc70b4e704d8dadf864dedf7173476909cf2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93858737"
---
# <span data-ttu-id="b1120-101">Get-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="b1120-101">Get-AzsComputeQuota</span></span>

## <span data-ttu-id="b1120-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b1120-102">SYNOPSIS</span></span>
<span data-ttu-id="b1120-103">Restituisce le quote che specificano i limiti di quota per gli oggetti COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="b1120-103">Returns quotas specifying the quota limits for compute objects.</span></span>

## <span data-ttu-id="b1120-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b1120-104">SYNTAX</span></span>

### <span data-ttu-id="b1120-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b1120-105">List (Default)</span></span>
```
Get-AzsComputeQuota [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="b1120-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="b1120-106">Get</span></span>
```
Get-AzsComputeQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="b1120-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1120-107">ResourceId</span></span>
```
Get-AzsComputeQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="b1120-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1120-108">DESCRIPTION</span></span>
<span data-ttu-id="b1120-109">Ottenere un elenco di quote esistenti.</span><span class="sxs-lookup"><span data-stu-id="b1120-109">Get a list of existing quotas.</span></span>

## <span data-ttu-id="b1120-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b1120-110">EXAMPLES</span></span>

### <span data-ttu-id="b1120-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b1120-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsComputeQuota -Location 'local'
```

<span data-ttu-id="b1120-112">Ottenere tutte le quote di calcolo nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="b1120-112">Get all compute quotas at the specified location.</span></span>

### <span data-ttu-id="b1120-113">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="b1120-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsComputeQuota 'Default Quota'
```

<span data-ttu-id="b1120-114">Ottenere una quota di calcolo specifica.</span><span class="sxs-lookup"><span data-stu-id="b1120-114">Get a specific compute quota.</span></span>

## <span data-ttu-id="b1120-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b1120-115">PARAMETERS</span></span>

### <span data-ttu-id="b1120-116">-Posizione</span><span class="sxs-lookup"><span data-stu-id="b1120-116">-Location</span></span>
<span data-ttu-id="b1120-117">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="b1120-117">Location of the resource.</span></span>

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

### <span data-ttu-id="b1120-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="b1120-118">-Name</span></span>
<span data-ttu-id="b1120-119">Nome della quota.</span><span class="sxs-lookup"><span data-stu-id="b1120-119">Name of the quota.</span></span>

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

### <span data-ttu-id="b1120-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1120-120">-ResourceId</span></span>
<span data-ttu-id="b1120-121">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="b1120-121">The resource id.</span></span>

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

### <span data-ttu-id="b1120-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1120-122">CommonParameters</span></span>
<span data-ttu-id="b1120-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1120-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1120-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1120-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1120-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b1120-125">INPUTS</span></span>

## <span data-ttu-id="b1120-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b1120-126">OUTPUTS</span></span>

### <span data-ttu-id="b1120-127">ComputeQuotaObject</span><span class="sxs-lookup"><span data-stu-id="b1120-127">ComputeQuotaObject</span></span>

## <span data-ttu-id="b1120-128">Note</span><span class="sxs-lookup"><span data-stu-id="b1120-128">NOTES</span></span>

## <span data-ttu-id="b1120-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b1120-129">RELATED LINKS</span></span>

