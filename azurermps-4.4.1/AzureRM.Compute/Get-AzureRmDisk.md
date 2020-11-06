---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmDisk.md
ms.openlocfilehash: e598c266f46815e7005c43e2d354ad8ece06efc7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521270"
---
# <span data-ttu-id="f664d-101">Get-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="f664d-101">Get-AzureRmDisk</span></span>

## <span data-ttu-id="f664d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f664d-102">SYNOPSIS</span></span>
<span data-ttu-id="f664d-103">Ottiene le proprietà di un disco.</span><span class="sxs-lookup"><span data-stu-id="f664d-103">Gets the properties of a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f664d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f664d-104">SYNTAX</span></span>

```
Get-AzureRmDisk [[-ResourceGroupName] <String>] [[-DiskName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f664d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f664d-105">DESCRIPTION</span></span>
<span data-ttu-id="f664d-106">Il cmdlet **Get-AzureRmDisk** ottiene le proprietà di un disco.</span><span class="sxs-lookup"><span data-stu-id="f664d-106">The **Get-AzureRmDisk** cmdlet gets the properties of a disk.</span></span>

## <span data-ttu-id="f664d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f664d-107">EXAMPLES</span></span>

### <span data-ttu-id="f664d-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f664d-108">Example 1</span></span>
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="f664d-109">Questo comando consente di ottenere le proprietà del disco denominato "Disk01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="f664d-109">This command gets the properties of the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="f664d-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f664d-110">Example 2</span></span>
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="f664d-111">Questo comando consente di ottenere le proprietà di tutti i dischi nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="f664d-111">This command gets the properties of all disks in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="f664d-112">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="f664d-112">Example 3</span></span>
```
PS C:\> Get-AzureRmDisk
```

<span data-ttu-id="f664d-113">Questo comando consente di ottenere le proprietà di tutti i dischi sotto l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="f664d-113">This command gets the properties of all disks under the subscription.</span></span>

## <span data-ttu-id="f664d-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f664d-114">PARAMETERS</span></span>

### <span data-ttu-id="f664d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f664d-115">-DefaultProfile</span></span>
<span data-ttu-id="f664d-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f664d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f664d-117">-Diskname</span><span class="sxs-lookup"><span data-stu-id="f664d-117">-DiskName</span></span>
<span data-ttu-id="f664d-118">Specifica il nome di un disco.</span><span class="sxs-lookup"><span data-stu-id="f664d-118">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f664d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f664d-119">-ResourceGroupName</span></span>
<span data-ttu-id="f664d-120">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f664d-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f664d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f664d-121">CommonParameters</span></span>
<span data-ttu-id="f664d-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f664d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f664d-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f664d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f664d-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f664d-124">INPUTS</span></span>

### <span data-ttu-id="f664d-125">System. String</span><span class="sxs-lookup"><span data-stu-id="f664d-125">System.String</span></span>

## <span data-ttu-id="f664d-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f664d-126">OUTPUTS</span></span>

### <span data-ttu-id="f664d-127">System. Object</span><span class="sxs-lookup"><span data-stu-id="f664d-127">System.Object</span></span>

## <span data-ttu-id="f664d-128">Note</span><span class="sxs-lookup"><span data-stu-id="f664d-128">NOTES</span></span>

## <span data-ttu-id="f664d-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f664d-129">RELATED LINKS</span></span>

