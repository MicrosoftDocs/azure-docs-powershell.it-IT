---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d5999718cc3085eb69da482df27fa0cb4379ed40
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030129"
---
# <span data-ttu-id="f2eb9-101">Get-AzsIpPool</span><span class="sxs-lookup"><span data-stu-id="f2eb9-101">Get-AzsIpPool</span></span>

## <span data-ttu-id="f2eb9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f2eb9-102">SYNOPSIS</span></span>
<span data-ttu-id="f2eb9-103">Restituisce un elenco di tutti i pool IP in una determinata posizione.</span><span class="sxs-lookup"><span data-stu-id="f2eb9-103">Returns a list of all IP pools at a certain location.</span></span>

## <span data-ttu-id="f2eb9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f2eb9-104">SYNTAX</span></span>

### <span data-ttu-id="f2eb9-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f2eb9-105">List (Default)</span></span>
```
Get-AzsIpPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="f2eb9-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="f2eb9-106">Get</span></span>
```
Get-AzsIpPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="f2eb9-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2eb9-107">ResourceId</span></span>
```
Get-AzsIpPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="f2eb9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f2eb9-108">DESCRIPTION</span></span>
<span data-ttu-id="f2eb9-109">Restituisce un elenco di tutti i pool IP in una determinata posizione.</span><span class="sxs-lookup"><span data-stu-id="f2eb9-109">Returns a list of all IP pools at a certain location.</span></span>

## <span data-ttu-id="f2eb9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f2eb9-110">EXAMPLES</span></span>

### <span data-ttu-id="f2eb9-111">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="f2eb9-111">EXAMPLE 1</span></span>
```
Get-AzsIpPool
```

<span data-ttu-id="f2eb9-112">Ottenere tutti i pool IP dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="f2eb9-112">Get an all infrastructure ip pools.</span></span>

### <span data-ttu-id="f2eb9-113">ESEMPIO 2</span><span class="sxs-lookup"><span data-stu-id="f2eb9-113">EXAMPLE 2</span></span>
```
Get-AzsIpPool -Name "08786a0f-ad8c-43aa-a154-06083abfc1ac"
```

<span data-ttu-id="f2eb9-114">Ottenere un pool IP dell'infrastruttura in base al nome.</span><span class="sxs-lookup"><span data-stu-id="f2eb9-114">Get an infrastructure ip pool based on name.</span></span>

## <span data-ttu-id="f2eb9-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f2eb9-115">PARAMETERS</span></span>

### <span data-ttu-id="f2eb9-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="f2eb9-116">-Name</span></span>
<span data-ttu-id="f2eb9-117">Nome del pool IP.</span><span class="sxs-lookup"><span data-stu-id="f2eb9-117">IP pool name.</span></span>

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

### <span data-ttu-id="f2eb9-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="f2eb9-118">-Location</span></span>
<span data-ttu-id="f2eb9-119">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="f2eb9-119">Location of the resource.</span></span>

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

### <span data-ttu-id="f2eb9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2eb9-120">-ResourceGroupName</span></span>
<span data-ttu-id="f2eb9-121">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="f2eb9-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="f2eb9-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2eb9-122">-ResourceId</span></span>
<span data-ttu-id="f2eb9-123">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="f2eb9-123">The resource id.</span></span>

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

### <span data-ttu-id="f2eb9-124">-Filtro</span><span class="sxs-lookup"><span data-stu-id="f2eb9-124">-Filter</span></span>
<span data-ttu-id="f2eb9-125">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="f2eb9-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="f2eb9-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="f2eb9-126">-Skip</span></span>
<span data-ttu-id="f2eb9-127">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="f2eb9-127">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2eb9-128">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="f2eb9-128">-Top</span></span>
<span data-ttu-id="f2eb9-129">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="f2eb9-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="f2eb9-130">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="f2eb9-130">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2eb9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2eb9-131">CommonParameters</span></span>
<span data-ttu-id="f2eb9-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2eb9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2eb9-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2eb9-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2eb9-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f2eb9-134">INPUTS</span></span>

## <span data-ttu-id="f2eb9-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f2eb9-135">OUTPUTS</span></span>

### <span data-ttu-id="f2eb9-136">Microsoft. AzureStack. Management. Fabric. admin. Models. IpPool</span><span class="sxs-lookup"><span data-stu-id="f2eb9-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.IpPool</span></span>

## <span data-ttu-id="f2eb9-137">Note</span><span class="sxs-lookup"><span data-stu-id="f2eb9-137">NOTES</span></span>

## <span data-ttu-id="f2eb9-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f2eb9-138">RELATED LINKS</span></span>
