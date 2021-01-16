---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azbastion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzBastion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzBastion.md
ms.openlocfilehash: 8030b0efbac800add6914d4da67821e35168f2de
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385290"
---
# <span data-ttu-id="216c7-101">Remove-AzBastion</span><span class="sxs-lookup"><span data-stu-id="216c7-101">Remove-AzBastion</span></span>

## <span data-ttu-id="216c7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="216c7-102">SYNOPSIS</span></span>
<span data-ttu-id="216c7-103">Rimuove una risorsa Bastion.</span><span class="sxs-lookup"><span data-stu-id="216c7-103">Removes a bastion resource.</span></span>

## <span data-ttu-id="216c7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="216c7-104">SYNTAX</span></span>

### <span data-ttu-id="216c7-105">ByResourceGroupName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="216c7-105">ByResourceGroupName (Default)</span></span>
```
Remove-AzBastion -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="216c7-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="216c7-106">ByInputObject</span></span>
```
Remove-AzBastion -InputObject <PSBastion> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="216c7-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="216c7-107">ByResourceId</span></span>
```
Remove-AzBastion -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="216c7-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="216c7-108">DESCRIPTION</span></span>
<span data-ttu-id="216c7-109">Rimuove una risorsa Bastion. Esempio1 Elimina il Bastion usando il relativo ResourceGroupName e il resourceName.</span><span class="sxs-lookup"><span data-stu-id="216c7-109">Removes a bastion resource.Example1 deletes the bastion using its ResourceGroupName and ResourceName.</span></span> <span data-ttu-id="216c7-110">Example2 Elimina il bastione usando il relativo oggetto con pipeline.</span><span class="sxs-lookup"><span data-stu-id="216c7-110">Example2 deletes the bastion using its object with pipeline.</span></span> <span data-ttu-id="216c7-111">Example3 Elimina il bastione usando il relativo oggetto.</span><span class="sxs-lookup"><span data-stu-id="216c7-111">Example3 deletes the bastion using its object.</span></span>

## <span data-ttu-id="216c7-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="216c7-112">EXAMPLES</span></span>

### <span data-ttu-id="216c7-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="216c7-113">Example 1</span></span>
```powershell
Remove-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion2"
```

### <span data-ttu-id="216c7-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="216c7-114">Example 2</span></span>
```powershell
Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion" | Remove-AzBastion
 ```

### <span data-ttu-id="216c7-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="216c7-115">Example 3</span></span>
```powershell
$bastion = Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion"
Remove-AzBastion -InputObject $bastion
 ```

## <span data-ttu-id="216c7-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="216c7-116">PARAMETERS</span></span>

### <span data-ttu-id="216c7-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="216c7-117">-Confirm</span></span>
<span data-ttu-id="216c7-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="216c7-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="216c7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="216c7-119">-DefaultProfile</span></span>
<span data-ttu-id="216c7-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="216c7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="216c7-121">-Force</span><span class="sxs-lookup"><span data-stu-id="216c7-121">-Force</span></span>
<span data-ttu-id="216c7-122">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="216c7-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="216c7-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="216c7-123">-InputObject</span></span>
<span data-ttu-id="216c7-124">Oggetto Bastion da eliminare.</span><span class="sxs-lookup"><span data-stu-id="216c7-124">The Bastion object to be deleted.</span></span>

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

### <span data-ttu-id="216c7-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="216c7-125">-Name</span></span>
<span data-ttu-id="216c7-126">Il nome della risorsa Bastion da eliminare.</span><span class="sxs-lookup"><span data-stu-id="216c7-126">The bastion resource name to be deleted.</span></span>

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

### <span data-ttu-id="216c7-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="216c7-127">-PassThru</span></span>
<span data-ttu-id="216c7-128">Restituisce un oggetto che rappresenta l'elemento in cui viene eseguita l'operazione.</span><span class="sxs-lookup"><span data-stu-id="216c7-128">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="216c7-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="216c7-129">-ResourceGroupName</span></span>
<span data-ttu-id="216c7-130">Il nome del gruppo di risorse in cui esiste Bastion.</span><span class="sxs-lookup"><span data-stu-id="216c7-130">The resource group name where bastion exists.</span></span>

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

### <span data-ttu-id="216c7-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="216c7-131">-ResourceId</span></span>
<span data-ttu-id="216c7-132">ID risorsa Azure per il Bastion da eliminare.</span><span class="sxs-lookup"><span data-stu-id="216c7-132">The Azure resource ID for the Bastion to be deleted.</span></span>

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

### <span data-ttu-id="216c7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="216c7-133">-WhatIf</span></span>
<span data-ttu-id="216c7-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="216c7-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="216c7-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="216c7-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="216c7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="216c7-136">CommonParameters</span></span>
<span data-ttu-id="216c7-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="216c7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="216c7-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="216c7-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="216c7-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="216c7-139">INPUTS</span></span>

### <span data-ttu-id="216c7-140">Microsoft. Azure. Commands. Network. Models. PSBastion</span><span class="sxs-lookup"><span data-stu-id="216c7-140">Microsoft.Azure.Commands.Network.Models.PSBastion</span></span>

### <span data-ttu-id="216c7-141">System. String</span><span class="sxs-lookup"><span data-stu-id="216c7-141">System.String</span></span>

## <span data-ttu-id="216c7-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="216c7-142">OUTPUTS</span></span>

### <span data-ttu-id="216c7-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="216c7-143">System.Boolean</span></span>

## <span data-ttu-id="216c7-144">Note</span><span class="sxs-lookup"><span data-stu-id="216c7-144">NOTES</span></span>

## <span data-ttu-id="216c7-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="216c7-145">RELATED LINKS</span></span>
[<span data-ttu-id="216c7-146">Get-AzBastion</span><span class="sxs-lookup"><span data-stu-id="216c7-146">Get-AzBastion</span></span>](./Get-AzBastion.md)

[<span data-ttu-id="216c7-147">New-AzBastion</span><span class="sxs-lookup"><span data-stu-id="216c7-147">New-AzBastion</span></span>](./New-AzBastion.md)