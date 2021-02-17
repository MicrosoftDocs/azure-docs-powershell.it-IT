---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/remove-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Remove-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Remove-AzKubernetesConfiguration.md
ms.openlocfilehash: 16b1e6f56cd5d324815dcf9453bc7f94e0de2480
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185326"
---
# <span data-ttu-id="63c19-101">Remove-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="63c19-101">Remove-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="63c19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63c19-102">SYNOPSIS</span></span>
<span data-ttu-id="63c19-103">In questo modo verrà eliminato il file YAML usato per configurare la configurazione del controllo del codice sorgente, interrompendo così la futura sincronizzazione dal repo di origine.</span><span class="sxs-lookup"><span data-stu-id="63c19-103">This will delete the YAML file used to set up the Source control configuration, thus stopping future sync from the source repo.</span></span>

## <span data-ttu-id="63c19-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="63c19-104">SYNTAX</span></span>

### <span data-ttu-id="63c19-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="63c19-105">Delete (Default)</span></span>
```
Remove-AzKubernetesConfiguration -ClusterName <String> -ClusterType <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="63c19-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="63c19-106">DeleteViaIdentity</span></span>
```
Remove-AzKubernetesConfiguration -InputObject <IKubernetesConfigurationIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="63c19-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="63c19-107">DESCRIPTION</span></span>
<span data-ttu-id="63c19-108">In questo modo verrà eliminato il file YAML usato per configurare la configurazione del controllo del codice sorgente, interrompendo così la futura sincronizzazione dal repo di origine.</span><span class="sxs-lookup"><span data-stu-id="63c19-108">This will delete the YAML file used to set up the Source control configuration, thus stopping future sync from the source repo.</span></span>

## <span data-ttu-id="63c19-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="63c19-109">EXAMPLES</span></span>

### <span data-ttu-id="63c19-110">Esempio 1: Rimuovere la configurazione di un cluster kubernetes in base al nome</span><span class="sxs-lookup"><span data-stu-id="63c19-110">Example 1: Remove a configuation of kubernetes cluster by name</span></span>
```powershell
PS C:\> Remove-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -Name  k8sconfig-t02 -ClusterType ConnectedClusters

```

<span data-ttu-id="63c19-111">Questo comando rimuove una configurazione del cluster kubernetes in base al nome.</span><span class="sxs-lookup"><span data-stu-id="63c19-111">This command removes a configuation of kubernetes cluster by name.</span></span>

### <span data-ttu-id="63c19-112">Esempio 2: Rimuovere una configurazione di kubernetes raggruppate per oggetto</span><span class="sxs-lookup"><span data-stu-id="63c19-112">Example 2: Remove a configuation of kubernetes cluster by object</span></span>
```powershell
PS C:\> $kubConf = Get-AzKubernetesConfiguration -ClusterName connaks-dkc29c -ClusterType ConnectedClusters -ResourceGroupName connaks-rg-w9vlnp -Name conf-test02 -ClusterRp Microsoft.Kubernetes
PS C:\> Remove-AzKubernetesConfiguration -InputObject $kubConf

```

<span data-ttu-id="63c19-113">Questo comando rimuove una configurazione di kubernetes raggruppati per oggetto.</span><span class="sxs-lookup"><span data-stu-id="63c19-113">This command removes a configuation of kubernetes cluster by object.</span></span>

## <span data-ttu-id="63c19-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="63c19-114">PARAMETERS</span></span>

