---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2cf36bf232ae48891b28562313fa2063e14a2be8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491158"
---
# <span data-ttu-id="98c96-101">Get-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="98c96-101">Get-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="98c96-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="98c96-102">SYNOPSIS</span></span>
<span data-ttu-id="98c96-103">Restituisce l'elenco dei processi di migrazione del disco gestito.</span><span class="sxs-lookup"><span data-stu-id="98c96-103">Returns the list of managed disk migration jobs.</span></span>

## <span data-ttu-id="98c96-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="98c96-104">SYNTAX</span></span>

### <span data-ttu-id="98c96-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="98c96-105">List (Default)</span></span>
```
Get-AzsDiskMigrationJob [-Status <String>] [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="98c96-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="98c96-106">ResourceId</span></span>
```
Get-AzsDiskMigrationJob -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="98c96-107">Ottieni</span><span class="sxs-lookup"><span data-stu-id="98c96-107">Get</span></span>
```
Get-AzsDiskMigrationJob [-Location <String>] -Name <String> [<CommonParameters>]
```

## <span data-ttu-id="98c96-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="98c96-108">DESCRIPTION</span></span>
<span data-ttu-id="98c96-109">Restituisce un elenco dei processi di migrazione del disco.</span><span class="sxs-lookup"><span data-stu-id="98c96-109">Returns a list of disk migration jobs.</span></span>

## <span data-ttu-id="98c96-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="98c96-110">EXAMPLES</span></span>

### <span data-ttu-id="98c96-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="98c96-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
$migration = Get-AzsDiskMigrationJob -location local -Name "mymigrationName"
```

<span data-ttu-id="98c96-112">Ottenere un processo di migrazione del disco gestito specifico.</span><span class="sxs-lookup"><span data-stu-id="98c96-112">Get a specific managed disk migration job.</span></span>

### <span data-ttu-id="98c96-113">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="98c96-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
$migration = Get-AzsDiskMigrationJob -location local
```

<span data-ttu-id="98c96-114">Restituisce un elenco dei processi di migrazione del disco gestito nella posizione locale.</span><span class="sxs-lookup"><span data-stu-id="98c96-114">Returns a list of managed disk migration jobs at the location local.</span></span>

## <span data-ttu-id="98c96-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="98c96-115">PARAMETERS</span></span>

### <span data-ttu-id="98c96-116">-Posizione</span><span class="sxs-lookup"><span data-stu-id="98c96-116">-Location</span></span>
<span data-ttu-id="98c96-117">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="98c96-117">Location of the resource.</span></span>

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

### <span data-ttu-id="98c96-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="98c96-118">-Name</span></span>
<span data-ttu-id="98c96-119">Nome GUID processo di migrazione.</span><span class="sxs-lookup"><span data-stu-id="98c96-119">The migration job guid name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: MigrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98c96-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98c96-120">-ResourceId</span></span>
<span data-ttu-id="98c96-121">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="98c96-121">The resource id.</span></span>

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

### <span data-ttu-id="98c96-122">-Stato</span><span class="sxs-lookup"><span data-stu-id="98c96-122">-Status</span></span>
<span data-ttu-id="98c96-123">Parametri dello stato del processo di migrazione del disco.</span><span class="sxs-lookup"><span data-stu-id="98c96-123">The parameters of disk migration job status.</span></span>

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

### <span data-ttu-id="98c96-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98c96-124">CommonParameters</span></span>
<span data-ttu-id="98c96-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98c96-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98c96-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98c96-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98c96-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="98c96-127">INPUTS</span></span>

## <span data-ttu-id="98c96-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="98c96-128">OUTPUTS</span></span>

### <span data-ttu-id="98c96-129">Microsoft. AzureStack. Management. Compute. admin. Models. DiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="98c96-129">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="98c96-130">Note</span><span class="sxs-lookup"><span data-stu-id="98c96-130">NOTES</span></span>

## <span data-ttu-id="98c96-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="98c96-131">RELATED LINKS</span></span>

