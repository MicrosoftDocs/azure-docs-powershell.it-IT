---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHost.md
ms.openlocfilehash: 21c623187e72406d1120e225bf567a48bb2e6f30
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983310"
---
# <span data-ttu-id="ace56-101">Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="ace56-101">Remove-AzHost</span></span>

## <span data-ttu-id="ace56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ace56-102">SYNOPSIS</span></span>
<span data-ttu-id="ace56-103">Rimuove un host.</span><span class="sxs-lookup"><span data-stu-id="ace56-103">Removes a host.</span></span>

## <span data-ttu-id="ace56-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ace56-104">SYNTAX</span></span>

### <span data-ttu-id="ace56-105">DefaultParameter (Default)</span><span class="sxs-lookup"><span data-stu-id="ace56-105">DefaultParameter (Default)</span></span>
```
Remove-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ace56-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="ace56-106">ResourceIdParameter</span></span>
```
Remove-AzHost [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ace56-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="ace56-107">ObjectParameter</span></span>
```
Remove-AzHost [-InputObject] <PSHost> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ace56-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ace56-108">DESCRIPTION</span></span>
<span data-ttu-id="ace56-109">Questo cmdlet eliminerà un host</span><span class="sxs-lookup"><span data-stu-id="ace56-109">This cmdlet will delete a Host</span></span>

## <span data-ttu-id="ace56-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ace56-110">EXAMPLES</span></span>

### <span data-ttu-id="ace56-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ace56-111">Example 1</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName | Remove-AzHost
```

<span data-ttu-id="ace56-112">Questo comando recupera e rimuove l'host specificato.</span><span class="sxs-lookup"><span data-stu-id="ace56-112">This command gets and removes the given host.</span></span>

### <span data-ttu-id="ace56-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ace56-113">Example 2</span></span>
```
PS C:\> Remove-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName
```

<span data-ttu-id="ace56-114">Questo comando rimuove l'host specificato.</span><span class="sxs-lookup"><span data-stu-id="ace56-114">This command removes the given host.</span></span>

## <span data-ttu-id="ace56-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ace56-115">PARAMETERS</span></span>

### <span data-ttu-id="ace56-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ace56-116">-AsJob</span></span>
<span data-ttu-id="ace56-117">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ace56-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ace56-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ace56-118">-DefaultProfile</span></span>
<span data-ttu-id="ace56-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ace56-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ace56-120">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="ace56-120">-HostGroupName</span></span>
<span data-ttu-id="ace56-121">Nome del gruppo host.</span><span class="sxs-lookup"><span data-stu-id="ace56-121">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ace56-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ace56-122">-InputObject</span></span>
<span data-ttu-id="ace56-123">Oggetto locale dell'host.</span><span class="sxs-lookup"><span data-stu-id="ace56-123">The local object of the host.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSHost
Parameter Sets: ObjectParameter
Aliases: Host

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ace56-124">-Name</span><span class="sxs-lookup"><span data-stu-id="ace56-124">-Name</span></span>
<span data-ttu-id="ace56-125">Nome dell'host.</span><span class="sxs-lookup"><span data-stu-id="ace56-125">The name of the host.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ace56-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ace56-126">-ResourceGroupName</span></span>
<span data-ttu-id="ace56-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ace56-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="ace56-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ace56-128">-ResourceId</span></span>
<span data-ttu-id="ace56-129">ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="ace56-129">The ID of the resource.</span></span>

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

### <span data-ttu-id="ace56-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ace56-130">-Confirm</span></span>
<span data-ttu-id="ace56-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ace56-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ace56-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ace56-132">-WhatIf</span></span>
<span data-ttu-id="ace56-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ace56-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ace56-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ace56-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ace56-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ace56-135">CommonParameters</span></span>
<span data-ttu-id="ace56-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ace56-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ace56-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ace56-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ace56-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="ace56-138">INPUTS</span></span>

### <span data-ttu-id="ace56-139">System.String</span><span class="sxs-lookup"><span data-stu-id="ace56-139">System.String</span></span>

### <span data-ttu-id="ace56-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span><span class="sxs-lookup"><span data-stu-id="ace56-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="ace56-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ace56-141">OUTPUTS</span></span>

### <span data-ttu-id="ace56-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="ace56-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="ace56-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="ace56-143">NOTES</span></span>

## <span data-ttu-id="ace56-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ace56-144">RELATED LINKS</span></span>
