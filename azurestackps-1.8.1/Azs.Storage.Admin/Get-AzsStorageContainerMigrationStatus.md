---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 96220d7bac0a71f579f81a4d01f4f1dc3cba9dd1
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859814"
---
# <span data-ttu-id="8d94a-101">Get-AzsStorageContainerMigrationStatus</span><span class="sxs-lookup"><span data-stu-id="8d94a-101">Get-AzsStorageContainerMigrationStatus</span></span>

## <span data-ttu-id="8d94a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8d94a-102">SYNOPSIS</span></span>
<span data-ttu-id="8d94a-103">Restituisce lo stato di un processo di migrazione dei contenitori.</span><span class="sxs-lookup"><span data-stu-id="8d94a-103">Returns the status of a container migration job.</span></span>

## <span data-ttu-id="8d94a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8d94a-104">SYNTAX</span></span>

```
Get-AzsStorageContainerMigrationStatus [-FarmName] <String> [-JobId] <String> [[-ResourceGroupName] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="8d94a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8d94a-105">DESCRIPTION</span></span>
<span data-ttu-id="8d94a-106">Restituisce lo stato di un processo di migrazione dei contenitori.</span><span class="sxs-lookup"><span data-stu-id="8d94a-106">Returns the status of a container migration job.</span></span>

## <span data-ttu-id="8d94a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8d94a-107">EXAMPLES</span></span>

### <span data-ttu-id="8d94a-108">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="8d94a-108">EXAMPLE 1</span></span>
```
Get-AzsStorageContainerMigrationStatus -FarmName "6ed442a3-ec47-4145-b2f0-9b90377b01d0" -JobId "6478ef3b-b7d5-4827-8d47-551c6afb9dd4"
```

<span data-ttu-id="8d94a-109">Ottenere lo stato di un processo di migrazione dei contenitori.</span><span class="sxs-lookup"><span data-stu-id="8d94a-109">Get the status of a container migration job.</span></span>

## <span data-ttu-id="8d94a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8d94a-110">PARAMETERS</span></span>

### <span data-ttu-id="8d94a-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="8d94a-111">-FarmName</span></span>
<span data-ttu-id="8d94a-112">ID farm.</span><span class="sxs-lookup"><span data-stu-id="8d94a-112">Farm Id.</span></span>

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

### <span data-ttu-id="8d94a-113">-JobId</span><span class="sxs-lookup"><span data-stu-id="8d94a-113">-JobId</span></span>
<span data-ttu-id="8d94a-114">ID operazione.</span><span class="sxs-lookup"><span data-stu-id="8d94a-114">Operation Id.</span></span>

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

### <span data-ttu-id="8d94a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d94a-115">-ResourceGroupName</span></span>
<span data-ttu-id="8d94a-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8d94a-116">Resource group name.</span></span>

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

### <span data-ttu-id="8d94a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d94a-117">CommonParameters</span></span>
<span data-ttu-id="8d94a-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d94a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d94a-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d94a-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d94a-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8d94a-120">INPUTS</span></span>

## <span data-ttu-id="8d94a-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8d94a-121">OUTPUTS</span></span>

### <span data-ttu-id="8d94a-122">Microsoft. AzureStack. Management. storage. admin. Models. MigrationResult</span><span class="sxs-lookup"><span data-stu-id="8d94a-122">Microsoft.AzureStack.Management.Storage.Admin.Models.MigrationResult</span></span>

## <span data-ttu-id="8d94a-123">Note</span><span class="sxs-lookup"><span data-stu-id="8d94a-123">NOTES</span></span>

## <span data-ttu-id="8d94a-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8d94a-124">RELATED LINKS</span></span>
