---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/set-azaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAks.md
ms.openlocfilehash: 9b63ede0bbd24adb98159ca6cfee08238b26aabc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676158"
---
# <span data-ttu-id="59871-101">Set-AzAks</span><span class="sxs-lookup"><span data-stu-id="59871-101">Set-AzAks</span></span>

## <span data-ttu-id="59871-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="59871-102">SYNOPSIS</span></span>
<span data-ttu-id="59871-103">Aggiornare o creare un cluster Kubernetes gestito.</span><span class="sxs-lookup"><span data-stu-id="59871-103">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="59871-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="59871-104">SYNTAX</span></span>

### <span data-ttu-id="59871-105">defaultParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="59871-105">defaultParameterSet (Default)</span></span>
```
Set-AzAks [-ResourceGroupName] <String> [-Name] <String> [[-ClientIdAndSecret] <PSCredential>]
 [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59871-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="59871-106">InputObjectParameterSet</span></span>
```
Set-AzAks -InputObject <PSKubernetesCluster> [-Location <String>] [-AdminUserName <String>]
 [-DnsNamePrefix <String>] [-KubernetesVersion <String>] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>]
 [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59871-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="59871-107">IdParameterSet</span></span>
```
Set-AzAks [-Id] <String> [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>]
 [-KubernetesVersion <String>] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>]
 [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59871-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59871-108">DESCRIPTION</span></span>
<span data-ttu-id="59871-109">Aggiornare o creare un cluster Kubernetes gestito.</span><span class="sxs-lookup"><span data-stu-id="59871-109">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="59871-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="59871-110">EXAMPLES</span></span>

### <span data-ttu-id="59871-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="59871-111">Example 1</span></span>
```
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Set-AzAks -NodeCount 5
```

<span data-ttu-id="59871-112">Impostare il numero di nodi nel cluster Kubernetes su 5.</span><span class="sxs-lookup"><span data-stu-id="59871-112">Set the number of nodes in the Kubernetes cluster to 5.</span></span>

## <span data-ttu-id="59871-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="59871-113">PARAMETERS</span></span>

### <span data-ttu-id="59871-114">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="59871-114">-AdminUserName</span></span>
<span data-ttu-id="59871-115">Nome utente per le macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="59871-115">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="59871-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="59871-116">-AsJob</span></span>
<span data-ttu-id="59871-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="59871-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="59871-118">-ClientIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="59871-118">-ClientIdAndSecret</span></span>
<span data-ttu-id="59871-119">ID client e segreto client associato all'entità dell'applicazione/servizio AAD.</span><span class="sxs-lookup"><span data-stu-id="59871-119">The client id and client secret associated with the AAD application / service principal.</span></span>

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

### <span data-ttu-id="59871-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59871-120">-DefaultProfile</span></span>
<span data-ttu-id="59871-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="59871-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59871-122">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="59871-122">-DnsNamePrefix</span></span>
<span data-ttu-id="59871-123">Prefisso del nome DNS per il cluster.</span><span class="sxs-lookup"><span data-stu-id="59871-123">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="59871-124">-ID</span><span class="sxs-lookup"><span data-stu-id="59871-124">-Id</span></span>
<span data-ttu-id="59871-125">ID di un cluster Kubernetes gestito</span><span class="sxs-lookup"><span data-stu-id="59871-125">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="59871-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59871-126">-InputObject</span></span>
<span data-ttu-id="59871-127">Un oggetto PSKubernetesCluster, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="59871-127">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="59871-128">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="59871-128">-KubernetesVersion</span></span>
<span data-ttu-id="59871-129">La versione di Kubernetes da usare per creare il cluster.</span><span class="sxs-lookup"><span data-stu-id="59871-129">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="59871-130">-Posizione</span><span class="sxs-lookup"><span data-stu-id="59871-130">-Location</span></span>
<span data-ttu-id="59871-131">Posizione di Azure per il cluster.</span><span class="sxs-lookup"><span data-stu-id="59871-131">Azure location for the cluster.</span></span>
<span data-ttu-id="59871-132">Il valore predefinito è la posizione del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="59871-132">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="59871-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="59871-133">-Name</span></span>
<span data-ttu-id="59871-134">Nome del cluster gestito Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="59871-134">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="59871-135">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="59871-135">-NodeCount</span></span>
<span data-ttu-id="59871-136">Numero predefinito di nodi per i pool di nodi.</span><span class="sxs-lookup"><span data-stu-id="59871-136">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="59871-137">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="59871-137">-NodeOsDiskSize</span></span>
<span data-ttu-id="59871-138">Numero predefinito di nodi per i pool di nodi.</span><span class="sxs-lookup"><span data-stu-id="59871-138">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="59871-139">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="59871-139">-NodeVmSize</span></span>
<span data-ttu-id="59871-140">Le dimensioni della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="59871-140">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="59871-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59871-141">-ResourceGroupName</span></span>
<span data-ttu-id="59871-142">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="59871-142">Resource Group Name.</span></span>

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

### <span data-ttu-id="59871-143">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="59871-143">-SshKeyValue</span></span>
<span data-ttu-id="59871-144">Valore del file di chiave SSH o percorso file chiave.</span><span class="sxs-lookup"><span data-stu-id="59871-144">SSH key file value or key file path.</span></span>
<span data-ttu-id="59871-145">Il valore predefinito è {HOME}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="59871-145">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="59871-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="59871-146">-Tag</span></span>
<span data-ttu-id="59871-147">Tag da applicare alla risorsa</span><span class="sxs-lookup"><span data-stu-id="59871-147">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="59871-148">-Confermare</span><span class="sxs-lookup"><span data-stu-id="59871-148">-Confirm</span></span>
<span data-ttu-id="59871-149">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59871-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59871-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59871-150">-WhatIf</span></span>
<span data-ttu-id="59871-151">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="59871-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59871-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="59871-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59871-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59871-153">CommonParameters</span></span>
<span data-ttu-id="59871-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59871-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59871-155">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59871-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59871-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="59871-156">INPUTS</span></span>

### <span data-ttu-id="59871-157">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="59871-157">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="59871-158">System. String</span><span class="sxs-lookup"><span data-stu-id="59871-158">System.String</span></span>

## <span data-ttu-id="59871-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="59871-159">OUTPUTS</span></span>

### <span data-ttu-id="59871-160">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="59871-160">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="59871-161">Note</span><span class="sxs-lookup"><span data-stu-id="59871-161">NOTES</span></span>

## <span data-ttu-id="59871-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="59871-162">RELATED LINKS</span></span>
