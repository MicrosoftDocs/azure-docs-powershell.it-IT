---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: e2e88cc676fddd6da7ce460fbe0d9d770756c4c9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974142"
---
# <span data-ttu-id="2a5c6-101">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2a5c6-101">Set-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="2a5c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a5c6-102">SYNOPSIS</span></span>
<span data-ttu-id="2a5c6-103">Imposta un criterio di accesso archiviato per una coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="2a5c6-103">Sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="2a5c6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2a5c6-104">SYNTAX</span></span>

```
Set-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a5c6-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2a5c6-105">DESCRIPTION</span></span>
<span data-ttu-id="2a5c6-106">Il cmdlet **Set-AzStorageQueueStoredAccessPolicy** imposta un criterio di accesso archiviato per una coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="2a5c6-106">The **Set-AzStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="2a5c6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2a5c6-107">EXAMPLES</span></span>

### <span data-ttu-id="2a5c6-108">Esempio 1: Impostare un criterio di accesso archiviato nella coda con autorizzazione completa</span><span class="sxs-lookup"><span data-stu-id="2a5c6-108">Example 1: Set a stored access policy in the queue with full permission</span></span>
```
PS C:\> Set-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07" -Permission arup
```

<span data-ttu-id="2a5c6-109">Questo comando imposta un criterio di accesso denominato Policy07 per la coda di archiviazione denominata MyQueue.</span><span class="sxs-lookup"><span data-stu-id="2a5c6-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="2a5c6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a5c6-110">PARAMETERS</span></span>

### <span data-ttu-id="2a5c6-111">-Context</span><span class="sxs-lookup"><span data-stu-id="2a5c6-111">-Context</span></span>
<span data-ttu-id="2a5c6-112">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="2a5c6-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="2a5c6-113">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzStorageContext archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2a5c6-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="2a5c6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a5c6-114">-DefaultProfile</span></span>
<span data-ttu-id="2a5c6-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2a5c6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a5c6-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="2a5c6-116">-ExpiryTime</span></span>
<span data-ttu-id="2a5c6-117">Specifica l'ora in cui i criteri di accesso archiviato non sono più validi.</span><span class="sxs-lookup"><span data-stu-id="2a5c6-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="2a5c6-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="2a5c6-118">-NoExpiryTime</span></span>
<span data-ttu-id="2a5c6-119">Indica che i criteri di accesso non hanno una data di scadenza.</span><span class="sxs-lookup"><span data-stu-id="2a5c6-119">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="2a5c6-120">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="2a5c6-120">-NoStartTime</span></span>
<span data-ttu-id="2a5c6-121">Indica che questo cmdlet imposta l'ora di inizio $Null.</span><span class="sxs-lookup"><span data-stu-id="2a5c6-121">Indicates that this cmdlet sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="2a5c6-122">-Permission</span><span class="sxs-lookup"><span data-stu-id="2a5c6-122">-Permission</span></span>
<span data-ttu-id="2a5c6-123">Specifica le autorizzazioni nei criteri di accesso archiviato per accedere alla coda di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2a5c6-123">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="2a5c6-124">È importante notare che si tratta di una stringa, ad esempio `rwd` (per Lettura, Scrittura ed Elimina).</span><span class="sxs-lookup"><span data-stu-id="2a5c6-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="2a5c6-125">-Policy</span><span class="sxs-lookup"><span data-stu-id="2a5c6-125">-Policy</span></span>
<span data-ttu-id="2a5c6-126">Specifica il nome per i criteri di accesso archiviato.</span><span class="sxs-lookup"><span data-stu-id="2a5c6-126">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="2a5c6-127">-Queue</span><span class="sxs-lookup"><span data-stu-id="2a5c6-127">-Queue</span></span>
<span data-ttu-id="2a5c6-128">Specifica il nome della coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="2a5c6-128">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="2a5c6-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="2a5c6-129">-StartTime</span></span>
<span data-ttu-id="2a5c6-130">Specifica l'ora in cui i criteri di accesso archiviato diventano validi.</span><span class="sxs-lookup"><span data-stu-id="2a5c6-130">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="2a5c6-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2a5c6-131">-Confirm</span></span>
<span data-ttu-id="2a5c6-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a5c6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a5c6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a5c6-133">-WhatIf</span></span>
<span data-ttu-id="2a5c6-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2a5c6-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2a5c6-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2a5c6-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a5c6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a5c6-136">CommonParameters</span></span>
<span data-ttu-id="2a5c6-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a5c6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a5c6-138">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a5c6-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a5c6-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="2a5c6-139">INPUTS</span></span>

### <span data-ttu-id="2a5c6-140">System.String</span><span class="sxs-lookup"><span data-stu-id="2a5c6-140">System.String</span></span>

### <span data-ttu-id="2a5c6-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2a5c6-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2a5c6-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2a5c6-142">OUTPUTS</span></span>

### <span data-ttu-id="2a5c6-143">System.String</span><span class="sxs-lookup"><span data-stu-id="2a5c6-143">System.String</span></span>

## <span data-ttu-id="2a5c6-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="2a5c6-144">NOTES</span></span>

## <span data-ttu-id="2a5c6-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2a5c6-145">RELATED LINKS</span></span>

[<span data-ttu-id="2a5c6-146">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2a5c6-146">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="2a5c6-147">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2a5c6-147">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="2a5c6-148">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2a5c6-148">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)
