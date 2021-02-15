---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azdatalakegen2aclrecursive
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2AclRecursive.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2AclRecursive.md
ms.openlocfilehash: 25b1c275aeed7ca56c4c2b873bdf4b9a79eb756b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195695"
---
# <span data-ttu-id="b262b-101">Set-AzDataLakeGen2AclRecursive</span><span class="sxs-lookup"><span data-stu-id="b262b-101">Set-AzDataLakeGen2AclRecursive</span></span>

## <span data-ttu-id="b262b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b262b-102">SYNOPSIS</span></span>
<span data-ttu-id="b262b-103">Impostare ACL in modo ricorsivo nel percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="b262b-103">Set ACL recursively on the specified path.</span></span> 

## <span data-ttu-id="b262b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b262b-104">SYNTAX</span></span>

```
Set-AzDataLakeGen2AclRecursive [-FileSystem] <String> [[-Path] <String>] [-ContinuationToken <String>]
 -Acl <PSPathAccessControlEntry[]> [-ContinueOnFailure] [-BatchSize <Int32>] [-MaxBatchCount <Int32>] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b262b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b262b-105">DESCRIPTION</span></span>
<span data-ttu-id="b262b-106">Il cmdlet **Set-AzDataLakeGen2AclRecursive** imposta L'ACL in modo ricorsivo nel percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="b262b-106">The **Set-AzDataLakeGen2AclRecursive** cmdlet sets ACL recursively on the specified path.</span></span> <span data-ttu-id="b262b-107">L'ACL di input sostituirà completamente l'ACL originale.</span><span class="sxs-lookup"><span data-stu-id="b262b-107">The input ACL will replace original ACL completely.</span></span>

## <span data-ttu-id="b262b-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b262b-108">EXAMPLES</span></span>

### <span data-ttu-id="b262b-109">Esempio 1: Impostare ACL in modo ricorsivo in una directory</span><span class="sxs-lookup"><span data-stu-id="b262b-109">Example 1: Set ACL recursively on a directory</span></span>
```
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\> Set-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl -Context $ctx

FailedEntries                   : 
TotalDirectoriesSuccessfulCount : 7
TotalFilesSuccessfulCount       : 5
TotalFailureCount               : 0
ContinuationToken               :
```

<span data-ttu-id="b262b-110">Questo comando crea prima un oggetto ACL con 3 voci di acl, quindi imposta L'ACL in modo ricorsivo in una directory.</span><span class="sxs-lookup"><span data-stu-id="b262b-110">This command first creates an ACL object with 3 acl entries, then sets ACL recursively on a directory.</span></span>

### <span data-ttu-id="b262b-111">Esempio 2: Impostare ACL in modo ricorsivo in una directory radice del filesystem</span><span class="sxs-lookup"><span data-stu-id="b262b-111">Example 2: Set ACL recursively on a root directory of filesystem</span></span>
```
PS C:\> $result = Set-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Acl $acl  -Context $ctx

PS C:\> $result

FailedEntries                   : {dir1/dir2/file4}
TotalDirectoriesSuccessfulCount : 500
TotalFilesSuccessfulCount       : 2500
TotalFailureCount               : 1
ContinuationToken               : VBaHi5TfyO2ai1wYTRhIL2FjbGNibjA2c3RmATAxRDVEN0UzRENFQzZCRTAvYWRsc3Rlc3QyATAxRDY2M0ZCQTZBN0JGQTkvZGlyMC9kaXIxL2ZpbGUzFgAAAA==

PS C:\> $result.FailedEntries

Name            IsDirectory ErrorMessage                                                                   
----            ----------- ------------                                                                   
dir0/dir2/file4       False This request is not authorized to perform this operation using this permission.

# user need fix the failed item , then can resume with ContinuationToken

PS C:\> $result = Set-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Acl $acl -ContinuationToken $result.ContinuationToken -Context $ctx

PS C:\> $result

