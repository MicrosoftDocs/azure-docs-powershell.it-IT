---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/new-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/New-AzureRmAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/New-AzureRmAks.md
ms.openlocfilehash: f91b4f2afdb1c6aaf7cbac16f952a333d3d362b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686980"
---
# <span data-ttu-id="7c513-101">New-AzureRmAks</span><span class="sxs-lookup"><span data-stu-id="7c513-101">New-AzureRmAks</span></span>

## <span data-ttu-id="7c513-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7c513-102">SYNOPSIS</span></span>
<span data-ttu-id="7c513-103">Creare un nuovo cluster Kubernetes gestito.</span><span class="sxs-lookup"><span data-stu-id="7c513-103">Create a new managed Kubernetes cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c513-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7c513-104">SYNTAX</span></span>

```
New-AzureRmAks [-Force] [-ResourceGroupName] <String> [-Name] <String> [[-ClientIdAndSecret] <PSCredential>]
 [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c513-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7c513-105">DESCRIPTION</span></span>

<span data-ttu-id="7c513-106">Creare un nuovo cluster Kubernetes gestito.</span><span class="sxs-lookup"><span data-stu-id="7c513-106">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="7c513-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7c513-107">EXAMPLES</span></span>

### <span data-ttu-id="7c513-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7c513-108">Example 1</span></span>

<span data-ttu-id="7c513-109">Creare un nuovo cluster Kubernetes gestito con params predefiniti.</span><span class="sxs-lookup"><span data-stu-id="7c513-109">Create a new managed Kubernetes cluster with default params.</span></span>

```
PS C:\> New-AzureRmAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="7c513-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7c513-110">PARAMETERS</span></span>

### <span data-ttu-id="7c513-111">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="7c513-111">-AdminUserName</span></span>
<span data-ttu-id="7c513-112">Nome utente per le macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="7c513-112">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="7c513-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c513-113">-AsJob</span></span>
<span data-ttu-id="7c513-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="7c513-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7c513-115">-ClientIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="7c513-115">-ClientIdAndSecret</span></span>
<span data-ttu-id="7c513-116">ID client e segreto client associato all'entità dell'applicazione/servizio AAD.</span><span class="sxs-lookup"><span data-stu-id="7c513-116">The client id and client secret associated with the AAD application / service principal.</span></span>

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

### <span data-ttu-id="7c513-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c513-117">-DefaultProfile</span></span>
<span data-ttu-id="7c513-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7c513-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c513-119">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="7c513-119">-DnsNamePrefix</span></span>
<span data-ttu-id="7c513-120">Prefisso del nome DNS per il cluster.</span><span class="sxs-lookup"><span data-stu-id="7c513-120">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="7c513-121">-Force</span><span class="sxs-lookup"><span data-stu-id="7c513-121">-Force</span></span>
<span data-ttu-id="7c513-122">Creare un cluster anche se esiste già</span><span class="sxs-lookup"><span data-stu-id="7c513-122">Create cluster even if it already exists</span></span>

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

### <span data-ttu-id="7c513-123">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="7c513-123">-KubernetesVersion</span></span>
<span data-ttu-id="7c513-124">La versione di Kubernetes da usare per creare il cluster.</span><span class="sxs-lookup"><span data-stu-id="7c513-124">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="7c513-125">-Posizione</span><span class="sxs-lookup"><span data-stu-id="7c513-125">-Location</span></span>
<span data-ttu-id="7c513-126">Posizione di Azure per il cluster.</span><span class="sxs-lookup"><span data-stu-id="7c513-126">Azure location for the cluster.</span></span>
<span data-ttu-id="7c513-127">Il valore predefinito è la posizione del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7c513-127">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="7c513-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="7c513-128">-Name</span></span>
<span data-ttu-id="7c513-129">Nome del cluster gestito Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="7c513-129">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="7c513-130">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="7c513-130">-NodeCount</span></span>
<span data-ttu-id="7c513-131">Numero predefinito di nodi per i pool di nodi.</span><span class="sxs-lookup"><span data-stu-id="7c513-131">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="7c513-132">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="7c513-132">-NodeOsDiskSize</span></span>
<span data-ttu-id="7c513-133">Dimensioni in GB del disco del sistema operativo per ogni nodo nel pool di nodi.</span><span class="sxs-lookup"><span data-stu-id="7c513-133">Size in GB of the OS disk for each node in the node pool.</span></span> <span data-ttu-id="7c513-134">Minimo 30 GB.</span><span class="sxs-lookup"><span data-stu-id="7c513-134">Minimum 30 GB.</span></span>

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

### <span data-ttu-id="7c513-135">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="7c513-135">-NodeVmSize</span></span>
<span data-ttu-id="7c513-136">Le dimensioni della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7c513-136">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="7c513-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c513-137">-ResourceGroupName</span></span>
<span data-ttu-id="7c513-138">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7c513-138">Resource Group Name.</span></span>

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

### <span data-ttu-id="7c513-139">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="7c513-139">-SshKeyValue</span></span>
<span data-ttu-id="7c513-140">Valore del file di chiave SSH o percorso file chiave.</span><span class="sxs-lookup"><span data-stu-id="7c513-140">SSH key file value or key file path.</span></span>
<span data-ttu-id="7c513-141">Il valore predefinito è {HOME}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="7c513-141">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="7c513-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="7c513-142">-Tag</span></span>
<span data-ttu-id="7c513-143">Tag da applicare alla risorsa</span><span class="sxs-lookup"><span data-stu-id="7c513-143">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="7c513-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7c513-144">-Confirm</span></span>
<span data-ttu-id="7c513-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c513-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c513-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c513-146">-WhatIf</span></span>
<span data-ttu-id="7c513-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7c513-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c513-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7c513-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c513-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c513-149">CommonParameters</span></span>
<span data-ttu-id="7c513-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c513-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c513-151">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c513-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c513-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7c513-152">INPUTS</span></span>

### <span data-ttu-id="7c513-153">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7c513-153">None</span></span>

## <span data-ttu-id="7c513-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7c513-154">OUTPUTS</span></span>

### <span data-ttu-id="7c513-155">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="7c513-155">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="7c513-156">Note</span><span class="sxs-lookup"><span data-stu-id="7c513-156">NOTES</span></span>

## <span data-ttu-id="7c513-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7c513-157">RELATED LINKS</span></span>
