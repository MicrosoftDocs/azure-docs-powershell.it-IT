---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/lock-azurermstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Lock-AzureRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Lock-AzureRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 726dc9043c1082f97e32da46305cf81192e1806c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507311"
---
# <span data-ttu-id="3ab06-101">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="3ab06-101">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="3ab06-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3ab06-102">SYNOPSIS</span></span>
<span data-ttu-id="3ab06-103">Blocca ImmutabilityPolicy di un contenitore BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="3ab06-103">Locks ImmutabilityPolicy of a Storage blob containers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ab06-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3ab06-104">SYNTAX</span></span>

### <span data-ttu-id="3ab06-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3ab06-105">AccountName (Default)</span></span>
```
Lock-AzureRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-ContainerName] <String> [-Etag] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ab06-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="3ab06-106">AccountObject</span></span>
```
Lock-AzureRmStorageContainerImmutabilityPolicy [-ContainerName] <String> -StorageAccount <PSStorageAccount>
 [-Etag] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ab06-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="3ab06-107">ContainerObject</span></span>
```
Lock-AzureRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ab06-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="3ab06-108">ImmutabilityPolicyObject</span></span>
```
Lock-AzureRmStorageContainerImmutabilityPolicy -InputObject <PSImmutabilityPolicy> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ab06-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ab06-109">DESCRIPTION</span></span>
<span data-ttu-id="3ab06-110">Il cmdlet **Lock-AzureRmStorageContainerImmutabilityPolicy** blocca ImmutabilityPolicy di contenitori BLOB di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3ab06-110">The **Lock-AzureRmStorageContainerImmutabilityPolicy** cmdlet locks ImmutabilityPolicy of a Storage blob containers.</span></span>

## <span data-ttu-id="3ab06-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3ab06-111">EXAMPLES</span></span>

### <span data-ttu-id="3ab06-112">Esempio 1: bloccare ImmutabilityPolicy di un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore</span><span class="sxs-lookup"><span data-stu-id="3ab06-112">Example 1: Lock ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Lock-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="3ab06-113">Questo comando blocca ImmutabilityPolicy di un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="3ab06-113">This command Locks ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="3ab06-114">Esempio 2: bloccare ImmutabilityPolicy di un contenitore BLOB di archiviazione con l'oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="3ab06-114">Example 2: Lock ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Lock-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag -Force
```

<span data-ttu-id="3ab06-115">Questo comando blocca ImmutabilityPolicy di un contenitore di BLOB di archiviazione con l'oggetto account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3ab06-115">This command locks ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="3ab06-116">Esempio 3: bloccare ImmutabilityPolicyof un contenitore BLOB di archiviazione con l'oggetto contenitore</span><span class="sxs-lookup"><span data-stu-id="3ab06-116">Example 3: Lock ImmutabilityPolicyof a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Lock-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag -Force
```

<span data-ttu-id="3ab06-117">Questo comando blocca ImmutabilityPolicy di un contenitore BLOB di archiviazione con l'oggetto contenitore di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3ab06-117">This command locks ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="3ab06-118">Esempio 4: bloccare ImmutabilityPolicy di un contenitore di BLOB di archiviazione con l'oggetto ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="3ab06-118">Example 4: Lock ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Lock-AzureRmStorageContainerImmutabilityPolicy -Force
```

<span data-ttu-id="3ab06-119">Questo comando blocca ImmutabilityPolicy di un contenitore di BLOB di archiviazione con l'oggetto ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="3ab06-119">This command locks ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> 

## <span data-ttu-id="3ab06-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3ab06-120">PARAMETERS</span></span>

### <span data-ttu-id="3ab06-121">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="3ab06-121">-Container</span></span>
<span data-ttu-id="3ab06-122">Oggetto contenitore di archiviazione</span><span class="sxs-lookup"><span data-stu-id="3ab06-122">Storage container object</span></span>

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

### <span data-ttu-id="3ab06-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="3ab06-123">-ContainerName</span></span>
<span data-ttu-id="3ab06-124">Nome contenitore</span><span class="sxs-lookup"><span data-stu-id="3ab06-124">Container Name</span></span>

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

### <span data-ttu-id="3ab06-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ab06-125">-DefaultProfile</span></span>
<span data-ttu-id="3ab06-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3ab06-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ab06-127">-ETag</span><span class="sxs-lookup"><span data-stu-id="3ab06-127">-Etag</span></span>
<span data-ttu-id="3ab06-128">Criteri di immutabilità ETag.</span><span class="sxs-lookup"><span data-stu-id="3ab06-128">Immutability policy etag.</span></span>

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

### <span data-ttu-id="3ab06-129">-Force</span><span class="sxs-lookup"><span data-stu-id="3ab06-129">-Force</span></span>
<span data-ttu-id="3ab06-130">Forza per rimuovere il ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="3ab06-130">Force to remove the ImmutabilityPolicy.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ab06-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ab06-131">-InputObject</span></span>
<span data-ttu-id="3ab06-132">Oggetto ImmutabilityPolicy da rimuovere</span><span class="sxs-lookup"><span data-stu-id="3ab06-132">ImmutabilityPolicy Object to Remove</span></span>

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

### <span data-ttu-id="3ab06-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ab06-133">-ResourceGroupName</span></span>
<span data-ttu-id="3ab06-134">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3ab06-134">Resource Group Name.</span></span>

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

### <span data-ttu-id="3ab06-135">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="3ab06-135">-StorageAccount</span></span>
<span data-ttu-id="3ab06-136">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="3ab06-136">Storage account object</span></span>

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

### <span data-ttu-id="3ab06-137">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3ab06-137">-StorageAccountName</span></span>
<span data-ttu-id="3ab06-138">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3ab06-138">Storage Account Name.</span></span>

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

### <span data-ttu-id="3ab06-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3ab06-139">-Confirm</span></span>
<span data-ttu-id="3ab06-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ab06-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ab06-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ab06-141">-WhatIf</span></span>
<span data-ttu-id="3ab06-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3ab06-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ab06-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3ab06-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ab06-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ab06-144">CommonParameters</span></span>
<span data-ttu-id="3ab06-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ab06-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ab06-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ab06-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ab06-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3ab06-147">INPUTS</span></span>

### <span data-ttu-id="3ab06-148">System. String</span><span class="sxs-lookup"><span data-stu-id="3ab06-148">System.String</span></span>
<span data-ttu-id="3ab06-149">Microsoft. Azure. Commands. Management. storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="3ab06-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="3ab06-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3ab06-150">OUTPUTS</span></span>

### <span data-ttu-id="3ab06-151">Microsoft. Azure. Commands. Management. storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="3ab06-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="3ab06-152">Note</span><span class="sxs-lookup"><span data-stu-id="3ab06-152">NOTES</span></span>

## <span data-ttu-id="3ab06-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3ab06-153">RELATED LINKS</span></span>

