---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/get-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
ms.openlocfilehash: daa058d1f3cc13e073d8533403341dad3db7c319
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185350"
---
# <span data-ttu-id="b613d-101">Get-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="b613d-101">Get-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="b613d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b613d-102">SYNOPSIS</span></span>
<span data-ttu-id="b613d-103">Recupera i dettagli della configurazione del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="b613d-103">Gets details of the Source Control Configuration.</span></span>

## <span data-ttu-id="b613d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b613d-104">SYNTAX</span></span>

### <span data-ttu-id="b613d-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b613d-105">List (Default)</span></span>
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b613d-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="b613d-106">Get</span></span>
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b613d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b613d-107">GetViaIdentity</span></span>
```
Get-AzKubernetesConfiguration -InputObject <IKubernetesConfigurationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b613d-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b613d-108">DESCRIPTION</span></span>
<span data-ttu-id="b613d-109">Recupera i dettagli della configurazione del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="b613d-109">Gets details of the Source Control Configuration.</span></span>

## <span data-ttu-id="b613d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b613d-110">EXAMPLES</span></span>

### <span data-ttu-id="b613d-111">Esempio 1: Ottenere tutte le configurazioni del cluster kubernetes</span><span class="sxs-lookup"><span data-stu-id="b613d-111">Example 1: Get all configurations of kubernetes cluster</span></span>
```powershell
PS C:\> Get-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:29:33 AM                                             12/21/2020 5:29:33 AM                                                          Microsoft.KubernetesConfiguration/so…
k8sconfig-t01 12/21/2020 5:26:17 AM                                             12/21/2020 5:27:45 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="b613d-112">Questo comando recupera tutte le configurazioni del cluster kubernetes.</span><span class="sxs-lookup"><span data-stu-id="b613d-112">This command gets all configurations of kubernetes cluster.</span></span>

### <span data-ttu-id="b613d-113">Esempio 2: Ottenere una configurazione di cluster kubernetes in base al nome</span><span class="sxs-lookup"><span data-stu-id="b613d-113">Example 2: Get a configuration of kubernetes cluster by name</span></span>
```powershell
PS C:\>  Get-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters -Name  k8sconfig-t02

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:29:33 AM                                             12/21/2020 5:29:33 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="b613d-114">Questo comando ottiene una configurazione di cluster kubernetes in base al nome.</span><span class="sxs-lookup"><span data-stu-id="b613d-114">This command gets a configuration of kubernetes cluster by name.</span></span>

### <span data-ttu-id="b613d-115">Esempio 3: Ottenere una configurazione di kubernetes raggruppate per oggetto</span><span class="sxs-lookup"><span data-stu-id="b613d-115">Example 3: Get a configuration of kubernetes cluster by object</span></span>
```powershell
PS C:\> $kubConf = New-AzKubernetesConfiguration -Name k8sconfig-t02 -ClusterName connaks-dkc29c -ResourceGroupName connaks-rg-w9vlnp -RepositoryUrl http://github.com/xxxx
PS C:\> Get-AzKubernetesConfiguration -InputObject $kubConf

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:29:33 AM                                             12/21/2020 5:29:33 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="b613d-116">Questo comando ottiene una configurazione di kubernetes raggruppati per oggetto.</span><span class="sxs-lookup"><span data-stu-id="b613d-116">This command gets a configuration of kubernetes cluster by object.</span></span>

