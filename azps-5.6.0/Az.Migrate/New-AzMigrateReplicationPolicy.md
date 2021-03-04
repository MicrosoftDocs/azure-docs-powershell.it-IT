---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/new-azmigratereplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationPolicy.md
ms.openlocfilehash: 7f9b78a6c287f7135f2463a6cfe63b2963ffe362
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982670"
---
# <span data-ttu-id="36a29-101">New-AzMigrateReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="36a29-101">New-AzMigrateReplicationPolicy</span></span>

## <span data-ttu-id="36a29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36a29-102">SYNOPSIS</span></span>
<span data-ttu-id="36a29-103">Operazione per la creazione di criteri di replica</span><span class="sxs-lookup"><span data-stu-id="36a29-103">The operation to create a replication policy</span></span>

## <span data-ttu-id="36a29-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="36a29-104">SYNTAX</span></span>

```
New-AzMigrateReplicationPolicy -PolicyName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-ProviderSpecificInput <IPolicyProviderSpecificInput>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="36a29-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="36a29-105">DESCRIPTION</span></span>
<span data-ttu-id="36a29-106">Operazione per la creazione di criteri di replica</span><span class="sxs-lookup"><span data-stu-id="36a29-106">The operation to create a replication policy</span></span>

## <span data-ttu-id="36a29-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="36a29-107">EXAMPLES</span></span>

### <span data-ttu-id="36a29-108">Esempio 1: Creare criteri di replica</span><span class="sxs-lookup"><span data-stu-id="36a29-108">Example 1: Create a replication policy</span></span>
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

<span data-ttu-id="36a29-109">Crea un criterio per VmWare Cbt</span><span class="sxs-lookup"><span data-stu-id="36a29-109">Creates a policy for VmWare Cbt</span></span>

## <span data-ttu-id="36a29-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36a29-110">PARAMETERS</span></span>

### <span data-ttu-id="36a29-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="36a29-111">-AsJob</span></span>
<span data-ttu-id="36a29-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="36a29-112">Run the command as a job</span></span>

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

### <span data-ttu-id="36a29-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36a29-113">-DefaultProfile</span></span>
<span data-ttu-id="36a29-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="36a29-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36a29-115">-NoWait</span><span class="sxs-lookup"><span data-stu-id="36a29-115">-NoWait</span></span>
<span data-ttu-id="36a29-116">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="36a29-116">Run the command asynchronously</span></span>

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

### <span data-ttu-id="36a29-117">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="36a29-117">-PolicyName</span></span>
<span data-ttu-id="36a29-118">Nome dei criteri di replica</span><span class="sxs-lookup"><span data-stu-id="36a29-118">Replication policy name</span></span>

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

### <span data-ttu-id="36a29-119">-ProviderSpecificInput</span><span class="sxs-lookup"><span data-stu-id="36a29-119">-ProviderSpecificInput</span></span>
<span data-ttu-id="36a29-120">The ReplicationProviderSettings.</span><span class="sxs-lookup"><span data-stu-id="36a29-120">The ReplicationProviderSettings.</span></span>
<span data-ttu-id="36a29-121">Per creare, vedere la sezione NOTES per le proprietà PROVIDERSPECIFICINPUT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="36a29-121">To construct, see NOTES section for PROVIDERSPECIFICINPUT properties and create a hash table.</span></span>

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

### <span data-ttu-id="36a29-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36a29-122">-ResourceGroupName</span></span>
<span data-ttu-id="36a29-123">Nome del gruppo di risorse in cui è presente la vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="36a29-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="36a29-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="36a29-124">-ResourceName</span></span>
<span data-ttu-id="36a29-125">Nome del vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="36a29-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="36a29-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="36a29-126">-SubscriptionId</span></span>
<span data-ttu-id="36a29-127">ID sottoscrizione di Azure in cui è stato creato il progetto di migrazione.</span><span class="sxs-lookup"><span data-stu-id="36a29-127">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="36a29-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36a29-128">-Confirm</span></span>
<span data-ttu-id="36a29-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36a29-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36a29-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36a29-130">-WhatIf</span></span>
<span data-ttu-id="36a29-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="36a29-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36a29-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="36a29-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36a29-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36a29-133">CommonParameters</span></span>
<span data-ttu-id="36a29-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36a29-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36a29-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="36a29-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36a29-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="36a29-136">INPUTS</span></span>

## <span data-ttu-id="36a29-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="36a29-137">OUTPUTS</span></span>

### <span data-ttu-id="36a29-138">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span><span class="sxs-lookup"><span data-stu-id="36a29-138">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span></span>

## <span data-ttu-id="36a29-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="36a29-139">NOTES</span></span>

<span data-ttu-id="36a29-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="36a29-140">ALIASES</span></span>

<span data-ttu-id="36a29-141">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="36a29-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="36a29-142">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="36a29-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="36a29-143">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="36a29-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="36a29-144">PROVIDERSPECIFICINPUT: <IPolicyProviderSpecificInput> ReplicationProviderSettings.</span><span class="sxs-lookup"><span data-stu-id="36a29-144">PROVIDERSPECIFICINPUT <IPolicyProviderSpecificInput>: The ReplicationProviderSettings.</span></span>
  - <span data-ttu-id="36a29-145">`[InstanceType <String>]`: il tipo di classe.</span><span class="sxs-lookup"><span data-stu-id="36a29-145">`[InstanceType <String>]`: The class type.</span></span>

## <span data-ttu-id="36a29-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="36a29-146">RELATED LINKS</span></span>

