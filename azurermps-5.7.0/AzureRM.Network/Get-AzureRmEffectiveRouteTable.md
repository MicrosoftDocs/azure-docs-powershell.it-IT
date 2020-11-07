---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermeffectiveroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveRouteTable.md
ms.openlocfilehash: 7826dad8b9f19e3fc289ec4b08efa98b8b1ed8a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686478"
---
# <span data-ttu-id="86172-101">Get-AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="86172-101">Get-AzureRmEffectiveRouteTable</span></span>

## <span data-ttu-id="86172-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="86172-102">SYNOPSIS</span></span>
<span data-ttu-id="86172-103">Ottiene la tabella di route effettiva di un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="86172-103">Gets the effective route table of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86172-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="86172-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86172-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86172-105">DESCRIPTION</span></span>
<span data-ttu-id="86172-106">Il cmdlet **Get-AzureRmEffectiveRouteTable** restituisce la tabella di route effettiva applicata a un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="86172-106">The **Get-AzureRmEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="86172-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="86172-107">EXAMPLES</span></span>

### <span data-ttu-id="86172-108">Esempio 1: ottenere la tabella di route effettiva in un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="86172-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="86172-109">Questo comando consente di ottenere la tabella di route effettiva associata all'interfaccia di rete denominata MyNetworkInterface nel gruppo di risorse denominato MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="86172-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="86172-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="86172-110">PARAMETERS</span></span>

### <span data-ttu-id="86172-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="86172-111">-AsJob</span></span>
<span data-ttu-id="86172-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="86172-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="86172-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86172-113">-DefaultProfile</span></span>
<span data-ttu-id="86172-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="86172-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86172-115">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="86172-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="86172-116">Specifica il nome di un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="86172-116">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="86172-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86172-117">-ResourceGroupName</span></span>
<span data-ttu-id="86172-118">Specifica il gruppo di risorse di un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="86172-118">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="86172-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86172-119">CommonParameters</span></span>
<span data-ttu-id="86172-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86172-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86172-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86172-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86172-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="86172-122">INPUTS</span></span>

### <span data-ttu-id="86172-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="86172-123">None</span></span>
<span data-ttu-id="86172-124">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="86172-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="86172-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="86172-125">OUTPUTS</span></span>

### <span data-ttu-id="86172-126">Microsoft. Azure. Commands. Network. Models. PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="86172-126">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="86172-127">Note</span><span class="sxs-lookup"><span data-stu-id="86172-127">NOTES</span></span>

## <span data-ttu-id="86172-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="86172-128">RELATED LINKS</span></span>

[<span data-ttu-id="86172-129">Get-AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="86172-129">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>](./Get-AzureRmEffectiveNetworkSecurityGroup.md)


