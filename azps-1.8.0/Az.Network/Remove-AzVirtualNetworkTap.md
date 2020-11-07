---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkTap.md
ms.openlocfilehash: 3883b8dd41f3070e74d16fb8382ed73cc75ce4eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678052"
---
# <span data-ttu-id="51206-101">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="51206-101">Remove-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="51206-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="51206-102">SYNOPSIS</span></span>
<span data-ttu-id="51206-103">Consente di rimuovere un tocco di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="51206-103">Removes a virtual network tap.</span></span>

## <span data-ttu-id="51206-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="51206-104">SYNTAX</span></span>

### <span data-ttu-id="51206-105">RemoveByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="51206-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51206-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="51206-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzVirtualNetworkTap -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51206-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="51206-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzVirtualNetworkTap -InputObject <PSVirtualNetworkTap> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51206-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="51206-108">DESCRIPTION</span></span>
<span data-ttu-id="51206-109">Il cmdlet **Remove-AzVirtualNetworkTap** rimuove un tocco di rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="51206-109">The **Remove-AzVirtualNetworkTap** cmdlet removes an Azure virtual network tap.</span></span>

## <span data-ttu-id="51206-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="51206-110">EXAMPLES</span></span>

### <span data-ttu-id="51206-111">Esempio 1: rimuovere un tocco di rete virtuak</span><span class="sxs-lookup"><span data-stu-id="51206-111">Example 1: Remove a virtuak network tap</span></span>
```
PS C:\>Remove-AzNetworkInterface -Name "VirtualNetworkTap1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="51206-112">Questo comando rimuove il VirtualNetworkTap1 nel gruppo di risorse ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="51206-112">This command removes the VirtualNetworkTap1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="51206-113">Poiché il parametro *Force* non viene usato, all'utente verrà richiesto di confermare questa azione.</span><span class="sxs-lookup"><span data-stu-id="51206-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

## <span data-ttu-id="51206-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="51206-114">PARAMETERS</span></span>

### <span data-ttu-id="51206-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="51206-115">-AsJob</span></span>
<span data-ttu-id="51206-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="51206-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="51206-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51206-117">-DefaultProfile</span></span>
<span data-ttu-id="51206-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="51206-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51206-119">-Force</span><span class="sxs-lookup"><span data-stu-id="51206-119">-Force</span></span>
<span data-ttu-id="51206-120">Non chiedere conferma se si vuole eliminare una risorsa</span><span class="sxs-lookup"><span data-stu-id="51206-120">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="51206-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51206-121">-InputObject</span></span>
<span data-ttu-id="51206-122">Riferimento alla risorsa VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="51206-122">Reference to VirtualNetworkTap resource</span></span>

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

### <span data-ttu-id="51206-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="51206-123">-Name</span></span>
<span data-ttu-id="51206-124">Nome del tocco.</span><span class="sxs-lookup"><span data-stu-id="51206-124">The name of the tap.</span></span>

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

### <span data-ttu-id="51206-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="51206-125">-PassThru</span></span>
<span data-ttu-id="51206-126">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="51206-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="51206-127">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="51206-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="51206-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51206-128">-ResourceGroupName</span></span>
<span data-ttu-id="51206-129">Nome del gruppo di risorse del tocco di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="51206-129">The resource group name of the virtual network tap.</span></span>

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

### <span data-ttu-id="51206-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51206-130">-ResourceId</span></span>
<span data-ttu-id="51206-131">VirtualNetworkTap resourceId</span><span class="sxs-lookup"><span data-stu-id="51206-131">VirtualNetworkTap resourceId</span></span>

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

### <span data-ttu-id="51206-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="51206-132">-Confirm</span></span>
<span data-ttu-id="51206-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51206-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51206-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51206-134">-WhatIf</span></span>
<span data-ttu-id="51206-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="51206-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51206-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="51206-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51206-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51206-137">CommonParameters</span></span>
<span data-ttu-id="51206-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51206-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51206-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51206-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51206-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="51206-140">INPUTS</span></span>

### <span data-ttu-id="51206-141">System. String</span><span class="sxs-lookup"><span data-stu-id="51206-141">System.String</span></span>

### <span data-ttu-id="51206-142">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="51206-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="51206-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="51206-143">OUTPUTS</span></span>

### <span data-ttu-id="51206-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="51206-144">System.Boolean</span></span>

## <span data-ttu-id="51206-145">Note</span><span class="sxs-lookup"><span data-stu-id="51206-145">NOTES</span></span>

## <span data-ttu-id="51206-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="51206-146">RELATED LINKS</span></span>

[<span data-ttu-id="51206-147">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="51206-147">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="51206-148">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="51206-148">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="51206-149">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="51206-149">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)
