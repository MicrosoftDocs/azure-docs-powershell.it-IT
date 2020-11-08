---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/remove-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksCluster.md
ms.openlocfilehash: d6364030eedb75b59c5f9a86bb57499864270fa2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200569"
---
# <span data-ttu-id="5a4d4-101">Remove-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="5a4d4-101">Remove-AzAksCluster</span></span>

## <span data-ttu-id="5a4d4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5a4d4-102">SYNOPSIS</span></span>
<span data-ttu-id="5a4d4-103">Eliminare un cluster Kubernetes gestito.</span><span class="sxs-lookup"><span data-stu-id="5a4d4-103">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="5a4d4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5a4d4-104">SYNTAX</span></span>

### <span data-ttu-id="5a4d4-105">GroupNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5a4d4-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAksCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a4d4-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a4d4-106">InputObjectParameterSet</span></span>
```
Remove-AzAksCluster -InputObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a4d4-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a4d4-107">IdParameterSet</span></span>
```
Remove-AzAksCluster [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a4d4-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5a4d4-108">DESCRIPTION</span></span>
<span data-ttu-id="5a4d4-109">Eliminare un cluster Kubernetes gestito.</span><span class="sxs-lookup"><span data-stu-id="5a4d4-109">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="5a4d4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5a4d4-110">EXAMPLES</span></span>

### <span data-ttu-id="5a4d4-111">Eliminare un cluster Kubernetes gestito esistente</span><span class="sxs-lookup"><span data-stu-id="5a4d4-111">Delete an existing managed Kubernetes cluster</span></span>
```powershell
PS C:\> Remove-AzAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="5a4d4-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5a4d4-112">PARAMETERS</span></span>

### <span data-ttu-id="5a4d4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5a4d4-113">-AsJob</span></span>
<span data-ttu-id="5a4d4-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="5a4d4-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5a4d4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a4d4-115">-DefaultProfile</span></span>
<span data-ttu-id="5a4d4-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5a4d4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a4d4-117">-Force</span><span class="sxs-lookup"><span data-stu-id="5a4d4-117">-Force</span></span>
<span data-ttu-id="5a4d4-118">Rimuovere il cluster gestito di Kubernetes senza richiesta</span><span class="sxs-lookup"><span data-stu-id="5a4d4-118">Remove managed Kubernetes cluster without prompt</span></span>

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

### <span data-ttu-id="5a4d4-119">-ID</span><span class="sxs-lookup"><span data-stu-id="5a4d4-119">-Id</span></span>
<span data-ttu-id="5a4d4-120">ID di un cluster Kubernetes gestito</span><span class="sxs-lookup"><span data-stu-id="5a4d4-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="5a4d4-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a4d4-121">-InputObject</span></span>
<span data-ttu-id="5a4d4-122">Un oggetto PSKubernetesCluster, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="5a4d4-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="5a4d4-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="5a4d4-123">-Name</span></span>
<span data-ttu-id="5a4d4-124">Nome del cluster di Kubernetes gestito</span><span class="sxs-lookup"><span data-stu-id="5a4d4-124">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="5a4d4-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a4d4-125">-PassThru</span></span>
<span data-ttu-id="5a4d4-126">Restituisce vero se l'eliminazione è riuscita</span><span class="sxs-lookup"><span data-stu-id="5a4d4-126">Returns true if deletion is successful</span></span>

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

### <span data-ttu-id="5a4d4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a4d4-127">-ResourceGroupName</span></span>
<span data-ttu-id="5a4d4-128">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="5a4d4-128">Resource group name</span></span>

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

### <span data-ttu-id="5a4d4-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5a4d4-129">-Confirm</span></span>
<span data-ttu-id="5a4d4-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a4d4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a4d4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a4d4-131">-WhatIf</span></span>
<span data-ttu-id="5a4d4-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5a4d4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a4d4-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5a4d4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a4d4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a4d4-134">CommonParameters</span></span>
<span data-ttu-id="5a4d4-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a4d4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a4d4-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5a4d4-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a4d4-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5a4d4-137">INPUTS</span></span>

### <span data-ttu-id="5a4d4-138">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="5a4d4-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="5a4d4-139">System. String</span><span class="sxs-lookup"><span data-stu-id="5a4d4-139">System.String</span></span>

## <span data-ttu-id="5a4d4-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5a4d4-140">OUTPUTS</span></span>

### <span data-ttu-id="5a4d4-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5a4d4-141">System.Boolean</span></span>

## <span data-ttu-id="5a4d4-142">Note</span><span class="sxs-lookup"><span data-stu-id="5a4d4-142">NOTES</span></span>

## <span data-ttu-id="5a4d4-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5a4d4-143">RELATED LINKS</span></span>
