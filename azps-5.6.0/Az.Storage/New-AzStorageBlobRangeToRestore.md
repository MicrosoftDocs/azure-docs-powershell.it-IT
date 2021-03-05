---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageblobrangetorestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
ms.openlocfilehash: 0f74ad9b146a0c5d2f2c65b7109fb57f56902834
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002590"
---
# <span data-ttu-id="0ac57-101">New-AzStorageBlobRangeToRestore</span><span class="sxs-lookup"><span data-stu-id="0ac57-101">New-AzStorageBlobRangeToRestore</span></span>

## <span data-ttu-id="0ac57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ac57-102">SYNOPSIS</span></span>
<span data-ttu-id="0ac57-103">Crea un oggetto Intervallo BLOB per ripristinare un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="0ac57-103">Creates a Blob Range object to restores a Storage account.</span></span>

## <span data-ttu-id="0ac57-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0ac57-104">SYNTAX</span></span>

```
New-AzStorageBlobRangeToRestore [-StartRange <String>] [-EndRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ac57-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0ac57-105">DESCRIPTION</span></span>
<span data-ttu-id="0ac57-106">Il cmdlet **New-AzStorageBlobRangeToRestore** crea un oggetto intervallo BLOB, che può essere usato in Restore-AzStorageBlobRange.</span><span class="sxs-lookup"><span data-stu-id="0ac57-106">The **New-AzStorageBlobRangeToRestore** cmdlet creates a Blob range object, which can be used in Restore-AzStorageBlobRange.</span></span>

## <span data-ttu-id="0ac57-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0ac57-107">EXAMPLES</span></span>

### <span data-ttu-id="0ac57-108">Esempio 1: Crea un intervallo BLOB da ripristinare</span><span class="sxs-lookup"><span data-stu-id="0ac57-108">Example 1: Creates a blob range to restore</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
```

<span data-ttu-id="0ac57-109">Questo comando crea un intervallo BLOB da ripristinare, che inizia in container1/BLOB1 (include) e termina con container2/BLOB2 (exclude).</span><span class="sxs-lookup"><span data-stu-id="0ac57-109">This command creates a blob range to restore, which starts at container1/blob1 (include), and ends at container2/blob2 (exclude).</span></span>

### <span data-ttu-id="0ac57-110">Esempio 2: Crea un intervallo BLOB che ripristina dal primo BLOB in ordine alfabetico, a un BLOB specifico (escluso)</span><span class="sxs-lookup"><span data-stu-id="0ac57-110">Example 2: Creates a blob range which will restore from first blob in alphabetical order, to a specific blob (exclude)</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange container2/blob2
```

<span data-ttu-id="0ac57-111">Questo comando crea un intervallo BLOB che ripristina dal primo BLOB in ordine alfabetico a uno specifico BLOB container2/BLOB2 (exclude)</span><span class="sxs-lookup"><span data-stu-id="0ac57-111">This command creates a blob range which will restore from first blob of alphabetical order, to a specific blob container2/blob2 (exclude)</span></span>

### <span data-ttu-id="0ac57-112">Esempio 3: Crea un intervallo BLOB che ripristina da un BLOB specifico (include) all'ultimo BLOB in ordine alfabetico</span><span class="sxs-lookup"><span data-stu-id="0ac57-112">Example 3: Creates a blob range which will restore from a specific blob (include), to the last blob in alphabetical order</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange ""
```

<span data-ttu-id="0ac57-113">Questo comando crea un intervallo BLOB che ripristina da uno specifico contenitore BLOB1/BLOB1 (include) all'ultimo BLOB in ordine alfabetico.</span><span class="sxs-lookup"><span data-stu-id="0ac57-113">This command creates a blob range which will restore from a specific blob container1/blob1 (include), to the last blob in alphabetical order.</span></span>

### <span data-ttu-id="0ac57-114">Esempio 4: Crea un intervallo BLOB che ripristina tutti i BLOB</span><span class="sxs-lookup"><span data-stu-id="0ac57-114">Example 4: Creates a blob range which will restore all blobs</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange ""
```

<span data-ttu-id="0ac57-115">Questo comando crea un intervallo BLOB che ripristina tutti i BLOB.</span><span class="sxs-lookup"><span data-stu-id="0ac57-115">This command creates a blob range which will restore all blobs.</span></span>

## <span data-ttu-id="0ac57-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ac57-116">PARAMETERS</span></span>

### <span data-ttu-id="0ac57-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ac57-117">-DefaultProfile</span></span>
<span data-ttu-id="0ac57-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0ac57-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ac57-119">-EndRange</span><span class="sxs-lookup"><span data-stu-id="0ac57-119">-EndRange</span></span>
<span data-ttu-id="0ac57-120">Specificare l'intervallo finale del ripristino BLOB.</span><span class="sxs-lookup"><span data-stu-id="0ac57-120">Specify the blob restore End range.</span></span>
<span data-ttu-id="0ac57-121">L'intervallo finale verrà escluso nei BLOB di ripristino.</span><span class="sxs-lookup"><span data-stu-id="0ac57-121">End range will be excluded in restore blobs.</span></span>
<span data-ttu-id="0ac57-122">Impostarlo come strng vuoto per ripristinare l'impostazione finale.</span><span class="sxs-lookup"><span data-stu-id="0ac57-122">Set it as empty strng to restore to the end.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ac57-123">-StartRange</span><span class="sxs-lookup"><span data-stu-id="0ac57-123">-StartRange</span></span>
<span data-ttu-id="0ac57-124">Specificare l'intervallo iniziale di ripristino BLOB.</span><span class="sxs-lookup"><span data-stu-id="0ac57-124">Specify the blob restore start range.</span></span>
<span data-ttu-id="0ac57-125">L'intervallo iniziale verrà incluso nei BLOB di ripristino.</span><span class="sxs-lookup"><span data-stu-id="0ac57-125">Start range will be included in restore blobs.</span></span>
<span data-ttu-id="0ac57-126">Impostarla come stringa vuota per ripristinarla dall'inizio.</span><span class="sxs-lookup"><span data-stu-id="0ac57-126">Set it as empty string to restore from begining.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ac57-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ac57-127">CommonParameters</span></span>
<span data-ttu-id="0ac57-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ac57-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ac57-129">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ac57-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ac57-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="0ac57-130">INPUTS</span></span>

### <span data-ttu-id="0ac57-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0ac57-131">None</span></span>

## <span data-ttu-id="0ac57-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0ac57-132">OUTPUTS</span></span>

### <span data-ttu-id="0ac57-133">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange</span><span class="sxs-lookup"><span data-stu-id="0ac57-133">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange</span></span>

## <span data-ttu-id="0ac57-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="0ac57-134">NOTES</span></span>

## <span data-ttu-id="0ac57-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0ac57-135">RELATED LINKS</span></span>
