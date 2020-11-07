---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0a75fafa646839375bf9dc7f1a64b3084fd31ee4
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859813"
---
# <span data-ttu-id="5844f-101">Get-AzsStorageDestinationShare</span><span class="sxs-lookup"><span data-stu-id="5844f-101">Get-AzsStorageDestinationShare</span></span>

## <span data-ttu-id="5844f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5844f-102">SYNOPSIS</span></span>
<span data-ttu-id="5844f-103">Restituisce un elenco di condivisioni di destinazione che il sistema considera come migliori candidati per la migrazione.</span><span class="sxs-lookup"><span data-stu-id="5844f-103">Returns a list of destination shares that the system considers as best candidates for migration.</span></span>

## <span data-ttu-id="5844f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5844f-104">SYNTAX</span></span>

```
Get-AzsStorageDestinationShare [-SourceShareName] <String> [-FarmName] <String> [[-ResourceGroupName] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="5844f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5844f-105">DESCRIPTION</span></span>
<span data-ttu-id="5844f-106">Restituisce un elenco di condivisioni di destinazione che il sistema considera come migliori candidati per la migrazione.</span><span class="sxs-lookup"><span data-stu-id="5844f-106">Returns a list of destination shares that the system considers as best candidates for migration.</span></span>

## <span data-ttu-id="5844f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5844f-107">EXAMPLES</span></span>

### <span data-ttu-id="5844f-108">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="5844f-108">EXAMPLE 1</span></span>
```
Get-AzsStorageDestinationShare -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -SourceShareName "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="5844f-109">Ottenere un elenco delle condivisioni di destinazione che il sistema ritiene migliori candidati per la migrazione.</span><span class="sxs-lookup"><span data-stu-id="5844f-109">Get a list of destination shares that the system considers as best candidates for migration.</span></span>

## <span data-ttu-id="5844f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5844f-110">PARAMETERS</span></span>

### <span data-ttu-id="5844f-111">-SourceShareName</span><span class="sxs-lookup"><span data-stu-id="5844f-111">-SourceShareName</span></span>
<span data-ttu-id="5844f-112">Nome della condivisione che contiene i contenitori di cui eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="5844f-112">Name of the share which holds containers to be migrated.</span></span>

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

### <span data-ttu-id="5844f-113">-Farmname</span><span class="sxs-lookup"><span data-stu-id="5844f-113">-FarmName</span></span>
<span data-ttu-id="5844f-114">ID farm.</span><span class="sxs-lookup"><span data-stu-id="5844f-114">Farm Id.</span></span>

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

### <span data-ttu-id="5844f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5844f-115">-ResourceGroupName</span></span>
<span data-ttu-id="5844f-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5844f-116">Resource group name.</span></span>

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

### <span data-ttu-id="5844f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5844f-117">CommonParameters</span></span>
<span data-ttu-id="5844f-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5844f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5844f-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5844f-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5844f-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5844f-120">INPUTS</span></span>

## <span data-ttu-id="5844f-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5844f-121">OUTPUTS</span></span>

## <span data-ttu-id="5844f-122">Note</span><span class="sxs-lookup"><span data-stu-id="5844f-122">NOTES</span></span>

## <span data-ttu-id="5844f-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5844f-123">RELATED LINKS</span></span>
