---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/restore-azstorageblobrange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzStorageBlobRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzStorageBlobRange.md
ms.openlocfilehash: ee8a8bd6a12d3f4aa1dc1624d0dc5c11de972b11
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479371"
---
# <span data-ttu-id="9d710-101">Restore-AzStorageBlobRange</span><span class="sxs-lookup"><span data-stu-id="9d710-101">Restore-AzStorageBlobRange</span></span>

## <span data-ttu-id="9d710-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9d710-102">SYNOPSIS</span></span>
<span data-ttu-id="9d710-103">Ripristina un account di archiviazione per intervalli di BLOB specifici.</span><span class="sxs-lookup"><span data-stu-id="9d710-103">Restores a Storage account for specific blob ranges.</span></span>

## <span data-ttu-id="9d710-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9d710-104">SYNTAX</span></span>

### <span data-ttu-id="9d710-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9d710-105">AccountName (Default)</span></span>
```
Restore-AzStorageBlobRange [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -TimeToRestore <DateTime> [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d710-106">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="9d710-106">AccountResourceId</span></span>
```
Restore-AzStorageBlobRange [-ResourceId] <String> -TimeToRestore <DateTime>
 [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d710-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="9d710-107">AccountObject</span></span>
```
Restore-AzStorageBlobRange -StorageAccount <PSStorageAccount> -TimeToRestore <DateTime>
 [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d710-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9d710-108">DESCRIPTION</span></span>
<span data-ttu-id="9d710-109">Il cmdlet **Restore-AzStorageBlobRange** Ripristina i BLOB in un account di archiviazione per specifici intervalli di BLOB.</span><span class="sxs-lookup"><span data-stu-id="9d710-109">The **Restore-AzStorageBlobRange** cmdlet restores blobs in a Storage account for specific blob ranges.</span></span>
<span data-ttu-id="9d710-110">L'intervallo di inizio è incluso e l'intervallo di fine è escluso nel ripristino BLOB.</span><span class="sxs-lookup"><span data-stu-id="9d710-110">The start range is included, and the end range is excluded in blob restore.</span></span>

## <span data-ttu-id="9d710-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9d710-111">EXAMPLES</span></span>

### <span data-ttu-id="9d710-112">Esempio 1: avviare il ripristino dei BLOB in un account di archiviazione con intervalli BLOB specifici</span><span class="sxs-lookup"><span data-stu-id="9d710-112">Example 1: Start restores blobs in a Storage account with specific blob ranges</span></span>
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

<span data-ttu-id="9d710-113">Questo comando crea prima due intervalli di BLOB, quindi avvia il ripristino di BLOB in un account di archiviazione con i 2 intervalli di BLOB di 1 giorno fa.</span><span class="sxs-lookup"><span data-stu-id="9d710-113">This command first creates 2 blob ranges, then start restores blobs in a Storage account with the 2 blob ranges from 1 day ago.</span></span> <span data-ttu-id="9d710-114">L'utente può usare Get-AzStorageAccount per rintracciare lo stato di ripristino in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="9d710-114">User can use Get-AzStorageAccount to trace the restore status later.</span></span>

### <span data-ttu-id="9d710-115">Esempio 2: Ripristina tutti i BLOB in un account di archiviazione nel backend</span><span class="sxs-lookup"><span data-stu-id="9d710-115">Example 2: Restores all blobs in a Storage account in the backend</span></span>
```powershell
PS C:\> $job = Restore-AzStorageBlobRange -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -TimeToRestore (Get-Date).AddMinutes(-30) -WaitForComplete -asjob

PS C:\> $job | Wait-Job

PS C:\> $job.Output

Status   RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges
------   ---------                            ------------- ------------------------     ---------------------
Complete 0387953a-bbe6-4602-818d-e661581ee44b               2020-08-28T07:11:33.9843100Z ["" -> ""]
```

<span data-ttu-id="9d710-116">Questo comando Ripristina tutti i BLOB in un account di archiviazione da 30 minuti fa e attende il completamento del ripristino.</span><span class="sxs-lookup"><span data-stu-id="9d710-116">This command restores all blobs in a Storage account from 30 minutes ago, and wait for the restore complete.</span></span> <span data-ttu-id="9d710-117">Poiché il ripristino dei BLOB può richiedere molto tempo, eseguirlo nel parametro backend con-AsJob e quindi attendere il completamento del processo e visualizzare il risultato.</span><span class="sxs-lookup"><span data-stu-id="9d710-117">Since restore blobs might take a long time, run it in the backend with -Asjob parameter, and then wait for the job complete and show the result.</span></span>

### <span data-ttu-id="9d710-118">Esempio 3: Ripristina i BLOB per gli intervalli di BLOB di input direttamente e attende il completamento</span><span class="sxs-lookup"><span data-stu-id="9d710-118">Example 3: Restores blobs by input blob ranges directly, and wait for complete</span></span>
```powershell
PS C:\> Restore-AzStorageBlobRange -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -WaitForComplete `
    -TimeToRestore (Get-Date).AddSeconds(-1) `
    -BlobRestoreRange @{StartRange="aaa/abc";EndRange="bbb/abc"},@{StartRange="bbb/acc";EndRange=""}
WARNING: Restore blob rang with Id 'd66d1d02-6e48-47ef-b516-0155dd8319c6' started. Restore blob ranges time to complete is dependent on the size of the restore.

Status   RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges   
------   ---------                            ------------- ------------------------     ---------------------   
Complete d66d1d02-6e48-47ef-b516-0155dd8319c6               2020-02-10T14:17:46.8189116Z ["aaa/abc" -> "bbb/abc",...]
```

<span data-ttu-id="9d710-119">Questo comando Ripristina i BLOB in un account di archiviazione da 1 giorno fa, per gli intervalli di input 2 BLOB direttamente nel cmdlet Restore-AzStorageBlobRange.</span><span class="sxs-lookup"><span data-stu-id="9d710-119">This command restores blobs in a Storage account from 1 day ago, by input 2 blob ranges directly to the Restore-AzStorageBlobRange cmdlet.</span></span> <span data-ttu-id="9d710-120">Questo comando attende il completamento del ripristino.</span><span class="sxs-lookup"><span data-stu-id="9d710-120">This command will wait for the restore complete.</span></span>

## <span data-ttu-id="9d710-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9d710-121">PARAMETERS</span></span>

### <span data-ttu-id="9d710-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9d710-122">-AsJob</span></span>
<span data-ttu-id="9d710-123">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="9d710-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9d710-124">-BlobRestoreRange</span><span class="sxs-lookup"><span data-stu-id="9d710-124">-BlobRestoreRange</span></span>
<span data-ttu-id="9d710-125">Intervallo di BLOB da ripristinare.</span><span class="sxs-lookup"><span data-stu-id="9d710-125">The blob range to Restore.</span></span>
<span data-ttu-id="9d710-126">Se non specifichi questo parametro, verranno ripristinati tutti i BLOB.</span><span class="sxs-lookup"><span data-stu-id="9d710-126">If not specify this parameter, will restore all blobs.</span></span>

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

### <span data-ttu-id="9d710-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d710-127">-DefaultProfile</span></span>
<span data-ttu-id="9d710-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9d710-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d710-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d710-129">-ResourceGroupName</span></span>
<span data-ttu-id="9d710-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9d710-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="9d710-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d710-131">-ResourceId</span></span>
<span data-ttu-id="9d710-132">ID risorsa account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="9d710-132">Storage Account Resource Id.</span></span>

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

### <span data-ttu-id="9d710-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="9d710-133">-StorageAccount</span></span>
<span data-ttu-id="9d710-134">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="9d710-134">Storage account object</span></span>

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

### <span data-ttu-id="9d710-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9d710-135">-StorageAccountName</span></span>
<span data-ttu-id="9d710-136">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="9d710-136">Storage Account Name.</span></span>

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

### <span data-ttu-id="9d710-137">-TimeToRestore</span><span class="sxs-lookup"><span data-stu-id="9d710-137">-TimeToRestore</span></span>
<span data-ttu-id="9d710-138">Il tempo necessario per ripristinare BLOB.</span><span class="sxs-lookup"><span data-stu-id="9d710-138">The Time to Restore Blob.</span></span>

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

### <span data-ttu-id="9d710-139">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="9d710-139">-WaitForComplete</span></span>
<span data-ttu-id="9d710-140">Attendere il completamento dell'attività di ripristino</span><span class="sxs-lookup"><span data-stu-id="9d710-140">Wait for Restore task complete</span></span>

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

### <span data-ttu-id="9d710-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9d710-141">-Confirm</span></span>
<span data-ttu-id="9d710-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d710-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d710-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d710-143">-WhatIf</span></span>
<span data-ttu-id="9d710-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9d710-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9d710-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9d710-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d710-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d710-146">CommonParameters</span></span>
<span data-ttu-id="9d710-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d710-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d710-148">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d710-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d710-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9d710-149">INPUTS</span></span>

### <span data-ttu-id="9d710-150">System. String</span><span class="sxs-lookup"><span data-stu-id="9d710-150">System.String</span></span>

### <span data-ttu-id="9d710-151">Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9d710-151">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="9d710-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9d710-152">OUTPUTS</span></span>

### <span data-ttu-id="9d710-153">Microsoft. Azure. Commands. Management. storage. Models. PSBlobRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="9d710-153">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreStatus</span></span>

## <span data-ttu-id="9d710-154">Note</span><span class="sxs-lookup"><span data-stu-id="9d710-154">NOTES</span></span>

## <span data-ttu-id="9d710-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9d710-155">RELATED LINKS</span></span>
