---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/test-azvmwarelocationquotaavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationQuotaAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationQuotaAvailability.md
ms.openlocfilehash: 9cb677ff172c986f18c7c11c00e0f8d7e0bbf5bf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190416"
---
# <span data-ttu-id="1ebd0-101">Test-AzVMWareLocationQuotaAvailability</span><span class="sxs-lookup"><span data-stu-id="1ebd0-101">Test-AzVMWareLocationQuotaAvailability</span></span>

## <span data-ttu-id="1ebd0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1ebd0-102">SYNOPSIS</span></span>
<span data-ttu-id="1ebd0-103">Quota di ritorno per l'abbonamento per area geografica</span><span class="sxs-lookup"><span data-stu-id="1ebd0-103">Return quota for subscription by region</span></span>

## <span data-ttu-id="1ebd0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1ebd0-104">SYNTAX</span></span>

### <span data-ttu-id="1ebd0-105">Controllo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1ebd0-105">Check (Default)</span></span>
```
Test-AzVMWareLocationQuotaAvailability -Location <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1ebd0-106">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1ebd0-106">CheckViaIdentity</span></span>
```
Test-AzVMWareLocationQuotaAvailability -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1ebd0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1ebd0-107">DESCRIPTION</span></span>
<span data-ttu-id="1ebd0-108">Quota di ritorno per l'abbonamento per area geografica</span><span class="sxs-lookup"><span data-stu-id="1ebd0-108">Return quota for subscription by region</span></span>

## <span data-ttu-id="1ebd0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1ebd0-109">EXAMPLES</span></span>

### <span data-ttu-id="1ebd0-110">Esempio 1: verificare la disponibilità delle quote</span><span class="sxs-lookup"><span data-stu-id="1ebd0-110">Example 1: Check quota availability</span></span>
```powershell
PS C:\> Test-AzVMWareLocationQuotaAvailability -Location eastus

Enabled
-------
Disabled
```

<span data-ttu-id="1ebd0-111">Verificare la disponibilità delle quote</span><span class="sxs-lookup"><span data-stu-id="1ebd0-111">Check quota availability</span></span>

## <span data-ttu-id="1ebd0-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1ebd0-112">PARAMETERS</span></span>

### <span data-ttu-id="1ebd0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ebd0-113">-DefaultProfile</span></span>
<span data-ttu-id="1ebd0-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1ebd0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ebd0-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ebd0-115">-InputObject</span></span>
<span data-ttu-id="1ebd0-116">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="1ebd0-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1ebd0-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="1ebd0-117">-Location</span></span>
<span data-ttu-id="1ebd0-118">Area di Azure</span><span class="sxs-lookup"><span data-stu-id="1ebd0-118">Azure region</span></span>

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

### <span data-ttu-id="1ebd0-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1ebd0-119">-SubscriptionId</span></span>
<span data-ttu-id="1ebd0-120">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1ebd0-120">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="1ebd0-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1ebd0-121">-Confirm</span></span>
<span data-ttu-id="1ebd0-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ebd0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ebd0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ebd0-123">-WhatIf</span></span>
<span data-ttu-id="1ebd0-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1ebd0-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ebd0-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1ebd0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ebd0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ebd0-126">CommonParameters</span></span>
<span data-ttu-id="1ebd0-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ebd0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ebd0-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1ebd0-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ebd0-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1ebd0-129">INPUTS</span></span>

### <span data-ttu-id="1ebd0-130">Microsoft. Azure. PowerShell. Cmdlets. VMWare. Models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="1ebd0-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="1ebd0-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1ebd0-131">OUTPUTS</span></span>

### <span data-ttu-id="1ebd0-132">Microsoft. Azure. PowerShell. Cmdlets. VMWare. Models. Api20200320. IQuota</span><span class="sxs-lookup"><span data-stu-id="1ebd0-132">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IQuota</span></span>

## <span data-ttu-id="1ebd0-133">Note</span><span class="sxs-lookup"><span data-stu-id="1ebd0-133">NOTES</span></span>

<span data-ttu-id="1ebd0-134">ALIAS</span><span class="sxs-lookup"><span data-stu-id="1ebd0-134">ALIASES</span></span>

<span data-ttu-id="1ebd0-135">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1ebd0-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1ebd0-136">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="1ebd0-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1ebd0-137">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1ebd0-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1ebd0-138">INPUTOBJECT <IVMWareIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="1ebd0-138">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1ebd0-139">`[AuthorizationName <String>]`: Nome dell'autorizzazione del circuito ExpressRoute nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="1ebd0-139">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="1ebd0-140">`[ClusterName <String>]`: Nome del cluster nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="1ebd0-140">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="1ebd0-141">`[HcxEnterpriseSiteName <String>]`: Nome del sito aziendale di HCX nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="1ebd0-141">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="1ebd0-142">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="1ebd0-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1ebd0-143">`[Location <String>]`: Area di Azure</span><span class="sxs-lookup"><span data-stu-id="1ebd0-143">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="1ebd0-144">`[PrivateCloudName <String>]`: Nome del cloud privato</span><span class="sxs-lookup"><span data-stu-id="1ebd0-144">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="1ebd0-145">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1ebd0-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="1ebd0-146">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="1ebd0-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="1ebd0-147">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1ebd0-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="1ebd0-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1ebd0-148">RELATED LINKS</span></span>

