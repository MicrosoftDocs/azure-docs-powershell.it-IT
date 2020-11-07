---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d5999718cc3085eb69da482df27fa0cb4379ed40
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "93858969"
---
# <span data-ttu-id="99f9b-101">Get-AzsIpPool</span><span class="sxs-lookup"><span data-stu-id="99f9b-101">Get-AzsIpPool</span></span>

## <span data-ttu-id="99f9b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="99f9b-102">SYNOPSIS</span></span>
<span data-ttu-id="99f9b-103">Restituisce un elenco di tutti i pool IP in una determinata posizione.</span><span class="sxs-lookup"><span data-stu-id="99f9b-103">Returns a list of all IP pools at a certain location.</span></span>

## <span data-ttu-id="99f9b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="99f9b-104">SYNTAX</span></span>

### <span data-ttu-id="99f9b-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="99f9b-105">List (Default)</span></span>
```
Get-AzsIpPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="99f9b-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="99f9b-106">Get</span></span>
```
Get-AzsIpPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="99f9b-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="99f9b-107">ResourceId</span></span>
```
Get-AzsIpPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="99f9b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="99f9b-108">DESCRIPTION</span></span>
<span data-ttu-id="99f9b-109">Restituisce un elenco di tutti i pool IP in una determinata posizione.</span><span class="sxs-lookup"><span data-stu-id="99f9b-109">Returns a list of all IP pools at a certain location.</span></span>

## <span data-ttu-id="99f9b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="99f9b-110">EXAMPLES</span></span>

### <span data-ttu-id="99f9b-111">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="99f9b-111">EXAMPLE 1</span></span>
```
Get-AzsIpPool
```

<span data-ttu-id="99f9b-112">Ottenere tutti i pool IP dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="99f9b-112">Get an all infrastructure ip pools.</span></span>

### <span data-ttu-id="99f9b-113">ESEMPIO 2</span><span class="sxs-lookup"><span data-stu-id="99f9b-113">EXAMPLE 2</span></span>
```
Get-AzsIpPool -Name "08786a0f-ad8c-43aa-a154-06083abfc1ac"
```

<span data-ttu-id="99f9b-114">Ottenere un pool IP dell'infrastruttura in base al nome.</span><span class="sxs-lookup"><span data-stu-id="99f9b-114">Get an infrastructure ip pool based on name.</span></span>

## <span data-ttu-id="99f9b-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="99f9b-115">PARAMETERS</span></span>

### <span data-ttu-id="99f9b-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="99f9b-116">-Name</span></span>
<span data-ttu-id="99f9b-117">Nome del pool IP.</span><span class="sxs-lookup"><span data-stu-id="99f9b-117">IP pool name.</span></span>

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

### <span data-ttu-id="99f9b-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="99f9b-118">-Location</span></span>
<span data-ttu-id="99f9b-119">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="99f9b-119">Location of the resource.</span></span>

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

### <span data-ttu-id="99f9b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99f9b-120">-ResourceGroupName</span></span>
<span data-ttu-id="99f9b-121">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="99f9b-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="99f9b-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="99f9b-122">-ResourceId</span></span>
<span data-ttu-id="99f9b-123">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="99f9b-123">The resource id.</span></span>

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

### <span data-ttu-id="99f9b-124">-Filtro</span><span class="sxs-lookup"><span data-stu-id="99f9b-124">-Filter</span></span>
<span data-ttu-id="99f9b-125">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="99f9b-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="99f9b-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="99f9b-126">-Skip</span></span>
<span data-ttu-id="99f9b-127">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="99f9b-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="99f9b-128">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="99f9b-128">-Top</span></span>
<span data-ttu-id="99f9b-129">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="99f9b-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="99f9b-130">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="99f9b-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="99f9b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99f9b-131">CommonParameters</span></span>
<span data-ttu-id="99f9b-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99f9b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99f9b-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99f9b-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99f9b-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="99f9b-134">INPUTS</span></span>

## <span data-ttu-id="99f9b-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="99f9b-135">OUTPUTS</span></span>

### <span data-ttu-id="99f9b-136">Microsoft. AzureStack. Management. Fabric. admin. Models. IpPool</span><span class="sxs-lookup"><span data-stu-id="99f9b-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.IpPool</span></span>

## <span data-ttu-id="99f9b-137">Note</span><span class="sxs-lookup"><span data-stu-id="99f9b-137">NOTES</span></span>

## <span data-ttu-id="99f9b-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="99f9b-138">RELATED LINKS</span></span>
