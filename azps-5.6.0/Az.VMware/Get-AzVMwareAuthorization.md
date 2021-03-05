---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/get-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwareAuthorization.md
ms.openlocfilehash: dad73292e6875e2cf38244ed74e0519490860c4f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991827"
---
# <span data-ttu-id="72c1c-101">Get-AzVMWareAuthorization</span><span class="sxs-lookup"><span data-stu-id="72c1c-101">Get-AzVMWareAuthorization</span></span>

## <span data-ttu-id="72c1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72c1c-102">SYNOPSIS</span></span>
<span data-ttu-id="72c1c-103">Ottenere un'autorizzazione del circuito ExpressRoute in base al nome in un cloud privato</span><span class="sxs-lookup"><span data-stu-id="72c1c-103">Get an ExpressRoute Circuit Authorization by name in a private cloud</span></span>

## <span data-ttu-id="72c1c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="72c1c-104">SYNTAX</span></span>

### <span data-ttu-id="72c1c-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="72c1c-105">List (Default)</span></span>
```
Get-AzVMWareAuthorization -PrivateCloudName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="72c1c-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="72c1c-106">Get</span></span>
```
Get-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="72c1c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="72c1c-107">GetViaIdentity</span></span>
```
Get-AzVMWareAuthorization -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="72c1c-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="72c1c-108">DESCRIPTION</span></span>
<span data-ttu-id="72c1c-109">Ottenere un'autorizzazione del circuito ExpressRoute in base al nome in un cloud privato</span><span class="sxs-lookup"><span data-stu-id="72c1c-109">Get an ExpressRoute Circuit Authorization by name in a private cloud</span></span>

## <span data-ttu-id="72c1c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="72c1c-110">EXAMPLES</span></span>

### <span data-ttu-id="72c1c-111">Esempio 1: Ottenere l'autorizzazione</span><span class="sxs-lookup"><span data-stu-id="72c1c-111">Example 1: Get authorization</span></span>
```powershell
PS C:\> Get-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="72c1c-112">Questo cmdlet ottiene `azps-test-auth` l'autorizzazione nel cloud privato `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="72c1c-112">This cmdlet gets authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

### <span data-ttu-id="72c1c-113">Esempio 2: Autorizzazione per l'elenco</span><span class="sxs-lookup"><span data-stu-id="72c1c-113">Example 2: List authorization</span></span>
```powershell
PS C:\> Get-AzVMWareAuthorization -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="72c1c-114">Questo cmdlet elenca `azps-test-auth` l'autorizzazione nel cloud privato `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="72c1c-114">This cmdlet lists authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

## <span data-ttu-id="72c1c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72c1c-115">PARAMETERS</span></span>

### <span data-ttu-id="72c1c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72c1c-116">-DefaultProfile</span></span>
<span data-ttu-id="72c1c-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="72c1c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72c1c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72c1c-118">-InputObject</span></span>
<span data-ttu-id="72c1c-119">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="72c1c-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="72c1c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="72c1c-120">-Name</span></span>
<span data-ttu-id="72c1c-121">Nome dell'autorizzazione del circuito ExpressRoute nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="72c1c-121">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AuthorizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72c1c-122">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="72c1c-122">-PrivateCloudName</span></span>
<span data-ttu-id="72c1c-123">Nome del cloud privato</span><span class="sxs-lookup"><span data-stu-id="72c1c-123">Name of the private cloud</span></span>

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

### <span data-ttu-id="72c1c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72c1c-124">-ResourceGroupName</span></span>
<span data-ttu-id="72c1c-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="72c1c-125">The name of the resource group.</span></span>
<span data-ttu-id="72c1c-126">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="72c1c-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="72c1c-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="72c1c-127">-SubscriptionId</span></span>
<span data-ttu-id="72c1c-128">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="72c1c-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="72c1c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72c1c-129">CommonParameters</span></span>
<span data-ttu-id="72c1c-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72c1c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72c1c-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="72c1c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72c1c-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="72c1c-132">INPUTS</span></span>

### <span data-ttu-id="72c1c-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="72c1c-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="72c1c-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="72c1c-134">OUTPUTS</span></span>

### <span data-ttu-id="72c1c-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span><span class="sxs-lookup"><span data-stu-id="72c1c-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span></span>

## <span data-ttu-id="72c1c-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="72c1c-136">NOTES</span></span>

<span data-ttu-id="72c1c-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="72c1c-137">ALIASES</span></span>

<span data-ttu-id="72c1c-138">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="72c1c-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="72c1c-139">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="72c1c-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="72c1c-140">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="72c1c-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="72c1c-141">INPUTOBJECT <IVMWareIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="72c1c-141">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="72c1c-142">`[AuthorizationName <String>]`: nome dell'autorizzazione del circuito ExpressRoute nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="72c1c-142">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="72c1c-143">`[ClusterName <String>]`: nome del cluster nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="72c1c-143">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="72c1c-144">`[HcxEnterpriseSiteName <String>]`: nome del sito HCX Enterprise nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="72c1c-144">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="72c1c-145">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="72c1c-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="72c1c-146">`[Location <String>]`: Area geografica Azure</span><span class="sxs-lookup"><span data-stu-id="72c1c-146">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="72c1c-147">`[PrivateCloudName <String>]`: nome del cloud privato</span><span class="sxs-lookup"><span data-stu-id="72c1c-147">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="72c1c-148">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="72c1c-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="72c1c-149">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="72c1c-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="72c1c-150">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="72c1c-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="72c1c-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="72c1c-151">RELATED LINKS</span></span>

