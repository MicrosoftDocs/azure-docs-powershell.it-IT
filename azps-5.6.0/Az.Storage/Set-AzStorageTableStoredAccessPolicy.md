---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FF2BFE34-4A12-49F9-9BE5-4084A36BC272
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 576b347ad260fc95cdafe7c4a11e42246feb09ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971709"
---
# <span data-ttu-id="d4650-101">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d4650-101">Set-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="d4650-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4650-102">SYNOPSIS</span></span>
<span data-ttu-id="d4650-103">Imposta i criteri di accesso archiviato per una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d4650-103">Sets the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="d4650-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d4650-104">SYNTAX</span></span>

```
Set-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4650-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d4650-105">DESCRIPTION</span></span>
<span data-ttu-id="d4650-106">Il cmdlet **Set-AzStorageTableStoredAccessPolicy** imposta i criteri di accesso archiviato per una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d4650-106">The **Set-AzStorageTableStoredAccessPolicy** cmdlet set the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="d4650-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d4650-107">EXAMPLES</span></span>

### <span data-ttu-id="d4650-108">Esempio 1: Impostare un criterio di accesso archiviato in una tabella con autorizzazioni complete</span><span class="sxs-lookup"><span data-stu-id="d4650-108">Example 1: Set a stored access policy in table with full permission</span></span>
```
PS C:\>Set-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy08" -Permission raud
```

<span data-ttu-id="d4650-109">Questo comando imposta un criterio di accesso denominato Policy08 per la tabella di archiviazione denominata Tabella_</span><span class="sxs-lookup"><span data-stu-id="d4650-109">This command sets an access policy named Policy08 for storage table named MyTable.</span></span>

## <span data-ttu-id="d4650-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4650-110">PARAMETERS</span></span>

### <span data-ttu-id="d4650-111">-Context</span><span class="sxs-lookup"><span data-stu-id="d4650-111">-Context</span></span>
<span data-ttu-id="d4650-112">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d4650-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="d4650-113">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzStorageContext archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d4650-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d4650-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4650-114">-DefaultProfile</span></span>
<span data-ttu-id="d4650-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d4650-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4650-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="d4650-116">-ExpiryTime</span></span>
<span data-ttu-id="d4650-117">Specifica l'ora di scadenza dei criteri di accesso archiviato.</span><span class="sxs-lookup"><span data-stu-id="d4650-117">Specifies the time at which the stored access policy expires.</span></span>

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

### <span data-ttu-id="d4650-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="d4650-118">-NoExpiryTime</span></span>
<span data-ttu-id="d4650-119">Indica che i criteri di accesso non hanno una data di scadenza.</span><span class="sxs-lookup"><span data-stu-id="d4650-119">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="d4650-120">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="d4650-120">-NoStartTime</span></span>
<span data-ttu-id="d4650-121">Indica che l'ora di inizio è impostata su $Null.</span><span class="sxs-lookup"><span data-stu-id="d4650-121">Indicates that the start time is set to $Null.</span></span>

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

### <span data-ttu-id="d4650-122">-Permission</span><span class="sxs-lookup"><span data-stu-id="d4650-122">-Permission</span></span>
<span data-ttu-id="d4650-123">Specifica le autorizzazioni nei criteri di accesso archiviato per accedere alla tabella di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d4650-123">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="d4650-124">È importante notare che si tratta di una stringa, ad esempio `rwd` (per Lettura, Scrittura ed Elimina).</span><span class="sxs-lookup"><span data-stu-id="d4650-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="d4650-125">-Policy</span><span class="sxs-lookup"><span data-stu-id="d4650-125">-Policy</span></span>
<span data-ttu-id="d4650-126">Specifica il nome per i criteri di accesso archiviato.</span><span class="sxs-lookup"><span data-stu-id="d4650-126">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="d4650-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="d4650-127">-StartTime</span></span>
<span data-ttu-id="d4650-128">Specifica l'ora in cui i criteri di accesso archiviato diventano validi.</span><span class="sxs-lookup"><span data-stu-id="d4650-128">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="d4650-129">-Table</span><span class="sxs-lookup"><span data-stu-id="d4650-129">-Table</span></span>
<span data-ttu-id="d4650-130">Specifica il nome della tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d4650-130">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="d4650-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d4650-131">-Confirm</span></span>
<span data-ttu-id="d4650-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4650-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4650-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4650-133">-WhatIf</span></span>
<span data-ttu-id="d4650-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d4650-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d4650-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d4650-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4650-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4650-136">CommonParameters</span></span>
<span data-ttu-id="d4650-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4650-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4650-138">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4650-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4650-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="d4650-139">INPUTS</span></span>

### <span data-ttu-id="d4650-140">System.String</span><span class="sxs-lookup"><span data-stu-id="d4650-140">System.String</span></span>

### <span data-ttu-id="d4650-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d4650-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d4650-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d4650-142">OUTPUTS</span></span>

### <span data-ttu-id="d4650-143">System.String</span><span class="sxs-lookup"><span data-stu-id="d4650-143">System.String</span></span>

## <span data-ttu-id="d4650-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="d4650-144">NOTES</span></span>

## <span data-ttu-id="d4650-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d4650-145">RELATED LINKS</span></span>

[<span data-ttu-id="d4650-146">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d4650-146">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="d4650-147">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="d4650-147">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="d4650-148">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d4650-148">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="d4650-149">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d4650-149">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)
