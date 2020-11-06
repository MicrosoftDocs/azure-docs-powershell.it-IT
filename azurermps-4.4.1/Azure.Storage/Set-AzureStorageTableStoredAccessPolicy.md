---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FF2BFE34-4A12-49F9-9BE5-4084A36BC272
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageTableStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: f4dfc77be9006229e2919dd1a4e0cdb1dd8c548e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518472"
---
# <span data-ttu-id="04c42-101">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="04c42-101">Set-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="04c42-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="04c42-102">SYNOPSIS</span></span>
<span data-ttu-id="04c42-103">Imposta i criteri di accesso archiviati per una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="04c42-103">Sets the stored access policy for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04c42-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="04c42-104">SYNTAX</span></span>

```
Set-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04c42-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="04c42-105">DESCRIPTION</span></span>
<span data-ttu-id="04c42-106">Il cmdlet **set-AzureStorageTableStoredAccessPolicy** imposta i criteri di accesso archiviati per una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="04c42-106">The **Set-AzureStorageTableStoredAccessPolicy** cmdlet set the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="04c42-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="04c42-107">EXAMPLES</span></span>

### <span data-ttu-id="04c42-108">Esempio 1: impostare i criteri di accesso archiviati in una tabella con l'autorizzazione completa</span><span class="sxs-lookup"><span data-stu-id="04c42-108">Example 1: Set a stored access policy in table with full permission</span></span>
```
PS C:\>Set-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy08" -Permission raud
```

<span data-ttu-id="04c42-109">Questo comando imposta un criterio di accesso denominato Policy08 per la tabella di archiviazione denominata MyTable.</span><span class="sxs-lookup"><span data-stu-id="04c42-109">This command sets an access policy named Policy08 for storage table named MyTable.</span></span>

## <span data-ttu-id="04c42-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="04c42-110">PARAMETERS</span></span>

### <span data-ttu-id="04c42-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="04c42-111">-Context</span></span>
<span data-ttu-id="04c42-112">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="04c42-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="04c42-113">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="04c42-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="04c42-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="04c42-114">-ExpiryTime</span></span>
<span data-ttu-id="04c42-115">Specifica il momento in cui i criteri di accesso archiviati scadono.</span><span class="sxs-lookup"><span data-stu-id="04c42-115">Specifies the time at which the stored access policy expires.</span></span>

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

### <span data-ttu-id="04c42-116">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="04c42-116">-NoExpiryTime</span></span>
<span data-ttu-id="04c42-117">Indica che il criterio di accesso non ha una data di scadenza.</span><span class="sxs-lookup"><span data-stu-id="04c42-117">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="04c42-118">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="04c42-118">-NoStartTime</span></span>
<span data-ttu-id="04c42-119">Indica che l'ora di inizio è impostata su $Null.</span><span class="sxs-lookup"><span data-stu-id="04c42-119">Indicates that the start time is set to $Null.</span></span>

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

### <span data-ttu-id="04c42-120">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="04c42-120">-Permission</span></span>
<span data-ttu-id="04c42-121">Specifica le autorizzazioni nei criteri di accesso archiviati per accedere alla tabella di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="04c42-121">Specifies permissions in the stored access policy to access the storage table.</span></span>

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

### <span data-ttu-id="04c42-122">-Policy</span><span class="sxs-lookup"><span data-stu-id="04c42-122">-Policy</span></span>
<span data-ttu-id="04c42-123">Specifica il nome per i criteri di accesso archiviati.</span><span class="sxs-lookup"><span data-stu-id="04c42-123">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="04c42-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="04c42-124">-StartTime</span></span>
<span data-ttu-id="04c42-125">Specifica il momento in cui i criteri di accesso archiviati diventano validi.</span><span class="sxs-lookup"><span data-stu-id="04c42-125">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="04c42-126">-Tabella</span><span class="sxs-lookup"><span data-stu-id="04c42-126">-Table</span></span>
<span data-ttu-id="04c42-127">Specifica il nome della tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="04c42-127">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="04c42-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="04c42-128">-Confirm</span></span>
<span data-ttu-id="04c42-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04c42-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04c42-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04c42-130">-WhatIf</span></span>
<span data-ttu-id="04c42-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="04c42-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="04c42-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="04c42-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04c42-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04c42-133">CommonParameters</span></span>
<span data-ttu-id="04c42-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04c42-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04c42-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04c42-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04c42-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="04c42-136">INPUTS</span></span>

### <span data-ttu-id="04c42-137">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="04c42-137">IStorageContext</span></span>

<span data-ttu-id="04c42-138">Il parametro "context" accetta il valore di tipo "IStorageContext" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="04c42-138">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="04c42-139">Stringa</span><span class="sxs-lookup"><span data-stu-id="04c42-139">String</span></span>

<span data-ttu-id="04c42-140">Il parametro "Table" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="04c42-140">Parameter 'Table' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="04c42-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="04c42-141">OUTPUTS</span></span>

### <span data-ttu-id="04c42-142">System. String</span><span class="sxs-lookup"><span data-stu-id="04c42-142">System.String</span></span>

## <span data-ttu-id="04c42-143">Note</span><span class="sxs-lookup"><span data-stu-id="04c42-143">NOTES</span></span>

## <span data-ttu-id="04c42-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="04c42-144">RELATED LINKS</span></span>

[<span data-ttu-id="04c42-145">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="04c42-145">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="04c42-146">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="04c42-146">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="04c42-147">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="04c42-147">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="04c42-148">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="04c42-148">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)
