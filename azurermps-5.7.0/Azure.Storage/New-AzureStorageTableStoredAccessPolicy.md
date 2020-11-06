---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 163c6ba0841b19edc76421259b1cd9cc8411e35e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515867"
---
# <span data-ttu-id="dd301-101">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="dd301-101">New-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="dd301-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dd301-102">SYNOPSIS</span></span>
<span data-ttu-id="dd301-103">Crea un criterio di accesso archiviato per una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="dd301-103">Creates a stored access policy for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd301-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dd301-104">SYNTAX</span></span>

```
New-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="dd301-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dd301-105">DESCRIPTION</span></span>
<span data-ttu-id="dd301-106">Il cmdlet **New-AzureStorageTableStoredAccessPolicy** crea un criterio di accesso archiviato per una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="dd301-106">The **New-AzureStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="dd301-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dd301-107">EXAMPLES</span></span>

### <span data-ttu-id="dd301-108">Esempio 1: creare criteri di accesso archiviati in una tabella</span><span class="sxs-lookup"><span data-stu-id="dd301-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="dd301-109">Questo comando crea un criterio di accesso denominato Policy02 nella tabella di archiviazione denominata MyTable.</span><span class="sxs-lookup"><span data-stu-id="dd301-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="dd301-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dd301-110">PARAMETERS</span></span>

### <span data-ttu-id="dd301-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="dd301-111">-Context</span></span>
<span data-ttu-id="dd301-112">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="dd301-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="dd301-113">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="dd301-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd301-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="dd301-114">-ExpiryTime</span></span>
<span data-ttu-id="dd301-115">Specifica il momento in cui il criterio di accesso archiviato diventa non valido.</span><span class="sxs-lookup"><span data-stu-id="dd301-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd301-116">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="dd301-116">-Permission</span></span>
<span data-ttu-id="dd301-117">Specifica le autorizzazioni nei criteri di accesso archiviati per accedere alla tabella di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="dd301-117">Specifies permissions in the stored access policy to access the storage table.</span></span>

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

### <span data-ttu-id="dd301-118">-Policy</span><span class="sxs-lookup"><span data-stu-id="dd301-118">-Policy</span></span>
<span data-ttu-id="dd301-119">Specifica un nome per i criteri di accesso archiviati.</span><span class="sxs-lookup"><span data-stu-id="dd301-119">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="dd301-120">-StartTime</span><span class="sxs-lookup"><span data-stu-id="dd301-120">-StartTime</span></span>
<span data-ttu-id="dd301-121">Specifica il momento in cui i criteri di accesso archiviati diventano validi.</span><span class="sxs-lookup"><span data-stu-id="dd301-121">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd301-122">-Tabella</span><span class="sxs-lookup"><span data-stu-id="dd301-122">-Table</span></span>
<span data-ttu-id="dd301-123">Specifica il nome della tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="dd301-123">Specifies the Azure storage table name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd301-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd301-124">CommonParameters</span></span>
<span data-ttu-id="dd301-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd301-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd301-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd301-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd301-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dd301-127">INPUTS</span></span>

### <span data-ttu-id="dd301-128">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="dd301-128">IStorageContext</span></span>

<span data-ttu-id="dd301-129">Il parametro "context" accetta il valore di tipo "IStorageContext" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="dd301-129">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="dd301-130">Stringa</span><span class="sxs-lookup"><span data-stu-id="dd301-130">String</span></span>

<span data-ttu-id="dd301-131">Il parametro "Table" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="dd301-131">Parameter 'Table' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="dd301-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dd301-132">OUTPUTS</span></span>

### <span data-ttu-id="dd301-133">System. String</span><span class="sxs-lookup"><span data-stu-id="dd301-133">System.String</span></span>

## <span data-ttu-id="dd301-134">Note</span><span class="sxs-lookup"><span data-stu-id="dd301-134">NOTES</span></span>

## <span data-ttu-id="dd301-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dd301-135">RELATED LINKS</span></span>

[<span data-ttu-id="dd301-136">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="dd301-136">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="dd301-137">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="dd301-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="dd301-138">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="dd301-138">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="dd301-139">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="dd301-139">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)


