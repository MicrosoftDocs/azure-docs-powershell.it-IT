---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azbastion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzBastion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzBastion.md
ms.openlocfilehash: 8030b0efbac800add6914d4da67821e35168f2de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202588"
---
# <span data-ttu-id="67036-101">Remove-AzBastion</span><span class="sxs-lookup"><span data-stu-id="67036-101">Remove-AzBastion</span></span>

## <span data-ttu-id="67036-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67036-102">SYNOPSIS</span></span>
<span data-ttu-id="67036-103">Rimuove una risorsa di base.</span><span class="sxs-lookup"><span data-stu-id="67036-103">Removes a bastion resource.</span></span>

## <span data-ttu-id="67036-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="67036-104">SYNTAX</span></span>

### <span data-ttu-id="67036-105">ByResourceGroupName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="67036-105">ByResourceGroupName (Default)</span></span>
```
Remove-AzBastion -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67036-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="67036-106">ByInputObject</span></span>
```
Remove-AzBastion -InputObject <PSBastion> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67036-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="67036-107">ByResourceId</span></span>
```
Remove-AzBastion -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67036-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="67036-108">DESCRIPTION</span></span>
<span data-ttu-id="67036-109">Rimuove una risorsa di base. L'esempio 1 elimina il bastion usando i nomi ResourceGroupName e ResourceName.</span><span class="sxs-lookup"><span data-stu-id="67036-109">Removes a bastion resource.Example1 deletes the bastion using its ResourceGroupName and ResourceName.</span></span> <span data-ttu-id="67036-110">L'esempio 2 elimina il bastion usando il relativo oggetto con una pipeline.</span><span class="sxs-lookup"><span data-stu-id="67036-110">Example2 deletes the bastion using its object with pipeline.</span></span> <span data-ttu-id="67036-111">L'esempio 3 elimina il basto usando il relativo oggetto.</span><span class="sxs-lookup"><span data-stu-id="67036-111">Example3 deletes the bastion using its object.</span></span>

## <span data-ttu-id="67036-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="67036-112">EXAMPLES</span></span>

### <span data-ttu-id="67036-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="67036-113">Example 1</span></span>
```powershell
Remove-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion2"
```

### <span data-ttu-id="67036-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="67036-114">Example 2</span></span>
```powershell
Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion" | Remove-AzBastion
 ```

### <span data-ttu-id="67036-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="67036-115">Example 3</span></span>
```powershell
$bastion = Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion"
Remove-AzBastion -InputObject $bastion
 ```

## <span data-ttu-id="67036-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67036-116">PARAMETERS</span></span>

### <span data-ttu-id="67036-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="67036-117">-Confirm</span></span>
<span data-ttu-id="67036-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67036-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67036-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67036-119">-DefaultProfile</span></span>
<span data-ttu-id="67036-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="67036-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67036-121">-Force</span><span class="sxs-lookup"><span data-stu-id="67036-121">-Force</span></span>
<span data-ttu-id="67036-122">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="67036-122">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67036-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67036-123">-InputObject</span></span>
<span data-ttu-id="67036-124">L'oggetto Bastion da eliminare.</span><span class="sxs-lookup"><span data-stu-id="67036-124">The Bastion object to be deleted.</span></span>

```yaml
Type: PSBastion
Parameter Sets: ByInputObject
Aliases: Bastion, BastionObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67036-125">-Name</span><span class="sxs-lookup"><span data-stu-id="67036-125">-Name</span></span>
<span data-ttu-id="67036-126">Nome della risorsa di base da eliminare.</span><span class="sxs-lookup"><span data-stu-id="67036-126">The bastion resource name to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupName
Aliases: ResourceName, BastionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67036-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="67036-127">-PassThru</span></span>
<span data-ttu-id="67036-128">Restituisce un oggetto che rappresenta l'elemento su cui viene eseguita l'operazione.</span><span class="sxs-lookup"><span data-stu-id="67036-128">Returns an object representing the item on which this operation is being performed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67036-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67036-129">-ResourceGroupName</span></span>
<span data-ttu-id="67036-130">Nome del gruppo di risorse in cui è presente il bastion.</span><span class="sxs-lookup"><span data-stu-id="67036-130">The resource group name where bastion exists.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67036-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="67036-131">-ResourceId</span></span>
<span data-ttu-id="67036-132">ID della risorsa Azure per il Bastion da eliminare.</span><span class="sxs-lookup"><span data-stu-id="67036-132">The Azure resource ID for the Bastion to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: BastionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67036-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67036-133">-WhatIf</span></span>
<span data-ttu-id="67036-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="67036-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67036-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="67036-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67036-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67036-136">CommonParameters</span></span>
<span data-ttu-id="67036-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67036-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67036-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="67036-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67036-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="67036-139">INPUTS</span></span>

### <span data-ttu-id="67036-140">Microsoft.Azure.Commands.Network.Models.PSBastion</span><span class="sxs-lookup"><span data-stu-id="67036-140">Microsoft.Azure.Commands.Network.Models.PSBastion</span></span>

### <span data-ttu-id="67036-141">System.String</span><span class="sxs-lookup"><span data-stu-id="67036-141">System.String</span></span>

## <span data-ttu-id="67036-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="67036-142">OUTPUTS</span></span>

### <span data-ttu-id="67036-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="67036-143">System.Boolean</span></span>

## <span data-ttu-id="67036-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="67036-144">NOTES</span></span>

## <span data-ttu-id="67036-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="67036-145">RELATED LINKS</span></span>
[<span data-ttu-id="67036-146">Get-AzBastion</span><span class="sxs-lookup"><span data-stu-id="67036-146">Get-AzBastion</span></span>](./Get-AzBastion.md)

[<span data-ttu-id="67036-147">New-AzBastion</span><span class="sxs-lookup"><span data-stu-id="67036-147">New-AzBastion</span></span>](./New-AzBastion.md)