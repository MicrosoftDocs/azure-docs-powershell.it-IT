---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipconfigurationbgppeeringaddressobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpConfigurationBgpPeeringAddressObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpConfigurationBgpPeeringAddressObject.md
ms.openlocfilehash: 2a31aa9db3264dd24c6d77bdad7b10d6ecad10b1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200734"
---
# <span data-ttu-id="5b564-101">New-AzIpConfigurationBgpPeeringAddressObject</span><span class="sxs-lookup"><span data-stu-id="5b564-101">New-AzIpConfigurationBgpPeeringAddressObject</span></span>

## <span data-ttu-id="5b564-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5b564-102">SYNOPSIS</span></span>
<span data-ttu-id="5b564-103">Crea un nuovo IpconfigurationBgpPeeringAddressObject</span><span class="sxs-lookup"><span data-stu-id="5b564-103">creates a new IpconfigurationBgpPeeringAddressObject</span></span>

## <span data-ttu-id="5b564-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5b564-104">SYNTAX</span></span>

### <span data-ttu-id="5b564-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5b564-105">Default (Default)</span></span>
```
New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId <String>
 -CustomAddress <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```
## <span data-ttu-id="5b564-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5b564-106">DESCRIPTION</span></span>
<span data-ttu-id="5b564-107">Il **nuovo AzIpConfigurationBgpPeeringAddressObject** crea un oggetto IpConfigurationBgpPeeringAddressObject che rappresenta la proprietà BgpPeeringAddresses nel gateway di rete virtuale bgpsettings.</span><span class="sxs-lookup"><span data-stu-id="5b564-107">The **New-AzIpConfigurationBgpPeeringAddressObject** creates a IpConfigurationBgpPeeringAddressObject object which represents BgpPeeringAddresses property in your virtual network gateway bgpsettings.</span></span>

## <span data-ttu-id="5b564-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5b564-108">EXAMPLES</span></span>

### <span data-ttu-id="5b564-109">1: creare un AzIpConfigurationBgpPeeringAddressObject</span><span class="sxs-lookup"><span data-stu-id="5b564-109">1: Create a AzIpConfigurationBgpPeeringAddressObject</span></span>
```
$ipconfigurationId1 = '/subscriptions/c886bc58-0000-4e01-993f-e01ba3702aaf/resourceGroups/testRg/providers/Microsoft.Network/virtualNetworkGateways/gw1/ipConfigurations/default'
$addresslist1 = @('169.254.21.5')
$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddresses -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1
```

<span data-ttu-id="5b564-110">Quanto sopra creerà un IpConfigurationBgpPeeringAddressObject. questo nuovo oggetto sarà gw1ipconfBgp1.</span><span class="sxs-lookup"><span data-stu-id="5b564-110">The above will create a IpConfigurationBgpPeeringAddressObject.This new object will be to gw1ipconfBgp1.</span></span>

## <span data-ttu-id="5b564-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5b564-111">PARAMETERS</span></span>

### <span data-ttu-id="5b564-112">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5b564-112">-Confirm</span></span>
<span data-ttu-id="5b564-113">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b564-113">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b564-114">-CustomAddress</span><span class="sxs-lookup"><span data-stu-id="5b564-114">-CustomAddress</span></span>
<span data-ttu-id="5b564-115">Elenco di CustomAddress di Virtual Network Gateway per BgpPeeringAddresses.</span><span class="sxs-lookup"><span data-stu-id="5b564-115">The virtual network gateway CustomAddress List for BgpPeeringAddresses.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b564-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b564-116">-DefaultProfile</span></span>
<span data-ttu-id="5b564-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5b564-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b564-118">-IpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="5b564-118">-IpConfigurationId</span></span>
<span data-ttu-id="5b564-119">Il gateway di rete virtuale IpConfigurationId per BgpPeeringAddresses.</span><span class="sxs-lookup"><span data-stu-id="5b564-119">The virtual network gateway IpConfigurationId for BgpPeeringAddresses.</span></span>

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

### <span data-ttu-id="5b564-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b564-120">-WhatIf</span></span>
<span data-ttu-id="5b564-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5b564-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b564-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5b564-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b564-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b564-123">CommonParameters</span></span>
<span data-ttu-id="5b564-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b564-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b564-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5b564-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b564-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5b564-126">INPUTS</span></span>

### <span data-ttu-id="5b564-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="5b564-127">None</span></span>

## <span data-ttu-id="5b564-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5b564-128">OUTPUTS</span></span>

### <span data-ttu-id="5b564-129">Microsoft. Azure. Commands. Network. Models. PSIpConfigurationBgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="5b564-129">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress</span></span>

## <span data-ttu-id="5b564-130">Note</span><span class="sxs-lookup"><span data-stu-id="5b564-130">NOTES</span></span>

## <span data-ttu-id="5b564-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5b564-131">RELATED LINKS</span></span>