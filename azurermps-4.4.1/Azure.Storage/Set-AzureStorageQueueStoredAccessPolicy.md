---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageQueueStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 69ec2307dfdf8525f892720281079c58c1e1bd55
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520832"
---
# <span data-ttu-id="2ab54-101">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2ab54-101">Set-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="2ab54-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2ab54-102">SYNOPSIS</span></span>
<span data-ttu-id="2ab54-103">Imposta un criterio di accesso archiviato per una coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="2ab54-103">Sets a stored access policy for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ab54-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2ab54-104">SYNTAX</span></span>

```
Set-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ab54-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2ab54-105">DESCRIPTION</span></span>
<span data-ttu-id="2ab54-106">Il cmdlet **set-AzureStorageQueueStoredAccessPolicy** imposta un criterio di accesso archiviato per una coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="2ab54-106">The **Set-AzureStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="2ab54-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2ab54-107">EXAMPLES</span></span>

### <span data-ttu-id="2ab54-108">Esempio 1: impostare un criterio di accesso archiviato nella coda con l'autorizzazione completa</span><span class="sxs-lookup"><span data-stu-id="2ab54-108">Example 1: Set a stored access policy in the queue with full permission</span></span>
```
PS C:\> Set-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07" -Permission arup
```

<span data-ttu-id="2ab54-109">Questo comando imposta un criterio di accesso denominato Policy07 per la coda di archiviazione denominata Queue.</span><span class="sxs-lookup"><span data-stu-id="2ab54-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="2ab54-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2ab54-110">PARAMETERS</span></span>

### <span data-ttu-id="2ab54-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="2ab54-111">-Context</span></span>
<span data-ttu-id="2ab54-112">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="2ab54-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="2ab54-113">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="2ab54-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="2ab54-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="2ab54-114">-ExpiryTime</span></span>
<span data-ttu-id="2ab54-115">Specifica il momento in cui il criterio di accesso archiviato diventa non valido.</span><span class="sxs-lookup"><span data-stu-id="2ab54-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="2ab54-116">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="2ab54-116">-NoExpiryTime</span></span>
<span data-ttu-id="2ab54-117">Indica che il criterio di accesso non ha una data di scadenza.</span><span class="sxs-lookup"><span data-stu-id="2ab54-117">Indicates that the access policy has no expiration date.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ab54-118">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="2ab54-118">-NoStartTime</span></span>
<span data-ttu-id="2ab54-119">Indica che questo cmdlet imposta l'ora di inizio da $Null.</span><span class="sxs-lookup"><span data-stu-id="2ab54-119">Indicates that this cmdlet sets the start time to be $Null.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ab54-120">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="2ab54-120">-Permission</span></span>
<span data-ttu-id="2ab54-121">Specifica le autorizzazioni nei criteri di accesso archiviati per accedere alla coda di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2ab54-121">Specifies permissions in the stored access policy to access the storage queue.</span></span>

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

### <span data-ttu-id="2ab54-122">-Policy</span><span class="sxs-lookup"><span data-stu-id="2ab54-122">-Policy</span></span>
<span data-ttu-id="2ab54-123">Specifica il nome per i criteri di accesso archiviati.</span><span class="sxs-lookup"><span data-stu-id="2ab54-123">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="2ab54-124">-Queue</span><span class="sxs-lookup"><span data-stu-id="2ab54-124">-Queue</span></span>
<span data-ttu-id="2ab54-125">Specifica il nome della coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="2ab54-125">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="2ab54-126">-StartTime</span><span class="sxs-lookup"><span data-stu-id="2ab54-126">-StartTime</span></span>
<span data-ttu-id="2ab54-127">Specifica il momento in cui i criteri di accesso archiviati diventano validi.</span><span class="sxs-lookup"><span data-stu-id="2ab54-127">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="2ab54-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2ab54-128">-Confirm</span></span>
<span data-ttu-id="2ab54-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ab54-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ab54-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ab54-130">-WhatIf</span></span>
<span data-ttu-id="2ab54-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2ab54-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2ab54-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2ab54-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ab54-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ab54-133">CommonParameters</span></span>
<span data-ttu-id="2ab54-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ab54-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ab54-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ab54-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ab54-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2ab54-136">INPUTS</span></span>

### <span data-ttu-id="2ab54-137">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2ab54-137">IStorageContext</span></span>

<span data-ttu-id="2ab54-138">Il parametro "context" accetta il valore di tipo "IStorageContext" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="2ab54-138">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="2ab54-139">Stringa</span><span class="sxs-lookup"><span data-stu-id="2ab54-139">String</span></span>

<span data-ttu-id="2ab54-140">Il parametro "Queue" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="2ab54-140">Parameter 'Queue' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="2ab54-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2ab54-141">OUTPUTS</span></span>

### <span data-ttu-id="2ab54-142">System. String</span><span class="sxs-lookup"><span data-stu-id="2ab54-142">System.String</span></span>

## <span data-ttu-id="2ab54-143">Note</span><span class="sxs-lookup"><span data-stu-id="2ab54-143">NOTES</span></span>

## <span data-ttu-id="2ab54-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2ab54-144">RELATED LINKS</span></span>

[<span data-ttu-id="2ab54-145">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2ab54-145">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="2ab54-146">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2ab54-146">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="2ab54-147">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2ab54-147">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)
