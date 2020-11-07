---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
ms.openlocfilehash: 107881e8d9ac1f631b9a90dbf68ba096a59cefb7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675278"
---
# <span data-ttu-id="91ba8-101">Remove-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="91ba8-101">Remove-AzHostGroup</span></span>

## <span data-ttu-id="91ba8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="91ba8-102">SYNOPSIS</span></span>
<span data-ttu-id="91ba8-103">Rimuove un gruppo host.</span><span class="sxs-lookup"><span data-stu-id="91ba8-103">Removes a host group.</span></span>

## <span data-ttu-id="91ba8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="91ba8-104">SYNTAX</span></span>

### <span data-ttu-id="91ba8-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="91ba8-105">DefaultParameter (Default)</span></span>
```
Remove-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91ba8-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="91ba8-106">ResourceIdParameter</span></span>
```
Remove-AzHostGroup [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91ba8-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="91ba8-107">ObjectParameter</span></span>
```
Remove-AzHostGroup [-InputObject] <PSHostGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91ba8-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91ba8-108">DESCRIPTION</span></span>
<span data-ttu-id="91ba8-109">Questo cmdlet eliminerà un gruppo host</span><span class="sxs-lookup"><span data-stu-id="91ba8-109">This cmdlet will delete a Host group</span></span>

## <span data-ttu-id="91ba8-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="91ba8-110">EXAMPLES</span></span>

### <span data-ttu-id="91ba8-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="91ba8-111">Example 1</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName | Remove-AzHostGroup
```

<span data-ttu-id="91ba8-112">Questo comando consente di ottenere e rimuovere il gruppo host indicato.</span><span class="sxs-lookup"><span data-stu-id="91ba8-112">This command gets and removes the given host group.</span></span>

### <span data-ttu-id="91ba8-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="91ba8-113">Example 2</span></span>
```
PS C:\> Remove-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName
```

<span data-ttu-id="91ba8-114">Questo comando rimuove il gruppo host indicato.</span><span class="sxs-lookup"><span data-stu-id="91ba8-114">This command removes the given host group.</span></span>

## <span data-ttu-id="91ba8-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="91ba8-115">PARAMETERS</span></span>

### <span data-ttu-id="91ba8-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91ba8-116">-AsJob</span></span>
<span data-ttu-id="91ba8-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="91ba8-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="91ba8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91ba8-118">-DefaultProfile</span></span>
<span data-ttu-id="91ba8-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="91ba8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91ba8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="91ba8-120">-InputObject</span></span>
<span data-ttu-id="91ba8-121">Oggetto local del gruppo host.</span><span class="sxs-lookup"><span data-stu-id="91ba8-121">The local object of the host group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup
Parameter Sets: ObjectParameter
Aliases: HostGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91ba8-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="91ba8-122">-Name</span></span>
<span data-ttu-id="91ba8-123">Nome del gruppo host.</span><span class="sxs-lookup"><span data-stu-id="91ba8-123">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91ba8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91ba8-124">-ResourceGroupName</span></span>
<span data-ttu-id="91ba8-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="91ba8-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91ba8-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="91ba8-126">-ResourceId</span></span>
<span data-ttu-id="91ba8-127">ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="91ba8-127">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91ba8-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="91ba8-128">-Confirm</span></span>
<span data-ttu-id="91ba8-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91ba8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91ba8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91ba8-130">-WhatIf</span></span>
<span data-ttu-id="91ba8-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="91ba8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91ba8-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="91ba8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91ba8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91ba8-133">CommonParameters</span></span>
<span data-ttu-id="91ba8-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91ba8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91ba8-135">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="91ba8-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91ba8-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="91ba8-136">INPUTS</span></span>

### <span data-ttu-id="91ba8-137">System. String</span><span class="sxs-lookup"><span data-stu-id="91ba8-137">System.String</span></span>

### <span data-ttu-id="91ba8-138">Microsoft. Azure. Commands. Compute. Automation. Models. PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="91ba8-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="91ba8-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="91ba8-139">OUTPUTS</span></span>

### <span data-ttu-id="91ba8-140">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="91ba8-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="91ba8-141">Note</span><span class="sxs-lookup"><span data-stu-id="91ba8-141">NOTES</span></span>

## <span data-ttu-id="91ba8-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="91ba8-142">RELATED LINKS</span></span>
