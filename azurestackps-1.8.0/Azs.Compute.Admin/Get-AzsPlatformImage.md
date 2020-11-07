---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 403f980af6b00272ca67b3ba180808ba8c82ebce
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "93859053"
---
# <span data-ttu-id="8ee23-101">Get-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="8ee23-101">Get-AzsPlatformImage</span></span>

## <span data-ttu-id="8ee23-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8ee23-102">SYNOPSIS</span></span>
<span data-ttu-id="8ee23-103">Restituisce le immagini della macchina virtuale caricate nel repository di immagini della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="8ee23-103">Returns virtual machine images loaded into the platform image repository.</span></span>

## <span data-ttu-id="8ee23-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8ee23-104">SYNTAX</span></span>

### <span data-ttu-id="8ee23-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8ee23-105">List (Default)</span></span>
```
Get-AzsPlatformImage [-Publisher <String>] [-Offer <String>] [-Sku <String>] [-Location <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="8ee23-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="8ee23-106">Get</span></span>
```
Get-AzsPlatformImage -Publisher <String> -Offer <String> -Sku <String> -Version <String> [-Location <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="8ee23-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ee23-107">ResourceId</span></span>
```
Get-AzsPlatformImage -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="8ee23-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8ee23-108">DESCRIPTION</span></span>
<span data-ttu-id="8ee23-109">Restituisce immagini della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="8ee23-109">Returns platform images.</span></span>

## <span data-ttu-id="8ee23-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8ee23-110">EXAMPLES</span></span>

### <span data-ttu-id="8ee23-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8ee23-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlatformImage
```

<span data-ttu-id="8ee23-112">Restituisce le immagini della macchina virtuale caricate nel repository di immagini della piattaforma nella posizione locale.</span><span class="sxs-lookup"><span data-stu-id="8ee23-112">Returns virtual machine images loaded into the platform image repository at the location local.</span></span>

### <span data-ttu-id="8ee23-113">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="8ee23-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsPlatformImage -Publisher Canonical -Offer UbuntuServer -Sku 16.04-LTS -Version 0.1.0
```

<span data-ttu-id="8ee23-114">Ottenere una specifica immagine della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="8ee23-114">Get a specific platform image.</span></span>

## <span data-ttu-id="8ee23-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8ee23-115">PARAMETERS</span></span>

### <span data-ttu-id="8ee23-116">-Posizione</span><span class="sxs-lookup"><span data-stu-id="8ee23-116">-Location</span></span>
<span data-ttu-id="8ee23-117">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="8ee23-117">Location of the resource.</span></span>

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

### <span data-ttu-id="8ee23-118">-Offerta</span><span class="sxs-lookup"><span data-stu-id="8ee23-118">-Offer</span></span>
<span data-ttu-id="8ee23-119">Nome dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="8ee23-119">Name of the offer.</span></span>

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

### <span data-ttu-id="8ee23-120">-Publisher</span><span class="sxs-lookup"><span data-stu-id="8ee23-120">-Publisher</span></span>
<span data-ttu-id="8ee23-121">Nome dell'autore.</span><span class="sxs-lookup"><span data-stu-id="8ee23-121">Name of the publisher.</span></span>

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

### <span data-ttu-id="8ee23-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ee23-122">-ResourceId</span></span>
<span data-ttu-id="8ee23-123">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="8ee23-123">The resource id.</span></span>

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

### <span data-ttu-id="8ee23-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="8ee23-124">-Sku</span></span>
<span data-ttu-id="8ee23-125">Nome dell'USK.</span><span class="sxs-lookup"><span data-stu-id="8ee23-125">Name of the SKU.</span></span>

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

### <span data-ttu-id="8ee23-126">-Versione</span><span class="sxs-lookup"><span data-stu-id="8ee23-126">-Version</span></span>
<span data-ttu-id="8ee23-127">Versione dell'immagine della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="8ee23-127">The version of the platform image.</span></span>

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

### <span data-ttu-id="8ee23-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ee23-128">CommonParameters</span></span>
<span data-ttu-id="8ee23-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ee23-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ee23-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ee23-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ee23-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8ee23-131">INPUTS</span></span>

## <span data-ttu-id="8ee23-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8ee23-132">OUTPUTS</span></span>

### <span data-ttu-id="8ee23-133">PlatformImageObject</span><span class="sxs-lookup"><span data-stu-id="8ee23-133">PlatformImageObject</span></span>

## <span data-ttu-id="8ee23-134">Note</span><span class="sxs-lookup"><span data-stu-id="8ee23-134">NOTES</span></span>

## <span data-ttu-id="8ee23-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8ee23-135">RELATED LINKS</span></span>

