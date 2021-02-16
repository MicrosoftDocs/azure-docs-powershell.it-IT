---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratereplicationprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationProtectionContainerMapping.md
ms.openlocfilehash: 996f33a967aaedc66bc0ed9b41cba09401f1dde4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194110"
---
# <span data-ttu-id="209cc-101">New-AzMigrateReplicationProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="209cc-101">New-AzMigrateReplicationProtectionContainerMapping</span></span>

## <span data-ttu-id="209cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="209cc-102">SYNOPSIS</span></span>
<span data-ttu-id="209cc-103">Operazione per creare un mapping del contenitore di protezione.</span><span class="sxs-lookup"><span data-stu-id="209cc-103">The operation to create a protection container mapping.</span></span>

## <span data-ttu-id="209cc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="209cc-104">SYNTAX</span></span>

```
New-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -MappingName <String>
 -ProtectionContainerName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-PolicyId <String>]
 [-ProviderSpecificInput <IReplicationProviderSpecificContainerMappingInput>]
 [-TargetProtectionContainerId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="209cc-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="209cc-105">DESCRIPTION</span></span>
<span data-ttu-id="209cc-106">Operazione per creare un mapping del contenitore di protezione.</span><span class="sxs-lookup"><span data-stu-id="209cc-106">The operation to create a protection container mapping.</span></span>

## <span data-ttu-id="209cc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="209cc-107">EXAMPLES</span></span>

### <span data-ttu-id="209cc-108">Esempio 1: Creare un mapping</span><span class="sxs-lookup"><span data-stu-id="209cc-108">Example 1: Create a mapping</span></span>
```powershell
PS C:\> $providerSpecificInput = [Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.VMwareCbtContainerMappingInput]::new()
PS C:\> $providerSpecificInput.InstanceType = "VMwareCbt"
PS C:\> $providerSpecificInput.KeyVaultId = "/subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.KeyVault/vaults/migratekv846827101"
PS C:\> $providerSpecificInput.KeyVaultUri = "https://migratekv846827101.vault.azure.net"
PS C:\> $providerSpecificInput.ServiceBusConnectionStringSecretName = "ServiceBusConnectionString"
PS C:\> $providerSpecificInput.StorageAccountId = "/subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Storage/storageAccounts/migrategwsa846827101"
PS C:\> $providerSpecificInput.StorageAccountSasSecretName = "migrategwsa846827101-gwySas"
PS C:\> $providerSpecificInput.TargetLocation = "centraluseuap"

PS C:\> New-AzMigrateReplicationProtectionContainerMapping -FabricName "AzMigratePWSHTc8d1replicationfabric" -MappingName "containermapping" -ProtectionContainerName "AzMigratePWSHTc8d1replicationcontainer" -ResourceGroupName "azmigratepwshtestasr13072020" -ResourceName "AzMigrateTestProjectPWSH02aarsvault"  -PolicyId "/subscriptionsxxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationPolicies/migrateAzMigratePWSHTc8d1sitepolicy"  -ProviderSpecificInput $providerSpecificInput -TargetProtectionContainerId  "Microsoft Azure"

Location Name             Type
-------- ----             ----
         containermapping Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectionContainerMappings
