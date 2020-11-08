---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorWafPolicy.md
ms.openlocfilehash: ec68316ecac3921f37641b83f45b9bd922e90b46
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018665"
---
# <span data-ttu-id="70e7b-101">Remove-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="70e7b-101">Remove-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="70e7b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="70e7b-102">SYNOPSIS</span></span>
<span data-ttu-id="70e7b-103">Rimuovere i criteri di WAF</span><span class="sxs-lookup"><span data-stu-id="70e7b-103">Remove WAF policy</span></span>

## <span data-ttu-id="70e7b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="70e7b-104">SYNTAX</span></span>

### <span data-ttu-id="70e7b-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="70e7b-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70e7b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="70e7b-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoorWafPolicy -InputObject <PSPolicy> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70e7b-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="70e7b-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoorWafPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70e7b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="70e7b-108">DESCRIPTION</span></span>
<span data-ttu-id="70e7b-109">Il cmdlet **Remove-AzFrontDoorWafPolicy** rimuove un criterio WAF sotto la sottoscrizione corrente</span><span class="sxs-lookup"><span data-stu-id="70e7b-109">The **Remove-AzFrontDoorWafPolicy** cmdlet removes a WAF policy under the current subscription</span></span>

## <span data-ttu-id="70e7b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="70e7b-110">EXAMPLES</span></span>

### <span data-ttu-id="70e7b-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="70e7b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName
```

<span data-ttu-id="70e7b-112">Rimuovere i criteri di WAF denominati $policyName in $resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="70e7b-112">Remove the WAF policy called $policyName in $resourceGroupName.</span></span>

### <span data-ttu-id="70e7b-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="70e7b-113">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName | Remove-AzFrontDoorWafPolicy
```

<span data-ttu-id="70e7b-114">Rimuovere tutti i criteri di WAF in $resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="70e7b-114">Remove all WAF policy in $resourceGroupName.</span></span>

## <span data-ttu-id="70e7b-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="70e7b-115">PARAMETERS</span></span>

### <span data-ttu-id="70e7b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70e7b-116">-DefaultProfile</span></span>
<span data-ttu-id="70e7b-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="70e7b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70e7b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70e7b-118">-InputObject</span></span>
<span data-ttu-id="70e7b-119">Oggetto Criteri WAF da eliminare.</span><span class="sxs-lookup"><span data-stu-id="70e7b-119">The WAF policy object to delete.</span></span>

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

### <span data-ttu-id="70e7b-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="70e7b-120">-Name</span></span>
<span data-ttu-id="70e7b-121">Il nome del criterio WAF da eliminare.</span><span class="sxs-lookup"><span data-stu-id="70e7b-121">The name of the WAF policy to delete.</span></span>

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

### <span data-ttu-id="70e7b-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="70e7b-122">-PassThru</span></span>
<span data-ttu-id="70e7b-123">Oggetto return (se specificato).</span><span class="sxs-lookup"><span data-stu-id="70e7b-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="70e7b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70e7b-124">-ResourceGroupName</span></span>
<span data-ttu-id="70e7b-125">Il gruppo di risorse a cui appartiene il criterio WAF.</span><span class="sxs-lookup"><span data-stu-id="70e7b-125">The resource group to which the WAF policy belongs.</span></span>

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

### <span data-ttu-id="70e7b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70e7b-126">-ResourceId</span></span>
<span data-ttu-id="70e7b-127">ID risorsa dei criteri di WAF da eliminare</span><span class="sxs-lookup"><span data-stu-id="70e7b-127">Resource Id of the WAF policy to delete</span></span>

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

### <span data-ttu-id="70e7b-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="70e7b-128">-Confirm</span></span>
<span data-ttu-id="70e7b-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70e7b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70e7b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70e7b-130">-WhatIf</span></span>
<span data-ttu-id="70e7b-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="70e7b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70e7b-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="70e7b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70e7b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70e7b-133">CommonParameters</span></span>
<span data-ttu-id="70e7b-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70e7b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70e7b-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="70e7b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70e7b-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="70e7b-136">INPUTS</span></span>

### <span data-ttu-id="70e7b-137">Microsoft. Azure. Commands. FrontDoor. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="70e7b-137">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="70e7b-138">System. String</span><span class="sxs-lookup"><span data-stu-id="70e7b-138">System.String</span></span>

## <span data-ttu-id="70e7b-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="70e7b-139">OUTPUTS</span></span>

### <span data-ttu-id="70e7b-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="70e7b-140">System.Boolean</span></span>

## <span data-ttu-id="70e7b-141">Note</span><span class="sxs-lookup"><span data-stu-id="70e7b-141">NOTES</span></span>

## <span data-ttu-id="70e7b-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="70e7b-142">RELATED LINKS</span></span>

<span data-ttu-id="70e7b-143">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="70e7b-143">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)</span></span>
