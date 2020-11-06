---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: ''
schema: 2.0.0
ms.openlocfilehash: b273dbec3fda421574c8866a10eda0a8098513ff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93507168"
---
# <span data-ttu-id="84324-101">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="84324-101">Set-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="84324-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="84324-102">SYNOPSIS</span></span>
<span data-ttu-id="84324-103">Imposta un criterio di accesso archiviato per una coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="84324-103">Sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="84324-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="84324-104">SYNTAX</span></span>

```
Set-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84324-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84324-105">DESCRIPTION</span></span>
<span data-ttu-id="84324-106">Il cmdlet **set-AzureStorageQueueStoredAccessPolicy** imposta un criterio di accesso archiviato per una coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="84324-106">The **Set-AzureStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="84324-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="84324-107">EXAMPLES</span></span>

### <span data-ttu-id="84324-108">Esempio 1: impostare un criterio di accesso archiviato nella coda</span><span class="sxs-lookup"><span data-stu-id="84324-108">Example 1: Set a stored access policy in the queue</span></span>
```
PS C:\> Set-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07"
```

<span data-ttu-id="84324-109">Questo comando imposta un criterio di accesso denominato Policy07 per la coda di archiviazione denominata Queue.</span><span class="sxs-lookup"><span data-stu-id="84324-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="84324-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="84324-110">PARAMETERS</span></span>

### <span data-ttu-id="84324-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="84324-111">-Context</span></span>
<span data-ttu-id="84324-112">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="84324-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="84324-113">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="84324-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="84324-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="84324-114">-ExpiryTime</span></span>
<span data-ttu-id="84324-115">Specifica il momento in cui il criterio di accesso archiviato diventa non valido.</span><span class="sxs-lookup"><span data-stu-id="84324-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="84324-116">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="84324-116">-NoExpiryTime</span></span>
<span data-ttu-id="84324-117">Indica che il criterio di accesso non ha una data di scadenza.</span><span class="sxs-lookup"><span data-stu-id="84324-117">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="84324-118">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="84324-118">-NoStartTime</span></span>
<span data-ttu-id="84324-119">Indica che questo cmdlet imposta l'ora di inizio da $Null.</span><span class="sxs-lookup"><span data-stu-id="84324-119">Indicates that this cmdlet sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="84324-120">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="84324-120">-Permission</span></span>
<span data-ttu-id="84324-121">Specifica il livello di accesso pubblico alla coda di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="84324-121">Specifies the level of public access to this storage queue.</span></span>

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

### <span data-ttu-id="84324-122">-Policy</span><span class="sxs-lookup"><span data-stu-id="84324-122">-Policy</span></span>
<span data-ttu-id="84324-123">Specifica un criterio di accesso archiviato, che include le autorizzazioni per il token SAS.</span><span class="sxs-lookup"><span data-stu-id="84324-123">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="84324-124">-Queue</span><span class="sxs-lookup"><span data-stu-id="84324-124">-Queue</span></span>
<span data-ttu-id="84324-125">Specifica il nome della coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="84324-125">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="84324-126">-StartTime</span><span class="sxs-lookup"><span data-stu-id="84324-126">-StartTime</span></span>
<span data-ttu-id="84324-127">Specifica il momento in cui i criteri di accesso archiviati diventano validi.</span><span class="sxs-lookup"><span data-stu-id="84324-127">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="84324-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="84324-128">-Confirm</span></span>
<span data-ttu-id="84324-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84324-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84324-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84324-130">-WhatIf</span></span>
<span data-ttu-id="84324-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="84324-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="84324-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="84324-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84324-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84324-133">CommonParameters</span></span>
<span data-ttu-id="84324-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84324-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84324-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84324-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84324-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="84324-136">INPUTS</span></span>

## <span data-ttu-id="84324-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="84324-137">OUTPUTS</span></span>

## <span data-ttu-id="84324-138">Note</span><span class="sxs-lookup"><span data-stu-id="84324-138">NOTES</span></span>

## <span data-ttu-id="84324-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="84324-139">RELATED LINKS</span></span>

[<span data-ttu-id="84324-140">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="84324-140">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="84324-141">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="84324-141">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="84324-142">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="84324-142">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)
