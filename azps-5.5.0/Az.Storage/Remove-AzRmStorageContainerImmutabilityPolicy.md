---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: eedeeb3311373c240cd564534d3438b948c7a0f6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190806"
---
# <span data-ttu-id="ede3e-101">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ede3e-101">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="ede3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ede3e-102">SYNOPSIS</span></span>
<span data-ttu-id="ede3e-103">Rimuove ImmutabilityPolicy di un contenitore BLOB Storage con un criterio sbloccato</span><span class="sxs-lookup"><span data-stu-id="ede3e-103">Removes ImmutabilityPolicy of a Storage blob container with an unlocked policy</span></span>

## <span data-ttu-id="ede3e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ede3e-104">SYNTAX</span></span>

### <span data-ttu-id="ede3e-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ede3e-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -Etag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ede3e-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="ede3e-106">AccountObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -Etag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ede3e-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="ede3e-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -Etag <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ede3e-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="ede3e-108">ImmutabilityPolicyObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ede3e-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ede3e-109">DESCRIPTION</span></span>
<span data-ttu-id="ede3e-110">Il cmdlet **Remove-AzRmStorageContainerImmutabilityPolicy** rimuove ImmutabilityPolicy di un contenitore BLOB Storage con un criterio sbloccato.</span><span class="sxs-lookup"><span data-stu-id="ede3e-110">The **Remove-AzRmStorageContainerImmutabilityPolicy** cmdlet removes ImmutabilityPolicy of a Storage blob container with an unlocked policy.</span></span>

## <span data-ttu-id="ede3e-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ede3e-111">EXAMPLES</span></span>

### <span data-ttu-id="ede3e-112">Esempio 1: Rimuovere un valore di ImmutabilityPolicy sbloccato di un contenitore BLOB Archiviazione con il nome dell'account di archiviazione e il nome del contenitore</span><span class="sxs-lookup"><span data-stu-id="ede3e-112">Example 1: Remove unlocked ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="ede3e-113">Questo comando rimuove un valore di ImmutabilityPolicy sbloccato di un contenitore BLOB Di archiviazione con il nome dell'account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="ede3e-113">This command removes unlocked ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="ede3e-114">Esempio 2: Rimuovere un valore unlocked ImmutabilityPolicy di un contenitore BLOB Storage con oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="ede3e-114">Example 2: Remove unlocked ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="ede3e-115">Questo comando rimuove il valore unlocked ImmutabilityPolicy di un contenitore BLOB Storage con oggetto account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ede3e-115">This command removes unlocked ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="ede3e-116">Esempio 3: Rimuovere un valore Unlocked ImmutabilityPolicy di un contenitore BLOB Storage con un oggetto contenitore</span><span class="sxs-lookup"><span data-stu-id="ede3e-116">Example 3: Remove unlocked ImmutabilityPolicy of a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag
```

<span data-ttu-id="ede3e-117">Questo comando rimuove il valore unlocked ImmutabilityPolicy di un contenitore BLOB Storage con oggetto contenitore Storage.</span><span class="sxs-lookup"><span data-stu-id="ede3e-117">This command removes unlocked ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="ede3e-118">Esempio 4: Rimuovere un oggetto ImmutabilityPolicy sbloccato di un contenitore BLOB Storage con oggetto ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ede3e-118">Example 4: Remove unlocked ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Remove-AzRmStorageContainerImmutabilityPolicy
```

<span data-ttu-id="ede3e-119">Questo comando rimuove il valore unlocked ImmutabilityPolicy di un contenitore BLOB Storage con oggetto ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="ede3e-119">This command removes unlocked ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span>

## <span data-ttu-id="ede3e-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ede3e-120">PARAMETERS</span></span>

### <span data-ttu-id="ede3e-121">-Container</span><span class="sxs-lookup"><span data-stu-id="ede3e-121">-Container</span></span>
<span data-ttu-id="ede3e-122">Oggetto contenitore di archiviazione</span><span class="sxs-lookup"><span data-stu-id="ede3e-122">Storage container object</span></span>

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

### <span data-ttu-id="ede3e-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="ede3e-123">-ContainerName</span></span>
<span data-ttu-id="ede3e-124">Nome contenitore</span><span class="sxs-lookup"><span data-stu-id="ede3e-124">Container Name</span></span>

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

### <span data-ttu-id="ede3e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ede3e-125">-DefaultProfile</span></span>
<span data-ttu-id="ede3e-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ede3e-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ede3e-127">-Etag</span><span class="sxs-lookup"><span data-stu-id="ede3e-127">-Etag</span></span>
<span data-ttu-id="ede3e-128">Etag dei criteri di non modificabilità.</span><span class="sxs-lookup"><span data-stu-id="ede3e-128">Immutability policy etag.</span></span>

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

### <span data-ttu-id="ede3e-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ede3e-129">-InputObject</span></span>
<span data-ttu-id="ede3e-130">Oggetto Unlocked ImmutabilityPolicy da rimuovere</span><span class="sxs-lookup"><span data-stu-id="ede3e-130">Unlocked ImmutabilityPolicy Object to Remove</span></span>

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

### <span data-ttu-id="ede3e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ede3e-131">-ResourceGroupName</span></span>
<span data-ttu-id="ede3e-132">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ede3e-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="ede3e-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="ede3e-133">-StorageAccount</span></span>
<span data-ttu-id="ede3e-134">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="ede3e-134">Storage account object</span></span>

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

### <span data-ttu-id="ede3e-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ede3e-135">-StorageAccountName</span></span>
<span data-ttu-id="ede3e-136">Nome account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ede3e-136">Storage Account Name.</span></span>

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

### <span data-ttu-id="ede3e-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ede3e-137">-Confirm</span></span>
<span data-ttu-id="ede3e-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ede3e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ede3e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ede3e-139">-WhatIf</span></span>
<span data-ttu-id="ede3e-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ede3e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ede3e-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ede3e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ede3e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ede3e-142">CommonParameters</span></span>
<span data-ttu-id="ede3e-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ede3e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ede3e-144">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ede3e-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ede3e-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="ede3e-145">INPUTS</span></span>

### <span data-ttu-id="ede3e-146">System.String</span><span class="sxs-lookup"><span data-stu-id="ede3e-146">System.String</span></span>

### <span data-ttu-id="ede3e-147">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ede3e-147">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="ede3e-148">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="ede3e-148">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="ede3e-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ede3e-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="ede3e-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ede3e-150">OUTPUTS</span></span>

### <span data-ttu-id="ede3e-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ede3e-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="ede3e-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="ede3e-152">NOTES</span></span>

## <span data-ttu-id="ede3e-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ede3e-153">RELATED LINKS</span></span>
