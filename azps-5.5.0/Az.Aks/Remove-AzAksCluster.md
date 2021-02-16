---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/remove-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksCluster.md
ms.openlocfilehash: d6364030eedb75b59c5f9a86bb57499864270fa2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199838"
---
# <span data-ttu-id="35dbf-101">Remove-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="35dbf-101">Remove-AzAksCluster</span></span>

## <span data-ttu-id="35dbf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35dbf-102">SYNOPSIS</span></span>
<span data-ttu-id="35dbf-103">Eliminare un cluster Kubernetes gestito.</span><span class="sxs-lookup"><span data-stu-id="35dbf-103">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="35dbf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="35dbf-104">SYNTAX</span></span>

### <span data-ttu-id="35dbf-105">GroupNameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="35dbf-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAksCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35dbf-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="35dbf-106">InputObjectParameterSet</span></span>
```
Remove-AzAksCluster -InputObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35dbf-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="35dbf-107">IdParameterSet</span></span>
```
Remove-AzAksCluster [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35dbf-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="35dbf-108">DESCRIPTION</span></span>
<span data-ttu-id="35dbf-109">Eliminare un cluster Kubernetes gestito.</span><span class="sxs-lookup"><span data-stu-id="35dbf-109">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="35dbf-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="35dbf-110">EXAMPLES</span></span>

### <span data-ttu-id="35dbf-111">Eliminare un cluster Kubernetes gestito esistente</span><span class="sxs-lookup"><span data-stu-id="35dbf-111">Delete an existing managed Kubernetes cluster</span></span>
```powershell
PS C:\> Remove-AzAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="35dbf-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35dbf-112">PARAMETERS</span></span>

### <span data-ttu-id="35dbf-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35dbf-113">-AsJob</span></span>
<span data-ttu-id="35dbf-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="35dbf-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="35dbf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35dbf-115">-DefaultProfile</span></span>
<span data-ttu-id="35dbf-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="35dbf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35dbf-117">-Force</span><span class="sxs-lookup"><span data-stu-id="35dbf-117">-Force</span></span>
<span data-ttu-id="35dbf-118">Rimuovere il cluster Kubernetes gestito senza richiesta</span><span class="sxs-lookup"><span data-stu-id="35dbf-118">Remove managed Kubernetes cluster without prompt</span></span>

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

### <span data-ttu-id="35dbf-119">-Id</span><span class="sxs-lookup"><span data-stu-id="35dbf-119">-Id</span></span>
<span data-ttu-id="35dbf-120">ID di un cluster Kubernetes gestito</span><span class="sxs-lookup"><span data-stu-id="35dbf-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="35dbf-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35dbf-121">-InputObject</span></span>
<span data-ttu-id="35dbf-122">Oggetto PSKubernetesCluster, che in genere passa attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="35dbf-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="35dbf-123">-Name</span><span class="sxs-lookup"><span data-stu-id="35dbf-123">-Name</span></span>
<span data-ttu-id="35dbf-124">Nome del cluster Kubernetes gestito</span><span class="sxs-lookup"><span data-stu-id="35dbf-124">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="35dbf-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="35dbf-125">-PassThru</span></span>
<span data-ttu-id="35dbf-126">restituisce true se l'eliminazione ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="35dbf-126">Returns true if deletion is successful</span></span>

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

### <span data-ttu-id="35dbf-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35dbf-127">-ResourceGroupName</span></span>
<span data-ttu-id="35dbf-128">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="35dbf-128">Resource group name</span></span>

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

### <span data-ttu-id="35dbf-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35dbf-129">-Confirm</span></span>
<span data-ttu-id="35dbf-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35dbf-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35dbf-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35dbf-131">-WhatIf</span></span>
<span data-ttu-id="35dbf-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="35dbf-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35dbf-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="35dbf-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35dbf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35dbf-134">CommonParameters</span></span>
<span data-ttu-id="35dbf-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35dbf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35dbf-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="35dbf-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35dbf-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="35dbf-137">INPUTS</span></span>

### <span data-ttu-id="35dbf-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="35dbf-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="35dbf-139">System.String</span><span class="sxs-lookup"><span data-stu-id="35dbf-139">System.String</span></span>

## <span data-ttu-id="35dbf-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="35dbf-140">OUTPUTS</span></span>

### <span data-ttu-id="35dbf-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="35dbf-141">System.Boolean</span></span>

## <span data-ttu-id="35dbf-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="35dbf-142">NOTES</span></span>

## <span data-ttu-id="35dbf-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="35dbf-143">RELATED LINKS</span></span>
