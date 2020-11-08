---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAks.md
ms.openlocfilehash: a5a376fea0dc40bbfd02ea1cb430c725c2bc14e8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021843"
---
# <span data-ttu-id="1b3a9-101">New-AzAks</span><span class="sxs-lookup"><span data-stu-id="1b3a9-101">New-AzAks</span></span>

## <span data-ttu-id="1b3a9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1b3a9-102">SYNOPSIS</span></span>
<span data-ttu-id="1b3a9-103">Creare un nuovo cluster Kubernetes gestito.</span><span class="sxs-lookup"><span data-stu-id="1b3a9-103">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="1b3a9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1b3a9-104">SYNTAX</span></span>

```
New-AzAks [-Force] [-ResourceGroupName] <String> [-Name] <String> [[-ClientIdAndSecret] <PSCredential>]
 [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b3a9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b3a9-105">DESCRIPTION</span></span>

<span data-ttu-id="1b3a9-106">Creare un nuovo cluster Kubernetes gestito.</span><span class="sxs-lookup"><span data-stu-id="1b3a9-106">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="1b3a9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1b3a9-107">EXAMPLES</span></span>

### <span data-ttu-id="1b3a9-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1b3a9-108">Example 1</span></span>

<span data-ttu-id="1b3a9-109">Creare un nuovo cluster Kubernetes gestito con params predefiniti.</span><span class="sxs-lookup"><span data-stu-id="1b3a9-109">Create a new managed Kubernetes cluster with default params.</span></span>

```
PS C:\> New-AzAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="1b3a9-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1b3a9-110">PARAMETERS</span></span>

### <span data-ttu-id="1b3a9-111">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="1b3a9-111">-AdminUserName</span></span>
<span data-ttu-id="1b3a9-112">Nome utente per le macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="1b3a9-112">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="1b3a9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1b3a9-113">-AsJob</span></span>
<span data-ttu-id="1b3a9-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="1b3a9-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1b3a9-115">-ClientIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="1b3a9-115">-ClientIdAndSecret</span></span>
<span data-ttu-id="1b3a9-116">ID client e segreto client associato all'entità dell'applicazione/servizio AAD.</span><span class="sxs-lookup"><span data-stu-id="1b3a9-116">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b3a9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b3a9-117">-DefaultProfile</span></span>
<span data-ttu-id="1b3a9-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1b3a9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b3a9-119">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="1b3a9-119">-DnsNamePrefix</span></span>
<span data-ttu-id="1b3a9-120">Prefisso del nome DNS per il cluster.</span><span class="sxs-lookup"><span data-stu-id="1b3a9-120">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="1b3a9-121">-Force</span><span class="sxs-lookup"><span data-stu-id="1b3a9-121">-Force</span></span>
<span data-ttu-id="1b3a9-122">Creare un cluster anche se esiste già</span><span class="sxs-lookup"><span data-stu-id="1b3a9-122">Create cluster even if it already exists</span></span>

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

### <span data-ttu-id="1b3a9-123">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="1b3a9-123">-KubernetesVersion</span></span>
<span data-ttu-id="1b3a9-124">La versione di Kubernetes da usare per creare il cluster.</span><span class="sxs-lookup"><span data-stu-id="1b3a9-124">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="1b3a9-125">-Posizione</span><span class="sxs-lookup"><span data-stu-id="1b3a9-125">-Location</span></span>
<span data-ttu-id="1b3a9-126">Posizione di Azure per il cluster.</span><span class="sxs-lookup"><span data-stu-id="1b3a9-126">Azure location for the cluster.</span></span>
<span data-ttu-id="1b3a9-127">Il valore predefinito è la posizione del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1b3a9-127">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="1b3a9-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="1b3a9-128">-Name</span></span>
<span data-ttu-id="1b3a9-129">Nome del cluster gestito Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="1b3a9-129">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b3a9-130">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="1b3a9-130">-NodeCount</span></span>
<span data-ttu-id="1b3a9-131">Numero predefinito di nodi per i pool di nodi.</span><span class="sxs-lookup"><span data-stu-id="1b3a9-131">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="1b3a9-132">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="1b3a9-132">-NodeOsDiskSize</span></span>
<span data-ttu-id="1b3a9-133">Dimensioni in GB del disco del sistema operativo per ogni nodo nel pool di nodi.</span><span class="sxs-lookup"><span data-stu-id="1b3a9-133">Size in GB of the OS disk for each node in the node pool.</span></span> <span data-ttu-id="1b3a9-134">Minimo 30 GB.</span><span class="sxs-lookup"><span data-stu-id="1b3a9-134">Minimum 30 GB.</span></span>

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

### <span data-ttu-id="1b3a9-135">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="1b3a9-135">-NodeVmSize</span></span>
<span data-ttu-id="1b3a9-136">Le dimensioni della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1b3a9-136">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="1b3a9-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b3a9-137">-ResourceGroupName</span></span>
<span data-ttu-id="1b3a9-138">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1b3a9-138">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b3a9-139">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="1b3a9-139">-SshKeyValue</span></span>
<span data-ttu-id="1b3a9-140">Valore del file di chiave SSH o percorso file chiave.</span><span class="sxs-lookup"><span data-stu-id="1b3a9-140">SSH key file value or key file path.</span></span>
<span data-ttu-id="1b3a9-141">Il valore predefinito è {HOME}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="1b3a9-141">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="1b3a9-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="1b3a9-142">-Tag</span></span>
<span data-ttu-id="1b3a9-143">Tag da applicare alla risorsa</span><span class="sxs-lookup"><span data-stu-id="1b3a9-143">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="1b3a9-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1b3a9-144">-Confirm</span></span>
<span data-ttu-id="1b3a9-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b3a9-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b3a9-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b3a9-146">-WhatIf</span></span>
<span data-ttu-id="1b3a9-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1b3a9-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b3a9-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1b3a9-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b3a9-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b3a9-149">CommonParameters</span></span>
<span data-ttu-id="1b3a9-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b3a9-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b3a9-151">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b3a9-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b3a9-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1b3a9-152">INPUTS</span></span>

### <span data-ttu-id="1b3a9-153">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1b3a9-153">None</span></span>

## <span data-ttu-id="1b3a9-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1b3a9-154">OUTPUTS</span></span>

### <span data-ttu-id="1b3a9-155">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="1b3a9-155">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="1b3a9-156">Note</span><span class="sxs-lookup"><span data-stu-id="1b3a9-156">NOTES</span></span>

## <span data-ttu-id="1b3a9-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1b3a9-157">RELATED LINKS</span></span>
