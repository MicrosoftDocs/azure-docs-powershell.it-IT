---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 351145AC-7C1E-4EB7-A17D-B8B7D8ED8DAB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 578eef176903576778325eb8610870040a515751
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93685228"
---
# <span data-ttu-id="34bf9-101">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="34bf9-101">New-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="34bf9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="34bf9-102">SYNOPSIS</span></span>
<span data-ttu-id="34bf9-103">Crea un criterio di accesso archiviato per una coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="34bf9-103">Creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="34bf9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="34bf9-104">SYNTAX</span></span>

```
New-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="34bf9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="34bf9-105">DESCRIPTION</span></span>
<span data-ttu-id="34bf9-106">Il cmdlet **New-AzureStorageQueueStoredAccessPolicy** crea un criterio di accesso archiviato per una coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="34bf9-106">The **New-AzureStorageQueueStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="34bf9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="34bf9-107">EXAMPLES</span></span>

### <span data-ttu-id="34bf9-108">Esempio 1: creare criteri di accesso archiviati in una coda di archiviazione</span><span class="sxs-lookup"><span data-stu-id="34bf9-108">Example 1: Create a stored access policy in a storage queue</span></span>
```
PS C:\>New-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy01"
```

<span data-ttu-id="34bf9-109">Questo comando crea un criterio di accesso denominato Policy01 nella coda di archiviazione denominata Queue.</span><span class="sxs-lookup"><span data-stu-id="34bf9-109">This command creates an access policy named Policy01 in the storage queue named MyQueue.</span></span>

## <span data-ttu-id="34bf9-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="34bf9-110">PARAMETERS</span></span>

### <span data-ttu-id="34bf9-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="34bf9-111">-Context</span></span>
<span data-ttu-id="34bf9-112">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="34bf9-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="34bf9-113">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="34bf9-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="34bf9-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="34bf9-114">-ExpiryTime</span></span>
<span data-ttu-id="34bf9-115">Specifica il momento in cui il criterio di accesso archiviato diventa non valido.</span><span class="sxs-lookup"><span data-stu-id="34bf9-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="34bf9-116">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="34bf9-116">-Permission</span></span>
<span data-ttu-id="34bf9-117">Specifica il livello di accesso pubblico alla coda di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="34bf9-117">Specifies the level of public access to this storage queue.</span></span>

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

### <span data-ttu-id="34bf9-118">-Policy</span><span class="sxs-lookup"><span data-stu-id="34bf9-118">-Policy</span></span>
<span data-ttu-id="34bf9-119">Specifica un criterio di accesso archiviato, che include le autorizzazioni per il token SAS.</span><span class="sxs-lookup"><span data-stu-id="34bf9-119">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="34bf9-120">-Queue</span><span class="sxs-lookup"><span data-stu-id="34bf9-120">-Queue</span></span>
<span data-ttu-id="34bf9-121">Specifica il nome della coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="34bf9-121">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="34bf9-122">-StartTime</span><span class="sxs-lookup"><span data-stu-id="34bf9-122">-StartTime</span></span>
<span data-ttu-id="34bf9-123">Specifica il momento in cui i criteri di accesso archiviati diventano validi.</span><span class="sxs-lookup"><span data-stu-id="34bf9-123">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="34bf9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34bf9-124">CommonParameters</span></span>
<span data-ttu-id="34bf9-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34bf9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34bf9-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34bf9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34bf9-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="34bf9-127">INPUTS</span></span>

## <span data-ttu-id="34bf9-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="34bf9-128">OUTPUTS</span></span>

## <span data-ttu-id="34bf9-129">Note</span><span class="sxs-lookup"><span data-stu-id="34bf9-129">NOTES</span></span>

## <span data-ttu-id="34bf9-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="34bf9-130">RELATED LINKS</span></span>

[<span data-ttu-id="34bf9-131">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="34bf9-131">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="34bf9-132">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="34bf9-132">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="34bf9-133">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="34bf9-133">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="34bf9-134">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="34bf9-134">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)


