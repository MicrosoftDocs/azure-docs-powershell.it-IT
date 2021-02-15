---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/test-azvmwarelocationquotaavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Test-AzVMwareLocationQuotaAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Test-AzVMwareLocationQuotaAvailability.md
ms.openlocfilehash: 93ede93fc47d5afcabeda8a38a4d8c5fc57c30c4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182535"
---
# <span data-ttu-id="c8c4b-101">Test-AzVMwareLocationQuotaAvailability</span><span class="sxs-lookup"><span data-stu-id="c8c4b-101">Test-AzVMwareLocationQuotaAvailability</span></span>

## <span data-ttu-id="c8c4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8c4b-102">SYNOPSIS</span></span>
<span data-ttu-id="c8c4b-103">Quota di ritorno per la sottoscrizione per area geografica</span><span class="sxs-lookup"><span data-stu-id="c8c4b-103">Return quota for subscription by region</span></span>

## <span data-ttu-id="c8c4b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c8c4b-104">SYNTAX</span></span>

### <span data-ttu-id="c8c4b-105">Controllo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c8c4b-105">Check (Default)</span></span>
```
Test-AzVMwareLocationQuotaAvailability -Location <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c8c4b-106">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c8c4b-106">CheckViaIdentity</span></span>
```
Test-AzVMwareLocationQuotaAvailability -InputObject <IVMwareIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c8c4b-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c8c4b-107">DESCRIPTION</span></span>
<span data-ttu-id="c8c4b-108">Quota di ritorno per la sottoscrizione per area geografica</span><span class="sxs-lookup"><span data-stu-id="c8c4b-108">Return quota for subscription by region</span></span>

## <span data-ttu-id="c8c4b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c8c4b-109">EXAMPLES</span></span>

### <span data-ttu-id="c8c4b-110">Esempio 1: Verificare la disponibilità delle quote</span><span class="sxs-lookup"><span data-stu-id="c8c4b-110">Example 1: Check quota availability</span></span>
```powershell
PS C:\> Test-AzVMwareLocationQuotaAvailability -Location eastus

Enabled
-------
Disabled
```

<span data-ttu-id="c8c4b-111">Verificare la disponibilità delle quote</span><span class="sxs-lookup"><span data-stu-id="c8c4b-111">Check quota availability</span></span>

## <span data-ttu-id="c8c4b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8c4b-112">PARAMETERS</span></span>

### <span data-ttu-id="c8c4b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8c4b-113">-DefaultProfile</span></span>
<span data-ttu-id="c8c4b-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c8c4b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8c4b-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8c4b-115">-InputObject</span></span>
<span data-ttu-id="c8c4b-116">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="c8c4b-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity
Parameter Sets: CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8c4b-117">-Location</span><span class="sxs-lookup"><span data-stu-id="c8c4b-117">-Location</span></span>
<span data-ttu-id="c8c4b-118">Area geografica Azure</span><span class="sxs-lookup"><span data-stu-id="c8c4b-118">Azure region</span></span>

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

### <span data-ttu-id="c8c4b-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c8c4b-119">-SubscriptionId</span></span>
<span data-ttu-id="c8c4b-120">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c8c4b-120">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="c8c4b-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c8c4b-121">-Confirm</span></span>
<span data-ttu-id="c8c4b-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8c4b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8c4b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8c4b-123">-WhatIf</span></span>
<span data-ttu-id="c8c4b-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c8c4b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8c4b-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c8c4b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8c4b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8c4b-126">CommonParameters</span></span>
<span data-ttu-id="c8c4b-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8c4b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8c4b-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c8c4b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8c4b-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="c8c4b-129">INPUTS</span></span>

### <span data-ttu-id="c8c4b-130">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span><span class="sxs-lookup"><span data-stu-id="c8c4b-130">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span></span>

## <span data-ttu-id="c8c4b-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c8c4b-131">OUTPUTS</span></span>

### <span data-ttu-id="c8c4b-132">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IQuota</span><span class="sxs-lookup"><span data-stu-id="c8c4b-132">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IQuota</span></span>

## <span data-ttu-id="c8c4b-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="c8c4b-133">NOTES</span></span>

<span data-ttu-id="c8c4b-134">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c8c4b-134">ALIASES</span></span>

<span data-ttu-id="c8c4b-135">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="c8c4b-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c8c4b-136">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="c8c4b-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c8c4b-137">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c8c4b-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c8c4b-138">INPUTOBJECT <IVMwareIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="c8c4b-138">INPUTOBJECT <IVMwareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c8c4b-139">`[AuthorizationName <String>]`: nome dell'autorizzazione del circuito ExpressRoute nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="c8c4b-139">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="c8c4b-140">`[ClusterName <String>]`: nome del cluster nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="c8c4b-140">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="c8c4b-141">`[HcxEnterpriseSiteName <String>]`: nome del sito HCX Enterprise nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="c8c4b-141">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="c8c4b-142">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="c8c4b-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c8c4b-143">`[Location <String>]`: Area geografica Azure</span><span class="sxs-lookup"><span data-stu-id="c8c4b-143">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="c8c4b-144">`[PrivateCloudName <String>]`: nome del cloud privato</span><span class="sxs-lookup"><span data-stu-id="c8c4b-144">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="c8c4b-145">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c8c4b-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="c8c4b-146">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="c8c4b-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="c8c4b-147">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c8c4b-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="c8c4b-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c8c4b-148">RELATED LINKS</span></span>

