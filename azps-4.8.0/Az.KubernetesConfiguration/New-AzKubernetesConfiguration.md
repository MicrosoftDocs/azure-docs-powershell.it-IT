---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/new-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
ms.openlocfilehash: 70ff3c636f6c88ac89e53a5c2b1acb209aad274a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189816"
---
# <span data-ttu-id="a5a86-101">New-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5a86-101">New-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="a5a86-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a5a86-102">SYNOPSIS</span></span>
<span data-ttu-id="a5a86-103">Creare una nuova configurazione del controllo del codice sorgente Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="a5a86-103">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="a5a86-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a5a86-104">SYNTAX</span></span>

```
New-AzKubernetesConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 -RepositoryUrl <String> [-ClusterType <String>] [-SubscriptionId <String>] [-ClusterScoped]
 [-EnableHelmOperator] [-HelmOperatorChartValues <String>] [-HelmOperatorChartVersion <String>]
 [-OperatorInstanceName <String>] [-OperatorNamespace <String>] [-OperatorParameters <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a5a86-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a5a86-105">DESCRIPTION</span></span>
<span data-ttu-id="a5a86-106">Creare una nuova configurazione del controllo del codice sorgente Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="a5a86-106">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="a5a86-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a5a86-107">EXAMPLES</span></span>

### <span data-ttu-id="a5a86-108">Esempio 1: creare un configuation per kubernetes cluster</span><span class="sxs-lookup"><span data-stu-id="a5a86-108">Example 1: Create a configuation for kubernetes cluster</span></span>
```powershell
PS C:\> New-AzKubernetesConfiguration -Name conf-test01 -ClusterName connaks-d983yc -ResourceGroupName connaks-rg-w9vlnp -RepositoryUrl http://github.com/xxxx

Name        Type
----        ----
conf-test01 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="a5a86-109">Questo comando crea un configuation per il cluster kubernetes.</span><span class="sxs-lookup"><span data-stu-id="a5a86-109">This command creates a configuation for kubernetes cluster.</span></span>

## <span data-ttu-id="a5a86-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a5a86-110">PARAMETERS</span></span>

### <span data-ttu-id="a5a86-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="a5a86-111">-ClusterName</span></span>
<span data-ttu-id="a5a86-112">Il nome del cluster kubernetes.</span><span class="sxs-lookup"><span data-stu-id="a5a86-112">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="a5a86-113">-ClusterScoped</span><span class="sxs-lookup"><span data-stu-id="a5a86-113">-ClusterScoped</span></span>
<span data-ttu-id="a5a86-114">Se passato imposta l'ambito della configurazione su cluster (il valore predefinito è nameSpace).</span><span class="sxs-lookup"><span data-stu-id="a5a86-114">If passed set the scope of the Configuration to Cluster (default is nameSpace).</span></span>

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

### <span data-ttu-id="a5a86-115">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="a5a86-115">-ClusterType</span></span>
<span data-ttu-id="a5a86-116">Il nome della risorsa del cluster Kubernetes-managedClusters (per i cluster AKS) o connectedClusters (per i cluster OnPrem K8S).</span><span class="sxs-lookup"><span data-stu-id="a5a86-116">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="a5a86-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5a86-117">-DefaultProfile</span></span>
<span data-ttu-id="a5a86-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a5a86-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5a86-119">-EnableHelmOperator</span><span class="sxs-lookup"><span data-stu-id="a5a86-119">-EnableHelmOperator</span></span>
<span data-ttu-id="a5a86-120">Opzione per abilitare l'operatore Helm per questa configurazione git.</span><span class="sxs-lookup"><span data-stu-id="a5a86-120">Option to enable Helm Operator for this git configuration.</span></span>

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

### <span data-ttu-id="a5a86-121">-HelmOperatorChartValues</span><span class="sxs-lookup"><span data-stu-id="a5a86-121">-HelmOperatorChartValues</span></span>
<span data-ttu-id="a5a86-122">Override dei valori per il grafico Helm dell'operatore.</span><span class="sxs-lookup"><span data-stu-id="a5a86-122">Values override for the operator Helm chart.</span></span>

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

