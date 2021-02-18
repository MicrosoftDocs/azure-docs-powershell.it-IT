---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznatgateway.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNatGateway.md
ms.openlocfilehash: fe19aba38402519a77185062ac6192d6ff9915eb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202458"
---
# <span data-ttu-id="88649-101">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="88649-101">Set-AzNatGateway</span></span>

## <span data-ttu-id="88649-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88649-102">SYNOPSIS</span></span>
<span data-ttu-id="88649-103">Aggiornare la risorsa Gateway Nat con l'indirizzo IP pubblico, il prefisso IP pubblico e IdleTimeoutInMinutes.</span><span class="sxs-lookup"><span data-stu-id="88649-103">Update Nat Gateway Resource with Public Ip Address, Public Ip Prefix and IdleTimeoutInMinutes.</span></span>

## <span data-ttu-id="88649-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="88649-104">SYNTAX</span></span>

### <span data-ttu-id="88649-105">SetByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="88649-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzNatGateway -ResourceGroupName <String> -Name <String> [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-AsJob] [-IdleTimeoutInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88649-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="88649-106">SetByResourceIdParameterSet</span></span>
```
Set-AzNatGateway -ResourceId <String> [-PublicIpAddress <PSResourceId[]>] [-PublicIpPrefix <PSResourceId[]>]
 [-AsJob] [-IdleTimeoutInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="88649-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="88649-107">SetByInputObjectParameterSet</span></span>
```
Set-AzNatGateway -InputObject <PSNatGateway> [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-AsJob] [-IdleTimeoutInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88649-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="88649-108">DESCRIPTION</span></span>
<span data-ttu-id="88649-109">Aggiornare la risorsa Gateway Nat con l'indirizzo IP pubblico, il prefisso IP pubblico e IdleTimeoutInMinutes.</span><span class="sxs-lookup"><span data-stu-id="88649-109">Update Nat Gateway Resource with Public Ip Address, Public Ip Prefix and IdleTimeoutInMinutes.</span></span>

## <span data-ttu-id="88649-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="88649-110">EXAMPLES</span></span>

### <span data-ttu-id="88649-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="88649-111">Example 1</span></span>
```powershell
PS C:\> $nGateway = Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "ng1"
PS C:\> $pipArray = $pip, $pip2
PS C:\> $natUpdate = Set-AzNatGateway -InputObject $nGateway -IdleTimeoutInMinutes 5 -PublicIpAddress $pipArray
PS C:\> $natUpdate = Set-AzNatGateway -ResourceGroupName "natgateway_test" -Name "ng1" -PublicIpAddress $pipArray
PS C:\> $natUpdate = Set-AzNatGateway -ResourceId "natgateway_id" -PublicIpAddress $pipArray
```

## <span data-ttu-id="88649-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88649-112">PARAMETERS</span></span>

### <span data-ttu-id="88649-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="88649-113">-AsJob</span></span>
<span data-ttu-id="88649-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="88649-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="88649-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88649-115">-DefaultProfile</span></span>
<span data-ttu-id="88649-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="88649-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88649-117">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="88649-117">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="88649-118">Timeout di inattività del gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="88649-118">The idle timeout of the nat gateway.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88649-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88649-119">-InputObject</span></span>
<span data-ttu-id="88649-120">Specifica la risorsa Gateway Nat.</span><span class="sxs-lookup"><span data-stu-id="88649-120">Specifies Nat Gateway Resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNatGateway
Parameter Sets: SetByInputObjectParameterSet
Aliases: NatGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88649-121">-Name</span><span class="sxs-lookup"><span data-stu-id="88649-121">-Name</span></span>
<span data-ttu-id="88649-122">Nome della risorsa Gateway Nat.</span><span class="sxs-lookup"><span data-stu-id="88649-122">Name of the Nat Gateway Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88649-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="88649-123">-PublicIpAddress</span></span>
<span data-ttu-id="88649-124">Matrice di indirizzi IP pubblici associati alla risorsa gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="88649-124">An array of public ip addresses associated with the nat gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88649-125">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="88649-125">-PublicIpPrefix</span></span>
<span data-ttu-id="88649-126">Matrice di prefissi IP pubblici associati alla risorsa gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="88649-126">An array of public ip prefixes associated with the nat gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88649-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88649-127">-ResourceGroupName</span></span>
<span data-ttu-id="88649-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="88649-128">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88649-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88649-129">-ResourceId</span></span>
<span data-ttu-id="88649-130">Specifica l'ID della risorsa Nat Gateway.</span><span class="sxs-lookup"><span data-stu-id="88649-130">Specifies the Id of the Nat Gateway resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases: NatGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88649-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="88649-131">-Confirm</span></span>
<span data-ttu-id="88649-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88649-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88649-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88649-133">-WhatIf</span></span>
<span data-ttu-id="88649-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="88649-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88649-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="88649-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88649-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88649-136">CommonParameters</span></span>
<span data-ttu-id="88649-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88649-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88649-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="88649-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88649-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="88649-139">INPUTS</span></span>

### <span data-ttu-id="88649-140">System.String</span><span class="sxs-lookup"><span data-stu-id="88649-140">System.String</span></span>

### <span data-ttu-id="88649-141">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="88649-141">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="88649-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="88649-142">OUTPUTS</span></span>

### <span data-ttu-id="88649-143">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="88649-143">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="88649-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="88649-144">NOTES</span></span>

## <span data-ttu-id="88649-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="88649-145">RELATED LINKS</span></span>
