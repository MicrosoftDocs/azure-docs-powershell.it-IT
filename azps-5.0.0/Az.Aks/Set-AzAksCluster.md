---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/set-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAksCluster.md
ms.openlocfilehash: 0df5c0d9975acc048ba5842543ec2c4d522567c8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200565"
---
# <span data-ttu-id="3c6b3-101">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="3c6b3-101">Set-AzAksCluster</span></span>

## <span data-ttu-id="3c6b3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3c6b3-102">SYNOPSIS</span></span>
<span data-ttu-id="3c6b3-103">Aggiornare o creare un cluster Kubernetes gestito.</span><span class="sxs-lookup"><span data-stu-id="3c6b3-103">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="3c6b3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3c6b3-104">SYNTAX</span></span>

### <span data-ttu-id="3c6b3-105">defaultParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3c6b3-105">defaultParameterSet (Default)</span></span>
```
Set-AzAksCluster [-NodePoolMode <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-ServicePrincipalIdAndSecret] <PSCredential>] [-Location <String>] [-LinuxProfileAdminUserName <String>]
 [-DnsNamePrefix <String>] [-KubernetesVersion <String>] [-NodeName <String>] [-NodeMinCount <Int32>]
 [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>]
 [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c6b3-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c6b3-106">InputObjectParameterSet</span></span>
```
Set-AzAksCluster -InputObject <PSKubernetesCluster> [-NodePoolMode <String>] [-Location <String>]
 [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c6b3-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c6b3-107">IdParameterSet</span></span>
```
Set-AzAksCluster [-NodePoolMode <String>] [-Id] <String> [-Location <String>]
 [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c6b3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c6b3-108">DESCRIPTION</span></span>
<span data-ttu-id="3c6b3-109">Aggiornare o creare un cluster Kubernetes gestito.</span><span class="sxs-lookup"><span data-stu-id="3c6b3-109">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="3c6b3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3c6b3-110">EXAMPLES</span></span>

### <span data-ttu-id="3c6b3-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3c6b3-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Set-AzAks -NodeCount 5
```

<span data-ttu-id="3c6b3-112">Impostare il numero di nodi nel cluster Kubernetes su 5.</span><span class="sxs-lookup"><span data-stu-id="3c6b3-112">Set the number of nodes in the Kubernetes cluster to 5.</span></span>

## <span data-ttu-id="3c6b3-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3c6b3-113">PARAMETERS</span></span>

### <span data-ttu-id="3c6b3-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c6b3-114">-AsJob</span></span>
<span data-ttu-id="3c6b3-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="3c6b3-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3c6b3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c6b3-116">-DefaultProfile</span></span>
<span data-ttu-id="3c6b3-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3c6b3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c6b3-118">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="3c6b3-118">-DnsNamePrefix</span></span>
<span data-ttu-id="3c6b3-119">Prefisso del nome DNS per il cluster.</span><span class="sxs-lookup"><span data-stu-id="3c6b3-119">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="3c6b3-120">-EnableNodeAutoScaling</span><span class="sxs-lookup"><span data-stu-id="3c6b3-120">-EnableNodeAutoScaling</span></span>
<span data-ttu-id="3c6b3-121">Se abilitare il ridimensionamento automatico</span><span class="sxs-lookup"><span data-stu-id="3c6b3-121">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="3c6b3-122">-ID</span><span class="sxs-lookup"><span data-stu-id="3c6b3-122">-Id</span></span>
<span data-ttu-id="3c6b3-123">ID di un cluster Kubernetes gestito</span><span class="sxs-lookup"><span data-stu-id="3c6b3-123">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c6b3-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c6b3-124">-InputObject</span></span>
<span data-ttu-id="3c6b3-125">Un oggetto PSKubernetesCluster, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="3c6b3-125">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c6b3-126">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="3c6b3-126">-KubernetesVersion</span></span>
<span data-ttu-id="3c6b3-127">La versione di Kubernetes da usare per creare il cluster.</span><span class="sxs-lookup"><span data-stu-id="3c6b3-127">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="3c6b3-128">-LinuxProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="3c6b3-128">-LinuxProfileAdminUserName</span></span>
<span data-ttu-id="3c6b3-129">Nome utente per le macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="3c6b3-129">User name for the Linux Virtual Machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AdminUserName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c6b3-130">-Posizione</span><span class="sxs-lookup"><span data-stu-id="3c6b3-130">-Location</span></span>
<span data-ttu-id="3c6b3-131">Posizione di Azure per il cluster.</span><span class="sxs-lookup"><span data-stu-id="3c6b3-131">Azure location for the cluster.</span></span>
<span data-ttu-id="3c6b3-132">Il valore predefinito è la posizione del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3c6b3-132">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="3c6b3-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="3c6b3-133">-Name</span></span>
<span data-ttu-id="3c6b3-134">Nome del cluster gestito Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="3c6b3-134">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c6b3-135">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="3c6b3-135">-NodeCount</span></span>
<span data-ttu-id="3c6b3-136">Numero predefinito di nodi per i pool di nodi.</span><span class="sxs-lookup"><span data-stu-id="3c6b3-136">The default number of nodes for the node pools.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c6b3-137">-NodeMaxCount</span><span class="sxs-lookup"><span data-stu-id="3c6b3-137">-NodeMaxCount</span></span>
<span data-ttu-id="3c6b3-138">Numero massimo di nodi per il ridimensionamento automatico</span><span class="sxs-lookup"><span data-stu-id="3c6b3-138">Maximum number of nodes for auto-scaling</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c6b3-139">-NodeMinCount</span><span class="sxs-lookup"><span data-stu-id="3c6b3-139">-NodeMinCount</span></span>
<span data-ttu-id="3c6b3-140">Numero minimo di nodi per il ridimensionamento automatico.</span><span class="sxs-lookup"><span data-stu-id="3c6b3-140">Minimum number of nodes for auto-scaling.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c6b3-141">-NodeName</span><span class="sxs-lookup"><span data-stu-id="3c6b3-141">-NodeName</span></span>
<span data-ttu-id="3c6b3-142">Nome univoco del profilo del pool di agenti nel contesto del gruppo sottoscrizioni e risorse.</span><span class="sxs-lookup"><span data-stu-id="3c6b3-142">Unique name of the agent pool profile in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="3c6b3-143">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="3c6b3-143">-NodeOsDiskSize</span></span>
<span data-ttu-id="3c6b3-144">Numero predefinito di nodi per i pool di nodi.</span><span class="sxs-lookup"><span data-stu-id="3c6b3-144">The default number of nodes for the node pools.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c6b3-145">-NodePoolMode</span><span class="sxs-lookup"><span data-stu-id="3c6b3-145">-NodePoolMode</span></span>
<span data-ttu-id="3c6b3-146">NodePoolMode rappresenta la modalità di un pool di nodi.</span><span class="sxs-lookup"><span data-stu-id="3c6b3-146">NodePoolMode represents mode of an node pool.</span></span>

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

### <span data-ttu-id="3c6b3-147">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="3c6b3-147">-NodeVmSize</span></span>
<span data-ttu-id="3c6b3-148">Le dimensioni della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3c6b3-148">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="3c6b3-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c6b3-149">-ResourceGroupName</span></span>
<span data-ttu-id="3c6b3-150">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3c6b3-150">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c6b3-151">-ServicePrincipalIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="3c6b3-151">-ServicePrincipalIdAndSecret</span></span>
<span data-ttu-id="3c6b3-152">ID client e segreto client associato all'entità dell'applicazione/servizio AAD.</span><span class="sxs-lookup"><span data-stu-id="3c6b3-152">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: defaultParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c6b3-153">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="3c6b3-153">-SshKeyValue</span></span>
<span data-ttu-id="3c6b3-154">Valore del file di chiave SSH o percorso file chiave.</span><span class="sxs-lookup"><span data-stu-id="3c6b3-154">SSH key file value or key file path.</span></span>
<span data-ttu-id="3c6b3-155">Il valore predefinito è {HOME}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="3c6b3-155">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SshKeyPath

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c6b3-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="3c6b3-156">-Tag</span></span>
<span data-ttu-id="3c6b3-157">Tag da applicare alla risorsa</span><span class="sxs-lookup"><span data-stu-id="3c6b3-157">Tags to be applied to the resource</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c6b3-158">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3c6b3-158">-Confirm</span></span>
<span data-ttu-id="3c6b3-159">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c6b3-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c6b3-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c6b3-160">-WhatIf</span></span>
<span data-ttu-id="3c6b3-161">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3c6b3-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c6b3-162">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3c6b3-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c6b3-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c6b3-163">CommonParameters</span></span>
<span data-ttu-id="3c6b3-164">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c6b3-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c6b3-165">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3c6b3-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c6b3-166">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3c6b3-166">INPUTS</span></span>

### <span data-ttu-id="3c6b3-167">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="3c6b3-167">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="3c6b3-168">System. String</span><span class="sxs-lookup"><span data-stu-id="3c6b3-168">System.String</span></span>

## <span data-ttu-id="3c6b3-169">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3c6b3-169">OUTPUTS</span></span>

### <span data-ttu-id="3c6b3-170">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="3c6b3-170">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="3c6b3-171">Note</span><span class="sxs-lookup"><span data-stu-id="3c6b3-171">NOTES</span></span>

## <span data-ttu-id="3c6b3-172">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3c6b3-172">RELATED LINKS</span></span>
