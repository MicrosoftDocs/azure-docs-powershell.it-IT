---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 34d5c967154f08526a0002f187b8cb869d933d39
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93860029"
---
# <span data-ttu-id="6275d-101">Get-AzsStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6275d-101">Get-AzsStorageContainer</span></span>

## <span data-ttu-id="6275d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6275d-102">SYNOPSIS</span></span>
<span data-ttu-id="6275d-103">Restituisce l'elenco di contenitori di cui è possibile eseguire la migrazione nella condivisione specificata.</span><span class="sxs-lookup"><span data-stu-id="6275d-103">Returns the list of containers which can be migrated in the specified share.</span></span>

## <span data-ttu-id="6275d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6275d-104">SYNTAX</span></span>

```
Get-AzsStorageContainer [-FarmName] <String> [-ShareName] <String> [[-ResourceGroupName] <String>]
 [[-MaxCount] <Int32>] [[-StartIndex] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="6275d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6275d-105">DESCRIPTION</span></span>
<span data-ttu-id="6275d-106">Restituisce l'elenco di contenitori di cui è possibile eseguire la migrazione nella condivisione specificata.</span><span class="sxs-lookup"><span data-stu-id="6275d-106">Returns the list of containers which can be migrated in the specified share.</span></span>

## <span data-ttu-id="6275d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6275d-107">EXAMPLES</span></span>

### <span data-ttu-id="6275d-108">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="6275d-108">EXAMPLE 1</span></span>
```
Get-AzsStorageContainer -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -ShareName "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="6275d-109">Ottenere un elenco di contenitori di cui è possibile eseguire la migrazione nella condivisione specificata.</span><span class="sxs-lookup"><span data-stu-id="6275d-109">Get a list of containers which can be migrated in the specified share.</span></span>

## <span data-ttu-id="6275d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6275d-110">PARAMETERS</span></span>

### <span data-ttu-id="6275d-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="6275d-111">-FarmName</span></span>
<span data-ttu-id="6275d-112">ID farm.</span><span class="sxs-lookup"><span data-stu-id="6275d-112">Farm Id.</span></span>

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

### <span data-ttu-id="6275d-113">-ShareName</span><span class="sxs-lookup"><span data-stu-id="6275d-113">-ShareName</span></span>
<span data-ttu-id="6275d-114">Condividere il nome che contiene i contenitori di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="6275d-114">Share name which holds the storage containers.</span></span>

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

### <span data-ttu-id="6275d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6275d-115">-ResourceGroupName</span></span>
<span data-ttu-id="6275d-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6275d-116">Resource group name.</span></span>

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

### <span data-ttu-id="6275d-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="6275d-117">-MaxCount</span></span>
<span data-ttu-id="6275d-118">Numero massimo di contenitori.</span><span class="sxs-lookup"><span data-stu-id="6275d-118">The max count of containers.</span></span>

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

### <span data-ttu-id="6275d-119">-StartIndex</span><span class="sxs-lookup"><span data-stu-id="6275d-119">-StartIndex</span></span>
<span data-ttu-id="6275d-120">Indice Start di Get Containers.</span><span class="sxs-lookup"><span data-stu-id="6275d-120">The start index of get containers.</span></span>

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

### <span data-ttu-id="6275d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6275d-121">CommonParameters</span></span>
<span data-ttu-id="6275d-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6275d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6275d-123">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6275d-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6275d-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6275d-124">INPUTS</span></span>

## <span data-ttu-id="6275d-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6275d-125">OUTPUTS</span></span>

## <span data-ttu-id="6275d-126">Note</span><span class="sxs-lookup"><span data-stu-id="6275d-126">NOTES</span></span>

## <span data-ttu-id="6275d-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6275d-127">RELATED LINKS</span></span>
