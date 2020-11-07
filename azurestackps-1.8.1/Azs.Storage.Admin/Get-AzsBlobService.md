---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a0fb6da4bde577d5a69c5bd85261822e3cf1865d
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859850"
---
# <span data-ttu-id="6cdff-101">Get-AzsBlobService</span><span class="sxs-lookup"><span data-stu-id="6cdff-101">Get-AzsBlobService</span></span>

## <span data-ttu-id="6cdff-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6cdff-102">SYNOPSIS</span></span>
<span data-ttu-id="6cdff-103">Restituisce il servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="6cdff-103">Returns the blob service.</span></span>

## <span data-ttu-id="6cdff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6cdff-104">SYNTAX</span></span>

```
Get-AzsBlobService [-FarmName] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

## <span data-ttu-id="6cdff-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6cdff-105">DESCRIPTION</span></span>
<span data-ttu-id="6cdff-106">Restituisce il servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="6cdff-106">Returns the blob service.</span></span>

## <span data-ttu-id="6cdff-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6cdff-107">EXAMPLES</span></span>

### <span data-ttu-id="6cdff-108">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="6cdff-108">EXAMPLE 1</span></span>
```
Get-AzsBlobService -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="6cdff-109">Ottenere il servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="6cdff-109">Get the blob service.</span></span>

## <span data-ttu-id="6cdff-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6cdff-110">PARAMETERS</span></span>

### <span data-ttu-id="6cdff-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="6cdff-111">-FarmName</span></span>
<span data-ttu-id="6cdff-112">ID farm.</span><span class="sxs-lookup"><span data-stu-id="6cdff-112">Farm Id.</span></span>

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

### <span data-ttu-id="6cdff-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cdff-113">-ResourceGroupName</span></span>
<span data-ttu-id="6cdff-114">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6cdff-114">Resource group name.</span></span>

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

### <span data-ttu-id="6cdff-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cdff-115">CommonParameters</span></span>
<span data-ttu-id="6cdff-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cdff-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cdff-117">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cdff-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cdff-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6cdff-118">INPUTS</span></span>

## <span data-ttu-id="6cdff-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6cdff-119">OUTPUTS</span></span>

### <span data-ttu-id="6cdff-120">Microsoft. AzureStack. Management. storage. admin. Models. BlobService</span><span class="sxs-lookup"><span data-stu-id="6cdff-120">Microsoft.AzureStack.Management.Storage.Admin.Models.BlobService</span></span>

## <span data-ttu-id="6cdff-121">Note</span><span class="sxs-lookup"><span data-stu-id="6cdff-121">NOTES</span></span>

## <span data-ttu-id="6cdff-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6cdff-122">RELATED LINKS</span></span>
