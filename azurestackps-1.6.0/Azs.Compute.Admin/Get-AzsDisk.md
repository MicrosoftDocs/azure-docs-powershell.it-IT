---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e4c464d2d0e822b745acc2a7c6daecf329449105
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490765"
---
# <span data-ttu-id="30271-101">Get-AzsDisk</span><span class="sxs-lookup"><span data-stu-id="30271-101">Get-AzsDisk</span></span>

## <span data-ttu-id="30271-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="30271-102">SYNOPSIS</span></span>
<span data-ttu-id="30271-103">Restituisce l'elenco dei dischi gestiti di cui è possibile eseguire la migrazione nella condivisione specificata.</span><span class="sxs-lookup"><span data-stu-id="30271-103">Returns the list of managed disks which can be migrated in the specified share.</span></span>

## <span data-ttu-id="30271-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="30271-104">SYNTAX</span></span>

### <span data-ttu-id="30271-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="30271-105">List (Default)</span></span>
```
Get-AzsDisk [-Location <String>] [-Start <Int32>] [-SharePath <String>] [-Count <Int32>]
 [-UserSubscriptionId <String>] [-Status <String>] [<CommonParameters>]
```

### <span data-ttu-id="30271-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="30271-106">ResourceId</span></span>
```
Get-AzsDisk -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="30271-107">Ottieni</span><span class="sxs-lookup"><span data-stu-id="30271-107">Get</span></span>
```
Get-AzsDisk [-Location <String>] -Name <String> [<CommonParameters>]
```

## <span data-ttu-id="30271-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="30271-108">DESCRIPTION</span></span>
<span data-ttu-id="30271-109">Restituisce un elenco di dischi.</span><span class="sxs-lookup"><span data-stu-id="30271-109">Returns a list of disks.</span></span>

## <span data-ttu-id="30271-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="30271-110">EXAMPLES</span></span>

### <span data-ttu-id="30271-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="30271-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
$disks = Get-AzsDisk -location local
```

<span data-ttu-id="30271-112">Restituisce un elenco di dischi gestiti nella posizione locale.</span><span class="sxs-lookup"><span data-stu-id="30271-112">Returns a list of managed disks at the location local.</span></span>
<span data-ttu-id="30271-113">Per impostazione predefinita, saranno i primi dischi di 100</span><span class="sxs-lookup"><span data-stu-id="30271-113">By default, it will the first 100 disks</span></span>

### <span data-ttu-id="30271-114">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="30271-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
$disk = Get-AzsDisk -location local -name $DiskId
```

<span data-ttu-id="30271-115">Ottenere uno specifico disco gestito.</span><span class="sxs-lookup"><span data-stu-id="30271-115">Get a specific managed disk.</span></span>

## <span data-ttu-id="30271-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="30271-116">PARAMETERS</span></span>

### <span data-ttu-id="30271-117">-Conteggio</span><span class="sxs-lookup"><span data-stu-id="30271-117">-Count</span></span>
<span data-ttu-id="30271-118">Numero massimo di dischi da restituire.</span><span class="sxs-lookup"><span data-stu-id="30271-118">The maximum number of disks to return.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30271-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="30271-119">-Location</span></span>
<span data-ttu-id="30271-120">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="30271-120">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30271-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="30271-121">-Name</span></span>
<span data-ttu-id="30271-122">GUID del disco come identità.</span><span class="sxs-lookup"><span data-stu-id="30271-122">The disk guid as identity.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: DiskId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30271-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="30271-123">-ResourceId</span></span>
<span data-ttu-id="30271-124">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="30271-124">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30271-125">-SharePath</span><span class="sxs-lookup"><span data-stu-id="30271-125">-SharePath</span></span>
<span data-ttu-id="30271-126">La condivisione di origine a cui appartiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="30271-126">The source share which the resource belongs to.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30271-127">-Inizio</span><span class="sxs-lookup"><span data-stu-id="30271-127">-Start</span></span>
<span data-ttu-id="30271-128">Indice Start dei dischi in query.</span><span class="sxs-lookup"><span data-stu-id="30271-128">The start index of disks in query.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30271-129">-Stato</span><span class="sxs-lookup"><span data-stu-id="30271-129">-Status</span></span>
<span data-ttu-id="30271-130">I parametri dello stato del disco.</span><span class="sxs-lookup"><span data-stu-id="30271-130">The parameters of disk state.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30271-131">-UserSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="30271-131">-UserSubscriptionId</span></span>
<span data-ttu-id="30271-132">ID abbonamento tenant a cui appartiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="30271-132">Tenant Subscription Id which the resource belongs to.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30271-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30271-133">CommonParameters</span></span>
<span data-ttu-id="30271-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30271-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30271-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30271-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30271-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="30271-136">INPUTS</span></span>

## <span data-ttu-id="30271-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="30271-137">OUTPUTS</span></span>

### <span data-ttu-id="30271-138">Microsoft. AzureStack. Management. Compute. admin. Models. disk</span><span class="sxs-lookup"><span data-stu-id="30271-138">Microsoft.AzureStack.Management.Compute.Admin.Models.Disk</span></span>

## <span data-ttu-id="30271-139">Note</span><span class="sxs-lookup"><span data-stu-id="30271-139">NOTES</span></span>

## <span data-ttu-id="30271-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="30271-140">RELATED LINKS</span></span>
