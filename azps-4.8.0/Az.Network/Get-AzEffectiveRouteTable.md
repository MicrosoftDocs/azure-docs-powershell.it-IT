---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azeffectiveroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveRouteTable.md
ms.openlocfilehash: e7d65e7797fb606306f0f0cc1e7c394fcf3d1d3d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188541"
---
# <span data-ttu-id="10e75-101">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="10e75-101">Get-AzEffectiveRouteTable</span></span>

## <span data-ttu-id="10e75-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="10e75-102">SYNOPSIS</span></span>
<span data-ttu-id="10e75-103">Ottiene la tabella di route effettiva di un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="10e75-103">Gets the effective route table of a network interface.</span></span>

## <span data-ttu-id="10e75-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="10e75-104">SYNTAX</span></span>

```
Get-AzEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10e75-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="10e75-105">DESCRIPTION</span></span>
<span data-ttu-id="10e75-106">Il cmdlet **Get-AzEffectiveRouteTable** restituisce la tabella di route effettiva applicata a un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="10e75-106">The **Get-AzEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="10e75-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="10e75-107">EXAMPLES</span></span>

### <span data-ttu-id="10e75-108">Esempio 1: ottenere la tabella di route effettiva in un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="10e75-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="10e75-109">Questo comando consente di ottenere la tabella di route effettiva associata all'interfaccia di rete denominata MyNetworkInterface nel gruppo di risorse denominato MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="10e75-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="10e75-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="10e75-110">PARAMETERS</span></span>

### <span data-ttu-id="10e75-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="10e75-111">-AsJob</span></span>
<span data-ttu-id="10e75-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="10e75-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="10e75-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10e75-113">-DefaultProfile</span></span>
<span data-ttu-id="10e75-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="10e75-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10e75-115">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="10e75-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="10e75-116">Specifica il nome di un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="10e75-116">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="10e75-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10e75-117">-ResourceGroupName</span></span>
<span data-ttu-id="10e75-118">Specifica il gruppo di risorse di un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="10e75-118">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="10e75-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10e75-119">CommonParameters</span></span>
<span data-ttu-id="10e75-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10e75-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10e75-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="10e75-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10e75-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="10e75-122">INPUTS</span></span>

### <span data-ttu-id="10e75-123">System. String</span><span class="sxs-lookup"><span data-stu-id="10e75-123">System.String</span></span>

## <span data-ttu-id="10e75-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="10e75-124">OUTPUTS</span></span>

### <span data-ttu-id="10e75-125">Microsoft. Azure. Commands. Network. Models. PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="10e75-125">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="10e75-126">Note</span><span class="sxs-lookup"><span data-stu-id="10e75-126">NOTES</span></span>

## <span data-ttu-id="10e75-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="10e75-127">RELATED LINKS</span></span>

[<span data-ttu-id="10e75-128">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="10e75-128">Get-AzEffectiveNetworkSecurityGroup</span></span>](./Get-AzEffectiveNetworkSecurityGroup.md)


