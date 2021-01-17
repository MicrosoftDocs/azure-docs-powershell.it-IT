---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/import-azakscredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Import-AzAksCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Import-AzAksCredential.md
ms.openlocfilehash: fe4e56e809dd2cda7c650e24b55ae3867a23a7b5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475986"
---
# <span data-ttu-id="c55be-101">Import-AzAksCredential</span><span class="sxs-lookup"><span data-stu-id="c55be-101">Import-AzAksCredential</span></span>

## <span data-ttu-id="c55be-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c55be-102">SYNOPSIS</span></span>
<span data-ttu-id="c55be-103">Importare e unire la configurazione di Kubectl per un cluster Kubernetes gestito.</span><span class="sxs-lookup"><span data-stu-id="c55be-103">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

## <span data-ttu-id="c55be-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c55be-104">SYNTAX</span></span>

### <span data-ttu-id="c55be-105">GroupNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c55be-105">GroupNameParameterSet (Default)</span></span>
```
Import-AzAksCredential [-ResourceGroupName] <String> [-Name] <String> [-Admin] [-ConfigPath <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c55be-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c55be-106">InputObjectParameterSet</span></span>
```
Import-AzAksCredential -InputObject <PSKubernetesCluster> [-Admin] [-ConfigPath <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c55be-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c55be-107">IdParameterSet</span></span>
```
Import-AzAksCredential [-Id] <String> [-Admin] [-ConfigPath <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c55be-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c55be-108">DESCRIPTION</span></span>
<span data-ttu-id="c55be-109">Importare e unire la configurazione di Kubectl per un cluster Kubernetes gestito.</span><span class="sxs-lookup"><span data-stu-id="c55be-109">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

## <span data-ttu-id="c55be-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c55be-110">EXAMPLES</span></span>

### <span data-ttu-id="c55be-111">Importare e unire la configurazione di Kubectl</span><span class="sxs-lookup"><span data-stu-id="c55be-111">Import and merge Kubectl config</span></span>
```
PS C:\> Import-AzAksCredential -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="c55be-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c55be-112">PARAMETERS</span></span>

### <span data-ttu-id="c55be-113">-Amministratore</span><span class="sxs-lookup"><span data-stu-id="c55be-113">-Admin</span></span>
<span data-ttu-id="c55be-114">Ottieni la configurazione di clusterAdmin'kubectl invece del valore predefinito "clusterUser".</span><span class="sxs-lookup"><span data-stu-id="c55be-114">Get the 'clusterAdmin' kubectl config instead of the default 'clusterUser'.</span></span>

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

### <span data-ttu-id="c55be-115">-ConfigPath</span><span class="sxs-lookup"><span data-stu-id="c55be-115">-ConfigPath</span></span>
<span data-ttu-id="c55be-116">File di configurazione di kubectl da creare o aggiornare.</span><span class="sxs-lookup"><span data-stu-id="c55be-116">A kubectl config file to create or update.</span></span>
<span data-ttu-id="c55be-117">USA '-' per stampare YAML in stdout.</span><span class="sxs-lookup"><span data-stu-id="c55be-117">Use '-' to print YAML to stdout instead.</span></span>
<span data-ttu-id="c55be-118">Impostazione predefinita:% Home%/.Kube/config.</span><span class="sxs-lookup"><span data-stu-id="c55be-118">Default: %Home%/.kube/config.</span></span>

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

### <span data-ttu-id="c55be-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c55be-119">-DefaultProfile</span></span>
<span data-ttu-id="c55be-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c55be-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c55be-121">-Force</span><span class="sxs-lookup"><span data-stu-id="c55be-121">-Force</span></span>
<span data-ttu-id="c55be-122">Importare la configurazione di Kubernetes anche se è l'impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="c55be-122">Import Kubernetes config even if it is the default</span></span>

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

### <span data-ttu-id="c55be-123">-ID</span><span class="sxs-lookup"><span data-stu-id="c55be-123">-Id</span></span>
<span data-ttu-id="c55be-124">ID di un cluster Kubernetes gestito</span><span class="sxs-lookup"><span data-stu-id="c55be-124">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="c55be-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c55be-125">-InputObject</span></span>
<span data-ttu-id="c55be-126">Un oggetto PSKubernetesCluster, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="c55be-126">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="c55be-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="c55be-127">-Name</span></span>
<span data-ttu-id="c55be-128">Nome del cluster di Kubernetes gestito</span><span class="sxs-lookup"><span data-stu-id="c55be-128">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c55be-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c55be-129">-PassThru</span></span>
<span data-ttu-id="c55be-130">Restituisce vero se l'importazione ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="c55be-130">Returns true if import is successful</span></span>

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

### <span data-ttu-id="c55be-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c55be-131">-ResourceGroupName</span></span>
<span data-ttu-id="c55be-132">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="c55be-132">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c55be-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c55be-133">-Confirm</span></span>
<span data-ttu-id="c55be-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c55be-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c55be-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c55be-135">-WhatIf</span></span>
<span data-ttu-id="c55be-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c55be-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c55be-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c55be-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c55be-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c55be-138">CommonParameters</span></span>
<span data-ttu-id="c55be-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c55be-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c55be-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c55be-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c55be-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c55be-141">INPUTS</span></span>

### <span data-ttu-id="c55be-142">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="c55be-142">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="c55be-143">System. String</span><span class="sxs-lookup"><span data-stu-id="c55be-143">System.String</span></span>

## <span data-ttu-id="c55be-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c55be-144">OUTPUTS</span></span>

### <span data-ttu-id="c55be-145">System. String</span><span class="sxs-lookup"><span data-stu-id="c55be-145">System.String</span></span>

## <span data-ttu-id="c55be-146">Note</span><span class="sxs-lookup"><span data-stu-id="c55be-146">NOTES</span></span>

## <span data-ttu-id="c55be-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c55be-147">RELATED LINKS</span></span>
