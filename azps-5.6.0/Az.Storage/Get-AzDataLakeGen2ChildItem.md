---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azdatalakegen2childitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ChildItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ChildItem.md
ms.openlocfilehash: 3505d9b07e1d56936a002b45bfeee7929823f4be
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985556"
---
# <span data-ttu-id="7c0ad-101">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="7c0ad-101">Get-AzDataLakeGen2ChildItem</span></span>

## <span data-ttu-id="7c0ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c0ad-102">SYNOPSIS</span></span>
<span data-ttu-id="7c0ad-103">Elenca le sotto directory e i file da una directory o da una radice del file system.</span><span class="sxs-lookup"><span data-stu-id="7c0ad-103">Lists sub directorys and files from a directory or filesystem root.</span></span>

## <span data-ttu-id="7c0ad-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7c0ad-104">SYNTAX</span></span>

```
Get-AzDataLakeGen2ChildItem [-FileSystem] <String> [[-Path] <String>] [-FetchProperty] [-Recurse]
 [-MaxCount <Int32>] [-ContinuationToken <String>] [-AsJob] [-OutputUserPrincipalName]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c0ad-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7c0ad-105">DESCRIPTION</span></span>
<span data-ttu-id="7c0ad-106">Il cmdlet **Get-AzDataLakeGen2Item Elenca** le sotto directory e i file in una directory o filesystem in un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="7c0ad-106">The **Get-AzDataLakeGen2ChildItem** cmdlet lists sub directorys and files in a directory or Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="7c0ad-107">Questo cmdlet funziona solo se lo spazio dei nomi gerarchico è abilitato per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7c0ad-107">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="7c0ad-108">Questo tipo di account può essere creato eseguire il cmdlet "New-AzStorageAccount" con "-EnableHierarchicalZone $true".</span><span class="sxs-lookup"><span data-stu-id="7c0ad-108">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="7c0ad-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7c0ad-109">EXAMPLES</span></span>

### <span data-ttu-id="7c0ad-110">Esempio 1: Elencare gli elementi secondari diretti da un filesystem</span><span class="sxs-lookup"><span data-stu-id="7c0ad-110">Example 1: List the direct sub items from a Filesystem</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" 

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1                 True                         2020-03-13 13:07:34Z rwxr-x---    $superuser           $superuser          
dir2                 True                         2020-03-23 09:28:36Z rwxr-x---    $superuser           $superuser
```

<span data-ttu-id="7c0ad-111">Questo comando elenca gli elementi secondari diretti da un filesystem</span><span class="sxs-lookup"><span data-stu-id="7c0ad-111">This command lists the direct sub items from a Filesystem</span></span>

### <span data-ttu-id="7c0ad-112">Esempio 2: Elencare in modo ricorsivo da una directory e recuperare le proprietà/ACL</span><span class="sxs-lookup"><span data-stu-id="7c0ad-112">Example 2: List recursively from a directory, and fetch Properties/ACL</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" -Path "dir1/" -Recurse -FetchProperty

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir3            True                         2020-03-23 09:34:31Z rwx---rwx    $superuser           $superuser          
dir1/file1           False        1024            2020-03-23 09:29:18Z rwx---rwx    $superuser           $superuser           
dir1/testfile_1K_0   False        1024            2020-03-23 09:29:21Z rw-r-----    $superuser           $superuser
```

<span data-ttu-id="7c0ad-113">Questo comando elenca gli elementi secondari diretti da un filesystem</span><span class="sxs-lookup"><span data-stu-id="7c0ad-113">This command lists the direct sub items from a Filesystem</span></span>

### <span data-ttu-id="7c0ad-114">Esempio 3: Elencare gli elementi in modo ricorsivo da un filesystem in più batch</span><span class="sxs-lookup"><span data-stu-id="7c0ad-114">Example 3: List items recursively from a Filesystem in multiple batches</span></span>
```
PS C:\> $MaxReturn = 10000
PS C:\> $FileSystemName = "filesystem1"
PS C:\> $Total = 0
PS C:\> $Token = $Null
PS C:\> do
 {
     $items = Get-AzDataLakeGen2ChildItem -FileSystem $FileSystemName -Recurse -MaxCount $MaxReturn  -ContinuationToken $Token
     $Total += $items.Count
     if($items.Length -le 0) { Break;}
     $Token = $items[$items.Count -1].ContinuationToken;
 }
 While ($Token -ne $Null)
