---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0983e05a36de72148571ccbbc7f1454343ad393a
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030096"
---
# <span data-ttu-id="2ab9a-101">Remove-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="2ab9a-101">Remove-AzsStorageQuota</span></span>

## <span data-ttu-id="2ab9a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2ab9a-102">SYNOPSIS</span></span>
<span data-ttu-id="2ab9a-103">Eliminare una quota esistente</span><span class="sxs-lookup"><span data-stu-id="2ab9a-103">Delete an existing quota</span></span>

## <span data-ttu-id="2ab9a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2ab9a-104">SYNTAX</span></span>

### <span data-ttu-id="2ab9a-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2ab9a-105">Delete (Default)</span></span>
```
Remove-AzsStorageQuota -Name <String> [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ab9a-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ab9a-106">ResourceId</span></span>
```
Remove-AzsStorageQuota -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ab9a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2ab9a-107">DESCRIPTION</span></span>
<span data-ttu-id="2ab9a-108">Eliminare una quota esistente</span><span class="sxs-lookup"><span data-stu-id="2ab9a-108">Delete an existing quota</span></span>

## <span data-ttu-id="2ab9a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2ab9a-109">EXAMPLES</span></span>

### <span data-ttu-id="2ab9a-110">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="2ab9a-110">EXAMPLE 1</span></span>
```
Remove-AzsStorageQuota -Name 'TestDeleteStorageQuota'
```

<span data-ttu-id="2ab9a-111">Rimuovere una quota di archiviazione per nome.</span><span class="sxs-lookup"><span data-stu-id="2ab9a-111">Remove a storage quota by name.</span></span>

### <span data-ttu-id="2ab9a-112">ESEMPIO 2</span><span class="sxs-lookup"><span data-stu-id="2ab9a-112">EXAMPLE 2</span></span>
```
Get-AzsStorageQuota -Name 'testquota' | Remove-AzsStorageQuota
```

<span data-ttu-id="2ab9a-113">Rimuovere una quota di archiviazione tramite piping.</span><span class="sxs-lookup"><span data-stu-id="2ab9a-113">Remove a storage quota by piping.</span></span>

## <span data-ttu-id="2ab9a-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2ab9a-114">PARAMETERS</span></span>

### <span data-ttu-id="2ab9a-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="2ab9a-115">-Name</span></span>
<span data-ttu-id="2ab9a-116">Nome della quota di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2ab9a-116">The name of the storage quota.</span></span>

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

### <span data-ttu-id="2ab9a-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="2ab9a-117">-Location</span></span>
<span data-ttu-id="2ab9a-118">Posizione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="2ab9a-118">Resource location.</span></span>

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

### <span data-ttu-id="2ab9a-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ab9a-119">-ResourceId</span></span>
<span data-ttu-id="2ab9a-120">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="2ab9a-120">The resource id.</span></span>

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

### <span data-ttu-id="2ab9a-121">-Force</span><span class="sxs-lookup"><span data-stu-id="2ab9a-121">-Force</span></span>
<span data-ttu-id="2ab9a-122">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="2ab9a-122">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="2ab9a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ab9a-123">-WhatIf</span></span>
<span data-ttu-id="2ab9a-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2ab9a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ab9a-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2ab9a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ab9a-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2ab9a-126">-Confirm</span></span>
<span data-ttu-id="2ab9a-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ab9a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ab9a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ab9a-128">CommonParameters</span></span>
<span data-ttu-id="2ab9a-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ab9a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ab9a-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ab9a-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ab9a-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2ab9a-131">INPUTS</span></span>

## <span data-ttu-id="2ab9a-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2ab9a-132">OUTPUTS</span></span>

## <span data-ttu-id="2ab9a-133">Note</span><span class="sxs-lookup"><span data-stu-id="2ab9a-133">NOTES</span></span>

## <span data-ttu-id="2ab9a-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2ab9a-134">RELATED LINKS</span></span>
