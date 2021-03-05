---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/test-azvmwarelocationtrialavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Test-AzVMwareLocationTrialAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Test-AzVMwareLocationTrialAvailability.md
ms.openlocfilehash: 133dc4dd259025556ab5f8dd3b848ae70a5101c7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988622"
---
# <span data-ttu-id="cb3f4-101">Test-AzVMWareLocationTrialAvailability</span><span class="sxs-lookup"><span data-stu-id="cb3f4-101">Test-AzVMWareLocationTrialAvailability</span></span>

## <span data-ttu-id="cb3f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb3f4-102">SYNOPSIS</span></span>
<span data-ttu-id="cb3f4-103">Restituire lo stato di valutazione per l'abbonamento in base all'area geografica</span><span class="sxs-lookup"><span data-stu-id="cb3f4-103">Return trial status for subscription by region</span></span>

## <span data-ttu-id="cb3f4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cb3f4-104">SYNTAX</span></span>

### <span data-ttu-id="cb3f4-105">Controllo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cb3f4-105">Check (Default)</span></span>
```
Test-AzVMWareLocationTrialAvailability -Location <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cb3f4-106">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cb3f4-106">CheckViaIdentity</span></span>
```
Test-AzVMWareLocationTrialAvailability -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cb3f4-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cb3f4-107">DESCRIPTION</span></span>
<span data-ttu-id="cb3f4-108">Restituire lo stato di valutazione per l'abbonamento in base all'area geografica</span><span class="sxs-lookup"><span data-stu-id="cb3f4-108">Return trial status for subscription by region</span></span>

## <span data-ttu-id="cb3f4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cb3f4-109">EXAMPLES</span></span>

### <span data-ttu-id="cb3f4-110">Esempio 1: Verificare la disponibilità della versione di valutazione</span><span class="sxs-lookup"><span data-stu-id="cb3f4-110">Example 1: Check trial availability</span></span>
```powershell
PS C:\> Test-AzVMWareLocationTrialAvailability -Location australiaeast

AvailableHost Status
------------- ------
0             TrialDisabled
```

<span data-ttu-id="cb3f4-111">Verificare la disponibilità della versione di valutazione</span><span class="sxs-lookup"><span data-stu-id="cb3f4-111">Check trial availability</span></span>

## <span data-ttu-id="cb3f4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb3f4-112">PARAMETERS</span></span>

### <span data-ttu-id="cb3f4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb3f4-113">-DefaultProfile</span></span>
<span data-ttu-id="cb3f4-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cb3f4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb3f4-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb3f4-115">-InputObject</span></span>
<span data-ttu-id="cb3f4-116">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="cb3f4-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb3f4-117">-Location</span><span class="sxs-lookup"><span data-stu-id="cb3f4-117">-Location</span></span>
<span data-ttu-id="cb3f4-118">Area geografica Azure</span><span class="sxs-lookup"><span data-stu-id="cb3f4-118">Azure region</span></span>

```yaml
Type: System.String
Parameter Sets: Check
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb3f4-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cb3f4-119">-SubscriptionId</span></span>
<span data-ttu-id="cb3f4-120">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="cb3f4-120">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Check
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb3f4-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cb3f4-121">-Confirm</span></span>
<span data-ttu-id="cb3f4-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb3f4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb3f4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb3f4-123">-WhatIf</span></span>
<span data-ttu-id="cb3f4-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cb3f4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb3f4-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cb3f4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb3f4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb3f4-126">CommonParameters</span></span>
<span data-ttu-id="cb3f4-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb3f4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb3f4-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cb3f4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb3f4-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="cb3f4-129">INPUTS</span></span>

### <span data-ttu-id="cb3f4-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="cb3f4-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="cb3f4-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cb3f4-131">OUTPUTS</span></span>

### <span data-ttu-id="cb3f4-132">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ITrial</span><span class="sxs-lookup"><span data-stu-id="cb3f4-132">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ITrial</span></span>

## <span data-ttu-id="cb3f4-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="cb3f4-133">NOTES</span></span>

<span data-ttu-id="cb3f4-134">ALIAS</span><span class="sxs-lookup"><span data-stu-id="cb3f4-134">ALIASES</span></span>

<span data-ttu-id="cb3f4-135">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="cb3f4-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cb3f4-136">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="cb3f4-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cb3f4-137">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cb3f4-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cb3f4-138">INPUTOBJECT <IVMWareIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="cb3f4-138">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cb3f4-139">`[AuthorizationName <String>]`: nome dell'autorizzazione del circuito ExpressRoute nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="cb3f4-139">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="cb3f4-140">`[ClusterName <String>]`: nome del cluster nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="cb3f4-140">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="cb3f4-141">`[HcxEnterpriseSiteName <String>]`: nome del sito HCX Enterprise nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="cb3f4-141">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="cb3f4-142">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="cb3f4-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cb3f4-143">`[Location <String>]`: Area geografica Azure</span><span class="sxs-lookup"><span data-stu-id="cb3f4-143">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="cb3f4-144">`[PrivateCloudName <String>]`: nome del cloud privato</span><span class="sxs-lookup"><span data-stu-id="cb3f4-144">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="cb3f4-145">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cb3f4-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="cb3f4-146">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="cb3f4-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="cb3f4-147">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="cb3f4-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="cb3f4-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cb3f4-148">RELATED LINKS</span></span>