FailedEntries                   : 
TotalDirectoriesSuccessfulCount : 100
TotalFilesSuccessfulCount       : 1000
TotalFailureCount               : 0
ContinuationToken               :
```

<span data-ttu-id="b262b-112">Questo comando imposta prima in modo ricorsivo l'ACL su una directory radice e non è riuscito, quindi riprende con ContinuationToken dopo che l'utente ha corretto il file non riuscito.</span><span class="sxs-lookup"><span data-stu-id="b262b-112">This command first sets ACL recursively to a root directory and failed, then resume with ContinuationToken after user fix the failed file.</span></span>

### <span data-ttu-id="b262b-113">Esempio 3: Impostare L'ACL in modo ricorsivo blocco per blocco</span><span class="sxs-lookup"><span data-stu-id="b262b-113">Example 3: Set ACL recursively chunk by chunk</span></span>
```
$token = $null
$TotalDirectoriesSuccess = 0
$TotalFilesSuccess = 0
$totalFailure = 0
$FailedEntries = New-Object System.Collections.Generic.List[System.Object]
do
{
    $result = Set-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -BatchSize 100 -MaxBatchCount 2 -ContinuationToken $token -Context $ctx

    # echo $result
    $TotalFilesSuccess += $result.TotalFilesSuccessfulCount
    $TotalDirectoriesSuccess += $result.TotalDirectoriesSuccessfulCount
    $totalFailure += $result.TotalFailureCount
    $FailedEntries += $result.FailedEntries
    $token = $result.ContinuationToken
}while (($token -ne $null) -and ($result.TotalFailureCount -eq 0))
echo ""
echo "[Result Summary]"
echo "TotalDirectoriesSuccessfulCount: `t$($TotalDirectoriesSuccess)"
echo "TotalFilesSuccessfulCount: `t`t`t$($TotalFilesSuccess)"
echo "TotalFailureCount: `t`t`t`t`t$($totalFailure)"
echo "ContinuationToken: `t`t`t`t`t$($token)"
echo "FailedEntries:"$($FailedEntries | ft)
```

<span data-ttu-id="b262b-114">Questo script imposta l'ACL in modo che blocchi per blocco della directory, con dimensioni dei blocchi come BatchSize \* MaxBatchCount.</span><span class="sxs-lookup"><span data-stu-id="b262b-114">This script sets ACL rescursively on directory chunk by chunk, with chunk size as BatchSize \* MaxBatchCount.</span></span> <span data-ttu-id="b262b-115">La dimensione dei blocchi è 200 in questo script.</span><span class="sxs-lookup"><span data-stu-id="b262b-115">Chunk size is 200 in this script.</span></span>

### <span data-ttu-id="b262b-116">Esempio 4: Impostare L'ACL in modo ricorsivo in una directory e ContinueOnFailure, quindi riprendere dagli errori uno alla volta</span><span class="sxs-lookup"><span data-stu-id="b262b-116">Example 4: Set ACL recursively on a directory and ContinueOnFailure, then resume from failures one by one</span></span>
```
PS C:\> $result = Set-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl -ContinueOnFailure -Context $ctx

PS C:\> $result

FailedEntries                   : {dir0/dir1/file1, dir0/dir2/file4}
TotalDirectoriesSuccessfulCount : 100
TotalFilesSuccessfulCount       : 500
TotalFailureCount               : 2
ContinuationToken               : VBaHi5TfyO2ai1wYTRhIL2FjbGNibjA2c3RmATAxRDVEN0UzRENFQzZCRTAvYWRsc3Rlc3QyATAxRDY2M0ZCQTZBN0JGQTkvZGlyMC9kaXIxL2ZpbGUzFgAAAA==

PS C:\> $result.FailedEntries

Name            IsDirectory ErrorMessage                                                                   
----            ----------- ------------                                                                   
dir0/dir1/file1       False This request is not authorized to perform this operation using this permission.
dir0/dir2/file4       False This request is not authorized to perform this operation using this permission.

# user need fix the failed item , then can resume with ContinuationToken

PS C:\> foreach ($path in $result.FailedEntries.Name)
        {
            # user code to fix failed entry in $path
            
            #set ACL again
            Set-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path $path -Acl $acl -Context $ctx
        }
