---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWareCluster.md
ms.openlocfilehash: bf763e152c482c4a3fda4951715b01008a730533
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476537"
---
# <span data-ttu-id="3d184-101">Get-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="3d184-101">Get-AzVMWareCluster</span></span>

## <span data-ttu-id="3d184-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3d184-102">SYNOPSIS</span></span>
<span data-ttu-id="3d184-103">Ottenere un cluster per nome in un cloud privato</span><span class="sxs-lookup"><span data-stu-id="3d184-103">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="3d184-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3d184-104">SYNTAX</span></span>

### <span data-ttu-id="3d184-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3d184-105">List (Default)</span></span>
```
Get-AzVMWareCluster -PrivateCloudName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3d184-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="3d184-106">Get</span></span>
```
Get-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3d184-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3d184-107">GetViaIdentity</span></span>
```
Get-AzVMWareCluster -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="3d184-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3d184-108">DESCRIPTION</span></span>
<span data-ttu-id="3d184-109">Ottenere un cluster per nome in un cloud privato</span><span class="sxs-lookup"><span data-stu-id="3d184-109">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="3d184-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3d184-110">EXAMPLES</span></span>

### <span data-ttu-id="3d184-111">Esempio 1: ottenere il cluster</span><span class="sxs-lookup"><span data-stu-id="3d184-111">Example 1: Get cluster</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="3d184-112">Ottenere un cluster</span><span class="sxs-lookup"><span data-stu-id="3d184-112">Get cluster</span></span>

### <span data-ttu-id="3d184-113">Esempio 2: raggruppamenti elenco</span><span class="sxs-lookup"><span data-stu-id="3d184-113">Example 2: List clusters</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="3d184-114">Raggruppamenti elenco</span><span class="sxs-lookup"><span data-stu-id="3d184-114">List clusters</span></span>

## <span data-ttu-id="3d184-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3d184-115">PARAMETERS</span></span>

### <span data-ttu-id="3d184-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d184-116">-DefaultProfile</span></span>
<span data-ttu-id="3d184-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3d184-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d184-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d184-118">-InputObject</span></span>
<span data-ttu-id="3d184-119">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="3d184-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3d184-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="3d184-120">-Name</span></span>
<span data-ttu-id="3d184-121">Nome del cluster nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="3d184-121">Name of the cluster in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d184-122">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="3d184-122">-PrivateCloudName</span></span>
<span data-ttu-id="3d184-123">Nome del cloud privato</span><span class="sxs-lookup"><span data-stu-id="3d184-123">Name of the private cloud</span></span>

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

### <span data-ttu-id="3d184-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d184-124">-ResourceGroupName</span></span>
<span data-ttu-id="3d184-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3d184-125">The name of the resource group.</span></span>
<span data-ttu-id="3d184-126">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="3d184-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="3d184-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3d184-127">-SubscriptionId</span></span>
<span data-ttu-id="3d184-128">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3d184-128">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d184-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d184-129">CommonParameters</span></span>
<span data-ttu-id="3d184-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d184-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d184-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d184-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d184-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3d184-132">INPUTS</span></span>

### <span data-ttu-id="3d184-133">Microsoft. Azure. PowerShell. Cmdlets. VMWare. Models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="3d184-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="3d184-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3d184-134">OUTPUTS</span></span>

### <span data-ttu-id="3d184-135">Microsoft. Azure. PowerShell. Cmdlets. VMWare. Models. Api20200320. ICluster</span><span class="sxs-lookup"><span data-stu-id="3d184-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="3d184-136">Note</span><span class="sxs-lookup"><span data-stu-id="3d184-136">NOTES</span></span>

<span data-ttu-id="3d184-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="3d184-137">ALIASES</span></span>

<span data-ttu-id="3d184-138">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3d184-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3d184-139">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="3d184-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3d184-140">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3d184-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3d184-141">INPUTOBJECT <IVMWareIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="3d184-141">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3d184-142">`[AuthorizationName <String>]`: Nome dell'autorizzazione del circuito ExpressRoute nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="3d184-142">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="3d184-143">`[ClusterName <String>]`: Nome del cluster nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="3d184-143">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="3d184-144">`[HcxEnterpriseSiteName <String>]`: Nome del sito aziendale di HCX nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="3d184-144">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="3d184-145">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="3d184-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3d184-146">`[Location <String>]`: Area di Azure</span><span class="sxs-lookup"><span data-stu-id="3d184-146">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="3d184-147">`[PrivateCloudName <String>]`: Nome del cloud privato</span><span class="sxs-lookup"><span data-stu-id="3d184-147">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="3d184-148">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3d184-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="3d184-149">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="3d184-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="3d184-150">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3d184-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="3d184-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3d184-151">RELATED LINKS</span></span>

