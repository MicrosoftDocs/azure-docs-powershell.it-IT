---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratereplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationPolicy.md
ms.openlocfilehash: 5978c247f14507934662f5a5d1846a02180cd812
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200777"
---
# <span data-ttu-id="c489d-101">New-AzMigrateReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="c489d-101">New-AzMigrateReplicationPolicy</span></span>

## <span data-ttu-id="c489d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c489d-102">SYNOPSIS</span></span>
<span data-ttu-id="c489d-103">Operazione per creare un criterio di replica</span><span class="sxs-lookup"><span data-stu-id="c489d-103">The operation to create a replication policy</span></span>

## <span data-ttu-id="c489d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c489d-104">SYNTAX</span></span>

```
New-AzMigrateReplicationPolicy -PolicyName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-ProviderSpecificInput <IPolicyProviderSpecificInput>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c489d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c489d-105">DESCRIPTION</span></span>
<span data-ttu-id="c489d-106">Operazione per creare un criterio di replica</span><span class="sxs-lookup"><span data-stu-id="c489d-106">The operation to create a replication policy</span></span>

## <span data-ttu-id="c489d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c489d-107">EXAMPLES</span></span>

### <span data-ttu-id="c489d-108">Esempio 1: creare un criterio di replica</span><span class="sxs-lookup"><span data-stu-id="c489d-108">Example 1: Create a replication policy</span></span>
```powershell
PS C:\> $providerSpecificPolicy = [Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.VMwareCbtPolicyCreationInput]::new()
PS C:\> $providerSpecificPolicy.AppConsistentFrequencyInMinute = 240
PS C:\> $providerSpecificPolicy.InstanceType = "VMwareCbt"
PS C:\> $providerSpecificPolicy.RecoveryPointHistoryInMinute = 4320
PS C:\> $providerSpecificPolicy.CrashConsistentFrequencyInMinute = 60
PS C:\> New-AzMigrateReplicationPolicy -PolicyName TestPolicy -ResourceGroupName ResourceGroup -ResourceName VaultName -SubscriptionId SubscriptionId -ProviderSpecificInput $providerSpecificPolicy

Location Name       Type
-------- ----       ----
         TestPolicy Microsoft.RecoveryServices/vaults/replicationPolicies
         
```

<span data-ttu-id="c489d-109">Crea un criterio per VmWare CBT</span><span class="sxs-lookup"><span data-stu-id="c489d-109">Creates a policy for VmWare Cbt</span></span>

## <span data-ttu-id="c489d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c489d-110">PARAMETERS</span></span>

### <span data-ttu-id="c489d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c489d-111">-AsJob</span></span>
<span data-ttu-id="c489d-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="c489d-112">Run the command as a job</span></span>

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

### <span data-ttu-id="c489d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c489d-113">-DefaultProfile</span></span>
<span data-ttu-id="c489d-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c489d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c489d-115">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="c489d-115">-NoWait</span></span>
<span data-ttu-id="c489d-116">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="c489d-116">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c489d-117">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="c489d-117">-PolicyName</span></span>
<span data-ttu-id="c489d-118">Nome criterio di replica</span><span class="sxs-lookup"><span data-stu-id="c489d-118">Replication policy name</span></span>

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

### <span data-ttu-id="c489d-119">-ProviderSpecificInput</span><span class="sxs-lookup"><span data-stu-id="c489d-119">-ProviderSpecificInput</span></span>
<span data-ttu-id="c489d-120">ReplicationProviderSettings.</span><span class="sxs-lookup"><span data-stu-id="c489d-120">The ReplicationProviderSettings.</span></span>
<span data-ttu-id="c489d-121">Per costruire, vedere la sezione Note per le proprietà di PROVIDERSPECIFICINPUT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="c489d-121">To construct, see NOTES section for PROVIDERSPECIFICINPUT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicyProviderSpecificInput
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c489d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c489d-122">-ResourceGroupName</span></span>
<span data-ttu-id="c489d-123">Nome del gruppo di risorse in cui è presente il Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="c489d-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="c489d-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="c489d-124">-ResourceName</span></span>
<span data-ttu-id="c489d-125">Nome del Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="c489d-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="c489d-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c489d-126">-SubscriptionId</span></span>
<span data-ttu-id="c489d-127">ID abbonamento.</span><span class="sxs-lookup"><span data-stu-id="c489d-127">The subscription Id.</span></span>

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

### <span data-ttu-id="c489d-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c489d-128">-Confirm</span></span>
<span data-ttu-id="c489d-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c489d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c489d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c489d-130">-WhatIf</span></span>
<span data-ttu-id="c489d-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c489d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c489d-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c489d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c489d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c489d-133">CommonParameters</span></span>
<span data-ttu-id="c489d-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c489d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c489d-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c489d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c489d-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c489d-136">INPUTS</span></span>

## <span data-ttu-id="c489d-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c489d-137">OUTPUTS</span></span>

### <span data-ttu-id="c489d-138">Microsoft. Azure. PowerShell. Cmdlets. migrate. Models. Api20180110. IPolicy</span><span class="sxs-lookup"><span data-stu-id="c489d-138">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span></span>

## <span data-ttu-id="c489d-139">Note</span><span class="sxs-lookup"><span data-stu-id="c489d-139">NOTES</span></span>

<span data-ttu-id="c489d-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c489d-140">ALIASES</span></span>

<span data-ttu-id="c489d-141">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c489d-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c489d-142">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="c489d-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c489d-143">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c489d-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c489d-144">PROVIDERSPECIFICINPUT <IPolicyProviderSpecificInput> : ReplicationProviderSettings.</span><span class="sxs-lookup"><span data-stu-id="c489d-144">PROVIDERSPECIFICINPUT <IPolicyProviderSpecificInput>: The ReplicationProviderSettings.</span></span>
  - <span data-ttu-id="c489d-145">`[InstanceType <String>]`: Il tipo di classe.</span><span class="sxs-lookup"><span data-stu-id="c489d-145">`[InstanceType <String>]`: The class type.</span></span>

## <span data-ttu-id="c489d-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c489d-146">RELATED LINKS</span></span>

