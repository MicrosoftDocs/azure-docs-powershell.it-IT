---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/remove-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Remove-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Remove-AzKubernetesConfiguration.md
ms.openlocfilehash: 2a9547b88129a199f97bbcff9281348f9d2c4659
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189823"
---
# <span data-ttu-id="b522b-101">Remove-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="b522b-101">Remove-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="b522b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b522b-102">SYNOPSIS</span></span>
<span data-ttu-id="b522b-103">Questo eliminerà il file YAML usato per configurare la configurazione del controllo del codice sorgente, impedendo così la sincronizzazione futura dal repo di origine.</span><span class="sxs-lookup"><span data-stu-id="b522b-103">This will delete the YAML file used to set up the Source control configuration, thus stopping future sync from the source repo.</span></span>

## <span data-ttu-id="b522b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b522b-104">SYNTAX</span></span>

### <span data-ttu-id="b522b-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b522b-105">Delete (Default)</span></span>
```
Remove-AzKubernetesConfiguration -ClusterName <String> -ClusterType <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b522b-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b522b-106">DeleteViaIdentity</span></span>
```
Remove-AzKubernetesConfiguration -InputObject <IKubernetesConfigurationIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b522b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b522b-107">DESCRIPTION</span></span>
<span data-ttu-id="b522b-108">Questo eliminerà il file YAML usato per configurare la configurazione del controllo del codice sorgente, impedendo così la sincronizzazione futura dal repo di origine.</span><span class="sxs-lookup"><span data-stu-id="b522b-108">This will delete the YAML file used to set up the Source control configuration, thus stopping future sync from the source repo.</span></span>

## <span data-ttu-id="b522b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b522b-109">EXAMPLES</span></span>

### <span data-ttu-id="b522b-110">Esempio 1: rimuovere un configuation di kubernetes cluster per nome</span><span class="sxs-lookup"><span data-stu-id="b522b-110">Example 1: Remove a configuation of kubernetes cluster by name</span></span>
```powershell
PS C:\> Remove-AzKubernetesConfiguration -ClusterName connaks-d983yc -ClusterType ConnectedClusters -ResourceGroupName connaks-rg-w9vlnp -Name conf-test01

```

<span data-ttu-id="b522b-111">Questo comando rimuove un configuation di kubernetes cluster per nome.</span><span class="sxs-lookup"><span data-stu-id="b522b-111">This command removes a configuation of kubernetes cluster by name.</span></span>

### <span data-ttu-id="b522b-112">Esempio 2: rimuovere un configuation di kubernetes cluster per oggetto</span><span class="sxs-lookup"><span data-stu-id="b522b-112">Example 2: Remove a configuation of kubernetes cluster by object</span></span>
```powershell
PS C:\> $kubConf = Get-AzKubernetesConfiguration -ClusterName connaks-dkc29c -ClusterType ConnectedClusters -ResourceGroupName connaks-rg-w9vlnp -Name conf-test02 -ClusterRp Microsoft.Kubernetes
PS C:\> Remove-AzKubernetesConfiguration -InputObject $kubConf

```

<span data-ttu-id="b522b-113">Questo comando rimuove un configuation di kubernetes cluster per oggetto.</span><span class="sxs-lookup"><span data-stu-id="b522b-113">This command removes a configuation of kubernetes cluster by object.</span></span>

## <span data-ttu-id="b522b-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b522b-114">PARAMETERS</span></span>

### <span data-ttu-id="b522b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b522b-115">-AsJob</span></span>
<span data-ttu-id="b522b-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="b522b-116">Run the command as a job</span></span>

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

