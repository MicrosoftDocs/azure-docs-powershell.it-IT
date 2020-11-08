---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/repair-azsalert
schema: 2.0.0
ms.openlocfilehash: b4017fdcabf1c7d955e8e2a754c3fca989448aa6
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2020
ms.locfileid: "94023179"
---
# <span data-ttu-id="5dfcd-101">Repair-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="5dfcd-101">Repair-AzsAlert</span></span>

## <span data-ttu-id="5dfcd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5dfcd-102">SYNOPSIS</span></span>
<span data-ttu-id="5dfcd-103">Ripristina un avviso.</span><span class="sxs-lookup"><span data-stu-id="5dfcd-103">Repairs an alert.</span></span>

## <span data-ttu-id="5dfcd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5dfcd-104">SYNTAX</span></span>

### <span data-ttu-id="5dfcd-105">Ripristino (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5dfcd-105">Repair (Default)</span></span>
```
Repair-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5dfcd-106">RepairViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5dfcd-106">RepairViaIdentity</span></span>
```
Repair-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5dfcd-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5dfcd-107">DESCRIPTION</span></span>
<span data-ttu-id="5dfcd-108">Ripristina un avviso.</span><span class="sxs-lookup"><span data-stu-id="5dfcd-108">Repairs an alert.</span></span>

## <span data-ttu-id="5dfcd-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5dfcd-109">EXAMPLES</span></span>

### <span data-ttu-id="5dfcd-110">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="5dfcd-110">Example 1:</span></span>
```powershell
PS C:\> Repair-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="5dfcd-111">Ripristina un avviso per nome.</span><span class="sxs-lookup"><span data-stu-id="5dfcd-111">Repairs an alert by Name.</span></span>

### <span data-ttu-id="5dfcd-112">Esempio 2:</span><span class="sxs-lookup"><span data-stu-id="5dfcd-112">Example 2:</span></span>
```powershell
PS C:\> Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Repair-AzsAlert
```

<span data-ttu-id="5dfcd-113">Ripristina un avviso tramite piping.</span><span class="sxs-lookup"><span data-stu-id="5dfcd-113">Repairs an alert through piping.</span></span>

## <span data-ttu-id="5dfcd-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5dfcd-114">PARAMETERS</span></span>

### <span data-ttu-id="5dfcd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5dfcd-115">-AsJob</span></span>
<span data-ttu-id="5dfcd-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="5dfcd-116">Run the command as a job</span></span>

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

### <span data-ttu-id="5dfcd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dfcd-117">-DefaultProfile</span></span>
<span data-ttu-id="5dfcd-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5dfcd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5dfcd-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5dfcd-119">-InputObject</span></span>
<span data-ttu-id="5dfcd-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="5dfcd-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity
Parameter Sets: RepairViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="5dfcd-121">-Posizione</span><span class="sxs-lookup"><span data-stu-id="5dfcd-121">-Location</span></span>
<span data-ttu-id="5dfcd-122">Nome dell'area geografica</span><span class="sxs-lookup"><span data-stu-id="5dfcd-122">Name of the region</span></span>

```yaml
Type: System.String
Parameter Sets: Repair
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5dfcd-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="5dfcd-123">-Name</span></span>
<span data-ttu-id="5dfcd-124">Nome dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="5dfcd-124">Name of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair
Aliases: AlertName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5dfcd-125">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="5dfcd-125">-NoWait</span></span>
<span data-ttu-id="5dfcd-126">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="5dfcd-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5dfcd-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5dfcd-127">-PassThru</span></span>
<span data-ttu-id="5dfcd-128">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="5dfcd-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5dfcd-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5dfcd-129">-ResourceGroupName</span></span>
<span data-ttu-id="5dfcd-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5dfcd-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5dfcd-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5dfcd-131">-SubscriptionId</span></span>
<span data-ttu-id="5dfcd-132">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5dfcd-132">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5dfcd-133">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="5dfcd-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5dfcd-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5dfcd-134">-Confirm</span></span>
<span data-ttu-id="5dfcd-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5dfcd-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5dfcd-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5dfcd-136">-WhatIf</span></span>
<span data-ttu-id="5dfcd-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5dfcd-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5dfcd-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5dfcd-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5dfcd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dfcd-139">CommonParameters</span></span>
<span data-ttu-id="5dfcd-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5dfcd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dfcd-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5dfcd-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dfcd-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5dfcd-142">INPUTS</span></span>

### <span data-ttu-id="5dfcd-143">Microsoft. Azure. PowerShell. Cmdlets. InfrastructureInsightsAdmin. Models. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="5dfcd-143">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="5dfcd-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5dfcd-144">OUTPUTS</span></span>

### <span data-ttu-id="5dfcd-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5dfcd-145">System.Boolean</span></span>



## <span data-ttu-id="5dfcd-146">Note</span><span class="sxs-lookup"><span data-stu-id="5dfcd-146">NOTES</span></span>

<span data-ttu-id="5dfcd-147">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="5dfcd-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5dfcd-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5dfcd-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="5dfcd-149">INPUTOBJECT <IInfrastructureInsightsAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="5dfcd-149">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5dfcd-150">`[AlertName <String>]`: Nome dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="5dfcd-150">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="5dfcd-151">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="5dfcd-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5dfcd-152">`[Location <String>]`: Nome dell'area geografica</span><span class="sxs-lookup"><span data-stu-id="5dfcd-152">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="5dfcd-153">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5dfcd-153">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="5dfcd-154">`[ResourceRegistrationId <String>]`: ID registrazione risorse.</span><span class="sxs-lookup"><span data-stu-id="5dfcd-154">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="5dfcd-155">`[ServiceHealth <String>]`: Nome integrità servizio.</span><span class="sxs-lookup"><span data-stu-id="5dfcd-155">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="5dfcd-156">`[ServiceRegistrationId <String>]`: ID registrazione servizio.</span><span class="sxs-lookup"><span data-stu-id="5dfcd-156">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="5dfcd-157">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5dfcd-157">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="5dfcd-158">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="5dfcd-158">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="5dfcd-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5dfcd-159">RELATED LINKS</span></span>

