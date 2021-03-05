---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/update-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageContainer.md
ms.openlocfilehash: 696070e19f1810ab352abde4ad6248f4bf42b180
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973325"
---
# <span data-ttu-id="553fb-101">Update-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="553fb-101">Update-AzRmStorageContainer</span></span>

## <span data-ttu-id="553fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="553fb-102">SYNOPSIS</span></span>
<span data-ttu-id="553fb-103">Modifica un contenitore BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="553fb-103">Modifies a Storage blob container</span></span>

## <span data-ttu-id="553fb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="553fb-104">SYNTAX</span></span>

### <span data-ttu-id="553fb-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="553fb-105">AccountName (Default)</span></span>
```
Update-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="553fb-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="553fb-106">AccountObject</span></span>
```
Update-AzRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="553fb-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="553fb-107">ContainerObject</span></span>
```
Update-AzRmStorageContainer -InputObject <PSContainer> [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="553fb-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="553fb-108">DESCRIPTION</span></span>
<span data-ttu-id="553fb-109">Il cmdlet **Update-AzRmStorageContainer** modifica un contenitore BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="553fb-109">The **Update-AzRmStorageContainer** cmdlet modifies a Storage blob container</span></span>

## <span data-ttu-id="553fb-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="553fb-110">EXAMPLES</span></span>

### <span data-ttu-id="553fb-111">Esempio 1: Modifica dei metadati e dell'accesso pubblico di un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore</span><span class="sxs-lookup"><span data-stu-id="553fb-111">Example 1: Modifies a Storage blob container's metadata and public access with Storage account name and container name</span></span>
```
PS C:\>Update-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -PublicAccess Container -Metadata @{tag0="value0";tag1="value1"}
```

<span data-ttu-id="553fb-112">Questo comando modifica i metadati e l'accesso pubblico di un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="553fb-112">This command modifies a Storage blob container's metadata and public access with Storage account name and container name.</span></span>

### <span data-ttu-id="553fb-113">Esempio 2: Disabilitare l'accesso pubblico in un contenitore BLOB archiviazione con l'oggetto account di archiviazione e il nome del contenitore</span><span class="sxs-lookup"><span data-stu-id="553fb-113">Example 2: Disable public access on a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Update-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess None
```

<span data-ttu-id="553fb-114">Questo comando disabilita l'accesso pubblico in un contenitore BLOB di archiviazione con l'oggetto account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="553fb-114">This command disables public access on a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="553fb-115">Esempio 3: Impostare l'accesso pubblico come BLOB per tutti i contenitori BLOB di archiviazione in un account di archiviazione con pipeline</span><span class="sxs-lookup"><span data-stu-id="553fb-115">Example 3: Set public access as Blob for all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Update-AzRmStorageContainer -PublicAccess Blob
```

<span data-ttu-id="553fb-116">Questo comando imposta l'accesso pubblico come BLOB per tutti i contenitori BLOB di archiviazione in un account di archiviazione con pipeline.</span><span class="sxs-lookup"><span data-stu-id="553fb-116">This command set public access as Blob for all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="553fb-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="553fb-117">PARAMETERS</span></span>

### <span data-ttu-id="553fb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="553fb-118">-DefaultProfile</span></span>
<span data-ttu-id="553fb-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="553fb-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="553fb-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="553fb-120">-InputObject</span></span>
<span data-ttu-id="553fb-121">Oggetto contenitore di archiviazione</span><span class="sxs-lookup"><span data-stu-id="553fb-121">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject
Aliases: Container

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="553fb-122">-Metadata</span><span class="sxs-lookup"><span data-stu-id="553fb-122">-Metadata</span></span>
<span data-ttu-id="553fb-123">Metadati contenitore</span><span class="sxs-lookup"><span data-stu-id="553fb-123">Container Metadata</span></span>

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

### <span data-ttu-id="553fb-124">-Name</span><span class="sxs-lookup"><span data-stu-id="553fb-124">-Name</span></span>
<span data-ttu-id="553fb-125">Nome contenitore</span><span class="sxs-lookup"><span data-stu-id="553fb-125">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="553fb-126">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="553fb-126">-PublicAccess</span></span>
<span data-ttu-id="553fb-127">Container PublicAccess</span><span class="sxs-lookup"><span data-stu-id="553fb-127">Container PublicAccess</span></span>

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

### <span data-ttu-id="553fb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="553fb-128">-ResourceGroupName</span></span>
<span data-ttu-id="553fb-129">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="553fb-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="553fb-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="553fb-130">-StorageAccount</span></span>
<span data-ttu-id="553fb-131">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="553fb-131">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="553fb-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="553fb-132">-StorageAccountName</span></span>
<span data-ttu-id="553fb-133">Nome account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="553fb-133">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="553fb-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="553fb-134">-Confirm</span></span>
<span data-ttu-id="553fb-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="553fb-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="553fb-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="553fb-136">-WhatIf</span></span>
<span data-ttu-id="553fb-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="553fb-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="553fb-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="553fb-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="553fb-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="553fb-139">CommonParameters</span></span>
<span data-ttu-id="553fb-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="553fb-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="553fb-141">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="553fb-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="553fb-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="553fb-142">INPUTS</span></span>

### <span data-ttu-id="553fb-143">System.String</span><span class="sxs-lookup"><span data-stu-id="553fb-143">System.String</span></span>

### <span data-ttu-id="553fb-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="553fb-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="553fb-145">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="553fb-145">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="553fb-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="553fb-146">OUTPUTS</span></span>

### <span data-ttu-id="553fb-147">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="553fb-147">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="553fb-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="553fb-148">NOTES</span></span>

## <span data-ttu-id="553fb-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="553fb-149">RELATED LINKS</span></span>
