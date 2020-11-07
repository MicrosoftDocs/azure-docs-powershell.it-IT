---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 54016a200b4304c7e37777202a8450fc9ad10e1e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673785"
---
# <span data-ttu-id="0c988-101">Start-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="0c988-101">Start-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="0c988-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0c988-102">SYNOPSIS</span></span>
<span data-ttu-id="0c988-103">Avvia un processo di migrazione del contenitore per eseguire la migrazione dei contenitori alla condivisione di destinazione specificata.</span><span class="sxs-lookup"><span data-stu-id="0c988-103">Starts a container migration job to migrate containers to the specified destination share.</span></span>

## <span data-ttu-id="0c988-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0c988-104">SYNTAX</span></span>

```
Start-AzsStorageContainerMigration [-StorageAccountName] <String> [-Name] <String> [-ShareName] <String>
 [[-ResourceGroupName] <String>] [-FarmName] <String> [-DestinationShareUncPath] <String> [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c988-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c988-105">DESCRIPTION</span></span>
<span data-ttu-id="0c988-106">Avvia un processo di migrazione del contenitore per eseguire la migrazione dei contenitori alla condivisione di destinazione specificata.</span><span class="sxs-lookup"><span data-stu-id="0c988-106">Starts a container migration job to migrate containers to the specified destination share.</span></span>

## <span data-ttu-id="0c988-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0c988-107">EXAMPLES</span></span>

### <span data-ttu-id="0c988-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0c988-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsStorageContainerMigration -StorageAccountName "accountTest" -Name "containerTest" -ShareName "shareTest" -FarmName "10e8d576-d73c-454c-a40a-aee31a77a5f0" -DestinationShareUncPath "\\***.***.***.***\C$\Test"
```

<span data-ttu-id="0c988-109">Avvia una migrazione di contenitori.</span><span class="sxs-lookup"><span data-stu-id="0c988-109">Starts a container migration.</span></span>

## <span data-ttu-id="0c988-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0c988-110">PARAMETERS</span></span>

### <span data-ttu-id="0c988-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0c988-111">-AsJob</span></span>
<span data-ttu-id="0c988-112">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="0c988-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="0c988-113">-DestinationShareUncPath</span><span class="sxs-lookup"><span data-stu-id="0c988-113">-DestinationShareUncPath</span></span>
<span data-ttu-id="0c988-114">Percorso UNC della condivisione di destinazione per la migrazione.</span><span class="sxs-lookup"><span data-stu-id="0c988-114">The UNC path of the destination share for migration.</span></span>

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

### <span data-ttu-id="0c988-115">-Farmname</span><span class="sxs-lookup"><span data-stu-id="0c988-115">-FarmName</span></span>
<span data-ttu-id="0c988-116">ID farm.</span><span class="sxs-lookup"><span data-stu-id="0c988-116">Farm Id.</span></span>

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

### <span data-ttu-id="0c988-117">-Force</span><span class="sxs-lookup"><span data-stu-id="0c988-117">-Force</span></span>
<span data-ttu-id="0c988-118">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="0c988-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0c988-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="0c988-119">-Name</span></span>
<span data-ttu-id="0c988-120">Nome del contenitore di cui eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="0c988-120">The name of the container to be migrated.</span></span>

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

### <span data-ttu-id="0c988-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c988-121">-ResourceGroupName</span></span>
<span data-ttu-id="0c988-122">Nome del gruppo di risorse in cui è stato registrato il provider di risorse di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="0c988-122">The resource group name in which the storage resource provider was registered under.</span></span>

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

### <span data-ttu-id="0c988-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="0c988-123">-ShareName</span></span>
<span data-ttu-id="0c988-124">Nome della condivisione contenente il contenitore specificato per la migrazione.</span><span class="sxs-lookup"><span data-stu-id="0c988-124">Name of the share containing the container specified for migration.</span></span>

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

### <span data-ttu-id="0c988-125">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0c988-125">-StorageAccountName</span></span>
<span data-ttu-id="0c988-126">Nome dell'account di archiviazione in cui viene individuato il contenitore.</span><span class="sxs-lookup"><span data-stu-id="0c988-126">The name of storage account where the container locates.</span></span>

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

### <span data-ttu-id="0c988-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0c988-127">-Confirm</span></span>
<span data-ttu-id="0c988-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c988-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c988-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c988-129">-WhatIf</span></span>
<span data-ttu-id="0c988-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0c988-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c988-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0c988-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c988-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c988-132">CommonParameters</span></span>
<span data-ttu-id="0c988-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c988-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c988-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c988-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c988-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0c988-135">INPUTS</span></span>

## <span data-ttu-id="0c988-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0c988-136">OUTPUTS</span></span>

## <span data-ttu-id="0c988-137">Note</span><span class="sxs-lookup"><span data-stu-id="0c988-137">NOTES</span></span>

## <span data-ttu-id="0c988-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0c988-138">RELATED LINKS</span></span>

