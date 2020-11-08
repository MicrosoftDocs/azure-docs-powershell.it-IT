---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 573a47b3684020817130e1d41c764abef717de0a
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030267"
---
# <span data-ttu-id="03038-101">Restore-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="03038-101">Restore-AzsBackup</span></span>

## <span data-ttu-id="03038-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="03038-102">SYNOPSIS</span></span>
<span data-ttu-id="03038-103">Ripristinare un backup.</span><span class="sxs-lookup"><span data-stu-id="03038-103">Restore a backup.</span></span>

## <span data-ttu-id="03038-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="03038-104">SYNTAX</span></span>

### <span data-ttu-id="03038-105">Backups_Restore (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="03038-105">Backups_Restore (Default)</span></span>
```
Restore-AzsBackup [-ResourceGroupName <String>] -Name <String> [-Location <String>] [-AsJob] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03038-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="03038-106">ResourceId</span></span>
```
Restore-AzsBackup -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03038-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="03038-107">DESCRIPTION</span></span>
<span data-ttu-id="03038-108">Ripristinare un backup.</span><span class="sxs-lookup"><span data-stu-id="03038-108">Restore a backup.</span></span>

## <span data-ttu-id="03038-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="03038-109">EXAMPLES</span></span>

### <span data-ttu-id="03038-110">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="03038-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Restore-AzsBackup -Backup 4e90bd2f-c7ab-47a3-a3c7-908cddd1ad0e
```

<span data-ttu-id="03038-111">Eseguire il ripristino da un backup di Azure stack.</span><span class="sxs-lookup"><span data-stu-id="03038-111">Restore from an Azure Stack backup.</span></span>

## <span data-ttu-id="03038-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="03038-112">PARAMETERS</span></span>

### <span data-ttu-id="03038-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03038-113">-AsJob</span></span>
<span data-ttu-id="03038-114">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="03038-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="03038-115">-Force</span><span class="sxs-lookup"><span data-stu-id="03038-115">-Force</span></span>
<span data-ttu-id="03038-116">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="03038-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="03038-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="03038-117">-Location</span></span>
<span data-ttu-id="03038-118">Nome della posizione in cui eseguire il backup.</span><span class="sxs-lookup"><span data-stu-id="03038-118">Name of location to backup.</span></span>

```yaml
Type: String
Parameter Sets: Backups_Restore
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03038-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="03038-119">-Name</span></span>
<span data-ttu-id="03038-120">Nome del backup.</span><span class="sxs-lookup"><span data-stu-id="03038-120">Name of the backup.</span></span>

```yaml
Type: String
Parameter Sets: Backups_Restore
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03038-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03038-121">-ResourceGroupName</span></span>
<span data-ttu-id="03038-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="03038-122">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: Backups_Restore
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03038-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="03038-123">-ResourceId</span></span>
<span data-ttu-id="03038-124">{{Fill ResourceId Description}}</span><span class="sxs-lookup"><span data-stu-id="03038-124">{{Fill ResourceId Description}}</span></span>

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

### <span data-ttu-id="03038-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="03038-125">-Confirm</span></span>
<span data-ttu-id="03038-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03038-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03038-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03038-127">-WhatIf</span></span>
<span data-ttu-id="03038-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="03038-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03038-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="03038-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03038-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03038-130">CommonParameters</span></span>
<span data-ttu-id="03038-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03038-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03038-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03038-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03038-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="03038-133">INPUTS</span></span>

## <span data-ttu-id="03038-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="03038-134">OUTPUTS</span></span>

## <span data-ttu-id="03038-135">Note</span><span class="sxs-lookup"><span data-stu-id="03038-135">NOTES</span></span>

## <span data-ttu-id="03038-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="03038-136">RELATED LINKS</span></span>

