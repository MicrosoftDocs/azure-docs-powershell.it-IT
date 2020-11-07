---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4847310f65a0b652d15321cd49583212ef5844d8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93858390"
---
# <span data-ttu-id="1bb0e-101">Get-AzsStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1bb0e-101">Get-AzsStorageContainer</span></span>

## <span data-ttu-id="1bb0e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1bb0e-102">SYNOPSIS</span></span>
<span data-ttu-id="1bb0e-103">Restituisce l'elenco di contenitori di cui è possibile eseguire la migrazione nella condivisione specificata.</span><span class="sxs-lookup"><span data-stu-id="1bb0e-103">Returns the list of containers which can be migrated in the specified share.</span></span>

## <span data-ttu-id="1bb0e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1bb0e-104">SYNTAX</span></span>

```
Get-AzsStorageContainer [-FarmName] <String> [-ShareName] <String> [[-ResourceGroupName] <String>]
 [[-MaxCount] <Int32>] [[-StartIndex] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="1bb0e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1bb0e-105">DESCRIPTION</span></span>
<span data-ttu-id="1bb0e-106">Restituisce l'elenco di contenitori di cui è possibile eseguire la migrazione nella condivisione specificata.</span><span class="sxs-lookup"><span data-stu-id="1bb0e-106">Returns the list of containers which can be migrated in the specified share.</span></span>

## <span data-ttu-id="1bb0e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1bb0e-107">EXAMPLES</span></span>

### <span data-ttu-id="1bb0e-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1bb0e-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageContainer -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -ShareName "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="1bb0e-109">Ottenere un elenco di contenitori di cui è possibile eseguire la migrazione nella condivisione specificata.</span><span class="sxs-lookup"><span data-stu-id="1bb0e-109">Get a list of containers which can be migrated in the specified share.</span></span>

## <span data-ttu-id="1bb0e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1bb0e-110">PARAMETERS</span></span>

### <span data-ttu-id="1bb0e-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="1bb0e-111">-FarmName</span></span>
<span data-ttu-id="1bb0e-112">ID farm.</span><span class="sxs-lookup"><span data-stu-id="1bb0e-112">Farm Id.</span></span>

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

### <span data-ttu-id="1bb0e-113">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="1bb0e-113">-MaxCount</span></span>
<span data-ttu-id="1bb0e-114">Numero massimo di contenitori.</span><span class="sxs-lookup"><span data-stu-id="1bb0e-114">The max count of containers.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: 100000000
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bb0e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bb0e-115">-ResourceGroupName</span></span>
<span data-ttu-id="1bb0e-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1bb0e-116">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bb0e-117">-ShareName</span><span class="sxs-lookup"><span data-stu-id="1bb0e-117">-ShareName</span></span>
<span data-ttu-id="1bb0e-118">Condividere il nome che contiene i contenitori di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1bb0e-118">Share name which holds the storage containers.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bb0e-119">-StartIndex</span><span class="sxs-lookup"><span data-stu-id="1bb0e-119">-StartIndex</span></span>
<span data-ttu-id="1bb0e-120">Indice Start di Get Containers.</span><span class="sxs-lookup"><span data-stu-id="1bb0e-120">The start index of get containers.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bb0e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bb0e-121">CommonParameters</span></span>
<span data-ttu-id="1bb0e-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bb0e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bb0e-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bb0e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bb0e-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1bb0e-124">INPUTS</span></span>

## <span data-ttu-id="1bb0e-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1bb0e-125">OUTPUTS</span></span>

## <span data-ttu-id="1bb0e-126">Note</span><span class="sxs-lookup"><span data-stu-id="1bb0e-126">NOTES</span></span>

## <span data-ttu-id="1bb0e-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1bb0e-127">RELATED LINKS</span></span>

