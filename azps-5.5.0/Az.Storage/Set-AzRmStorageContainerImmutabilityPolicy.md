---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 9631855803b4ad16312c907c1d1c747b3aee6fdf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197502"
---
# <span data-ttu-id="b75c5-101">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="b75c5-101">Set-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="b75c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b75c5-102">SYNOPSIS</span></span>
<span data-ttu-id="b75c5-103">Crea o aggiorna ImmutabilityPolicy di contenitori BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="b75c5-103">Creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="b75c5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b75c5-104">SYNTAX</span></span>

### <span data-ttu-id="b75c5-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b75c5-105">AccountName (Default)</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> [-ImmutabilityPeriod <Int32>] [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b75c5-106">ExtendAccountName</span><span class="sxs-lookup"><span data-stu-id="b75c5-106">ExtendAccountName</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b75c5-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="b75c5-107">AccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 [-ImmutabilityPeriod <Int32>] [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b75c5-108">ExtendAccountObject</span><span class="sxs-lookup"><span data-stu-id="b75c5-108">ExtendAccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b75c5-109">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="b75c5-109">ContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-ImmutabilityPeriod <Int32>]
 [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b75c5-110">ExtendContainerObject</span><span class="sxs-lookup"><span data-stu-id="b75c5-110">ExtendContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32> -Etag <String>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b75c5-111">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="b75c5-111">ImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> [-ImmutabilityPeriod <Int32>]
 [-AllowProtectedAppendWrite <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b75c5-112">ExtendImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="b75c5-112">ExtendImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b75c5-113">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b75c5-113">DESCRIPTION</span></span>
<span data-ttu-id="b75c5-114">Il cmdlet **Set-AzRmStorageContainerImmutabilityPolicy** crea o aggiorna ImmutabilityPolicy di contenitori BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="b75c5-114">The **Set-AzRmStorageContainerImmutabilityPolicy** cmdlet creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="b75c5-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b75c5-115">EXAMPLES</span></span>

### <span data-ttu-id="b75c5-116">Esempio 1: Creare o aggiornare ImmutabilityPolicy di un contenitore BLOB Archiviazione con il nome dell'account di archiviazione e il nome del contenitore</span><span class="sxs-lookup"><span data-stu-id="b75c5-116">Example 1: Create or update ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -ImmutabilityPeriod 10
```

<span data-ttu-id="b75c5-117">Questo comando crea o aggiorna ImmutabilityPolicy di un contenitore BLOB Archiviazione con il nome dell'account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="b75c5-117">This command creates or updates ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="b75c5-118">Esempio 2: Estendere ImmutabilityPolicy di un contenitore BLOB Storage, con oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="b75c5-118">Example 2: Extend ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -ImmutabilityPeriod 20 -Etag $policy.Etag -ExtendPolicy
```

<span data-ttu-id="b75c5-119">Questo comando estende ImmutabilityPolicy di un contenitore BLOB Storage, con oggetto account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="b75c5-119">This command extend ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> <span data-ttu-id="b75c5-120">Extend ImmutabilityPolicy può essere eseguito solo dopo il blocco di ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="b75c5-120">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

### <span data-ttu-id="b75c5-121">Esempio 3: Aggiornare ImmutabilityPolicy di un contenitore BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="b75c5-121">Example 3: Update ImmutabilityPolicy of a Storage blob container</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 12
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 9 -Etag $policy.Etag
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -AllowProtectedAppendWrite $true
```

<span data-ttu-id="b75c5-122">Questo comando aggiorna ImmutabilityPolicy di un contenitore BLOB Storage con oggetto contenitore storage 3 volte: First to ImmutabilityPeriod 12 days without etag, then to ImmutabilityPeriod 9 days with etag, finally enabled AllowProtectedAppendWrite.</span><span class="sxs-lookup"><span data-stu-id="b75c5-122">This command updates ImmutabilityPolicy of a Storage blob container with Storage container object 3 times: First to ImmutabilityPeriod 12 days without etag, then to ImmutabilityPeriod 9 days with etag, finally enabled AllowProtectedAppendWrite.</span></span>

### <span data-ttu-id="b75c5-123">Esempio 4: Estendere ImmutabilityPolicy di un contenitore BLOB Storage, con oggetto ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="b75c5-123">Example 4: Extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Set-AzRmStorageContainerImmutabilityPolicy -ImmutabilityPeriod 15 -ExtendPolicy
```

<span data-ttu-id="b75c5-124">Questo comando estende ImmutabilityPolicy di un contenitore BLOB Storage, con oggetto ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="b75c5-124">This command extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> <span data-ttu-id="b75c5-125">Extend ImmutabilityPolicy può essere eseguito solo dopo il blocco di ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="b75c5-125">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

## <span data-ttu-id="b75c5-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b75c5-126">PARAMETERS</span></span>

### <span data-ttu-id="b75c5-127">-AllowProtectedAppendWrite</span><span class="sxs-lookup"><span data-stu-id="b75c5-127">-AllowProtectedAppendWrite</span></span>
<span data-ttu-id="b75c5-128">Questa proprietà può essere modificata solo per i criteri di conservazione con scadenza sbloccata.</span><span class="sxs-lookup"><span data-stu-id="b75c5-128">This property can only be changed for unlocked time-based retention policies.</span></span> <span data-ttu-id="b75c5-129">Con questa proprietà abilitata, è possibile scrivere nuovi blocchi in un BLOB di accodamento mantenendo al contempo la protezione dell'inattibilità e la conformità.</span><span class="sxs-lookup"><span data-stu-id="b75c5-129">With this property enabled, new blocks can be written to an append blob while maintaining immutability protection and compliance.</span></span> <span data-ttu-id="b75c5-130">È possibile aggiungere solo nuovi blocchi e gli eventuali blocchi esistenti non possono essere modificati o eliminati.</span><span class="sxs-lookup"><span data-stu-id="b75c5-130">Only new blocks can be added and any existing blocks cannot be modified or deleted.</span></span>

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

### <span data-ttu-id="b75c5-131">-Container</span><span class="sxs-lookup"><span data-stu-id="b75c5-131">-Container</span></span>
<span data-ttu-id="b75c5-132">Oggetto contenitore di archiviazione</span><span class="sxs-lookup"><span data-stu-id="b75c5-132">Storage container object</span></span>

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

### <span data-ttu-id="b75c5-133">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="b75c5-133">-ContainerName</span></span>
<span data-ttu-id="b75c5-134">Nome contenitore</span><span class="sxs-lookup"><span data-stu-id="b75c5-134">Container Name</span></span>

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

### <span data-ttu-id="b75c5-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b75c5-135">-DefaultProfile</span></span>
<span data-ttu-id="b75c5-136">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b75c5-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b75c5-137">-Etag</span><span class="sxs-lookup"><span data-stu-id="b75c5-137">-Etag</span></span>
<span data-ttu-id="b75c5-138">Etag dei criteri di non modificabilità.</span><span class="sxs-lookup"><span data-stu-id="b75c5-138">Immutability policy etag.</span></span> <span data-ttu-id="b75c5-139">Se -ExtendPolicy non è specificato, l'Etag è facoltativo; else Etag is required.</span><span class="sxs-lookup"><span data-stu-id="b75c5-139">If -ExtendPolicy is not specified, Etag is optional; else Etag is required.</span></span>

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

### <span data-ttu-id="b75c5-140">-ExtendPolicy</span><span class="sxs-lookup"><span data-stu-id="b75c5-140">-ExtendPolicy</span></span>
<span data-ttu-id="b75c5-141">Indicare ExtendPolicy per estendere un valore ImmutabilityPolicy esistente.</span><span class="sxs-lookup"><span data-stu-id="b75c5-141">Indicate ExtendPolicy to Extend an existing ImmutabilityPolicy.</span></span>  <span data-ttu-id="b75c5-142">Quando ImmutabilityPolicy è bloccato, può essere esteso solo.</span><span class="sxs-lookup"><span data-stu-id="b75c5-142">After ImmutabilityPolicy is locked, it can only be extend.</span></span> 

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

### <span data-ttu-id="b75c5-143">-ImmutabilityPeriod</span><span class="sxs-lookup"><span data-stu-id="b75c5-143">-ImmutabilityPeriod</span></span>
<span data-ttu-id="b75c5-144">Periodo di messaggistica istantanea dalla creazione in giorni.</span><span class="sxs-lookup"><span data-stu-id="b75c5-144">Immutability period since creation in days.</span></span>

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

### <span data-ttu-id="b75c5-145">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b75c5-145">-InputObject</span></span>
<span data-ttu-id="b75c5-146">Nome contenitore</span><span class="sxs-lookup"><span data-stu-id="b75c5-146">Container Name</span></span>

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

### <span data-ttu-id="b75c5-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b75c5-147">-ResourceGroupName</span></span>
<span data-ttu-id="b75c5-148">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b75c5-148">Resource Group Name.</span></span>

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

### <span data-ttu-id="b75c5-149">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="b75c5-149">-StorageAccount</span></span>
<span data-ttu-id="b75c5-150">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="b75c5-150">Storage account object</span></span>

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

### <span data-ttu-id="b75c5-151">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b75c5-151">-StorageAccountName</span></span>
<span data-ttu-id="b75c5-152">Nome account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="b75c5-152">Storage Account Name.</span></span>

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

### <span data-ttu-id="b75c5-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b75c5-153">-Confirm</span></span>
<span data-ttu-id="b75c5-154">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b75c5-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b75c5-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b75c5-155">-WhatIf</span></span>
<span data-ttu-id="b75c5-156">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b75c5-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b75c5-157">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b75c5-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b75c5-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b75c5-158">CommonParameters</span></span>
<span data-ttu-id="b75c5-159">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b75c5-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b75c5-160">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b75c5-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b75c5-161">INPUT</span><span class="sxs-lookup"><span data-stu-id="b75c5-161">INPUTS</span></span>

### <span data-ttu-id="b75c5-162">System.String</span><span class="sxs-lookup"><span data-stu-id="b75c5-162">System.String</span></span>

### <span data-ttu-id="b75c5-163">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b75c5-163">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="b75c5-164">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="b75c5-164">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="b75c5-165">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="b75c5-165">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="b75c5-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b75c5-166">OUTPUTS</span></span>

### <span data-ttu-id="b75c5-167">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="b75c5-167">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="b75c5-168">NOTE</span><span class="sxs-lookup"><span data-stu-id="b75c5-168">NOTES</span></span>

## <span data-ttu-id="b75c5-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b75c5-169">RELATED LINKS</span></span>
