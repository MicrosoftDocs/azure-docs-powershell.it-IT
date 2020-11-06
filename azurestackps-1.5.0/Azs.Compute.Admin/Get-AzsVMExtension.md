---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f81cf1ed28b822a0686d1db71541585023f1e57b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491157"
---
# <span data-ttu-id="d17cc-101">Get-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="d17cc-101">Get-AzsVMExtension</span></span>

## <span data-ttu-id="d17cc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d17cc-102">SYNOPSIS</span></span>
<span data-ttu-id="d17cc-103">Restituisce le estensioni delle immagini della macchina virtuale attualmente disponibili.</span><span class="sxs-lookup"><span data-stu-id="d17cc-103">Returns virtual machine image extensions currently available.</span></span>

## <span data-ttu-id="d17cc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d17cc-104">SYNTAX</span></span>

### <span data-ttu-id="d17cc-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d17cc-105">List (Default)</span></span>
```
Get-AzsVMExtension [-Publisher <String>] [-Type <String>] [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="d17cc-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="d17cc-106">Get</span></span>
```
Get-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="d17cc-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d17cc-107">ResourceId</span></span>
```
Get-AzsVMExtension -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="d17cc-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d17cc-108">DESCRIPTION</span></span>
<span data-ttu-id="d17cc-109">Restituisce le estensioni delle immagini della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d17cc-109">Returns virtual machine image extensions.</span></span>

## <span data-ttu-id="d17cc-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d17cc-110">EXAMPLES</span></span>

### <span data-ttu-id="d17cc-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d17cc-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsVMExtension
```

<span data-ttu-id="d17cc-112">Ottenere tutte le estensioni della VM in una posizione.</span><span class="sxs-lookup"><span data-stu-id="d17cc-112">Get all VM extensions at a location.</span></span>

### <span data-ttu-id="d17cc-113">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="d17cc-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0"
```

<span data-ttu-id="d17cc-114">Ottenere una specifica estensione della VM.</span><span class="sxs-lookup"><span data-stu-id="d17cc-114">Get specific VM extension.</span></span>

## <span data-ttu-id="d17cc-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d17cc-115">PARAMETERS</span></span>

### <span data-ttu-id="d17cc-116">-Posizione</span><span class="sxs-lookup"><span data-stu-id="d17cc-116">-Location</span></span>
<span data-ttu-id="d17cc-117">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="d17cc-117">Location of the resource.</span></span>

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

### <span data-ttu-id="d17cc-118">-Publisher</span><span class="sxs-lookup"><span data-stu-id="d17cc-118">-Publisher</span></span>
<span data-ttu-id="d17cc-119">Nome dell'autore.</span><span class="sxs-lookup"><span data-stu-id="d17cc-119">Name of the publisher.</span></span>

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

### <span data-ttu-id="d17cc-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d17cc-120">-ResourceId</span></span>
<span data-ttu-id="d17cc-121">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="d17cc-121">The resource id.</span></span>

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

### <span data-ttu-id="d17cc-122">-Digitare</span><span class="sxs-lookup"><span data-stu-id="d17cc-122">-Type</span></span>
<span data-ttu-id="d17cc-123">Tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="d17cc-123">Type of extension.</span></span>

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

### <span data-ttu-id="d17cc-124">-Versione</span><span class="sxs-lookup"><span data-stu-id="d17cc-124">-Version</span></span>
<span data-ttu-id="d17cc-125">Versione dell'estensione dell'immagine della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d17cc-125">The version of the virtual machine image extension.</span></span>

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

### <span data-ttu-id="d17cc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d17cc-126">CommonParameters</span></span>
<span data-ttu-id="d17cc-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d17cc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d17cc-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d17cc-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d17cc-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d17cc-129">INPUTS</span></span>

## <span data-ttu-id="d17cc-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d17cc-130">OUTPUTS</span></span>

### <span data-ttu-id="d17cc-131">VmExtensionObject</span><span class="sxs-lookup"><span data-stu-id="d17cc-131">VmExtensionObject</span></span>

## <span data-ttu-id="d17cc-132">Note</span><span class="sxs-lookup"><span data-stu-id="d17cc-132">NOTES</span></span>

## <span data-ttu-id="d17cc-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d17cc-133">RELATED LINKS</span></span>
