---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermeffectiveroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveRouteTable.md
ms.openlocfilehash: 8095e2ebd1d9e55e8f5bc847f4a72277363e197a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520935"
---
# <span data-ttu-id="713e7-101">Get-AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="713e7-101">Get-AzureRmEffectiveRouteTable</span></span>

## <span data-ttu-id="713e7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="713e7-102">SYNOPSIS</span></span>
<span data-ttu-id="713e7-103">Ottiene la tabella di route effettiva di un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="713e7-103">Gets the effective route table of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="713e7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="713e7-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="713e7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="713e7-105">DESCRIPTION</span></span>
<span data-ttu-id="713e7-106">Il cmdlet **Get-AzureRmEffectiveRouteTable** restituisce la tabella di route effettiva applicata a un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="713e7-106">The **Get-AzureRmEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="713e7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="713e7-107">EXAMPLES</span></span>

### <span data-ttu-id="713e7-108">Esempio 1: ottenere la tabella di route effettiva in un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="713e7-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="713e7-109">Questo comando consente di ottenere la tabella di route effettiva associata all'interfaccia di rete denominata MyNetworkInterface nel gruppo di risorse denominato MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="713e7-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="713e7-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="713e7-110">PARAMETERS</span></span>

### <span data-ttu-id="713e7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="713e7-111">-AsJob</span></span>
<span data-ttu-id="713e7-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="713e7-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="713e7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="713e7-113">-DefaultProfile</span></span>
<span data-ttu-id="713e7-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="713e7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="713e7-115">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="713e7-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="713e7-116">Specifica il nome di un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="713e7-116">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="713e7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="713e7-117">-ResourceGroupName</span></span>
<span data-ttu-id="713e7-118">Specifica il gruppo di risorse di un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="713e7-118">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="713e7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="713e7-119">CommonParameters</span></span>
<span data-ttu-id="713e7-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="713e7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="713e7-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="713e7-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="713e7-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="713e7-122">INPUTS</span></span>

### <span data-ttu-id="713e7-123">System. String</span><span class="sxs-lookup"><span data-stu-id="713e7-123">System.String</span></span>

## <span data-ttu-id="713e7-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="713e7-124">OUTPUTS</span></span>

### <span data-ttu-id="713e7-125">Microsoft. Azure. Commands. Network. Models. PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="713e7-125">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="713e7-126">Note</span><span class="sxs-lookup"><span data-stu-id="713e7-126">NOTES</span></span>

## <span data-ttu-id="713e7-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="713e7-127">RELATED LINKS</span></span>

[<span data-ttu-id="713e7-128">Get-AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="713e7-128">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>](./Get-AzureRmEffectiveNetworkSecurityGroup.md)


