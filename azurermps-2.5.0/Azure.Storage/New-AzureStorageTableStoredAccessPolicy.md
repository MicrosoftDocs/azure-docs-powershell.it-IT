---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragetablestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 21e289ce0a8e7ca2d430d64ab9cc75bfd0c1a3ad
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866936"
---
# <span data-ttu-id="d0ea4-101">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d0ea4-101">New-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="d0ea4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d0ea4-102">SYNOPSIS</span></span>
<span data-ttu-id="d0ea4-103">Crea un criterio di accesso archiviato per una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d0ea4-103">Creates a stored access policy for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0ea4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d0ea4-104">SYNTAX</span></span>

```
New-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0ea4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d0ea4-105">DESCRIPTION</span></span>
<span data-ttu-id="d0ea4-106">Il cmdlet **New-AzureStorageTableStoredAccessPolicy** crea un criterio di accesso archiviato per una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d0ea4-106">The **New-AzureStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="d0ea4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d0ea4-107">EXAMPLES</span></span>

### <span data-ttu-id="d0ea4-108">Esempio 1: creare criteri di accesso archiviati in una tabella</span><span class="sxs-lookup"><span data-stu-id="d0ea4-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="d0ea4-109">Questo comando crea un criterio di accesso denominato Policy02 nella tabella di archiviazione denominata MyTable.</span><span class="sxs-lookup"><span data-stu-id="d0ea4-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="d0ea4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d0ea4-110">PARAMETERS</span></span>

### <span data-ttu-id="d0ea4-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="d0ea4-111">-Context</span></span>
<span data-ttu-id="d0ea4-112">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d0ea4-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="d0ea4-113">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="d0ea4-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d0ea4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0ea4-114">-DefaultProfile</span></span>
<span data-ttu-id="d0ea4-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d0ea4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0ea4-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="d0ea4-116">-ExpiryTime</span></span>
<span data-ttu-id="d0ea4-117">Specifica il momento in cui il criterio di accesso archiviato diventa non valido.</span><span class="sxs-lookup"><span data-stu-id="d0ea4-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="d0ea4-118">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="d0ea4-118">-Permission</span></span>
<span data-ttu-id="d0ea4-119">Specifica le autorizzazioni nei criteri di accesso archiviati per accedere alla tabella di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d0ea4-119">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="d0ea4-120">È importante notare che si tratta di una stringa, ad esempio `rwd` (per lettura, scrittura ed eliminazione).</span><span class="sxs-lookup"><span data-stu-id="d0ea4-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="d0ea4-121">-Policy</span><span class="sxs-lookup"><span data-stu-id="d0ea4-121">-Policy</span></span>
<span data-ttu-id="d0ea4-122">Specifica un nome per i criteri di accesso archiviati.</span><span class="sxs-lookup"><span data-stu-id="d0ea4-122">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="d0ea4-123">-StartTime</span><span class="sxs-lookup"><span data-stu-id="d0ea4-123">-StartTime</span></span>
<span data-ttu-id="d0ea4-124">Specifica il momento in cui i criteri di accesso archiviati diventano validi.</span><span class="sxs-lookup"><span data-stu-id="d0ea4-124">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="d0ea4-125">-Tabella</span><span class="sxs-lookup"><span data-stu-id="d0ea4-125">-Table</span></span>
<span data-ttu-id="d0ea4-126">Specifica il nome della tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d0ea4-126">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="d0ea4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0ea4-127">CommonParameters</span></span>
<span data-ttu-id="d0ea4-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0ea4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0ea4-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0ea4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0ea4-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d0ea4-130">INPUTS</span></span>

### <span data-ttu-id="d0ea4-131">System. String</span><span class="sxs-lookup"><span data-stu-id="d0ea4-131">System.String</span></span>

### <span data-ttu-id="d0ea4-132">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d0ea4-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d0ea4-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d0ea4-133">OUTPUTS</span></span>

### <span data-ttu-id="d0ea4-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d0ea4-134">System.String</span></span>

## <span data-ttu-id="d0ea4-135">Note</span><span class="sxs-lookup"><span data-stu-id="d0ea4-135">NOTES</span></span>

## <span data-ttu-id="d0ea4-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d0ea4-136">RELATED LINKS</span></span>

[<span data-ttu-id="d0ea4-137">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d0ea4-137">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="d0ea4-138">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="d0ea4-138">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="d0ea4-139">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d0ea4-139">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="d0ea4-140">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d0ea4-140">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)


