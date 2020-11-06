---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d38e4bd949a6118f55ce0096a8ca56d08137bb2a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491473"
---
# <span data-ttu-id="1a101-101">Stop-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="1a101-101">Stop-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="1a101-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1a101-102">SYNOPSIS</span></span>
<span data-ttu-id="1a101-103">Annullare un processo di migrazione su disco gestito.</span><span class="sxs-lookup"><span data-stu-id="1a101-103">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="1a101-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1a101-104">SYNTAX</span></span>

```
Stop-AzsDiskMigrationJob [[-Location] <String>] [[-Name] <String>] [<CommonParameters>]
```

## <span data-ttu-id="1a101-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a101-105">DESCRIPTION</span></span>
<span data-ttu-id="1a101-106">Annullare un processo di migrazione del disco.</span><span class="sxs-lookup"><span data-stu-id="1a101-106">Cancel a disk migration job.</span></span>

## <span data-ttu-id="1a101-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1a101-107">EXAMPLES</span></span>

### <span data-ttu-id="1a101-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1a101-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsDiskMigrationJob -Location local -MigrationId $migration.MigrationId
```

<span data-ttu-id="1a101-109">Annullare un processo di migrazione su disco gestito.</span><span class="sxs-lookup"><span data-stu-id="1a101-109">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="1a101-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1a101-110">PARAMETERS</span></span>

### <span data-ttu-id="1a101-111">-Posizione</span><span class="sxs-lookup"><span data-stu-id="1a101-111">-Location</span></span>
<span data-ttu-id="1a101-112">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="1a101-112">Location of the resource.</span></span>

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

### <span data-ttu-id="1a101-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="1a101-113">-Name</span></span>
<span data-ttu-id="1a101-114">Nome GUID processo di migrazione.</span><span class="sxs-lookup"><span data-stu-id="1a101-114">The migration job guid name.</span></span>

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

### <span data-ttu-id="1a101-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a101-115">CommonParameters</span></span>
<span data-ttu-id="1a101-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a101-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a101-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a101-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a101-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1a101-118">INPUTS</span></span>

## <span data-ttu-id="1a101-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1a101-119">OUTPUTS</span></span>

### <span data-ttu-id="1a101-120">Microsoft. AzureStack. Management. Compute. admin. Models. DiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="1a101-120">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="1a101-121">Note</span><span class="sxs-lookup"><span data-stu-id="1a101-121">NOTES</span></span>

## <span data-ttu-id="1a101-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1a101-122">RELATED LINKS</span></span>

