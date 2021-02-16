---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/import-azakscredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Import-AzAksCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Import-AzAksCredential.md
ms.openlocfilehash: fe4e56e809dd2cda7c650e24b55ae3867a23a7b5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199855"
---
# <span data-ttu-id="03c80-101">Import-AzAksCredential</span><span class="sxs-lookup"><span data-stu-id="03c80-101">Import-AzAksCredential</span></span>

## <span data-ttu-id="03c80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03c80-102">SYNOPSIS</span></span>
<span data-ttu-id="03c80-103">Importare e unire la configurazione Kubectl per un cluster Kubernetes gestito.</span><span class="sxs-lookup"><span data-stu-id="03c80-103">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

## <span data-ttu-id="03c80-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="03c80-104">SYNTAX</span></span>

### <span data-ttu-id="03c80-105">GroupNameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="03c80-105">GroupNameParameterSet (Default)</span></span>
```
Import-AzAksCredential [-ResourceGroupName] <String> [-Name] <String> [-Admin] [-ConfigPath <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03c80-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="03c80-106">InputObjectParameterSet</span></span>
```
Import-AzAksCredential -InputObject <PSKubernetesCluster> [-Admin] [-ConfigPath <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03c80-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="03c80-107">IdParameterSet</span></span>
```
Import-AzAksCredential [-Id] <String> [-Admin] [-ConfigPath <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03c80-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="03c80-108">DESCRIPTION</span></span>
<span data-ttu-id="03c80-109">Importare e unire la configurazione Kubectl per un cluster Kubernetes gestito.</span><span class="sxs-lookup"><span data-stu-id="03c80-109">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

## <span data-ttu-id="03c80-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="03c80-110">EXAMPLES</span></span>

### <span data-ttu-id="03c80-111">Importare e unire la configurazione kubectl</span><span class="sxs-lookup"><span data-stu-id="03c80-111">Import and merge Kubectl config</span></span>
```
PS C:\> Import-AzAksCredential -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="03c80-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03c80-112">PARAMETERS</span></span>

### <span data-ttu-id="03c80-113">-Admin</span><span class="sxs-lookup"><span data-stu-id="03c80-113">-Admin</span></span>
<span data-ttu-id="03c80-114">Ottenere la configurazione kubectl di 'clusterAdmin' invece dell'impostazione predefinita 'clusterUser'.</span><span class="sxs-lookup"><span data-stu-id="03c80-114">Get the 'clusterAdmin' kubectl config instead of the default 'clusterUser'.</span></span>

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

### <span data-ttu-id="03c80-115">-ConfigPath</span><span class="sxs-lookup"><span data-stu-id="03c80-115">-ConfigPath</span></span>
<span data-ttu-id="03c80-116">Un file di configurazione kubectl da creare o aggiornare.</span><span class="sxs-lookup"><span data-stu-id="03c80-116">A kubectl config file to create or update.</span></span>
<span data-ttu-id="03c80-117">Usare invece "-" per stampare YAML su stdout.</span><span class="sxs-lookup"><span data-stu-id="03c80-117">Use '-' to print YAML to stdout instead.</span></span>
<span data-ttu-id="03c80-118">Impostazione predefinita: %Home%/.kube/config.</span><span class="sxs-lookup"><span data-stu-id="03c80-118">Default: %Home%/.kube/config.</span></span>

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

### <span data-ttu-id="03c80-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03c80-119">-DefaultProfile</span></span>
<span data-ttu-id="03c80-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="03c80-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03c80-121">-Force</span><span class="sxs-lookup"><span data-stu-id="03c80-121">-Force</span></span>
<span data-ttu-id="03c80-122">Importa configurazione Kubernetes anche se è l'impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="03c80-122">Import Kubernetes config even if it is the default</span></span>

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

### <span data-ttu-id="03c80-123">-Id</span><span class="sxs-lookup"><span data-stu-id="03c80-123">-Id</span></span>
<span data-ttu-id="03c80-124">ID di un cluster Kubernetes gestito</span><span class="sxs-lookup"><span data-stu-id="03c80-124">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="03c80-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03c80-125">-InputObject</span></span>
<span data-ttu-id="03c80-126">Oggetto PSKubernetesCluster, che in genere passa attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="03c80-126">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="03c80-127">-Name</span><span class="sxs-lookup"><span data-stu-id="03c80-127">-Name</span></span>
<span data-ttu-id="03c80-128">Nome del cluster Kubernetes gestito</span><span class="sxs-lookup"><span data-stu-id="03c80-128">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="03c80-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03c80-129">-PassThru</span></span>
<span data-ttu-id="03c80-130">Restituisce true se l'importazione riesce</span><span class="sxs-lookup"><span data-stu-id="03c80-130">Returns true if import is successful</span></span>

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

### <span data-ttu-id="03c80-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03c80-131">-ResourceGroupName</span></span>
<span data-ttu-id="03c80-132">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="03c80-132">Resource group name</span></span>

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

### <span data-ttu-id="03c80-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="03c80-133">-Confirm</span></span>
<span data-ttu-id="03c80-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03c80-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03c80-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03c80-135">-WhatIf</span></span>
<span data-ttu-id="03c80-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="03c80-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03c80-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="03c80-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03c80-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03c80-138">CommonParameters</span></span>
<span data-ttu-id="03c80-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03c80-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03c80-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="03c80-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03c80-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="03c80-141">INPUTS</span></span>

### <span data-ttu-id="03c80-142">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="03c80-142">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="03c80-143">System.String</span><span class="sxs-lookup"><span data-stu-id="03c80-143">System.String</span></span>

## <span data-ttu-id="03c80-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="03c80-144">OUTPUTS</span></span>

### <span data-ttu-id="03c80-145">System.String</span><span class="sxs-lookup"><span data-stu-id="03c80-145">System.String</span></span>

## <span data-ttu-id="03c80-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="03c80-146">NOTES</span></span>

## <span data-ttu-id="03c80-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="03c80-147">RELATED LINKS</span></span>
