---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3e7eac7b9d23914aa909a111958d64cc9d4247d3
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030093"
---
# <span data-ttu-id="011d3-101">Get-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="011d3-101">Get-AzsVMExtension</span></span>

## <span data-ttu-id="011d3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="011d3-102">SYNOPSIS</span></span>
<span data-ttu-id="011d3-103">Restituisce le estensioni delle immagini della macchina virtuale attualmente disponibili.</span><span class="sxs-lookup"><span data-stu-id="011d3-103">Returns virtual machine image extensions currently available.</span></span>

## <span data-ttu-id="011d3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="011d3-104">SYNTAX</span></span>

### <span data-ttu-id="011d3-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="011d3-105">List (Default)</span></span>
```
Get-AzsVMExtension [-Publisher <String>] [-Type <String>] [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="011d3-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="011d3-106">Get</span></span>
```
Get-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="011d3-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="011d3-107">ResourceId</span></span>
```
Get-AzsVMExtension -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="011d3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="011d3-108">DESCRIPTION</span></span>
<span data-ttu-id="011d3-109">Restituisce le estensioni delle immagini della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="011d3-109">Returns virtual machine image extensions.</span></span>

## <span data-ttu-id="011d3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="011d3-110">EXAMPLES</span></span>

### <span data-ttu-id="011d3-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="011d3-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsVMExtension
```

<span data-ttu-id="011d3-112">Ottenere tutte le estensioni della VM in una posizione.</span><span class="sxs-lookup"><span data-stu-id="011d3-112">Get all VM extensions at a location.</span></span>

### <span data-ttu-id="011d3-113">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="011d3-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0"
```

<span data-ttu-id="011d3-114">Ottenere una specifica estensione della VM.</span><span class="sxs-lookup"><span data-stu-id="011d3-114">Get specific VM extension.</span></span>

## <span data-ttu-id="011d3-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="011d3-115">PARAMETERS</span></span>

### <span data-ttu-id="011d3-116">-Posizione</span><span class="sxs-lookup"><span data-stu-id="011d3-116">-Location</span></span>
<span data-ttu-id="011d3-117">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="011d3-117">Location of the resource.</span></span>

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

### <span data-ttu-id="011d3-118">-Publisher</span><span class="sxs-lookup"><span data-stu-id="011d3-118">-Publisher</span></span>
<span data-ttu-id="011d3-119">Nome dell'autore.</span><span class="sxs-lookup"><span data-stu-id="011d3-119">Name of the publisher.</span></span>

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

### <span data-ttu-id="011d3-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="011d3-120">-ResourceId</span></span>
<span data-ttu-id="011d3-121">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="011d3-121">The resource id.</span></span>

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

### <span data-ttu-id="011d3-122">-Digitare</span><span class="sxs-lookup"><span data-stu-id="011d3-122">-Type</span></span>
<span data-ttu-id="011d3-123">Tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="011d3-123">Type of extension.</span></span>

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

### <span data-ttu-id="011d3-124">-Versione</span><span class="sxs-lookup"><span data-stu-id="011d3-124">-Version</span></span>
<span data-ttu-id="011d3-125">Versione dell'estensione dell'immagine della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="011d3-125">The version of the virtual machine image extension.</span></span>

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

### <span data-ttu-id="011d3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="011d3-126">CommonParameters</span></span>
<span data-ttu-id="011d3-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="011d3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="011d3-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="011d3-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="011d3-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="011d3-129">INPUTS</span></span>

## <span data-ttu-id="011d3-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="011d3-130">OUTPUTS</span></span>

### <span data-ttu-id="011d3-131">VmExtensionObject</span><span class="sxs-lookup"><span data-stu-id="011d3-131">VmExtensionObject</span></span>

## <span data-ttu-id="011d3-132">Note</span><span class="sxs-lookup"><span data-stu-id="011d3-132">NOTES</span></span>

## <span data-ttu-id="011d3-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="011d3-133">RELATED LINKS</span></span>

