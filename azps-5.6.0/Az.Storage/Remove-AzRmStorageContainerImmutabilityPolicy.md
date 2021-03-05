---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: d94b84455f18a2823612ae1592e9cb337a4be3c7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970157"
---
# <span data-ttu-id="c8cbb-101">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="c8cbb-101">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="c8cbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8cbb-102">SYNOPSIS</span></span>
<span data-ttu-id="c8cbb-103">Rimuove ImmutabilityPolicy di un contenitore BLOB Archiviazione con un criterio sbloccato</span><span class="sxs-lookup"><span data-stu-id="c8cbb-103">Removes ImmutabilityPolicy of a Storage blob container with an unlocked policy</span></span>

## <span data-ttu-id="c8cbb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c8cbb-104">SYNTAX</span></span>

### <span data-ttu-id="c8cbb-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c8cbb-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -Etag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c8cbb-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="c8cbb-106">AccountObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -Etag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8cbb-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="c8cbb-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -Etag <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8cbb-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="c8cbb-108">ImmutabilityPolicyObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8cbb-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c8cbb-109">DESCRIPTION</span></span>
<span data-ttu-id="c8cbb-110">Il cmdlet **Remove-AzRmStorageContainerImmutabilityPolicy** rimuove ImmutabilityPolicy di un contenitore BLOB Storage con un criterio sbloccato.</span><span class="sxs-lookup"><span data-stu-id="c8cbb-110">The **Remove-AzRmStorageContainerImmutabilityPolicy** cmdlet removes ImmutabilityPolicy of a Storage blob container with an unlocked policy.</span></span>

## <span data-ttu-id="c8cbb-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c8cbb-111">EXAMPLES</span></span>

### <span data-ttu-id="c8cbb-112">Esempio 1: Rimuovere un valore di ImmutabilityPolicy sbloccato di un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore</span><span class="sxs-lookup"><span data-stu-id="c8cbb-112">Example 1: Remove unlocked ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="c8cbb-113">Questo comando rimuove un valore di ImmutabilityPolicy sbloccato di un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="c8cbb-113">This command removes unlocked ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="c8cbb-114">Esempio 2: Rimuovere un valore unlocked ImmutabilityPolicy di un contenitore BLOB Storage con oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="c8cbb-114">Example 2: Remove unlocked ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="c8cbb-115">Questo comando rimuove il valore unlocked ImmutabilityPolicy di un contenitore BLOB Storage con oggetto account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c8cbb-115">This command removes unlocked ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="c8cbb-116">Esempio 3: Rimuovere un valore unlocked ImmutabilityPolicy di un contenitore BLOB Storage con un oggetto contenitore</span><span class="sxs-lookup"><span data-stu-id="c8cbb-116">Example 3: Remove unlocked ImmutabilityPolicy of a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag
```

<span data-ttu-id="c8cbb-117">Questo comando rimuove il valore unlocked ImmutabilityPolicy di un contenitore BLOB Archiviazione con oggetto contenitore di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c8cbb-117">This command removes unlocked ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="c8cbb-118">Esempio 4: Rimuovere un oggetto ImmutabilityPolicy sbloccato di un contenitore BLOB Storage con oggetto ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="c8cbb-118">Example 4: Remove unlocked ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Remove-AzRmStorageContainerImmutabilityPolicy
```

<span data-ttu-id="c8cbb-119">Questo comando rimuove il valore unlocked ImmutabilityPolicy di un contenitore BLOB Storage con oggetto ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="c8cbb-119">This command removes unlocked ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span>

## <span data-ttu-id="c8cbb-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8cbb-120">PARAMETERS</span></span>

### <span data-ttu-id="c8cbb-121">-Container</span><span class="sxs-lookup"><span data-stu-id="c8cbb-121">-Container</span></span>
<span data-ttu-id="c8cbb-122">Oggetto contenitore di archiviazione</span><span class="sxs-lookup"><span data-stu-id="c8cbb-122">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8cbb-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="c8cbb-123">-ContainerName</span></span>
<span data-ttu-id="c8cbb-124">Nome contenitore</span><span class="sxs-lookup"><span data-stu-id="c8cbb-124">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8cbb-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8cbb-125">-DefaultProfile</span></span>
<span data-ttu-id="c8cbb-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c8cbb-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8cbb-127">-Etag</span><span class="sxs-lookup"><span data-stu-id="c8cbb-127">-Etag</span></span>
<span data-ttu-id="c8cbb-128">Etag dei criteri di non modificabilità.</span><span class="sxs-lookup"><span data-stu-id="c8cbb-128">Immutability policy etag.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject, ContainerObject
Aliases: IfMatch

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8cbb-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8cbb-129">-InputObject</span></span>
<span data-ttu-id="c8cbb-130">Oggetto Unlocked ImmutabilityPolicy da rimuovere</span><span class="sxs-lookup"><span data-stu-id="c8cbb-130">Unlocked ImmutabilityPolicy Object to Remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy
Parameter Sets: ImmutabilityPolicyObject
Aliases: ImmutabilityPolicy

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8cbb-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8cbb-131">-ResourceGroupName</span></span>
<span data-ttu-id="c8cbb-132">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c8cbb-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="c8cbb-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="c8cbb-133">-StorageAccount</span></span>
<span data-ttu-id="c8cbb-134">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="c8cbb-134">Storage account object</span></span>

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

### <span data-ttu-id="c8cbb-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c8cbb-135">-StorageAccountName</span></span>
<span data-ttu-id="c8cbb-136">Nome account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c8cbb-136">Storage Account Name.</span></span>

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

### <span data-ttu-id="c8cbb-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c8cbb-137">-Confirm</span></span>
<span data-ttu-id="c8cbb-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8cbb-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8cbb-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8cbb-139">-WhatIf</span></span>
<span data-ttu-id="c8cbb-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c8cbb-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8cbb-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c8cbb-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8cbb-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8cbb-142">CommonParameters</span></span>
<span data-ttu-id="c8cbb-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8cbb-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8cbb-144">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8cbb-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8cbb-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="c8cbb-145">INPUTS</span></span>

### <span data-ttu-id="c8cbb-146">System.String</span><span class="sxs-lookup"><span data-stu-id="c8cbb-146">System.String</span></span>

### <span data-ttu-id="c8cbb-147">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c8cbb-147">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="c8cbb-148">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="c8cbb-148">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="c8cbb-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="c8cbb-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="c8cbb-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c8cbb-150">OUTPUTS</span></span>

### <span data-ttu-id="c8cbb-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="c8cbb-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="c8cbb-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="c8cbb-152">NOTES</span></span>

## <span data-ttu-id="c8cbb-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c8cbb-153">RELATED LINKS</span></span>
