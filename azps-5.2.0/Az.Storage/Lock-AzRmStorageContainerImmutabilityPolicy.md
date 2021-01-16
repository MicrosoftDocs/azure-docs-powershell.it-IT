---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/lock-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Lock-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Lock-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 0cb3a4e65d8e464dda85e18e12dc106620e3eee8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349528"
---
# <span data-ttu-id="8bc92-101">Lock-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="8bc92-101">Lock-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="8bc92-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8bc92-102">SYNOPSIS</span></span>
<span data-ttu-id="8bc92-103">Blocca ImmutabilityPolicy di un contenitore BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="8bc92-103">Locks ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="8bc92-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8bc92-104">SYNTAX</span></span>

### <span data-ttu-id="8bc92-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8bc92-105">AccountName (Default)</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -Etag <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bc92-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="8bc92-106">AccountObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -Etag <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bc92-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="8bc92-107">ContainerObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -Etag <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bc92-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="8bc92-108">ImmutabilityPolicyObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bc92-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8bc92-109">DESCRIPTION</span></span>
<span data-ttu-id="8bc92-110">Il cmdlet **Lock-AzRmStorageContainerImmutabilityPolicy** blocca ImmutabilityPolicy di contenitori BLOB di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="8bc92-110">The **Lock-AzRmStorageContainerImmutabilityPolicy** cmdlet locks ImmutabilityPolicy of a Storage blob containers.</span></span>

## <span data-ttu-id="8bc92-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8bc92-111">EXAMPLES</span></span>

### <span data-ttu-id="8bc92-112">Esempio 1: bloccare ImmutabilityPolicy di un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore</span><span class="sxs-lookup"><span data-stu-id="8bc92-112">Example 1: Lock ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="8bc92-113">Questo comando blocca ImmutabilityPolicy di un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="8bc92-113">This command Locks ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="8bc92-114">Esempio 2: bloccare ImmutabilityPolicy di un contenitore BLOB di archiviazione con l'oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="8bc92-114">Example 2: Lock ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag -Force
```

<span data-ttu-id="8bc92-115">Questo comando blocca ImmutabilityPolicy di un contenitore di BLOB di archiviazione con l'oggetto account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="8bc92-115">This command locks ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="8bc92-116">Esempio 3: bloccare ImmutabilityPolicyof un contenitore BLOB di archiviazione con l'oggetto contenitore</span><span class="sxs-lookup"><span data-stu-id="8bc92-116">Example 3: Lock ImmutabilityPolicyof a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag -Force
```

<span data-ttu-id="8bc92-117">Questo comando blocca ImmutabilityPolicy di un contenitore BLOB di archiviazione con l'oggetto contenitore di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="8bc92-117">This command locks ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="8bc92-118">Esempio 4: bloccare ImmutabilityPolicy di un contenitore di BLOB di archiviazione con l'oggetto ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="8bc92-118">Example 4: Lock ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Lock-AzRmStorageContainerImmutabilityPolicy -Force
```

<span data-ttu-id="8bc92-119">Questo comando blocca ImmutabilityPolicy di un contenitore di BLOB di archiviazione con l'oggetto ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="8bc92-119">This command locks ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> 

## <span data-ttu-id="8bc92-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8bc92-120">PARAMETERS</span></span>

### <span data-ttu-id="8bc92-121">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="8bc92-121">-Container</span></span>
<span data-ttu-id="8bc92-122">Oggetto contenitore di archiviazione</span><span class="sxs-lookup"><span data-stu-id="8bc92-122">Storage container object</span></span>

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

### <span data-ttu-id="8bc92-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="8bc92-123">-ContainerName</span></span>
<span data-ttu-id="8bc92-124">Nome contenitore</span><span class="sxs-lookup"><span data-stu-id="8bc92-124">Container Name</span></span>

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

### <span data-ttu-id="8bc92-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bc92-125">-DefaultProfile</span></span>
<span data-ttu-id="8bc92-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8bc92-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8bc92-127">-ETag</span><span class="sxs-lookup"><span data-stu-id="8bc92-127">-Etag</span></span>
<span data-ttu-id="8bc92-128">Criteri di immutabilità ETag.</span><span class="sxs-lookup"><span data-stu-id="8bc92-128">Immutability policy etag.</span></span>

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

### <span data-ttu-id="8bc92-129">-Force</span><span class="sxs-lookup"><span data-stu-id="8bc92-129">-Force</span></span>
<span data-ttu-id="8bc92-130">Forza per rimuovere il ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="8bc92-130">Force to remove the ImmutabilityPolicy.</span></span>

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

### <span data-ttu-id="8bc92-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8bc92-131">-InputObject</span></span>
<span data-ttu-id="8bc92-132">Oggetto ImmutabilityPolicy da rimuovere</span><span class="sxs-lookup"><span data-stu-id="8bc92-132">ImmutabilityPolicy Object to Remove</span></span>

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

### <span data-ttu-id="8bc92-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bc92-133">-ResourceGroupName</span></span>
<span data-ttu-id="8bc92-134">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8bc92-134">Resource Group Name.</span></span>

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

### <span data-ttu-id="8bc92-135">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="8bc92-135">-StorageAccount</span></span>
<span data-ttu-id="8bc92-136">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="8bc92-136">Storage account object</span></span>

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

### <span data-ttu-id="8bc92-137">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8bc92-137">-StorageAccountName</span></span>
<span data-ttu-id="8bc92-138">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="8bc92-138">Storage Account Name.</span></span>

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

### <span data-ttu-id="8bc92-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8bc92-139">-Confirm</span></span>
<span data-ttu-id="8bc92-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bc92-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bc92-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bc92-141">-WhatIf</span></span>
<span data-ttu-id="8bc92-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8bc92-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bc92-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8bc92-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bc92-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bc92-144">CommonParameters</span></span>
<span data-ttu-id="8bc92-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bc92-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bc92-146">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bc92-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bc92-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8bc92-147">INPUTS</span></span>

### <span data-ttu-id="8bc92-148">System. String</span><span class="sxs-lookup"><span data-stu-id="8bc92-148">System.String</span></span>

### <span data-ttu-id="8bc92-149">Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8bc92-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="8bc92-150">Microsoft. Azure. Commands. Management. storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="8bc92-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="8bc92-151">Microsoft. Azure. Commands. Management. storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="8bc92-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="8bc92-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8bc92-152">OUTPUTS</span></span>

### <span data-ttu-id="8bc92-153">Microsoft. Azure. Commands. Management. storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="8bc92-153">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="8bc92-154">Note</span><span class="sxs-lookup"><span data-stu-id="8bc92-154">NOTES</span></span>

## <span data-ttu-id="8bc92-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8bc92-155">RELATED LINKS</span></span>
