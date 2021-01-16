---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 9631855803b4ad16312c907c1d1c747b3aee6fdf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376179"
---
# <span data-ttu-id="ae9b2-101">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ae9b2-101">Set-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="ae9b2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ae9b2-102">SYNOPSIS</span></span>
<span data-ttu-id="ae9b2-103">Crea o aggiorna ImmutabilityPolicy di un contenitore BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="ae9b2-103">Creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="ae9b2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ae9b2-104">SYNTAX</span></span>

### <span data-ttu-id="ae9b2-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ae9b2-105">AccountName (Default)</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> [-ImmutabilityPeriod <Int32>] [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae9b2-106">ExtendAccountName</span><span class="sxs-lookup"><span data-stu-id="ae9b2-106">ExtendAccountName</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae9b2-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="ae9b2-107">AccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 [-ImmutabilityPeriod <Int32>] [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae9b2-108">ExtendAccountObject</span><span class="sxs-lookup"><span data-stu-id="ae9b2-108">ExtendAccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae9b2-109">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="ae9b2-109">ContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-ImmutabilityPeriod <Int32>]
 [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae9b2-110">ExtendContainerObject</span><span class="sxs-lookup"><span data-stu-id="ae9b2-110">ExtendContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32> -Etag <String>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae9b2-111">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="ae9b2-111">ImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> [-ImmutabilityPeriod <Int32>]
 [-AllowProtectedAppendWrite <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ae9b2-112">ExtendImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="ae9b2-112">ExtendImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae9b2-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ae9b2-113">DESCRIPTION</span></span>
<span data-ttu-id="ae9b2-114">Il cmdlet **set-AzRmStorageContainerImmutabilityPolicy** crea o aggiorna ImmutabilityPolicy di contenitori BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="ae9b2-114">The **Set-AzRmStorageContainerImmutabilityPolicy** cmdlet creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="ae9b2-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ae9b2-115">EXAMPLES</span></span>

### <span data-ttu-id="ae9b2-116">Esempio 1: creare o aggiornare ImmutabilityPolicy di un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore</span><span class="sxs-lookup"><span data-stu-id="ae9b2-116">Example 1: Create or update ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -ImmutabilityPeriod 10
```

<span data-ttu-id="ae9b2-117">Questo comando crea o aggiorna ImmutabilityPolicy di un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="ae9b2-117">This command creates or updates ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="ae9b2-118">Esempio 2: estendere ImmutabilityPolicy di un contenitore di BLOB di archiviazione con l'oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="ae9b2-118">Example 2: Extend ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -ImmutabilityPeriod 20 -Etag $policy.Etag -ExtendPolicy
```

<span data-ttu-id="ae9b2-119">Questo comando estende ImmutabilityPolicy di un contenitore di BLOB di archiviazione con l'oggetto account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ae9b2-119">This command extend ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> <span data-ttu-id="ae9b2-120">Estendi ImmutabilityPolicy può essere eseguito solo dopo che ImmutabilityPolicy è stato bloccato.</span><span class="sxs-lookup"><span data-stu-id="ae9b2-120">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

### <span data-ttu-id="ae9b2-121">Esempio 3: aggiornare ImmutabilityPolicy di un contenitore di BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="ae9b2-121">Example 3: Update ImmutabilityPolicy of a Storage blob container</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 12
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 9 -Etag $policy.Etag
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -AllowProtectedAppendWrite $true
```

<span data-ttu-id="ae9b2-122">Questo comando Aggiorna ImmutabilityPolicy di un contenitore BLOB di archiviazione con l'oggetto contenitore di archiviazione 3 volte: prima di ImmutabilityPeriod 12 giorni senza eTag, quindi per ImmutabilityPeriod 9 giorni con ETag, infine abilitato AllowProtectedAppendWrite.</span><span class="sxs-lookup"><span data-stu-id="ae9b2-122">This command updates ImmutabilityPolicy of a Storage blob container with Storage container object 3 times: First to ImmutabilityPeriod 12 days without etag, then to ImmutabilityPeriod 9 days with etag, finally enabled AllowProtectedAppendWrite.</span></span>

### <span data-ttu-id="ae9b2-123">Esempio 4: estendere ImmutabilityPolicy di un contenitore di BLOB di archiviazione con l'oggetto ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ae9b2-123">Example 4: Extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Set-AzRmStorageContainerImmutabilityPolicy -ImmutabilityPeriod 15 -ExtendPolicy
```

<span data-ttu-id="ae9b2-124">Questo comando estende ImmutabilityPolicy di un contenitore di BLOB di archiviazione con l'oggetto ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="ae9b2-124">This command extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> <span data-ttu-id="ae9b2-125">Estendi ImmutabilityPolicy può essere eseguito solo dopo che ImmutabilityPolicy è stato bloccato.</span><span class="sxs-lookup"><span data-stu-id="ae9b2-125">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

## <span data-ttu-id="ae9b2-126">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ae9b2-126">PARAMETERS</span></span>

### <span data-ttu-id="ae9b2-127">-AllowProtectedAppendWrite</span><span class="sxs-lookup"><span data-stu-id="ae9b2-127">-AllowProtectedAppendWrite</span></span>
<span data-ttu-id="ae9b2-128">Questa proprietà può essere modificata solo per i criteri di conservazione basati sul tempo sbloccati.</span><span class="sxs-lookup"><span data-stu-id="ae9b2-128">This property can only be changed for unlocked time-based retention policies.</span></span> <span data-ttu-id="ae9b2-129">Con questa proprietà abilitata, i nuovi blocchi possono essere scritti in un BLOB di Accodamento mantenendo la protezione e la conformità dell'immutabilità.</span><span class="sxs-lookup"><span data-stu-id="ae9b2-129">With this property enabled, new blocks can be written to an append blob while maintaining immutability protection and compliance.</span></span> <span data-ttu-id="ae9b2-130">È possibile aggiungere solo nuovi blocchi ed eventuali blocchi esistenti non possono essere modificati o eliminati.</span><span class="sxs-lookup"><span data-stu-id="ae9b2-130">Only new blocks can be added and any existing blocks cannot be modified or deleted.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AccountName, AccountObject, ContainerObject, ImmutabilityPolicyObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae9b2-131">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="ae9b2-131">-Container</span></span>
<span data-ttu-id="ae9b2-132">Oggetto contenitore di archiviazione</span><span class="sxs-lookup"><span data-stu-id="ae9b2-132">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject, ExtendContainerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae9b2-133">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="ae9b2-133">-ContainerName</span></span>
<span data-ttu-id="ae9b2-134">Nome contenitore</span><span class="sxs-lookup"><span data-stu-id="ae9b2-134">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, ExtendAccountName, AccountObject, ExtendAccountObject
Aliases: N

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae9b2-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae9b2-135">-DefaultProfile</span></span>
<span data-ttu-id="ae9b2-136">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ae9b2-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae9b2-137">-ETag</span><span class="sxs-lookup"><span data-stu-id="ae9b2-137">-Etag</span></span>
<span data-ttu-id="ae9b2-138">Criteri di immutabilità ETag.</span><span class="sxs-lookup"><span data-stu-id="ae9b2-138">Immutability policy etag.</span></span> <span data-ttu-id="ae9b2-139">Se non viene specificato-ExtendPolicy, ETag è facoltativo; è necessario un altro ETag.</span><span class="sxs-lookup"><span data-stu-id="ae9b2-139">If -ExtendPolicy is not specified, Etag is optional; else Etag is required.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject, ContainerObject
Aliases: IfMatch

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject
Aliases: IfMatch

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae9b2-140">-ExtendPolicy</span><span class="sxs-lookup"><span data-stu-id="ae9b2-140">-ExtendPolicy</span></span>
<span data-ttu-id="ae9b2-141">Indica ExtendPolicy per estendere un ImmutabilityPolicy esistente.</span><span class="sxs-lookup"><span data-stu-id="ae9b2-141">Indicate ExtendPolicy to Extend an existing ImmutabilityPolicy.</span></span>  <span data-ttu-id="ae9b2-142">Dopo il blocco di ImmutabilityPolicy, può essere esteso solo.</span><span class="sxs-lookup"><span data-stu-id="ae9b2-142">After ImmutabilityPolicy is locked, it can only be extend.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject, ExtendImmutabilityPolicyObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae9b2-143">-ImmutabilityPeriod</span><span class="sxs-lookup"><span data-stu-id="ae9b2-143">-ImmutabilityPeriod</span></span>
<span data-ttu-id="ae9b2-144">Periodo di immutabilità dalla creazione in giorni.</span><span class="sxs-lookup"><span data-stu-id="ae9b2-144">Immutability period since creation in days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: AccountName, AccountObject, ContainerObject, ImmutabilityPolicyObject
Aliases: ImmutabilityPeriodSinceCreationInDays

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject, ExtendImmutabilityPolicyObject
Aliases: ImmutabilityPeriodSinceCreationInDays

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae9b2-145">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae9b2-145">-InputObject</span></span>
<span data-ttu-id="ae9b2-146">Nome contenitore</span><span class="sxs-lookup"><span data-stu-id="ae9b2-146">Container Name</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy
Parameter Sets: ImmutabilityPolicyObject, ExtendImmutabilityPolicyObject
Aliases: ImmutabilityPolicy

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae9b2-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae9b2-147">-ResourceGroupName</span></span>
<span data-ttu-id="ae9b2-148">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ae9b2-148">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, ExtendAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae9b2-149">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="ae9b2-149">-StorageAccount</span></span>
<span data-ttu-id="ae9b2-150">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="ae9b2-150">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject, ExtendAccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae9b2-151">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ae9b2-151">-StorageAccountName</span></span>
<span data-ttu-id="ae9b2-152">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ae9b2-152">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, ExtendAccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae9b2-153">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ae9b2-153">-Confirm</span></span>
<span data-ttu-id="ae9b2-154">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae9b2-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae9b2-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae9b2-155">-WhatIf</span></span>
<span data-ttu-id="ae9b2-156">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ae9b2-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae9b2-157">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ae9b2-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae9b2-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae9b2-158">CommonParameters</span></span>
<span data-ttu-id="ae9b2-159">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae9b2-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae9b2-160">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae9b2-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae9b2-161">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ae9b2-161">INPUTS</span></span>

### <span data-ttu-id="ae9b2-162">System. String</span><span class="sxs-lookup"><span data-stu-id="ae9b2-162">System.String</span></span>

### <span data-ttu-id="ae9b2-163">Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ae9b2-163">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="ae9b2-164">Microsoft. Azure. Commands. Management. storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="ae9b2-164">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="ae9b2-165">Microsoft. Azure. Commands. Management. storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ae9b2-165">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="ae9b2-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ae9b2-166">OUTPUTS</span></span>

### <span data-ttu-id="ae9b2-167">Microsoft. Azure. Commands. Management. storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ae9b2-167">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="ae9b2-168">Note</span><span class="sxs-lookup"><span data-stu-id="ae9b2-168">NOTES</span></span>

## <span data-ttu-id="ae9b2-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ae9b2-169">RELATED LINKS</span></span>
