---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2eec56d9fc157da994521a5b258cd28132344c52
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "93859078"
---
# <span data-ttu-id="45218-101">Set-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="45218-101">Set-AzsStorageQuota</span></span>

## <span data-ttu-id="45218-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="45218-102">SYNOPSIS</span></span>
<span data-ttu-id="45218-103">Creare o aggiornare una quota di archiviazione esistente.</span><span class="sxs-lookup"><span data-stu-id="45218-103">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="45218-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="45218-104">SYNTAX</span></span>

### <span data-ttu-id="45218-105">Update (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="45218-105">Update (Default)</span></span>
```
Set-AzsStorageQuota -Name <String> [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>]
 [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45218-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="45218-106">ResourceId</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -ResourceId <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45218-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="45218-107">InputObject</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -InputObject <StorageQuota>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45218-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="45218-108">DESCRIPTION</span></span>
<span data-ttu-id="45218-109">Creare o aggiornare una quota di archiviazione esistente.</span><span class="sxs-lookup"><span data-stu-id="45218-109">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="45218-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="45218-110">EXAMPLES</span></span>

### <span data-ttu-id="45218-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="45218-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsStorageQuota -Name 'TestUpdateStorageQuota' -CapacityInGb 123 -NumberOfStorageAccounts 10
```

<span data-ttu-id="45218-112">Aggiornare una quota di archiviazione esistente.</span><span class="sxs-lookup"><span data-stu-id="45218-112">Update an existing storage quota.</span></span>

## <span data-ttu-id="45218-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="45218-113">PARAMETERS</span></span>

### <span data-ttu-id="45218-114">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="45218-114">-CapacityInGb</span></span>
<span data-ttu-id="45218-115">Capacità Maxium (GB).</span><span class="sxs-lookup"><span data-stu-id="45218-115">Maxium capacity (GB).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45218-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45218-116">-InputObject</span></span>
<span data-ttu-id="45218-117">Quota di archiviazione modificata di Posbbily restituita da Get-AzsStorageQuota.</span><span class="sxs-lookup"><span data-stu-id="45218-117">Posbbily modified storage quota returned by Get-AzsStorageQuota.</span></span>

```yaml
Type: StorageQuota
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45218-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="45218-118">-Location</span></span>
<span data-ttu-id="45218-119">Posizione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="45218-119">Resource location.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45218-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="45218-120">-Name</span></span>
<span data-ttu-id="45218-121">Nome della quota di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="45218-121">The name of the storage quota.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45218-122">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="45218-122">-NumberOfStorageAccounts</span></span>
<span data-ttu-id="45218-123">Numero totale di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="45218-123">Total number of storage accounts.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45218-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45218-124">-ResourceId</span></span>
<span data-ttu-id="45218-125">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="45218-125">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45218-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="45218-126">-Confirm</span></span>
<span data-ttu-id="45218-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45218-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45218-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45218-128">-WhatIf</span></span>
<span data-ttu-id="45218-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="45218-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45218-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="45218-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45218-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45218-131">CommonParameters</span></span>
<span data-ttu-id="45218-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45218-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45218-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45218-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45218-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="45218-134">INPUTS</span></span>

## <span data-ttu-id="45218-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="45218-135">OUTPUTS</span></span>

### <span data-ttu-id="45218-136">Microsoft. AzureStack. Management. storage. admin. Models. StorageQuota consente</span><span class="sxs-lookup"><span data-stu-id="45218-136">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="45218-137">Note</span><span class="sxs-lookup"><span data-stu-id="45218-137">NOTES</span></span>

## <span data-ttu-id="45218-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="45218-138">RELATED LINKS</span></span>

