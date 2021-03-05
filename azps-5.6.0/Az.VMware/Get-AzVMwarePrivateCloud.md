---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/get-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwarePrivateCloud.md
ms.openlocfilehash: ae53ac56d60d61340e2592233901556a0e1d6b62
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988650"
---
# <span data-ttu-id="f963e-101">Get-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="f963e-101">Get-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="f963e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f963e-102">SYNOPSIS</span></span>
<span data-ttu-id="f963e-103">Ottenere un cloud privato</span><span class="sxs-lookup"><span data-stu-id="f963e-103">Get a private cloud</span></span>

## <span data-ttu-id="f963e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f963e-104">SYNTAX</span></span>

### <span data-ttu-id="f963e-105">Elenco1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f963e-105">List1 (Default)</span></span>
```
Get-AzVMWarePrivateCloud [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f963e-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="f963e-106">Get</span></span>
```
Get-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f963e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f963e-107">GetViaIdentity</span></span>
```
Get-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f963e-108">Elenco</span><span class="sxs-lookup"><span data-stu-id="f963e-108">List</span></span>
```
Get-AzVMWarePrivateCloud -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="f963e-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f963e-109">DESCRIPTION</span></span>
<span data-ttu-id="f963e-110">Ottenere un cloud privato</span><span class="sxs-lookup"><span data-stu-id="f963e-110">Get a private cloud</span></span>

## <span data-ttu-id="f963e-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f963e-111">EXAMPLES</span></span>

### <span data-ttu-id="f963e-112">Esempio 1: Elencare il cloud privato nell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="f963e-112">Example 1: List private cloud under subscription</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="f963e-113">Elencare il cloud privato nell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="f963e-113">List private cloud under subscription</span></span>

### <span data-ttu-id="f963e-114">Esempio 2: Elencare il cloud privato nel gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="f963e-114">Example 2: List private cloud under resource group</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="f963e-115">Elencare il cloud privato nel gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="f963e-115">List private cloud under resource group</span></span>

### <span data-ttu-id="f963e-116">Esempio 3: Ottenere un cloud privato</span><span class="sxs-lookup"><span data-stu-id="f963e-116">Example 3: Get private cloud</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="f963e-117">Scarica cloud privato</span><span class="sxs-lookup"><span data-stu-id="f963e-117">Get private cloud</span></span>

## <span data-ttu-id="f963e-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f963e-118">PARAMETERS</span></span>

### <span data-ttu-id="f963e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f963e-119">-DefaultProfile</span></span>
<span data-ttu-id="f963e-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f963e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f963e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f963e-121">-InputObject</span></span>
<span data-ttu-id="f963e-122">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="f963e-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f963e-123">-Name</span><span class="sxs-lookup"><span data-stu-id="f963e-123">-Name</span></span>
<span data-ttu-id="f963e-124">Nome del cloud privato</span><span class="sxs-lookup"><span data-stu-id="f963e-124">Name of the private cloud</span></span>

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

### <span data-ttu-id="f963e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f963e-125">-ResourceGroupName</span></span>
<span data-ttu-id="f963e-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f963e-126">The name of the resource group.</span></span>
<span data-ttu-id="f963e-127">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="f963e-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f963e-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f963e-128">-SubscriptionId</span></span>
<span data-ttu-id="f963e-129">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f963e-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f963e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f963e-130">CommonParameters</span></span>
<span data-ttu-id="f963e-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f963e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f963e-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f963e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f963e-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="f963e-133">INPUTS</span></span>

### <span data-ttu-id="f963e-134">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="f963e-134">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="f963e-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f963e-135">OUTPUTS</span></span>

### <span data-ttu-id="f963e-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="f963e-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="f963e-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="f963e-137">NOTES</span></span>

<span data-ttu-id="f963e-138">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f963e-138">ALIASES</span></span>

<span data-ttu-id="f963e-139">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="f963e-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f963e-140">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="f963e-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f963e-141">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f963e-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f963e-142">INPUTOBJECT <IVMWareIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="f963e-142">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f963e-143">`[AuthorizationName <String>]`: nome dell'autorizzazione del circuito ExpressRoute nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="f963e-143">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="f963e-144">`[ClusterName <String>]`: nome del cluster nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="f963e-144">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="f963e-145">`[HcxEnterpriseSiteName <String>]`: nome del sito HCX Enterprise nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="f963e-145">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="f963e-146">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="f963e-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f963e-147">`[Location <String>]`: Area geografica Azure</span><span class="sxs-lookup"><span data-stu-id="f963e-147">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="f963e-148">`[PrivateCloudName <String>]`: nome del cloud privato</span><span class="sxs-lookup"><span data-stu-id="f963e-148">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="f963e-149">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f963e-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f963e-150">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="f963e-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="f963e-151">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f963e-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="f963e-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f963e-152">RELATED LINKS</span></span>

