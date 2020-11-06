---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientConfiguration.md
ms.openlocfilehash: 09c3862513b893003908b07992ae479656ba7ab1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521886"
---
# <span data-ttu-id="34131-101">Get-AzureRmVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="34131-101">Get-AzureRmVpnClientConfiguration</span></span>

## <span data-ttu-id="34131-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="34131-102">SYNOPSIS</span></span>
<span data-ttu-id="34131-103">Consente agli utenti di scaricare facilmente il pacchetto del profilo VPN generato tramite la New-AzureRmVpnClientConfiguration unifiedgroup.</span><span class="sxs-lookup"><span data-stu-id="34131-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzureRmVpnClientConfiguration commandlet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34131-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="34131-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34131-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="34131-105">DESCRIPTION</span></span>
<span data-ttu-id="34131-106">{{Fill nella descrizione}}</span><span class="sxs-lookup"><span data-stu-id="34131-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="34131-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="34131-107">EXAMPLES</span></span>

### <span data-ttu-id="34131-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="34131-108">Example 1</span></span>
```
PS C:\> New-AzureRmVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzureRmVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="34131-109">Ottiene l'URL per scaricare un profilo VpnClient che in precedenza è stato generato tramite il comando New-AzureRMVpnClientConfiguration.</span><span class="sxs-lookup"><span data-stu-id="34131-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzureRMVpnClientConfiguration command.</span></span>

## <span data-ttu-id="34131-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="34131-110">PARAMETERS</span></span>

### <span data-ttu-id="34131-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34131-111">-DefaultProfile</span></span>
<span data-ttu-id="34131-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="34131-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
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

### <span data-ttu-id="34131-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="34131-113">-Name</span></span>
<span data-ttu-id="34131-114">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="34131-114">The resource name.</span></span>

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

### <span data-ttu-id="34131-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34131-115">-ResourceGroupName</span></span>
<span data-ttu-id="34131-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="34131-116">The resource group name.</span></span>

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

### <span data-ttu-id="34131-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="34131-117">-Confirm</span></span>
<span data-ttu-id="34131-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34131-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34131-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34131-119">-WhatIf</span></span>
<span data-ttu-id="34131-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="34131-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="34131-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="34131-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34131-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34131-122">CommonParameters</span></span>
<span data-ttu-id="34131-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34131-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34131-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34131-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34131-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="34131-125">INPUTS</span></span>

### <span data-ttu-id="34131-126">System. String</span><span class="sxs-lookup"><span data-stu-id="34131-126">System.String</span></span>

## <span data-ttu-id="34131-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="34131-127">OUTPUTS</span></span>

### <span data-ttu-id="34131-128">Microsoft. Azure. Commands. Network. Models. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="34131-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="34131-129">Note</span><span class="sxs-lookup"><span data-stu-id="34131-129">NOTES</span></span>

## <span data-ttu-id="34131-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="34131-130">RELATED LINKS</span></span>

