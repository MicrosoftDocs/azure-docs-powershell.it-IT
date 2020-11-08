---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: af9c5d2c5ebb547a6e09d2e4f4302ed2da470a39
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030516"
---
# <span data-ttu-id="dab99-101">Start-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="dab99-101">Start-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="dab99-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dab99-102">SYNOPSIS</span></span>
<span data-ttu-id="dab99-103">Avvia un processo di migrazione del contenitore per eseguire la migrazione dei contenitori alla condivisione di destinazione specificata.</span><span class="sxs-lookup"><span data-stu-id="dab99-103">Starts a container migration job to migrate containers to the specified destination share.</span></span>

## <span data-ttu-id="dab99-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dab99-104">SYNTAX</span></span>

```
Start-AzsStorageContainerMigration [-StorageAccountName] <String> [-ContainerName] <String>
 [-ShareName] <String> [[-ResourceGroupName] <String>] [-FarmName] <String> [-DestinationShareUncPath] <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dab99-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dab99-105">DESCRIPTION</span></span>
<span data-ttu-id="dab99-106">Avvia un processo di migrazione del contenitore per eseguire la migrazione dei contenitori alla condivisione di destinazione specificata.</span><span class="sxs-lookup"><span data-stu-id="dab99-106">Starts a container migration job to migrate containers to the specified destination share.</span></span>

## <span data-ttu-id="dab99-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dab99-107">EXAMPLES</span></span>

### <span data-ttu-id="dab99-108">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="dab99-108">EXAMPLE 1</span></span>
```
Start-AzsStorageContainerMigration -StorageAccountName "accountTest" -ContainerName "containerTest" -ShareName "shareTest" -FarmName "10e8d576-d73c-454c-a40a-aee31a77a5f0" -DestinationShareUncPath "\\***.***.***.***\C$\Test"
```

<span data-ttu-id="dab99-109">Avvia una migrazione di contenitori.</span><span class="sxs-lookup"><span data-stu-id="dab99-109">Starts a container migration.</span></span>

## <span data-ttu-id="dab99-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dab99-110">PARAMETERS</span></span>

### <span data-ttu-id="dab99-111">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="dab99-111">-StorageAccountName</span></span>
<span data-ttu-id="dab99-112">Nome dell'account di archiviazione in cui viene individuato il contenitore.</span><span class="sxs-lookup"><span data-stu-id="dab99-112">The name of storage account where the container locates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dab99-113">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="dab99-113">-ContainerName</span></span>
<span data-ttu-id="dab99-114">Nome del contenitore di cui eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="dab99-114">The name of the container to be migrated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dab99-115">-ShareName</span><span class="sxs-lookup"><span data-stu-id="dab99-115">-ShareName</span></span>
<span data-ttu-id="dab99-116">Nome della condivisione contenente il contenitore specificato per la migrazione.</span><span class="sxs-lookup"><span data-stu-id="dab99-116">Name of the share containing the container specified for migration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dab99-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dab99-117">-ResourceGroupName</span></span>
<span data-ttu-id="dab99-118">Nome del gruppo di risorse in cui è stato registrato il provider di risorse di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="dab99-118">The resource group name in which the storage resource provider was registered under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dab99-119">-Farmname</span><span class="sxs-lookup"><span data-stu-id="dab99-119">-FarmName</span></span>
<span data-ttu-id="dab99-120">ID farm.</span><span class="sxs-lookup"><span data-stu-id="dab99-120">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dab99-121">-DestinationShareUncPath</span><span class="sxs-lookup"><span data-stu-id="dab99-121">-DestinationShareUncPath</span></span>
<span data-ttu-id="dab99-122">Percorso UNC della condivisione di destinazione per la migrazione.</span><span class="sxs-lookup"><span data-stu-id="dab99-122">The UNC path of the destination share for migration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dab99-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dab99-123">-AsJob</span></span>
<span data-ttu-id="dab99-124">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="dab99-124">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="dab99-125">-Force</span><span class="sxs-lookup"><span data-stu-id="dab99-125">-Force</span></span>
<span data-ttu-id="dab99-126">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="dab99-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="dab99-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dab99-127">-WhatIf</span></span>
<span data-ttu-id="dab99-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dab99-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dab99-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dab99-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dab99-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dab99-130">-Confirm</span></span>
<span data-ttu-id="dab99-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dab99-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dab99-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dab99-132">CommonParameters</span></span>
<span data-ttu-id="dab99-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dab99-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dab99-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dab99-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dab99-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dab99-135">INPUTS</span></span>

## <span data-ttu-id="dab99-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dab99-136">OUTPUTS</span></span>

## <span data-ttu-id="dab99-137">Note</span><span class="sxs-lookup"><span data-stu-id="dab99-137">NOTES</span></span>

## <span data-ttu-id="dab99-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dab99-138">RELATED LINKS</span></span>
