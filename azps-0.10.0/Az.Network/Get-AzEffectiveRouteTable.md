---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azeffectiveroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzEffectiveRouteTable.md
ms.openlocfilehash: 37c9827f2af970c0c376c31f4d67ba7723e02e99
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860833"
---
# <span data-ttu-id="708a4-101">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="708a4-101">Get-AzEffectiveRouteTable</span></span>

## <span data-ttu-id="708a4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="708a4-102">SYNOPSIS</span></span>
<span data-ttu-id="708a4-103">Ottiene la tabella di route effettiva di un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="708a4-103">Gets the effective route table of a network interface.</span></span>

## <span data-ttu-id="708a4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="708a4-104">SYNTAX</span></span>

```
Get-AzEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="708a4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="708a4-105">DESCRIPTION</span></span>
<span data-ttu-id="708a4-106">Il cmdlet **Get-AzEffectiveRouteTable** restituisce la tabella di route effettiva applicata a un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="708a4-106">The **Get-AzEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="708a4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="708a4-107">EXAMPLES</span></span>

### <span data-ttu-id="708a4-108">Esempio 1: ottenere la tabella di route effettiva in un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="708a4-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="708a4-109">Questo comando consente di ottenere la tabella di route effettiva associata all'interfaccia di rete denominata MyNetworkInterface nel gruppo di risorse denominato MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="708a4-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="708a4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="708a4-110">PARAMETERS</span></span>

### <span data-ttu-id="708a4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="708a4-111">-AsJob</span></span>
<span data-ttu-id="708a4-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="708a4-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="708a4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="708a4-113">-DefaultProfile</span></span>
<span data-ttu-id="708a4-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="708a4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="708a4-115">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="708a4-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="708a4-116">Specifica il nome di un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="708a4-116">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="708a4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="708a4-117">-ResourceGroupName</span></span>
<span data-ttu-id="708a4-118">Specifica il gruppo di risorse di un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="708a4-118">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="708a4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="708a4-119">CommonParameters</span></span>
<span data-ttu-id="708a4-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="708a4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="708a4-121">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="708a4-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="708a4-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="708a4-122">INPUTS</span></span>

## <span data-ttu-id="708a4-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="708a4-123">OUTPUTS</span></span>

### <span data-ttu-id="708a4-124">Microsoft. Azure. Commands. Network. Models. PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="708a4-124">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="708a4-125">Note</span><span class="sxs-lookup"><span data-stu-id="708a4-125">NOTES</span></span>

## <span data-ttu-id="708a4-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="708a4-126">RELATED LINKS</span></span>

[<span data-ttu-id="708a4-127">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="708a4-127">Get-AzEffectiveNetworkSecurityGroup</span></span>](./Get-AzEffectiveNetworkSecurityGroup.md)


