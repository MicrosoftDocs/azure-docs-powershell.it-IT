---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c7dff6c2d9c191d852420ab2c2017a0b9d1cf8d3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93685236"
---
# <span data-ttu-id="228a7-101">Start-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="228a7-101">Start-AzsBackup</span></span>

## <span data-ttu-id="228a7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="228a7-102">SYNOPSIS</span></span>
<span data-ttu-id="228a7-103">Eseguire il backup di una posizione specifica.</span><span class="sxs-lookup"><span data-stu-id="228a7-103">Back up a specific location.</span></span>

## <span data-ttu-id="228a7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="228a7-104">SYNTAX</span></span>

### <span data-ttu-id="228a7-105">CreateBackup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="228a7-105">CreateBackup (Default)</span></span>
```
Start-AzsBackup [-ResourceGroupName <String>] [-Location <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="228a7-106">CreateBackup_FromResourceId</span><span class="sxs-lookup"><span data-stu-id="228a7-106">CreateBackup_FromResourceId</span></span>
```
Start-AzsBackup -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="228a7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="228a7-107">DESCRIPTION</span></span>
<span data-ttu-id="228a7-108">Eseguire il backup di una posizione specifica.</span><span class="sxs-lookup"><span data-stu-id="228a7-108">Back up a specific location.</span></span>

## <span data-ttu-id="228a7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="228a7-109">EXAMPLES</span></span>

### <span data-ttu-id="228a7-110">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="228a7-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsBackup
```

<span data-ttu-id="228a7-111">Avviare un backup di Azure stack.</span><span class="sxs-lookup"><span data-stu-id="228a7-111">Start an Azure Stack backup.</span></span>

## <span data-ttu-id="228a7-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="228a7-112">PARAMETERS</span></span>

### <span data-ttu-id="228a7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="228a7-113">-AsJob</span></span>
<span data-ttu-id="228a7-114">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="228a7-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="228a7-115">-Force</span><span class="sxs-lookup"><span data-stu-id="228a7-115">-Force</span></span>
<span data-ttu-id="228a7-116">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="228a7-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="228a7-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="228a7-117">-Location</span></span>
<span data-ttu-id="228a7-118">Nome del percorso di backup.</span><span class="sxs-lookup"><span data-stu-id="228a7-118">Name of the backup location.</span></span>

```yaml
Type: String
Parameter Sets: CreateBackup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="228a7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="228a7-119">-ResourceGroupName</span></span>
<span data-ttu-id="228a7-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="228a7-120">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: CreateBackup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="228a7-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="228a7-121">-ResourceId</span></span>
<span data-ttu-id="228a7-122">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="228a7-122">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: CreateBackup_FromResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="228a7-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="228a7-123">-Confirm</span></span>
<span data-ttu-id="228a7-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="228a7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="228a7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="228a7-125">-WhatIf</span></span>
<span data-ttu-id="228a7-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="228a7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="228a7-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="228a7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="228a7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="228a7-128">CommonParameters</span></span>
<span data-ttu-id="228a7-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="228a7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="228a7-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="228a7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="228a7-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="228a7-131">INPUTS</span></span>

## <span data-ttu-id="228a7-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="228a7-132">OUTPUTS</span></span>

### <span data-ttu-id="228a7-133">Microsoft. AzureStack. Management. backup. admin. Models. LongRunningOperationStatus</span><span class="sxs-lookup"><span data-stu-id="228a7-133">Microsoft.AzureStack.Management.Backup.Admin.Models.LongRunningOperationStatus</span></span>

## <span data-ttu-id="228a7-134">Note</span><span class="sxs-lookup"><span data-stu-id="228a7-134">NOTES</span></span>

## <span data-ttu-id="228a7-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="228a7-135">RELATED LINKS</span></span>

