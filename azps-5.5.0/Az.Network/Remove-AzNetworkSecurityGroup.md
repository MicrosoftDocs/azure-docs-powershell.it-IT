---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 01F56553-1685-43D4-89E6-DDCDF17D1E00
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityGroup.md
ms.openlocfilehash: c5a5cbbbc46106fe6c388ee8f16117411f03fe0c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206594"
---
# <span data-ttu-id="e3d52-101">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e3d52-101">Remove-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="e3d52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3d52-102">SYNOPSIS</span></span>
<span data-ttu-id="e3d52-103">Rimuove un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="e3d52-103">Removes a network security group.</span></span>

## <span data-ttu-id="e3d52-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e3d52-104">SYNTAX</span></span>

```
Remove-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3d52-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e3d52-105">DESCRIPTION</span></span>
<span data-ttu-id="e3d52-106">Il cmdlet **Remove-AzNetworkSecurityGroup** rimuove un gruppo di sicurezza di rete Azure.</span><span class="sxs-lookup"><span data-stu-id="e3d52-106">The **Remove-AzNetworkSecurityGroup** cmdlet removes an Azure network security group.</span></span>

## <span data-ttu-id="e3d52-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e3d52-107">EXAMPLES</span></span>

### <span data-ttu-id="e3d52-108">Esempio 1: Rimuovere un gruppo di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="e3d52-108">Example 1: Remove a network security group</span></span>
```
PS C:\>Remove-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
```

<span data-ttu-id="e3d52-109">Questo comando rimuove il gruppo di sicurezza NSG-FrontEnd gruppo di risorse denominato TestRG.</span><span class="sxs-lookup"><span data-stu-id="e3d52-109">This command removes the security group named NSG-FrontEnd in the resource group named TestRG.</span></span>

## <span data-ttu-id="e3d52-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3d52-110">PARAMETERS</span></span>

### <span data-ttu-id="e3d52-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e3d52-111">-AsJob</span></span>
<span data-ttu-id="e3d52-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e3d52-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e3d52-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3d52-113">-DefaultProfile</span></span>
<span data-ttu-id="e3d52-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e3d52-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3d52-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e3d52-115">-Force</span></span>
<span data-ttu-id="e3d52-116">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="e3d52-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e3d52-117">-Name</span><span class="sxs-lookup"><span data-stu-id="e3d52-117">-Name</span></span>
<span data-ttu-id="e3d52-118">Specifica il nome del gruppo di sicurezza di rete rimosso dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3d52-118">Specifies the name of the network security group that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e3d52-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e3d52-119">-PassThru</span></span>
<span data-ttu-id="e3d52-120">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="e3d52-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e3d52-121">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="e3d52-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e3d52-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3d52-122">-ResourceGroupName</span></span>
<span data-ttu-id="e3d52-123">Specifica il nome di un gruppo di risorse da cui questo cmdlet rimuove un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="e3d52-123">Specifies the name of a resource group that this cmdlet removes a network security group from.</span></span>

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

### <span data-ttu-id="e3d52-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3d52-124">-Confirm</span></span>
<span data-ttu-id="e3d52-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3d52-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3d52-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3d52-126">-WhatIf</span></span>
<span data-ttu-id="e3d52-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3d52-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3d52-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3d52-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3d52-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3d52-129">CommonParameters</span></span>
<span data-ttu-id="e3d52-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3d52-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3d52-131">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3d52-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3d52-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="e3d52-132">INPUTS</span></span>

### <span data-ttu-id="e3d52-133">System.String</span><span class="sxs-lookup"><span data-stu-id="e3d52-133">System.String</span></span>

## <span data-ttu-id="e3d52-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e3d52-134">OUTPUTS</span></span>

### <span data-ttu-id="e3d52-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e3d52-135">System.Boolean</span></span>

## <span data-ttu-id="e3d52-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="e3d52-136">NOTES</span></span>

## <span data-ttu-id="e3d52-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e3d52-137">RELATED LINKS</span></span>

[<span data-ttu-id="e3d52-138">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e3d52-138">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="e3d52-139">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e3d52-139">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="e3d52-140">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e3d52-140">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)


