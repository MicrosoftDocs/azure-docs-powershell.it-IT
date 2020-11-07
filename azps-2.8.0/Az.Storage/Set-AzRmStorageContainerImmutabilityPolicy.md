---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: c216765657cc87c958cc20dd0f2014f0e1c16970
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93858261"
---
# <span data-ttu-id="fed31-101">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="fed31-101">Set-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="fed31-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fed31-102">SYNOPSIS</span></span>
<span data-ttu-id="fed31-103">Crea o aggiorna ImmutabilityPolicy di un contenitore BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="fed31-103">Creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="fed31-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fed31-104">SYNTAX</span></span>

### <span data-ttu-id="fed31-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fed31-105">AccountName (Default)</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -ImmutabilityPeriod <Int32> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fed31-106">ExtendAccountName</span><span class="sxs-lookup"><span data-stu-id="fed31-106">ExtendAccountName</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fed31-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="fed31-107">AccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fed31-108">ExtendAccountObject</span><span class="sxs-lookup"><span data-stu-id="fed31-108">ExtendAccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fed31-109">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="fed31-109">ContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fed31-110">ExtendContainerObject</span><span class="sxs-lookup"><span data-stu-id="fed31-110">ExtendContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32> -Etag <String>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fed31-111">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="fed31-111">ImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fed31-112">ExtendImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="fed31-112">ExtendImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fed31-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fed31-113">DESCRIPTION</span></span>
<span data-ttu-id="fed31-114">Il cmdlet **set-AzRmStorageContainerImmutabilityPolicy** crea o aggiorna ImmutabilityPolicy di contenitori BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="fed31-114">The **Set-AzRmStorageContainerImmutabilityPolicy** cmdlet creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="fed31-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fed31-115">EXAMPLES</span></span>

### <span data-ttu-id="fed31-116">Esempio 1: creare o aggiornare ImmutabilityPolicy di un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore</span><span class="sxs-lookup"><span data-stu-id="fed31-116">Example 1: Create or update ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -ImmutabilityPeriod 10
```

<span data-ttu-id="fed31-117">Questo comando crea o aggiorna ImmutabilityPolicy di un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="fed31-117">This command creates or updates ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="fed31-118">Esempio 2: estendere ImmutabilityPolicy di un contenitore di BLOB di archiviazione con l'oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="fed31-118">Example 2: Extend ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -ImmutabilityPeriod 20 -Etag $policy.Etag -ExtendPolicy
```

<span data-ttu-id="fed31-119">Questo comando estende ImmutabilityPolicy di un contenitore di BLOB di archiviazione con l'oggetto account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="fed31-119">This command extend ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> <span data-ttu-id="fed31-120">Estendi ImmutabilityPolicy può essere eseguito solo dopo che ImmutabilityPolicy è stato bloccato.</span><span class="sxs-lookup"><span data-stu-id="fed31-120">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

### <span data-ttu-id="fed31-121">Esempio 3: aggiornare ImmutabilityPolicyof un contenitore BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="fed31-121">Example 3: Update ImmutabilityPolicyof a Storage blob container</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 12
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 9 -Etag $policy.Etag
```

<span data-ttu-id="fed31-122">Questo comando Aggiorna ImmutabilityPolicy di un contenitore BLOB di archiviazione con l'oggetto contenitore di archiviazione 2 volte, prima di ImmutabilityPeriod 12 giorni senza eTag, quindi ImmutabilityPeriod 9 giorni con ETag.</span><span class="sxs-lookup"><span data-stu-id="fed31-122">This command updates ImmutabilityPolicy of a Storage blob container with Storage container object 2 times, first to ImmutabilityPeriod 12 days without etag, then to ImmutabilityPeriod 9 days with etag.</span></span>

### <span data-ttu-id="fed31-123">Esempio 4: estendere ImmutabilityPolicy di un contenitore di BLOB di archiviazione con l'oggetto ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="fed31-123">Example 4: Extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Set-AzRmStorageContainerImmutabilityPolicy -ImmutabilityPeriod 15 -ExtendPolicy
```

<span data-ttu-id="fed31-124">Questo comando estende ImmutabilityPolicy di un contenitore di BLOB di archiviazione con l'oggetto ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="fed31-124">This command extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> <span data-ttu-id="fed31-125">Estendi ImmutabilityPolicy può essere eseguito solo dopo che ImmutabilityPolicy è stato bloccato.</span><span class="sxs-lookup"><span data-stu-id="fed31-125">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

## <span data-ttu-id="fed31-126">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fed31-126">PARAMETERS</span></span>

