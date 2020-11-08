---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/remove-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksCluster.md
ms.openlocfilehash: d6364030eedb75b59c5f9a86bb57499864270fa2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188642"
---
# <span data-ttu-id="31952-101">Remove-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="31952-101">Remove-AzAksCluster</span></span>

## <span data-ttu-id="31952-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="31952-102">SYNOPSIS</span></span>
<span data-ttu-id="31952-103">Eliminare un cluster Kubernetes gestito.</span><span class="sxs-lookup"><span data-stu-id="31952-103">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="31952-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="31952-104">SYNTAX</span></span>

### <span data-ttu-id="31952-105">GroupNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="31952-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAksCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31952-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="31952-106">InputObjectParameterSet</span></span>
```
Remove-AzAksCluster -InputObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31952-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="31952-107">IdParameterSet</span></span>
```
Remove-AzAksCluster [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31952-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31952-108">DESCRIPTION</span></span>
<span data-ttu-id="31952-109">Eliminare un cluster Kubernetes gestito.</span><span class="sxs-lookup"><span data-stu-id="31952-109">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="31952-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="31952-110">EXAMPLES</span></span>

### <span data-ttu-id="31952-111">Eliminare un cluster Kubernetes gestito esistente</span><span class="sxs-lookup"><span data-stu-id="31952-111">Delete an existing managed Kubernetes cluster</span></span>
```powershell
PS C:\> Remove-AzAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="31952-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="31952-112">PARAMETERS</span></span>

### <span data-ttu-id="31952-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="31952-113">-AsJob</span></span>
<span data-ttu-id="31952-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="31952-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="31952-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31952-115">-DefaultProfile</span></span>
<span data-ttu-id="31952-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="31952-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31952-117">-Force</span><span class="sxs-lookup"><span data-stu-id="31952-117">-Force</span></span>
<span data-ttu-id="31952-118">Rimuovere il cluster gestito di Kubernetes senza richiesta</span><span class="sxs-lookup"><span data-stu-id="31952-118">Remove managed Kubernetes cluster without prompt</span></span>

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

### <span data-ttu-id="31952-119">-ID</span><span class="sxs-lookup"><span data-stu-id="31952-119">-Id</span></span>
<span data-ttu-id="31952-120">ID di un cluster Kubernetes gestito</span><span class="sxs-lookup"><span data-stu-id="31952-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="31952-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31952-121">-InputObject</span></span>
<span data-ttu-id="31952-122">Un oggetto PSKubernetesCluster, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="31952-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="31952-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="31952-123">-Name</span></span>
<span data-ttu-id="31952-124">Nome del cluster di Kubernetes gestito</span><span class="sxs-lookup"><span data-stu-id="31952-124">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="31952-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="31952-125">-PassThru</span></span>
<span data-ttu-id="31952-126">Restituisce vero se l'eliminazione è riuscita</span><span class="sxs-lookup"><span data-stu-id="31952-126">Returns true if deletion is successful</span></span>

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

### <span data-ttu-id="31952-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31952-127">-ResourceGroupName</span></span>
<span data-ttu-id="31952-128">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="31952-128">Resource group name</span></span>

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

### <span data-ttu-id="31952-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="31952-129">-Confirm</span></span>
<span data-ttu-id="31952-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31952-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31952-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31952-131">-WhatIf</span></span>
<span data-ttu-id="31952-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="31952-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31952-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="31952-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31952-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31952-134">CommonParameters</span></span>
<span data-ttu-id="31952-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31952-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31952-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="31952-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31952-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="31952-137">INPUTS</span></span>

### <span data-ttu-id="31952-138">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="31952-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="31952-139">System. String</span><span class="sxs-lookup"><span data-stu-id="31952-139">System.String</span></span>

## <span data-ttu-id="31952-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="31952-140">OUTPUTS</span></span>

### <span data-ttu-id="31952-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="31952-141">System.Boolean</span></span>

## <span data-ttu-id="31952-142">Note</span><span class="sxs-lookup"><span data-stu-id="31952-142">NOTES</span></span>

## <span data-ttu-id="31952-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="31952-143">RELATED LINKS</span></span>
