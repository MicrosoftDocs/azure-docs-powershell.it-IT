---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznatgateway.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNatGateway.md
ms.openlocfilehash: fe19aba38402519a77185062ac6192d6ff9915eb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200699"
---
# <span data-ttu-id="a2edc-101">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a2edc-101">Set-AzNatGateway</span></span>

## <span data-ttu-id="a2edc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a2edc-102">SYNOPSIS</span></span>
<span data-ttu-id="a2edc-103">Aggiornare la risorsa gateway NAT con l'indirizzo IP pubblico, il prefisso IP pubblico e IdleTimeoutInMinutes.</span><span class="sxs-lookup"><span data-stu-id="a2edc-103">Update Nat Gateway Resource with Public Ip Address, Public Ip Prefix and IdleTimeoutInMinutes.</span></span>

## <span data-ttu-id="a2edc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a2edc-104">SYNTAX</span></span>

### <span data-ttu-id="a2edc-105">SetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a2edc-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzNatGateway -ResourceGroupName <String> -Name <String> [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-AsJob] [-IdleTimeoutInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2edc-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2edc-106">SetByResourceIdParameterSet</span></span>
```
Set-AzNatGateway -ResourceId <String> [-PublicIpAddress <PSResourceId[]>] [-PublicIpPrefix <PSResourceId[]>]
 [-AsJob] [-IdleTimeoutInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a2edc-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2edc-107">SetByInputObjectParameterSet</span></span>
```
Set-AzNatGateway -InputObject <PSNatGateway> [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-AsJob] [-IdleTimeoutInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2edc-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a2edc-108">DESCRIPTION</span></span>
<span data-ttu-id="a2edc-109">Aggiornare la risorsa gateway NAT con l'indirizzo IP pubblico, il prefisso IP pubblico e IdleTimeoutInMinutes.</span><span class="sxs-lookup"><span data-stu-id="a2edc-109">Update Nat Gateway Resource with Public Ip Address, Public Ip Prefix and IdleTimeoutInMinutes.</span></span>

## <span data-ttu-id="a2edc-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a2edc-110">EXAMPLES</span></span>

### <span data-ttu-id="a2edc-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a2edc-111">Example 1</span></span>
```powershell
PS C:\> $nGateway = Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "ng1"
PS C:\> $pipArray = $pip, $pip2
PS C:\> $natUpdate = Set-AzNatGateway -InputObject $nGateway -IdleTimeoutInMinutes 5 -PublicIpAddress $pipArray
PS C:\> $natUpdate = Set-AzNatGateway -ResourceGroupName "natgateway_test" -Name "ng1" -PublicIpAddress $pipArray
PS C:\> $natUpdate = Set-AzNatGateway -ResourceId "natgateway_id" -PublicIpAddress $pipArray
```

## <span data-ttu-id="a2edc-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a2edc-112">PARAMETERS</span></span>

### <span data-ttu-id="a2edc-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2edc-113">-AsJob</span></span>
<span data-ttu-id="a2edc-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a2edc-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a2edc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2edc-115">-DefaultProfile</span></span>
<span data-ttu-id="a2edc-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a2edc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2edc-117">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="a2edc-117">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="a2edc-118">Timeout inattivo del gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="a2edc-118">The idle timeout of the nat gateway.</span></span>

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

### <span data-ttu-id="a2edc-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2edc-119">-InputObject</span></span>
<span data-ttu-id="a2edc-120">Specifica la risorsa gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="a2edc-120">Specifies Nat Gateway Resource.</span></span>

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

### <span data-ttu-id="a2edc-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="a2edc-121">-Name</span></span>
<span data-ttu-id="a2edc-122">Nome della risorsa gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="a2edc-122">Name of the Nat Gateway Resource.</span></span>

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

### <span data-ttu-id="a2edc-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a2edc-123">-PublicIpAddress</span></span>
<span data-ttu-id="a2edc-124">Matrice di indirizzi IP pubblici associata alla risorsa gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="a2edc-124">An array of public ip addresses associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="a2edc-125">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="a2edc-125">-PublicIpPrefix</span></span>
<span data-ttu-id="a2edc-126">Matrice di prefissi IP pubblici associata alla risorsa gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="a2edc-126">An array of public ip prefixes associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="a2edc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2edc-127">-ResourceGroupName</span></span>
<span data-ttu-id="a2edc-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a2edc-128">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="a2edc-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2edc-129">-ResourceId</span></span>
<span data-ttu-id="a2edc-130">Specifica l'ID della risorsa gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="a2edc-130">Specifies the Id of the Nat Gateway resource.</span></span>

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

### <span data-ttu-id="a2edc-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a2edc-131">-Confirm</span></span>
<span data-ttu-id="a2edc-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2edc-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2edc-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2edc-133">-WhatIf</span></span>
<span data-ttu-id="a2edc-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a2edc-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2edc-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a2edc-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2edc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2edc-136">CommonParameters</span></span>
<span data-ttu-id="a2edc-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2edc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2edc-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a2edc-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2edc-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a2edc-139">INPUTS</span></span>

### <span data-ttu-id="a2edc-140">System. String</span><span class="sxs-lookup"><span data-stu-id="a2edc-140">System.String</span></span>

### <span data-ttu-id="a2edc-141">Microsoft. Azure. Commands. Network. Models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="a2edc-141">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="a2edc-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a2edc-142">OUTPUTS</span></span>

### <span data-ttu-id="a2edc-143">Microsoft. Azure. Commands. Network. Models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="a2edc-143">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="a2edc-144">Note</span><span class="sxs-lookup"><span data-stu-id="a2edc-144">NOTES</span></span>

## <span data-ttu-id="a2edc-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a2edc-145">RELATED LINKS</span></span>