### <span data-ttu-id="63c19-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="63c19-115">-AsJob</span></span>
<span data-ttu-id="63c19-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="63c19-116">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63c19-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="63c19-117">-ClusterName</span></span>
<span data-ttu-id="63c19-118">Il nome del cluster kubernetes.</span><span class="sxs-lookup"><span data-stu-id="63c19-118">The name of the kubernetes cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63c19-119">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="63c19-119">-ClusterType</span></span>
<span data-ttu-id="63c19-120">Nome della risorsa cluster Kubernetes: managedClusters (per i cluster AKS) o connectedClusters (per i cluster K8S OnPrem).</span><span class="sxs-lookup"><span data-stu-id="63c19-120">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63c19-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63c19-121">-DefaultProfile</span></span>
<span data-ttu-id="63c19-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="63c19-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63c19-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63c19-123">-InputObject</span></span>
<span data-ttu-id="63c19-124">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="63c19-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63c19-125">-Name</span><span class="sxs-lookup"><span data-stu-id="63c19-125">-Name</span></span>
<span data-ttu-id="63c19-126">Nome della configurazione del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="63c19-126">Name of the Source Control Configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SourceControlConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63c19-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="63c19-127">-NoWait</span></span>
<span data-ttu-id="63c19-128">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="63c19-128">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63c19-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="63c19-129">-PassThru</span></span>
<span data-ttu-id="63c19-130">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="63c19-130">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63c19-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63c19-131">-ResourceGroupName</span></span>
<span data-ttu-id="63c19-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="63c19-132">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63c19-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="63c19-133">-SubscriptionId</span></span>
<span data-ttu-id="63c19-134">ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="63c19-134">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63c19-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="63c19-135">-Confirm</span></span>
<span data-ttu-id="63c19-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63c19-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63c19-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63c19-137">-WhatIf</span></span>
<span data-ttu-id="63c19-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="63c19-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63c19-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="63c19-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63c19-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63c19-140">CommonParameters</span></span>
<span data-ttu-id="63c19-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63c19-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63c19-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="63c19-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63c19-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="63c19-143">INPUTS</span></span>

### <span data-ttu-id="63c19-144">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="63c19-144">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span></span>

## <span data-ttu-id="63c19-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="63c19-145">OUTPUTS</span></span>

### <span data-ttu-id="63c19-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="63c19-146">System.Boolean</span></span>

## <span data-ttu-id="63c19-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="63c19-147">NOTES</span></span>

<span data-ttu-id="63c19-148">ALIAS</span><span class="sxs-lookup"><span data-stu-id="63c19-148">ALIASES</span></span>

<span data-ttu-id="63c19-149">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="63c19-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="63c19-150">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="63c19-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="63c19-151">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="63c19-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="63c19-152">INPUTOBJECT <IKubernetesConfigurationIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="63c19-152">INPUTOBJECT <IKubernetesConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="63c19-153">`[ClusterName <String>]`: il nome del cluster kubernetes.</span><span class="sxs-lookup"><span data-stu-id="63c19-153">`[ClusterName <String>]`: The name of the kubernetes cluster.</span></span>
  - <span data-ttu-id="63c19-154">`[ClusterResourceName <String>]`: il nome della risorsa cluster Kubernetes - managedClusters (per i cluster AKS) o connectedClusters (per i cluster K8S OnPrem).</span><span class="sxs-lookup"><span data-stu-id="63c19-154">`[ClusterResourceName <String>]`: The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="63c19-155">`[ClusterRp <String>]`: il cluster Kubernetes RP - Microsoft.ContainerService (per cluster AKS) o Microsoft.Kubernetes (per i cluster K8S OnPrem).</span><span class="sxs-lookup"><span data-stu-id="63c19-155">`[ClusterRp <String>]`: The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="63c19-156">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="63c19-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="63c19-157">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="63c19-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="63c19-158">`[SourceControlConfigurationName <String>]`: nome della configurazione del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="63c19-158">`[SourceControlConfigurationName <String>]`: Name of the Source Control Configuration.</span></span>
  - <span data-ttu-id="63c19-159">`[SubscriptionId <String>]`: l'ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="63c19-159">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="63c19-160">Stringa in formato GUID, ad esempio 00000000-0000-0000-0000-0000-00000000000000</span><span class="sxs-lookup"><span data-stu-id="63c19-160">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="63c19-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="63c19-161">RELATED LINKS</span></span>

