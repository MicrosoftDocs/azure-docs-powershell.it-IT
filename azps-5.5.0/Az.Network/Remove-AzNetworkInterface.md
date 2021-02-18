---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C83A0465-45EF-4FCC-B706-D5DF819664F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterface.md
ms.openlocfilehash: f4de49bb2e35bf3d392fba06d663800a5bdc44a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184278"
---
# <span data-ttu-id="2ba44-101">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2ba44-101">Remove-AzNetworkInterface</span></span>

## <span data-ttu-id="2ba44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ba44-102">SYNOPSIS</span></span>
<span data-ttu-id="2ba44-103">Rimuove un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="2ba44-103">Removes a network interface.</span></span>

## <span data-ttu-id="2ba44-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2ba44-104">SYNTAX</span></span>

```
Remove-AzNetworkInterface -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ba44-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2ba44-105">DESCRIPTION</span></span>
<span data-ttu-id="2ba44-106">Il cmdlet **Remove-AzNetworkInterface rimuove** un'interfaccia di rete di Azure.</span><span class="sxs-lookup"><span data-stu-id="2ba44-106">The **Remove-AzNetworkInterface** cmdlet removes an Azure network interface.</span></span>

## <span data-ttu-id="2ba44-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2ba44-107">EXAMPLES</span></span>

### <span data-ttu-id="2ba44-108">Esempio 1: Rimuovere un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="2ba44-108">Example 1: Remove a network interface</span></span>
```
PS C:\>Remove-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="2ba44-109">Questo comando rimuove l'interfaccia di rete NetworkInterface1 nel gruppo di risorse ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="2ba44-109">This command removes the network interface NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="2ba44-110">Poiché il *parametro Force* non viene usato, all'utente verrà chiesto di confermare l'azione.</span><span class="sxs-lookup"><span data-stu-id="2ba44-110">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="2ba44-111">Esempio 2: Rimuovere un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="2ba44-111">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" | Remove-AzNetworkInterface -Force
```

<span data-ttu-id="2ba44-112">Questo comando rimuove tutte le interfacce di rete nel gruppo di risorse ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="2ba44-112">This command removes all network interfaces in resource group ResourceGroup1.</span></span>
<span data-ttu-id="2ba44-113">Poiché viene *usato* il parametro Force, all'utente non viene richiesta conferma.</span><span class="sxs-lookup"><span data-stu-id="2ba44-113">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="2ba44-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ba44-114">PARAMETERS</span></span>

### <span data-ttu-id="2ba44-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2ba44-115">-AsJob</span></span>
<span data-ttu-id="2ba44-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="2ba44-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2ba44-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ba44-117">-DefaultProfile</span></span>
<span data-ttu-id="2ba44-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2ba44-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ba44-119">-Force</span><span class="sxs-lookup"><span data-stu-id="2ba44-119">-Force</span></span>
<span data-ttu-id="2ba44-120">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="2ba44-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2ba44-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2ba44-121">-Name</span></span>
<span data-ttu-id="2ba44-122">Specifica il nome dell'interfaccia di rete rimossa dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ba44-122">Specifies the name of the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2ba44-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2ba44-123">-PassThru</span></span>
<span data-ttu-id="2ba44-124">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="2ba44-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2ba44-125">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="2ba44-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2ba44-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ba44-126">-ResourceGroupName</span></span>
<span data-ttu-id="2ba44-127">Specifica il nome di un gruppo di risorse che contiene l'interfaccia di rete rimossa dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ba44-127">Specifies the name of a resource group that contains the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2ba44-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2ba44-128">-Confirm</span></span>
<span data-ttu-id="2ba44-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ba44-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ba44-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ba44-130">-WhatIf</span></span>
<span data-ttu-id="2ba44-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2ba44-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ba44-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2ba44-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ba44-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ba44-133">CommonParameters</span></span>
<span data-ttu-id="2ba44-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ba44-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ba44-135">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ba44-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ba44-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="2ba44-136">INPUTS</span></span>

### <span data-ttu-id="2ba44-137">System.String</span><span class="sxs-lookup"><span data-stu-id="2ba44-137">System.String</span></span>

## <span data-ttu-id="2ba44-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2ba44-138">OUTPUTS</span></span>

### <span data-ttu-id="2ba44-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2ba44-139">System.Boolean</span></span>

## <span data-ttu-id="2ba44-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="2ba44-140">NOTES</span></span>

## <span data-ttu-id="2ba44-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2ba44-141">RELATED LINKS</span></span>

[<span data-ttu-id="2ba44-142">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2ba44-142">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="2ba44-143">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2ba44-143">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="2ba44-144">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2ba44-144">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)


