---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azipconfigurationbgppeeringaddressobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpConfigurationBgpPeeringAddressObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpConfigurationBgpPeeringAddressObject.md
ms.openlocfilehash: ba713650670abdeb9c64242109b30f47d99724f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001102"
---
# <span data-ttu-id="53b59-101">New-AzIpConfigurationBgpPeeringAddressObject</span><span class="sxs-lookup"><span data-stu-id="53b59-101">New-AzIpConfigurationBgpPeeringAddressObject</span></span>

## <span data-ttu-id="53b59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53b59-102">SYNOPSIS</span></span>
<span data-ttu-id="53b59-103">crea una nuova ipconfigurationBgpAddressingAddressObject</span><span class="sxs-lookup"><span data-stu-id="53b59-103">creates a new IpconfigurationBgpPeeringAddressObject</span></span>

## <span data-ttu-id="53b59-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="53b59-104">SYNTAX</span></span>

### <span data-ttu-id="53b59-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="53b59-105">Default (Default)</span></span>
```
New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId <String>
 -CustomAddress <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```
## <span data-ttu-id="53b59-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="53b59-106">DESCRIPTION</span></span>
<span data-ttu-id="53b59-107">**New-AzIpConfigurationBgpAddressingAddressObject** crea un oggetto IpConfigurationBgpAddressingAddressObject che rappresenta la proprietà BgpAddressingAddresses nel gateway di rete virtuale bgpsettings.</span><span class="sxs-lookup"><span data-stu-id="53b59-107">The **New-AzIpConfigurationBgpPeeringAddressObject** creates a IpConfigurationBgpPeeringAddressObject object which represents BgpPeeringAddresses property in your virtual network gateway bgpsettings.</span></span>

## <span data-ttu-id="53b59-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="53b59-108">EXAMPLES</span></span>

### <span data-ttu-id="53b59-109">1: Creare un AzIpConfigurationBgpAddressingAddressObject</span><span class="sxs-lookup"><span data-stu-id="53b59-109">1: Create a AzIpConfigurationBgpPeeringAddressObject</span></span>
```
$ipconfigurationId1 = '/subscriptions/c886bc58-0000-4e01-993f-e01ba3702aaf/resourceGroups/testRg/providers/Microsoft.Network/virtualNetworkGateways/gw1/ipConfigurations/default'
$addresslist1 = @('169.254.21.5')
$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddresses -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1
```

<span data-ttu-id="53b59-110">La procedura descritta sopra creerà un oggetto IpConfigurationBgpAddressingAddressObject.Questo nuovo oggetto sarà gw1ipconfBgp1.</span><span class="sxs-lookup"><span data-stu-id="53b59-110">The above will create a IpConfigurationBgpPeeringAddressObject.This new object will be to gw1ipconfBgp1.</span></span>

## <span data-ttu-id="53b59-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53b59-111">PARAMETERS</span></span>

### <span data-ttu-id="53b59-112">-Confirm</span><span class="sxs-lookup"><span data-stu-id="53b59-112">-Confirm</span></span>
<span data-ttu-id="53b59-113">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53b59-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53b59-114">-CustomAddress</span><span class="sxs-lookup"><span data-stu-id="53b59-114">-CustomAddress</span></span>
<span data-ttu-id="53b59-115">Elenco CustomAddress del gateway di rete virtuale per BgpAddressingAddresses.</span><span class="sxs-lookup"><span data-stu-id="53b59-115">The virtual network gateway CustomAddress List for BgpPeeringAddresses.</span></span>

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

### <span data-ttu-id="53b59-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53b59-116">-DefaultProfile</span></span>
<span data-ttu-id="53b59-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="53b59-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53b59-118">-IpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="53b59-118">-IpConfigurationId</span></span>
<span data-ttu-id="53b59-119">IpConfigurationId del gateway di rete virtuale per BgpAddressingAddresses.</span><span class="sxs-lookup"><span data-stu-id="53b59-119">The virtual network gateway IpConfigurationId for BgpPeeringAddresses.</span></span>

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

### <span data-ttu-id="53b59-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53b59-120">-WhatIf</span></span>
<span data-ttu-id="53b59-121">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="53b59-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53b59-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="53b59-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53b59-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53b59-123">CommonParameters</span></span>
<span data-ttu-id="53b59-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53b59-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53b59-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="53b59-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53b59-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="53b59-126">INPUTS</span></span>

### <span data-ttu-id="53b59-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="53b59-127">None</span></span>

## <span data-ttu-id="53b59-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="53b59-128">OUTPUTS</span></span>

### <span data-ttu-id="53b59-129">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpAddress</span><span class="sxs-lookup"><span data-stu-id="53b59-129">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress</span></span>

## <span data-ttu-id="53b59-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="53b59-130">NOTES</span></span>

## <span data-ttu-id="53b59-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="53b59-131">RELATED LINKS</span></span>
