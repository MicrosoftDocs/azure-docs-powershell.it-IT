---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratereplicationprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationProtectionContainerMapping.md
ms.openlocfilehash: b92d483689c94e6dd9f9af69e47f5b17ea1ab795
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202097"
---
# <span data-ttu-id="bc1cb-101">New-AzMigrateReplicationProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="bc1cb-101">New-AzMigrateReplicationProtectionContainerMapping</span></span>

## <span data-ttu-id="bc1cb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bc1cb-102">SYNOPSIS</span></span>
<span data-ttu-id="bc1cb-103">Operazione per creare un mapping contenitore di protezione.</span><span class="sxs-lookup"><span data-stu-id="bc1cb-103">The operation to create a protection container mapping.</span></span>

## <span data-ttu-id="bc1cb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bc1cb-104">SYNTAX</span></span>

```
New-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -MappingName <String>
 -ProtectionContainerName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-PolicyId <String>]
 [-ProviderSpecificInput <IReplicationProviderSpecificContainerMappingInput>]
 [-TargetProtectionContainerId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="bc1cb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bc1cb-105">DESCRIPTION</span></span>
<span data-ttu-id="bc1cb-106">Operazione per creare un mapping contenitore di protezione.</span><span class="sxs-lookup"><span data-stu-id="bc1cb-106">The operation to create a protection container mapping.</span></span>

## <span data-ttu-id="bc1cb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bc1cb-107">EXAMPLES</span></span>

### <span data-ttu-id="bc1cb-108">Esempio 1: creare un mapping</span><span class="sxs-lookup"><span data-stu-id="bc1cb-108">Example 1: Create a mapping</span></span>
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

<span data-ttu-id="bc1cb-109">Creare un mapping</span><span class="sxs-lookup"><span data-stu-id="bc1cb-109">Create a mapping</span></span>

## <span data-ttu-id="bc1cb-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bc1cb-110">PARAMETERS</span></span>

### <span data-ttu-id="bc1cb-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bc1cb-111">-AsJob</span></span>
<span data-ttu-id="bc1cb-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="bc1cb-112">Run the command as a job</span></span>

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

### <span data-ttu-id="bc1cb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc1cb-113">-DefaultProfile</span></span>
<span data-ttu-id="bc1cb-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bc1cb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc1cb-115">-Fabricname</span><span class="sxs-lookup"><span data-stu-id="bc1cb-115">-FabricName</span></span>
<span data-ttu-id="bc1cb-116">Nome tessuto.</span><span class="sxs-lookup"><span data-stu-id="bc1cb-116">Fabric name.</span></span>

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

### <span data-ttu-id="bc1cb-117">-MappingName</span><span class="sxs-lookup"><span data-stu-id="bc1cb-117">-MappingName</span></span>
<span data-ttu-id="bc1cb-118">Nome del mapping del contenitore di protezione.</span><span class="sxs-lookup"><span data-stu-id="bc1cb-118">Protection container mapping name.</span></span>

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

### <span data-ttu-id="bc1cb-119">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="bc1cb-119">-NoWait</span></span>
<span data-ttu-id="bc1cb-120">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="bc1cb-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="bc1cb-121">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="bc1cb-121">-PolicyId</span></span>
<span data-ttu-id="bc1cb-122">Criteri applicabili.</span><span class="sxs-lookup"><span data-stu-id="bc1cb-122">Applicable policy.</span></span>

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

### <span data-ttu-id="bc1cb-123">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="bc1cb-123">-ProtectionContainerName</span></span>
<span data-ttu-id="bc1cb-124">Nome del contenitore di protezione.</span><span class="sxs-lookup"><span data-stu-id="bc1cb-124">Protection container name.</span></span>

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

### <span data-ttu-id="bc1cb-125">-ProviderSpecificInput</span><span class="sxs-lookup"><span data-stu-id="bc1cb-125">-ProviderSpecificInput</span></span>
<span data-ttu-id="bc1cb-126">Input specifico del provider per l'associazione.</span><span class="sxs-lookup"><span data-stu-id="bc1cb-126">Provider specific input for pairing.</span></span>
<span data-ttu-id="bc1cb-127">Per costruire, vedere la sezione Note per le proprietà di PROVIDERSPECIFICINPUT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="bc1cb-127">To construct, see NOTES section for PROVIDERSPECIFICINPUT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bc1cb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc1cb-128">-ResourceGroupName</span></span>
<span data-ttu-id="bc1cb-129">Nome del gruppo di risorse in cui è presente il Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="bc1cb-129">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="bc1cb-130">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="bc1cb-130">-ResourceName</span></span>
<span data-ttu-id="bc1cb-131">Nome del Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="bc1cb-131">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="bc1cb-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bc1cb-132">-SubscriptionId</span></span>
<span data-ttu-id="bc1cb-133">ID abbonamento.</span><span class="sxs-lookup"><span data-stu-id="bc1cb-133">The subscription Id.</span></span>

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

### <span data-ttu-id="bc1cb-134">-TargetProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="bc1cb-134">-TargetProtectionContainerId</span></span>
<span data-ttu-id="bc1cb-135">Nome del contenitore di protezione univoco di destinazione.</span><span class="sxs-lookup"><span data-stu-id="bc1cb-135">The target unique protection container name.</span></span>

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

### <span data-ttu-id="bc1cb-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bc1cb-136">-Confirm</span></span>
<span data-ttu-id="bc1cb-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc1cb-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc1cb-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc1cb-138">-WhatIf</span></span>
<span data-ttu-id="bc1cb-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bc1cb-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc1cb-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bc1cb-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc1cb-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc1cb-141">CommonParameters</span></span>
<span data-ttu-id="bc1cb-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc1cb-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc1cb-143">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bc1cb-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc1cb-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bc1cb-144">INPUTS</span></span>

## <span data-ttu-id="bc1cb-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bc1cb-145">OUTPUTS</span></span>

### <span data-ttu-id="bc1cb-146">Microsoft. Azure. PowerShell. Cmdlets. migrate. Models. Api20180110. IProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="bc1cb-146">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span></span>

## <span data-ttu-id="bc1cb-147">Note</span><span class="sxs-lookup"><span data-stu-id="bc1cb-147">NOTES</span></span>

<span data-ttu-id="bc1cb-148">ALIAS</span><span class="sxs-lookup"><span data-stu-id="bc1cb-148">ALIASES</span></span>

<span data-ttu-id="bc1cb-149">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bc1cb-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bc1cb-150">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="bc1cb-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bc1cb-151">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bc1cb-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bc1cb-152">PROVIDERSPECIFICINPUT <IReplicationProviderSpecificContainerMappingInput> : input specifico del provider per l'associazione.</span><span class="sxs-lookup"><span data-stu-id="bc1cb-152">PROVIDERSPECIFICINPUT <IReplicationProviderSpecificContainerMappingInput>: Provider specific input for pairing.</span></span>
  - <span data-ttu-id="bc1cb-153">`[InstanceType <String>]`: Il tipo di classe.</span><span class="sxs-lookup"><span data-stu-id="bc1cb-153">`[InstanceType <String>]`: The class type.</span></span>

## <span data-ttu-id="bc1cb-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bc1cb-154">RELATED LINKS</span></span>