### <span data-ttu-id="fed31-127">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="fed31-127">-Container</span></span>
<span data-ttu-id="fed31-128">Oggetto contenitore di archiviazione</span><span class="sxs-lookup"><span data-stu-id="fed31-128">Storage container object</span></span>

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

### <span data-ttu-id="fed31-129">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="fed31-129">-ContainerName</span></span>
<span data-ttu-id="fed31-130">Nome contenitore</span><span class="sxs-lookup"><span data-stu-id="fed31-130">Container Name</span></span>

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

### <span data-ttu-id="fed31-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fed31-131">-DefaultProfile</span></span>
<span data-ttu-id="fed31-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fed31-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fed31-133">-ETag</span><span class="sxs-lookup"><span data-stu-id="fed31-133">-Etag</span></span>
<span data-ttu-id="fed31-134">Criteri di immutabilità ETag.</span><span class="sxs-lookup"><span data-stu-id="fed31-134">Immutability policy etag.</span></span> <span data-ttu-id="fed31-135">Se non viene specificato-ExtendPolicy, ETag è facoltativo; è necessario un altro ETag.</span><span class="sxs-lookup"><span data-stu-id="fed31-135">If -ExtendPolicy is not specified, Etag is optional; else Etag is required.</span></span>

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

### <span data-ttu-id="fed31-136">-ExtendPolicy</span><span class="sxs-lookup"><span data-stu-id="fed31-136">-ExtendPolicy</span></span>
<span data-ttu-id="fed31-137">Indica ExtendPolicy per estendere un ImmutabilityPolicy esistente.</span><span class="sxs-lookup"><span data-stu-id="fed31-137">Indicate ExtendPolicy to Extend an existing ImmutabilityPolicy.</span></span>  <span data-ttu-id="fed31-138">Dopo il blocco di ImmutabilityPolicy, può essere esteso solo.</span><span class="sxs-lookup"><span data-stu-id="fed31-138">After ImmutabilityPolicy is locked, it can only be extend.</span></span> 

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

### <span data-ttu-id="fed31-139">-ImmutabilityPeriod</span><span class="sxs-lookup"><span data-stu-id="fed31-139">-ImmutabilityPeriod</span></span>
<span data-ttu-id="fed31-140">Periodo di immutabilità dalla creazione in giorni.</span><span class="sxs-lookup"><span data-stu-id="fed31-140">Immutability period since creation in days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: ImmutabilityPeriodSinceCreationInDays

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fed31-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fed31-141">-InputObject</span></span>
<span data-ttu-id="fed31-142">Nome contenitore</span><span class="sxs-lookup"><span data-stu-id="fed31-142">Container Name</span></span>

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

### <span data-ttu-id="fed31-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fed31-143">-ResourceGroupName</span></span>
<span data-ttu-id="fed31-144">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fed31-144">Resource Group Name.</span></span>

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

### <span data-ttu-id="fed31-145">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="fed31-145">-StorageAccount</span></span>
<span data-ttu-id="fed31-146">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="fed31-146">Storage account object</span></span>

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

### <span data-ttu-id="fed31-147">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="fed31-147">-StorageAccountName</span></span>
<span data-ttu-id="fed31-148">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="fed31-148">Storage Account Name.</span></span>

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

### <span data-ttu-id="fed31-149">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fed31-149">-Confirm</span></span>
<span data-ttu-id="fed31-150">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fed31-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fed31-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fed31-151">-WhatIf</span></span>
<span data-ttu-id="fed31-152">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fed31-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fed31-153">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fed31-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fed31-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fed31-154">CommonParameters</span></span>
<span data-ttu-id="fed31-155">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fed31-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fed31-156">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fed31-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fed31-157">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fed31-157">INPUTS</span></span>

### <span data-ttu-id="fed31-158">System. String</span><span class="sxs-lookup"><span data-stu-id="fed31-158">System.String</span></span>

### <span data-ttu-id="fed31-159">Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fed31-159">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="fed31-160">Microsoft. Azure. Commands. Management. storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="fed31-160">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="fed31-161">Microsoft. Azure. Commands. Management. storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="fed31-161">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="fed31-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fed31-162">OUTPUTS</span></span>

### <span data-ttu-id="fed31-163">Microsoft. Azure. Commands. Management. storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="fed31-163">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="fed31-164">Note</span><span class="sxs-lookup"><span data-stu-id="fed31-164">NOTES</span></span>

## <span data-ttu-id="fed31-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fed31-165">RELATED LINKS</span></span>