PS C:\> Echo "Total $Total items in Filesystem $FileSystemName"
```

<span data-ttu-id="7c0ad-115">Questo esempio usa i *parametri MaxCount* e *ContinuationToken* per elencare gli elementi in modo ricorsivo da un filesystem in più batch.</span><span class="sxs-lookup"><span data-stu-id="7c0ad-115">This example uses the *MaxCount* and *ContinuationToken* parameters to list items recursively from a Filesystem in multiple batches.</span></span>
<span data-ttu-id="7c0ad-116">I primi quattro comandi assegnano valori alle variabili da usare nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="7c0ad-116">The first four commands assign values to variables to use in the example.</span></span>
<span data-ttu-id="7c0ad-117">Il quinto comando specifica **un'istruzione Do-While** che usa il cmdlet **Get-AzDataLakeGen2Item** per elencare gli elementi.</span><span class="sxs-lookup"><span data-stu-id="7c0ad-117">The fifth command specifies a **Do-While** statement that uses the **Get-AzDataLakeGen2ChildItem** cmdlet to list items.</span></span>
<span data-ttu-id="7c0ad-118">L'istruzione include il token di continuazione archiviato nella $Token variabile.</span><span class="sxs-lookup"><span data-stu-id="7c0ad-118">The statement includes the continuation token stored in the $Token variable.</span></span>
<span data-ttu-id="7c0ad-119">$Token cambia valore durante l'esecuzione del ciclo.</span><span class="sxs-lookup"><span data-stu-id="7c0ad-119">$Token changes value as the loop runs.</span></span>
<span data-ttu-id="7c0ad-120">Il comando finale usa il **comando Eco** schermo per visualizzare il totale.</span><span class="sxs-lookup"><span data-stu-id="7c0ad-120">The final command uses the **Echo** command to display the total.</span></span>

## <span data-ttu-id="7c0ad-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c0ad-121">PARAMETERS</span></span>

### <span data-ttu-id="7c0ad-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c0ad-122">-AsJob</span></span>
<span data-ttu-id="7c0ad-123">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="7c0ad-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7c0ad-124">-Context</span><span class="sxs-lookup"><span data-stu-id="7c0ad-124">-Context</span></span>
<span data-ttu-id="7c0ad-125">Oggetto contesto archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="7c0ad-125">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="7c0ad-126">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="7c0ad-126">-ContinuationToken</span></span>
<span data-ttu-id="7c0ad-127">Token di continuazione.</span><span class="sxs-lookup"><span data-stu-id="7c0ad-127">Continuation Token.</span></span>

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

### <span data-ttu-id="7c0ad-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c0ad-128">-DefaultProfile</span></span>
<span data-ttu-id="7c0ad-129">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7c0ad-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c0ad-130">-FetchProperty</span><span class="sxs-lookup"><span data-stu-id="7c0ad-130">-FetchProperty</span></span>
<span data-ttu-id="7c0ad-131">Recuperare le proprietà dell'elemento della connessione dati e l'ACL.</span><span class="sxs-lookup"><span data-stu-id="7c0ad-131">Fetch the datalake item properties and ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: FetchPermission

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c0ad-132">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="7c0ad-132">-FileSystem</span></span>
<span data-ttu-id="7c0ad-133">Nome filesystem</span><span class="sxs-lookup"><span data-stu-id="7c0ad-133">FileSystem name</span></span>

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

### <span data-ttu-id="7c0ad-134">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="7c0ad-134">-MaxCount</span></span>
<span data-ttu-id="7c0ad-135">Numero massimo di BLOB che possono essere restituiti.</span><span class="sxs-lookup"><span data-stu-id="7c0ad-135">The max count of the blobs that can return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c0ad-136">-OutputUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="7c0ad-136">-OutputUserPrincipalName</span></span>
<span data-ttu-id="7c0ad-137">Se si specifica questo parametro, i valori di identità utente restituiti nei campi del proprietario e del gruppo di ogni voce di elenco verranno trasformati dagli ID oggetto di Azure Active Directory in nomi dell'entità utente.</span><span class="sxs-lookup"><span data-stu-id="7c0ad-137">If speicify this parameter, the user identity values returned in the owner and group fields of each list entry will be transformed from Azure Active Directory Object IDs to User Principal Names.</span></span> <span data-ttu-id="7c0ad-138">Se non si specifica questo parametro, i valori verranno restituiti come ID oggetto di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7c0ad-138">If not speicify this parameter, the values will be returned as Azure Active Directory Object IDs.</span></span> <span data-ttu-id="7c0ad-139">Si noti che gli ID oggetto di gruppo e applicazione non vengono tradotti perché non hanno nomi univoci descrittivi.</span><span class="sxs-lookup"><span data-stu-id="7c0ad-139">Note that group and application Object IDs are not translated because they do not have unique friendly names.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: UserPrincipalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c0ad-140">-Path</span><span class="sxs-lookup"><span data-stu-id="7c0ad-140">-Path</span></span>
<span data-ttu-id="7c0ad-141">Percorso nel file system specificato che deve essere recuperato.</span><span class="sxs-lookup"><span data-stu-id="7c0ad-141">The path in the specified Filesystem that should be retrieved.</span></span>
<span data-ttu-id="7c0ad-142">Deve essere una directory, nel formato 'directory1/directory2/'.</span><span class="sxs-lookup"><span data-stu-id="7c0ad-142">Should be a directory, in the format 'directory1/directory2/'.</span></span>

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

### <span data-ttu-id="7c0ad-143">-Ricorrenza</span><span class="sxs-lookup"><span data-stu-id="7c0ad-143">-Recurse</span></span>
<span data-ttu-id="7c0ad-144">Indica se l'elemento figlio viene visualizzato in modo ricorsivo.</span><span class="sxs-lookup"><span data-stu-id="7c0ad-144">Indicates if will recursively get the Child Item.</span></span>
<span data-ttu-id="7c0ad-145">L'impostazione predefinita è false.</span><span class="sxs-lookup"><span data-stu-id="7c0ad-145">The default is false.</span></span>

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

### <span data-ttu-id="7c0ad-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c0ad-146">CommonParameters</span></span>
<span data-ttu-id="7c0ad-147">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c0ad-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c0ad-148">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c0ad-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c0ad-149">INPUT</span><span class="sxs-lookup"><span data-stu-id="7c0ad-149">INPUTS</span></span>

### <span data-ttu-id="7c0ad-150">System.String</span><span class="sxs-lookup"><span data-stu-id="7c0ad-150">System.String</span></span>

### <span data-ttu-id="7c0ad-151">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7c0ad-151">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7c0ad-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7c0ad-152">OUTPUTS</span></span>

### <span data-ttu-id="7c0ad-153">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="7c0ad-153">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="7c0ad-154">NOTE</span><span class="sxs-lookup"><span data-stu-id="7c0ad-154">NOTES</span></span>

## <span data-ttu-id="7c0ad-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7c0ad-155">RELATED LINKS</span></span>