### <span data-ttu-id="b613d-117">Esempio 4: Ottenere una configurazione di kubernetes cluster by pipeline</span><span class="sxs-lookup"><span data-stu-id="b613d-117">Example 4: Get a configuration of kubernetes cluster by pipeline</span></span>
```powershell
PS C:\> @{Id='/subscriptions/xxxxx-xxxxxxx-xxxxx-xxxxxx/resourceGroups/connaks-rg-w9vlnp/providers/Microsoft.Kubernetes/connectedClusters/connaks-d983yc/providers/Microsoft.KubernetesConfiguration/sourceControlConfigurations/k8sconfig-t02'} | Get-AzKubernetesConfiguration

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:29:33 AM                                             12/21/2020 5:29:33 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="b613d-118">Questo comando ottiene una configurazione di kubernetes cluster by pipeline.</span><span class="sxs-lookup"><span data-stu-id="b613d-118">This command gets a configuration of kubernetes cluster by pipeline.</span></span>

## <span data-ttu-id="b613d-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b613d-119">PARAMETERS</span></span>

### <span data-ttu-id="b613d-120">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b613d-120">-ClusterName</span></span>
<span data-ttu-id="b613d-121">Il nome del cluster kubernetes.</span><span class="sxs-lookup"><span data-stu-id="b613d-121">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="b613d-122">-ClusterRp</span><span class="sxs-lookup"><span data-stu-id="b613d-122">-ClusterRp</span></span>
<span data-ttu-id="b613d-123">Il cluster Kubernetes RP - Microsoft.ContainerService (per cluster AKS) o Microsoft.Kubernetes (per cluster K8S OnPrem).</span><span class="sxs-lookup"><span data-stu-id="b613d-123">The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="b613d-124">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="b613d-124">-ClusterType</span></span>
<span data-ttu-id="b613d-125">Nome della risorsa cluster Kubernetes: managedClusters (per i cluster AKS) o connectedClusters (per i cluster K8S OnPrem).</span><span class="sxs-lookup"><span data-stu-id="b613d-125">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="b613d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b613d-126">-DefaultProfile</span></span>
<span data-ttu-id="b613d-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b613d-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b613d-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b613d-128">-InputObject</span></span>
<span data-ttu-id="b613d-129">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="b613d-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b613d-130">-Name</span><span class="sxs-lookup"><span data-stu-id="b613d-130">-Name</span></span>
<span data-ttu-id="b613d-131">Nome della configurazione del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="b613d-131">Name of the Source Control Configuration.</span></span>

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

### <span data-ttu-id="b613d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b613d-132">-ResourceGroupName</span></span>
<span data-ttu-id="b613d-133">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b613d-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="b613d-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b613d-134">-SubscriptionId</span></span>
<span data-ttu-id="b613d-135">ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="b613d-135">The Azure subscription ID.</span></span>
<span data-ttu-id="b613d-136">Stringa in formato GUID, ad esempio 00000000-0000-0000-0000-0000-00000000000000</span><span class="sxs-lookup"><span data-stu-id="b613d-136">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="b613d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b613d-137">CommonParameters</span></span>
<span data-ttu-id="b613d-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b613d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b613d-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b613d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b613d-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="b613d-140">INPUTS</span></span>

### <span data-ttu-id="b613d-141">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="b613d-141">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span></span>

## <span data-ttu-id="b613d-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b613d-142">OUTPUTS</span></span>

### <span data-ttu-id="b613d-143">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20201001Preview.ISourceControlConfiguration</span><span class="sxs-lookup"><span data-stu-id="b613d-143">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20201001Preview.ISourceControlConfiguration</span></span>

## <span data-ttu-id="b613d-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="b613d-144">NOTES</span></span>

<span data-ttu-id="b613d-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b613d-145">ALIASES</span></span>

<span data-ttu-id="b613d-146">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="b613d-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b613d-147">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="b613d-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b613d-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b613d-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b613d-149">INPUTOBJECT <IKubernetesConfigurationIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="b613d-149">INPUTOBJECT <IKubernetesConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b613d-150">`[ClusterName <String>]`: il nome del cluster kubernetes.</span><span class="sxs-lookup"><span data-stu-id="b613d-150">`[ClusterName <String>]`: The name of the kubernetes cluster.</span></span>
  - <span data-ttu-id="b613d-151">`[ClusterResourceName <String>]`: il nome della risorsa cluster Kubernetes - managedClusters (per i cluster AKS) o connectedClusters (per i cluster K8S OnPrem).</span><span class="sxs-lookup"><span data-stu-id="b613d-151">`[ClusterResourceName <String>]`: The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="b613d-152">`[ClusterRp <String>]`: il cluster Kubernetes RP - Microsoft.ContainerService (per cluster AKS) o Microsoft.Kubernetes (per i cluster K8S OnPrem).</span><span class="sxs-lookup"><span data-stu-id="b613d-152">`[ClusterRp <String>]`: The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="b613d-153">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="b613d-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b613d-154">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b613d-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="b613d-155">`[SourceControlConfigurationName <String>]`: nome della configurazione del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="b613d-155">`[SourceControlConfigurationName <String>]`: Name of the Source Control Configuration.</span></span>
  - <span data-ttu-id="b613d-156">`[SubscriptionId <String>]`: l'ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="b613d-156">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="b613d-157">Stringa in formato GUID, ad esempio 00000000-0000-0000-0000-0000-00000000000000</span><span class="sxs-lookup"><span data-stu-id="b613d-157">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="b613d-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b613d-158">RELATED LINKS</span></span>

