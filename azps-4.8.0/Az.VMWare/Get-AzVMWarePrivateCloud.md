---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloud.md
ms.openlocfilehash: 31400d3b9b6e57190a852ae579fffcaa9fc60401
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191397"
---
# <span data-ttu-id="4a4de-101">Get-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="4a4de-101">Get-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="4a4de-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4a4de-102">SYNOPSIS</span></span>
<span data-ttu-id="4a4de-103">Ottenere un cloud privato</span><span class="sxs-lookup"><span data-stu-id="4a4de-103">Get a private cloud</span></span>

## <span data-ttu-id="4a4de-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4a4de-104">SYNTAX</span></span>

### <span data-ttu-id="4a4de-105">List1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4a4de-105">List1 (Default)</span></span>
```
Get-AzVMWarePrivateCloud [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4a4de-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="4a4de-106">Get</span></span>
```
Get-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4a4de-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4a4de-107">GetViaIdentity</span></span>
```
Get-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4a4de-108">Elenco</span><span class="sxs-lookup"><span data-stu-id="4a4de-108">List</span></span>
```
Get-AzVMWarePrivateCloud -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="4a4de-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4a4de-109">DESCRIPTION</span></span>
<span data-ttu-id="4a4de-110">Ottenere un cloud privato</span><span class="sxs-lookup"><span data-stu-id="4a4de-110">Get a private cloud</span></span>

## <span data-ttu-id="4a4de-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4a4de-111">EXAMPLES</span></span>

### <span data-ttu-id="4a4de-112">Esempio 1: elencare il cloud privato in abbonamento</span><span class="sxs-lookup"><span data-stu-id="4a4de-112">Example 1: List private cloud under subscription</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="4a4de-113">Elenco cloud privato in abbonamento</span><span class="sxs-lookup"><span data-stu-id="4a4de-113">List private cloud under subscription</span></span>

### <span data-ttu-id="4a4de-114">Esempio 2: elenco cloud privato in gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="4a4de-114">Example 2: List private cloud under resource group</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="4a4de-115">Elenco cloud privato in gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="4a4de-115">List private cloud under resource group</span></span>

### <span data-ttu-id="4a4de-116">Esempio 3: ottenere cloud privato</span><span class="sxs-lookup"><span data-stu-id="4a4de-116">Example 3: Get private cloud</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="4a4de-117">Ottenere cloud privato</span><span class="sxs-lookup"><span data-stu-id="4a4de-117">Get private cloud</span></span>

## <span data-ttu-id="4a4de-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4a4de-118">PARAMETERS</span></span>

### <span data-ttu-id="4a4de-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a4de-119">-DefaultProfile</span></span>
<span data-ttu-id="4a4de-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4a4de-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a4de-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a4de-121">-InputObject</span></span>
<span data-ttu-id="4a4de-122">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="4a4de-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a4de-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="4a4de-123">-Name</span></span>
<span data-ttu-id="4a4de-124">Nome del cloud privato</span><span class="sxs-lookup"><span data-stu-id="4a4de-124">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a4de-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a4de-125">-ResourceGroupName</span></span>
<span data-ttu-id="4a4de-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4a4de-126">The name of the resource group.</span></span>
<span data-ttu-id="4a4de-127">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="4a4de-127">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a4de-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4a4de-128">-SubscriptionId</span></span>
<span data-ttu-id="4a4de-129">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4a4de-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a4de-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a4de-130">CommonParameters</span></span>
<span data-ttu-id="4a4de-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a4de-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a4de-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a4de-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a4de-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4a4de-133">INPUTS</span></span>

### <span data-ttu-id="4a4de-134">Microsoft. Azure. PowerShell. Cmdlets. VMWare. Models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="4a4de-134">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="4a4de-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4a4de-135">OUTPUTS</span></span>

### <span data-ttu-id="4a4de-136">Microsoft. Azure. PowerShell. Cmdlets. VMWare. Models. Api20200320. IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="4a4de-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="4a4de-137">Note</span><span class="sxs-lookup"><span data-stu-id="4a4de-137">NOTES</span></span>

<span data-ttu-id="4a4de-138">ALIAS</span><span class="sxs-lookup"><span data-stu-id="4a4de-138">ALIASES</span></span>

<span data-ttu-id="4a4de-139">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4a4de-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4a4de-140">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="4a4de-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4a4de-141">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4a4de-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4a4de-142">INPUTOBJECT <IVMWareIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="4a4de-142">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4a4de-143">`[AuthorizationName <String>]`: Nome dell'autorizzazione del circuito ExpressRoute nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="4a4de-143">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="4a4de-144">`[ClusterName <String>]`: Nome del cluster nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="4a4de-144">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="4a4de-145">`[HcxEnterpriseSiteName <String>]`: Nome del sito aziendale di HCX nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="4a4de-145">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="4a4de-146">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="4a4de-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4a4de-147">`[Location <String>]`: Area di Azure</span><span class="sxs-lookup"><span data-stu-id="4a4de-147">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="4a4de-148">`[PrivateCloudName <String>]`: Nome del cloud privato</span><span class="sxs-lookup"><span data-stu-id="4a4de-148">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="4a4de-149">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4a4de-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="4a4de-150">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="4a4de-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="4a4de-151">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4a4de-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="4a4de-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4a4de-152">RELATED LINKS</span></span>
