---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: eedeeb3311373c240cd564534d3438b948c7a0f6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190025"
---
# <span data-ttu-id="acc25-101">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="acc25-101">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="acc25-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="acc25-102">SYNOPSIS</span></span>
<span data-ttu-id="acc25-103">Rimuove ImmutabilityPolicy di un contenitore BLOB di archiviazione con un criterio sbloccato</span><span class="sxs-lookup"><span data-stu-id="acc25-103">Removes ImmutabilityPolicy of a Storage blob container with an unlocked policy</span></span>

## <span data-ttu-id="acc25-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="acc25-104">SYNTAX</span></span>

### <span data-ttu-id="acc25-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="acc25-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -Etag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="acc25-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="acc25-106">AccountObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -Etag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acc25-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="acc25-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -Etag <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acc25-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="acc25-108">ImmutabilityPolicyObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="acc25-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="acc25-109">DESCRIPTION</span></span>
<span data-ttu-id="acc25-110">Il cmdlet **Remove-AzRmStorageContainerImmutabilityPolicy** rimuove ImmutabilityPolicy di un contenitore di BLOB di archiviazione con un criterio sbloccato.</span><span class="sxs-lookup"><span data-stu-id="acc25-110">The **Remove-AzRmStorageContainerImmutabilityPolicy** cmdlet removes ImmutabilityPolicy of a Storage blob container with an unlocked policy.</span></span>

## <span data-ttu-id="acc25-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="acc25-111">EXAMPLES</span></span>

### <span data-ttu-id="acc25-112">Esempio 1: rimuovere il ImmutabilityPolicy sbloccato di un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore</span><span class="sxs-lookup"><span data-stu-id="acc25-112">Example 1: Remove unlocked ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="acc25-113">Questo comando rimuove ImmutabilityPolicy sbloccato di un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="acc25-113">This command removes unlocked ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="acc25-114">Esempio 2: rimuovere il ImmutabilityPolicy sbloccato di un contenitore di BLOB di archiviazione con l'oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="acc25-114">Example 2: Remove unlocked ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="acc25-115">Questo comando rimuove ImmutabilityPolicy sbloccato di un contenitore di BLOB di archiviazione con l'oggetto account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="acc25-115">This command removes unlocked ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="acc25-116">Esempio 3: rimuovere il ImmutabilityPolicy sbloccato di un contenitore di BLOB di archiviazione con l'oggetto contenitore</span><span class="sxs-lookup"><span data-stu-id="acc25-116">Example 3: Remove unlocked ImmutabilityPolicy of a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag
```

<span data-ttu-id="acc25-117">Questo comando rimuove ImmutabilityPolicy sbloccato di un contenitore BLOB di archiviazione con l'oggetto contenitore di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="acc25-117">This command removes unlocked ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="acc25-118">Esempio 4: rimuovere ImmutabilityPolicy sbloccato di un contenitore BLOB di archiviazione con l'oggetto ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="acc25-118">Example 4: Remove unlocked ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Remove-AzRmStorageContainerImmutabilityPolicy
```

<span data-ttu-id="acc25-119">Questo comando rimuove ImmutabilityPolicy sbloccato di un contenitore di BLOB di archiviazione con l'oggetto ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="acc25-119">This command removes unlocked ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span>

## <span data-ttu-id="acc25-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="acc25-120">PARAMETERS</span></span>

### <span data-ttu-id="acc25-121">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="acc25-121">-Container</span></span>
<span data-ttu-id="acc25-122">Oggetto contenitore di archiviazione</span><span class="sxs-lookup"><span data-stu-id="acc25-122">Storage container object</span></span>

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

### <span data-ttu-id="acc25-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="acc25-123">-ContainerName</span></span>
<span data-ttu-id="acc25-124">Nome contenitore</span><span class="sxs-lookup"><span data-stu-id="acc25-124">Container Name</span></span>

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

### <span data-ttu-id="acc25-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acc25-125">-DefaultProfile</span></span>
<span data-ttu-id="acc25-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="acc25-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="acc25-127">-ETag</span><span class="sxs-lookup"><span data-stu-id="acc25-127">-Etag</span></span>
<span data-ttu-id="acc25-128">Criteri di immutabilità ETag.</span><span class="sxs-lookup"><span data-stu-id="acc25-128">Immutability policy etag.</span></span>

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

### <span data-ttu-id="acc25-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="acc25-129">-InputObject</span></span>
<span data-ttu-id="acc25-130">Oggetto ImmutabilityPolicy sbloccato da rimuovere</span><span class="sxs-lookup"><span data-stu-id="acc25-130">Unlocked ImmutabilityPolicy Object to Remove</span></span>

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

### <span data-ttu-id="acc25-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acc25-131">-ResourceGroupName</span></span>
<span data-ttu-id="acc25-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="acc25-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="acc25-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="acc25-133">-StorageAccount</span></span>
<span data-ttu-id="acc25-134">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="acc25-134">Storage account object</span></span>

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

### <span data-ttu-id="acc25-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="acc25-135">-StorageAccountName</span></span>
<span data-ttu-id="acc25-136">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="acc25-136">Storage Account Name.</span></span>

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

### <span data-ttu-id="acc25-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="acc25-137">-Confirm</span></span>
<span data-ttu-id="acc25-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="acc25-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acc25-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acc25-139">-WhatIf</span></span>
<span data-ttu-id="acc25-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="acc25-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acc25-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="acc25-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acc25-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acc25-142">CommonParameters</span></span>
<span data-ttu-id="acc25-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acc25-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acc25-144">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acc25-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acc25-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="acc25-145">INPUTS</span></span>

### <span data-ttu-id="acc25-146">System. String</span><span class="sxs-lookup"><span data-stu-id="acc25-146">System.String</span></span>

### <span data-ttu-id="acc25-147">Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="acc25-147">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="acc25-148">Microsoft. Azure. Commands. Management. storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="acc25-148">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="acc25-149">Microsoft. Azure. Commands. Management. storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="acc25-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="acc25-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="acc25-150">OUTPUTS</span></span>

### <span data-ttu-id="acc25-151">Microsoft. Azure. Commands. Management. storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="acc25-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="acc25-152">Note</span><span class="sxs-lookup"><span data-stu-id="acc25-152">NOTES</span></span>

## <span data-ttu-id="acc25-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="acc25-153">RELATED LINKS</span></span>