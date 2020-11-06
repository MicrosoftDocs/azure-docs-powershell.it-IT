---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmSnapshot.md
ms.openlocfilehash: 9f4d2c4e6321d36079cf4c5e87747863c8dc51c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516883"
---
# <span data-ttu-id="73ac9-101">Get-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="73ac9-101">Get-AzureRmSnapshot</span></span>

## <span data-ttu-id="73ac9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="73ac9-102">SYNOPSIS</span></span>
<span data-ttu-id="73ac9-103">Ottiene le proprietà di uno snapshot</span><span class="sxs-lookup"><span data-stu-id="73ac9-103">Gets the properties of a snapshot</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73ac9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="73ac9-104">SYNTAX</span></span>

```
Get-AzureRmSnapshot [[-ResourceGroupName] <String>] [[-SnapshotName] <String>] [<CommonParameters>]
```

## <span data-ttu-id="73ac9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="73ac9-105">DESCRIPTION</span></span>
<span data-ttu-id="73ac9-106">Il cmdlet **Get-AzureRmSnapshot** ottiene le proprietà di uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="73ac9-106">The **Get-AzureRmSnapshot** cmdlet gets the properties of a snapshot.</span></span>

## <span data-ttu-id="73ac9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="73ac9-107">EXAMPLES</span></span>

### <span data-ttu-id="73ac9-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="73ac9-108">Example 1</span></span>
```
PS C:\> Get-AzureRmSnapshot
```

<span data-ttu-id="73ac9-109">Questo comando consente di ottenere le proprietà di tutti gli snapshot dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="73ac9-109">This command gets the properties of all snapshots of the subscription.</span></span>

### <span data-ttu-id="73ac9-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="73ac9-110">Example 2</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1"
```

<span data-ttu-id="73ac9-111">Questo comando consente di ottenere le proprietà di tutti gli snapshot nel gruppo di risorse denominato "ResourceGroupName1".</span><span class="sxs-lookup"><span data-stu-id="73ac9-111">This command gets the properties of all snapshots in the resource group named "ResourceGroupName1"</span></span>

### <span data-ttu-id="73ac9-112">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="73ac9-112">Example 3</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1" -SnapshotName "SnapshotName1"
```

<span data-ttu-id="73ac9-113">Questo comando consente di ottenere le proprietà dello snapshot denominato "SnapshotName1" nel gruppo di risorse denominato "ResourceGroupName1".</span><span class="sxs-lookup"><span data-stu-id="73ac9-113">This command gets the properties of the snapshot named "SnapshotName1" in the resource group named "ResourceGroupName1"</span></span>

## <span data-ttu-id="73ac9-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="73ac9-114">PARAMETERS</span></span>

### <span data-ttu-id="73ac9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73ac9-115">-ResourceGroupName</span></span>
<span data-ttu-id="73ac9-116">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="73ac9-116">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73ac9-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="73ac9-117">-SnapshotName</span></span>
<span data-ttu-id="73ac9-118">Specifica il nome di uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="73ac9-118">Specifies the name of a snapshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73ac9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73ac9-119">CommonParameters</span></span>
<span data-ttu-id="73ac9-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73ac9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73ac9-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73ac9-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73ac9-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="73ac9-122">INPUTS</span></span>

### <span data-ttu-id="73ac9-123">System. String</span><span class="sxs-lookup"><span data-stu-id="73ac9-123">System.String</span></span>

## <span data-ttu-id="73ac9-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="73ac9-124">OUTPUTS</span></span>

### <span data-ttu-id="73ac9-125">System. Object</span><span class="sxs-lookup"><span data-stu-id="73ac9-125">System.Object</span></span>

## <span data-ttu-id="73ac9-126">Note</span><span class="sxs-lookup"><span data-stu-id="73ac9-126">NOTES</span></span>

## <span data-ttu-id="73ac9-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="73ac9-127">RELATED LINKS</span></span>

