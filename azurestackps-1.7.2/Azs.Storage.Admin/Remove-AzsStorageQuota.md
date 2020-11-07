---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 85b62b8ffbdcdcefff5bbb5c984a19ef0b7cb644
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93858033"
---
# <span data-ttu-id="c4d89-101">Remove-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="c4d89-101">Remove-AzsStorageQuota</span></span>

## <span data-ttu-id="c4d89-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c4d89-102">SYNOPSIS</span></span>
<span data-ttu-id="c4d89-103">Eliminare una quota esistente</span><span class="sxs-lookup"><span data-stu-id="c4d89-103">Delete an existing quota</span></span>

## <span data-ttu-id="c4d89-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c4d89-104">SYNTAX</span></span>

### <span data-ttu-id="c4d89-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c4d89-105">Delete (Default)</span></span>
```
Remove-AzsStorageQuota -Name <String> [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4d89-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4d89-106">ResourceId</span></span>
```
Remove-AzsStorageQuota -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4d89-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c4d89-107">DESCRIPTION</span></span>
<span data-ttu-id="c4d89-108">Eliminare una quota esistente</span><span class="sxs-lookup"><span data-stu-id="c4d89-108">Delete an existing quota</span></span>

## <span data-ttu-id="c4d89-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c4d89-109">EXAMPLES</span></span>

### <span data-ttu-id="c4d89-110">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c4d89-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsStorageQuota -Name 'TestDeleteStorageQuota'
```

<span data-ttu-id="c4d89-111">Rimuovere una quota di archiviazione per nome.</span><span class="sxs-lookup"><span data-stu-id="c4d89-111">Remove a storage quota by name.</span></span>

### <span data-ttu-id="c4d89-112">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="c4d89-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageQuota -Name 'testquota' | Remove-AzsStorageQuota
```

<span data-ttu-id="c4d89-113">Rimuovere una quota di archiviazione tramite piping.</span><span class="sxs-lookup"><span data-stu-id="c4d89-113">Remove a storage quota by piping.</span></span>

## <span data-ttu-id="c4d89-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c4d89-114">PARAMETERS</span></span>

### <span data-ttu-id="c4d89-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c4d89-115">-Force</span></span>
<span data-ttu-id="c4d89-116">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="c4d89-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="c4d89-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="c4d89-117">-Location</span></span>
<span data-ttu-id="c4d89-118">Posizione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="c4d89-118">Resource location.</span></span>

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

### <span data-ttu-id="c4d89-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="c4d89-119">-Name</span></span>
<span data-ttu-id="c4d89-120">Nome della quota di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c4d89-120">The name of the storage quota.</span></span>

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

### <span data-ttu-id="c4d89-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4d89-121">-ResourceId</span></span>
<span data-ttu-id="c4d89-122">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="c4d89-122">The resource id.</span></span>

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

### <span data-ttu-id="c4d89-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c4d89-123">-Confirm</span></span>
<span data-ttu-id="c4d89-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4d89-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4d89-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4d89-125">-WhatIf</span></span>
<span data-ttu-id="c4d89-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c4d89-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4d89-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c4d89-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4d89-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4d89-128">CommonParameters</span></span>
<span data-ttu-id="c4d89-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4d89-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4d89-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4d89-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4d89-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c4d89-131">INPUTS</span></span>

## <span data-ttu-id="c4d89-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c4d89-132">OUTPUTS</span></span>

## <span data-ttu-id="c4d89-133">Note</span><span class="sxs-lookup"><span data-stu-id="c4d89-133">NOTES</span></span>

## <span data-ttu-id="c4d89-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c4d89-134">RELATED LINKS</span></span>

