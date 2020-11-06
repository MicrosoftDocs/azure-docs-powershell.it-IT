---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 54b28caaf39bd3d4750e341da4f4564d60b59138
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490790"
---
# <span data-ttu-id="21ea7-101">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="21ea7-101">New-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="21ea7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="21ea7-102">SYNOPSIS</span></span>
<span data-ttu-id="21ea7-103">Crea un criterio di accesso archiviato per una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="21ea7-103">Creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="21ea7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="21ea7-104">SYNTAX</span></span>

```
New-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="21ea7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="21ea7-105">DESCRIPTION</span></span>
<span data-ttu-id="21ea7-106">Il cmdlet **New-AzureStorageTableStoredAccessPolicy** crea un criterio di accesso archiviato per una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="21ea7-106">The **New-AzureStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="21ea7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="21ea7-107">EXAMPLES</span></span>

### <span data-ttu-id="21ea7-108">Esempio 1: creare criteri di accesso archiviati in una tabella</span><span class="sxs-lookup"><span data-stu-id="21ea7-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="21ea7-109">Questo comando crea un criterio di accesso denominato Policy02 nella tabella di archiviazione denominata MyTable.</span><span class="sxs-lookup"><span data-stu-id="21ea7-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="21ea7-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="21ea7-110">PARAMETERS</span></span>

### <span data-ttu-id="21ea7-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="21ea7-111">-Context</span></span>
<span data-ttu-id="21ea7-112">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="21ea7-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="21ea7-113">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="21ea7-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="21ea7-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="21ea7-114">-ExpiryTime</span></span>
<span data-ttu-id="21ea7-115">Specifica il momento in cui il criterio di accesso archiviato diventa non valido.</span><span class="sxs-lookup"><span data-stu-id="21ea7-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="21ea7-116">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="21ea7-116">-Permission</span></span>
<span data-ttu-id="21ea7-117">Specifica il livello di accesso pubblico alla tabella di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="21ea7-117">Specifies the level of public access to this storage table.</span></span>

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

### <span data-ttu-id="21ea7-118">-Policy</span><span class="sxs-lookup"><span data-stu-id="21ea7-118">-Policy</span></span>
<span data-ttu-id="21ea7-119">Specifica un criterio di accesso archiviato, che include le autorizzazioni per il token SAS (Shared Access Signature).</span><span class="sxs-lookup"><span data-stu-id="21ea7-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="21ea7-120">-StartTime</span><span class="sxs-lookup"><span data-stu-id="21ea7-120">-StartTime</span></span>
<span data-ttu-id="21ea7-121">Specifica il momento in cui i criteri di accesso archiviati diventano validi.</span><span class="sxs-lookup"><span data-stu-id="21ea7-121">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="21ea7-122">-Tabella</span><span class="sxs-lookup"><span data-stu-id="21ea7-122">-Table</span></span>
<span data-ttu-id="21ea7-123">Specifica il nome della tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="21ea7-123">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="21ea7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21ea7-124">CommonParameters</span></span>
<span data-ttu-id="21ea7-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21ea7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21ea7-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21ea7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21ea7-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="21ea7-127">INPUTS</span></span>

## <span data-ttu-id="21ea7-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="21ea7-128">OUTPUTS</span></span>

## <span data-ttu-id="21ea7-129">Note</span><span class="sxs-lookup"><span data-stu-id="21ea7-129">NOTES</span></span>

## <span data-ttu-id="21ea7-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="21ea7-130">RELATED LINKS</span></span>

[<span data-ttu-id="21ea7-131">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="21ea7-131">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="21ea7-132">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="21ea7-132">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="21ea7-133">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="21ea7-133">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="21ea7-134">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="21ea7-134">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)


