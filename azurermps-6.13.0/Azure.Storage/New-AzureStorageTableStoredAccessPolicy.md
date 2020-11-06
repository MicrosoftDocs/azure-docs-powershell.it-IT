---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 5a2890f052e57c37ca86197b2fd3841ba3b5c388
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520310"
---
# <span data-ttu-id="ce564-101">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ce564-101">New-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="ce564-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ce564-102">SYNOPSIS</span></span>
<span data-ttu-id="ce564-103">Crea un criterio di accesso archiviato per una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="ce564-103">Creates a stored access policy for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce564-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ce564-104">SYNTAX</span></span>

```
New-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce564-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ce564-105">DESCRIPTION</span></span>
<span data-ttu-id="ce564-106">Il cmdlet **New-AzureStorageTableStoredAccessPolicy** crea un criterio di accesso archiviato per una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="ce564-106">The **New-AzureStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="ce564-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ce564-107">EXAMPLES</span></span>

### <span data-ttu-id="ce564-108">Esempio 1: creare criteri di accesso archiviati in una tabella</span><span class="sxs-lookup"><span data-stu-id="ce564-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="ce564-109">Questo comando crea un criterio di accesso denominato Policy02 nella tabella di archiviazione denominata MyTable.</span><span class="sxs-lookup"><span data-stu-id="ce564-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="ce564-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ce564-110">PARAMETERS</span></span>

### <span data-ttu-id="ce564-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="ce564-111">-Context</span></span>
<span data-ttu-id="ce564-112">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="ce564-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ce564-113">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="ce564-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce564-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce564-114">-DefaultProfile</span></span>
<span data-ttu-id="ce564-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ce564-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce564-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="ce564-116">-ExpiryTime</span></span>
<span data-ttu-id="ce564-117">Specifica il momento in cui il criterio di accesso archiviato diventa non valido.</span><span class="sxs-lookup"><span data-stu-id="ce564-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce564-118">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="ce564-118">-Permission</span></span>
<span data-ttu-id="ce564-119">Specifica le autorizzazioni nei criteri di accesso archiviati per accedere alla tabella di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ce564-119">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="ce564-120">È importante notare che si tratta di una stringa, ad esempio `rwd` (per lettura, scrittura ed eliminazione).</span><span class="sxs-lookup"><span data-stu-id="ce564-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="ce564-121">-Policy</span><span class="sxs-lookup"><span data-stu-id="ce564-121">-Policy</span></span>
<span data-ttu-id="ce564-122">Specifica un nome per i criteri di accesso archiviati.</span><span class="sxs-lookup"><span data-stu-id="ce564-122">Specifies a name for the stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce564-123">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ce564-123">-StartTime</span></span>
<span data-ttu-id="ce564-124">Specifica il momento in cui i criteri di accesso archiviati diventano validi.</span><span class="sxs-lookup"><span data-stu-id="ce564-124">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce564-125">-Tabella</span><span class="sxs-lookup"><span data-stu-id="ce564-125">-Table</span></span>
<span data-ttu-id="ce564-126">Specifica il nome della tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="ce564-126">Specifies the Azure storage table name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce564-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce564-127">CommonParameters</span></span>
<span data-ttu-id="ce564-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce564-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce564-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce564-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce564-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ce564-130">INPUTS</span></span>

### <span data-ttu-id="ce564-131">System. String</span><span class="sxs-lookup"><span data-stu-id="ce564-131">System.String</span></span>

### <span data-ttu-id="ce564-132">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ce564-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ce564-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ce564-133">OUTPUTS</span></span>

### <span data-ttu-id="ce564-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ce564-134">System.String</span></span>

## <span data-ttu-id="ce564-135">Note</span><span class="sxs-lookup"><span data-stu-id="ce564-135">NOTES</span></span>

## <span data-ttu-id="ce564-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ce564-136">RELATED LINKS</span></span>

[<span data-ttu-id="ce564-137">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ce564-137">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="ce564-138">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="ce564-138">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="ce564-139">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ce564-139">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="ce564-140">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ce564-140">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)