```

<span data-ttu-id="209cc-109">Creare un mapping</span><span class="sxs-lookup"><span data-stu-id="209cc-109">Create a mapping</span></span>

## <span data-ttu-id="209cc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="209cc-110">PARAMETERS</span></span>

### <span data-ttu-id="209cc-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="209cc-111">-AsJob</span></span>
<span data-ttu-id="209cc-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="209cc-112">Run the command as a job</span></span>

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

### <span data-ttu-id="209cc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="209cc-113">-DefaultProfile</span></span>
<span data-ttu-id="209cc-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="209cc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="209cc-115">-FabricName</span><span class="sxs-lookup"><span data-stu-id="209cc-115">-FabricName</span></span>
<span data-ttu-id="209cc-116">Nome del tessuto.</span><span class="sxs-lookup"><span data-stu-id="209cc-116">Fabric name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="209cc-117">-MappingName</span><span class="sxs-lookup"><span data-stu-id="209cc-117">-MappingName</span></span>
<span data-ttu-id="209cc-118">Nome mapping contenitore di protezione.</span><span class="sxs-lookup"><span data-stu-id="209cc-118">Protection container mapping name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="209cc-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="209cc-119">-NoWait</span></span>
<span data-ttu-id="209cc-120">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="209cc-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="209cc-121">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="209cc-121">-PolicyId</span></span>
<span data-ttu-id="209cc-122">Criterio applicabile.</span><span class="sxs-lookup"><span data-stu-id="209cc-122">Applicable policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="209cc-123">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="209cc-123">-ProtectionContainerName</span></span>
<span data-ttu-id="209cc-124">Nome del contenitore di protezione.</span><span class="sxs-lookup"><span data-stu-id="209cc-124">Protection container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="209cc-125">-ProviderSpecificInput</span><span class="sxs-lookup"><span data-stu-id="209cc-125">-ProviderSpecificInput</span></span>
<span data-ttu-id="209cc-126">Input specifico del provider per l'associazione.</span><span class="sxs-lookup"><span data-stu-id="209cc-126">Provider specific input for pairing.</span></span>
<span data-ttu-id="209cc-127">Per creare, vedere la sezione NOTES per le proprietà PROVIDERSPECIFICINPUT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="209cc-127">To construct, see NOTES section for PROVIDERSPECIFICINPUT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IReplicationProviderSpecificContainerMappingInput
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="209cc-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="209cc-128">-ResourceGroupName</span></span>
<span data-ttu-id="209cc-129">Nome del gruppo di risorse in cui è presente la vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="209cc-129">The name of the resource group where the recovery services vault is present.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="209cc-130">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="209cc-130">-ResourceName</span></span>
<span data-ttu-id="209cc-131">Nome del vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="209cc-131">The name of the recovery services vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="209cc-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="209cc-132">-SubscriptionId</span></span>
<span data-ttu-id="209cc-133">ID sottoscrizione di Azure in cui è stato creato il progetto di migrazione.</span><span class="sxs-lookup"><span data-stu-id="209cc-133">Azure Subscription Id in which migrate project was created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="209cc-134">-TargetProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="209cc-134">-TargetProtectionContainerId</span></span>
<span data-ttu-id="209cc-135">Nome del contenitore di protezione univoco di destinazione.</span><span class="sxs-lookup"><span data-stu-id="209cc-135">The target unique protection container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="209cc-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="209cc-136">-Confirm</span></span>
<span data-ttu-id="209cc-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="209cc-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="209cc-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="209cc-138">-WhatIf</span></span>
<span data-ttu-id="209cc-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="209cc-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="209cc-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="209cc-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="209cc-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="209cc-141">CommonParameters</span></span>
<span data-ttu-id="209cc-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="209cc-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="209cc-143">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="209cc-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="209cc-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="209cc-144">INPUTS</span></span>

## <span data-ttu-id="209cc-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="209cc-145">OUTPUTS</span></span>

### <span data-ttu-id="209cc-146">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="209cc-146">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span></span>

## <span data-ttu-id="209cc-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="209cc-147">NOTES</span></span>

<span data-ttu-id="209cc-148">ALIAS</span><span class="sxs-lookup"><span data-stu-id="209cc-148">ALIASES</span></span>

<span data-ttu-id="209cc-149">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="209cc-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="209cc-150">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="209cc-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="209cc-151">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="209cc-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="209cc-152">PROVIDERSPECIFICINPUT: <IReplicationProviderSpecificContainerMappingInput> input specifico del provider per l'associazione.</span><span class="sxs-lookup"><span data-stu-id="209cc-152">PROVIDERSPECIFICINPUT <IReplicationProviderSpecificContainerMappingInput>: Provider specific input for pairing.</span></span>
  - <span data-ttu-id="209cc-153">`[InstanceType <String>]`: il tipo di classe.</span><span class="sxs-lookup"><span data-stu-id="209cc-153">`[InstanceType <String>]`: The class type.</span></span>

## <span data-ttu-id="209cc-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="209cc-154">RELATED LINKS</span></span>

