---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkProfile.md
ms.openlocfilehash: 3a83b7200f7634574fd457d2fa08f926a62b9a82
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370954"
---
# <span data-ttu-id="dd5df-101">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="dd5df-101">Remove-AzNetworkProfile</span></span>

## <span data-ttu-id="dd5df-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dd5df-102">SYNOPSIS</span></span>
<span data-ttu-id="dd5df-103">Rimuove un profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="dd5df-103">Removes a network profile.</span></span>

## <span data-ttu-id="dd5df-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dd5df-104">SYNTAX</span></span>

### <span data-ttu-id="dd5df-105">RemoveByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dd5df-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzNetworkProfile -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd5df-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd5df-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzNetworkProfile -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd5df-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd5df-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzNetworkProfile -InputObject <PSNetworkProfile> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd5df-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dd5df-108">DESCRIPTION</span></span>
<span data-ttu-id="dd5df-109">Il cmdlet **Remove-AzNetworkProfile** rimuove un profilo di rete se non sono state create interfacce di rete di contenitori (in contrapposizione a una **configurazione** di interfaccia di rete contenitore).</span><span class="sxs-lookup"><span data-stu-id="dd5df-109">The **Remove-AzNetworkProfile** cmdlet removes a network profile if no container network interfaces (as contrasted to a container network interface **configuration**) have been created.</span></span>

## <span data-ttu-id="dd5df-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dd5df-110">EXAMPLES</span></span>

### <span data-ttu-id="dd5df-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="dd5df-111">Example 1</span></span>
```powershell
Remove-AzNetworkProfile -Name np1 -ResourceGroupName rg1
```

<span data-ttu-id="dd5df-112">In questo articolo viene rimosso il profilo di rete con il nome NP1 dal gruppo di risorse RG1.</span><span class="sxs-lookup"><span data-stu-id="dd5df-112">This removes the network profile with name np1 from the resource group rg1.</span></span>

## <span data-ttu-id="dd5df-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dd5df-113">PARAMETERS</span></span>

### <span data-ttu-id="dd5df-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd5df-114">-AsJob</span></span>
<span data-ttu-id="dd5df-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="dd5df-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dd5df-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd5df-116">-DefaultProfile</span></span>
<span data-ttu-id="dd5df-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dd5df-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd5df-118">-Force</span><span class="sxs-lookup"><span data-stu-id="dd5df-118">-Force</span></span>
<span data-ttu-id="dd5df-119">Non chiedere conferma se si vuole eliminare una risorsa</span><span class="sxs-lookup"><span data-stu-id="dd5df-119">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="dd5df-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd5df-120">-InputObject</span></span>
<span data-ttu-id="dd5df-121">Oggetto profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="dd5df-121">Network profile object.</span></span>

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

### <span data-ttu-id="dd5df-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="dd5df-122">-Name</span></span>
<span data-ttu-id="dd5df-123">Nome del profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="dd5df-123">The name of the network profile.</span></span>

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

### <span data-ttu-id="dd5df-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd5df-124">-PassThru</span></span>
<span data-ttu-id="dd5df-125">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="dd5df-125">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="dd5df-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd5df-126">-ResourceGroupName</span></span>
<span data-ttu-id="dd5df-127">Nome del gruppo di risorse del profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="dd5df-127">The resource group name of the network profile.</span></span>

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

### <span data-ttu-id="dd5df-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd5df-128">-ResourceId</span></span>
<span data-ttu-id="dd5df-129">ID risorsa di Azure Resource Manager del profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="dd5df-129">The Azure resource manager resource ID of the network profile.</span></span>

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

### <span data-ttu-id="dd5df-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dd5df-130">-Confirm</span></span>
<span data-ttu-id="dd5df-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd5df-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd5df-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd5df-132">-WhatIf</span></span>
<span data-ttu-id="dd5df-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dd5df-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd5df-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dd5df-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd5df-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd5df-135">CommonParameters</span></span>
<span data-ttu-id="dd5df-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd5df-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd5df-137">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd5df-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd5df-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dd5df-138">INPUTS</span></span>

### <span data-ttu-id="dd5df-139">System. String</span><span class="sxs-lookup"><span data-stu-id="dd5df-139">System.String</span></span>

### <span data-ttu-id="dd5df-140">Microsoft. Azure. Commands. Network. Models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="dd5df-140">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="dd5df-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dd5df-141">OUTPUTS</span></span>

### <span data-ttu-id="dd5df-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dd5df-142">System.Boolean</span></span>

## <span data-ttu-id="dd5df-143">Note</span><span class="sxs-lookup"><span data-stu-id="dd5df-143">NOTES</span></span>

## <span data-ttu-id="dd5df-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dd5df-144">RELATED LINKS</span></span>

[<span data-ttu-id="dd5df-145">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="dd5df-145">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="dd5df-146">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="dd5df-146">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="dd5df-147">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="dd5df-147">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)
