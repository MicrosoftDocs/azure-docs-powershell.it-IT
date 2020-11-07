---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragequeuestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 4e1b58e2ca2586ada574b55a03287d1cc5915b6f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93867173"
---
# <span data-ttu-id="44ffc-101">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="44ffc-101">Set-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="44ffc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="44ffc-102">SYNOPSIS</span></span>
<span data-ttu-id="44ffc-103">Imposta un criterio di accesso archiviato per una coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="44ffc-103">Sets a stored access policy for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44ffc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="44ffc-104">SYNTAX</span></span>

```
Set-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44ffc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="44ffc-105">DESCRIPTION</span></span>
<span data-ttu-id="44ffc-106">Il cmdlet **set-AzureStorageQueueStoredAccessPolicy** imposta un criterio di accesso archiviato per una coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="44ffc-106">The **Set-AzureStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="44ffc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="44ffc-107">EXAMPLES</span></span>

### <span data-ttu-id="44ffc-108">Esempio 1: impostare un criterio di accesso archiviato nella coda con l'autorizzazione completa</span><span class="sxs-lookup"><span data-stu-id="44ffc-108">Example 1: Set a stored access policy in the queue with full permission</span></span>
```
PS C:\> Set-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07" -Permission arup
```

<span data-ttu-id="44ffc-109">Questo comando imposta un criterio di accesso denominato Policy07 per la coda di archiviazione denominata Queue.</span><span class="sxs-lookup"><span data-stu-id="44ffc-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="44ffc-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="44ffc-110">PARAMETERS</span></span>

### <span data-ttu-id="44ffc-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="44ffc-111">-Context</span></span>
<span data-ttu-id="44ffc-112">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="44ffc-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="44ffc-113">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="44ffc-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="44ffc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44ffc-114">-DefaultProfile</span></span>
<span data-ttu-id="44ffc-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="44ffc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44ffc-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="44ffc-116">-ExpiryTime</span></span>
<span data-ttu-id="44ffc-117">Specifica il momento in cui il criterio di accesso archiviato diventa non valido.</span><span class="sxs-lookup"><span data-stu-id="44ffc-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="44ffc-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="44ffc-118">-NoExpiryTime</span></span>
<span data-ttu-id="44ffc-119">Indica che il criterio di accesso non ha una data di scadenza.</span><span class="sxs-lookup"><span data-stu-id="44ffc-119">Indicates that the access policy has no expiration date.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44ffc-120">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="44ffc-120">-NoStartTime</span></span>
<span data-ttu-id="44ffc-121">Indica che questo cmdlet imposta l'ora di inizio da $Null.</span><span class="sxs-lookup"><span data-stu-id="44ffc-121">Indicates that this cmdlet sets the start time to be $Null.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44ffc-122">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="44ffc-122">-Permission</span></span>
<span data-ttu-id="44ffc-123">Specifica le autorizzazioni nei criteri di accesso archiviati per accedere alla coda di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="44ffc-123">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="44ffc-124">È importante notare che si tratta di una stringa, ad esempio `rwd` (per lettura, scrittura ed eliminazione).</span><span class="sxs-lookup"><span data-stu-id="44ffc-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="44ffc-125">-Policy</span><span class="sxs-lookup"><span data-stu-id="44ffc-125">-Policy</span></span>
<span data-ttu-id="44ffc-126">Specifica il nome per i criteri di accesso archiviati.</span><span class="sxs-lookup"><span data-stu-id="44ffc-126">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="44ffc-127">-Queue</span><span class="sxs-lookup"><span data-stu-id="44ffc-127">-Queue</span></span>
<span data-ttu-id="44ffc-128">Specifica il nome della coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="44ffc-128">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="44ffc-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="44ffc-129">-StartTime</span></span>
<span data-ttu-id="44ffc-130">Specifica il momento in cui i criteri di accesso archiviati diventano validi.</span><span class="sxs-lookup"><span data-stu-id="44ffc-130">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="44ffc-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="44ffc-131">-Confirm</span></span>
<span data-ttu-id="44ffc-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44ffc-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44ffc-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44ffc-133">-WhatIf</span></span>
<span data-ttu-id="44ffc-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="44ffc-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="44ffc-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="44ffc-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44ffc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44ffc-136">CommonParameters</span></span>
<span data-ttu-id="44ffc-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44ffc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44ffc-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44ffc-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44ffc-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="44ffc-139">INPUTS</span></span>

### <span data-ttu-id="44ffc-140">System. String</span><span class="sxs-lookup"><span data-stu-id="44ffc-140">System.String</span></span>

### <span data-ttu-id="44ffc-141">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="44ffc-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="44ffc-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="44ffc-142">OUTPUTS</span></span>

### <span data-ttu-id="44ffc-143">System. String</span><span class="sxs-lookup"><span data-stu-id="44ffc-143">System.String</span></span>

## <span data-ttu-id="44ffc-144">Note</span><span class="sxs-lookup"><span data-stu-id="44ffc-144">NOTES</span></span>

## <span data-ttu-id="44ffc-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="44ffc-145">RELATED LINKS</span></span>

[<span data-ttu-id="44ffc-146">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="44ffc-146">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="44ffc-147">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="44ffc-147">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="44ffc-148">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="44ffc-148">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)
