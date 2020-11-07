---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5c686faa457d83ab0ddffb932b20ab5fcd168ff0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93858265"
---
# <span data-ttu-id="6130c-101">Get-AzsMacAddressPool</span><span class="sxs-lookup"><span data-stu-id="6130c-101">Get-AzsMacAddressPool</span></span>

## <span data-ttu-id="6130c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6130c-102">SYNOPSIS</span></span>
<span data-ttu-id="6130c-103">Restituisce un elenco di tutti i pool di indirizzi MAC in una posizione.</span><span class="sxs-lookup"><span data-stu-id="6130c-103">Returns a list of all MAC address pools at a location.</span></span>

## <span data-ttu-id="6130c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6130c-104">SYNTAX</span></span>

### <span data-ttu-id="6130c-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6130c-105">List (Default)</span></span>
```
Get-AzsMacAddressPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="6130c-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="6130c-106">Get</span></span>
```
Get-AzsMacAddressPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="6130c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6130c-107">ResourceId</span></span>
```
Get-AzsMacAddressPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="6130c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6130c-108">DESCRIPTION</span></span>
<span data-ttu-id="6130c-109">Restituisce un elenco di tutti i pool di indirizzi MAC in una posizione.</span><span class="sxs-lookup"><span data-stu-id="6130c-109">Returns a list of all MAC address pools at a location.</span></span>

## <span data-ttu-id="6130c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6130c-110">EXAMPLES</span></span>

### <span data-ttu-id="6130c-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6130c-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsMacAddressPool
```

<span data-ttu-id="6130c-112">Ottenere tutti i pool di indirizzi MAC in una posizione.</span><span class="sxs-lookup"><span data-stu-id="6130c-112">Get all MAC address pools at a location.</span></span>

### <span data-ttu-id="6130c-113">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="6130c-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsMacAddressPool -Name "8197fd09-8a69-417e-a55c-10c2c61f5ee7"
```

<span data-ttu-id="6130c-114">Ottenere uno specifico pool di indirizzi MAC in una posizione in base al nome.</span><span class="sxs-lookup"><span data-stu-id="6130c-114">Get a specific MAC address pool at a location based on name.</span></span>

## <span data-ttu-id="6130c-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6130c-115">PARAMETERS</span></span>

### <span data-ttu-id="6130c-116">-Filtro</span><span class="sxs-lookup"><span data-stu-id="6130c-116">-Filter</span></span>
<span data-ttu-id="6130c-117">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="6130c-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="6130c-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="6130c-118">-Location</span></span>
<span data-ttu-id="6130c-119">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="6130c-119">Location of the resource.</span></span>

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

### <span data-ttu-id="6130c-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="6130c-120">-Name</span></span>
<span data-ttu-id="6130c-121">Nome del pool di indirizzi MAC.</span><span class="sxs-lookup"><span data-stu-id="6130c-121">Name of the MAC address pool.</span></span>

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

### <span data-ttu-id="6130c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6130c-122">-ResourceGroupName</span></span>
<span data-ttu-id="6130c-123">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="6130c-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="6130c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6130c-124">-ResourceId</span></span>
<span data-ttu-id="6130c-125">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="6130c-125">The resource id.</span></span>

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

### <span data-ttu-id="6130c-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="6130c-126">-Skip</span></span>
<span data-ttu-id="6130c-127">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="6130c-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="6130c-128">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="6130c-128">-Top</span></span>
<span data-ttu-id="6130c-129">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="6130c-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="6130c-130">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="6130c-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="6130c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6130c-131">CommonParameters</span></span>
<span data-ttu-id="6130c-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6130c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6130c-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6130c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6130c-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6130c-134">INPUTS</span></span>

## <span data-ttu-id="6130c-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6130c-135">OUTPUTS</span></span>

### <span data-ttu-id="6130c-136">Microsoft. AzureStack. Management. Fabric. admin. Models. MacAddressPool</span><span class="sxs-lookup"><span data-stu-id="6130c-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.MacAddressPool</span></span>

## <span data-ttu-id="6130c-137">Note</span><span class="sxs-lookup"><span data-stu-id="6130c-137">NOTES</span></span>

## <span data-ttu-id="6130c-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6130c-138">RELATED LINKS</span></span>

