---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 01F56553-1685-43D4-89E6-DDCDF17D1E00
online version: https://docs.microsoft.com/powershell/module/az.network/remove-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityGroup.md
ms.openlocfilehash: 27822e64c697ace3a69e6faf5f291215a2d89935
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993633"
---
# <span data-ttu-id="5437a-101">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5437a-101">Remove-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="5437a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5437a-102">SYNOPSIS</span></span>
<span data-ttu-id="5437a-103">Rimuove un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="5437a-103">Removes a network security group.</span></span>

## <span data-ttu-id="5437a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5437a-104">SYNTAX</span></span>

```
Remove-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5437a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5437a-105">DESCRIPTION</span></span>
<span data-ttu-id="5437a-106">Il cmdlet **Remove-AzNetworkSecurityGroup** rimuove un gruppo di sicurezza di rete azure.</span><span class="sxs-lookup"><span data-stu-id="5437a-106">The **Remove-AzNetworkSecurityGroup** cmdlet removes an Azure network security group.</span></span>

## <span data-ttu-id="5437a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5437a-107">EXAMPLES</span></span>

### <span data-ttu-id="5437a-108">Esempio 1: Rimuovere un gruppo di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="5437a-108">Example 1: Remove a network security group</span></span>
```
PS C:\>Remove-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
```

<span data-ttu-id="5437a-109">Questo comando rimuove il gruppo di sicurezza NSG-FrontEnd gruppo di risorse denominato TestRG.</span><span class="sxs-lookup"><span data-stu-id="5437a-109">This command removes the security group named NSG-FrontEnd in the resource group named TestRG.</span></span>

## <span data-ttu-id="5437a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5437a-110">PARAMETERS</span></span>

### <span data-ttu-id="5437a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5437a-111">-AsJob</span></span>
<span data-ttu-id="5437a-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="5437a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5437a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5437a-113">-DefaultProfile</span></span>
<span data-ttu-id="5437a-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5437a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5437a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5437a-115">-Force</span></span>
<span data-ttu-id="5437a-116">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="5437a-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5437a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="5437a-117">-Name</span></span>
<span data-ttu-id="5437a-118">Specifica il nome del gruppo di sicurezza di rete rimosso dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5437a-118">Specifies the name of the network security group that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5437a-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5437a-119">-PassThru</span></span>
<span data-ttu-id="5437a-120">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="5437a-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5437a-121">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="5437a-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5437a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5437a-122">-ResourceGroupName</span></span>
<span data-ttu-id="5437a-123">Specifica il nome di un gruppo di risorse da cui questo cmdlet rimuove un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="5437a-123">Specifies the name of a resource group that this cmdlet removes a network security group from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5437a-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5437a-124">-Confirm</span></span>
<span data-ttu-id="5437a-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5437a-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5437a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5437a-126">-WhatIf</span></span>
<span data-ttu-id="5437a-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5437a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5437a-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5437a-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5437a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5437a-129">CommonParameters</span></span>
<span data-ttu-id="5437a-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5437a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5437a-131">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5437a-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5437a-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="5437a-132">INPUTS</span></span>

### <span data-ttu-id="5437a-133">System.String</span><span class="sxs-lookup"><span data-stu-id="5437a-133">System.String</span></span>

## <span data-ttu-id="5437a-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5437a-134">OUTPUTS</span></span>

### <span data-ttu-id="5437a-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5437a-135">System.Boolean</span></span>

## <span data-ttu-id="5437a-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="5437a-136">NOTES</span></span>

## <span data-ttu-id="5437a-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5437a-137">RELATED LINKS</span></span>

[<span data-ttu-id="5437a-138">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5437a-138">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="5437a-139">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5437a-139">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="5437a-140">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5437a-140">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)


