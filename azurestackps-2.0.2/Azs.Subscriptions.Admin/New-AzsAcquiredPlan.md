---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/new-azsacquiredplan
schema: 2.0.0
ms.openlocfilehash: 0db0f7ae4358e49ff62f94132701be1f4bd4d0b7
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030284"
---
# <span data-ttu-id="1be6b-101">New-AzsAcquiredPlan</span><span class="sxs-lookup"><span data-stu-id="1be6b-101">New-AzsAcquiredPlan</span></span>

## <span data-ttu-id="1be6b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1be6b-102">SYNOPSIS</span></span>


## <span data-ttu-id="1be6b-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1be6b-103">SYNTAX</span></span>

### <span data-ttu-id="1be6b-104">CreateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1be6b-104">CreateExpanded (Default)</span></span>
```
New-AzsAcquiredPlan -TargetSubscriptionId <String> [-PlanAcquisitionId <String>] [-SubscriptionId <String>]
 [-AcquisitionTime <DateTime>] [-ExternalReferenceId <String>] [-Id <String>] [-PlanId <String>]
 [-ProvisioningState <ProvisioningState>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="1be6b-105">Creare</span><span class="sxs-lookup"><span data-stu-id="1be6b-105">Create</span></span>
```
New-AzsAcquiredPlan -TargetSubscriptionId <String> -AcquiredPlanDefinition <IPlanAcquisition>
 [-PlanAcquisitionId <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="1be6b-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1be6b-106">DESCRIPTION</span></span>


## <span data-ttu-id="1be6b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1be6b-107">EXAMPLES</span></span>

### <span data-ttu-id="1be6b-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1be6b-108">Example 1</span></span>
```powershell
PS C:\> New-AzsAcquiredPlan -PlanAcquisitionId $([Guid]::NewGuid()) -PlanId "/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/testplan" -TargetSubscriptionId "d77ed1d7-cb62-4658-a777-386a8ae523dd"

AcquisitionId       : 718c7f7c-4868-479a-98ce-5caaa8f158c1
AcquisitionTime     : 3/12/2020 11:16:08 PM
ExternalReferenceId : 
Id                  : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/acquiredPlan
                      s/718c7f7c-4868-479a-98ce-5caaa8f158c1
PlanId              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/plans/testplan
ProvisioningState   : Succeeded
```

<span data-ttu-id="1be6b-109">Creare un piano per gli abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="1be6b-109">Create a subscription plan.</span></span>

## <span data-ttu-id="1be6b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1be6b-110">PARAMETERS</span></span>

### <span data-ttu-id="1be6b-111">-AcquiredPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="1be6b-111">-AcquiredPlanDefinition</span></span>
<span data-ttu-id="1be6b-112">Per costruire, vedere la sezione Note per le proprietà di ACQUIREDPLANDEFINITION e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="1be6b-112">To construct, see NOTES section for ACQUIREDPLANDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanAcquisition
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="1be6b-113">-AcquisitionTime</span><span class="sxs-lookup"><span data-stu-id="1be6b-113">-AcquisitionTime</span></span>


```yaml
Type: System.DateTime
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1be6b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1be6b-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="1be6b-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="1be6b-115">-ExternalReferenceId</span></span>


```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1be6b-116">-ID</span><span class="sxs-lookup"><span data-stu-id="1be6b-116">-Id</span></span>


```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1be6b-117">-PlanAcquisitionId</span><span class="sxs-lookup"><span data-stu-id="1be6b-117">-PlanAcquisitionId</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: $([Guid]::NewGuid().ToString())
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1be6b-118">-PlanId</span><span class="sxs-lookup"><span data-stu-id="1be6b-118">-PlanId</span></span>


```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1be6b-119">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="1be6b-119">-ProvisioningState</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.ProvisioningState
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1be6b-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1be6b-120">-SubscriptionId</span></span>


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

### <span data-ttu-id="1be6b-121">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1be6b-121">-TargetSubscriptionId</span></span>


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

### <span data-ttu-id="1be6b-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1be6b-122">-Confirm</span></span>
<span data-ttu-id="1be6b-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1be6b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1be6b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1be6b-124">-WhatIf</span></span>
<span data-ttu-id="1be6b-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1be6b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1be6b-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1be6b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1be6b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1be6b-127">CommonParameters</span></span>
<span data-ttu-id="1be6b-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1be6b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1be6b-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1be6b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1be6b-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1be6b-130">INPUTS</span></span>

### <span data-ttu-id="1be6b-131">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IPlanAcquisition</span><span class="sxs-lookup"><span data-stu-id="1be6b-131">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanAcquisition</span></span>

## <span data-ttu-id="1be6b-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1be6b-132">OUTPUTS</span></span>

### <span data-ttu-id="1be6b-133">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IPlanAcquisition</span><span class="sxs-lookup"><span data-stu-id="1be6b-133">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanAcquisition</span></span>

<span data-ttu-id="1be6b-134">ALIAS</span><span class="sxs-lookup"><span data-stu-id="1be6b-134">ALIASES</span></span>

<span data-ttu-id="1be6b-135">New-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="1be6b-135">New-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="1be6b-136">Note</span><span class="sxs-lookup"><span data-stu-id="1be6b-136">NOTES</span></span>

<span data-ttu-id="1be6b-137">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="1be6b-137">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1be6b-138">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1be6b-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="1be6b-139">ACQUIREDPLANDEFINITION <IPlanAcquisition> :</span><span class="sxs-lookup"><span data-stu-id="1be6b-139">ACQUIREDPLANDEFINITION <IPlanAcquisition>:</span></span> 
  - <span data-ttu-id="1be6b-140">`[AcquisitionId <String>]`: Identificatore acquisizione.</span><span class="sxs-lookup"><span data-stu-id="1be6b-140">`[AcquisitionId <String>]`: Acquisition identifier.</span></span>
  - <span data-ttu-id="1be6b-141">`[AcquisitionTime <DateTime?>]`: Tempo di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="1be6b-141">`[AcquisitionTime <DateTime?>]`: Acquisition time.</span></span>
  - <span data-ttu-id="1be6b-142">`[ExternalReferenceId <String>]`: Identificatore di riferimento esterno.</span><span class="sxs-lookup"><span data-stu-id="1be6b-142">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="1be6b-143">`[Id <String>]`: Identificatore nel contesto della sottoscrizione tenant.</span><span class="sxs-lookup"><span data-stu-id="1be6b-143">`[Id <String>]`: Identifier in the tenant subscription context.</span></span>
  - <span data-ttu-id="1be6b-144">`[PlanId <String>]`: Identificatore piano nel contesto dell'abbonamento tenant.</span><span class="sxs-lookup"><span data-stu-id="1be6b-144">`[PlanId <String>]`: Plan identifier in the tenant subscription context.</span></span>
  - <span data-ttu-id="1be6b-145">`[ProvisioningState <ProvisioningState?>]`: Stato del provisioning.</span><span class="sxs-lookup"><span data-stu-id="1be6b-145">`[ProvisioningState <ProvisioningState?>]`: State of the provisioning.</span></span>

## <span data-ttu-id="1be6b-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1be6b-146">RELATED LINKS</span></span>

