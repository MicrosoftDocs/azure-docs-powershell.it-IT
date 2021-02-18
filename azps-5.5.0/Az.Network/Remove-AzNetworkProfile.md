---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkProfile.md
ms.openlocfilehash: 3a83b7200f7634574fd457d2fa08f926a62b9a82
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206595"
---
# <span data-ttu-id="1cd1a-101">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="1cd1a-101">Remove-AzNetworkProfile</span></span>

## <span data-ttu-id="1cd1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1cd1a-102">SYNOPSIS</span></span>
<span data-ttu-id="1cd1a-103">Rimuove un profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="1cd1a-103">Removes a network profile.</span></span>

## <span data-ttu-id="1cd1a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1cd1a-104">SYNTAX</span></span>

### <span data-ttu-id="1cd1a-105">RemoveByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1cd1a-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzNetworkProfile -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cd1a-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cd1a-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzNetworkProfile -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cd1a-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cd1a-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzNetworkProfile -InputObject <PSNetworkProfile> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cd1a-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1cd1a-108">DESCRIPTION</span></span>
<span data-ttu-id="1cd1a-109">Il cmdlet **Remove-AzNetworkProfile** rimuove un profilo di rete se non sono state create interfacce di rete dei contenitori, a differenza di una configurazione dell'interfaccia di rete dei contenitori.</span><span class="sxs-lookup"><span data-stu-id="1cd1a-109">The **Remove-AzNetworkProfile** cmdlet removes a network profile if no container network interfaces (as contrasted to a container network interface **configuration**) have been created.</span></span>

## <span data-ttu-id="1cd1a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1cd1a-110">EXAMPLES</span></span>

### <span data-ttu-id="1cd1a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1cd1a-111">Example 1</span></span>
```powershell
Remove-AzNetworkProfile -Name np1 -ResourceGroupName rg1
```

<span data-ttu-id="1cd1a-112">Verrà rimosso il profilo di rete con nome np1 dal gruppo di risorse rg1.</span><span class="sxs-lookup"><span data-stu-id="1cd1a-112">This removes the network profile with name np1 from the resource group rg1.</span></span>

## <span data-ttu-id="1cd1a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1cd1a-113">PARAMETERS</span></span>

### <span data-ttu-id="1cd1a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1cd1a-114">-AsJob</span></span>
<span data-ttu-id="1cd1a-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="1cd1a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1cd1a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cd1a-116">-DefaultProfile</span></span>
<span data-ttu-id="1cd1a-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1cd1a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1cd1a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="1cd1a-118">-Force</span></span>
<span data-ttu-id="1cd1a-119">Non chiedere conferma se si vuole eliminare una risorsa</span><span class="sxs-lookup"><span data-stu-id="1cd1a-119">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="1cd1a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1cd1a-120">-InputObject</span></span>
<span data-ttu-id="1cd1a-121">Oggetto profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="1cd1a-121">Network profile object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkProfile
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1cd1a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="1cd1a-122">-Name</span></span>
<span data-ttu-id="1cd1a-123">Nome del profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="1cd1a-123">The name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cd1a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1cd1a-124">-PassThru</span></span>
<span data-ttu-id="1cd1a-125">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="1cd1a-125">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="1cd1a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cd1a-126">-ResourceGroupName</span></span>
<span data-ttu-id="1cd1a-127">Nome del gruppo di risorse del profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="1cd1a-127">The resource group name of the network profile.</span></span>

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

### <span data-ttu-id="1cd1a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1cd1a-128">-ResourceId</span></span>
<span data-ttu-id="1cd1a-129">ID risorsa di Gestione risorse di Azure del profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="1cd1a-129">The Azure resource manager resource ID of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cd1a-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1cd1a-130">-Confirm</span></span>
<span data-ttu-id="1cd1a-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1cd1a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cd1a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cd1a-132">-WhatIf</span></span>
<span data-ttu-id="1cd1a-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1cd1a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cd1a-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1cd1a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cd1a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cd1a-135">CommonParameters</span></span>
<span data-ttu-id="1cd1a-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cd1a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cd1a-137">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cd1a-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cd1a-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="1cd1a-138">INPUTS</span></span>

### <span data-ttu-id="1cd1a-139">System.String</span><span class="sxs-lookup"><span data-stu-id="1cd1a-139">System.String</span></span>

### <span data-ttu-id="1cd1a-140">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="1cd1a-140">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="1cd1a-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1cd1a-141">OUTPUTS</span></span>

### <span data-ttu-id="1cd1a-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1cd1a-142">System.Boolean</span></span>

## <span data-ttu-id="1cd1a-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="1cd1a-143">NOTES</span></span>

## <span data-ttu-id="1cd1a-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1cd1a-144">RELATED LINKS</span></span>

[<span data-ttu-id="1cd1a-145">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="1cd1a-145">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="1cd1a-146">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="1cd1a-146">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="1cd1a-147">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="1cd1a-147">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)
