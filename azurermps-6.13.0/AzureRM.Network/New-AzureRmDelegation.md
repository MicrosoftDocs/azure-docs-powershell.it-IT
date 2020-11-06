---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmDelegation.md
ms.openlocfilehash: 9912d41cd9e2600c55d378fbb88510a0defaaa85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519258"
---
# <span data-ttu-id="20a94-101">New-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="20a94-101">New-AzureRmDelegation</span></span>

## <span data-ttu-id="20a94-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="20a94-102">SYNOPSIS</span></span>
<span data-ttu-id="20a94-103">Crea una delega di servizio.</span><span class="sxs-lookup"><span data-stu-id="20a94-103">Creates a service delegation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20a94-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="20a94-104">SYNTAX</span></span>

```
New-AzureRmDelegation -Name <String> -ServiceName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="20a94-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20a94-105">DESCRIPTION</span></span>
<span data-ttu-id="20a94-106">Il cmdlet **New-AzureRmDelegation** crea una delega del servizio che può essere aggiunta a una subnet.</span><span class="sxs-lookup"><span data-stu-id="20a94-106">The **New-AzureRmDelegation** cmdlet creates a service delegation that can be added to a subnet.</span></span>

## <span data-ttu-id="20a94-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="20a94-107">EXAMPLES</span></span>

### <span data-ttu-id="20a94-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="20a94-108">Example 1</span></span>
```powershell
PS C:\> $delegation = New-AzureRmDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet.Delegations.Add($delegation)
PS C:\> Set-AzureRmVirtualNetwork $vnet
```

<span data-ttu-id="20a94-109">Il primo cmdlet crea una delega che può essere aggiunta a una subnet e la archivia nella variabile $delegation.</span><span class="sxs-lookup"><span data-stu-id="20a94-109">The first cmdlet creates a delegation that can be added to a subnet, and stores it in the $delegation variable.</span></span> <span data-ttu-id="20a94-110">Il secondo e il terzo cmdlet recuperano la subnet da delegare.</span><span class="sxs-lookup"><span data-stu-id="20a94-110">The second and third cmdlets retrieve the subnet to be delegated.</span></span> <span data-ttu-id="20a94-111">Il quarto cmdlet aggiunge la delega creata alla subnet di interesse e il cmdlet finale Invia la configurazione aggiornata al server.</span><span class="sxs-lookup"><span data-stu-id="20a94-111">The fourth cmdlet adds the created delegation to the subnet of interest, and the final cmdlet sends the updated configuration to the server.</span></span>

## <span data-ttu-id="20a94-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="20a94-112">PARAMETERS</span></span>

### <span data-ttu-id="20a94-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20a94-113">-DefaultProfile</span></span>
<span data-ttu-id="20a94-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="20a94-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20a94-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="20a94-115">-Name</span></span>
<span data-ttu-id="20a94-116">Nome della delega</span><span class="sxs-lookup"><span data-stu-id="20a94-116">The name of the delegation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20a94-117">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="20a94-117">-ServiceName</span></span>
<span data-ttu-id="20a94-118">Nome del servizio a cui la subnet deve essere delegata</span><span class="sxs-lookup"><span data-stu-id="20a94-118">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="20a94-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20a94-119">CommonParameters</span></span>
<span data-ttu-id="20a94-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20a94-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="20a94-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20a94-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20a94-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="20a94-122">INPUTS</span></span>

### <span data-ttu-id="20a94-123">System. String</span><span class="sxs-lookup"><span data-stu-id="20a94-123">System.String</span></span>

## <span data-ttu-id="20a94-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="20a94-124">OUTPUTS</span></span>

### <span data-ttu-id="20a94-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span><span class="sxs-lookup"><span data-stu-id="20a94-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="20a94-126">Note</span><span class="sxs-lookup"><span data-stu-id="20a94-126">NOTES</span></span>

## <span data-ttu-id="20a94-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="20a94-127">RELATED LINKS</span></span>
<span data-ttu-id="20a94-128">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md) 
 [Get-AzureRmDelegation](./Get-AzureRmDelegation.md) 
 [Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md) 
 [Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md) 
 [Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md) 
 [Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="20a94-128">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md)
[Get-AzureRmDelegation](./Get-AzureRmDelegation.md)
[Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md)
[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md)
[Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)
[Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span></span>
