---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2Item.md
ms.openlocfilehash: 06bb30dd98c491267675893192f61d4eb61529bf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022634"
---
# <span data-ttu-id="7c719-101">Remove-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="7c719-101">Remove-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="7c719-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7c719-102">SYNOPSIS</span></span>
<span data-ttu-id="7c719-103">Rimuovere un file o una directory.</span><span class="sxs-lookup"><span data-stu-id="7c719-103">Remove a file or directory.</span></span>

## <span data-ttu-id="7c719-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7c719-104">SYNTAX</span></span>

### <span data-ttu-id="7c719-105">ReceiveManual (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7c719-105">ReceiveManual (Default)</span></span>
```
Remove-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> [-Force] [-AsJob] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7c719-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="7c719-106">ItemPipeline</span></span>
```
Remove-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> [-Force] [-AsJob] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7c719-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7c719-107">DESCRIPTION</span></span>
<span data-ttu-id="7c719-108">Il cmdlet **Remove-AzDataLakeGen2Item** consente di rimuovere un file o una directory da un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7c719-108">The **Remove-AzDataLakeGen2Item** cmdlet removes a file or directory from a Storage account.</span></span>
<span data-ttu-id="7c719-109">Questo cmdlet funziona solo se lo spazio dei nomi gerarchico è abilitato per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7c719-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="7c719-110">Questo tipo di account può essere creato eseguendo il cmdlet "New-AzStorageAccount" con "-EnableHierarchicalNamespace $true".</span><span class="sxs-lookup"><span data-stu-id="7c719-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="7c719-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7c719-111">EXAMPLES</span></span>

### <span data-ttu-id="7c719-112">Esempio 1: rimuove una directory</span><span class="sxs-lookup"><span data-stu-id="7c719-112">Example 1: Removes a directory</span></span>
```
PS C:\>Remove-AzDataLakeGen2tem -FileSystem "filesystem1" -Path "dir1/"
```

<span data-ttu-id="7c719-113">Questo comando rimuove una directory da un filesystem.</span><span class="sxs-lookup"><span data-stu-id="7c719-113">This command removes a directory from a Filesystem.</span></span>

### <span data-ttu-id="7c719-114">Esempio 2: rimuove un file senza richiesta</span><span class="sxs-lookup"><span data-stu-id="7c719-114">Example 2: Removes a file without prompt</span></span>
```
PS C:\>Remove-AzDataLakeGen2tem -FileSystem "filesystem1" -Path "dir1/file1" -Force
```

<span data-ttu-id="7c719-115">Questo comando rimuove una directory da un filesystem, senza richiesta.</span><span class="sxs-lookup"><span data-stu-id="7c719-115">This command removes a directory from a Filesystem, without prompt.</span></span>

### <span data-ttu-id="7c719-116">Esempio 3: rimuovere tutti gli elementi in un filesystem con pipeline</span><span class="sxs-lookup"><span data-stu-id="7c719-116">Example 3: Remove all items in a Filesystem with pipeline</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" | Remove-AzDataLakeGen2Item -Force
```

<span data-ttu-id="7c719-117">Questo comando rimuove tutti gli elementi in un filesystem con pipeline.</span><span class="sxs-lookup"><span data-stu-id="7c719-117">This command removes all items in a Filesystem with pipeline.</span></span>

## <span data-ttu-id="7c719-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7c719-118">PARAMETERS</span></span>

### <span data-ttu-id="7c719-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c719-119">-AsJob</span></span>
<span data-ttu-id="7c719-120">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="7c719-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7c719-121">-Contesto</span><span class="sxs-lookup"><span data-stu-id="7c719-121">-Context</span></span>
<span data-ttu-id="7c719-122">Oggetto contesto di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="7c719-122">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="7c719-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c719-123">-DefaultProfile</span></span>
<span data-ttu-id="7c719-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7c719-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c719-125">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="7c719-125">-FileSystem</span></span>
<span data-ttu-id="7c719-126">Nome FileSystem</span><span class="sxs-lookup"><span data-stu-id="7c719-126">FileSystem name</span></span>

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

### <span data-ttu-id="7c719-127">-Force</span><span class="sxs-lookup"><span data-stu-id="7c719-127">-Force</span></span>
<span data-ttu-id="7c719-128">Forza per rimuovere il filesystem e tutto il contenuto</span><span class="sxs-lookup"><span data-stu-id="7c719-128">Force to remove the Filesystem and all content in it</span></span>

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

### <span data-ttu-id="7c719-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c719-129">-InputObject</span></span>
<span data-ttu-id="7c719-130">Oggetto Item di Azure datalake Gen2 da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="7c719-130">Azure Datalake Gen2 Item Object to remove.</span></span>

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

### <span data-ttu-id="7c719-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c719-131">-PassThru</span></span>
<span data-ttu-id="7c719-132">Restituisce se il filesystem specificato viene rimosso correttamente</span><span class="sxs-lookup"><span data-stu-id="7c719-132">Return whether the specified Filesystem is successfully removed</span></span>

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

### <span data-ttu-id="7c719-133">-Path</span><span class="sxs-lookup"><span data-stu-id="7c719-133">-Path</span></span>
<span data-ttu-id="7c719-134">Il percorso nel filesystem specificato che deve essere rimosso.</span><span class="sxs-lookup"><span data-stu-id="7c719-134">The path in the specified Filesystem that should be removed.</span></span>
<span data-ttu-id="7c719-135">Può essere un file o una directory nel formato ' directory/file.txt' o ' directory1/directory2/'</span><span class="sxs-lookup"><span data-stu-id="7c719-135">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

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

### <span data-ttu-id="7c719-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7c719-136">-Confirm</span></span>
<span data-ttu-id="7c719-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c719-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c719-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c719-138">-WhatIf</span></span>
<span data-ttu-id="7c719-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7c719-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c719-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7c719-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c719-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c719-141">CommonParameters</span></span>
<span data-ttu-id="7c719-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c719-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c719-143">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c719-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c719-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7c719-144">INPUTS</span></span>

### <span data-ttu-id="7c719-145">System. String</span><span class="sxs-lookup"><span data-stu-id="7c719-145">System.String</span></span>

### <span data-ttu-id="7c719-146">Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="7c719-146">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="7c719-147">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7c719-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7c719-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7c719-148">OUTPUTS</span></span>

### <span data-ttu-id="7c719-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7c719-149">System.Boolean</span></span>

## <span data-ttu-id="7c719-150">Note</span><span class="sxs-lookup"><span data-stu-id="7c719-150">NOTES</span></span>

## <span data-ttu-id="7c719-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7c719-151">RELATED LINKS</span></span>
