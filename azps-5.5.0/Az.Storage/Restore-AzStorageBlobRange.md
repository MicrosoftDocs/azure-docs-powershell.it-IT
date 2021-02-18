---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/restore-azstorageblobrange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzStorageBlobRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzStorageBlobRange.md
ms.openlocfilehash: ee8a8bd6a12d3f4aa1dc1624d0dc5c11de972b11
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190727"
---
# <span data-ttu-id="715de-101">Restore-AzStorageBlobRange</span><span class="sxs-lookup"><span data-stu-id="715de-101">Restore-AzStorageBlobRange</span></span>

## <span data-ttu-id="715de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="715de-102">SYNOPSIS</span></span>
<span data-ttu-id="715de-103">Ripristina un account di archiviazione per intervalli BLOB specifici.</span><span class="sxs-lookup"><span data-stu-id="715de-103">Restores a Storage account for specific blob ranges.</span></span>

## <span data-ttu-id="715de-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="715de-104">SYNTAX</span></span>

### <span data-ttu-id="715de-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="715de-105">AccountName (Default)</span></span>
```
Restore-AzStorageBlobRange [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -TimeToRestore <DateTime> [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="715de-106">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="715de-106">AccountResourceId</span></span>
```
Restore-AzStorageBlobRange [-ResourceId] <String> -TimeToRestore <DateTime>
 [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="715de-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="715de-107">AccountObject</span></span>
```
Restore-AzStorageBlobRange -StorageAccount <PSStorageAccount> -TimeToRestore <DateTime>
 [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="715de-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="715de-108">DESCRIPTION</span></span>
<span data-ttu-id="715de-109">Il cmdlet **Restore-AzStorageBlobRange** ripristina i BLOB in un account di archiviazione per intervalli BLOB specifici.</span><span class="sxs-lookup"><span data-stu-id="715de-109">The **Restore-AzStorageBlobRange** cmdlet restores blobs in a Storage account for specific blob ranges.</span></span>
<span data-ttu-id="715de-110">L'intervallo iniziale è incluso e l'intervallo finale escluso in Ripristino BLOB.</span><span class="sxs-lookup"><span data-stu-id="715de-110">The start range is included, and the end range is excluded in blob restore.</span></span>

## <span data-ttu-id="715de-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="715de-111">EXAMPLES</span></span>

### <span data-ttu-id="715de-112">Esempio 1: Avviare il ripristino di BLOB in un account di archiviazione con intervalli BLOB specifici</span><span class="sxs-lookup"><span data-stu-id="715de-112">Example 1: Start restores blobs in a Storage account with specific blob ranges</span></span>
```powershell
PS C:\> $range1 = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
PS C:\> $range2 = New-AzStorageBlobRangeToRestore -StartRange container3/blob3 -EndRange container4/blob4
PS C:\> Restore-AzStorageBlobRange -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -TimeToRestore (Get-Date).AddDays(-1) -BlobRestoreRange $range1,$range2

Status     RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges                     
------     ---------                            ------------- ------------------------     ---------------------                     
InProgress 6ca55a8b-fca0-461a-8e4c-13927a9707e6               2020-02-10T13:58:44.6841810Z ["container1/blob1" -> "container2/blob2",...]

PS C:\> (Get-AzStorageAccount -ResourceGroupName $rgname -StorageAccountName $accountName -IncludeBlobRestoreStatus).BlobRestoreStatus 

Status   RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges                     
------   ---------                            ------------- ------------------------     ---------------------                     
Complete 6ca55a8b-fca0-461a-8e4c-13927a9707e6               2020-02-10T13:58:44.6841810Z ["container1/blob1" -> "container2/blob2",...]
```

<span data-ttu-id="715de-113">Questo comando crea prima 2 intervalli di BLOB, quindi avvia il ripristino dei BLOB in un account di archiviazione con i 2 intervalli di BLOB di 1 giorno fa.</span><span class="sxs-lookup"><span data-stu-id="715de-113">This command first creates 2 blob ranges, then start restores blobs in a Storage account with the 2 blob ranges from 1 day ago.</span></span> <span data-ttu-id="715de-114">L'utente può usare Get-AzStorageAccount per tracciare lo stato di ripristino in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="715de-114">User can use Get-AzStorageAccount to trace the restore status later.</span></span>

### <span data-ttu-id="715de-115">Esempio 2: Ripristina tutti i BLOB in un account di archiviazione nel back-end</span><span class="sxs-lookup"><span data-stu-id="715de-115">Example 2: Restores all blobs in a Storage account in the backend</span></span>
```powershell
PS C:\> $job = Restore-AzStorageBlobRange -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -TimeToRestore (Get-Date).AddMinutes(-30) -WaitForComplete -asjob

PS C:\> $job | Wait-Job

PS C:\> $job.Output

Status   RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges
------   ---------                            ------------- ------------------------     ---------------------
Complete 0387953a-bbe6-4602-818d-e661581ee44b               2020-08-28T07:11:33.9843100Z ["" -> ""]
```

<span data-ttu-id="715de-116">Questo comando ripristina tutti i BLOB in un account di archiviazione da 30 minuti fa e attende il completamento del ripristino.</span><span class="sxs-lookup"><span data-stu-id="715de-116">This command restores all blobs in a Storage account from 30 minutes ago, and wait for the restore complete.</span></span> <span data-ttu-id="715de-117">Poiché il ripristino dei BLOB potrebbe richiedere molto tempo, eseguirlo nel back-end con il parametro -Asjob e quindi attendere il completamento del processo e visualizzare il risultato.</span><span class="sxs-lookup"><span data-stu-id="715de-117">Since restore blobs might take a long time, run it in the backend with -Asjob parameter, and then wait for the job complete and show the result.</span></span>

### <span data-ttu-id="715de-118">Esempio 3: Ripristina direttamente i BLOB in base a intervalli BLOB di input e attendi il completamento</span><span class="sxs-lookup"><span data-stu-id="715de-118">Example 3: Restores blobs by input blob ranges directly, and wait for complete</span></span>
```powershell
PS C:\> Restore-AzStorageBlobRange -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -WaitForComplete `
    -TimeToRestore (Get-Date).AddSeconds(-1) `
    -BlobRestoreRange @{StartRange="aaa/abc";EndRange="bbb/abc"},@{StartRange="bbb/acc";EndRange=""}
WARNING: Restore blob rang with Id 'd66d1d02-6e48-47ef-b516-0155dd8319c6' started. Restore blob ranges time to complete is dependent on the size of the restore.

Status   RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges   
------   ---------                            ------------- ------------------------     ---------------------   
Complete d66d1d02-6e48-47ef-b516-0155dd8319c6               2020-02-10T14:17:46.8189116Z ["aaa/abc" -> "bbb/abc",...]
```

<span data-ttu-id="715de-119">Questo comando ripristina i BLOB in un account di archiviazione da 1 giorno prima, input 2 intervalli BLOB direttamente nel cmdlet Restore-AzStorageBlobRange archiviazione.</span><span class="sxs-lookup"><span data-stu-id="715de-119">This command restores blobs in a Storage account from 1 day ago, by input 2 blob ranges directly to the Restore-AzStorageBlobRange cmdlet.</span></span> <span data-ttu-id="715de-120">Questo comando attenderà il completamento del ripristino.</span><span class="sxs-lookup"><span data-stu-id="715de-120">This command will wait for the restore complete.</span></span>

## <span data-ttu-id="715de-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="715de-121">PARAMETERS</span></span>

### <span data-ttu-id="715de-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="715de-122">-AsJob</span></span>
<span data-ttu-id="715de-123">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="715de-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="715de-124">-BlobRestoreRange</span><span class="sxs-lookup"><span data-stu-id="715de-124">-BlobRestoreRange</span></span>
<span data-ttu-id="715de-125">Intervallo BLOB da ripristinare.</span><span class="sxs-lookup"><span data-stu-id="715de-125">The blob range to Restore.</span></span>
<span data-ttu-id="715de-126">Se non si specifica questo parametro, verranno ripristinati tutti i BLOB.</span><span class="sxs-lookup"><span data-stu-id="715de-126">If not specify this parameter, will restore all blobs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="715de-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="715de-127">-DefaultProfile</span></span>
<span data-ttu-id="715de-128">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="715de-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="715de-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="715de-129">-ResourceGroupName</span></span>
<span data-ttu-id="715de-130">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="715de-130">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="715de-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="715de-131">-ResourceId</span></span>
<span data-ttu-id="715de-132">ID risorsa account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="715de-132">Storage Account Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="715de-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="715de-133">-StorageAccount</span></span>
<span data-ttu-id="715de-134">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="715de-134">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="715de-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="715de-135">-StorageAccountName</span></span>
<span data-ttu-id="715de-136">Nome account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="715de-136">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="715de-137">-TimeToRestore</span><span class="sxs-lookup"><span data-stu-id="715de-137">-TimeToRestore</span></span>
<span data-ttu-id="715de-138">Ora di ripristino blob.</span><span class="sxs-lookup"><span data-stu-id="715de-138">The Time to Restore Blob.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="715de-139">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="715de-139">-WaitForComplete</span></span>
<span data-ttu-id="715de-140">Attendere il completamento dell'attività di ripristino</span><span class="sxs-lookup"><span data-stu-id="715de-140">Wait for Restore task complete</span></span>

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

### <span data-ttu-id="715de-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="715de-141">-Confirm</span></span>
<span data-ttu-id="715de-142">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="715de-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="715de-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="715de-143">-WhatIf</span></span>
<span data-ttu-id="715de-144">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="715de-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="715de-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="715de-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="715de-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="715de-146">CommonParameters</span></span>
<span data-ttu-id="715de-147">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="715de-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="715de-148">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="715de-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="715de-149">INPUT</span><span class="sxs-lookup"><span data-stu-id="715de-149">INPUTS</span></span>

### <span data-ttu-id="715de-150">System.String</span><span class="sxs-lookup"><span data-stu-id="715de-150">System.String</span></span>

### <span data-ttu-id="715de-151">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="715de-151">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="715de-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="715de-152">OUTPUTS</span></span>

### <span data-ttu-id="715de-153">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="715de-153">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreStatus</span></span>

## <span data-ttu-id="715de-154">NOTE</span><span class="sxs-lookup"><span data-stu-id="715de-154">NOTES</span></span>

## <span data-ttu-id="715de-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="715de-155">RELATED LINKS</span></span>
