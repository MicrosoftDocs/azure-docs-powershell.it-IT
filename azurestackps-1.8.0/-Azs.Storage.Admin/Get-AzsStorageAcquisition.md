---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3562b169211d4c3b1f87260be37a94f6de2e8b85
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "93859386"
---
# <span data-ttu-id="d964b-101">Get-AzsStorageAcquisition</span><span class="sxs-lookup"><span data-stu-id="d964b-101">Get-AzsStorageAcquisition</span></span>

## <span data-ttu-id="d964b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d964b-102">SYNOPSIS</span></span>
<span data-ttu-id="d964b-103">Restituisce un elenco di BLOB Acquistions.</span><span class="sxs-lookup"><span data-stu-id="d964b-103">Returns a list of blob acquistions.</span></span>

## <span data-ttu-id="d964b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d964b-104">SYNTAX</span></span>

```
Get-AzsStorageAcquisition [-FarmName] <String> [-ResourceGroupName <String>] [-Filter <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="d964b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d964b-105">DESCRIPTION</span></span>
<span data-ttu-id="d964b-106">Restituisce un elenco di BLOB Acquistions.</span><span class="sxs-lookup"><span data-stu-id="d964b-106">Returns a list of blob acquistions.</span></span>

## <span data-ttu-id="d964b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d964b-107">EXAMPLES</span></span>

### <span data-ttu-id="d964b-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d964b-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageAcquisition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="d964b-109">Ottenere l'elenco di BLOB Acquistions.</span><span class="sxs-lookup"><span data-stu-id="d964b-109">Get the list of blob acquistions.</span></span>

### <span data-ttu-id="d964b-110">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="d964b-110">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageAcquisition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -Filter "startswith(properties/Storageaccount, 'Test'"
```

<span data-ttu-id="d964b-111">Ottenere l'elenco di BLOB Acquistions.</span><span class="sxs-lookup"><span data-stu-id="d964b-111">Get the list of blob acquistions.</span></span>

## <span data-ttu-id="d964b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d964b-112">PARAMETERS</span></span>

### <span data-ttu-id="d964b-113">-Farmname</span><span class="sxs-lookup"><span data-stu-id="d964b-113">-FarmName</span></span>
<span data-ttu-id="d964b-114">ID farm.</span><span class="sxs-lookup"><span data-stu-id="d964b-114">Farm Id.</span></span>

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

### <span data-ttu-id="d964b-115">-Filtro</span><span class="sxs-lookup"><span data-stu-id="d964b-115">-Filter</span></span>
<span data-ttu-id="d964b-116">Stringa di filtro</span><span class="sxs-lookup"><span data-stu-id="d964b-116">Filter string</span></span>

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

### <span data-ttu-id="d964b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d964b-117">-ResourceGroupName</span></span>
<span data-ttu-id="d964b-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d964b-118">Resource group name.</span></span>

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

### <span data-ttu-id="d964b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d964b-119">CommonParameters</span></span>
<span data-ttu-id="d964b-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d964b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d964b-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d964b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d964b-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d964b-122">INPUTS</span></span>

## <span data-ttu-id="d964b-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d964b-123">OUTPUTS</span></span>

## <span data-ttu-id="d964b-124">Note</span><span class="sxs-lookup"><span data-stu-id="d964b-124">NOTES</span></span>

## <span data-ttu-id="d964b-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d964b-125">RELATED LINKS</span></span>

