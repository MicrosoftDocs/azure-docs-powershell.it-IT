---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobrangetorestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
ms.openlocfilehash: cfbe2cc695ceb2db7c498e8ee2750fa0427da114
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324808"
---
# <span data-ttu-id="51f0f-101">New-AzStorageBlobRangeToRestore</span><span class="sxs-lookup"><span data-stu-id="51f0f-101">New-AzStorageBlobRangeToRestore</span></span>

## <span data-ttu-id="51f0f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="51f0f-102">SYNOPSIS</span></span>
<span data-ttu-id="51f0f-103">Crea un oggetto Range BLOB per ripristinare un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="51f0f-103">Creates a Blob Range object to restores a Storage account.</span></span>

## <span data-ttu-id="51f0f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="51f0f-104">SYNTAX</span></span>

```
New-AzStorageBlobRangeToRestore [-StartRange <String>] [-EndRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51f0f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="51f0f-105">DESCRIPTION</span></span>
<span data-ttu-id="51f0f-106">Il cmdlet **New-AzStorageBlobRangeToRestore** crea un oggetto Range BLOB, che può essere usato in Restore-AzStorageBlobRange.</span><span class="sxs-lookup"><span data-stu-id="51f0f-106">The **New-AzStorageBlobRangeToRestore** cmdlet creates a Blob range object, which can be used in Restore-AzStorageBlobRange.</span></span>

## <span data-ttu-id="51f0f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="51f0f-107">EXAMPLES</span></span>

### <span data-ttu-id="51f0f-108">Esempio 1: crea un intervallo di BLOB da ripristinare</span><span class="sxs-lookup"><span data-stu-id="51f0f-108">Example 1: Creates a blob range to restore</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
```

<span data-ttu-id="51f0f-109">Questo comando crea un intervallo di BLOB da ripristinare, che inizia in container1/blob1 (include), e termina in container2/blob2 (Escludi).</span><span class="sxs-lookup"><span data-stu-id="51f0f-109">This command creates a blob range to restore, which starts at container1/blob1 (include), and ends at container2/blob2 (exclude).</span></span>

### <span data-ttu-id="51f0f-110">Esempio 2: crea un intervallo di BLOB che verrà ripristinato dal primo BLOB in ordine alfabetico a un blob specifico (Escludi)</span><span class="sxs-lookup"><span data-stu-id="51f0f-110">Example 2: Creates a blob range which will restore from first blob in alphabetical order, to a specific blob (exclude)</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange container2/blob2
```

<span data-ttu-id="51f0f-111">Questo comando crea un intervallo di BLOB che ripristinerà dal primo BLOB di ordine alfabetico a un blob specifico container2/blob2 (Escludi)</span><span class="sxs-lookup"><span data-stu-id="51f0f-111">This command creates a blob range which will restore from first blob of alphabetical order, to a specific blob container2/blob2 (exclude)</span></span>

### <span data-ttu-id="51f0f-112">Esempio 3: crea un intervallo di BLOB che verrà ripristinato da un blob specifico (include), all'ultimo BLOB in ordine alfabetico</span><span class="sxs-lookup"><span data-stu-id="51f0f-112">Example 3: Creates a blob range which will restore from a specific blob (include), to the last blob in alphabetical order</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange ""
```

<span data-ttu-id="51f0f-113">Questo comando crea un intervallo di BLOB che verrà ripristinato da un blob specifico container1/blob1 (include), all'ultimo BLOB in ordine alfabetico.</span><span class="sxs-lookup"><span data-stu-id="51f0f-113">This command creates a blob range which will restore from a specific blob container1/blob1 (include), to the last blob in alphabetical order.</span></span>

### <span data-ttu-id="51f0f-114">Esempio 4: crea un intervallo di BLOB che ripristinerà tutti i BLOB</span><span class="sxs-lookup"><span data-stu-id="51f0f-114">Example 4: Creates a blob range which will restore all blobs</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange ""
```

<span data-ttu-id="51f0f-115">Questo comando crea un intervallo di BLOB che ripristinerà tutti i BLOB.</span><span class="sxs-lookup"><span data-stu-id="51f0f-115">This command creates a blob range which will restore all blobs.</span></span>

## <span data-ttu-id="51f0f-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="51f0f-116">PARAMETERS</span></span>

### <span data-ttu-id="51f0f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51f0f-117">-DefaultProfile</span></span>
<span data-ttu-id="51f0f-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="51f0f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51f0f-119">-EndRange</span><span class="sxs-lookup"><span data-stu-id="51f0f-119">-EndRange</span></span>
<span data-ttu-id="51f0f-120">Specificare l'intervallo di fine ripristino BLOB.</span><span class="sxs-lookup"><span data-stu-id="51f0f-120">Specify the blob restore End range.</span></span>
<span data-ttu-id="51f0f-121">L'intervallo di fine verrà escluso in ripristini BLOB.</span><span class="sxs-lookup"><span data-stu-id="51f0f-121">End range will be excluded in restore blobs.</span></span>
<span data-ttu-id="51f0f-122">Impostarlo come strng vuoto da ripristinare alla fine.</span><span class="sxs-lookup"><span data-stu-id="51f0f-122">Set it as empty strng to restore to the end.</span></span>

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

### <span data-ttu-id="51f0f-123">-StartRange</span><span class="sxs-lookup"><span data-stu-id="51f0f-123">-StartRange</span></span>
<span data-ttu-id="51f0f-124">Specificare l'intervallo di inizio ripristino BLOB.</span><span class="sxs-lookup"><span data-stu-id="51f0f-124">Specify the blob restore start range.</span></span>
<span data-ttu-id="51f0f-125">L'intervallo di inizio verrà incluso nei BLOB di ripristino.</span><span class="sxs-lookup"><span data-stu-id="51f0f-125">Start range will be included in restore blobs.</span></span>
<span data-ttu-id="51f0f-126">Impostarla come stringa vuota per il ripristino dall'inizio.</span><span class="sxs-lookup"><span data-stu-id="51f0f-126">Set it as empty string to restore from begining.</span></span>

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

### <span data-ttu-id="51f0f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51f0f-127">CommonParameters</span></span>
<span data-ttu-id="51f0f-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51f0f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51f0f-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51f0f-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51f0f-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="51f0f-130">INPUTS</span></span>

### <span data-ttu-id="51f0f-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="51f0f-131">None</span></span>

## <span data-ttu-id="51f0f-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="51f0f-132">OUTPUTS</span></span>

### <span data-ttu-id="51f0f-133">Microsoft. Azure. Commands. Management. storage. Models. PSBlobRestoreRange</span><span class="sxs-lookup"><span data-stu-id="51f0f-133">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange</span></span>

## <span data-ttu-id="51f0f-134">Note</span><span class="sxs-lookup"><span data-stu-id="51f0f-134">NOTES</span></span>

## <span data-ttu-id="51f0f-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="51f0f-135">RELATED LINKS</span></span>
