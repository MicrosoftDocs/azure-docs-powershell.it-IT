---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 54016a200b4304c7e37777202a8450fc9ad10e1e
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "93859070"
---
# <span data-ttu-id="44318-101">Start-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="44318-101">Start-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="44318-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="44318-102">SYNOPSIS</span></span>
<span data-ttu-id="44318-103">Avvia un processo di migrazione del contenitore per eseguire la migrazione dei contenitori alla condivisione di destinazione specificata.</span><span class="sxs-lookup"><span data-stu-id="44318-103">Starts a container migration job to migrate containers to the specified destination share.</span></span>

## <span data-ttu-id="44318-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="44318-104">SYNTAX</span></span>

```
Start-AzsStorageContainerMigration [-StorageAccountName] <String> [-Name] <String> [-ShareName] <String>
 [[-ResourceGroupName] <String>] [-FarmName] <String> [-DestinationShareUncPath] <String> [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44318-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="44318-105">DESCRIPTION</span></span>
<span data-ttu-id="44318-106">Avvia un processo di migrazione del contenitore per eseguire la migrazione dei contenitori alla condivisione di destinazione specificata.</span><span class="sxs-lookup"><span data-stu-id="44318-106">Starts a container migration job to migrate containers to the specified destination share.</span></span>

## <span data-ttu-id="44318-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="44318-107">EXAMPLES</span></span>

### <span data-ttu-id="44318-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="44318-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsStorageContainerMigration -StorageAccountName "accountTest" -Name "containerTest" -ShareName "shareTest" -FarmName "10e8d576-d73c-454c-a40a-aee31a77a5f0" -DestinationShareUncPath "\\***.***.***.***\C$\Test"
```

<span data-ttu-id="44318-109">Avvia una migrazione di contenitori.</span><span class="sxs-lookup"><span data-stu-id="44318-109">Starts a container migration.</span></span>

## <span data-ttu-id="44318-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="44318-110">PARAMETERS</span></span>

### <span data-ttu-id="44318-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="44318-111">-AsJob</span></span>
<span data-ttu-id="44318-112">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="44318-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="44318-113">-DestinationShareUncPath</span><span class="sxs-lookup"><span data-stu-id="44318-113">-DestinationShareUncPath</span></span>
<span data-ttu-id="44318-114">Percorso UNC della condivisione di destinazione per la migrazione.</span><span class="sxs-lookup"><span data-stu-id="44318-114">The UNC path of the destination share for migration.</span></span>

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

### <span data-ttu-id="44318-115">-Farmname</span><span class="sxs-lookup"><span data-stu-id="44318-115">-FarmName</span></span>
<span data-ttu-id="44318-116">ID farm.</span><span class="sxs-lookup"><span data-stu-id="44318-116">Farm Id.</span></span>

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

### <span data-ttu-id="44318-117">-Force</span><span class="sxs-lookup"><span data-stu-id="44318-117">-Force</span></span>
<span data-ttu-id="44318-118">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="44318-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="44318-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="44318-119">-Name</span></span>
<span data-ttu-id="44318-120">Nome del contenitore di cui eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="44318-120">The name of the container to be migrated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44318-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44318-121">-ResourceGroupName</span></span>
<span data-ttu-id="44318-122">Nome del gruppo di risorse in cui è stato registrato il provider di risorse di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="44318-122">The resource group name in which the storage resource provider was registered under.</span></span>

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

### <span data-ttu-id="44318-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="44318-123">-ShareName</span></span>
<span data-ttu-id="44318-124">Nome della condivisione contenente il contenitore specificato per la migrazione.</span><span class="sxs-lookup"><span data-stu-id="44318-124">Name of the share containing the container specified for migration.</span></span>

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

### <span data-ttu-id="44318-125">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="44318-125">-StorageAccountName</span></span>
<span data-ttu-id="44318-126">Nome dell'account di archiviazione in cui viene individuato il contenitore.</span><span class="sxs-lookup"><span data-stu-id="44318-126">The name of storage account where the container locates.</span></span>

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

### <span data-ttu-id="44318-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="44318-127">-Confirm</span></span>
<span data-ttu-id="44318-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44318-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44318-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44318-129">-WhatIf</span></span>
<span data-ttu-id="44318-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="44318-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44318-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="44318-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44318-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44318-132">CommonParameters</span></span>
<span data-ttu-id="44318-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44318-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44318-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44318-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44318-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="44318-135">INPUTS</span></span>

## <span data-ttu-id="44318-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="44318-136">OUTPUTS</span></span>

## <span data-ttu-id="44318-137">Note</span><span class="sxs-lookup"><span data-stu-id="44318-137">NOTES</span></span>

## <span data-ttu-id="44318-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="44318-138">RELATED LINKS</span></span>

