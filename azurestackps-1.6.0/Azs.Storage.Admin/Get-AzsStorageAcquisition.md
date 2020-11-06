---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3562b169211d4c3b1f87260be37a94f6de2e8b85
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491290"
---
# <span data-ttu-id="174c8-101">Get-AzsStorageAcquisition</span><span class="sxs-lookup"><span data-stu-id="174c8-101">Get-AzsStorageAcquisition</span></span>

## <span data-ttu-id="174c8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="174c8-102">SYNOPSIS</span></span>
<span data-ttu-id="174c8-103">Restituisce un elenco di BLOB Acquistions.</span><span class="sxs-lookup"><span data-stu-id="174c8-103">Returns a list of blob acquistions.</span></span>

## <span data-ttu-id="174c8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="174c8-104">SYNTAX</span></span>

```
Get-AzsStorageAcquisition [-FarmName] <String> [-ResourceGroupName <String>] [-Filter <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="174c8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="174c8-105">DESCRIPTION</span></span>
<span data-ttu-id="174c8-106">Restituisce un elenco di BLOB Acquistions.</span><span class="sxs-lookup"><span data-stu-id="174c8-106">Returns a list of blob acquistions.</span></span>

## <span data-ttu-id="174c8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="174c8-107">EXAMPLES</span></span>

### <span data-ttu-id="174c8-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="174c8-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageAcquisition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="174c8-109">Ottenere l'elenco di BLOB Acquistions.</span><span class="sxs-lookup"><span data-stu-id="174c8-109">Get the list of blob acquistions.</span></span>

### <span data-ttu-id="174c8-110">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="174c8-110">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageAcquisition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -Filter "startswith(properties/Storageaccount, 'Test'"
```

<span data-ttu-id="174c8-111">Ottenere l'elenco di BLOB Acquistions.</span><span class="sxs-lookup"><span data-stu-id="174c8-111">Get the list of blob acquistions.</span></span>

## <span data-ttu-id="174c8-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="174c8-112">PARAMETERS</span></span>

### <span data-ttu-id="174c8-113">-Farmname</span><span class="sxs-lookup"><span data-stu-id="174c8-113">-FarmName</span></span>
<span data-ttu-id="174c8-114">ID farm.</span><span class="sxs-lookup"><span data-stu-id="174c8-114">Farm Id.</span></span>

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

### <span data-ttu-id="174c8-115">-Filtro</span><span class="sxs-lookup"><span data-stu-id="174c8-115">-Filter</span></span>
<span data-ttu-id="174c8-116">Stringa di filtro</span><span class="sxs-lookup"><span data-stu-id="174c8-116">Filter string</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="174c8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="174c8-117">-ResourceGroupName</span></span>
<span data-ttu-id="174c8-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="174c8-118">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="174c8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="174c8-119">CommonParameters</span></span>
<span data-ttu-id="174c8-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="174c8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="174c8-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="174c8-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="174c8-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="174c8-122">INPUTS</span></span>

## <span data-ttu-id="174c8-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="174c8-123">OUTPUTS</span></span>

## <span data-ttu-id="174c8-124">Note</span><span class="sxs-lookup"><span data-stu-id="174c8-124">NOTES</span></span>

## <span data-ttu-id="174c8-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="174c8-125">RELATED LINKS</span></span>

