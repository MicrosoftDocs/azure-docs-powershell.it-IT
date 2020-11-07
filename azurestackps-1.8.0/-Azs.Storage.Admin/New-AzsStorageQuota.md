---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 143f368b73aac490242e42f21ed76ee76ab012dc
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "93859102"
---
# <span data-ttu-id="bb733-101">New-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="bb733-101">New-AzsStorageQuota</span></span>

## <span data-ttu-id="bb733-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bb733-102">SYNOPSIS</span></span>
<span data-ttu-id="bb733-103">Creare una nuova quota di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="bb733-103">Create a new storage quota.</span></span>

## <span data-ttu-id="bb733-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bb733-104">SYNTAX</span></span>

```
New-AzsStorageQuota [-Name] <String> [[-CapacityInGb] <Int32>] [[-NumberOfStorageAccounts] <Int32>]
 [[-Location] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb733-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb733-105">DESCRIPTION</span></span>
<span data-ttu-id="bb733-106">Creare una nuova quota di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="bb733-106">Create a new storage quota.</span></span>

## <span data-ttu-id="bb733-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bb733-107">EXAMPLES</span></span>

### <span data-ttu-id="bb733-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="bb733-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsStorageQuota -CapacityInGb 1000 -NumberOfStorageAccounts 100 -Name 'TestCreateStorageQuota'
```

<span data-ttu-id="bb733-109">Creare una nuova quota di archiviazione con valori specificati.</span><span class="sxs-lookup"><span data-stu-id="bb733-109">Create a new storage quota with specified values.</span></span>

## <span data-ttu-id="bb733-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bb733-110">PARAMETERS</span></span>

### <span data-ttu-id="bb733-111">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="bb733-111">-CapacityInGb</span></span>
<span data-ttu-id="bb733-112">Capacità Maxium (GB).</span><span class="sxs-lookup"><span data-stu-id="bb733-112">Maxium capacity (GB).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: 500
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb733-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="bb733-113">-Location</span></span>
<span data-ttu-id="bb733-114">Posizione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="bb733-114">Resource location.</span></span>

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

### <span data-ttu-id="bb733-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="bb733-115">-Name</span></span>
<span data-ttu-id="bb733-116">Nome della quota di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="bb733-116">The name of the storage quota.</span></span>

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

### <span data-ttu-id="bb733-117">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="bb733-117">-NumberOfStorageAccounts</span></span>
<span data-ttu-id="bb733-118">Numero totale di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="bb733-118">Total number of storage accounts.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: 20
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb733-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bb733-119">-Confirm</span></span>
<span data-ttu-id="bb733-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb733-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb733-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb733-121">-WhatIf</span></span>
<span data-ttu-id="bb733-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bb733-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb733-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bb733-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb733-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb733-124">CommonParameters</span></span>
<span data-ttu-id="bb733-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb733-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb733-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb733-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb733-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bb733-127">INPUTS</span></span>

## <span data-ttu-id="bb733-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bb733-128">OUTPUTS</span></span>

### <span data-ttu-id="bb733-129">Microsoft. AzureStack. Management. storage. admin. Models. StorageQuota consente</span><span class="sxs-lookup"><span data-stu-id="bb733-129">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="bb733-130">Note</span><span class="sxs-lookup"><span data-stu-id="bb733-130">NOTES</span></span>

## <span data-ttu-id="bb733-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bb733-131">RELATED LINKS</span></span>

