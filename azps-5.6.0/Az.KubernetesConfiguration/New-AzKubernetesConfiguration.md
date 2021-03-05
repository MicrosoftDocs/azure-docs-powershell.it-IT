---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/powershell/module/az.kubernetesconfiguration/new-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
ms.openlocfilehash: 0040ab3bc037527400ea1f3eabf3c887189fc73c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976829"
---
# <span data-ttu-id="8b820-101">New-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="8b820-101">New-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="8b820-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b820-102">SYNOPSIS</span></span>
<span data-ttu-id="8b820-103">Creare una nuova configurazione del controllo del controllo del codice sorgente di Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="8b820-103">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="8b820-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8b820-104">SYNTAX</span></span>

```
New-AzKubernetesConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 -RepositoryUrl <String> [-ClusterType <String>] [-SubscriptionId <String>] [-ClusterScoped]
 [-EnableHelmOperator] [-HelmOperatorChartValues <String>] [-HelmOperatorChartVersion <String>]
 [-OperatorInstanceName <String>] [-OperatorNamespace <String>] [-OperatorParameters <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8b820-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8b820-105">DESCRIPTION</span></span>
<span data-ttu-id="8b820-106">Creare una nuova configurazione del controllo del controllo del codice sorgente di Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="8b820-106">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="8b820-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8b820-107">EXAMPLES</span></span>

### <span data-ttu-id="8b820-108">Esempio 1: Creare una configurazione per il cluster kubernetes</span><span class="sxs-lookup"><span data-stu-id="8b820-108">Example 1: Create a configuration for kubernetes cluster</span></span>
```powershell
PS C:\> New-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -Name k8sconfig-t01 -RepositoryUrl http://github.com/xxxx

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t01 12/21/2020 5:26:17 AM                                             12/21/2020 5:26:17 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="8b820-109">Questo comando crea una configurazione per il cluster kubernetes.</span><span class="sxs-lookup"><span data-stu-id="8b820-109">This command creates a configuration for kubernetes cluster.</span></span>

