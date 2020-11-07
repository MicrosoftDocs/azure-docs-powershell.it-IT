---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06f2d231754fc422115cf800ef66189378e0cd4d
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859725"
---
# <span data-ttu-id="82843-101">Get-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="82843-101">Get-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="82843-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="82843-102">SYNOPSIS</span></span>
<span data-ttu-id="82843-103">Restituisce l'elenco dei processi di migrazione del disco gestito.</span><span class="sxs-lookup"><span data-stu-id="82843-103">Returns the list of managed disk migration jobs.</span></span>

## <span data-ttu-id="82843-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="82843-104">SYNTAX</span></span>

### <span data-ttu-id="82843-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="82843-105">List (Default)</span></span>
```
Get-AzsDiskMigrationJob [-Status <String>] [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="82843-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="82843-106">ResourceId</span></span>
```
Get-AzsDiskMigrationJob -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="82843-107">Ottieni</span><span class="sxs-lookup"><span data-stu-id="82843-107">Get</span></span>
```
Get-AzsDiskMigrationJob [-Location <String>] -Name <String> [<CommonParameters>]
```

## <span data-ttu-id="82843-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82843-108">DESCRIPTION</span></span>
<span data-ttu-id="82843-109">Restituisce un elenco dei processi di migrazione del disco.</span><span class="sxs-lookup"><span data-stu-id="82843-109">Returns a list of disk migration jobs.</span></span>

## <span data-ttu-id="82843-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="82843-110">EXAMPLES</span></span>

### <span data-ttu-id="82843-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="82843-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
$migration = Get-AzsDiskMigrationJob -location local -Name "mymigrationName"
```

<span data-ttu-id="82843-112">Ottenere un processo di migrazione del disco gestito specifico.</span><span class="sxs-lookup"><span data-stu-id="82843-112">Get a specific managed disk migration job.</span></span>

### <span data-ttu-id="82843-113">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="82843-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
$migration = Get-AzsDiskMigrationJob -location local
```

<span data-ttu-id="82843-114">Restituisce un elenco dei processi di migrazione del disco gestito nella posizione locale.</span><span class="sxs-lookup"><span data-stu-id="82843-114">Returns a list of managed disk migration jobs at the location local.</span></span>

## <span data-ttu-id="82843-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="82843-115">PARAMETERS</span></span>

### <span data-ttu-id="82843-116">-Posizione</span><span class="sxs-lookup"><span data-stu-id="82843-116">-Location</span></span>
<span data-ttu-id="82843-117">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="82843-117">Location of the resource.</span></span>

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

### <span data-ttu-id="82843-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="82843-118">-Name</span></span>
<span data-ttu-id="82843-119">Nome GUID processo di migrazione.</span><span class="sxs-lookup"><span data-stu-id="82843-119">The migration job guid name.</span></span>

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

### <span data-ttu-id="82843-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82843-120">-ResourceId</span></span>
<span data-ttu-id="82843-121">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="82843-121">The resource id.</span></span>

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

### <span data-ttu-id="82843-122">-Stato</span><span class="sxs-lookup"><span data-stu-id="82843-122">-Status</span></span>
<span data-ttu-id="82843-123">Parametri dello stato del processo di migrazione del disco.</span><span class="sxs-lookup"><span data-stu-id="82843-123">The parameters of disk migration job status.</span></span>

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

### <span data-ttu-id="82843-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82843-124">CommonParameters</span></span>
<span data-ttu-id="82843-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82843-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82843-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82843-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82843-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="82843-127">INPUTS</span></span>

## <span data-ttu-id="82843-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="82843-128">OUTPUTS</span></span>

### <span data-ttu-id="82843-129">Microsoft. AzureStack. Management. Compute. admin. Models. DiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="82843-129">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="82843-130">Note</span><span class="sxs-lookup"><span data-stu-id="82843-130">NOTES</span></span>

## <span data-ttu-id="82843-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="82843-131">RELATED LINKS</span></span>