### <span data-ttu-id="a5a86-123">-HelmOperatorChartVersion</span><span class="sxs-lookup"><span data-stu-id="a5a86-123">-HelmOperatorChartVersion</span></span>
<span data-ttu-id="a5a86-124">Versione del grafico timone operatore.</span><span class="sxs-lookup"><span data-stu-id="a5a86-124">Version of the operator Helm chart.</span></span>

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

### <span data-ttu-id="a5a86-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="a5a86-125">-Name</span></span>
<span data-ttu-id="a5a86-126">Nome della configurazione del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="a5a86-126">Name of the Source Control Configuration.</span></span>

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

### <span data-ttu-id="a5a86-127">-OperatorInstanceName</span><span class="sxs-lookup"><span data-stu-id="a5a86-127">-OperatorInstanceName</span></span>
<span data-ttu-id="a5a86-128">Nome dell'istanza dell'operatore che identifica la configurazione specifica.</span><span class="sxs-lookup"><span data-stu-id="a5a86-128">Instance name of the operator - identifying the specific configuration.</span></span>

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

### <span data-ttu-id="a5a86-129">-OperatorNamespace</span><span class="sxs-lookup"><span data-stu-id="a5a86-129">-OperatorNamespace</span></span>
<span data-ttu-id="a5a86-130">Lo spazio dei nomi a cui è installato l'operatore.</span><span class="sxs-lookup"><span data-stu-id="a5a86-130">The namespace to which this operator is installed to.</span></span>
<span data-ttu-id="a5a86-131">Massimo di 253 caratteri alfanumerici, segno meno e punto solo.</span><span class="sxs-lookup"><span data-stu-id="a5a86-131">Maximum of 253 lower case alphanumeric characters, hyphen and period only.</span></span>

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

### <span data-ttu-id="a5a86-132">-OperatorParameters</span><span class="sxs-lookup"><span data-stu-id="a5a86-132">-OperatorParameters</span></span>
<span data-ttu-id="a5a86-133">Tutti i parametri per l'istanza dell'operatore in formato stringa.</span><span class="sxs-lookup"><span data-stu-id="a5a86-133">Any Parameters for the Operator instance in string format.</span></span>

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

### <span data-ttu-id="a5a86-134">-RepositoryUrl</span><span class="sxs-lookup"><span data-stu-id="a5a86-134">-RepositoryUrl</span></span>
<span data-ttu-id="a5a86-135">URL del repository SourceControl.</span><span class="sxs-lookup"><span data-stu-id="a5a86-135">Url of the SourceControl Repository.</span></span>

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

### <span data-ttu-id="a5a86-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5a86-136">-ResourceGroupName</span></span>
<span data-ttu-id="a5a86-137">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a5a86-137">The name of the resource group.</span></span>

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

### <span data-ttu-id="a5a86-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a5a86-138">-SubscriptionId</span></span>
<span data-ttu-id="a5a86-139">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="a5a86-139">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="a5a86-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a5a86-140">-Confirm</span></span>
<span data-ttu-id="a5a86-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5a86-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5a86-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5a86-142">-WhatIf</span></span>
<span data-ttu-id="a5a86-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a5a86-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5a86-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a5a86-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5a86-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5a86-145">CommonParameters</span></span>
<span data-ttu-id="a5a86-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5a86-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5a86-147">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5a86-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5a86-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a5a86-148">INPUTS</span></span>

## <span data-ttu-id="a5a86-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a5a86-149">OUTPUTS</span></span>

### <span data-ttu-id="a5a86-150">Microsoft. Azure. PowerShell. Cmdlets. KubernetesConfiguration. Models. Api20191101Preview. ISourceControlConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5a86-150">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20191101Preview.ISourceControlConfiguration</span></span>

## <span data-ttu-id="a5a86-151">Note</span><span class="sxs-lookup"><span data-stu-id="a5a86-151">NOTES</span></span>

<span data-ttu-id="a5a86-152">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a5a86-152">ALIASES</span></span>

## <span data-ttu-id="a5a86-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a5a86-153">RELATED LINKS</span></span>