### <span data-ttu-id="b522b-117">-Clustername</span><span class="sxs-lookup"><span data-stu-id="b522b-117">-ClusterName</span></span>
<span data-ttu-id="b522b-118">Il nome del cluster kubernetes.</span><span class="sxs-lookup"><span data-stu-id="b522b-118">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="b522b-119">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="b522b-119">-ClusterType</span></span>
<span data-ttu-id="b522b-120">Il nome della risorsa del cluster Kubernetes-managedClusters (per i cluster AKS) o connectedClusters (per i cluster OnPrem K8S).</span><span class="sxs-lookup"><span data-stu-id="b522b-120">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="b522b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b522b-121">-DefaultProfile</span></span>
<span data-ttu-id="b522b-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b522b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b522b-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b522b-123">-InputObject</span></span>
<span data-ttu-id="b522b-124">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="b522b-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b522b-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="b522b-125">-Name</span></span>
<span data-ttu-id="b522b-126">Nome della configurazione del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="b522b-126">Name of the Source Control Configuration.</span></span>

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

### <span data-ttu-id="b522b-127">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="b522b-127">-NoWait</span></span>
<span data-ttu-id="b522b-128">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="b522b-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b522b-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b522b-129">-PassThru</span></span>
<span data-ttu-id="b522b-130">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="b522b-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b522b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b522b-131">-ResourceGroupName</span></span>
<span data-ttu-id="b522b-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b522b-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="b522b-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b522b-133">-SubscriptionId</span></span>
<span data-ttu-id="b522b-134">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="b522b-134">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="b522b-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b522b-135">-Confirm</span></span>
<span data-ttu-id="b522b-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b522b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b522b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b522b-137">-WhatIf</span></span>
<span data-ttu-id="b522b-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b522b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b522b-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b522b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b522b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b522b-140">CommonParameters</span></span>
<span data-ttu-id="b522b-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b522b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b522b-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b522b-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b522b-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b522b-143">INPUTS</span></span>

### <span data-ttu-id="b522b-144">Microsoft. Azure. PowerShell. Cmdlets. KubernetesConfiguration. Models. IKubernetesConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="b522b-144">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span></span>

## <span data-ttu-id="b522b-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b522b-145">OUTPUTS</span></span>

### <span data-ttu-id="b522b-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b522b-146">System.Boolean</span></span>

## <span data-ttu-id="b522b-147">Note</span><span class="sxs-lookup"><span data-stu-id="b522b-147">NOTES</span></span>

<span data-ttu-id="b522b-148">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b522b-148">ALIASES</span></span>

<span data-ttu-id="b522b-149">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b522b-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b522b-150">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="b522b-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b522b-151">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b522b-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b522b-152">INPUTOBJECT <IKubernetesConfigurationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="b522b-152">INPUTOBJECT <IKubernetesConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b522b-153">`[ClusterName <String>]`: Nome del cluster kubernetes.</span><span class="sxs-lookup"><span data-stu-id="b522b-153">`[ClusterName <String>]`: The name of the kubernetes cluster.</span></span>
  - <span data-ttu-id="b522b-154">`[ClusterResourceName <String>]`: Il nome della risorsa del cluster Kubernetes-managedClusters (per i cluster AKS) o connectedClusters (per i cluster OnPrem K8S).</span><span class="sxs-lookup"><span data-stu-id="b522b-154">`[ClusterResourceName <String>]`: The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="b522b-155">`[ClusterRp <String>]`: Il cluster Kubernetes RP-Microsoft. ContainerService (per i cluster AKS) o Microsoft. Kubernetes (per i cluster OnPrem K8S).</span><span class="sxs-lookup"><span data-stu-id="b522b-155">`[ClusterRp <String>]`: The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="b522b-156">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="b522b-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b522b-157">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b522b-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="b522b-158">`[SourceControlConfigurationName <String>]`: Nome della configurazione del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="b522b-158">`[SourceControlConfigurationName <String>]`: Name of the Source Control Configuration.</span></span>
  - <span data-ttu-id="b522b-159">`[SubscriptionId <String>]`: ID abbonamento Azure.</span><span class="sxs-lookup"><span data-stu-id="b522b-159">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="b522b-160">Si tratta di una stringa formattata con GUID (ad esempio 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="b522b-160">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="b522b-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b522b-161">RELATED LINKS</span></span>
