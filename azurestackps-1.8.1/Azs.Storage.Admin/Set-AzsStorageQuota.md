---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 641017c75243a253a6b9eb0054df7737a674f671
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859958"
---
# <span data-ttu-id="43bc8-101">Set-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="43bc8-101">Set-AzsStorageQuota</span></span>

## <span data-ttu-id="43bc8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="43bc8-102">SYNOPSIS</span></span>
<span data-ttu-id="43bc8-103">Creare o aggiornare una quota di archiviazione esistente.</span><span class="sxs-lookup"><span data-stu-id="43bc8-103">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="43bc8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="43bc8-104">SYNTAX</span></span>

### <span data-ttu-id="43bc8-105">Update (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="43bc8-105">Update (Default)</span></span>
```
Set-AzsStorageQuota -Name <String> [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>]
 [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43bc8-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="43bc8-106">ResourceId</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -ResourceId <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43bc8-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="43bc8-107">InputObject</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -InputObject <StorageQuota>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43bc8-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43bc8-108">DESCRIPTION</span></span>
<span data-ttu-id="43bc8-109">Creare o aggiornare una quota di archiviazione esistente.</span><span class="sxs-lookup"><span data-stu-id="43bc8-109">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="43bc8-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="43bc8-110">EXAMPLES</span></span>

### <span data-ttu-id="43bc8-111">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="43bc8-111">EXAMPLE 1</span></span>
```
Set-AzsStorageQuota -Name 'TestUpdateStorageQuota' -CapacityInGb 123 -NumberOfStorageAccounts 10
```

<span data-ttu-id="43bc8-112">Aggiornare una quota di archiviazione esistente.</span><span class="sxs-lookup"><span data-stu-id="43bc8-112">Update an existing storage quota.</span></span>

## <span data-ttu-id="43bc8-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="43bc8-113">PARAMETERS</span></span>

### <span data-ttu-id="43bc8-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="43bc8-114">-Name</span></span>
<span data-ttu-id="43bc8-115">Nome della quota di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="43bc8-115">The name of the storage quota.</span></span>

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

### <span data-ttu-id="43bc8-116">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="43bc8-116">-CapacityInGb</span></span>
<span data-ttu-id="43bc8-117">Capacità Maxium (GB).</span><span class="sxs-lookup"><span data-stu-id="43bc8-117">Maxium capacity (GB).</span></span>

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

### <span data-ttu-id="43bc8-118">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="43bc8-118">-NumberOfStorageAccounts</span></span>
<span data-ttu-id="43bc8-119">Numero totale di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="43bc8-119">Total number of storage accounts.</span></span>

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

### <span data-ttu-id="43bc8-120">-Posizione</span><span class="sxs-lookup"><span data-stu-id="43bc8-120">-Location</span></span>
<span data-ttu-id="43bc8-121">Posizione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="43bc8-121">Resource location.</span></span>

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

### <span data-ttu-id="43bc8-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43bc8-122">-ResourceId</span></span>
<span data-ttu-id="43bc8-123">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="43bc8-123">The resource id.</span></span>

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

### <span data-ttu-id="43bc8-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43bc8-124">-InputObject</span></span>
<span data-ttu-id="43bc8-125">Quota di archiviazione modificata di Posbbily restituita da Get-AzsStorageQuota.</span><span class="sxs-lookup"><span data-stu-id="43bc8-125">Posbbily modified storage quota returned by Get-AzsStorageQuota.</span></span>

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

### <span data-ttu-id="43bc8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43bc8-126">-WhatIf</span></span>
<span data-ttu-id="43bc8-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="43bc8-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43bc8-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="43bc8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43bc8-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="43bc8-129">-Confirm</span></span>
<span data-ttu-id="43bc8-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43bc8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43bc8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43bc8-131">CommonParameters</span></span>
<span data-ttu-id="43bc8-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43bc8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43bc8-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43bc8-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43bc8-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="43bc8-134">INPUTS</span></span>

## <span data-ttu-id="43bc8-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="43bc8-135">OUTPUTS</span></span>

### <span data-ttu-id="43bc8-136">Microsoft. AzureStack. Management. storage. admin. Models. StorageQuota consente</span><span class="sxs-lookup"><span data-stu-id="43bc8-136">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="43bc8-137">Note</span><span class="sxs-lookup"><span data-stu-id="43bc8-137">NOTES</span></span>

## <span data-ttu-id="43bc8-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="43bc8-138">RELATED LINKS</span></span>
