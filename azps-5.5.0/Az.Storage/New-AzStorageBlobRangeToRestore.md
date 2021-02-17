---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobrangetorestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
ms.openlocfilehash: cfbe2cc695ceb2db7c498e8ee2750fa0427da114
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198471"
---
# <span data-ttu-id="a1212-101">New-AzStorageBlobRangeToRestore</span><span class="sxs-lookup"><span data-stu-id="a1212-101">New-AzStorageBlobRangeToRestore</span></span>

## <span data-ttu-id="a1212-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1212-102">SYNOPSIS</span></span>
<span data-ttu-id="a1212-103">Crea un oggetto Intervallo BLOB per ripristinare un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a1212-103">Creates a Blob Range object to restores a Storage account.</span></span>

## <span data-ttu-id="a1212-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a1212-104">SYNTAX</span></span>

```
New-AzStorageBlobRangeToRestore [-StartRange <String>] [-EndRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1212-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a1212-105">DESCRIPTION</span></span>
<span data-ttu-id="a1212-106">Il cmdlet **New-AzStorageBlobRangeToRestore** crea un oggetto intervallo BLOB, che può essere usato in Restore-AzStorageBlobRange.</span><span class="sxs-lookup"><span data-stu-id="a1212-106">The **New-AzStorageBlobRangeToRestore** cmdlet creates a Blob range object, which can be used in Restore-AzStorageBlobRange.</span></span>

## <span data-ttu-id="a1212-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a1212-107">EXAMPLES</span></span>

### <span data-ttu-id="a1212-108">Esempio 1: Crea un intervallo BLOB da ripristinare</span><span class="sxs-lookup"><span data-stu-id="a1212-108">Example 1: Creates a blob range to restore</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
```

<span data-ttu-id="a1212-109">Questo comando crea un intervallo BLOB da ripristinare, che inizia in container1/BLOB1 (include) e termina con container2/BLOB2 (exclude).</span><span class="sxs-lookup"><span data-stu-id="a1212-109">This command creates a blob range to restore, which starts at container1/blob1 (include), and ends at container2/blob2 (exclude).</span></span>

### <span data-ttu-id="a1212-110">Esempio 2: Crea un intervallo BLOB che ripristina dal primo BLOB in ordine alfabetico a un BLOB specifico (escluso)</span><span class="sxs-lookup"><span data-stu-id="a1212-110">Example 2: Creates a blob range which will restore from first blob in alphabetical order, to a specific blob (exclude)</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange container2/blob2
```

<span data-ttu-id="a1212-111">Questo comando crea un intervallo BLOB che ripristina dal primo BLOB in ordine alfabetico a uno specifico contenitore BLOB2/BLOB2 (escluso)</span><span class="sxs-lookup"><span data-stu-id="a1212-111">This command creates a blob range which will restore from first blob of alphabetical order, to a specific blob container2/blob2 (exclude)</span></span>

### <span data-ttu-id="a1212-112">Esempio 3: Crea un intervallo BLOB che ripristina da un BLOB specifico (include) all'ultimo BLOB in ordine alfabetico</span><span class="sxs-lookup"><span data-stu-id="a1212-112">Example 3: Creates a blob range which will restore from a specific blob (include), to the last blob in alphabetical order</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange ""
```

<span data-ttu-id="a1212-113">Questo comando crea un intervallo BLOB che ripristina da uno specifico contenitore BLOB1/BLOB1 (include) all'ultimo BLOB in ordine alfabetico.</span><span class="sxs-lookup"><span data-stu-id="a1212-113">This command creates a blob range which will restore from a specific blob container1/blob1 (include), to the last blob in alphabetical order.</span></span>

### <span data-ttu-id="a1212-114">Esempio 4: Crea un intervallo BLOB che ripristina tutti i BLOB</span><span class="sxs-lookup"><span data-stu-id="a1212-114">Example 4: Creates a blob range which will restore all blobs</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange ""
```

<span data-ttu-id="a1212-115">Questo comando crea un intervallo BLOB che ripristina tutti i BLOB.</span><span class="sxs-lookup"><span data-stu-id="a1212-115">This command creates a blob range which will restore all blobs.</span></span>

## <span data-ttu-id="a1212-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1212-116">PARAMETERS</span></span>

### <span data-ttu-id="a1212-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1212-117">-DefaultProfile</span></span>
<span data-ttu-id="a1212-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a1212-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1212-119">-EndRange</span><span class="sxs-lookup"><span data-stu-id="a1212-119">-EndRange</span></span>
<span data-ttu-id="a1212-120">Specificare l'intervallo finale del ripristino BLOB.</span><span class="sxs-lookup"><span data-stu-id="a1212-120">Specify the blob restore End range.</span></span>
<span data-ttu-id="a1212-121">L'intervallo finale verrà escluso nei BLOB di ripristino.</span><span class="sxs-lookup"><span data-stu-id="a1212-121">End range will be excluded in restore blobs.</span></span>
<span data-ttu-id="a1212-122">Impostarlo come strng vuoto per ripristinare l'impostazione finale.</span><span class="sxs-lookup"><span data-stu-id="a1212-122">Set it as empty strng to restore to the end.</span></span>

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

### <span data-ttu-id="a1212-123">-StartRange</span><span class="sxs-lookup"><span data-stu-id="a1212-123">-StartRange</span></span>
<span data-ttu-id="a1212-124">Specificare l'intervallo iniziale di ripristino BLOB.</span><span class="sxs-lookup"><span data-stu-id="a1212-124">Specify the blob restore start range.</span></span>
<span data-ttu-id="a1212-125">L'intervallo iniziale verrà incluso nei BLOB di ripristino.</span><span class="sxs-lookup"><span data-stu-id="a1212-125">Start range will be included in restore blobs.</span></span>
<span data-ttu-id="a1212-126">Impostarla come stringa vuota per ripristinarla dall'inizio.</span><span class="sxs-lookup"><span data-stu-id="a1212-126">Set it as empty string to restore from begining.</span></span>

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

### <span data-ttu-id="a1212-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1212-127">CommonParameters</span></span>
<span data-ttu-id="a1212-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1212-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1212-129">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1212-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1212-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="a1212-130">INPUTS</span></span>

### <span data-ttu-id="a1212-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a1212-131">None</span></span>

## <span data-ttu-id="a1212-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a1212-132">OUTPUTS</span></span>

### <span data-ttu-id="a1212-133">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange</span><span class="sxs-lookup"><span data-stu-id="a1212-133">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange</span></span>

## <span data-ttu-id="a1212-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="a1212-134">NOTES</span></span>

## <span data-ttu-id="a1212-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a1212-135">RELATED LINKS</span></span>
