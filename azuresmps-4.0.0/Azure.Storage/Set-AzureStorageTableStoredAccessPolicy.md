---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FF2BFE34-4A12-49F9-9BE5-4084A36BC272
online version: ''
schema: 2.0.0
ms.openlocfilehash: d517ca49f0be3b6add58d151b3b2f79dad17611c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93507159"
---
# <span data-ttu-id="d3ca2-101">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d3ca2-101">Set-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="d3ca2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d3ca2-102">SYNOPSIS</span></span>
<span data-ttu-id="d3ca2-103">Imposta i criteri di accesso archiviati per una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d3ca2-103">Sets the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="d3ca2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d3ca2-104">SYNTAX</span></span>

```
Set-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3ca2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3ca2-105">DESCRIPTION</span></span>
<span data-ttu-id="d3ca2-106">Il cmdlet **set-AzureStorageTableStoredAccessPolicy** imposta i criteri di accesso archiviati per una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d3ca2-106">The **Set-AzureStorageTableStoredAccessPolicy** cmdlet set the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="d3ca2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d3ca2-107">EXAMPLES</span></span>

### <span data-ttu-id="d3ca2-108">Esempio 1: impostare i criteri di accesso archiviati in una tabella con l'autorizzazione completa</span><span class="sxs-lookup"><span data-stu-id="d3ca2-108">Example 1: Set a stored access policy in table with full permission</span></span>
```
PS C:\>Set-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy08"
```

<span data-ttu-id="d3ca2-109">Questo comando imposta un criterio di accesso denominato Policy08 per la tabella di archiviazione denominata MyTable.</span><span class="sxs-lookup"><span data-stu-id="d3ca2-109">This command sets an access policy named Policy08 for storage table named MyTable.</span></span>

## <span data-ttu-id="d3ca2-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d3ca2-110">PARAMETERS</span></span>

### <span data-ttu-id="d3ca2-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="d3ca2-111">-Context</span></span>
<span data-ttu-id="d3ca2-112">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d3ca2-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="d3ca2-113">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="d3ca2-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d3ca2-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="d3ca2-114">-ExpiryTime</span></span>
<span data-ttu-id="d3ca2-115">Specifica il momento in cui i criteri di accesso archiviati scadono.</span><span class="sxs-lookup"><span data-stu-id="d3ca2-115">Specifies the time at which the stored access policy expires.</span></span>

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

### <span data-ttu-id="d3ca2-116">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="d3ca2-116">-NoExpiryTime</span></span>
<span data-ttu-id="d3ca2-117">Indica che il criterio di accesso non ha una data di scadenza.</span><span class="sxs-lookup"><span data-stu-id="d3ca2-117">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="d3ca2-118">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="d3ca2-118">-NoStartTime</span></span>
<span data-ttu-id="d3ca2-119">Indica che l'ora di inizio è impostata su $Null.</span><span class="sxs-lookup"><span data-stu-id="d3ca2-119">Indicates that the start time is set to $Null.</span></span>

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

### <span data-ttu-id="d3ca2-120">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="d3ca2-120">-Permission</span></span>
<span data-ttu-id="d3ca2-121">Specifica il livello di accesso pubblico alla tabella di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d3ca2-121">Specifies the level of public access to this storage table.</span></span>

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

### <span data-ttu-id="d3ca2-122">-Policy</span><span class="sxs-lookup"><span data-stu-id="d3ca2-122">-Policy</span></span>
<span data-ttu-id="d3ca2-123">Specifica un criterio di accesso archiviato, che include le autorizzazioni per il token SAS.</span><span class="sxs-lookup"><span data-stu-id="d3ca2-123">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="d3ca2-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="d3ca2-124">-StartTime</span></span>
<span data-ttu-id="d3ca2-125">Specifica il momento in cui i criteri di accesso archiviati diventano validi.</span><span class="sxs-lookup"><span data-stu-id="d3ca2-125">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="d3ca2-126">-Tabella</span><span class="sxs-lookup"><span data-stu-id="d3ca2-126">-Table</span></span>
<span data-ttu-id="d3ca2-127">Specifica il nome della tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d3ca2-127">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="d3ca2-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d3ca2-128">-Confirm</span></span>
<span data-ttu-id="d3ca2-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3ca2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3ca2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3ca2-130">-WhatIf</span></span>
<span data-ttu-id="d3ca2-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d3ca2-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d3ca2-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d3ca2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3ca2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3ca2-133">CommonParameters</span></span>
<span data-ttu-id="d3ca2-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3ca2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3ca2-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3ca2-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3ca2-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d3ca2-136">INPUTS</span></span>

## <span data-ttu-id="d3ca2-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d3ca2-137">OUTPUTS</span></span>

## <span data-ttu-id="d3ca2-138">Note</span><span class="sxs-lookup"><span data-stu-id="d3ca2-138">NOTES</span></span>

## <span data-ttu-id="d3ca2-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d3ca2-139">RELATED LINKS</span></span>

[<span data-ttu-id="d3ca2-140">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d3ca2-140">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="d3ca2-141">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="d3ca2-141">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="d3ca2-142">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d3ca2-142">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="d3ca2-143">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d3ca2-143">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)
