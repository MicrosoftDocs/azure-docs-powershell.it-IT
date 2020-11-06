---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e2580e2b6de179cdc3a9407b514848cc832e798e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490758"
---
# <span data-ttu-id="3e7e3-101">Get-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="3e7e3-101">Get-AzsPlatformImage</span></span>

## <span data-ttu-id="3e7e3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3e7e3-102">SYNOPSIS</span></span>
<span data-ttu-id="3e7e3-103">Restituisce le immagini della macchina virtuale caricate nel repository di immagini della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="3e7e3-103">Returns virtual machine images loaded into the platform image repository.</span></span>

## <span data-ttu-id="3e7e3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3e7e3-104">SYNTAX</span></span>

### <span data-ttu-id="3e7e3-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3e7e3-105">List (Default)</span></span>
```
Get-AzsPlatformImage [-Publisher <String>] [-Offer <String>] [-Sku <String>] [-Location <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="3e7e3-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="3e7e3-106">Get</span></span>
```
Get-AzsPlatformImage -Publisher <String> -Offer <String> -Sku <String> -Version <String> [-Location <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="3e7e3-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e7e3-107">ResourceId</span></span>
```
Get-AzsPlatformImage -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="3e7e3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e7e3-108">DESCRIPTION</span></span>
<span data-ttu-id="3e7e3-109">Restituisce immagini della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="3e7e3-109">Returns platform images.</span></span>

## <span data-ttu-id="3e7e3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3e7e3-110">EXAMPLES</span></span>

### <span data-ttu-id="3e7e3-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3e7e3-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlatformImage
```

<span data-ttu-id="3e7e3-112">Restituisce le immagini della macchina virtuale caricate nel repository di immagini della piattaforma nella posizione locale.</span><span class="sxs-lookup"><span data-stu-id="3e7e3-112">Returns virtual machine images loaded into the platform image repository at the location local.</span></span>

### <span data-ttu-id="3e7e3-113">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="3e7e3-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsPlatformImage -Publisher Canonical -Offer UbuntuServer -Sku 16.04-LTS -Version 0.1.0
```

<span data-ttu-id="3e7e3-114">Ottenere una specifica immagine della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="3e7e3-114">Get a specific platform image.</span></span>

## <span data-ttu-id="3e7e3-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3e7e3-115">PARAMETERS</span></span>

### <span data-ttu-id="3e7e3-116">-Posizione</span><span class="sxs-lookup"><span data-stu-id="3e7e3-116">-Location</span></span>
<span data-ttu-id="3e7e3-117">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="3e7e3-117">Location of the resource.</span></span>

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

### <span data-ttu-id="3e7e3-118">-Offerta</span><span class="sxs-lookup"><span data-stu-id="3e7e3-118">-Offer</span></span>
<span data-ttu-id="3e7e3-119">Nome dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="3e7e3-119">Name of the offer.</span></span>

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

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e7e3-120">-Publisher</span><span class="sxs-lookup"><span data-stu-id="3e7e3-120">-Publisher</span></span>
<span data-ttu-id="3e7e3-121">Nome dell'autore.</span><span class="sxs-lookup"><span data-stu-id="3e7e3-121">Name of the publisher.</span></span>

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

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e7e3-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e7e3-122">-ResourceId</span></span>
<span data-ttu-id="3e7e3-123">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="3e7e3-123">The resource id.</span></span>

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

### <span data-ttu-id="3e7e3-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="3e7e3-124">-Sku</span></span>
<span data-ttu-id="3e7e3-125">Nome dell'USK.</span><span class="sxs-lookup"><span data-stu-id="3e7e3-125">Name of the SKU.</span></span>

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

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e7e3-126">-Versione</span><span class="sxs-lookup"><span data-stu-id="3e7e3-126">-Version</span></span>
<span data-ttu-id="3e7e3-127">Versione dell'immagine della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="3e7e3-127">The version of the platform image.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e7e3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e7e3-128">CommonParameters</span></span>
<span data-ttu-id="3e7e3-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e7e3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e7e3-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e7e3-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e7e3-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3e7e3-131">INPUTS</span></span>

## <span data-ttu-id="3e7e3-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3e7e3-132">OUTPUTS</span></span>

### <span data-ttu-id="3e7e3-133">PlatformImageObject</span><span class="sxs-lookup"><span data-stu-id="3e7e3-133">PlatformImageObject</span></span>

## <span data-ttu-id="3e7e3-134">Note</span><span class="sxs-lookup"><span data-stu-id="3e7e3-134">NOTES</span></span>

## <span data-ttu-id="3e7e3-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3e7e3-135">RELATED LINKS</span></span>

