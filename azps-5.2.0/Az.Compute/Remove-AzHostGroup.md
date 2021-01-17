---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
ms.openlocfilehash: 17397d2bd1056b6e4280d560b2640abcacb1250a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342391"
---
# <span data-ttu-id="ab74d-101">Remove-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="ab74d-101">Remove-AzHostGroup</span></span>

## <span data-ttu-id="ab74d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ab74d-102">SYNOPSIS</span></span>
<span data-ttu-id="ab74d-103">Rimuove un gruppo host.</span><span class="sxs-lookup"><span data-stu-id="ab74d-103">Removes a host group.</span></span>

## <span data-ttu-id="ab74d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ab74d-104">SYNTAX</span></span>

### <span data-ttu-id="ab74d-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ab74d-105">DefaultParameter (Default)</span></span>
```
Remove-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab74d-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="ab74d-106">ResourceIdParameter</span></span>
```
Remove-AzHostGroup [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab74d-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="ab74d-107">ObjectParameter</span></span>
```
Remove-AzHostGroup [-InputObject] <PSHostGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab74d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab74d-108">DESCRIPTION</span></span>
<span data-ttu-id="ab74d-109">Questo cmdlet eliminerà un gruppo host</span><span class="sxs-lookup"><span data-stu-id="ab74d-109">This cmdlet will delete a Host group</span></span>

## <span data-ttu-id="ab74d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ab74d-110">EXAMPLES</span></span>

### <span data-ttu-id="ab74d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ab74d-111">Example 1</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName | Remove-AzHostGroup
```

<span data-ttu-id="ab74d-112">Questo comando consente di ottenere e rimuovere il gruppo host indicato.</span><span class="sxs-lookup"><span data-stu-id="ab74d-112">This command gets and removes the given host group.</span></span>

### <span data-ttu-id="ab74d-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ab74d-113">Example 2</span></span>
```
PS C:\> Remove-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName
```

<span data-ttu-id="ab74d-114">Questo comando rimuove il gruppo host indicato.</span><span class="sxs-lookup"><span data-stu-id="ab74d-114">This command removes the given host group.</span></span>

## <span data-ttu-id="ab74d-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ab74d-115">PARAMETERS</span></span>

### <span data-ttu-id="ab74d-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ab74d-116">-AsJob</span></span>
<span data-ttu-id="ab74d-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ab74d-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ab74d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab74d-118">-DefaultProfile</span></span>
<span data-ttu-id="ab74d-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ab74d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab74d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab74d-120">-InputObject</span></span>
<span data-ttu-id="ab74d-121">Oggetto local del gruppo host.</span><span class="sxs-lookup"><span data-stu-id="ab74d-121">The local object of the host group.</span></span>

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

### <span data-ttu-id="ab74d-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="ab74d-122">-Name</span></span>
<span data-ttu-id="ab74d-123">Nome del gruppo host.</span><span class="sxs-lookup"><span data-stu-id="ab74d-123">The name of the host group.</span></span>

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

### <span data-ttu-id="ab74d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab74d-124">-ResourceGroupName</span></span>
<span data-ttu-id="ab74d-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ab74d-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="ab74d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab74d-126">-ResourceId</span></span>
<span data-ttu-id="ab74d-127">ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="ab74d-127">The ID of the resource.</span></span>

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

### <span data-ttu-id="ab74d-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ab74d-128">-Confirm</span></span>
<span data-ttu-id="ab74d-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab74d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab74d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab74d-130">-WhatIf</span></span>
<span data-ttu-id="ab74d-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ab74d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab74d-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ab74d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab74d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab74d-133">CommonParameters</span></span>
<span data-ttu-id="ab74d-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab74d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab74d-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab74d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab74d-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ab74d-136">INPUTS</span></span>

### <span data-ttu-id="ab74d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="ab74d-137">System.String</span></span>

### <span data-ttu-id="ab74d-138">Microsoft. Azure. Commands. Compute. Automation. Models. PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="ab74d-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="ab74d-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ab74d-139">OUTPUTS</span></span>

### <span data-ttu-id="ab74d-140">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="ab74d-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="ab74d-141">Note</span><span class="sxs-lookup"><span data-stu-id="ab74d-141">NOTES</span></span>

## <span data-ttu-id="ab74d-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ab74d-142">RELATED LINKS</span></span>
