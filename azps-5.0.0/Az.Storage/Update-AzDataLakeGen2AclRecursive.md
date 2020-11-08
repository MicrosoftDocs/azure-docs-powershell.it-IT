---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azdatalakegen2aclrecursive
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2AclRecursive.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2AclRecursive.md
ms.openlocfilehash: 80b1816dff686db7e84bf876fd74f9642389b42f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201922"
---
# <span data-ttu-id="06e30-101">Update-AzDataLakeGen2AclRecursive</span><span class="sxs-lookup"><span data-stu-id="06e30-101">Update-AzDataLakeGen2AclRecursive</span></span>

## <span data-ttu-id="06e30-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="06e30-102">SYNOPSIS</span></span>
<span data-ttu-id="06e30-103">Aggiornare l'ACL in modo ricorsivo nel percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="06e30-103">Update ACL recursively on the specified path.</span></span> 

## <span data-ttu-id="06e30-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="06e30-104">SYNTAX</span></span>

```
Update-AzDataLakeGen2AclRecursive [-FileSystem] <String> [[-Path] <String>] [-ContinuationToken <String>]
 -Acl <PSPathAccessControlEntry[]> [-ContinueOnFailure] [-BatchSize <Int32>] [-MaxBatchCount <Int32>] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="06e30-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06e30-105">DESCRIPTION</span></span>
<span data-ttu-id="06e30-106">Il cmdlet **Update-AzDataLakeGen2AclRecursive** Aggiorna ricorsivamente ACL nel percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="06e30-106">The **Update-AzDataLakeGen2AclRecursive** cmdlet updates ACL recursively on the specified path.</span></span> <span data-ttu-id="06e30-107">L'ACL di input consentirà di unire l'ACL originale: se la voce ACL con lo stesso AccessControlType/EntityId/DefaultScope esiste, l'autorizzazione di aggiornamento; else aggiungere una nuova voce ACL.</span><span class="sxs-lookup"><span data-stu-id="06e30-107">The input ACL will merge the the original ACL: If ACL entry with same AccessControlType/EntityId/DefaultScope exist, update permission; else add a new ACL entry.</span></span>

## <span data-ttu-id="06e30-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="06e30-108">EXAMPLES</span></span>

### <span data-ttu-id="06e30-109">Esempio 1: aggiornare l'ACL in modo ricorsivo in un directiry radice di filesystem</span><span class="sxs-lookup"><span data-stu-id="06e30-109">Example 1: Update ACL recursively on a root directiry of filesystem</span></span>
```
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\> Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Acl $acl -Context $ctx

FailedEntries                   : 
TotalDirectoriesSuccessfulCount : 7
TotalFilesSuccessfulCount       : 5
TotalFailureCount               : 0
ContinuationToken               :
```

<span data-ttu-id="06e30-110">Questo comando crea prima di tutto un oggetto ACL con 3 voci ACL, quindi aggiorna l'ACL in modo ricorsivo in una directory radice di un file System.</span><span class="sxs-lookup"><span data-stu-id="06e30-110">This command first creates an ACL object with 3 acl entries, then updates ACL recursively on a root directory of a file system.</span></span>

### <span data-ttu-id="06e30-111">Esempio 2: aggiornare ACL in modo ricorsivo in una directory e riprendere da un errore con ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="06e30-111">Example 2: Update ACL recursively on a directory, and resume from failure with ContinuationToken</span></span>
```
PS C:\> $result = Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -Context $ctx

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

PS C:\> $result = Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl -ContinuationToken $result.ContinuationToken -Context $ctx

PS C:\> $result