### <span data-ttu-id="8b820-110">Esempio 1: Creare una configurazione per il cluster kubernetes con specify paramter OperatorParamTer</span><span class="sxs-lookup"><span data-stu-id="8b820-110">Example 1: Create a configuration for kubernetes cluster with specify paramter OperatorNamespace</span></span>
```powershell
PS C:\> New-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -Name k8sconfig-t02 -RepositoryUrl http://github.com/xxxx -OperatorNamespace namespace-t01

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:26:17 AM                                             12/21/2020 5:26:17 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="8b820-111">Questo comando crea una configurazione nel nuovo spazio dei nomi dell'operatore per il cluster kubernetes.</span><span class="sxs-lookup"><span data-stu-id="8b820-111">This command creates a configuration in the new operator namespace for kubernetes cluster.</span></span>
<span data-ttu-id="8b820-112">Nota: Non è possibile creare una configurazione in uno spazio dei nomi operatore esistente.</span><span class="sxs-lookup"><span data-stu-id="8b820-112">Note, Unable to create a configuration in an existing operator namespace.</span></span>

## <span data-ttu-id="8b820-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b820-113">PARAMETERS</span></span>

### <span data-ttu-id="8b820-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="8b820-114">-ClusterName</span></span>
<span data-ttu-id="8b820-115">Il nome del cluster kubernetes.</span><span class="sxs-lookup"><span data-stu-id="8b820-115">The name of the kubernetes cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b820-116">-ClusterScoped</span><span class="sxs-lookup"><span data-stu-id="8b820-116">-ClusterScoped</span></span>
<span data-ttu-id="8b820-117">Se l'ambito della configurazione è stato superato, viene impostato su Cluster (l'impostazione predefinita è nameSpace).</span><span class="sxs-lookup"><span data-stu-id="8b820-117">If passed set the scope of the Configuration to Cluster (default is nameSpace).</span></span>

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

### <span data-ttu-id="8b820-118">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="8b820-118">-ClusterType</span></span>
<span data-ttu-id="8b820-119">Nome della risorsa cluster Kubernetes: managedClusters (per i cluster AKS) o connectedClusters (per i cluster K8S OnPrem).</span><span class="sxs-lookup"><span data-stu-id="8b820-119">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b820-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b820-120">-DefaultProfile</span></span>
<span data-ttu-id="8b820-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8b820-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b820-122">-EnableHelmOperator</span><span class="sxs-lookup"><span data-stu-id="8b820-122">-EnableHelmOperator</span></span>
<span data-ttu-id="8b820-123">Opzione per abilitare Operatore operatore operatore per questa configurazione git.</span><span class="sxs-lookup"><span data-stu-id="8b820-123">Option to enable Helm Operator for this git configuration.</span></span>

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

### <span data-ttu-id="8b820-124">-IntasatoOperatorChartValues</span><span class="sxs-lookup"><span data-stu-id="8b820-124">-HelmOperatorChartValues</span></span>
<span data-ttu-id="8b820-125">I valori vengono sovrascritti per il grafico a due operatore.</span><span class="sxs-lookup"><span data-stu-id="8b820-125">Values override for the operator Helm chart.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b820-126">-Una versione di Office 365 che mostra una versione di Office 365</span><span class="sxs-lookup"><span data-stu-id="8b820-126">-HelmOperatorChartVersion</span></span>
<span data-ttu-id="8b820-127">Versione del grafico a barre dell'operatore.</span><span class="sxs-lookup"><span data-stu-id="8b820-127">Version of the operator Helm chart.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b820-128">-Name</span><span class="sxs-lookup"><span data-stu-id="8b820-128">-Name</span></span>
<span data-ttu-id="8b820-129">Nome della configurazione del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="8b820-129">Name of the Source Control Configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourceControlConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b820-130">-OperatorInstanceName</span><span class="sxs-lookup"><span data-stu-id="8b820-130">-OperatorInstanceName</span></span>
<span data-ttu-id="8b820-131">Nome dell'istanza dell'operatore, che identifica la configurazione specifica.</span><span class="sxs-lookup"><span data-stu-id="8b820-131">Instance name of the operator - identifying the specific configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b820-132">-OperatorEnne</span><span class="sxs-lookup"><span data-stu-id="8b820-132">-OperatorNamespace</span></span>
<span data-ttu-id="8b820-133">Spazio dei nomi in cui è installato l'operatore.</span><span class="sxs-lookup"><span data-stu-id="8b820-133">The namespace to which this operator is installed to.</span></span>
<span data-ttu-id="8b820-134">Massimo 253 caratteri alfanumerici minuscoli, trattino e punto.</span><span class="sxs-lookup"><span data-stu-id="8b820-134">Maximum of 253 lower case alphanumeric characters, hyphen and period only.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b820-135">-OperatorParameters</span><span class="sxs-lookup"><span data-stu-id="8b820-135">-OperatorParameters</span></span>
<span data-ttu-id="8b820-136">Qualsiasi parametro per l'istanza operatore in formato stringa.</span><span class="sxs-lookup"><span data-stu-id="8b820-136">Any Parameters for the Operator instance in string format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b820-137">-RepositoryUrl</span><span class="sxs-lookup"><span data-stu-id="8b820-137">-RepositoryUrl</span></span>
<span data-ttu-id="8b820-138">URL del repository SourceControl.</span><span class="sxs-lookup"><span data-stu-id="8b820-138">Url of the SourceControl Repository.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b820-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b820-139">-ResourceGroupName</span></span>
<span data-ttu-id="8b820-140">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8b820-140">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b820-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8b820-141">-SubscriptionId</span></span>
<span data-ttu-id="8b820-142">ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="8b820-142">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b820-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8b820-143">-Confirm</span></span>
<span data-ttu-id="8b820-144">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b820-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b820-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b820-145">-WhatIf</span></span>
<span data-ttu-id="8b820-146">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8b820-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b820-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8b820-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b820-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b820-148">CommonParameters</span></span>
<span data-ttu-id="8b820-149">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b820-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b820-150">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8b820-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b820-151">INPUT</span><span class="sxs-lookup"><span data-stu-id="8b820-151">INPUTS</span></span>

## <span data-ttu-id="8b820-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8b820-152">OUTPUTS</span></span>

### <span data-ttu-id="8b820-153">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20210301.ISourceControlConfiguration</span><span class="sxs-lookup"><span data-stu-id="8b820-153">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20210301.ISourceControlConfiguration</span></span>

## <span data-ttu-id="8b820-154">NOTE</span><span class="sxs-lookup"><span data-stu-id="8b820-154">NOTES</span></span>

<span data-ttu-id="8b820-155">ALIAS</span><span class="sxs-lookup"><span data-stu-id="8b820-155">ALIASES</span></span>

## <span data-ttu-id="8b820-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8b820-156">RELATED LINKS</span></span>

