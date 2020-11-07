---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4cc08220a92dce5a49544cf958db79d7243b9ebb
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859989"
---
# <span data-ttu-id="cd282-101">New-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="cd282-101">New-AzsStorageQuota</span></span>

## <span data-ttu-id="cd282-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cd282-102">SYNOPSIS</span></span>
<span data-ttu-id="cd282-103">Creare una nuova quota di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cd282-103">Create a new storage quota.</span></span>

## <span data-ttu-id="cd282-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cd282-104">SYNTAX</span></span>

```
New-AzsStorageQuota [-Name] <String> [[-CapacityInGb] <Int32>] [[-NumberOfStorageAccounts] <Int32>]
 [[-Location] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd282-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd282-105">DESCRIPTION</span></span>
<span data-ttu-id="cd282-106">Creare una nuova quota di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cd282-106">Create a new storage quota.</span></span>

## <span data-ttu-id="cd282-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cd282-107">EXAMPLES</span></span>

### <span data-ttu-id="cd282-108">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="cd282-108">EXAMPLE 1</span></span>
```
New-AzsStorageQuota -CapacityInGb 1000 -NumberOfStorageAccounts 100 -Name 'TestCreateStorageQuota'
```

<span data-ttu-id="cd282-109">Creare una nuova quota di archiviazione con valori specificati.</span><span class="sxs-lookup"><span data-stu-id="cd282-109">Create a new storage quota with specified values.</span></span>

## <span data-ttu-id="cd282-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cd282-110">PARAMETERS</span></span>

### <span data-ttu-id="cd282-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="cd282-111">-Name</span></span>
<span data-ttu-id="cd282-112">Nome della quota di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cd282-112">The name of the storage quota.</span></span>

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

### <span data-ttu-id="cd282-113">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="cd282-113">-CapacityInGb</span></span>
<span data-ttu-id="cd282-114">Capacità Maxium (GB).</span><span class="sxs-lookup"><span data-stu-id="cd282-114">Maxium capacity (GB).</span></span>

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

### <span data-ttu-id="cd282-115">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="cd282-115">-NumberOfStorageAccounts</span></span>
<span data-ttu-id="cd282-116">Numero totale di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cd282-116">Total number of storage accounts.</span></span>

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

### <span data-ttu-id="cd282-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="cd282-117">-Location</span></span>
<span data-ttu-id="cd282-118">Posizione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="cd282-118">Resource location.</span></span>

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

### <span data-ttu-id="cd282-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd282-119">-WhatIf</span></span>
<span data-ttu-id="cd282-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd282-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd282-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd282-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd282-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cd282-122">-Confirm</span></span>
<span data-ttu-id="cd282-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd282-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd282-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd282-124">CommonParameters</span></span>
<span data-ttu-id="cd282-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd282-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd282-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd282-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd282-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cd282-127">INPUTS</span></span>

## <span data-ttu-id="cd282-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cd282-128">OUTPUTS</span></span>

### <span data-ttu-id="cd282-129">Microsoft. AzureStack. Management. storage. admin. Models. StorageQuota consente</span><span class="sxs-lookup"><span data-stu-id="cd282-129">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="cd282-130">Note</span><span class="sxs-lookup"><span data-stu-id="cd282-130">NOTES</span></span>

## <span data-ttu-id="cd282-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cd282-131">RELATED LINKS</span></span>