FailedEntries                   : 
TotalDirectoriesSuccessfulCount : 100
TotalFilesSuccessfulCount       : 1000
TotalFailureCount               : 0
ContinuationToken               :
```

<span data-ttu-id="06e30-112">Questo comando Aggiorna prima di tutto ACL ricorsivamente a una directory e non riesce, quindi riprende con ContinuationToken dopo che l'utente ha risolto il file non riuscito.</span><span class="sxs-lookup"><span data-stu-id="06e30-112">This command first updateds ACL recursively to a directory and failed, then resume with ContinuationToken after user fix the failed file.</span></span>

### <span data-ttu-id="06e30-113">Esempio 3: aggiornare ACL in modo ricorsivo per blocco</span><span class="sxs-lookup"><span data-stu-id="06e30-113">Example 3: Update ACL recursively chunk by chunk</span></span>
```
$ContinueOnFailure = $true # Set it to $false if want to terminate the operation quickly on encountering failures
$token = $null
$TotalDirectoriesSuccess = 0
$TotalFilesSuccess = 0
$totalFailure = 0
$FailedEntries = New-Object System.Collections.Generic.List[System.Object]
do
{
    
    if ($ContinueOnFailure)
    {
        $result = Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -BatchSize 100 -MaxBatchCount 50 -ContinuationToken $token -Context $ctx -ContinueOnFailure
    }
    else
    {
        $result = Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -BatchSize 100 -MaxBatchCount 50 -ContinuationToken $token -Context $ctx
    }

    # echo $result
    $TotalFilesSuccess += $result.TotalFilesSuccessfulCount
    $TotalDirectoriesSuccess += $result.TotalDirectoriesSuccessfulCount
    $totalFailure += $result.TotalFailureCount
    $FailedEntries += $result.FailedEntries
    $token = $result.ContinuationToken
}while (($token -ne $null) -and (($ContinueOnFailure) -or ($result.TotalFailureCount -eq 0)))
echo ""
echo "[Result Summary]"
echo "TotalDirectoriesSuccessfulCount: `t$($TotalDirectoriesSuccess)"
echo "TotalFilesSuccessfulCount: `t`t`t$($TotalFilesSuccess)"
echo "TotalFailureCount: `t`t`t`t`t$($totalFailure)"
echo "ContinuationToken: `t`t`t`t`t$($token)"
echo "FailedEntries:"$($FailedEntries | ft)
```

<span data-ttu-id="06e30-114">Questo script aggiornerà ACL rescursively in blocco directory per blocco, con dimensione del blocco come BatchSize \* MaxBatchCount.</span><span class="sxs-lookup"><span data-stu-id="06e30-114">This script will update ACL rescursively on directory chunk by chunk, with chunk size as BatchSize \* MaxBatchCount.</span></span> <span data-ttu-id="06e30-115">La dimensione del blocco è 5000 in questo script.</span><span class="sxs-lookup"><span data-stu-id="06e30-115">Chunk size is 5000 in this script.</span></span>

### <span data-ttu-id="06e30-116">Esempio 4: aggiornare ACL in modo ricorsivo in una directory e in ContinueOnFailure, quindi riprendere da errori uno alla volta</span><span class="sxs-lookup"><span data-stu-id="06e30-116">Example 4: Update ACL recursively on a directory and ContinueOnFailure, then resume from failures one by one</span></span>
```
PS C:\> $result = Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl -ContinueOnFailure -Context $ctx

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

<span data-ttu-id="06e30-117">Questo comando Aggiorna l'ACL ricorsivamente in una directory con ContinueOnFailure e alcuni elementi non riescono, quindi Riprendi uno alla volta gli elementi falliti.</span><span class="sxs-lookup"><span data-stu-id="06e30-117">This command first updateds ACL recursively to a directory with ContinueOnFailure, and some items failed, then resume the failed items one by one.</span></span>

## <span data-ttu-id="06e30-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="06e30-118">PARAMETERS</span></span>

### <span data-ttu-id="06e30-119">-ACL</span><span class="sxs-lookup"><span data-stu-id="06e30-119">-Acl</span></span>
<span data-ttu-id="06e30-120">L'elenco di controllo di accesso POSIX da impostare ricorsivamente per il file o la directory.</span><span class="sxs-lookup"><span data-stu-id="06e30-120">The POSIX access control list to set recursively for the file or directory.</span></span>

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

### <span data-ttu-id="06e30-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06e30-121">-AsJob</span></span>
<span data-ttu-id="06e30-122">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="06e30-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="06e30-123">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="06e30-123">-BatchSize</span></span>
<span data-ttu-id="06e30-124">Se le dimensioni del set di dati superano le dimensioni del batch, l'operazione verrà divisa in più richieste in modo che sia possibile tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="06e30-124">If data set size exceeds batch size then operation will be split into multiple requests so that progress can be tracked.</span></span>
<span data-ttu-id="06e30-125">La dimensione del batch deve essere compresa tra 1 e 2000.</span><span class="sxs-lookup"><span data-stu-id="06e30-125">Batch size should be between 1 and 2000.</span></span>
<span data-ttu-id="06e30-126">Il valore predefinito è 2000.</span><span class="sxs-lookup"><span data-stu-id="06e30-126">Default is 2000.</span></span>

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

