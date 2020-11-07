---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/new-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/New-AzureRmAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/New-AzureRmAks.md
ms.openlocfilehash: ed68271ae29c7af0219fa08d1c342b636d7d3fbd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687962"
---
# <span data-ttu-id="9dddf-101">New-AzureRmAks</span><span class="sxs-lookup"><span data-stu-id="9dddf-101">New-AzureRmAks</span></span>

## <span data-ttu-id="9dddf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9dddf-102">SYNOPSIS</span></span>
<span data-ttu-id="9dddf-103">Creare un nuovo cluster Kubernetes gestito.</span><span class="sxs-lookup"><span data-stu-id="9dddf-103">Create a new managed Kubernetes cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9dddf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9dddf-104">SYNTAX</span></span>

```
New-AzureRmAks [-ResourceGroupName] <String> [-Name] <String> [[-ClientIdAndSecret] <PSCredential>]
 [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-Force] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9dddf-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9dddf-105">DESCRIPTION</span></span>
<span data-ttu-id="9dddf-106">Creare un nuovo cluster Kubernetes gestito.</span><span class="sxs-lookup"><span data-stu-id="9dddf-106">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="9dddf-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9dddf-107">EXAMPLES</span></span>

### <span data-ttu-id="9dddf-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9dddf-108">Example 1</span></span>
<span data-ttu-id="9dddf-109">Creare un nuovo cluster Kubernetes gestito con params predefiniti</span><span class="sxs-lookup"><span data-stu-id="9dddf-109">Create a new managed Kubernetes cluster with default params</span></span>

```
PS C:\> New-AzureRmAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="9dddf-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9dddf-110">PARAMETERS</span></span>

### <span data-ttu-id="9dddf-111">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="9dddf-111">-AdminUserName</span></span>
<span data-ttu-id="9dddf-112">Nome utente per le macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="9dddf-112">User name for the Linux Virtual Machines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dddf-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9dddf-113">-AsJob</span></span>
<span data-ttu-id="9dddf-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="9dddf-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dddf-115">-ClientIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="9dddf-115">-ClientIdAndSecret</span></span>
<span data-ttu-id="9dddf-116">ID client e segreto client associato all'entità dell'applicazione/servizio AAD.</span><span class="sxs-lookup"><span data-stu-id="9dddf-116">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dddf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dddf-117">-DefaultProfile</span></span>
<span data-ttu-id="9dddf-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9dddf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dddf-119">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="9dddf-119">-DnsNamePrefix</span></span>
<span data-ttu-id="9dddf-120">Prefisso del nome DNS per il cluster.</span><span class="sxs-lookup"><span data-stu-id="9dddf-120">The DNS name prefix for the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dddf-121">-Force</span><span class="sxs-lookup"><span data-stu-id="9dddf-121">-Force</span></span>
<span data-ttu-id="9dddf-122">Creare un cluster anche se esiste già</span><span class="sxs-lookup"><span data-stu-id="9dddf-122">Create cluster even if it already exists</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dddf-123">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="9dddf-123">-KubernetesVersion</span></span>
<span data-ttu-id="9dddf-124">La versione di Kubernetes da usare per creare il cluster.</span><span class="sxs-lookup"><span data-stu-id="9dddf-124">The version of Kubernetes to use for creating the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dddf-125">-Posizione</span><span class="sxs-lookup"><span data-stu-id="9dddf-125">-Location</span></span>
<span data-ttu-id="9dddf-126">Posizione di Azure per il cluster.</span><span class="sxs-lookup"><span data-stu-id="9dddf-126">Azure location for the cluster.</span></span>
<span data-ttu-id="9dddf-127">Il valore predefinito è la posizione del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9dddf-127">Defaults to the location of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dddf-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="9dddf-128">-Name</span></span>
<span data-ttu-id="9dddf-129">Nome del cluster gestito Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="9dddf-129">Kubernetes managed cluster Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dddf-130">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="9dddf-130">-NodeCount</span></span>
<span data-ttu-id="9dddf-131">Numero predefinito di nodi per i pool di nodi.</span><span class="sxs-lookup"><span data-stu-id="9dddf-131">The default number of nodes for the node pools.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dddf-132">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="9dddf-132">-NodeOsDiskSize</span></span>
<span data-ttu-id="9dddf-133">Numero predefinito di nodi per i pool di nodi.</span><span class="sxs-lookup"><span data-stu-id="9dddf-133">The default number of nodes for the node pools.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dddf-134">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="9dddf-134">-NodeVmSize</span></span>
<span data-ttu-id="9dddf-135">Le dimensioni della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9dddf-135">The size of the Virtual Machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dddf-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dddf-136">-ResourceGroupName</span></span>
<span data-ttu-id="9dddf-137">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9dddf-137">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dddf-138">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="9dddf-138">-SshKeyValue</span></span>
<span data-ttu-id="9dddf-139">Valore del file di chiave SSH o percorso file chiave.</span><span class="sxs-lookup"><span data-stu-id="9dddf-139">SSH key file value or key file path.</span></span>
<span data-ttu-id="9dddf-140">Il valore predefinito è {HOME}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="9dddf-140">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SshKeyPath

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dddf-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="9dddf-141">-Tag</span></span>
<span data-ttu-id="9dddf-142">Tag da applicare alla risorsa</span><span class="sxs-lookup"><span data-stu-id="9dddf-142">Tags to be applied to the resource</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dddf-143">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9dddf-143">-Confirm</span></span>
<span data-ttu-id="9dddf-144">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9dddf-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dddf-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dddf-145">-WhatIf</span></span>
<span data-ttu-id="9dddf-146">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9dddf-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9dddf-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9dddf-147">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dddf-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dddf-148">CommonParameters</span></span>
<span data-ttu-id="9dddf-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dddf-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dddf-150">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9dddf-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dddf-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9dddf-151">INPUTS</span></span>

### <span data-ttu-id="9dddf-152">Nessuno</span><span class="sxs-lookup"><span data-stu-id="9dddf-152">None</span></span>

## <span data-ttu-id="9dddf-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9dddf-153">OUTPUTS</span></span>

### <span data-ttu-id="9dddf-154">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="9dddf-154">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="9dddf-155">Note</span><span class="sxs-lookup"><span data-stu-id="9dddf-155">NOTES</span></span>

## <span data-ttu-id="9dddf-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9dddf-156">RELATED LINKS</span></span>
