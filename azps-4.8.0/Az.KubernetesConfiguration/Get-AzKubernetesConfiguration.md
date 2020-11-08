---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/get-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
ms.openlocfilehash: 3fd93e42b8f38659f61fcbeb0f49040409f635a8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189826"
---
# <span data-ttu-id="dd59c-101">Get-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="dd59c-101">Get-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="dd59c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dd59c-102">SYNOPSIS</span></span>
<span data-ttu-id="dd59c-103">Ottiene i dettagli della configurazione del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="dd59c-103">Gets details of the Source Control Configuration.</span></span>

## <span data-ttu-id="dd59c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dd59c-104">SYNTAX</span></span>

### <span data-ttu-id="dd59c-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dd59c-105">List (Default)</span></span>
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dd59c-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="dd59c-106">Get</span></span>
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dd59c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="dd59c-107">GetViaIdentity</span></span>
```
Get-AzKubernetesConfiguration -InputObject <IKubernetesConfigurationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="dd59c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dd59c-108">DESCRIPTION</span></span>
<span data-ttu-id="dd59c-109">Ottiene i dettagli della configurazione del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="dd59c-109">Gets details of the Source Control Configuration.</span></span>

## <span data-ttu-id="dd59c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dd59c-110">EXAMPLES</span></span>

### <span data-ttu-id="dd59c-111">Esempio 1: ottenere tutte le configurazioni del cluster kubernetes</span><span class="sxs-lookup"><span data-stu-id="dd59c-111">Example 1: Get all configurations of kubernetes cluster</span></span>
```powershell
PS C:\> Get-AzKubernetesConfiguration -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t02 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters

Name        Type
----        ----
conf-test01 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="dd59c-112">Questo comando consente di ottenere tutte le configurazioni del cluster kubernetes.</span><span class="sxs-lookup"><span data-stu-id="dd59c-112">This command gets all configurations of kubernetes cluster.</span></span>

### <span data-ttu-id="dd59c-113">Esempio 2: ottenere una configurazione del cluster kubernetes per nome</span><span class="sxs-lookup"><span data-stu-id="dd59c-113">Example 2: Get a configuration of kubernetes cluster by name</span></span>
```powershell
PS C:\> Get-AzKubernetesConfiguration -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t02 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters -Name conf-t02

Name     Type
----     ----
conf-t02 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="dd59c-114">Questo comando ottiene una configurazione del cluster kubernetes per nome.</span><span class="sxs-lookup"><span data-stu-id="dd59c-114">This command gets a configuration of kubernetes cluster by name.</span></span>

### <span data-ttu-id="dd59c-115">Esempio 3: ottenere una configurazione di kubernetes cluster by Object</span><span class="sxs-lookup"><span data-stu-id="dd59c-115">Example 3: Get a configuration of kubernetes cluster by object</span></span>
```powershell
PS C:\> $kubConf = New-AzKubernetesConfiguration -Name conf-test02 -ClusterName connaks-dkc29c -ResourceGroupName connaks-rg-w9vlnp -RepositoryUrl http://github.com/xxxx
PS C:\> Get-AzKubernetesConfiguration -InputObject $kubConf

Name     Type
----     ----
conf-t02 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="dd59c-116">Questo comando ottiene una configurazione di kubernetes cluster by Object.</span><span class="sxs-lookup"><span data-stu-id="dd59c-116">This command gets a configuration of kubernetes cluster by object.</span></span>

