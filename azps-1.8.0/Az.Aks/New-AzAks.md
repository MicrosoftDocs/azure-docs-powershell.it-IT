---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAks.md
ms.openlocfilehash: 1de3cef0d14213a52873742f9bf878aaa545e8bf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673704"
---
# <span data-ttu-id="f57bf-101">New-AzAks</span><span class="sxs-lookup"><span data-stu-id="f57bf-101">New-AzAks</span></span>

## <span data-ttu-id="f57bf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f57bf-102">SYNOPSIS</span></span>
<span data-ttu-id="f57bf-103">Creare un nuovo cluster Kubernetes gestito.</span><span class="sxs-lookup"><span data-stu-id="f57bf-103">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="f57bf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f57bf-104">SYNTAX</span></span>

```
New-AzAks [-Force] [-ResourceGroupName] <String> [-Name] <String> [[-ClientIdAndSecret] <PSCredential>]
 [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f57bf-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f57bf-105">DESCRIPTION</span></span>

<span data-ttu-id="f57bf-106">Creare un nuovo cluster Kubernetes gestito.</span><span class="sxs-lookup"><span data-stu-id="f57bf-106">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="f57bf-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f57bf-107">EXAMPLES</span></span>

### <span data-ttu-id="f57bf-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f57bf-108">Example 1</span></span>

<span data-ttu-id="f57bf-109">Creare un nuovo cluster Kubernetes gestito con params predefiniti.</span><span class="sxs-lookup"><span data-stu-id="f57bf-109">Create a new managed Kubernetes cluster with default params.</span></span>

```
PS C:\> New-AzAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="f57bf-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f57bf-110">PARAMETERS</span></span>

### <span data-ttu-id="f57bf-111">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="f57bf-111">-AdminUserName</span></span>
<span data-ttu-id="f57bf-112">Nome utente per le macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="f57bf-112">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="f57bf-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f57bf-113">-AsJob</span></span>
<span data-ttu-id="f57bf-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f57bf-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f57bf-115">-ClientIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="f57bf-115">-ClientIdAndSecret</span></span>
<span data-ttu-id="f57bf-116">ID client e segreto client associato all'entità dell'applicazione/servizio AAD.</span><span class="sxs-lookup"><span data-stu-id="f57bf-116">The client id and client secret associated with the AAD application / service principal.</span></span>

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

### <span data-ttu-id="f57bf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f57bf-117">-DefaultProfile</span></span>
<span data-ttu-id="f57bf-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f57bf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f57bf-119">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="f57bf-119">-DnsNamePrefix</span></span>
<span data-ttu-id="f57bf-120">Prefisso del nome DNS per il cluster.</span><span class="sxs-lookup"><span data-stu-id="f57bf-120">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="f57bf-121">-Force</span><span class="sxs-lookup"><span data-stu-id="f57bf-121">-Force</span></span>
<span data-ttu-id="f57bf-122">Creare un cluster anche se esiste già</span><span class="sxs-lookup"><span data-stu-id="f57bf-122">Create cluster even if it already exists</span></span>

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

### <span data-ttu-id="f57bf-123">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="f57bf-123">-KubernetesVersion</span></span>
<span data-ttu-id="f57bf-124">La versione di Kubernetes da usare per creare il cluster.</span><span class="sxs-lookup"><span data-stu-id="f57bf-124">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="f57bf-125">-Posizione</span><span class="sxs-lookup"><span data-stu-id="f57bf-125">-Location</span></span>
<span data-ttu-id="f57bf-126">Posizione di Azure per il cluster.</span><span class="sxs-lookup"><span data-stu-id="f57bf-126">Azure location for the cluster.</span></span>
<span data-ttu-id="f57bf-127">Il valore predefinito è la posizione del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f57bf-127">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="f57bf-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="f57bf-128">-Name</span></span>
<span data-ttu-id="f57bf-129">Nome del cluster gestito Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="f57bf-129">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="f57bf-130">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="f57bf-130">-NodeCount</span></span>
<span data-ttu-id="f57bf-131">Numero predefinito di nodi per i pool di nodi.</span><span class="sxs-lookup"><span data-stu-id="f57bf-131">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="f57bf-132">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="f57bf-132">-NodeOsDiskSize</span></span>
<span data-ttu-id="f57bf-133">Dimensioni in GB del disco del sistema operativo per ogni nodo nel pool di nodi.</span><span class="sxs-lookup"><span data-stu-id="f57bf-133">Size in GB of the OS disk for each node in the node pool.</span></span> <span data-ttu-id="f57bf-134">Minimo 30 GB.</span><span class="sxs-lookup"><span data-stu-id="f57bf-134">Minimum 30 GB.</span></span>

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

### <span data-ttu-id="f57bf-135">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="f57bf-135">-NodeVmSize</span></span>
<span data-ttu-id="f57bf-136">Le dimensioni della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f57bf-136">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="f57bf-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f57bf-137">-ResourceGroupName</span></span>
<span data-ttu-id="f57bf-138">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f57bf-138">Resource Group Name.</span></span>

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

### <span data-ttu-id="f57bf-139">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="f57bf-139">-SshKeyValue</span></span>
<span data-ttu-id="f57bf-140">Valore del file di chiave SSH o percorso file chiave.</span><span class="sxs-lookup"><span data-stu-id="f57bf-140">SSH key file value or key file path.</span></span>
<span data-ttu-id="f57bf-141">Il valore predefinito è {HOME}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="f57bf-141">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="f57bf-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="f57bf-142">-Tag</span></span>
<span data-ttu-id="f57bf-143">Tag da applicare alla risorsa</span><span class="sxs-lookup"><span data-stu-id="f57bf-143">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="f57bf-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f57bf-144">-Confirm</span></span>
<span data-ttu-id="f57bf-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f57bf-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f57bf-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f57bf-146">-WhatIf</span></span>
<span data-ttu-id="f57bf-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f57bf-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f57bf-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f57bf-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f57bf-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f57bf-149">CommonParameters</span></span>
<span data-ttu-id="f57bf-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f57bf-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f57bf-151">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f57bf-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f57bf-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f57bf-152">INPUTS</span></span>

### <span data-ttu-id="f57bf-153">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f57bf-153">None</span></span>

## <span data-ttu-id="f57bf-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f57bf-154">OUTPUTS</span></span>

### <span data-ttu-id="f57bf-155">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="f57bf-155">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="f57bf-156">Note</span><span class="sxs-lookup"><span data-stu-id="f57bf-156">NOTES</span></span>

## <span data-ttu-id="f57bf-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f57bf-157">RELATED LINKS</span></span>