```

<span data-ttu-id="b262b-117">Questo comando imposta prima in modo ricorsivo l'ACL su una directory con ContinueOnFailure e alcuni elementi non sono riusciti, quindi riprende gli elementi non riusciti uno alla volta.</span><span class="sxs-lookup"><span data-stu-id="b262b-117">This command first sets ACL recursively to a directory with ContinueOnFailure, and some items failed, then resume the failed items one by one.</span></span>

## <span data-ttu-id="b262b-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b262b-118">PARAMETERS</span></span>

### <span data-ttu-id="b262b-119">-Acl</span><span class="sxs-lookup"><span data-stu-id="b262b-119">-Acl</span></span>
<span data-ttu-id="b262b-120">Elenco di controllo di accesso POSIX da impostare in modo ricorsivo per il file o la directory.</span><span class="sxs-lookup"><span data-stu-id="b262b-120">The POSIX access control list to set recursively for the file or directory.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b262b-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b262b-121">-AsJob</span></span>
<span data-ttu-id="b262b-122">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="b262b-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b262b-123">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="b262b-123">-BatchSize</span></span>
<span data-ttu-id="b262b-124">Se le dimensioni del set di dati superano le dimensioni del batch, l'operazione verrà suddivisa in più richieste in modo che sia possibile tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="b262b-124">If data set size exceeds batch size then operation will be split into multiple requests so that progress can be tracked.</span></span>
<span data-ttu-id="b262b-125">La dimensione del batch deve essere compresa tra 1 e 2000.</span><span class="sxs-lookup"><span data-stu-id="b262b-125">Batch size should be between 1 and 2000.</span></span>
<span data-ttu-id="b262b-126">L'impostazione predefinita è 2000.</span><span class="sxs-lookup"><span data-stu-id="b262b-126">Default is 2000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b262b-127">-Context</span><span class="sxs-lookup"><span data-stu-id="b262b-127">-Context</span></span>
<span data-ttu-id="b262b-128">Oggetto contesto archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="b262b-128">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="b262b-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="b262b-129">-ContinuationToken</span></span>
<span data-ttu-id="b262b-130">Token di continuazione.</span><span class="sxs-lookup"><span data-stu-id="b262b-130">Continuation Token.</span></span>

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

### <span data-ttu-id="b262b-131">-ContinueOnFailure</span><span class="sxs-lookup"><span data-stu-id="b262b-131">-ContinueOnFailure</span></span>
<span data-ttu-id="b262b-132">Impostare questo parametro in modo da ignorare gli errori e continuare la procezione con l'operazione su altre entità secondarie della directory.</span><span class="sxs-lookup"><span data-stu-id="b262b-132">Set this parameter to ignore failures and continue proceeing with the operation on other sub-entities of the directory.</span></span> <span data-ttu-id="b262b-133">Per impostazione predefinita, l'operazione si interromperà rapidamente in caso di errori.</span><span class="sxs-lookup"><span data-stu-id="b262b-133">Default the operation will terminate quickly on encountering failures.</span></span>

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

### <span data-ttu-id="b262b-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b262b-134">-DefaultProfile</span></span>
<span data-ttu-id="b262b-135">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b262b-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b262b-136">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="b262b-136">-FileSystem</span></span>
<span data-ttu-id="b262b-137">Nome filesystem</span><span class="sxs-lookup"><span data-stu-id="b262b-137">FileSystem name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b262b-138">-MaxBatchCount</span><span class="sxs-lookup"><span data-stu-id="b262b-138">-MaxBatchCount</span></span>
<span data-ttu-id="b262b-139">Numero massimo di batch che è possibile eseguire con una singola operazione di controllo di accesso.</span><span class="sxs-lookup"><span data-stu-id="b262b-139">Maximum number of batches that single change Access Control operation can execute.</span></span> <span data-ttu-id="b262b-140">Se le dimensioni del set di dati superano MaxBatchCount per la moltiplicazione di BatchSize, verrà restituito un token di continuazione.</span><span class="sxs-lookup"><span data-stu-id="b262b-140">If data set size exceeds MaxBatchCount multiply BatchSize, continuation token will be return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b262b-141">-Path</span><span class="sxs-lookup"><span data-stu-id="b262b-141">-Path</span></span>
<span data-ttu-id="b262b-142">Percorso nel FileSystem specificato che consente di modificare l'Acl in modo ricorsivo.</span><span class="sxs-lookup"><span data-stu-id="b262b-142">The path in the specified FileSystem that to change Acl recursively.</span></span>
<span data-ttu-id="b262b-143">Può essere un file o una directory.</span><span class="sxs-lookup"><span data-stu-id="b262b-143">Can be a file or directory.</span></span>
<span data-ttu-id="b262b-144">Nel formato "directory/file.txt" o "directory1/directory2/".</span><span class="sxs-lookup"><span data-stu-id="b262b-144">In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="b262b-145">Ignorare questo parametro per modificare l'Acl in modo ricorsivo dalla directory radice del Filesystem.</span><span class="sxs-lookup"><span data-stu-id="b262b-145">Skip set this parameter to change Acl recursively from root directory of the Filesystem.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b262b-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b262b-146">-Confirm</span></span>
<span data-ttu-id="b262b-147">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b262b-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b262b-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b262b-148">-WhatIf</span></span>
<span data-ttu-id="b262b-149">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b262b-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b262b-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b262b-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b262b-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b262b-151">CommonParameters</span></span>
<span data-ttu-id="b262b-152">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b262b-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b262b-153">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b262b-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b262b-154">INPUT</span><span class="sxs-lookup"><span data-stu-id="b262b-154">INPUTS</span></span>

### <span data-ttu-id="b262b-155">System.String</span><span class="sxs-lookup"><span data-stu-id="b262b-155">System.String</span></span>

### <span data-ttu-id="b262b-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b262b-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b262b-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b262b-157">OUTPUTS</span></span>

### <span data-ttu-id="b262b-158">System.String</span><span class="sxs-lookup"><span data-stu-id="b262b-158">System.String</span></span>

## <span data-ttu-id="b262b-159">NOTE</span><span class="sxs-lookup"><span data-stu-id="b262b-159">NOTES</span></span>

## <span data-ttu-id="b262b-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b262b-160">RELATED LINKS</span></span>
