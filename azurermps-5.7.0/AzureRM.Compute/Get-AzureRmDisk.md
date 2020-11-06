---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmDisk.md
ms.openlocfilehash: e34016b3bc7677c9591c07e54dd42a88a820d44b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516891"
---
# <span data-ttu-id="6135d-101">Get-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="6135d-101">Get-AzureRmDisk</span></span>

## <span data-ttu-id="6135d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6135d-102">SYNOPSIS</span></span>
<span data-ttu-id="6135d-103">Ottiene le proprietà di un disco.</span><span class="sxs-lookup"><span data-stu-id="6135d-103">Gets the properties of a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6135d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6135d-104">SYNTAX</span></span>

```
Get-AzureRmDisk [[-ResourceGroupName] <String>] [[-DiskName] <String>] [<CommonParameters>]
```

## <span data-ttu-id="6135d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6135d-105">DESCRIPTION</span></span>
<span data-ttu-id="6135d-106">Il cmdlet **Get-AzureRmDisk** ottiene le proprietà di un disco.</span><span class="sxs-lookup"><span data-stu-id="6135d-106">The **Get-AzureRmDisk** cmdlet gets the properties of a disk.</span></span>

## <span data-ttu-id="6135d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6135d-107">EXAMPLES</span></span>

### <span data-ttu-id="6135d-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6135d-108">Example 1</span></span>
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="6135d-109">Questo comando consente di ottenere le proprietà del disco denominato "Disk01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="6135d-109">This command gets the properties of the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="6135d-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="6135d-110">Example 2</span></span>
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="6135d-111">Questo comando consente di ottenere le proprietà di tutti i dischi nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="6135d-111">This command gets the properties of all disks in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="6135d-112">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="6135d-112">Example 3</span></span>
```
PS C:\> Get-AzureRmDisk
```

<span data-ttu-id="6135d-113">Questo comando consente di ottenere le proprietà di tutti i dischi sotto l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="6135d-113">This command gets the properties of all disks under the subscription.</span></span>

## <span data-ttu-id="6135d-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6135d-114">PARAMETERS</span></span>

### <span data-ttu-id="6135d-115">-Diskname</span><span class="sxs-lookup"><span data-stu-id="6135d-115">-DiskName</span></span>
<span data-ttu-id="6135d-116">Specifica il nome di un disco.</span><span class="sxs-lookup"><span data-stu-id="6135d-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="6135d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6135d-117">-ResourceGroupName</span></span>
<span data-ttu-id="6135d-118">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6135d-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="6135d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6135d-119">CommonParameters</span></span>
<span data-ttu-id="6135d-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6135d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6135d-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6135d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6135d-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6135d-122">INPUTS</span></span>

### <span data-ttu-id="6135d-123">System. String</span><span class="sxs-lookup"><span data-stu-id="6135d-123">System.String</span></span>

## <span data-ttu-id="6135d-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6135d-124">OUTPUTS</span></span>

### <span data-ttu-id="6135d-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskList</span><span class="sxs-lookup"><span data-stu-id="6135d-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskList</span></span>

## <span data-ttu-id="6135d-126">Note</span><span class="sxs-lookup"><span data-stu-id="6135d-126">NOTES</span></span>

## <span data-ttu-id="6135d-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6135d-127">RELATED LINKS</span></span>

