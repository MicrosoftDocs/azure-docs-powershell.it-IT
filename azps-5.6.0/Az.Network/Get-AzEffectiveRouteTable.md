---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: https://docs.microsoft.com/powershell/module/az.network/get-azeffectiveroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveRouteTable.md
ms.openlocfilehash: 28ec38b9f2dfbb658203aa46fe0d8225aca08a5e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967917"
---
# <span data-ttu-id="8924b-101">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="8924b-101">Get-AzEffectiveRouteTable</span></span>

## <span data-ttu-id="8924b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8924b-102">SYNOPSIS</span></span>
<span data-ttu-id="8924b-103">Ottiene la tabella di route effettiva di un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="8924b-103">Gets the effective route table of a network interface.</span></span>

## <span data-ttu-id="8924b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8924b-104">SYNTAX</span></span>

```
Get-AzEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8924b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8924b-105">DESCRIPTION</span></span>
<span data-ttu-id="8924b-106">Il cmdlet **Get-AzEffectiveRouteTable** restituisce la tabella di route effettiva applicata a un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="8924b-106">The **Get-AzEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="8924b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8924b-107">EXAMPLES</span></span>

### <span data-ttu-id="8924b-108">Esempio 1: Ottenere la tabella di route effettiva in un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="8924b-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="8924b-109">Questo comando ottiene la tabella di route effettiva associata all'interfaccia di rete denominata MyNetworkInterface nel gruppo di risorse denominato MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8924b-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="8924b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8924b-110">PARAMETERS</span></span>

### <span data-ttu-id="8924b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8924b-111">-AsJob</span></span>
<span data-ttu-id="8924b-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="8924b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8924b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8924b-113">-DefaultProfile</span></span>
<span data-ttu-id="8924b-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8924b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8924b-115">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="8924b-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="8924b-116">È stato specificato il nome di un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="8924b-116">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="8924b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8924b-117">-ResourceGroupName</span></span>
<span data-ttu-id="8924b-118">Specifica il gruppo di risorse di un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="8924b-118">Specifies the resource group of a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8924b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8924b-119">CommonParameters</span></span>
<span data-ttu-id="8924b-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8924b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8924b-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8924b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8924b-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="8924b-122">INPUTS</span></span>

### <span data-ttu-id="8924b-123">System.String</span><span class="sxs-lookup"><span data-stu-id="8924b-123">System.String</span></span>

## <span data-ttu-id="8924b-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8924b-124">OUTPUTS</span></span>

### <span data-ttu-id="8924b-125">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="8924b-125">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="8924b-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="8924b-126">NOTES</span></span>

## <span data-ttu-id="8924b-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8924b-127">RELATED LINKS</span></span>

[<span data-ttu-id="8924b-128">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8924b-128">Get-AzEffectiveNetworkSecurityGroup</span></span>](./Get-AzEffectiveNetworkSecurityGroup.md)


