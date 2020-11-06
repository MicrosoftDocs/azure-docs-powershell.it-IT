---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: b87dd24c78b835e16ab1c4e8e9c0c3bb265d4feb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93522013"
---
# <span data-ttu-id="2b9f3-101">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2b9f3-101">New-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="2b9f3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2b9f3-102">SYNOPSIS</span></span>
<span data-ttu-id="2b9f3-103">Crea un criterio di accesso archiviato per una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="2b9f3-103">Creates a stored access policy for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b9f3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2b9f3-104">SYNTAX</span></span>

```
New-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="2b9f3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b9f3-105">DESCRIPTION</span></span>
<span data-ttu-id="2b9f3-106">Il cmdlet **New-AzureStorageTableStoredAccessPolicy** crea un criterio di accesso archiviato per una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="2b9f3-106">The **New-AzureStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="2b9f3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2b9f3-107">EXAMPLES</span></span>

### <span data-ttu-id="2b9f3-108">Esempio 1: creare criteri di accesso archiviati in una tabella</span><span class="sxs-lookup"><span data-stu-id="2b9f3-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="2b9f3-109">Questo comando crea un criterio di accesso denominato Policy02 nella tabella di archiviazione denominata MyTable.</span><span class="sxs-lookup"><span data-stu-id="2b9f3-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="2b9f3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2b9f3-110">PARAMETERS</span></span>

### <span data-ttu-id="2b9f3-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="2b9f3-111">-Context</span></span>
<span data-ttu-id="2b9f3-112">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="2b9f3-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="2b9f3-113">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="2b9f3-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="2b9f3-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="2b9f3-114">-ExpiryTime</span></span>
<span data-ttu-id="2b9f3-115">Specifica il momento in cui il criterio di accesso archiviato diventa non valido.</span><span class="sxs-lookup"><span data-stu-id="2b9f3-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="2b9f3-116">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="2b9f3-116">-Permission</span></span>
<span data-ttu-id="2b9f3-117">Specifica le autorizzazioni nei criteri di accesso archiviati per accedere alla tabella di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2b9f3-117">Specifies permissions in the stored access policy to access the storage table.</span></span>

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

### <span data-ttu-id="2b9f3-118">-Policy</span><span class="sxs-lookup"><span data-stu-id="2b9f3-118">-Policy</span></span>
<span data-ttu-id="2b9f3-119">Specifica un nome per i criteri di accesso archiviati.</span><span class="sxs-lookup"><span data-stu-id="2b9f3-119">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="2b9f3-120">-StartTime</span><span class="sxs-lookup"><span data-stu-id="2b9f3-120">-StartTime</span></span>
<span data-ttu-id="2b9f3-121">Specifica il momento in cui i criteri di accesso archiviati diventano validi.</span><span class="sxs-lookup"><span data-stu-id="2b9f3-121">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="2b9f3-122">-Tabella</span><span class="sxs-lookup"><span data-stu-id="2b9f3-122">-Table</span></span>
<span data-ttu-id="2b9f3-123">Specifica il nome della tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="2b9f3-123">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="2b9f3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b9f3-124">CommonParameters</span></span>
<span data-ttu-id="2b9f3-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b9f3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b9f3-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b9f3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b9f3-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2b9f3-127">INPUTS</span></span>

### <span data-ttu-id="2b9f3-128">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2b9f3-128">IStorageContext</span></span>

<span data-ttu-id="2b9f3-129">Il parametro "context" accetta il valore di tipo "IStorageContext" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="2b9f3-129">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="2b9f3-130">Stringa</span><span class="sxs-lookup"><span data-stu-id="2b9f3-130">String</span></span>

<span data-ttu-id="2b9f3-131">Il parametro "Table" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="2b9f3-131">Parameter 'Table' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="2b9f3-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2b9f3-132">OUTPUTS</span></span>

### <span data-ttu-id="2b9f3-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2b9f3-133">System.String</span></span>

## <span data-ttu-id="2b9f3-134">Note</span><span class="sxs-lookup"><span data-stu-id="2b9f3-134">NOTES</span></span>

## <span data-ttu-id="2b9f3-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2b9f3-135">RELATED LINKS</span></span>

[<span data-ttu-id="2b9f3-136">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2b9f3-136">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="2b9f3-137">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="2b9f3-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="2b9f3-138">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2b9f3-138">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="2b9f3-139">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2b9f3-139">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)


