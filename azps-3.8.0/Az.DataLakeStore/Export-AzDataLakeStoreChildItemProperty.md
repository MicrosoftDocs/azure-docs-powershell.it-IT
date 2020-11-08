---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/export-azdatalakestorechilditemproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreChildItemProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreChildItemProperty.md
ms.openlocfilehash: 25615684db8b78a461b39b1a8cfc159d42a56883
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018469"
---
# <span data-ttu-id="a36d6-101">Export-AzDataLakeStoreChildItemProperty</span><span class="sxs-lookup"><span data-stu-id="a36d6-101">Export-AzDataLakeStoreChildItemProperty</span></span>

## <span data-ttu-id="a36d6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a36d6-102">SYNOPSIS</span></span>
<span data-ttu-id="a36d6-103">Esporta le proprietà (utilizzo del disco e ACL) per l'intero albero dal percorso specificato a un percorso di output</span><span class="sxs-lookup"><span data-stu-id="a36d6-103">Exports the properties (Disk usage and Acl) for the entire tree from the specified path to a output path</span></span>

## <span data-ttu-id="a36d6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a36d6-104">SYNTAX</span></span>

### <span data-ttu-id="a36d6-105">GetDiskUsage</span><span class="sxs-lookup"><span data-stu-id="a36d6-105">GetDiskUsage</span></span>
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a36d6-106">GetAllProperties</span><span class="sxs-lookup"><span data-stu-id="a36d6-106">GetAllProperties</span></span>
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-GetAcl] [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a36d6-107">GetAclDump</span><span class="sxs-lookup"><span data-stu-id="a36d6-107">GetAclDump</span></span>
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>] [-GetAcl]
 [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a36d6-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a36d6-108">DESCRIPTION</span></span>
<span data-ttu-id="a36d6-109">L' **Export-AzDataLakeStoreChildItemProperty** viene usato per segnalare l'utilizzo dello spazio ADL o/e l'uso di ACL per la directory specificata, oltre a directory secondarie e file.</span><span class="sxs-lookup"><span data-stu-id="a36d6-109">The **Export-AzDataLakeStoreChildItemProperty** is used to report the ADLS space usage or/and ACL usage for the given directory and it's sub directories and files.</span></span>

## <span data-ttu-id="a36d6-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a36d6-110">EXAMPLES</span></span>

### <span data-ttu-id="a36d6-111">Esempio 1: ottenere l'utilizzo del disco e l'utilizzo di ACL per tutte le sottodirectory e i file</span><span class="sxs-lookup"><span data-stu-id="a36d6-111">Example 1: Get the disk usage and ACL usage for all subdirectories and files</span></span>
```
PS C:\> Export-AzDataLakeStoreChildItemProperty -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -GetDiskUsage -IncludeFile
```

<span data-ttu-id="a36d6-112">Ottenere l'utilizzo del disco e l'utilizzo di ACL per tutte le sottodirectory e i file in/a.</span><span class="sxs-lookup"><span data-stu-id="a36d6-112">Get the disk usage and ACL usage for all subdirectories and files under /a.</span></span> <span data-ttu-id="a36d6-113">IncludeFile assicura che l'utilizzo venga segnalato anche per i file</span><span class="sxs-lookup"><span data-stu-id="a36d6-113">IncludeFile ensures the usage is reported for files also</span></span>

### <span data-ttu-id="a36d6-114">Esempio 2: ottenere l'utilizzo di ACL per tutte le sottodirectory e i file con l'ACL coerente nascosto</span><span class="sxs-lookup"><span data-stu-id="a36d6-114">Example 2: Get the ACL usage for all subdirectories and files with the consistent ACL hidden</span></span>
```
PS C:\> $fullAcl="user:contoso-userid:--x|user::rwx|other::---|group::rwx"
PS C:\> $newFullAcl = $fullAcl.Split("{|}");
PS C:\> Set-AzDataLakeStoreItemAcl -Account ContosoADL -Path /a -Acl $newFullAcl -Recurse -Debug

PS C:\> Export-AzDataLakeStoreChildItemProperty -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -HideConsistentAcl -IncludeFile
```

<span data-ttu-id="a36d6-115">Ottenere l'utilizzo di ACL per tutte le sottodirectory e i file in/a.</span><span class="sxs-lookup"><span data-stu-id="a36d6-115">Get the ACL usage for all subdirectories and files under /a.</span></span> <span data-ttu-id="a36d6-116">IncludeFile assicura che l'uso sia segnalato anche per i file.</span><span class="sxs-lookup"><span data-stu-id="a36d6-116">IncludeFile ensures the usage is reported for files also.</span></span> <span data-ttu-id="a36d6-117">HideconsistentAcl in questo caso verrà visualizzato l'ACL di/a, non i relativi elementi figlio poiché tutti gli elementi figlio hanno lo stesso ACL di/a.</span><span class="sxs-lookup"><span data-stu-id="a36d6-117">HideconsistentAcl in this case will show the Acl of /a, not it's children since all of the children has same acl as /a.</span></span> <span data-ttu-id="a36d6-118">Questo flag ignora l'output ACL del sottoalbero se tutti gli ACL sono uguali alla radice.</span><span class="sxs-lookup"><span data-stu-id="a36d6-118">This flag skips the acl output of subtree if all it's acls are same as the root.</span></span>

## <span data-ttu-id="a36d6-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a36d6-119">PARAMETERS</span></span>

### <span data-ttu-id="a36d6-120">-Account</span><span class="sxs-lookup"><span data-stu-id="a36d6-120">-Account</span></span>
<span data-ttu-id="a36d6-121">L'account di data Lake Store per eseguire l'operazione filesystem in</span><span class="sxs-lookup"><span data-stu-id="a36d6-121">The Data Lake Store account to execute the filesystem operation in</span></span>

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

### <span data-ttu-id="a36d6-122">-Concorrenza</span><span class="sxs-lookup"><span data-stu-id="a36d6-122">-Concurrency</span></span>
<span data-ttu-id="a36d6-123">Indica il numero di file/directory elaborati in parallelo.</span><span class="sxs-lookup"><span data-stu-id="a36d6-123">Indicates the number of files/directories processed in parallel.</span></span>
<span data-ttu-id="a36d6-124">L'impostazione predefinita verrà calcolata come uno sforzo ottimale in base alle specifiche di sistema.</span><span class="sxs-lookup"><span data-stu-id="a36d6-124">Default will be computed as a best effort based on system specification.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a36d6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a36d6-125">-DefaultProfile</span></span>
<span data-ttu-id="a36d6-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a36d6-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a36d6-127">-GetAcl</span><span class="sxs-lookup"><span data-stu-id="a36d6-127">-GetAcl</span></span>
<span data-ttu-id="a36d6-128">Recupera l'ACL a partire dal percorso radice</span><span class="sxs-lookup"><span data-stu-id="a36d6-128">Retrieves the acl starting from the root path</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetAllProperties, GetAclDump
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a36d6-129">-GetDiskUsage</span><span class="sxs-lookup"><span data-stu-id="a36d6-129">-GetDiskUsage</span></span>
<span data-ttu-id="a36d6-130">Recupera l'utilizzo del disco a partire dal percorso radice</span><span class="sxs-lookup"><span data-stu-id="a36d6-130">Retrieves the disk usage starting from the root path</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetDiskUsage, GetAllProperties
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a36d6-131">-HideConsistentAcl</span><span class="sxs-lookup"><span data-stu-id="a36d6-131">-HideConsistentAcl</span></span>
<span data-ttu-id="a36d6-132">Non mostrare la sottostruttura della directory se gli ACL sono gli stessi in tutto l'intero sottoalbero.</span><span class="sxs-lookup"><span data-stu-id="a36d6-132">Do not show directory subtree if the ACLs are the same throughout the entire subtree.</span></span> <span data-ttu-id="a36d6-133">In questo modo è più semplice visualizzare solo i percorsi in cui gli ACL differiscono. Ad esempio, se tutti i file e le cartelle in/a/b sono gli stessi, non mostrare il subtreeunder/a/b e solo l'output/a/b con "true" nell'ACL coerente columnCannot essere impostato se IncludeFiles non è impostato, perché non è possibile determinare l'ACL coerente senza recuperare gli ACL per i file.</span><span class="sxs-lookup"><span data-stu-id="a36d6-133">This makes it easier to see only the paths up to which the ACLs differ.For example if all files and folders under /a/b are the same, do not show the subtreeunder /a/b, and just output /a/b with 'True' in the Consistent ACL columnCannot be set if IncludeFiles is not set, because consistent Acl cannot be determined without retrieving acls for the files.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetAllProperties, GetAclDump
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a36d6-134">-IncludeFile</span><span class="sxs-lookup"><span data-stu-id="a36d6-134">-IncludeFile</span></span>
<span data-ttu-id="a36d6-135">Mostra statistiche a livello di file (l'impostazione predefinita è mostrare solo le informazioni a livello di directory)</span><span class="sxs-lookup"><span data-stu-id="a36d6-135">Show stats at file level (default is to show directory-level info only)</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a36d6-136">-MaximumDepth</span><span class="sxs-lookup"><span data-stu-id="a36d6-136">-MaximumDepth</span></span>
<span data-ttu-id="a36d6-137">Profondità massima dalla directory radice fino a cui viene visualizzato l'utilizzo del disco o l'ACL</span><span class="sxs-lookup"><span data-stu-id="a36d6-137">Maximum depth from the root directory till which disk usage or acl is displayed</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a36d6-138">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="a36d6-138">-OutputPath</span></span>
<span data-ttu-id="a36d6-139">Percorso del file di output.</span><span class="sxs-lookup"><span data-stu-id="a36d6-139">Path to output file.</span></span> <span data-ttu-id="a36d6-140">Può essere un percorso locale o un percorso ADL.</span><span class="sxs-lookup"><span data-stu-id="a36d6-140">Can be a Local path or Adl Path.</span></span> <span data-ttu-id="a36d6-141">Per impostazione predefinita, è locale.</span><span class="sxs-lookup"><span data-stu-id="a36d6-141">By default it is local.</span></span> <span data-ttu-id="a36d6-142">Se si specifica SaveToAdl, si tratta di un percorso ADL nello stesso account</span><span class="sxs-lookup"><span data-stu-id="a36d6-142">If SaveToAdl is specified then it is an ADL path in the same account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a36d6-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a36d6-143">-PassThru</span></span>
<span data-ttu-id="a36d6-144">Indica che deve essere restituita una risposta booleana che indica il risultato dell'operazione di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="a36d6-144">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a36d6-145">-Path</span><span class="sxs-lookup"><span data-stu-id="a36d6-145">-Path</span></span>
<span data-ttu-id="a36d6-146">Il percorso nell'account del lago dati specificato che deve essere recuperato.</span><span class="sxs-lookup"><span data-stu-id="a36d6-146">The path in the specified Data Lake account that should be retrieve.</span></span>
<span data-ttu-id="a36d6-147">Può essere un file o una cartella nel formato "/folder/file.txt", in cui il primo "/" dopo il DNS indica la radice del file System.</span><span class="sxs-lookup"><span data-stu-id="a36d6-147">Can be a file or folder In the format '/folder/file.txt', where the first '/' after the DNS indicates the root of the file system.</span></span>

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

### <span data-ttu-id="a36d6-148">-SaveToAdl</span><span class="sxs-lookup"><span data-stu-id="a36d6-148">-SaveToAdl</span></span>
<span data-ttu-id="a36d6-149">Se passato, Salva il file di dump in ADL.</span><span class="sxs-lookup"><span data-stu-id="a36d6-149">If passed then saves the dump file to ADL.</span></span>
<span data-ttu-id="a36d6-150">Il DumpFile wil essere un percorso ADL in questo caso</span><span class="sxs-lookup"><span data-stu-id="a36d6-150">The DumpFile wil be a ADL path in that case</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a36d6-151">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a36d6-151">-Confirm</span></span>
<span data-ttu-id="a36d6-152">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a36d6-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a36d6-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a36d6-153">-WhatIf</span></span>
<span data-ttu-id="a36d6-154">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a36d6-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a36d6-155">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a36d6-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a36d6-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a36d6-156">CommonParameters</span></span>
<span data-ttu-id="a36d6-157">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a36d6-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a36d6-158">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a36d6-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a36d6-159">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a36d6-159">INPUTS</span></span>

### <span data-ttu-id="a36d6-160">System. String</span><span class="sxs-lookup"><span data-stu-id="a36d6-160">System.String</span></span>

### <span data-ttu-id="a36d6-161">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="a36d6-161">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="a36d6-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a36d6-162">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="a36d6-163">System. Int32</span><span class="sxs-lookup"><span data-stu-id="a36d6-163">System.Int32</span></span>

## <span data-ttu-id="a36d6-164">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a36d6-164">OUTPUTS</span></span>

### <span data-ttu-id="a36d6-165">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a36d6-165">System.Boolean</span></span>

## <span data-ttu-id="a36d6-166">Note</span><span class="sxs-lookup"><span data-stu-id="a36d6-166">NOTES</span></span>

## <span data-ttu-id="a36d6-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a36d6-167">RELATED LINKS</span></span>
