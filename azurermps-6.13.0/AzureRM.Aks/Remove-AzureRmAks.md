---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/remove-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Remove-AzureRmAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Remove-AzureRmAks.md
ms.openlocfilehash: 909121a78d09db7d15591a93db9479d0ccc8381b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519319"
---
# <span data-ttu-id="9c95b-101">Remove-AzureRmAks</span><span class="sxs-lookup"><span data-stu-id="9c95b-101">Remove-AzureRmAks</span></span>

## <span data-ttu-id="9c95b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9c95b-102">SYNOPSIS</span></span>
<span data-ttu-id="9c95b-103">Eliminare un cluster Kubernetes gestito.</span><span class="sxs-lookup"><span data-stu-id="9c95b-103">Delete a managed Kubernetes cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c95b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9c95b-104">SYNTAX</span></span>

### <span data-ttu-id="9c95b-105">GroupNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9c95b-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzureRmAks [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c95b-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c95b-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmAks -InputObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c95b-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c95b-107">IdParameterSet</span></span>
```
Remove-AzureRmAks [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c95b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9c95b-108">DESCRIPTION</span></span>
<span data-ttu-id="9c95b-109">Eliminare un cluster Kubernetes gestito.</span><span class="sxs-lookup"><span data-stu-id="9c95b-109">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="9c95b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9c95b-110">EXAMPLES</span></span>

### <span data-ttu-id="9c95b-111">Eliminare un cluster Kubernetes gestito esistente</span><span class="sxs-lookup"><span data-stu-id="9c95b-111">Delete an existing managed Kubernetes cluster</span></span>
```
PS C:\> Remove-AzureRmAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="9c95b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9c95b-112">PARAMETERS</span></span>

### <span data-ttu-id="9c95b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9c95b-113">-AsJob</span></span>
<span data-ttu-id="9c95b-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="9c95b-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9c95b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c95b-115">-DefaultProfile</span></span>
<span data-ttu-id="9c95b-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9c95b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c95b-117">-Force</span><span class="sxs-lookup"><span data-stu-id="9c95b-117">-Force</span></span>
<span data-ttu-id="9c95b-118">Rimuovere il cluster gestito di Kubernetes senza richiesta</span><span class="sxs-lookup"><span data-stu-id="9c95b-118">Remove managed Kubernetes cluster without prompt</span></span>

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

### <span data-ttu-id="9c95b-119">-ID</span><span class="sxs-lookup"><span data-stu-id="9c95b-119">-Id</span></span>
<span data-ttu-id="9c95b-120">ID di un cluster Kubernetes gestito</span><span class="sxs-lookup"><span data-stu-id="9c95b-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="9c95b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c95b-121">-InputObject</span></span>
<span data-ttu-id="9c95b-122">Un oggetto PSKubernetesCluster, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="9c95b-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="9c95b-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="9c95b-123">-Name</span></span>
<span data-ttu-id="9c95b-124">Nome del cluster di Kubernetes gestito</span><span class="sxs-lookup"><span data-stu-id="9c95b-124">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="9c95b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c95b-125">-PassThru</span></span>
<span data-ttu-id="9c95b-126">Restituisce vero se l'eliminazione è riuscita</span><span class="sxs-lookup"><span data-stu-id="9c95b-126">Returns true if deletion is successful</span></span>

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

### <span data-ttu-id="9c95b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c95b-127">-ResourceGroupName</span></span>
<span data-ttu-id="9c95b-128">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="9c95b-128">Resource group name</span></span>

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

### <span data-ttu-id="9c95b-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9c95b-129">-Confirm</span></span>
<span data-ttu-id="9c95b-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c95b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c95b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c95b-131">-WhatIf</span></span>
<span data-ttu-id="9c95b-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9c95b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c95b-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9c95b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c95b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c95b-134">CommonParameters</span></span>
<span data-ttu-id="9c95b-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c95b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c95b-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c95b-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c95b-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9c95b-137">INPUTS</span></span>

### <span data-ttu-id="9c95b-138">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="9c95b-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>
<span data-ttu-id="9c95b-139">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9c95b-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="9c95b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="9c95b-140">System.String</span></span>

## <span data-ttu-id="9c95b-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9c95b-141">OUTPUTS</span></span>

### <span data-ttu-id="9c95b-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9c95b-142">System.Boolean</span></span>

## <span data-ttu-id="9c95b-143">Note</span><span class="sxs-lookup"><span data-stu-id="9c95b-143">NOTES</span></span>

## <span data-ttu-id="9c95b-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9c95b-144">RELATED LINKS</span></span>
