---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitemexpiry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
ms.openlocfilehash: 6908bc4d474d0dbe9df045332f3820b5f7536dac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519473"
---
# <span data-ttu-id="e56f9-101">Set-AzureRmDataLakeStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="e56f9-101">Set-AzureRmDataLakeStoreItemExpiry</span></span>

## <span data-ttu-id="e56f9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e56f9-102">SYNOPSIS</span></span>
<span data-ttu-id="e56f9-103">Imposta o rimuove il tempo di scadenza per un file in un account di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e56f9-103">Sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e56f9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e56f9-104">SYNTAX</span></span>

### <span data-ttu-id="e56f9-105">SetAbsoluteNeverExpireExpiry (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e56f9-105">SetAbsoluteNeverExpireExpiry (Default)</span></span>
```
Set-AzureRmDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-Expiration] <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e56f9-106">SetRelativeExpiry</span><span class="sxs-lookup"><span data-stu-id="e56f9-106">SetRelativeExpiry</span></span>
```
Set-AzureRmDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-RelativeFileExpiryOption] <PathRelativeExpiryOptions>] [[-RelativeTime] <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e56f9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e56f9-107">DESCRIPTION</span></span>
<span data-ttu-id="e56f9-108">Il cmdlet **set-AzureRmDataLakeStoreItemExpiry** imposta o rimuove il tempo di scadenza per un file in un account di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e56f9-108">The **Set-AzureRmDataLakeStoreItemExpiry** cmdlet sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="e56f9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e56f9-109">EXAMPLES</span></span>

### <span data-ttu-id="e56f9-110">Esempio 1: impostare la data di scadenza per un file</span><span class="sxs-lookup"><span data-stu-id="e56f9-110">Example 1: Set the expiration time for a file</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt -Expiration [DateTimeOffset]::Now.AddHours(2)
```

<span data-ttu-id="e56f9-111">Imposta la scadenza nel file myfile.txt in account ContosoADL da due ore da ora.</span><span class="sxs-lookup"><span data-stu-id="e56f9-111">Sets expiration on the file myfile.txt in account ContosoADL to be two hours from now.</span></span>
<span data-ttu-id="e56f9-112">In questo modo il file scadrà (contrassegnato per Delete) in due ore.</span><span class="sxs-lookup"><span data-stu-id="e56f9-112">This will cause the file to expire (be marked for delete) in two hours.</span></span>

### <span data-ttu-id="e56f9-113">Esempio 2: rimuovere la scadenza in un file</span><span class="sxs-lookup"><span data-stu-id="e56f9-113">Example 2: Remove the expiration on a file</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt
```

<span data-ttu-id="e56f9-114">Rimuove la scadenza precedentemente impostata sul file "myfile.txt" nell'account "ContosoADL".</span><span class="sxs-lookup"><span data-stu-id="e56f9-114">Removes any expiration that was previously set on file 'myfile.txt' in account 'ContosoADL'.</span></span>
<span data-ttu-id="e56f9-115">Questo significa che il file non scadrà automaticamente (da contrassegnare per l'eliminazione) e dovrà essere eliminato manualmente o impostato in modo che scada di nuovo.</span><span class="sxs-lookup"><span data-stu-id="e56f9-115">This means the file will not automatically expire (be marked for delete) and will need to be manually deleted or set to expire again.</span></span>


### <span data-ttu-id="e56f9-116">Esempio 3: impostare la data di scadenza per un file relativo a Now</span><span class="sxs-lookup"><span data-stu-id="e56f9-116">Example 3: Set expiration time for a file relative to now</span></span>
```
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToNow -RelativeTime 240000
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToCreationDate -RelativeTime 240000
```

<span data-ttu-id="e56f9-117">Il primo comando imposta la data di scadenza del file/myfile.txt 240 secondi rispetto all'ora corrente al server.</span><span class="sxs-lookup"><span data-stu-id="e56f9-117">The first command sets the expiration time of the file /myfile.txt 240 seconds relative to current time at server.</span></span>

<span data-ttu-id="e56f9-118">Il secondo comando imposta la data di scadenza del file/myfile.txt 240 secondi rispetto all'ora di creazione nel server.</span><span class="sxs-lookup"><span data-stu-id="e56f9-118">The second command sets the expiration time of the file /myfile.txt 240 seconds relative to creation time at server.</span></span>

## <span data-ttu-id="e56f9-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e56f9-119">PARAMETERS</span></span>

### <span data-ttu-id="e56f9-120">-Account</span><span class="sxs-lookup"><span data-stu-id="e56f9-120">-Account</span></span>
<span data-ttu-id="e56f9-121">Specifica il nome dell'account Store Data Lake.</span><span class="sxs-lookup"><span data-stu-id="e56f9-121">Specifies the Data Lake Store account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e56f9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e56f9-122">-DefaultProfile</span></span>
<span data-ttu-id="e56f9-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e56f9-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e56f9-124">-Scadenza</span><span class="sxs-lookup"><span data-stu-id="e56f9-124">-Expiration</span></span>
<span data-ttu-id="e56f9-125">Ora di scadenza assoluta per il file specificato.</span><span class="sxs-lookup"><span data-stu-id="e56f9-125">The absolute expiration time for the specified file.</span></span>
<span data-ttu-id="e56f9-126">Se nessun valore o impostato su MaxValue, il file non scadrà mai.</span><span class="sxs-lookup"><span data-stu-id="e56f9-126">If no value or set to MaxValue, the file will never expire.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: Set expiry as Absolute or NeverExpire
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e56f9-127">-RelativeFileExpiryOption</span><span class="sxs-lookup"><span data-stu-id="e56f9-127">-RelativeFileExpiryOption</span></span>
<span data-ttu-id="e56f9-128">Opzioni relative alla scadenza.</span><span class="sxs-lookup"><span data-stu-id="e56f9-128">Relative expiry options.</span></span> <span data-ttu-id="e56f9-129">RelativeToNow o RelativeToCreationDate sono opzioni correnti</span><span class="sxs-lookup"><span data-stu-id="e56f9-129">RelativeToNow or RelativeToCreationDate are current options</span></span>
```yaml
Type: PathRelativeExpiryOptions
Parameter Sets: Set expiry as relative to creation or now
Aliases: 
Accepted values: RelativeToNow, RelativeToCreationDate

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e56f9-130">-Path</span><span class="sxs-lookup"><span data-stu-id="e56f9-130">-Path</span></span>
<span data-ttu-id="e56f9-131">Specifica il percorso dello Store Data Lake dell'elemento file per il quale impostare o rimuovere la scadenza.</span><span class="sxs-lookup"><span data-stu-id="e56f9-131">Specifies the Data Lake Store path of the file item for which to set or remove expiry.</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e56f9-132">-RelativeTime</span><span class="sxs-lookup"><span data-stu-id="e56f9-132">-RelativeTime</span></span>
<span data-ttu-id="e56f9-133">Il tempo relativo in millisecondi rispetto a ora o alla data di creazione</span><span class="sxs-lookup"><span data-stu-id="e56f9-133">The relative time in milliseconds with respect to now or creation time</span></span>
```yaml
Type: Int64
Parameter Sets: Set expiry as relative to creation or now
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e56f9-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e56f9-134">-Confirm</span></span>
<span data-ttu-id="e56f9-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e56f9-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e56f9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e56f9-136">-WhatIf</span></span>
<span data-ttu-id="e56f9-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e56f9-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e56f9-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e56f9-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e56f9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e56f9-139">CommonParameters</span></span>
<span data-ttu-id="e56f9-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e56f9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e56f9-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e56f9-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e56f9-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e56f9-142">INPUTS</span></span>

### <span data-ttu-id="e56f9-143">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e56f9-143">None</span></span>
<span data-ttu-id="e56f9-144">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="e56f9-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e56f9-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e56f9-145">OUTPUTS</span></span>

### <span data-ttu-id="e56f9-146">DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e56f9-146">DataLakeStoreItem</span></span>
<span data-ttu-id="e56f9-147">Il file aggiornato con una nuova data di scadenza.</span><span class="sxs-lookup"><span data-stu-id="e56f9-147">The updated file with a new expiration time.</span></span>

## <span data-ttu-id="e56f9-148">Note</span><span class="sxs-lookup"><span data-stu-id="e56f9-148">NOTES</span></span>
<span data-ttu-id="e56f9-149">Alias: Set-AdlStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="e56f9-149">Alias: Set-AdlStoreItemExpiry</span></span>

## <span data-ttu-id="e56f9-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e56f9-150">RELATED LINKS</span></span>

[<span data-ttu-id="e56f9-151">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e56f9-151">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

