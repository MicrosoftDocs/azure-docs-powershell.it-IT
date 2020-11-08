---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 403f980af6b00272ca67b3ba180808ba8c82ebce
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030584"
---
# <span data-ttu-id="bfeb7-101">Get-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="bfeb7-101">Get-AzsPlatformImage</span></span>

## <span data-ttu-id="bfeb7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bfeb7-102">SYNOPSIS</span></span>
<span data-ttu-id="bfeb7-103">Restituisce le immagini della macchina virtuale caricate nel repository di immagini della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="bfeb7-103">Returns virtual machine images loaded into the platform image repository.</span></span>

## <span data-ttu-id="bfeb7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bfeb7-104">SYNTAX</span></span>

### <span data-ttu-id="bfeb7-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bfeb7-105">List (Default)</span></span>
```
Get-AzsPlatformImage [-Publisher <String>] [-Offer <String>] [-Sku <String>] [-Location <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="bfeb7-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="bfeb7-106">Get</span></span>
```
Get-AzsPlatformImage -Publisher <String> -Offer <String> -Sku <String> -Version <String> [-Location <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="bfeb7-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="bfeb7-107">ResourceId</span></span>
```
Get-AzsPlatformImage -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="bfeb7-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bfeb7-108">DESCRIPTION</span></span>
<span data-ttu-id="bfeb7-109">Restituisce immagini della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="bfeb7-109">Returns platform images.</span></span>

## <span data-ttu-id="bfeb7-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bfeb7-110">EXAMPLES</span></span>

### <span data-ttu-id="bfeb7-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="bfeb7-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlatformImage
```

<span data-ttu-id="bfeb7-112">Restituisce le immagini della macchina virtuale caricate nel repository di immagini della piattaforma nella posizione locale.</span><span class="sxs-lookup"><span data-stu-id="bfeb7-112">Returns virtual machine images loaded into the platform image repository at the location local.</span></span>

### <span data-ttu-id="bfeb7-113">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="bfeb7-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsPlatformImage -Publisher Canonical -Offer UbuntuServer -Sku 16.04-LTS -Version 0.1.0
```

<span data-ttu-id="bfeb7-114">Ottenere una specifica immagine della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="bfeb7-114">Get a specific platform image.</span></span>

## <span data-ttu-id="bfeb7-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bfeb7-115">PARAMETERS</span></span>

### <span data-ttu-id="bfeb7-116">-Posizione</span><span class="sxs-lookup"><span data-stu-id="bfeb7-116">-Location</span></span>
<span data-ttu-id="bfeb7-117">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="bfeb7-117">Location of the resource.</span></span>

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

### <span data-ttu-id="bfeb7-118">-Offerta</span><span class="sxs-lookup"><span data-stu-id="bfeb7-118">-Offer</span></span>
<span data-ttu-id="bfeb7-119">Nome dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="bfeb7-119">Name of the offer.</span></span>

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

### <span data-ttu-id="bfeb7-120">-Publisher</span><span class="sxs-lookup"><span data-stu-id="bfeb7-120">-Publisher</span></span>
<span data-ttu-id="bfeb7-121">Nome dell'autore.</span><span class="sxs-lookup"><span data-stu-id="bfeb7-121">Name of the publisher.</span></span>

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

### <span data-ttu-id="bfeb7-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bfeb7-122">-ResourceId</span></span>
<span data-ttu-id="bfeb7-123">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="bfeb7-123">The resource id.</span></span>

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

### <span data-ttu-id="bfeb7-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="bfeb7-124">-Sku</span></span>
<span data-ttu-id="bfeb7-125">Nome dell'USK.</span><span class="sxs-lookup"><span data-stu-id="bfeb7-125">Name of the SKU.</span></span>

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

### <span data-ttu-id="bfeb7-126">-Versione</span><span class="sxs-lookup"><span data-stu-id="bfeb7-126">-Version</span></span>
<span data-ttu-id="bfeb7-127">Versione dell'immagine della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="bfeb7-127">The version of the platform image.</span></span>

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

### <span data-ttu-id="bfeb7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfeb7-128">CommonParameters</span></span>
<span data-ttu-id="bfeb7-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfeb7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfeb7-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfeb7-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfeb7-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bfeb7-131">INPUTS</span></span>

## <span data-ttu-id="bfeb7-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bfeb7-132">OUTPUTS</span></span>

### <span data-ttu-id="bfeb7-133">PlatformImageObject</span><span class="sxs-lookup"><span data-stu-id="bfeb7-133">PlatformImageObject</span></span>

## <span data-ttu-id="bfeb7-134">Note</span><span class="sxs-lookup"><span data-stu-id="bfeb7-134">NOTES</span></span>

## <span data-ttu-id="bfeb7-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bfeb7-135">RELATED LINKS</span></span>

