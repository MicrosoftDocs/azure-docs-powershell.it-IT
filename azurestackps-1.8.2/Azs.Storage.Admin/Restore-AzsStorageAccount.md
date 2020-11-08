---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 769567562199d33116911f1f1f5e258ae2decbbe
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030369"
---
# <span data-ttu-id="f4af7-101">Restore-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f4af7-101">Restore-AzsStorageAccount</span></span>

## <span data-ttu-id="f4af7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f4af7-102">SYNOPSIS</span></span>
<span data-ttu-id="f4af7-103">Annullare l'eliminazione di un account di archiviazione eliminato.</span><span class="sxs-lookup"><span data-stu-id="f4af7-103">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="f4af7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f4af7-104">SYNTAX</span></span>

### <span data-ttu-id="f4af7-105">Annulla eliminazione (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f4af7-105">Undelete (Default)</span></span>
```
Restore-AzsStorageAccount -FarmName <String> -Name <String> [-ResourceGroupName <String>] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4af7-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4af7-106">ResourceId</span></span>
```
Restore-AzsStorageAccount -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4af7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4af7-107">DESCRIPTION</span></span>
<span data-ttu-id="f4af7-108">Annullare l'eliminazione di un account di archiviazione eliminato.</span><span class="sxs-lookup"><span data-stu-id="f4af7-108">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="f4af7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f4af7-109">EXAMPLES</span></span>

### <span data-ttu-id="f4af7-110">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="f4af7-110">EXAMPLE 1</span></span>
```
Restore-AzsStorageAccount -FarmName "90987d65-eb60-42ae-b735-18bcd7ff69da" -Name "83fe9ac0-f1e7-433e-b04c-c61ae0712093"
```

<span data-ttu-id="f4af7-111">Annullare l'eliminazione di un account di archiviazione eliminato.</span><span class="sxs-lookup"><span data-stu-id="f4af7-111">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="f4af7-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f4af7-112">PARAMETERS</span></span>

### <span data-ttu-id="f4af7-113">-Farmname</span><span class="sxs-lookup"><span data-stu-id="f4af7-113">-FarmName</span></span>
<span data-ttu-id="f4af7-114">ID farm.</span><span class="sxs-lookup"><span data-stu-id="f4af7-114">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: Undelete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4af7-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="f4af7-115">-Name</span></span>
<span data-ttu-id="f4af7-116">ID account di archiviazione interno, che non è visibile al tenant.</span><span class="sxs-lookup"><span data-stu-id="f4af7-116">Internal storage account ID, which is not visible to tenant.</span></span>

```yaml
Type: String
Parameter Sets: Undelete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4af7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4af7-117">-ResourceGroupName</span></span>
<span data-ttu-id="f4af7-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f4af7-118">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: Undelete
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4af7-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4af7-119">-ResourceId</span></span>
<span data-ttu-id="f4af7-120">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="f4af7-120">The resource id.</span></span>

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

### <span data-ttu-id="f4af7-121">-Force</span><span class="sxs-lookup"><span data-stu-id="f4af7-121">-Force</span></span>
<span data-ttu-id="f4af7-122">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="f4af7-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f4af7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4af7-123">-WhatIf</span></span>
<span data-ttu-id="f4af7-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f4af7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4af7-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f4af7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4af7-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f4af7-126">-Confirm</span></span>
<span data-ttu-id="f4af7-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4af7-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4af7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4af7-128">CommonParameters</span></span>
<span data-ttu-id="f4af7-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4af7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4af7-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4af7-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4af7-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f4af7-131">INPUTS</span></span>

## <span data-ttu-id="f4af7-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f4af7-132">OUTPUTS</span></span>

## <span data-ttu-id="f4af7-133">Note</span><span class="sxs-lookup"><span data-stu-id="f4af7-133">NOTES</span></span>

## <span data-ttu-id="f4af7-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f4af7-134">RELATED LINKS</span></span>
