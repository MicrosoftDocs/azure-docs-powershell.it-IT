---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzDisk.md
ms.openlocfilehash: 1da5ac8a6952e2a03367e84894f2069ba7ff250f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863814"
---
# <span data-ttu-id="79af0-101">Get-AzDisk</span><span class="sxs-lookup"><span data-stu-id="79af0-101">Get-AzDisk</span></span>

## <span data-ttu-id="79af0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="79af0-102">SYNOPSIS</span></span>
<span data-ttu-id="79af0-103">Ottiene le proprietà di un disco gestito.</span><span class="sxs-lookup"><span data-stu-id="79af0-103">Gets the properties of a Managed disk.</span></span>

## <span data-ttu-id="79af0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="79af0-104">SYNTAX</span></span>

```
Get-AzDisk [[-ResourceGroupName] <String>] [[-DiskName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79af0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="79af0-105">DESCRIPTION</span></span>
<span data-ttu-id="79af0-106">Il cmdlet **Get-AzDisk** ottiene le proprietà di un disco gestito.</span><span class="sxs-lookup"><span data-stu-id="79af0-106">The **Get-AzDisk** cmdlet gets the properties of a Managed disk.</span></span>

## <span data-ttu-id="79af0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="79af0-107">EXAMPLES</span></span>

### <span data-ttu-id="79af0-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="79af0-108">Example 1</span></span>
```
PS C:\> Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="79af0-109">Questo comando consente di ottenere le proprietà del disco denominato "Disk01" nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="79af0-109">This command gets the properties of the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="79af0-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="79af0-110">Example 2</span></span>
```
PS C:\> Get-AzDisk -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="79af0-111">Questo comando consente di ottenere le proprietà di tutti i dischi nel gruppo di risorse "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="79af0-111">This command gets the properties of all disks in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="79af0-112">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="79af0-112">Example 3</span></span>
```
PS C:\> Get-AzDisk
```

<span data-ttu-id="79af0-113">Questo comando consente di ottenere le proprietà di tutti i dischi sotto l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="79af0-113">This command gets the properties of all disks under the subscription.</span></span>

## <span data-ttu-id="79af0-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="79af0-114">PARAMETERS</span></span>

### <span data-ttu-id="79af0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79af0-115">-DefaultProfile</span></span>
<span data-ttu-id="79af0-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="79af0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79af0-117">-Diskname</span><span class="sxs-lookup"><span data-stu-id="79af0-117">-DiskName</span></span>
<span data-ttu-id="79af0-118">Specifica il nome di un disco.</span><span class="sxs-lookup"><span data-stu-id="79af0-118">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="79af0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79af0-119">-ResourceGroupName</span></span>
<span data-ttu-id="79af0-120">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="79af0-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="79af0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79af0-121">CommonParameters</span></span>
<span data-ttu-id="79af0-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79af0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79af0-123">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79af0-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79af0-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="79af0-124">INPUTS</span></span>

### <span data-ttu-id="79af0-125">System. String</span><span class="sxs-lookup"><span data-stu-id="79af0-125">System.String</span></span>

## <span data-ttu-id="79af0-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="79af0-126">OUTPUTS</span></span>

### <span data-ttu-id="79af0-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="79af0-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="79af0-128">Note</span><span class="sxs-lookup"><span data-stu-id="79af0-128">NOTES</span></span>

## <span data-ttu-id="79af0-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="79af0-129">RELATED LINKS</span></span>

