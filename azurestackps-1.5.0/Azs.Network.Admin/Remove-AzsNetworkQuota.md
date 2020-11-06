---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3f7f40982a4c7d24e02e7e365163cc6250ff8791
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490998"
---
# <span data-ttu-id="7974d-101">Remove-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="7974d-101">Remove-AzsNetworkQuota</span></span>

## <span data-ttu-id="7974d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7974d-102">SYNOPSIS</span></span>
<span data-ttu-id="7974d-103">Eliminare una quota per nome.</span><span class="sxs-lookup"><span data-stu-id="7974d-103">Delete a quota by name.</span></span>

## <span data-ttu-id="7974d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7974d-104">SYNTAX</span></span>

### <span data-ttu-id="7974d-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7974d-105">Delete (Default)</span></span>
```
Remove-AzsNetworkQuota -Name <String> [-Location <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7974d-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7974d-106">ResourceId</span></span>
```
Remove-AzsNetworkQuota -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7974d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7974d-107">DESCRIPTION</span></span>
<span data-ttu-id="7974d-108">Eliminare una quota per nome.</span><span class="sxs-lookup"><span data-stu-id="7974d-108">Delete a quota by name.</span></span>

## <span data-ttu-id="7974d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7974d-109">EXAMPLES</span></span>

### <span data-ttu-id="7974d-110">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7974d-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="7974d-111">Rimuovere una quota di rete per nome.</span><span class="sxs-lookup"><span data-stu-id="7974d-111">Remove a network quota by name.</span></span>

### <span data-ttu-id="7974d-112">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="7974d-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1 | Remove-AzsNetworkQuota
```

<span data-ttu-id="7974d-113">Rimuovere una quota di rete usando una pipe.</span><span class="sxs-lookup"><span data-stu-id="7974d-113">Remove a network quota using a pipe.</span></span>

### <span data-ttu-id="7974d-114">--------------------------ESEMPIO 3--------------------------</span><span class="sxs-lookup"><span data-stu-id="7974d-114">-------------------------- EXAMPLE 3 --------------------------</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="7974d-115">Rimuovere una quota di rete.</span><span class="sxs-lookup"><span data-stu-id="7974d-115">Remove a network quota.</span></span>

## <span data-ttu-id="7974d-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7974d-116">PARAMETERS</span></span>

### <span data-ttu-id="7974d-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7974d-117">-AsJob</span></span>
<span data-ttu-id="7974d-118">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="7974d-118">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="7974d-119">-Force</span><span class="sxs-lookup"><span data-stu-id="7974d-119">-Force</span></span>
<span data-ttu-id="7974d-120">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="7974d-120">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="7974d-121">-Posizione</span><span class="sxs-lookup"><span data-stu-id="7974d-121">-Location</span></span>
<span data-ttu-id="7974d-122">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="7974d-122">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7974d-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="7974d-123">-Name</span></span>
<span data-ttu-id="7974d-124">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="7974d-124">Name of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7974d-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7974d-125">-ResourceId</span></span>
<span data-ttu-id="7974d-126">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="7974d-126">The resource id.</span></span>

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

### <span data-ttu-id="7974d-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7974d-127">-Confirm</span></span>
<span data-ttu-id="7974d-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7974d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7974d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7974d-129">-WhatIf</span></span>
<span data-ttu-id="7974d-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7974d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7974d-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7974d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7974d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7974d-132">CommonParameters</span></span>
<span data-ttu-id="7974d-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7974d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7974d-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7974d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7974d-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7974d-135">INPUTS</span></span>

## <span data-ttu-id="7974d-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7974d-136">OUTPUTS</span></span>

## <span data-ttu-id="7974d-137">Note</span><span class="sxs-lookup"><span data-stu-id="7974d-137">NOTES</span></span>

## <span data-ttu-id="7974d-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7974d-138">RELATED LINKS</span></span>

