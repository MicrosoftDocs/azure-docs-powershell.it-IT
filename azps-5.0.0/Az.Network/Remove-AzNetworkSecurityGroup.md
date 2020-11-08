---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 01F56553-1685-43D4-89E6-DDCDF17D1E00
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityGroup.md
ms.openlocfilehash: c5a5cbbbc46106fe6c388ee8f16117411f03fe0c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200714"
---
# <span data-ttu-id="a8bee-101">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a8bee-101">Remove-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="a8bee-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a8bee-102">SYNOPSIS</span></span>
<span data-ttu-id="a8bee-103">Rimuove un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="a8bee-103">Removes a network security group.</span></span>

## <span data-ttu-id="a8bee-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a8bee-104">SYNTAX</span></span>

```
Remove-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8bee-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8bee-105">DESCRIPTION</span></span>
<span data-ttu-id="a8bee-106">Il cmdlet **Remove-AzNetworkSecurityGroup** rimuove un gruppo di sicurezza di rete Azure.</span><span class="sxs-lookup"><span data-stu-id="a8bee-106">The **Remove-AzNetworkSecurityGroup** cmdlet removes an Azure network security group.</span></span>

## <span data-ttu-id="a8bee-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a8bee-107">EXAMPLES</span></span>

### <span data-ttu-id="a8bee-108">Esempio 1: rimuovere un gruppo di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="a8bee-108">Example 1: Remove a network security group</span></span>
```
PS C:\>Remove-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
```

<span data-ttu-id="a8bee-109">Questo comando rimuove il gruppo di sicurezza denominato NSG-FrontEnd nel gruppo di risorse denominato TestRG.</span><span class="sxs-lookup"><span data-stu-id="a8bee-109">This command removes the security group named NSG-FrontEnd in the resource group named TestRG.</span></span>

## <span data-ttu-id="a8bee-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a8bee-110">PARAMETERS</span></span>

### <span data-ttu-id="a8bee-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a8bee-111">-AsJob</span></span>
<span data-ttu-id="a8bee-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a8bee-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a8bee-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8bee-113">-DefaultProfile</span></span>
<span data-ttu-id="a8bee-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a8bee-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8bee-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a8bee-115">-Force</span></span>
<span data-ttu-id="a8bee-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a8bee-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a8bee-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="a8bee-117">-Name</span></span>
<span data-ttu-id="a8bee-118">Specifica il nome del gruppo di sicurezza di rete rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8bee-118">Specifies the name of the network security group that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a8bee-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8bee-119">-PassThru</span></span>
<span data-ttu-id="a8bee-120">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="a8bee-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a8bee-121">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="a8bee-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a8bee-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8bee-122">-ResourceGroupName</span></span>
<span data-ttu-id="a8bee-123">Specifica il nome di un gruppo di risorse da cui questo cmdlet rimuove un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="a8bee-123">Specifies the name of a resource group that this cmdlet removes a network security group from.</span></span>

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

### <span data-ttu-id="a8bee-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a8bee-124">-Confirm</span></span>
<span data-ttu-id="a8bee-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8bee-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8bee-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8bee-126">-WhatIf</span></span>
<span data-ttu-id="a8bee-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a8bee-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8bee-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a8bee-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8bee-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8bee-129">CommonParameters</span></span>
<span data-ttu-id="a8bee-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8bee-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8bee-131">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8bee-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8bee-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a8bee-132">INPUTS</span></span>

### <span data-ttu-id="a8bee-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a8bee-133">System.String</span></span>

## <span data-ttu-id="a8bee-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a8bee-134">OUTPUTS</span></span>

### <span data-ttu-id="a8bee-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a8bee-135">System.Boolean</span></span>

## <span data-ttu-id="a8bee-136">Note</span><span class="sxs-lookup"><span data-stu-id="a8bee-136">NOTES</span></span>

## <span data-ttu-id="a8bee-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a8bee-137">RELATED LINKS</span></span>

[<span data-ttu-id="a8bee-138">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a8bee-138">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="a8bee-139">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a8bee-139">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="a8bee-140">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a8bee-140">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)

