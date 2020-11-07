---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemexpiry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemExpiry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemExpiry.md
ms.openlocfilehash: 074e6224c7a5b1ea1e8039901b75d223581495d7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684512"
---
# <span data-ttu-id="2aa02-101">Set-AzDataLakeStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="2aa02-101">Set-AzDataLakeStoreItemExpiry</span></span>

## <span data-ttu-id="2aa02-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2aa02-102">SYNOPSIS</span></span>
<span data-ttu-id="2aa02-103">Imposta o rimuove il tempo di scadenza per un file in un account di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2aa02-103">Sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="2aa02-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2aa02-104">SYNTAX</span></span>

### <span data-ttu-id="2aa02-105">SetAbsoluteNeverExpireExpiry (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2aa02-105">SetAbsoluteNeverExpireExpiry (Default)</span></span>
```
Set-AzDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-Expiration] <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2aa02-106">SetRelativeExpiry</span><span class="sxs-lookup"><span data-stu-id="2aa02-106">SetRelativeExpiry</span></span>
```
Set-AzDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-RelativeFileExpiryOption] <PathRelativeExpiryOptions> [[-RelativeTime] <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2aa02-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2aa02-107">DESCRIPTION</span></span>
<span data-ttu-id="2aa02-108">Il cmdlet **set-AzDataLakeStoreItemExpiry** imposta o rimuove il tempo di scadenza per un file in un account di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2aa02-108">The **Set-AzDataLakeStoreItemExpiry** cmdlet sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="2aa02-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2aa02-109">EXAMPLES</span></span>

### <span data-ttu-id="2aa02-110">Esempio 1: impostare la data di scadenza per un file</span><span class="sxs-lookup"><span data-stu-id="2aa02-110">Example 1: Set the expiration time for a file</span></span>
```
PS C:\> Set-AzDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt -Expiration [DateTimeOffset]::Now.AddHours(2)
```

<span data-ttu-id="2aa02-111">Imposta la scadenza nel file myfile.txt in account ContosoADL da due ore da ora.</span><span class="sxs-lookup"><span data-stu-id="2aa02-111">Sets expiration on the file myfile.txt in account ContosoADL to be two hours from now.</span></span>
<span data-ttu-id="2aa02-112">In questo modo il file scadrà (contrassegnato per Delete) in due ore.</span><span class="sxs-lookup"><span data-stu-id="2aa02-112">This will cause the file to expire (be marked for delete) in two hours.</span></span>

### <span data-ttu-id="2aa02-113">Esempio 2: rimuovere la scadenza in un file</span><span class="sxs-lookup"><span data-stu-id="2aa02-113">Example 2: Remove the expiration on a file</span></span>
```
PS C:\> Set-AzDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt
```

<span data-ttu-id="2aa02-114">Rimuove la scadenza precedentemente impostata sul file "myfile.txt" nell'account "ContosoADL".</span><span class="sxs-lookup"><span data-stu-id="2aa02-114">Removes any expiration that was previously set on file 'myfile.txt' in account 'ContosoADL'.</span></span>
<span data-ttu-id="2aa02-115">Questo significa che il file non scadrà automaticamente (da contrassegnare per l'eliminazione) e dovrà essere eliminato manualmente o impostato in modo che scada di nuovo.</span><span class="sxs-lookup"><span data-stu-id="2aa02-115">This means the file will not automatically expire (be marked for delete) and will need to be manually deleted or set to expire again.</span></span>

### <span data-ttu-id="2aa02-116">Esempio 3: impostare la data di scadenza per un file relativo a Now</span><span class="sxs-lookup"><span data-stu-id="2aa02-116">Example 3: Set expiration time for a file relative to now</span></span>
```
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToNow -RelativeTime 240000
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToCreationDate -RelativeTime 240000
```

<span data-ttu-id="2aa02-117">Il primo comando imposta la data di scadenza del file/myfile.txt 240 secondi rispetto all'ora corrente al server.</span><span class="sxs-lookup"><span data-stu-id="2aa02-117">The first command sets the expiration time of the file /myfile.txt 240 seconds relative to current time at server.</span></span>
<span data-ttu-id="2aa02-118">Il secondo comando imposta la data di scadenza del file/myfile.txt 240 secondi rispetto all'ora di creazione nel server.</span><span class="sxs-lookup"><span data-stu-id="2aa02-118">The second command sets the expiration time of the file /myfile.txt 240 seconds relative to creation time at server.</span></span>

## <span data-ttu-id="2aa02-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2aa02-119">PARAMETERS</span></span>

### <span data-ttu-id="2aa02-120">-Account</span><span class="sxs-lookup"><span data-stu-id="2aa02-120">-Account</span></span>
<span data-ttu-id="2aa02-121">Specifica il nome dell'account Store Data Lake.</span><span class="sxs-lookup"><span data-stu-id="2aa02-121">Specifies the Data Lake Store account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2aa02-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2aa02-122">-DefaultProfile</span></span>
<span data-ttu-id="2aa02-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2aa02-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aa02-124">-Scadenza</span><span class="sxs-lookup"><span data-stu-id="2aa02-124">-Expiration</span></span>
<span data-ttu-id="2aa02-125">Ora di scadenza assoluta per il file specificato.</span><span class="sxs-lookup"><span data-stu-id="2aa02-125">The absolute expiration time for the specified file.</span></span>
<span data-ttu-id="2aa02-126">Se nessun valore o impostato su MaxValue, il file non scadrà mai.</span><span class="sxs-lookup"><span data-stu-id="2aa02-126">If no value or set to MaxValue, the file will never expire.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: SetAbsoluteNeverExpireExpiry
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2aa02-127">-Path</span><span class="sxs-lookup"><span data-stu-id="2aa02-127">-Path</span></span>
<span data-ttu-id="2aa02-128">Specifica il percorso dello Store Data Lake dell'elemento file per il quale impostare o rimuovere la scadenza.</span><span class="sxs-lookup"><span data-stu-id="2aa02-128">Specifies the Data Lake Store path of the file item for which to set or remove expiry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2aa02-129">-RelativeFileExpiryOption</span><span class="sxs-lookup"><span data-stu-id="2aa02-129">-RelativeFileExpiryOption</span></span>
<span data-ttu-id="2aa02-130">Opzioni relative alla scadenza.</span><span class="sxs-lookup"><span data-stu-id="2aa02-130">Relative expiry options.</span></span> <span data-ttu-id="2aa02-131">RelativeToNow o RelativeToCreationDate sono opzioni correnti</span><span class="sxs-lookup"><span data-stu-id="2aa02-131">RelativeToNow or RelativeToCreationDate are current options</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathRelativeExpiryOptions
Parameter Sets: SetRelativeExpiry
Aliases:
Accepted values: RelativeToNow, RelativeToCreationDate

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2aa02-132">-RelativeTime</span><span class="sxs-lookup"><span data-stu-id="2aa02-132">-RelativeTime</span></span>
<span data-ttu-id="2aa02-133">Il tempo relativo in millisecondi rispetto a ora o alla data di creazione</span><span class="sxs-lookup"><span data-stu-id="2aa02-133">The relative time in milliseconds with respect to now or creation time</span></span>

```yaml
Type: System.Int64
Parameter Sets: SetRelativeExpiry
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2aa02-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2aa02-134">-Confirm</span></span>
<span data-ttu-id="2aa02-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2aa02-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2aa02-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2aa02-136">-WhatIf</span></span>
<span data-ttu-id="2aa02-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2aa02-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2aa02-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2aa02-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2aa02-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aa02-139">CommonParameters</span></span>
<span data-ttu-id="2aa02-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2aa02-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aa02-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2aa02-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aa02-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2aa02-142">INPUTS</span></span>

### <span data-ttu-id="2aa02-143">System. String</span><span class="sxs-lookup"><span data-stu-id="2aa02-143">System.String</span></span>

### <span data-ttu-id="2aa02-144">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="2aa02-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="2aa02-145">System. DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2aa02-145">System.DateTimeOffset</span></span>

### <span data-ttu-id="2aa02-146">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreEnums + PathRelativeExpiryOptions</span><span class="sxs-lookup"><span data-stu-id="2aa02-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathRelativeExpiryOptions</span></span>

### <span data-ttu-id="2aa02-147">System. Int64</span><span class="sxs-lookup"><span data-stu-id="2aa02-147">System.Int64</span></span>

## <span data-ttu-id="2aa02-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2aa02-148">OUTPUTS</span></span>

### <span data-ttu-id="2aa02-149">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2aa02-149">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="2aa02-150">Note</span><span class="sxs-lookup"><span data-stu-id="2aa02-150">NOTES</span></span>
<span data-ttu-id="2aa02-151">Alias: Set-AdlStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="2aa02-151">Alias: Set-AdlStoreItemExpiry</span></span>

## <span data-ttu-id="2aa02-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2aa02-152">RELATED LINKS</span></span>

[<span data-ttu-id="2aa02-153">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2aa02-153">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

