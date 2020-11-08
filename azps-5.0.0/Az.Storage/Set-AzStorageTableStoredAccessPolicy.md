---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FF2BFE34-4A12-49F9-9BE5-4084A36BC272
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 822781f6c46eeb76a953eaa66935c03cd76df737
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193708"
---
# <span data-ttu-id="d2af6-101">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d2af6-101">Set-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="d2af6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d2af6-102">SYNOPSIS</span></span>
<span data-ttu-id="d2af6-103">Imposta i criteri di accesso archiviati per una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d2af6-103">Sets the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="d2af6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d2af6-104">SYNTAX</span></span>

```
Set-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2af6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d2af6-105">DESCRIPTION</span></span>
<span data-ttu-id="d2af6-106">Il cmdlet **set-AzStorageTableStoredAccessPolicy** imposta i criteri di accesso archiviati per una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d2af6-106">The **Set-AzStorageTableStoredAccessPolicy** cmdlet set the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="d2af6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d2af6-107">EXAMPLES</span></span>

### <span data-ttu-id="d2af6-108">Esempio 1: impostare i criteri di accesso archiviati in una tabella con l'autorizzazione completa</span><span class="sxs-lookup"><span data-stu-id="d2af6-108">Example 1: Set a stored access policy in table with full permission</span></span>
```
PS C:\>Set-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy08" -Permission raud
```

<span data-ttu-id="d2af6-109">Questo comando imposta un criterio di accesso denominato Policy08 per la tabella di archiviazione denominata MyTable.</span><span class="sxs-lookup"><span data-stu-id="d2af6-109">This command sets an access policy named Policy08 for storage table named MyTable.</span></span>

## <span data-ttu-id="d2af6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d2af6-110">PARAMETERS</span></span>

### <span data-ttu-id="d2af6-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="d2af6-111">-Context</span></span>
<span data-ttu-id="d2af6-112">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d2af6-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="d2af6-113">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="d2af6-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d2af6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2af6-114">-DefaultProfile</span></span>
<span data-ttu-id="d2af6-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d2af6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2af6-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="d2af6-116">-ExpiryTime</span></span>
<span data-ttu-id="d2af6-117">Specifica il momento in cui i criteri di accesso archiviati scadono.</span><span class="sxs-lookup"><span data-stu-id="d2af6-117">Specifies the time at which the stored access policy expires.</span></span>

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

### <span data-ttu-id="d2af6-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="d2af6-118">-NoExpiryTime</span></span>
<span data-ttu-id="d2af6-119">Indica che il criterio di accesso non ha una data di scadenza.</span><span class="sxs-lookup"><span data-stu-id="d2af6-119">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="d2af6-120">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="d2af6-120">-NoStartTime</span></span>
<span data-ttu-id="d2af6-121">Indica che l'ora di inizio è impostata su $Null.</span><span class="sxs-lookup"><span data-stu-id="d2af6-121">Indicates that the start time is set to $Null.</span></span>

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

### <span data-ttu-id="d2af6-122">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="d2af6-122">-Permission</span></span>
<span data-ttu-id="d2af6-123">Specifica le autorizzazioni nei criteri di accesso archiviati per accedere alla tabella di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d2af6-123">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="d2af6-124">È importante notare che si tratta di una stringa, ad esempio `rwd` (per lettura, scrittura ed eliminazione).</span><span class="sxs-lookup"><span data-stu-id="d2af6-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="d2af6-125">-Policy</span><span class="sxs-lookup"><span data-stu-id="d2af6-125">-Policy</span></span>
<span data-ttu-id="d2af6-126">Specifica il nome per i criteri di accesso archiviati.</span><span class="sxs-lookup"><span data-stu-id="d2af6-126">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="d2af6-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="d2af6-127">-StartTime</span></span>
<span data-ttu-id="d2af6-128">Specifica il momento in cui i criteri di accesso archiviati diventano validi.</span><span class="sxs-lookup"><span data-stu-id="d2af6-128">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="d2af6-129">-Tabella</span><span class="sxs-lookup"><span data-stu-id="d2af6-129">-Table</span></span>
<span data-ttu-id="d2af6-130">Specifica il nome della tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d2af6-130">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="d2af6-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d2af6-131">-Confirm</span></span>
<span data-ttu-id="d2af6-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2af6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2af6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2af6-133">-WhatIf</span></span>
<span data-ttu-id="d2af6-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d2af6-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d2af6-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d2af6-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2af6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2af6-136">CommonParameters</span></span>
<span data-ttu-id="d2af6-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2af6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2af6-138">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2af6-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2af6-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d2af6-139">INPUTS</span></span>

### <span data-ttu-id="d2af6-140">System. String</span><span class="sxs-lookup"><span data-stu-id="d2af6-140">System.String</span></span>

### <span data-ttu-id="d2af6-141">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d2af6-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d2af6-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d2af6-142">OUTPUTS</span></span>

### <span data-ttu-id="d2af6-143">System. String</span><span class="sxs-lookup"><span data-stu-id="d2af6-143">System.String</span></span>

## <span data-ttu-id="d2af6-144">Note</span><span class="sxs-lookup"><span data-stu-id="d2af6-144">NOTES</span></span>

## <span data-ttu-id="d2af6-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d2af6-145">RELATED LINKS</span></span>

[<span data-ttu-id="d2af6-146">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d2af6-146">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="d2af6-147">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="d2af6-147">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="d2af6-148">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d2af6-148">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="d2af6-149">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d2af6-149">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)