### <span data-ttu-id="06e30-127">-Contesto</span><span class="sxs-lookup"><span data-stu-id="06e30-127">-Context</span></span>
<span data-ttu-id="06e30-128">Oggetto contesto di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="06e30-128">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="06e30-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="06e30-129">-ContinuationToken</span></span>
<span data-ttu-id="06e30-130">Token di continuazione.</span><span class="sxs-lookup"><span data-stu-id="06e30-130">Continuation Token.</span></span>

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

### <span data-ttu-id="06e30-131">-ContinueOnFailure</span><span class="sxs-lookup"><span data-stu-id="06e30-131">-ContinueOnFailure</span></span>
<span data-ttu-id="06e30-132">Imposta questo parametro per ignorare gli errori e continuare proceeing con l'operazione su altre entità secondarie della directory.</span><span class="sxs-lookup"><span data-stu-id="06e30-132">Set this parameter to ignore failures and continue proceeing with the operation on other sub-entities of the directory.</span></span> <span data-ttu-id="06e30-133">Impostazione predefinita l'operazione viene terminata rapidamente quando si verificano errori.</span><span class="sxs-lookup"><span data-stu-id="06e30-133">Default the operation will terminate quickly on encountering failures.</span></span>

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

### <span data-ttu-id="06e30-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06e30-134">-DefaultProfile</span></span>
<span data-ttu-id="06e30-135">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="06e30-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06e30-136">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="06e30-136">-FileSystem</span></span>
<span data-ttu-id="06e30-137">Nome FileSystem</span><span class="sxs-lookup"><span data-stu-id="06e30-137">FileSystem name</span></span>

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

### <span data-ttu-id="06e30-138">-MaxBatchCount</span><span class="sxs-lookup"><span data-stu-id="06e30-138">-MaxBatchCount</span></span>
<span data-ttu-id="06e30-139">Numero massimo di batch in cui può essere eseguita l'operazione di controllo di accesso a singola modifica.</span><span class="sxs-lookup"><span data-stu-id="06e30-139">Maximum number of batches that single change Access Control operation can execute.</span></span> <span data-ttu-id="06e30-140">Se le dimensioni del set di dati superano MaxBatchCount Multiply BatchSize, il token di continuazione sarà return.</span><span class="sxs-lookup"><span data-stu-id="06e30-140">If data set size exceeds MaxBatchCount multiply BatchSize, continuation token will be return.</span></span>

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

### <span data-ttu-id="06e30-141">-Path</span><span class="sxs-lookup"><span data-stu-id="06e30-141">-Path</span></span>
<span data-ttu-id="06e30-142">Il percorso nel file system specificato che consente di modificare l'ACL in modo ricorsivo.</span><span class="sxs-lookup"><span data-stu-id="06e30-142">The path in the specified FileSystem that to change Acl recursively.</span></span>
<span data-ttu-id="06e30-143">Può essere un file o una directory.</span><span class="sxs-lookup"><span data-stu-id="06e30-143">Can be a file or directory.</span></span>
<span data-ttu-id="06e30-144">Nel formato ' directory/file.txt' o ' directory1/directory2/'.</span><span class="sxs-lookup"><span data-stu-id="06e30-144">In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="06e30-145">Ignora imposta questo parametro per modificare l'ACL ricorsivamente dalla directory radice del filesystem.</span><span class="sxs-lookup"><span data-stu-id="06e30-145">Skip set this parameter to change Acl recursively from root directory of the Filesystem.</span></span>

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

### <span data-ttu-id="06e30-146">-Confermare</span><span class="sxs-lookup"><span data-stu-id="06e30-146">-Confirm</span></span>
<span data-ttu-id="06e30-147">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06e30-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06e30-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06e30-148">-WhatIf</span></span>
<span data-ttu-id="06e30-149">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="06e30-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06e30-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="06e30-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06e30-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06e30-151">CommonParameters</span></span>
<span data-ttu-id="06e30-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06e30-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06e30-153">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06e30-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06e30-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="06e30-154">INPUTS</span></span>

### <span data-ttu-id="06e30-155">System. String</span><span class="sxs-lookup"><span data-stu-id="06e30-155">System.String</span></span>

### <span data-ttu-id="06e30-156">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="06e30-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="06e30-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="06e30-157">OUTPUTS</span></span>

### <span data-ttu-id="06e30-158">System. String</span><span class="sxs-lookup"><span data-stu-id="06e30-158">System.String</span></span>

## <span data-ttu-id="06e30-159">Note</span><span class="sxs-lookup"><span data-stu-id="06e30-159">NOTES</span></span>

## <span data-ttu-id="06e30-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="06e30-160">RELATED LINKS</span></span>
