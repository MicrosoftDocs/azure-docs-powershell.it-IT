---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C83A0465-45EF-4FCC-B706-D5DF819664F0
online version: https://docs.microsoft.com/powershell/module/az.network/remove-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterface.md
ms.openlocfilehash: 54bc4a3b9875f68df8a7c824c7e4f754e6f35a4e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993648"
---
# <span data-ttu-id="0523d-101">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="0523d-101">Remove-AzNetworkInterface</span></span>

## <span data-ttu-id="0523d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0523d-102">SYNOPSIS</span></span>
<span data-ttu-id="0523d-103">Rimuove un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="0523d-103">Removes a network interface.</span></span>

## <span data-ttu-id="0523d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0523d-104">SYNTAX</span></span>

```
Remove-AzNetworkInterface -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0523d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0523d-105">DESCRIPTION</span></span>
<span data-ttu-id="0523d-106">Il cmdlet **Remove-AzNetworkInterface rimuove** un'interfaccia di rete di Azure.</span><span class="sxs-lookup"><span data-stu-id="0523d-106">The **Remove-AzNetworkInterface** cmdlet removes an Azure network interface.</span></span>

## <span data-ttu-id="0523d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0523d-107">EXAMPLES</span></span>

### <span data-ttu-id="0523d-108">Esempio 1: Rimuovere un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="0523d-108">Example 1: Remove a network interface</span></span>
```
PS C:\>Remove-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="0523d-109">Questo comando rimuove l'interfaccia di rete NetworkInterface1 nel gruppo di risorse ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="0523d-109">This command removes the network interface NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="0523d-110">Poiché il *parametro Force* non viene usato, all'utente verrà chiesto di confermare l'azione.</span><span class="sxs-lookup"><span data-stu-id="0523d-110">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="0523d-111">Esempio 2: Rimuovere un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="0523d-111">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" | Remove-AzNetworkInterface -Force
```

<span data-ttu-id="0523d-112">Questo comando rimuove tutte le interfacce di rete nel gruppo di risorse ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="0523d-112">This command removes all network interfaces in resource group ResourceGroup1.</span></span>
<span data-ttu-id="0523d-113">Poiché viene *usato* il parametro Force, all'utente non viene richiesta conferma.</span><span class="sxs-lookup"><span data-stu-id="0523d-113">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="0523d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0523d-114">PARAMETERS</span></span>

### <span data-ttu-id="0523d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0523d-115">-AsJob</span></span>
<span data-ttu-id="0523d-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="0523d-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0523d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0523d-117">-DefaultProfile</span></span>
<span data-ttu-id="0523d-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0523d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0523d-119">-Force</span><span class="sxs-lookup"><span data-stu-id="0523d-119">-Force</span></span>
<span data-ttu-id="0523d-120">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="0523d-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0523d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0523d-121">-Name</span></span>
<span data-ttu-id="0523d-122">Specifica il nome dell'interfaccia di rete rimossa dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0523d-122">Specifies the name of the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0523d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0523d-123">-PassThru</span></span>
<span data-ttu-id="0523d-124">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="0523d-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0523d-125">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="0523d-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0523d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0523d-126">-ResourceGroupName</span></span>
<span data-ttu-id="0523d-127">Specifica il nome di un gruppo di risorse che contiene l'interfaccia di rete rimossa dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0523d-127">Specifies the name of a resource group that contains the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0523d-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0523d-128">-Confirm</span></span>
<span data-ttu-id="0523d-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0523d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0523d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0523d-130">-WhatIf</span></span>
<span data-ttu-id="0523d-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0523d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0523d-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0523d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0523d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0523d-133">CommonParameters</span></span>
<span data-ttu-id="0523d-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0523d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0523d-135">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0523d-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0523d-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="0523d-136">INPUTS</span></span>

### <span data-ttu-id="0523d-137">System.String</span><span class="sxs-lookup"><span data-stu-id="0523d-137">System.String</span></span>

## <span data-ttu-id="0523d-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0523d-138">OUTPUTS</span></span>

### <span data-ttu-id="0523d-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0523d-139">System.Boolean</span></span>

## <span data-ttu-id="0523d-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="0523d-140">NOTES</span></span>

## <span data-ttu-id="0523d-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0523d-141">RELATED LINKS</span></span>

[<span data-ttu-id="0523d-142">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="0523d-142">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="0523d-143">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="0523d-143">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="0523d-144">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="0523d-144">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)


