---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 74963ef36a33bed6145d315f5792aa776a36bc7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517312"
---
# <span data-ttu-id="99991-101">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="99991-101">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="99991-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="99991-102">SYNOPSIS</span></span>
<span data-ttu-id="99991-103">Rimuove ImmutabilityPolicy di contenitori BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="99991-103">Removes ImmutabilityPolicy of a Storage blob containers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99991-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="99991-104">SYNTAX</span></span>

### <span data-ttu-id="99991-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="99991-105">AccountName (Default)</span></span>
```
Remove-AzureRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-ContainerName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="99991-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="99991-106">AccountObject</span></span>
```
Remove-AzureRmStorageContainerImmutabilityPolicy [-ContainerName] <String> -StorageAccount <PSStorageAccount>
 [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99991-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="99991-107">ContainerObject</span></span>
```
Remove-AzureRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99991-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="99991-108">ImmutabilityPolicyObject</span></span>
```
Remove-AzureRmStorageContainerImmutabilityPolicy -InputObject <PSImmutabilityPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99991-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="99991-109">DESCRIPTION</span></span>
<span data-ttu-id="99991-110">Il cmdlet **Remove-AzureRmStorageContainerImmutabilityPolicy** rimuove ImmutabilityPolicy di contenitori BLOB di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="99991-110">The **Remove-AzureRmStorageContainerImmutabilityPolicy** cmdlet removes ImmutabilityPolicy of a Storage blob containers.</span></span>

## <span data-ttu-id="99991-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="99991-111">EXAMPLES</span></span>

### <span data-ttu-id="99991-112">Esempio 1: rimuovere ImmutabilityPolicy di un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore</span><span class="sxs-lookup"><span data-stu-id="99991-112">Example 1: Remove ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Remove-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="99991-113">Questo comando rimuove ImmutabilityPolicy di un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="99991-113">This command removes ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="99991-114">Esempio 2: rimuovere ImmutabilityPolicy di un contenitore BLOB di archiviazione con l'oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="99991-114">Example 2: Remove ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Remove-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="99991-115">Questo comando rimuove ImmutabilityPolicy di un contenitore BLOB di archiviazione con l'oggetto account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="99991-115">This command removes ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="99991-116">Esempio 3: rimuovere ImmutabilityPolicyof un contenitore BLOB di archiviazione con l'oggetto contenitore</span><span class="sxs-lookup"><span data-stu-id="99991-116">Example 3: Remove ImmutabilityPolicyof a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Remove-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag
```

<span data-ttu-id="99991-117">Questo comando rimuove ImmutabilityPolicy di un contenitore BLOB di archiviazione con l'oggetto contenitore di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="99991-117">This command removes ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="99991-118">Esempio 4: rimuovere ImmutabilityPolicy di un contenitore BLOB di archiviazione con l'oggetto ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="99991-118">Example 4: Remove ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Remove-AzureRmStorageContainerImmutabilityPolicy
```

<span data-ttu-id="99991-119">Questo comando rimuove ImmutabilityPolicy di un contenitore di BLOB di archiviazione con l'oggetto ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="99991-119">This command removes ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span>

## <span data-ttu-id="99991-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="99991-120">PARAMETERS</span></span>

### <span data-ttu-id="99991-121">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="99991-121">-Container</span></span>
<span data-ttu-id="99991-122">Oggetto contenitore di archiviazione</span><span class="sxs-lookup"><span data-stu-id="99991-122">Storage container object</span></span>

```yaml
Type: PSContainer
Parameter Sets: ContainerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99991-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="99991-123">-ContainerName</span></span>
<span data-ttu-id="99991-124">Nome contenitore</span><span class="sxs-lookup"><span data-stu-id="99991-124">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject
Aliases: N

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99991-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99991-125">-DefaultProfile</span></span>
<span data-ttu-id="99991-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="99991-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99991-127">-ETag</span><span class="sxs-lookup"><span data-stu-id="99991-127">-Etag</span></span>
<span data-ttu-id="99991-128">Criteri di immutabilità ETag.</span><span class="sxs-lookup"><span data-stu-id="99991-128">Immutability policy etag.</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject, ContainerObject
Aliases: IfMatch

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99991-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99991-129">-InputObject</span></span>
<span data-ttu-id="99991-130">Oggetto ImmutabilityPolicy da rimuovere</span><span class="sxs-lookup"><span data-stu-id="99991-130">ImmutabilityPolicy Object to Remove</span></span>

```yaml
Type: PSImmutabilityPolicy
Parameter Sets: ImmutabilityPolicyObject
Aliases: ImmutabilityPolicy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99991-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99991-131">-ResourceGroupName</span></span>
<span data-ttu-id="99991-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="99991-132">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99991-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="99991-133">-StorageAccount</span></span>
<span data-ttu-id="99991-134">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="99991-134">Storage account object</span></span>

```yaml
Type: PSStorageAccount
Parameter Sets: AccountObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99991-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="99991-135">-StorageAccountName</span></span>
<span data-ttu-id="99991-136">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="99991-136">Storage Account Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99991-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="99991-137">-Confirm</span></span>
<span data-ttu-id="99991-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99991-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99991-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99991-139">-WhatIf</span></span>
<span data-ttu-id="99991-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="99991-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99991-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="99991-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99991-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99991-142">CommonParameters</span></span>
<span data-ttu-id="99991-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99991-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99991-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99991-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99991-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="99991-145">INPUTS</span></span>

### <span data-ttu-id="99991-146">System. String</span><span class="sxs-lookup"><span data-stu-id="99991-146">System.String</span></span>
<span data-ttu-id="99991-147">Microsoft. Azure. Commands. Management. storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="99991-147">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="99991-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="99991-148">OUTPUTS</span></span>

### <span data-ttu-id="99991-149">Microsoft. Azure. Commands. Management. storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="99991-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="99991-150">Note</span><span class="sxs-lookup"><span data-stu-id="99991-150">NOTES</span></span>

## <span data-ttu-id="99991-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="99991-151">RELATED LINKS</span></span>

