---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3a53b5af4cf77ec961e65f8c0c0d84b05b4adfa1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030354"
---
# <span data-ttu-id="286c4-101">Get-AzsStorageAcquisition</span><span class="sxs-lookup"><span data-stu-id="286c4-101">Get-AzsStorageAcquisition</span></span>

## <span data-ttu-id="286c4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="286c4-102">SYNOPSIS</span></span>
<span data-ttu-id="286c4-103">Restituisce un elenco di BLOB Acquistions.</span><span class="sxs-lookup"><span data-stu-id="286c4-103">Returns a list of blob acquistions.</span></span>

## <span data-ttu-id="286c4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="286c4-104">SYNTAX</span></span>

```
Get-AzsStorageAcquisition [-FarmName] <String> [-ResourceGroupName <String>] [-Filter <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="286c4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="286c4-105">DESCRIPTION</span></span>
<span data-ttu-id="286c4-106">Restituisce un elenco di BLOB Acquistions.</span><span class="sxs-lookup"><span data-stu-id="286c4-106">Returns a list of blob acquistions.</span></span>

## <span data-ttu-id="286c4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="286c4-107">EXAMPLES</span></span>

### <span data-ttu-id="286c4-108">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="286c4-108">EXAMPLE 1</span></span>
```
Get-AzsStorageAcquisition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="286c4-109">Ottenere l'elenco di BLOB Acquistions.</span><span class="sxs-lookup"><span data-stu-id="286c4-109">Get the list of blob acquistions.</span></span>

### <span data-ttu-id="286c4-110">ESEMPIO 2</span><span class="sxs-lookup"><span data-stu-id="286c4-110">EXAMPLE 2</span></span>
```
Get-AzsStorageAcquisition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -Filter "startswith(properties/Storageaccount, 'Test'"
```

<span data-ttu-id="286c4-111">Ottenere l'elenco di BLOB Acquistions.</span><span class="sxs-lookup"><span data-stu-id="286c4-111">Get the list of blob acquistions.</span></span>

## <span data-ttu-id="286c4-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="286c4-112">PARAMETERS</span></span>

### <span data-ttu-id="286c4-113">-Farmname</span><span class="sxs-lookup"><span data-stu-id="286c4-113">-FarmName</span></span>
<span data-ttu-id="286c4-114">ID farm.</span><span class="sxs-lookup"><span data-stu-id="286c4-114">Farm Id.</span></span>

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

### <span data-ttu-id="286c4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="286c4-115">-ResourceGroupName</span></span>
<span data-ttu-id="286c4-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="286c4-116">Resource group name.</span></span>

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

### <span data-ttu-id="286c4-117">-Filtro</span><span class="sxs-lookup"><span data-stu-id="286c4-117">-Filter</span></span>
<span data-ttu-id="286c4-118">Stringa di filtro</span><span class="sxs-lookup"><span data-stu-id="286c4-118">Filter string</span></span>

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

### <span data-ttu-id="286c4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="286c4-119">CommonParameters</span></span>
<span data-ttu-id="286c4-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="286c4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="286c4-121">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="286c4-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="286c4-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="286c4-122">INPUTS</span></span>

## <span data-ttu-id="286c4-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="286c4-123">OUTPUTS</span></span>

## <span data-ttu-id="286c4-124">Note</span><span class="sxs-lookup"><span data-stu-id="286c4-124">NOTES</span></span>

## <span data-ttu-id="286c4-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="286c4-125">RELATED LINKS</span></span>
