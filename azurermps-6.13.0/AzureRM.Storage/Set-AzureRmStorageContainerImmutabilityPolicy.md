---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/set-azurermstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Set-AzureRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Set-AzureRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 7717aaa76efba736015a1cf762c95af440b28218
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517303"
---
# <span data-ttu-id="15fbd-101">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="15fbd-101">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="15fbd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="15fbd-102">SYNOPSIS</span></span>
<span data-ttu-id="15fbd-103">Crea o aggiorna ImmutabilityPolicy di un contenitore BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="15fbd-103">Creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15fbd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="15fbd-104">SYNTAX</span></span>

### <span data-ttu-id="15fbd-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="15fbd-105">AccountName (Default)</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-ContainerName] <String> -ImmutabilityPeriod <Int32> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15fbd-106">ExtendAccountName</span><span class="sxs-lookup"><span data-stu-id="15fbd-106">ExtendAccountName</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-ContainerName] <String> -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15fbd-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="15fbd-107">AccountObject</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy [-ContainerName] <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="15fbd-108">ExtendAccountObject</span><span class="sxs-lookup"><span data-stu-id="15fbd-108">ExtendAccountObject</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy [-ContainerName] <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15fbd-109">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="15fbd-109">ContainerObject</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15fbd-110">ExtendContainerObject</span><span class="sxs-lookup"><span data-stu-id="15fbd-110">ExtendContainerObject</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32>
 -Etag <String> [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="15fbd-111">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="15fbd-111">ImmutabilityPolicyObject</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy -InputObject <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15fbd-112">ExtendImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="15fbd-112">ExtendImmutabilityPolicyObject</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy -InputObject <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15fbd-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="15fbd-113">DESCRIPTION</span></span>
<span data-ttu-id="15fbd-114">Il cmdlet **set-AzureRmStorageContainerImmutabilityPolicy** crea o aggiorna ImmutabilityPolicy di contenitori BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="15fbd-114">The **Set-AzureRmStorageContainerImmutabilityPolicy** cmdlet creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="15fbd-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="15fbd-115">EXAMPLES</span></span>

### <span data-ttu-id="15fbd-116">Esempio 1: creare o aggiornare ImmutabilityPolicy di un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore</span><span class="sxs-lookup"><span data-stu-id="15fbd-116">Example 1: Create or update ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Set-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -ImmutabilityPeriod 10 
```

<span data-ttu-id="15fbd-117">Questo comando crea o aggiorna ImmutabilityPolicy di un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="15fbd-117">This command creates or updates ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="15fbd-118">Esempio 2: estendere ImmutabilityPolicy di un contenitore di BLOB di archiviazione con l'oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="15fbd-118">Example 2: Extend ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Set-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -ImmutabilityPeriod 20 -Etag $policy.Etag -ExtendPolicy
```

<span data-ttu-id="15fbd-119">Questo comando estende ImmutabilityPolicy di un contenitore di BLOB di archiviazione con l'oggetto account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="15fbd-119">This command extend ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> <span data-ttu-id="15fbd-120">Estendi ImmutabilityPolicy può essere eseguito solo dopo che ImmutabilityPolicy è stato bloccato.</span><span class="sxs-lookup"><span data-stu-id="15fbd-120">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

### <span data-ttu-id="15fbd-121">Esempio 3: aggiornare ImmutabilityPolicyof un contenitore BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="15fbd-121">Example 3: Update ImmutabilityPolicyof a Storage blob container</span></span> 
```
PS C:\>$containerObject = Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Set-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 12
PS C:\>$policy = Set-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 9 -Etag $policy.Etag
```

<span data-ttu-id="15fbd-122">Questo comando Aggiorna ImmutabilityPolicy di un contenitore BLOB di archiviazione con l'oggetto contenitore di archiviazione 2 volte, prima di ImmutabilityPeriod 12 giorni senza eTag, quindi ImmutabilityPeriod 9 giorni con ETag.</span><span class="sxs-lookup"><span data-stu-id="15fbd-122">This command updates ImmutabilityPolicy of a Storage blob container with Storage container object 2 times, first to ImmutabilityPeriod 12 days without etag, then to ImmutabilityPeriod 9 days with etag.</span></span>

### <span data-ttu-id="15fbd-123">Esempio 4: estendere ImmutabilityPolicy di un contenitore di BLOB di archiviazione con l'oggetto ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="15fbd-123">Example 4: Extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Set-AzureRmStorageContainerImmutabilityPolicy -ImmutabilityPeriod 15 -ExtendPolicy
```

<span data-ttu-id="15fbd-124">Questo comando estende ImmutabilityPolicy di un contenitore di BLOB di archiviazione con l'oggetto ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="15fbd-124">This command extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> <span data-ttu-id="15fbd-125">Estendi ImmutabilityPolicy può essere eseguito solo dopo che ImmutabilityPolicy è stato bloccato.</span><span class="sxs-lookup"><span data-stu-id="15fbd-125">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

## <span data-ttu-id="15fbd-126">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="15fbd-126">PARAMETERS</span></span>

### <span data-ttu-id="15fbd-127">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="15fbd-127">-Container</span></span>
<span data-ttu-id="15fbd-128">Oggetto contenitore di archiviazione</span><span class="sxs-lookup"><span data-stu-id="15fbd-128">Storage container object</span></span>

```yaml
Type: PSContainer
Parameter Sets: ContainerObject, ExtendContainerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15fbd-129">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="15fbd-129">-ContainerName</span></span>
<span data-ttu-id="15fbd-130">Nome contenitore</span><span class="sxs-lookup"><span data-stu-id="15fbd-130">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AccountName, ExtendAccountName, AccountObject, ExtendAccountObject
Aliases: N

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15fbd-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15fbd-131">-DefaultProfile</span></span>
<span data-ttu-id="15fbd-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="15fbd-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15fbd-133">-ETag</span><span class="sxs-lookup"><span data-stu-id="15fbd-133">-Etag</span></span>
<span data-ttu-id="15fbd-134">Criteri di immutabilità ETag.</span><span class="sxs-lookup"><span data-stu-id="15fbd-134">Immutability policy etag.</span></span> <span data-ttu-id="15fbd-135">Se non viene specificato-ExtendPolicy, ETag è facoltativo; è necessario un altro ETag.</span><span class="sxs-lookup"><span data-stu-id="15fbd-135">If -ExtendPolicy is not specified, Etag is optional; else Etag is required.</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject, ContainerObject
Aliases: IfMatch

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject
Aliases: IfMatch

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15fbd-136">-ExtendPolicy</span><span class="sxs-lookup"><span data-stu-id="15fbd-136">-ExtendPolicy</span></span>
<span data-ttu-id="15fbd-137">Indica ExtendPolicy per estendere un ImmutabilityPolicy esistente.</span><span class="sxs-lookup"><span data-stu-id="15fbd-137">Indicate ExtendPolicy to Extend an existing ImmutabilityPolicy.</span></span>  <span data-ttu-id="15fbd-138">Dopo il blocco di ImmutabilityPolicy, può essere esteso solo.</span><span class="sxs-lookup"><span data-stu-id="15fbd-138">After ImmutabilityPolicy is locked, it can only be extend.</span></span> 

```yaml
Type: SwitchParameter
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject, ExtendImmutabilityPolicyObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15fbd-139">-ImmutabilityPeriod</span><span class="sxs-lookup"><span data-stu-id="15fbd-139">-ImmutabilityPeriod</span></span>
<span data-ttu-id="15fbd-140">Periodo di immutabilità dalla creazione in giorni.</span><span class="sxs-lookup"><span data-stu-id="15fbd-140">Immutability period since creation in days.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: ImmutabilityPeriodSinceCreationInDays

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15fbd-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="15fbd-141">-InputObject</span></span>
<span data-ttu-id="15fbd-142">Nome contenitore</span><span class="sxs-lookup"><span data-stu-id="15fbd-142">Container Name</span></span>

```yaml
Type: PSImmutabilityPolicy
Parameter Sets: ImmutabilityPolicyObject, ExtendImmutabilityPolicyObject
Aliases: ImmutabilityPolicy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15fbd-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15fbd-143">-ResourceGroupName</span></span>
<span data-ttu-id="15fbd-144">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="15fbd-144">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName, ExtendAccountName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15fbd-145">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="15fbd-145">-StorageAccount</span></span>
<span data-ttu-id="15fbd-146">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="15fbd-146">Storage account object</span></span>

```yaml
Type: PSStorageAccount
Parameter Sets: AccountObject, ExtendAccountObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15fbd-147">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="15fbd-147">-StorageAccountName</span></span>
<span data-ttu-id="15fbd-148">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="15fbd-148">Storage Account Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName, ExtendAccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15fbd-149">-Confermare</span><span class="sxs-lookup"><span data-stu-id="15fbd-149">-Confirm</span></span>
<span data-ttu-id="15fbd-150">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15fbd-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15fbd-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15fbd-151">-WhatIf</span></span>
<span data-ttu-id="15fbd-152">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="15fbd-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15fbd-153">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="15fbd-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15fbd-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15fbd-154">CommonParameters</span></span>
<span data-ttu-id="15fbd-155">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15fbd-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15fbd-156">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15fbd-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15fbd-157">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="15fbd-157">INPUTS</span></span>

### <span data-ttu-id="15fbd-158">System. String</span><span class="sxs-lookup"><span data-stu-id="15fbd-158">System.String</span></span>
<span data-ttu-id="15fbd-159">Microsoft. Azure. Commands. Management. storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="15fbd-159">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="15fbd-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="15fbd-160">OUTPUTS</span></span>

### <span data-ttu-id="15fbd-161">Microsoft. Azure. Commands. Management. storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="15fbd-161">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="15fbd-162">Note</span><span class="sxs-lookup"><span data-stu-id="15fbd-162">NOTES</span></span>

## <span data-ttu-id="15fbd-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="15fbd-163">RELATED LINKS</span></span>

