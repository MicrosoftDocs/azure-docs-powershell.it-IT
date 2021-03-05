---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-aznatgateway.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNatGateway.md
ms.openlocfilehash: e0c8b550b6d9571c3dd55552bab101441085f3ac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003374"
---
# <span data-ttu-id="75a02-101">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="75a02-101">Set-AzNatGateway</span></span>

## <span data-ttu-id="75a02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75a02-102">SYNOPSIS</span></span>
<span data-ttu-id="75a02-103">Aggiornare la risorsa Gateway Nat con l'indirizzo IP pubblico, il prefisso IP pubblico e IdleTimeoutInMinutes.</span><span class="sxs-lookup"><span data-stu-id="75a02-103">Update Nat Gateway Resource with Public Ip Address, Public Ip Prefix and IdleTimeoutInMinutes.</span></span>

## <span data-ttu-id="75a02-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="75a02-104">SYNTAX</span></span>

### <span data-ttu-id="75a02-105">SetByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="75a02-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzNatGateway -ResourceGroupName <String> -Name <String> [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-AsJob] [-IdleTimeoutInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75a02-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="75a02-106">SetByResourceIdParameterSet</span></span>
```
Set-AzNatGateway -ResourceId <String> [-PublicIpAddress <PSResourceId[]>] [-PublicIpPrefix <PSResourceId[]>]
 [-AsJob] [-IdleTimeoutInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75a02-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="75a02-107">SetByInputObjectParameterSet</span></span>
```
Set-AzNatGateway -InputObject <PSNatGateway> [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-AsJob] [-IdleTimeoutInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75a02-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="75a02-108">DESCRIPTION</span></span>
<span data-ttu-id="75a02-109">Aggiornare la risorsa Gateway Nat con l'indirizzo IP pubblico, il prefisso IP pubblico e IdleTimeoutInMinutes.</span><span class="sxs-lookup"><span data-stu-id="75a02-109">Update Nat Gateway Resource with Public Ip Address, Public Ip Prefix and IdleTimeoutInMinutes.</span></span>

## <span data-ttu-id="75a02-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="75a02-110">EXAMPLES</span></span>

### <span data-ttu-id="75a02-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="75a02-111">Example 1</span></span>
```powershell
PS C:\> $nGateway = Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "ng1"
PS C:\> $pipArray = $pip, $pip2
PS C:\> $natUpdate = Set-AzNatGateway -InputObject $nGateway -IdleTimeoutInMinutes 5 -PublicIpAddress $pipArray
PS C:\> $natUpdate = Set-AzNatGateway -ResourceGroupName "natgateway_test" -Name "ng1" -PublicIpAddress $pipArray
PS C:\> $natUpdate = Set-AzNatGateway -ResourceId "natgateway_id" -PublicIpAddress $pipArray
```

## <span data-ttu-id="75a02-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75a02-112">PARAMETERS</span></span>

### <span data-ttu-id="75a02-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="75a02-113">-AsJob</span></span>
<span data-ttu-id="75a02-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="75a02-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="75a02-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75a02-115">-DefaultProfile</span></span>
<span data-ttu-id="75a02-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="75a02-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75a02-117">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="75a02-117">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="75a02-118">Timeout di inattività del gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="75a02-118">The idle timeout of the nat gateway.</span></span>

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

### <span data-ttu-id="75a02-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75a02-119">-InputObject</span></span>
<span data-ttu-id="75a02-120">Specifica la risorsa Gateway Nat.</span><span class="sxs-lookup"><span data-stu-id="75a02-120">Specifies Nat Gateway Resource.</span></span>

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

### <span data-ttu-id="75a02-121">-Name</span><span class="sxs-lookup"><span data-stu-id="75a02-121">-Name</span></span>
<span data-ttu-id="75a02-122">Nome della risorsa Gateway Nat.</span><span class="sxs-lookup"><span data-stu-id="75a02-122">Name of the Nat Gateway Resource.</span></span>

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

### <span data-ttu-id="75a02-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="75a02-123">-PublicIpAddress</span></span>
<span data-ttu-id="75a02-124">Matrice di indirizzi IP pubblici associati alla risorsa gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="75a02-124">An array of public ip addresses associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="75a02-125">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="75a02-125">-PublicIpPrefix</span></span>
<span data-ttu-id="75a02-126">Matrice di prefissi IP pubblici associati alla risorsa gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="75a02-126">An array of public ip prefixes associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="75a02-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75a02-127">-ResourceGroupName</span></span>
<span data-ttu-id="75a02-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="75a02-128">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="75a02-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75a02-129">-ResourceId</span></span>
<span data-ttu-id="75a02-130">Specifica l'ID della risorsa Nat Gateway.</span><span class="sxs-lookup"><span data-stu-id="75a02-130">Specifies the Id of the Nat Gateway resource.</span></span>

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

### <span data-ttu-id="75a02-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75a02-131">-Confirm</span></span>
<span data-ttu-id="75a02-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75a02-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75a02-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75a02-133">-WhatIf</span></span>
<span data-ttu-id="75a02-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="75a02-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75a02-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="75a02-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75a02-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75a02-136">CommonParameters</span></span>
<span data-ttu-id="75a02-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75a02-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75a02-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="75a02-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75a02-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="75a02-139">INPUTS</span></span>

### <span data-ttu-id="75a02-140">System.String</span><span class="sxs-lookup"><span data-stu-id="75a02-140">System.String</span></span>

### <span data-ttu-id="75a02-141">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="75a02-141">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="75a02-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="75a02-142">OUTPUTS</span></span>

### <span data-ttu-id="75a02-143">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="75a02-143">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="75a02-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="75a02-144">NOTES</span></span>

## <span data-ttu-id="75a02-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="75a02-145">RELATED LINKS</span></span>
