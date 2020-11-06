---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 143f368b73aac490242e42f21ed76ee76ab012dc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491237"
---
# <span data-ttu-id="f8bcd-101">New-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="f8bcd-101">New-AzsStorageQuota</span></span>

## <span data-ttu-id="f8bcd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f8bcd-102">SYNOPSIS</span></span>
<span data-ttu-id="f8bcd-103">Creare una nuova quota di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="f8bcd-103">Create a new storage quota.</span></span>

## <span data-ttu-id="f8bcd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f8bcd-104">SYNTAX</span></span>

```
New-AzsStorageQuota [-Name] <String> [[-CapacityInGb] <Int32>] [[-NumberOfStorageAccounts] <Int32>]
 [[-Location] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8bcd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f8bcd-105">DESCRIPTION</span></span>
<span data-ttu-id="f8bcd-106">Creare una nuova quota di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="f8bcd-106">Create a new storage quota.</span></span>

## <span data-ttu-id="f8bcd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f8bcd-107">EXAMPLES</span></span>

### <span data-ttu-id="f8bcd-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f8bcd-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsStorageQuota -CapacityInGb 1000 -NumberOfStorageAccounts 100 -Name 'TestCreateStorageQuota'
```

<span data-ttu-id="f8bcd-109">Creare una nuova quota di archiviazione con valori specificati.</span><span class="sxs-lookup"><span data-stu-id="f8bcd-109">Create a new storage quota with specified values.</span></span>

## <span data-ttu-id="f8bcd-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f8bcd-110">PARAMETERS</span></span>

### <span data-ttu-id="f8bcd-111">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="f8bcd-111">-CapacityInGb</span></span>
<span data-ttu-id="f8bcd-112">Capacità Maxium (GB).</span><span class="sxs-lookup"><span data-stu-id="f8bcd-112">Maxium capacity (GB).</span></span>

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

### <span data-ttu-id="f8bcd-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="f8bcd-113">-Location</span></span>
<span data-ttu-id="f8bcd-114">Posizione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="f8bcd-114">Resource location.</span></span>

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

### <span data-ttu-id="f8bcd-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="f8bcd-115">-Name</span></span>
<span data-ttu-id="f8bcd-116">Nome della quota di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="f8bcd-116">The name of the storage quota.</span></span>

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

### <span data-ttu-id="f8bcd-117">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="f8bcd-117">-NumberOfStorageAccounts</span></span>
<span data-ttu-id="f8bcd-118">Numero totale di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="f8bcd-118">Total number of storage accounts.</span></span>

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

### <span data-ttu-id="f8bcd-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f8bcd-119">-Confirm</span></span>
<span data-ttu-id="f8bcd-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8bcd-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8bcd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8bcd-121">-WhatIf</span></span>
<span data-ttu-id="f8bcd-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f8bcd-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8bcd-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f8bcd-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8bcd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8bcd-124">CommonParameters</span></span>
<span data-ttu-id="f8bcd-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8bcd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8bcd-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8bcd-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8bcd-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f8bcd-127">INPUTS</span></span>

## <span data-ttu-id="f8bcd-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f8bcd-128">OUTPUTS</span></span>

### <span data-ttu-id="f8bcd-129">Microsoft. AzureStack. Management. storage. admin. Models. StorageQuota consente</span><span class="sxs-lookup"><span data-stu-id="f8bcd-129">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="f8bcd-130">Note</span><span class="sxs-lookup"><span data-stu-id="f8bcd-130">NOTES</span></span>

## <span data-ttu-id="f8bcd-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f8bcd-131">RELATED LINKS</span></span>