### <span data-ttu-id="dd59c-117">Esempio 4: ottenere una configurazione del cluster kubernetes per pipeline</span><span class="sxs-lookup"><span data-stu-id="dd59c-117">Example 4: Get a configuration of kubernetes cluster by pipeline</span></span>
```powershell
PS C:\> @{Id='/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/connaks-rg-w9vlnp/providers/Microsoft.Kubernetes/connectedClusters/connaks-d983yc/providers/Microsoft.KubernetesConfiguration/sourceControlConfigurations/conf-test01'} | Get-AzKubernetesConfiguration

Name        Type
----        ----
conf-test01 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="dd59c-118">Questo comando ottiene una configurazione del cluster kubernetes per pipeline.</span><span class="sxs-lookup"><span data-stu-id="dd59c-118">This command gets a configuration of kubernetes cluster by pipeline.</span></span>

## <span data-ttu-id="dd59c-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dd59c-119">PARAMETERS</span></span>

### <span data-ttu-id="dd59c-120">-Clustername</span><span class="sxs-lookup"><span data-stu-id="dd59c-120">-ClusterName</span></span>
<span data-ttu-id="dd59c-121">Il nome del cluster kubernetes.</span><span class="sxs-lookup"><span data-stu-id="dd59c-121">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="dd59c-122">-ClusterRp</span><span class="sxs-lookup"><span data-stu-id="dd59c-122">-ClusterRp</span></span>
<span data-ttu-id="dd59c-123">Il cluster Kubernetes RP-Microsoft. ContainerService (per i cluster AKS) o Microsoft. Kubernetes (per i cluster OnPrem K8S).</span><span class="sxs-lookup"><span data-stu-id="dd59c-123">The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="dd59c-124">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="dd59c-124">-ClusterType</span></span>
<span data-ttu-id="dd59c-125">Il nome della risorsa del cluster Kubernetes-managedClusters (per i cluster AKS) o connectedClusters (per i cluster OnPrem K8S).</span><span class="sxs-lookup"><span data-stu-id="dd59c-125">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="dd59c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd59c-126">-DefaultProfile</span></span>
<span data-ttu-id="dd59c-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dd59c-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd59c-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd59c-128">-InputObject</span></span>
<span data-ttu-id="dd59c-129">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="dd59c-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd59c-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="dd59c-130">-Name</span></span>
<span data-ttu-id="dd59c-131">Nome della configurazione del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="dd59c-131">Name of the Source Control Configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SourceControlConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd59c-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd59c-132">-ResourceGroupName</span></span>
<span data-ttu-id="dd59c-133">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dd59c-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="dd59c-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dd59c-134">-SubscriptionId</span></span>
<span data-ttu-id="dd59c-135">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="dd59c-135">The Azure subscription ID.</span></span>
<span data-ttu-id="dd59c-136">Si tratta di una stringa formattata con GUID (ad esempio 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="dd59c-136">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="dd59c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd59c-137">CommonParameters</span></span>
<span data-ttu-id="dd59c-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd59c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd59c-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd59c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd59c-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dd59c-140">INPUTS</span></span>

### <span data-ttu-id="dd59c-141">Microsoft. Azure. PowerShell. Cmdlets. KubernetesConfiguration. Models. IKubernetesConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="dd59c-141">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span></span>

## <span data-ttu-id="dd59c-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dd59c-142">OUTPUTS</span></span>

### <span data-ttu-id="dd59c-143">Microsoft. Azure. PowerShell. Cmdlets. KubernetesConfiguration. Models. Api20191101Preview. ISourceControlConfiguration</span><span class="sxs-lookup"><span data-stu-id="dd59c-143">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20191101Preview.ISourceControlConfiguration</span></span>

## <span data-ttu-id="dd59c-144">Note</span><span class="sxs-lookup"><span data-stu-id="dd59c-144">NOTES</span></span>

<span data-ttu-id="dd59c-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="dd59c-145">ALIASES</span></span>

<span data-ttu-id="dd59c-146">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dd59c-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dd59c-147">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="dd59c-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dd59c-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dd59c-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dd59c-149">INPUTOBJECT <IKubernetesConfigurationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="dd59c-149">INPUTOBJECT <IKubernetesConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dd59c-150">`[ClusterName <String>]`: Nome del cluster kubernetes.</span><span class="sxs-lookup"><span data-stu-id="dd59c-150">`[ClusterName <String>]`: The name of the kubernetes cluster.</span></span>
  - <span data-ttu-id="dd59c-151">`[ClusterResourceName <String>]`: Il nome della risorsa del cluster Kubernetes-managedClusters (per i cluster AKS) o connectedClusters (per i cluster OnPrem K8S).</span><span class="sxs-lookup"><span data-stu-id="dd59c-151">`[ClusterResourceName <String>]`: The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="dd59c-152">`[ClusterRp <String>]`: Il cluster Kubernetes RP-Microsoft. ContainerService (per i cluster AKS) o Microsoft. Kubernetes (per i cluster OnPrem K8S).</span><span class="sxs-lookup"><span data-stu-id="dd59c-152">`[ClusterRp <String>]`: The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="dd59c-153">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="dd59c-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dd59c-154">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dd59c-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="dd59c-155">`[SourceControlConfigurationName <String>]`: Nome della configurazione del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="dd59c-155">`[SourceControlConfigurationName <String>]`: Name of the Source Control Configuration.</span></span>
  - <span data-ttu-id="dd59c-156">`[SubscriptionId <String>]`: ID abbonamento Azure.</span><span class="sxs-lookup"><span data-stu-id="dd59c-156">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="dd59c-157">Si tratta di una stringa formattata con GUID (ad esempio 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="dd59c-157">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="dd59c-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dd59c-158">RELATED LINKS</span></span>

