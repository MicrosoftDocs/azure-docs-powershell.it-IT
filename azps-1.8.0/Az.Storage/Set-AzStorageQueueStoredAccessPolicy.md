---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 32ba9d7c10b80eee23c2d41ec48eac4c01239681
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676496"
---
# <span data-ttu-id="0632b-101">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0632b-101">Set-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="0632b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0632b-102">SYNOPSIS</span></span>
<span data-ttu-id="0632b-103">Imposta un criterio di accesso archiviato per una coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="0632b-103">Sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="0632b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0632b-104">SYNTAX</span></span>

```
Set-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0632b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0632b-105">DESCRIPTION</span></span>
<span data-ttu-id="0632b-106">Il cmdlet **set-AzStorageQueueStoredAccessPolicy** imposta un criterio di accesso archiviato per una coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="0632b-106">The **Set-AzStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="0632b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0632b-107">EXAMPLES</span></span>

### <span data-ttu-id="0632b-108">Esempio 1: impostare un criterio di accesso archiviato nella coda con l'autorizzazione completa</span><span class="sxs-lookup"><span data-stu-id="0632b-108">Example 1: Set a stored access policy in the queue with full permission</span></span>
```
PS C:\> Set-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07" -Permission arup
```

<span data-ttu-id="0632b-109">Questo comando imposta un criterio di accesso denominato Policy07 per la coda di archiviazione denominata Queue.</span><span class="sxs-lookup"><span data-stu-id="0632b-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="0632b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0632b-110">PARAMETERS</span></span>

### <span data-ttu-id="0632b-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="0632b-111">-Context</span></span>
<span data-ttu-id="0632b-112">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="0632b-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="0632b-113">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="0632b-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="0632b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0632b-114">-DefaultProfile</span></span>
<span data-ttu-id="0632b-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0632b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0632b-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="0632b-116">-ExpiryTime</span></span>
<span data-ttu-id="0632b-117">Specifica il momento in cui il criterio di accesso archiviato diventa non valido.</span><span class="sxs-lookup"><span data-stu-id="0632b-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="0632b-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="0632b-118">-NoExpiryTime</span></span>
<span data-ttu-id="0632b-119">Indica che il criterio di accesso non ha una data di scadenza.</span><span class="sxs-lookup"><span data-stu-id="0632b-119">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="0632b-120">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="0632b-120">-NoStartTime</span></span>
<span data-ttu-id="0632b-121">Indica che questo cmdlet imposta l'ora di inizio da $Null.</span><span class="sxs-lookup"><span data-stu-id="0632b-121">Indicates that this cmdlet sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="0632b-122">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="0632b-122">-Permission</span></span>
<span data-ttu-id="0632b-123">Specifica le autorizzazioni nei criteri di accesso archiviati per accedere alla coda di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="0632b-123">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="0632b-124">È importante notare che si tratta di una stringa, ad esempio `rwd` (per lettura, scrittura ed eliminazione).</span><span class="sxs-lookup"><span data-stu-id="0632b-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="0632b-125">-Policy</span><span class="sxs-lookup"><span data-stu-id="0632b-125">-Policy</span></span>
<span data-ttu-id="0632b-126">Specifica il nome per i criteri di accesso archiviati.</span><span class="sxs-lookup"><span data-stu-id="0632b-126">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="0632b-127">-Queue</span><span class="sxs-lookup"><span data-stu-id="0632b-127">-Queue</span></span>
<span data-ttu-id="0632b-128">Specifica il nome della coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="0632b-128">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="0632b-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="0632b-129">-StartTime</span></span>
<span data-ttu-id="0632b-130">Specifica il momento in cui i criteri di accesso archiviati diventano validi.</span><span class="sxs-lookup"><span data-stu-id="0632b-130">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="0632b-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0632b-131">-Confirm</span></span>
<span data-ttu-id="0632b-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0632b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0632b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0632b-133">-WhatIf</span></span>
<span data-ttu-id="0632b-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0632b-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0632b-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0632b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0632b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0632b-136">CommonParameters</span></span>
<span data-ttu-id="0632b-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0632b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0632b-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0632b-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0632b-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0632b-139">INPUTS</span></span>

### <span data-ttu-id="0632b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="0632b-140">System.String</span></span>

### <span data-ttu-id="0632b-141">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0632b-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0632b-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0632b-142">OUTPUTS</span></span>

### <span data-ttu-id="0632b-143">System. String</span><span class="sxs-lookup"><span data-stu-id="0632b-143">System.String</span></span>

## <span data-ttu-id="0632b-144">Note</span><span class="sxs-lookup"><span data-stu-id="0632b-144">NOTES</span></span>

## <span data-ttu-id="0632b-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0632b-145">RELATED LINKS</span></span>

[<span data-ttu-id="0632b-146">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0632b-146">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="0632b-147">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0632b-147">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="0632b-148">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0632b-148">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)