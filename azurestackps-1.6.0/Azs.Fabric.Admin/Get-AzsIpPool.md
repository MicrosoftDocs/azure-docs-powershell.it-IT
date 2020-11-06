---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2528d9b4f9443d8857006b6fc1e94100b0b477ec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490910"
---
# <span data-ttu-id="193f5-101">Get-AzsIpPool</span><span class="sxs-lookup"><span data-stu-id="193f5-101">Get-AzsIpPool</span></span>

## <span data-ttu-id="193f5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="193f5-102">SYNOPSIS</span></span>
<span data-ttu-id="193f5-103">Restituisce un elenco di tutti i pool IP in una determinata posizione.</span><span class="sxs-lookup"><span data-stu-id="193f5-103">Returns a list of all IP pools at a certain location.</span></span>

## <span data-ttu-id="193f5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="193f5-104">SYNTAX</span></span>

### <span data-ttu-id="193f5-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="193f5-105">List (Default)</span></span>
```
Get-AzsIpPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="193f5-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="193f5-106">Get</span></span>
```
Get-AzsIpPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="193f5-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="193f5-107">ResourceId</span></span>
```
Get-AzsIpPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="193f5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="193f5-108">DESCRIPTION</span></span>
<span data-ttu-id="193f5-109">Restituisce un elenco di tutti i pool IP in una determinata posizione.</span><span class="sxs-lookup"><span data-stu-id="193f5-109">Returns a list of all IP pools at a certain location.</span></span>

## <span data-ttu-id="193f5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="193f5-110">EXAMPLES</span></span>

### <span data-ttu-id="193f5-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="193f5-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsIpPool
```

<span data-ttu-id="193f5-112">Ottenere tutti i pool IP dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="193f5-112">Get an all infrastructure ip pools.</span></span>

### <span data-ttu-id="193f5-113">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="193f5-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsIpPool -Name "08786a0f-ad8c-43aa-a154-06083abfc1ac"
```

<span data-ttu-id="193f5-114">Ottenere un pool IP dell'infrastruttura in base al nome.</span><span class="sxs-lookup"><span data-stu-id="193f5-114">Get an infrastructure ip pool based on name.</span></span>

## <span data-ttu-id="193f5-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="193f5-115">PARAMETERS</span></span>

### <span data-ttu-id="193f5-116">-Filtro</span><span class="sxs-lookup"><span data-stu-id="193f5-116">-Filter</span></span>
<span data-ttu-id="193f5-117">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="193f5-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="193f5-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="193f5-118">-Location</span></span>
<span data-ttu-id="193f5-119">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="193f5-119">Location of the resource.</span></span>

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

### <span data-ttu-id="193f5-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="193f5-120">-Name</span></span>
<span data-ttu-id="193f5-121">Nome del pool IP.</span><span class="sxs-lookup"><span data-stu-id="193f5-121">IP pool name.</span></span>

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

### <span data-ttu-id="193f5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="193f5-122">-ResourceGroupName</span></span>
<span data-ttu-id="193f5-123">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="193f5-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="193f5-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="193f5-124">-ResourceId</span></span>
<span data-ttu-id="193f5-125">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="193f5-125">The resource id.</span></span>

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

### <span data-ttu-id="193f5-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="193f5-126">-Skip</span></span>
<span data-ttu-id="193f5-127">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="193f5-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="193f5-128">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="193f5-128">-Top</span></span>
<span data-ttu-id="193f5-129">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="193f5-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="193f5-130">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="193f5-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="193f5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="193f5-131">CommonParameters</span></span>
<span data-ttu-id="193f5-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="193f5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="193f5-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="193f5-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="193f5-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="193f5-134">INPUTS</span></span>

## <span data-ttu-id="193f5-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="193f5-135">OUTPUTS</span></span>

### <span data-ttu-id="193f5-136">Microsoft. AzureStack. Management. Fabric. admin. Models. IpPool</span><span class="sxs-lookup"><span data-stu-id="193f5-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.IpPool</span></span>

## <span data-ttu-id="193f5-137">Note</span><span class="sxs-lookup"><span data-stu-id="193f5-137">NOTES</span></span>

## <span data-ttu-id="193f5-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="193f5-138">RELATED LINKS</span></span>

