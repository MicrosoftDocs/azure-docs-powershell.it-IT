---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2f87690c20357cbff7f85a405dd6d3fae3a72dc9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491042"
---
# <span data-ttu-id="fe2ec-101">Remove-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="fe2ec-101">Remove-AzsVMExtension</span></span>

## <span data-ttu-id="fe2ec-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fe2ec-102">SYNOPSIS</span></span>
<span data-ttu-id="fe2ec-103">Elimina un'immagine dell'estensione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fe2ec-103">Deletes a virtual machine extension image.</span></span>

## <span data-ttu-id="fe2ec-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fe2ec-104">SYNTAX</span></span>

### <span data-ttu-id="fe2ec-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fe2ec-105">Delete (Default)</span></span>
```
Remove-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe2ec-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe2ec-106">ResourceId</span></span>
```
Remove-AzsVMExtension -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe2ec-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fe2ec-107">DESCRIPTION</span></span>
<span data-ttu-id="fe2ec-108">Elimina l'immagine dell'estensione della macchina virtuale specificata.</span><span class="sxs-lookup"><span data-stu-id="fe2ec-108">Deletes specified virtual machine extension image.</span></span>

## <span data-ttu-id="fe2ec-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fe2ec-109">EXAMPLES</span></span>

### <span data-ttu-id="fe2ec-110">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="fe2ec-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0"
```

<span data-ttu-id="fe2ec-111">Rimuovere un'estensione di immagine della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="fe2ec-111">Remove a platform image extension.</span></span>

## <span data-ttu-id="fe2ec-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fe2ec-112">PARAMETERS</span></span>

### <span data-ttu-id="fe2ec-113">-Force</span><span class="sxs-lookup"><span data-stu-id="fe2ec-113">-Force</span></span>
<span data-ttu-id="fe2ec-114">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="fe2ec-114">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe2ec-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="fe2ec-115">-Location</span></span>
<span data-ttu-id="fe2ec-116">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="fe2ec-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe2ec-117">-Publisher</span><span class="sxs-lookup"><span data-stu-id="fe2ec-117">-Publisher</span></span>
<span data-ttu-id="fe2ec-118">Nome dell'autore.</span><span class="sxs-lookup"><span data-stu-id="fe2ec-118">Name of the publisher.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe2ec-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe2ec-119">-ResourceId</span></span>
<span data-ttu-id="fe2ec-120">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="fe2ec-120">The resource id.</span></span>

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

### <span data-ttu-id="fe2ec-121">-Digitare</span><span class="sxs-lookup"><span data-stu-id="fe2ec-121">-Type</span></span>
<span data-ttu-id="fe2ec-122">Tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="fe2ec-122">Type of extension.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe2ec-123">-Versione</span><span class="sxs-lookup"><span data-stu-id="fe2ec-123">-Version</span></span>
<span data-ttu-id="fe2ec-124">Versione dell'immagine dell'estensione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fe2ec-124">The version of the virtual machine extension image.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe2ec-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fe2ec-125">-Confirm</span></span>
<span data-ttu-id="fe2ec-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe2ec-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe2ec-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe2ec-127">-WhatIf</span></span>
<span data-ttu-id="fe2ec-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fe2ec-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe2ec-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fe2ec-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe2ec-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe2ec-130">CommonParameters</span></span>
<span data-ttu-id="fe2ec-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe2ec-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe2ec-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe2ec-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe2ec-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fe2ec-133">INPUTS</span></span>

## <span data-ttu-id="fe2ec-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fe2ec-134">OUTPUTS</span></span>

## <span data-ttu-id="fe2ec-135">Note</span><span class="sxs-lookup"><span data-stu-id="fe2ec-135">NOTES</span></span>

## <span data-ttu-id="fe2ec-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fe2ec-136">RELATED LINKS</span></span>

