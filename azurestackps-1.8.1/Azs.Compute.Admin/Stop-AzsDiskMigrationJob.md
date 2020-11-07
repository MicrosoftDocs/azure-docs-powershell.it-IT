---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ee1a9ae5a4d5ef7545ee9a3e071fcc06475034f4
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859685"
---
# <span data-ttu-id="9c344-101">Stop-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="9c344-101">Stop-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="9c344-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9c344-102">SYNOPSIS</span></span>
<span data-ttu-id="9c344-103">Annullare un processo di migrazione su disco gestito.</span><span class="sxs-lookup"><span data-stu-id="9c344-103">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="9c344-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9c344-104">SYNTAX</span></span>

```
Stop-AzsDiskMigrationJob [[-Location] <String>] [[-Name] <String>] [<CommonParameters>]
```

## <span data-ttu-id="9c344-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9c344-105">DESCRIPTION</span></span>
<span data-ttu-id="9c344-106">Annullare un processo di migrazione del disco.</span><span class="sxs-lookup"><span data-stu-id="9c344-106">Cancel a disk migration job.</span></span>

## <span data-ttu-id="9c344-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9c344-107">EXAMPLES</span></span>

### <span data-ttu-id="9c344-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9c344-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsDiskMigrationJob -Location local -MigrationId $migration.MigrationId
```

<span data-ttu-id="9c344-109">Annullare un processo di migrazione su disco gestito.</span><span class="sxs-lookup"><span data-stu-id="9c344-109">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="9c344-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9c344-110">PARAMETERS</span></span>

### <span data-ttu-id="9c344-111">-Posizione</span><span class="sxs-lookup"><span data-stu-id="9c344-111">-Location</span></span>
<span data-ttu-id="9c344-112">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="9c344-112">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c344-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="9c344-113">-Name</span></span>
<span data-ttu-id="9c344-114">Nome GUID processo di migrazione.</span><span class="sxs-lookup"><span data-stu-id="9c344-114">The migration job guid name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: MigrationId

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c344-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c344-115">CommonParameters</span></span>
<span data-ttu-id="9c344-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c344-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c344-117">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c344-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c344-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9c344-118">INPUTS</span></span>

## <span data-ttu-id="9c344-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9c344-119">OUTPUTS</span></span>

### <span data-ttu-id="9c344-120">Microsoft. AzureStack. Management. Compute. admin. Models. DiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="9c344-120">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="9c344-121">Note</span><span class="sxs-lookup"><span data-stu-id="9c344-121">NOTES</span></span>

## <span data-ttu-id="9c344-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9c344-122">RELATED LINKS</span></span>

