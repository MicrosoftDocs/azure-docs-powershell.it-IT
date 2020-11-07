---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a2b639a09789960393ac26d035a80157069dbaaa
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "93859062"
---
# <span data-ttu-id="ae2ae-101">Get-AzsDisk</span><span class="sxs-lookup"><span data-stu-id="ae2ae-101">Get-AzsDisk</span></span>

## <span data-ttu-id="ae2ae-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ae2ae-102">SYNOPSIS</span></span>
<span data-ttu-id="ae2ae-103">Restituisce l'elenco dei dischi gestiti di cui è possibile eseguire la migrazione nella condivisione specificata.</span><span class="sxs-lookup"><span data-stu-id="ae2ae-103">Returns the list of managed disks which can be migrated in the specified share.</span></span>

## <span data-ttu-id="ae2ae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ae2ae-104">SYNTAX</span></span>

### <span data-ttu-id="ae2ae-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ae2ae-105">List (Default)</span></span>
```
Get-AzsDisk [-Location <String>] [-Start <Int32>] [-SharePath <String>] [-Count <Int32>]
 [-UserSubscriptionId <String>] [-Status <String>] [<CommonParameters>]
```

### <span data-ttu-id="ae2ae-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae2ae-106">ResourceId</span></span>
```
Get-AzsDisk -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="ae2ae-107">Ottieni</span><span class="sxs-lookup"><span data-stu-id="ae2ae-107">Get</span></span>
```
Get-AzsDisk [-Location <String>] -Name <String> [<CommonParameters>]
```

## <span data-ttu-id="ae2ae-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ae2ae-108">DESCRIPTION</span></span>
<span data-ttu-id="ae2ae-109">Restituisce un elenco di dischi.</span><span class="sxs-lookup"><span data-stu-id="ae2ae-109">Returns a list of disks.</span></span>

## <span data-ttu-id="ae2ae-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ae2ae-110">EXAMPLES</span></span>

### <span data-ttu-id="ae2ae-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ae2ae-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
$disks = Get-AzsDisk -location local
```

<span data-ttu-id="ae2ae-112">Restituisce un elenco di dischi gestiti nella posizione locale.</span><span class="sxs-lookup"><span data-stu-id="ae2ae-112">Returns a list of managed disks at the location local.</span></span>
<span data-ttu-id="ae2ae-113">Per impostazione predefinita, saranno i primi dischi di 100</span><span class="sxs-lookup"><span data-stu-id="ae2ae-113">By default, it will the first 100 disks</span></span>

### <span data-ttu-id="ae2ae-114">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="ae2ae-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
$disk = Get-AzsDisk -location local -name $DiskId
```

<span data-ttu-id="ae2ae-115">Ottenere uno specifico disco gestito.</span><span class="sxs-lookup"><span data-stu-id="ae2ae-115">Get a specific managed disk.</span></span>

## <span data-ttu-id="ae2ae-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ae2ae-116">PARAMETERS</span></span>

### <span data-ttu-id="ae2ae-117">-Conteggio</span><span class="sxs-lookup"><span data-stu-id="ae2ae-117">-Count</span></span>
<span data-ttu-id="ae2ae-118">Numero massimo di dischi da restituire.</span><span class="sxs-lookup"><span data-stu-id="ae2ae-118">The maximum number of disks to return.</span></span>

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

### <span data-ttu-id="ae2ae-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="ae2ae-119">-Location</span></span>
<span data-ttu-id="ae2ae-120">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="ae2ae-120">Location of the resource.</span></span>

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

### <span data-ttu-id="ae2ae-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="ae2ae-121">-Name</span></span>
<span data-ttu-id="ae2ae-122">GUID del disco come identità.</span><span class="sxs-lookup"><span data-stu-id="ae2ae-122">The disk guid as identity.</span></span>

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

### <span data-ttu-id="ae2ae-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae2ae-123">-ResourceId</span></span>
<span data-ttu-id="ae2ae-124">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="ae2ae-124">The resource id.</span></span>

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

### <span data-ttu-id="ae2ae-125">-SharePath</span><span class="sxs-lookup"><span data-stu-id="ae2ae-125">-SharePath</span></span>
<span data-ttu-id="ae2ae-126">La condivisione di origine a cui appartiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="ae2ae-126">The source share which the resource belongs to.</span></span>

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

### <span data-ttu-id="ae2ae-127">-Inizio</span><span class="sxs-lookup"><span data-stu-id="ae2ae-127">-Start</span></span>
<span data-ttu-id="ae2ae-128">Indice Start dei dischi in query.</span><span class="sxs-lookup"><span data-stu-id="ae2ae-128">The start index of disks in query.</span></span>

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

### <span data-ttu-id="ae2ae-129">-Stato</span><span class="sxs-lookup"><span data-stu-id="ae2ae-129">-Status</span></span>
<span data-ttu-id="ae2ae-130">I parametri dello stato del disco.</span><span class="sxs-lookup"><span data-stu-id="ae2ae-130">The parameters of disk state.</span></span>

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

### <span data-ttu-id="ae2ae-131">-UserSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ae2ae-131">-UserSubscriptionId</span></span>
<span data-ttu-id="ae2ae-132">ID abbonamento tenant a cui appartiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="ae2ae-132">Tenant Subscription Id which the resource belongs to.</span></span>

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

### <span data-ttu-id="ae2ae-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae2ae-133">CommonParameters</span></span>
<span data-ttu-id="ae2ae-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae2ae-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae2ae-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae2ae-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae2ae-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ae2ae-136">INPUTS</span></span>

## <span data-ttu-id="ae2ae-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ae2ae-137">OUTPUTS</span></span>

### <span data-ttu-id="ae2ae-138">Microsoft. AzureStack. Management. Compute. admin. Models. disk</span><span class="sxs-lookup"><span data-stu-id="ae2ae-138">Microsoft.AzureStack.Management.Compute.Admin.Models.Disk</span></span>

## <span data-ttu-id="ae2ae-139">Note</span><span class="sxs-lookup"><span data-stu-id="ae2ae-139">NOTES</span></span>

## <span data-ttu-id="ae2ae-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ae2ae-140">RELATED LINKS</span></span>

