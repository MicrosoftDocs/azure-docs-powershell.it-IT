---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWareAuthorization.md
ms.openlocfilehash: fc89f62711744ad1e6bd7182eeb61fffd0478eaf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345007"
---
# <span data-ttu-id="50ff4-101">Get-AzVMWareAuthorization</span><span class="sxs-lookup"><span data-stu-id="50ff4-101">Get-AzVMWareAuthorization</span></span>

## <span data-ttu-id="50ff4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="50ff4-102">SYNOPSIS</span></span>
<span data-ttu-id="50ff4-103">Ottenere un'autorizzazione del circuito ExpressRoute per nome in un cloud privato</span><span class="sxs-lookup"><span data-stu-id="50ff4-103">Get an ExpressRoute Circuit Authorization by name in a private cloud</span></span>

## <span data-ttu-id="50ff4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="50ff4-104">SYNTAX</span></span>

### <span data-ttu-id="50ff4-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="50ff4-105">List (Default)</span></span>
```
Get-AzVMWareAuthorization -PrivateCloudName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="50ff4-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="50ff4-106">Get</span></span>
```
Get-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="50ff4-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="50ff4-107">GetViaIdentity</span></span>
```
Get-AzVMWareAuthorization -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="50ff4-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50ff4-108">DESCRIPTION</span></span>
<span data-ttu-id="50ff4-109">Ottenere un'autorizzazione del circuito ExpressRoute per nome in un cloud privato</span><span class="sxs-lookup"><span data-stu-id="50ff4-109">Get an ExpressRoute Circuit Authorization by name in a private cloud</span></span>

## <span data-ttu-id="50ff4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="50ff4-110">EXAMPLES</span></span>

### <span data-ttu-id="50ff4-111">Esempio 1: ottenere l'autorizzazione</span><span class="sxs-lookup"><span data-stu-id="50ff4-111">Example 1: Get authorization</span></span>
```powershell
PS C:\> Get-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="50ff4-112">Questo cmdlet ottiene l'autorizzazione `azps-test-auth` in private cloud `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="50ff4-112">This cmdlet gets authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

### <span data-ttu-id="50ff4-113">Esempio 2: autorizzazione elenco</span><span class="sxs-lookup"><span data-stu-id="50ff4-113">Example 2: List authorization</span></span>
```powershell
PS C:\> Get-AzVMWareAuthorization -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="50ff4-114">Questo cmdlet elenca l'autorizzazione `azps-test-auth` in private cloud `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="50ff4-114">This cmdlet lists authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

## <span data-ttu-id="50ff4-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="50ff4-115">PARAMETERS</span></span>

### <span data-ttu-id="50ff4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50ff4-116">-DefaultProfile</span></span>
<span data-ttu-id="50ff4-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="50ff4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50ff4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50ff4-118">-InputObject</span></span>
<span data-ttu-id="50ff4-119">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="50ff4-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="50ff4-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="50ff4-120">-Name</span></span>
<span data-ttu-id="50ff4-121">Nome dell'autorizzazione del circuito ExpressRoute nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="50ff4-121">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

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

### <span data-ttu-id="50ff4-122">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="50ff4-122">-PrivateCloudName</span></span>
<span data-ttu-id="50ff4-123">Nome del cloud privato</span><span class="sxs-lookup"><span data-stu-id="50ff4-123">Name of the private cloud</span></span>

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

### <span data-ttu-id="50ff4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50ff4-124">-ResourceGroupName</span></span>
<span data-ttu-id="50ff4-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="50ff4-125">The name of the resource group.</span></span>
<span data-ttu-id="50ff4-126">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="50ff4-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="50ff4-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="50ff4-127">-SubscriptionId</span></span>
<span data-ttu-id="50ff4-128">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="50ff4-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="50ff4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50ff4-129">CommonParameters</span></span>
<span data-ttu-id="50ff4-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50ff4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50ff4-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="50ff4-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50ff4-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="50ff4-132">INPUTS</span></span>

### <span data-ttu-id="50ff4-133">Microsoft. Azure. PowerShell. Cmdlets. VMWare. Models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="50ff4-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="50ff4-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="50ff4-134">OUTPUTS</span></span>

### <span data-ttu-id="50ff4-135">Microsoft. Azure. PowerShell. Cmdlets. VMWare. Models. Api20200320. IExpressRouteAuthorization</span><span class="sxs-lookup"><span data-stu-id="50ff4-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span></span>

## <span data-ttu-id="50ff4-136">Note</span><span class="sxs-lookup"><span data-stu-id="50ff4-136">NOTES</span></span>

<span data-ttu-id="50ff4-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="50ff4-137">ALIASES</span></span>

<span data-ttu-id="50ff4-138">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="50ff4-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="50ff4-139">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="50ff4-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="50ff4-140">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="50ff4-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="50ff4-141">INPUTOBJECT <IVMWareIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="50ff4-141">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="50ff4-142">`[AuthorizationName <String>]`: Nome dell'autorizzazione del circuito ExpressRoute nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="50ff4-142">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="50ff4-143">`[ClusterName <String>]`: Nome del cluster nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="50ff4-143">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="50ff4-144">`[HcxEnterpriseSiteName <String>]`: Nome del sito aziendale di HCX nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="50ff4-144">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="50ff4-145">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="50ff4-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="50ff4-146">`[Location <String>]`: Area di Azure</span><span class="sxs-lookup"><span data-stu-id="50ff4-146">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="50ff4-147">`[PrivateCloudName <String>]`: Nome del cloud privato</span><span class="sxs-lookup"><span data-stu-id="50ff4-147">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="50ff4-148">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="50ff4-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="50ff4-149">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="50ff4-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="50ff4-150">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="50ff4-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="50ff4-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="50ff4-151">RELATED LINKS</span></span>

