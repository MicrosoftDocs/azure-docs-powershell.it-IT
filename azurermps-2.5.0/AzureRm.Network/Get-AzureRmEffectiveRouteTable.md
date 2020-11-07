---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermeffectiveroutetable
schema: 2.0.0
ms.openlocfilehash: 403a3d37418e022032988d5d7fccb40a1e79f449
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866093"
---
# <span data-ttu-id="57fce-101">Get-AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="57fce-101">Get-AzureRmEffectiveRouteTable</span></span>

## <span data-ttu-id="57fce-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="57fce-102">SYNOPSIS</span></span>
<span data-ttu-id="57fce-103">Ottiene la tabella di route effettiva di un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="57fce-103">Gets the effective route table of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57fce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="57fce-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57fce-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="57fce-105">DESCRIPTION</span></span>
<span data-ttu-id="57fce-106">Il cmdlet **Get-AzureRmEffectiveRouteTable** restituisce la tabella di route effettiva applicata a un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="57fce-106">The **Get-AzureRmEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="57fce-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="57fce-107">EXAMPLES</span></span>

### <span data-ttu-id="57fce-108">Esempio 1: ottenere la tabella di route effettiva in un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="57fce-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="57fce-109">Questo comando consente di ottenere la tabella di route effettiva associata all'interfaccia di rete denominata MyNetworkInterface nel gruppo di risorse denominato MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="57fce-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="57fce-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="57fce-110">PARAMETERS</span></span>

### <span data-ttu-id="57fce-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="57fce-111">-AsJob</span></span>
<span data-ttu-id="57fce-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="57fce-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57fce-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57fce-113">-DefaultProfile</span></span>
<span data-ttu-id="57fce-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="57fce-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57fce-115">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="57fce-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="57fce-116">Specifica il nome di un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="57fce-116">Specified the name of a network interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57fce-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57fce-117">-ResourceGroupName</span></span>
<span data-ttu-id="57fce-118">Specifica il gruppo di risorse di un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="57fce-118">Specifies the resource group of a network interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57fce-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57fce-119">CommonParameters</span></span>
<span data-ttu-id="57fce-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57fce-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57fce-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57fce-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57fce-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="57fce-122">INPUTS</span></span>

## <span data-ttu-id="57fce-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="57fce-123">OUTPUTS</span></span>

### <span data-ttu-id="57fce-124">Microsoft. Azure. Commands. Network. Models. PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="57fce-124">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="57fce-125">Note</span><span class="sxs-lookup"><span data-stu-id="57fce-125">NOTES</span></span>

## <span data-ttu-id="57fce-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="57fce-126">RELATED LINKS</span></span>

[<span data-ttu-id="57fce-127">Get-AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="57fce-127">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>](./Get-AzureRmEffectiveNetworkSecurityGroup.md)


