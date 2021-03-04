---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2Item.md
ms.openlocfilehash: 2d3db18c49d29cabb8f6459adcd46a9c0242c02f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981966"
---
# <span data-ttu-id="76f21-101">Remove-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="76f21-101">Remove-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="76f21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76f21-102">SYNOPSIS</span></span>
<span data-ttu-id="76f21-103">Rimuovere un file o una directory.</span><span class="sxs-lookup"><span data-stu-id="76f21-103">Remove a file or directory.</span></span>

## <span data-ttu-id="76f21-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="76f21-104">SYNTAX</span></span>

### <span data-ttu-id="76f21-105">ReceiveManual (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="76f21-105">ReceiveManual (Default)</span></span>
```
Remove-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> [-Force] [-AsJob] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="76f21-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="76f21-106">ItemPipeline</span></span>
```
Remove-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> [-Force] [-AsJob] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="76f21-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="76f21-107">DESCRIPTION</span></span>
<span data-ttu-id="76f21-108">Il cmdlet **Remove-AzDataLakeGen2Item** rimuove un file o una directory da un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="76f21-108">The **Remove-AzDataLakeGen2Item** cmdlet removes a file or directory from a Storage account.</span></span>
<span data-ttu-id="76f21-109">Questo cmdlet funziona solo se lo spazio dei nomi gerarchico è abilitato per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="76f21-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="76f21-110">Questo tipo di account può essere creato eseguire il cmdlet "New-AzStorageAccount" con "-EnableHierarchicalZone $true".</span><span class="sxs-lookup"><span data-stu-id="76f21-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="76f21-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="76f21-111">EXAMPLES</span></span>

### <span data-ttu-id="76f21-112">Esempio 1: Rimuove una directory</span><span class="sxs-lookup"><span data-stu-id="76f21-112">Example 1: Removes a directory</span></span>
```
PS C:\>Remove-AzDataLakeGen2tem -FileSystem "filesystem1" -Path "dir1/"
```

<span data-ttu-id="76f21-113">Questo comando rimuove una directory da un filesystem.</span><span class="sxs-lookup"><span data-stu-id="76f21-113">This command removes a directory from a Filesystem.</span></span>

### <span data-ttu-id="76f21-114">Esempio 2: Rimuove un file senza richiesta</span><span class="sxs-lookup"><span data-stu-id="76f21-114">Example 2: Removes a file without prompt</span></span>
```
PS C:\>Remove-AzDataLakeGen2tem -FileSystem "filesystem1" -Path "dir1/file1" -Force
```

<span data-ttu-id="76f21-115">Questo comando rimuove una directory da un file system, senza chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="76f21-115">This command removes a directory from a Filesystem, without prompt.</span></span>

### <span data-ttu-id="76f21-116">Esempio 3: Rimuovere tutti gli elementi in un filesystem con pipeline</span><span class="sxs-lookup"><span data-stu-id="76f21-116">Example 3: Remove all items in a Filesystem with pipeline</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" | Remove-AzDataLakeGen2Item -Force
```

<span data-ttu-id="76f21-117">Questo comando rimuove tutti gli elementi in un Filesystem con pipeline.</span><span class="sxs-lookup"><span data-stu-id="76f21-117">This command removes all items in a Filesystem with pipeline.</span></span>

## <span data-ttu-id="76f21-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76f21-118">PARAMETERS</span></span>

### <span data-ttu-id="76f21-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="76f21-119">-AsJob</span></span>
<span data-ttu-id="76f21-120">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="76f21-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="76f21-121">-Context</span><span class="sxs-lookup"><span data-stu-id="76f21-121">-Context</span></span>
<span data-ttu-id="76f21-122">Oggetto contesto archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="76f21-122">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="76f21-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76f21-123">-DefaultProfile</span></span>
<span data-ttu-id="76f21-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="76f21-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76f21-125">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="76f21-125">-FileSystem</span></span>
<span data-ttu-id="76f21-126">Nome filesystem</span><span class="sxs-lookup"><span data-stu-id="76f21-126">FileSystem name</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76f21-127">-Force</span><span class="sxs-lookup"><span data-stu-id="76f21-127">-Force</span></span>
<span data-ttu-id="76f21-128">Forzare la rimozione del file system e di tutto il contenuto in esso contenuto</span><span class="sxs-lookup"><span data-stu-id="76f21-128">Force to remove the Filesystem and all content in it</span></span>

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

### <span data-ttu-id="76f21-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76f21-129">-InputObject</span></span>
<span data-ttu-id="76f21-130">Oggetto Elemento Gen2 di Azure Datalake da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="76f21-130">Azure Datalake Gen2 Item Object to remove.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item
Parameter Sets: ItemPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76f21-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="76f21-131">-PassThru</span></span>
<span data-ttu-id="76f21-132">Restituisce se il filesystem specificato è stato rimosso correttamente</span><span class="sxs-lookup"><span data-stu-id="76f21-132">Return whether the specified Filesystem is successfully removed</span></span>

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

### <span data-ttu-id="76f21-133">-Path</span><span class="sxs-lookup"><span data-stu-id="76f21-133">-Path</span></span>
<span data-ttu-id="76f21-134">Percorso nel file system specificato che deve essere rimosso.</span><span class="sxs-lookup"><span data-stu-id="76f21-134">The path in the specified Filesystem that should be removed.</span></span>
<span data-ttu-id="76f21-135">Può essere un file o una directory nel formato 'directory/file.txt' o 'directory1/directory2/'</span><span class="sxs-lookup"><span data-stu-id="76f21-135">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76f21-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76f21-136">-Confirm</span></span>
<span data-ttu-id="76f21-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76f21-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76f21-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76f21-138">-WhatIf</span></span>
<span data-ttu-id="76f21-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="76f21-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76f21-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="76f21-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76f21-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76f21-141">CommonParameters</span></span>
<span data-ttu-id="76f21-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76f21-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76f21-143">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76f21-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76f21-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="76f21-144">INPUTS</span></span>

### <span data-ttu-id="76f21-145">System.String</span><span class="sxs-lookup"><span data-stu-id="76f21-145">System.String</span></span>

### <span data-ttu-id="76f21-146">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="76f21-146">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="76f21-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="76f21-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="76f21-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="76f21-148">OUTPUTS</span></span>

### <span data-ttu-id="76f21-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="76f21-149">System.Boolean</span></span>

## <span data-ttu-id="76f21-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="76f21-150">NOTES</span></span>

## <span data-ttu-id="76f21-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="76f21-151">RELATED LINKS</span></span>
