---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 573a47b3684020817130e1d41c764abef717de0a
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93860066"
---
# <span data-ttu-id="36d84-101">Restore-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="36d84-101">Restore-AzsBackup</span></span>

## <span data-ttu-id="36d84-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="36d84-102">SYNOPSIS</span></span>
<span data-ttu-id="36d84-103">Ripristinare un backup.</span><span class="sxs-lookup"><span data-stu-id="36d84-103">Restore a backup.</span></span>

## <span data-ttu-id="36d84-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="36d84-104">SYNTAX</span></span>

### <span data-ttu-id="36d84-105">Backups_Restore (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="36d84-105">Backups_Restore (Default)</span></span>
```
Restore-AzsBackup [-ResourceGroupName <String>] -Name <String> [-Location <String>] [-AsJob] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36d84-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="36d84-106">ResourceId</span></span>
```
Restore-AzsBackup -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36d84-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="36d84-107">DESCRIPTION</span></span>
<span data-ttu-id="36d84-108">Ripristinare un backup.</span><span class="sxs-lookup"><span data-stu-id="36d84-108">Restore a backup.</span></span>

## <span data-ttu-id="36d84-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="36d84-109">EXAMPLES</span></span>

### <span data-ttu-id="36d84-110">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="36d84-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Restore-AzsBackup -Backup 4e90bd2f-c7ab-47a3-a3c7-908cddd1ad0e
```

<span data-ttu-id="36d84-111">Eseguire il ripristino da un backup di Azure stack.</span><span class="sxs-lookup"><span data-stu-id="36d84-111">Restore from an Azure Stack backup.</span></span>

## <span data-ttu-id="36d84-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="36d84-112">PARAMETERS</span></span>

### <span data-ttu-id="36d84-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="36d84-113">-AsJob</span></span>
<span data-ttu-id="36d84-114">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="36d84-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="36d84-115">-Force</span><span class="sxs-lookup"><span data-stu-id="36d84-115">-Force</span></span>
<span data-ttu-id="36d84-116">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="36d84-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="36d84-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="36d84-117">-Location</span></span>
<span data-ttu-id="36d84-118">Nome della posizione in cui eseguire il backup.</span><span class="sxs-lookup"><span data-stu-id="36d84-118">Name of location to backup.</span></span>

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

### <span data-ttu-id="36d84-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="36d84-119">-Name</span></span>
<span data-ttu-id="36d84-120">Nome del backup.</span><span class="sxs-lookup"><span data-stu-id="36d84-120">Name of the backup.</span></span>

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

### <span data-ttu-id="36d84-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36d84-121">-ResourceGroupName</span></span>
<span data-ttu-id="36d84-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="36d84-122">Name of the resource group.</span></span>

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

### <span data-ttu-id="36d84-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36d84-123">-ResourceId</span></span>
<span data-ttu-id="36d84-124">{{Fill ResourceId Description}}</span><span class="sxs-lookup"><span data-stu-id="36d84-124">{{Fill ResourceId Description}}</span></span>

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

### <span data-ttu-id="36d84-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="36d84-125">-Confirm</span></span>
<span data-ttu-id="36d84-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36d84-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36d84-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36d84-127">-WhatIf</span></span>
<span data-ttu-id="36d84-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="36d84-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36d84-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="36d84-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36d84-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36d84-130">CommonParameters</span></span>
<span data-ttu-id="36d84-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36d84-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36d84-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36d84-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36d84-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="36d84-133">INPUTS</span></span>

## <span data-ttu-id="36d84-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="36d84-134">OUTPUTS</span></span>

## <span data-ttu-id="36d84-135">Note</span><span class="sxs-lookup"><span data-stu-id="36d84-135">NOTES</span></span>

## <span data-ttu-id="36d84-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="36d84-136">RELATED LINKS</span></span>

