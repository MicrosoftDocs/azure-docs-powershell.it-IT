---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/remove-azaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAks.md
ms.openlocfilehash: 25a138b326a2fc086138f25a3d85f5182ba027fb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019178"
---
# <span data-ttu-id="17259-101">Remove-AzAks</span><span class="sxs-lookup"><span data-stu-id="17259-101">Remove-AzAks</span></span>

## <span data-ttu-id="17259-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="17259-102">SYNOPSIS</span></span>
<span data-ttu-id="17259-103">Eliminare un cluster Kubernetes gestito.</span><span class="sxs-lookup"><span data-stu-id="17259-103">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="17259-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="17259-104">SYNTAX</span></span>

### <span data-ttu-id="17259-105">GroupNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="17259-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAks [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17259-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="17259-106">InputObjectParameterSet</span></span>
```
Remove-AzAks -InputObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17259-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="17259-107">IdParameterSet</span></span>
```
Remove-AzAks [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17259-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="17259-108">DESCRIPTION</span></span>
<span data-ttu-id="17259-109">Eliminare un cluster Kubernetes gestito.</span><span class="sxs-lookup"><span data-stu-id="17259-109">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="17259-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="17259-110">EXAMPLES</span></span>

### <span data-ttu-id="17259-111">Eliminare un cluster Kubernetes gestito esistente</span><span class="sxs-lookup"><span data-stu-id="17259-111">Delete an existing managed Kubernetes cluster</span></span>
```
PS C:\> Remove-AzAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="17259-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="17259-112">PARAMETERS</span></span>

### <span data-ttu-id="17259-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="17259-113">-AsJob</span></span>
<span data-ttu-id="17259-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="17259-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="17259-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17259-115">-DefaultProfile</span></span>
<span data-ttu-id="17259-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="17259-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17259-117">-Force</span><span class="sxs-lookup"><span data-stu-id="17259-117">-Force</span></span>
<span data-ttu-id="17259-118">Rimuovere il cluster gestito di Kubernetes senza richiesta</span><span class="sxs-lookup"><span data-stu-id="17259-118">Remove managed Kubernetes cluster without prompt</span></span>

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

### <span data-ttu-id="17259-119">-ID</span><span class="sxs-lookup"><span data-stu-id="17259-119">-Id</span></span>
<span data-ttu-id="17259-120">ID di un cluster Kubernetes gestito</span><span class="sxs-lookup"><span data-stu-id="17259-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="17259-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17259-121">-InputObject</span></span>
<span data-ttu-id="17259-122">Un oggetto PSKubernetesCluster, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="17259-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="17259-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="17259-123">-Name</span></span>
<span data-ttu-id="17259-124">Nome del cluster di Kubernetes gestito</span><span class="sxs-lookup"><span data-stu-id="17259-124">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="17259-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="17259-125">-PassThru</span></span>
<span data-ttu-id="17259-126">Restituisce vero se l'eliminazione è riuscita</span><span class="sxs-lookup"><span data-stu-id="17259-126">Returns true if deletion is successful</span></span>

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

### <span data-ttu-id="17259-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17259-127">-ResourceGroupName</span></span>
<span data-ttu-id="17259-128">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="17259-128">Resource group name</span></span>

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

### <span data-ttu-id="17259-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="17259-129">-Confirm</span></span>
<span data-ttu-id="17259-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17259-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17259-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17259-131">-WhatIf</span></span>
<span data-ttu-id="17259-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="17259-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17259-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="17259-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17259-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17259-134">CommonParameters</span></span>
<span data-ttu-id="17259-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17259-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17259-136">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17259-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17259-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="17259-137">INPUTS</span></span>

### <span data-ttu-id="17259-138">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="17259-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="17259-139">System. String</span><span class="sxs-lookup"><span data-stu-id="17259-139">System.String</span></span>

## <span data-ttu-id="17259-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="17259-140">OUTPUTS</span></span>

### <span data-ttu-id="17259-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="17259-141">System.Boolean</span></span>

## <span data-ttu-id="17259-142">Note</span><span class="sxs-lookup"><span data-stu-id="17259-142">NOTES</span></span>

## <span data-ttu-id="17259-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="17259-143">RELATED LINKS</span></span>
