---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkTap.md
ms.openlocfilehash: bfe1c586d85a44460b1adbb84942be9b556973dd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488930"
---
# <span data-ttu-id="7e033-101">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="7e033-101">Remove-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="7e033-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7e033-102">SYNOPSIS</span></span>
<span data-ttu-id="7e033-103">Consente di rimuovere un tocco di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="7e033-103">Removes a virtual network tap.</span></span>

## <span data-ttu-id="7e033-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7e033-104">SYNTAX</span></span>

### <span data-ttu-id="7e033-105">RemoveByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7e033-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e033-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e033-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzVirtualNetworkTap -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e033-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e033-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzVirtualNetworkTap -InputObject <PSVirtualNetworkTap> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e033-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e033-108">DESCRIPTION</span></span>
<span data-ttu-id="7e033-109">Il cmdlet **Remove-AzVirtualNetworkTap** rimuove un tocco di rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="7e033-109">The **Remove-AzVirtualNetworkTap** cmdlet removes an Azure virtual network tap.</span></span>

## <span data-ttu-id="7e033-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7e033-110">EXAMPLES</span></span>

### <span data-ttu-id="7e033-111">Esempio 1: rimuovere un tocco di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="7e033-111">Example 1: Remove a virtual network tap</span></span>
```
PS C:\>Remove-AzNetworkInterface -Name "VirtualNetworkTap1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="7e033-112">Questo comando rimuove il VirtualNetworkTap1 nel gruppo di risorse ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="7e033-112">This command removes the VirtualNetworkTap1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="7e033-113">Poiché il parametro *Force* non viene usato, all'utente verrà richiesto di confermare questa azione.</span><span class="sxs-lookup"><span data-stu-id="7e033-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

## <span data-ttu-id="7e033-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7e033-114">PARAMETERS</span></span>

### <span data-ttu-id="7e033-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7e033-115">-AsJob</span></span>
<span data-ttu-id="7e033-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="7e033-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7e033-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e033-117">-DefaultProfile</span></span>
<span data-ttu-id="7e033-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7e033-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e033-119">-Force</span><span class="sxs-lookup"><span data-stu-id="7e033-119">-Force</span></span>
<span data-ttu-id="7e033-120">Non chiedere conferma se si vuole eliminare una risorsa</span><span class="sxs-lookup"><span data-stu-id="7e033-120">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="7e033-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e033-121">-InputObject</span></span>
<span data-ttu-id="7e033-122">Riferimento alla risorsa VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="7e033-122">Reference to VirtualNetworkTap resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e033-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="7e033-123">-Name</span></span>
<span data-ttu-id="7e033-124">Nome del tocco.</span><span class="sxs-lookup"><span data-stu-id="7e033-124">The name of the tap.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e033-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7e033-125">-PassThru</span></span>
<span data-ttu-id="7e033-126">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="7e033-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7e033-127">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="7e033-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7e033-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e033-128">-ResourceGroupName</span></span>
<span data-ttu-id="7e033-129">Nome del gruppo di risorse del tocco di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="7e033-129">The resource group name of the virtual network tap.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e033-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7e033-130">-ResourceId</span></span>
<span data-ttu-id="7e033-131">VirtualNetworkTap resourceId</span><span class="sxs-lookup"><span data-stu-id="7e033-131">VirtualNetworkTap resourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e033-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7e033-132">-Confirm</span></span>
<span data-ttu-id="7e033-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e033-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e033-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e033-134">-WhatIf</span></span>
<span data-ttu-id="7e033-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7e033-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e033-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7e033-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e033-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e033-137">CommonParameters</span></span>
<span data-ttu-id="7e033-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e033-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e033-139">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e033-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e033-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7e033-140">INPUTS</span></span>

### <span data-ttu-id="7e033-141">System. String</span><span class="sxs-lookup"><span data-stu-id="7e033-141">System.String</span></span>

### <span data-ttu-id="7e033-142">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="7e033-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="7e033-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7e033-143">OUTPUTS</span></span>

### <span data-ttu-id="7e033-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7e033-144">System.Boolean</span></span>

## <span data-ttu-id="7e033-145">Note</span><span class="sxs-lookup"><span data-stu-id="7e033-145">NOTES</span></span>

## <span data-ttu-id="7e033-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7e033-146">RELATED LINKS</span></span>

[<span data-ttu-id="7e033-147">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="7e033-147">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="7e033-148">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="7e033-148">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="7e033-149">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="7e033-149">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)
