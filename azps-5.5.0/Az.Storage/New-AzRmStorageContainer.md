---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
ms.openlocfilehash: 901061390c68853832bad14965620abad21817e8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197559"
---
# <span data-ttu-id="f04b6-101">New-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f04b6-101">New-AzRmStorageContainer</span></span>

## <span data-ttu-id="f04b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f04b6-102">SYNOPSIS</span></span>
<span data-ttu-id="f04b6-103">Crea un contenitore BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="f04b6-103">Creates a Storage blob container</span></span>

## <span data-ttu-id="f04b6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f04b6-104">SYNTAX</span></span>

### <span data-ttu-id="f04b6-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f04b6-105">AccountName (Default)</span></span>
```
New-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f04b6-106">AccountNameEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="f04b6-106">AccountNameEncryptionScope</span></span>
```
New-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 -DefaultEncryptionScope <String> -PreventEncryptionScopeOverride <Boolean> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f04b6-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="f04b6-107">AccountObject</span></span>
```
New-AzRmStorageContainer -StorageAccount <PSStorageAccount> -Name <String> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f04b6-108">AccountObjectEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="f04b6-108">AccountObjectEncryptionScope</span></span>
```
New-AzRmStorageContainer -StorageAccount <PSStorageAccount> -Name <String> -DefaultEncryptionScope <String>
 -PreventEncryptionScopeOverride <Boolean> [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f04b6-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f04b6-109">DESCRIPTION</span></span>
<span data-ttu-id="f04b6-110">Il cmdlet **New-AzRmStorageContainer** crea un contenitore BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="f04b6-110">The **New-AzRmStorageContainer** cmdlet creates a Storage blob container</span></span>

## <span data-ttu-id="f04b6-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f04b6-111">EXAMPLES</span></span>

### <span data-ttu-id="f04b6-112">Esempio 1: Creare un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore, con metadati</span><span class="sxs-lookup"><span data-stu-id="f04b6-112">Example 1: Create a Storage blob container with Storage account name and container name, with metadata</span></span>
```
PS C:\>New-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Metadata @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="f04b6-113">Questo comando crea un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore, con metadati.</span><span class="sxs-lookup"><span data-stu-id="f04b6-113">This command creates a Storage blob container with Storage account name and container name, with metadata.</span></span>

### <span data-ttu-id="f04b6-114">Esempio 2: Creare un contenitore BLOB di archiviazione con l'oggetto account di archiviazione e il nome del contenitore, con accesso pubblico come BLOB</span><span class="sxs-lookup"><span data-stu-id="f04b6-114">Example 2: Create a Storage blob container with Storage account object and container name, with public access as Blob</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>New-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess Blob
```

<span data-ttu-id="f04b6-115">Questo comando crea un contenitore BLOB di archiviazione con l'oggetto account di archiviazione e il nome del contenitore, con accesso pubblico come BLOB.</span><span class="sxs-lookup"><span data-stu-id="f04b6-115">This command creates a Storage blob container with Storage account object and container name, with public access as Blob.</span></span>

### <span data-ttu-id="f04b6-116">Esempio 3: Creare un contenitore di archiviazione con l'impostazione EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="f04b6-116">Example 3: Create a storage container with EncryptionScope setting</span></span>
```
PS C:\> $c = New-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name testcontainer -DefaultEncryptionScope "testscope" -PreventEncryptionScopeOverride $true

PS C:\> $c

   ResourceGroupName: myResourceGroup, StorageAccountName: myStorageAccount

Name          PublicAccess LastModified HasLegalHold HasImmutabilityPolicy
----          ------------ ------------ ------------ ---------------------
testcontainer                           False        False                

PS C:\> $c.DefaultEncryptionScope
testscope

PS C:\> $c.DenyEncryptionScopeOverride
True
```

<span data-ttu-id="f04b6-117">Questo comando crea un contenitore di archiviazione con un ambito di crittografia defalt e blocca l'override dell'ambito di crittografia rispetto all'impostazione predefinita del contenitore.</span><span class="sxs-lookup"><span data-stu-id="f04b6-117">This command creates a storage container with a defalt encryptionScope, and blocks override of encryption scope from the container default.</span></span>
<span data-ttu-id="f04b6-118">Visualizzare quindi le proprietà del contenitore correlate.</span><span class="sxs-lookup"><span data-stu-id="f04b6-118">Then show the related container properties.</span></span>

## <span data-ttu-id="f04b6-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f04b6-119">PARAMETERS</span></span>

### <span data-ttu-id="f04b6-120">-DefaultEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="f04b6-120">-DefaultEncryptionScope</span></span>
<span data-ttu-id="f04b6-121">Impostazione predefinita del contenitore da usare con l'ambito di crittografia specificato per tutte le operazioni di scrittura.</span><span class="sxs-lookup"><span data-stu-id="f04b6-121">Default the container to use specified encryption scope for all writes.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameEncryptionScope, AccountObjectEncryptionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f04b6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f04b6-122">-DefaultProfile</span></span>
<span data-ttu-id="f04b6-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f04b6-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f04b6-124">-Metadata</span><span class="sxs-lookup"><span data-stu-id="f04b6-124">-Metadata</span></span>
<span data-ttu-id="f04b6-125">Metadati contenitore</span><span class="sxs-lookup"><span data-stu-id="f04b6-125">Container Metadata</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f04b6-126">-Name</span><span class="sxs-lookup"><span data-stu-id="f04b6-126">-Name</span></span>
<span data-ttu-id="f04b6-127">Nome contenitore</span><span class="sxs-lookup"><span data-stu-id="f04b6-127">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f04b6-128">-PreventEncryptionScopeOverride</span><span class="sxs-lookup"><span data-stu-id="f04b6-128">-PreventEncryptionScopeOverride</span></span>
<span data-ttu-id="f04b6-129">Bloccare l'override dell'ambito di crittografia dal contenitore predefinito.</span><span class="sxs-lookup"><span data-stu-id="f04b6-129">Block override of encryption scope from the container default.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AccountNameEncryptionScope, AccountObjectEncryptionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f04b6-130">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="f04b6-130">-PublicAccess</span></span>
<span data-ttu-id="f04b6-131">Container PublicAccess</span><span class="sxs-lookup"><span data-stu-id="f04b6-131">Container PublicAccess</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSPublicAccess
Parameter Sets: (All)
Aliases:
Accepted values: Container, Blob, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f04b6-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f04b6-132">-ResourceGroupName</span></span>
<span data-ttu-id="f04b6-133">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f04b6-133">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameEncryptionScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f04b6-134">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="f04b6-134">-StorageAccount</span></span>
<span data-ttu-id="f04b6-135">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="f04b6-135">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject, AccountObjectEncryptionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f04b6-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f04b6-136">-StorageAccountName</span></span>
<span data-ttu-id="f04b6-137">Nome account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="f04b6-137">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameEncryptionScope
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f04b6-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f04b6-138">-Confirm</span></span>
<span data-ttu-id="f04b6-139">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f04b6-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f04b6-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f04b6-140">-WhatIf</span></span>
<span data-ttu-id="f04b6-141">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f04b6-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f04b6-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f04b6-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f04b6-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f04b6-143">CommonParameters</span></span>
<span data-ttu-id="f04b6-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f04b6-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f04b6-145">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f04b6-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f04b6-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="f04b6-146">INPUTS</span></span>

### <span data-ttu-id="f04b6-147">System.String</span><span class="sxs-lookup"><span data-stu-id="f04b6-147">System.String</span></span>

### <span data-ttu-id="f04b6-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f04b6-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="f04b6-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f04b6-149">OUTPUTS</span></span>

### <span data-ttu-id="f04b6-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="f04b6-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="f04b6-151">NOTE</span><span class="sxs-lookup"><span data-stu-id="f04b6-151">NOTES</span></span>

## <span data-ttu-id="f04b6-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f04b6-152">RELATED LINKS</span></span>
