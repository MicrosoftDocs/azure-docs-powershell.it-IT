---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 47ac85406955592cba566df505900e6c42befb7a
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "93859378"
---
# <span data-ttu-id="8007f-101">Get-AzsStorageDestinationShare</span><span class="sxs-lookup"><span data-stu-id="8007f-101">Get-AzsStorageDestinationShare</span></span>

## <span data-ttu-id="8007f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8007f-102">SYNOPSIS</span></span>
<span data-ttu-id="8007f-103">Restituisce un elenco di condivisioni di destinazione che il sistema considera come migliori candidati per la migrazione.</span><span class="sxs-lookup"><span data-stu-id="8007f-103">Returns a list of destination shares that the system considers as best candidates for migration.</span></span>

## <span data-ttu-id="8007f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8007f-104">SYNTAX</span></span>

```
Get-AzsStorageDestinationShare [-SourceShareName] <String> [-FarmName] <String> [[-ResourceGroupName] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="8007f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8007f-105">DESCRIPTION</span></span>
<span data-ttu-id="8007f-106">Restituisce un elenco di condivisioni di destinazione che il sistema considera come migliori candidati per la migrazione.</span><span class="sxs-lookup"><span data-stu-id="8007f-106">Returns a list of destination shares that the system considers as best candidates for migration.</span></span>

## <span data-ttu-id="8007f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8007f-107">EXAMPLES</span></span>

### <span data-ttu-id="8007f-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8007f-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageDestinationShare -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -SourceShareName "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="8007f-109">Ottenere un elenco delle condivisioni di destinazione che il sistema ritiene migliori candidati per la migrazione.</span><span class="sxs-lookup"><span data-stu-id="8007f-109">Get a list of destination shares that the system considers as best candidates for migration.</span></span>

## <span data-ttu-id="8007f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8007f-110">PARAMETERS</span></span>

### <span data-ttu-id="8007f-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="8007f-111">-FarmName</span></span>
<span data-ttu-id="8007f-112">ID farm.</span><span class="sxs-lookup"><span data-stu-id="8007f-112">Farm Id.</span></span>

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

### <span data-ttu-id="8007f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8007f-113">-ResourceGroupName</span></span>
<span data-ttu-id="8007f-114">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8007f-114">Resource group name.</span></span>

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

### <span data-ttu-id="8007f-115">-SourceShareName</span><span class="sxs-lookup"><span data-stu-id="8007f-115">-SourceShareName</span></span>
<span data-ttu-id="8007f-116">Nome della condivisione che contiene i contenitori di cui eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="8007f-116">Name of the share which holds containers to be migrated.</span></span>

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

### <span data-ttu-id="8007f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8007f-117">CommonParameters</span></span>
<span data-ttu-id="8007f-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8007f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8007f-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8007f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8007f-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8007f-120">INPUTS</span></span>

## <span data-ttu-id="8007f-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8007f-121">OUTPUTS</span></span>

## <span data-ttu-id="8007f-122">Note</span><span class="sxs-lookup"><span data-stu-id="8007f-122">NOTES</span></span>

## <span data-ttu-id="8007f-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8007f-123">RELATED LINKS</span></span>

