---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorWafPolicy.md
ms.openlocfilehash: ec68316ecac3921f37641b83f45b9bd922e90b46
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185918"
---
# <span data-ttu-id="219e8-101">Remove-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="219e8-101">Remove-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="219e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="219e8-102">SYNOPSIS</span></span>
<span data-ttu-id="219e8-103">Rimuovere i criteri WAF</span><span class="sxs-lookup"><span data-stu-id="219e8-103">Remove WAF policy</span></span>

## <span data-ttu-id="219e8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="219e8-104">SYNTAX</span></span>

### <span data-ttu-id="219e8-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="219e8-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="219e8-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="219e8-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoorWafPolicy -InputObject <PSPolicy> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="219e8-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="219e8-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoorWafPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="219e8-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="219e8-108">DESCRIPTION</span></span>
<span data-ttu-id="219e8-109">Il cmdlet **Remove-AzFrontDoorWafPolicy** rimuove un criterio WAF nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="219e8-109">The **Remove-AzFrontDoorWafPolicy** cmdlet removes a WAF policy under the current subscription</span></span>

## <span data-ttu-id="219e8-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="219e8-110">EXAMPLES</span></span>

### <span data-ttu-id="219e8-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="219e8-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName
```

<span data-ttu-id="219e8-112">Rimuovere i criteri WAF denominati $policyName in $resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="219e8-112">Remove the WAF policy called $policyName in $resourceGroupName.</span></span>

### <span data-ttu-id="219e8-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="219e8-113">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName | Remove-AzFrontDoorWafPolicy
```

<span data-ttu-id="219e8-114">Rimuovere tutti i criteri WAF in $resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="219e8-114">Remove all WAF policy in $resourceGroupName.</span></span>

## <span data-ttu-id="219e8-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="219e8-115">PARAMETERS</span></span>

### <span data-ttu-id="219e8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="219e8-116">-DefaultProfile</span></span>
<span data-ttu-id="219e8-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="219e8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="219e8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="219e8-118">-InputObject</span></span>
<span data-ttu-id="219e8-119">Oggetto criterio WAF da eliminare.</span><span class="sxs-lookup"><span data-stu-id="219e8-119">The WAF policy object to delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="219e8-120">-Name</span><span class="sxs-lookup"><span data-stu-id="219e8-120">-Name</span></span>
<span data-ttu-id="219e8-121">Nome dei criteri WAF da eliminare.</span><span class="sxs-lookup"><span data-stu-id="219e8-121">The name of the WAF policy to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="219e8-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="219e8-122">-PassThru</span></span>
<span data-ttu-id="219e8-123">Oggetto restituito (se specificato).</span><span class="sxs-lookup"><span data-stu-id="219e8-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="219e8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="219e8-124">-ResourceGroupName</span></span>
<span data-ttu-id="219e8-125">Gruppo di risorse a cui appartengono i criteri WAF.</span><span class="sxs-lookup"><span data-stu-id="219e8-125">The resource group to which the WAF policy belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="219e8-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="219e8-126">-ResourceId</span></span>
<span data-ttu-id="219e8-127">ID risorsa dei criteri WAF da eliminare</span><span class="sxs-lookup"><span data-stu-id="219e8-127">Resource Id of the WAF policy to delete</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="219e8-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="219e8-128">-Confirm</span></span>
<span data-ttu-id="219e8-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="219e8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="219e8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="219e8-130">-WhatIf</span></span>
<span data-ttu-id="219e8-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="219e8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="219e8-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="219e8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="219e8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="219e8-133">CommonParameters</span></span>
<span data-ttu-id="219e8-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="219e8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="219e8-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="219e8-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="219e8-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="219e8-136">INPUTS</span></span>

### <span data-ttu-id="219e8-137">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="219e8-137">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="219e8-138">System.String</span><span class="sxs-lookup"><span data-stu-id="219e8-138">System.String</span></span>

## <span data-ttu-id="219e8-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="219e8-139">OUTPUTS</span></span>

### <span data-ttu-id="219e8-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="219e8-140">System.Boolean</span></span>

## <span data-ttu-id="219e8-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="219e8-141">NOTES</span></span>

## <span data-ttu-id="219e8-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="219e8-142">RELATED LINKS</span></span>

<span data-ttu-id="219e8-143">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="219e8-143">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)</span></span>
