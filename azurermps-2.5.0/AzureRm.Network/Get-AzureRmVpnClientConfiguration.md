---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientconfiguration
schema: 2.0.0
ms.openlocfilehash: 4d6e95534cdadd694fa2ed87d43d3f7387ec9b20
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866070"
---
# <span data-ttu-id="0ec7f-101">Get-AzureRmVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="0ec7f-101">Get-AzureRmVpnClientConfiguration</span></span>

## <span data-ttu-id="0ec7f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0ec7f-102">SYNOPSIS</span></span>
<span data-ttu-id="0ec7f-103">Consente agli utenti di scaricare facilmente il pacchetto del profilo VPN generato tramite la New-AzureRmVpnClientConfiguration unifiedgroup.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzureRmVpnClientConfiguration commandlet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ec7f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0ec7f-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ec7f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0ec7f-105">DESCRIPTION</span></span>
<span data-ttu-id="0ec7f-106">{{Fill nella descrizione}}</span><span class="sxs-lookup"><span data-stu-id="0ec7f-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="0ec7f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0ec7f-107">EXAMPLES</span></span>

### <span data-ttu-id="0ec7f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0ec7f-108">Example 1</span></span>
```
PS C:\> New-AzureRmVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzureRmVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="0ec7f-109">Ottiene l'URL per scaricare un profilo VpnClient che in precedenza è stato generato tramite il comando New-AzureRMVpnClientConfiguration.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzureRMVpnClientConfiguration command.</span></span>

## <span data-ttu-id="0ec7f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0ec7f-110">PARAMETERS</span></span>

### <span data-ttu-id="0ec7f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ec7f-111">-DefaultProfile</span></span>
<span data-ttu-id="0ec7f-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
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

### <span data-ttu-id="0ec7f-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="0ec7f-113">-Name</span></span>
<span data-ttu-id="0ec7f-114">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-114">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ec7f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ec7f-115">-ResourceGroupName</span></span>
<span data-ttu-id="0ec7f-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-116">The resource group name.</span></span>

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

### <span data-ttu-id="0ec7f-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0ec7f-117">-Confirm</span></span>
<span data-ttu-id="0ec7f-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ec7f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ec7f-119">-WhatIf</span></span>
<span data-ttu-id="0ec7f-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0ec7f-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ec7f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ec7f-122">CommonParameters</span></span>
<span data-ttu-id="0ec7f-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ec7f-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ec7f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ec7f-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0ec7f-125">INPUTS</span></span>

### <span data-ttu-id="0ec7f-126">System. String</span><span class="sxs-lookup"><span data-stu-id="0ec7f-126">System.String</span></span>

## <span data-ttu-id="0ec7f-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0ec7f-127">OUTPUTS</span></span>

### <span data-ttu-id="0ec7f-128">Microsoft. Azure. Commands. Network. Models. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="0ec7f-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="0ec7f-129">Note</span><span class="sxs-lookup"><span data-stu-id="0ec7f-129">NOTES</span></span>

## <span data-ttu-id="0ec7f-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0ec7f-130">RELATED LINKS</span></span>

