---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientConfiguration.md
ms.openlocfilehash: 9ab4af1eefa6214d43eca84f65053eeecb12d912
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513739"
---
# <span data-ttu-id="facf4-101">Get-AzureRmVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="facf4-101">Get-AzureRmVpnClientConfiguration</span></span>

## <span data-ttu-id="facf4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="facf4-102">SYNOPSIS</span></span>
<span data-ttu-id="facf4-103">Consente agli utenti di scaricare facilmente il pacchetto del profilo VPN generato tramite la New-AzureRmVpnClientConfiguration unifiedgroup.</span><span class="sxs-lookup"><span data-stu-id="facf4-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzureRmVpnClientConfiguration commandlet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="facf4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="facf4-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="facf4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="facf4-105">DESCRIPTION</span></span>
<span data-ttu-id="facf4-106">Il Get-AzureRmVpnClientConfiguration restituisce l'URL in cui è possibile scaricare il client VPN.</span><span class="sxs-lookup"><span data-stu-id="facf4-106">The Get-AzureRmVpnClientConfiguration returns the URL where the VPN client can be downloaded from.</span></span>

## <span data-ttu-id="facf4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="facf4-107">EXAMPLES</span></span>

### <span data-ttu-id="facf4-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="facf4-108">Example 1</span></span>
```
PS C:\> New-AzureRmVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzureRmVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="facf4-109">Ottiene l'URL per scaricare un profilo VpnClient che in precedenza è stato generato tramite il comando New-AzureRMVpnClientConfiguration.</span><span class="sxs-lookup"><span data-stu-id="facf4-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzureRMVpnClientConfiguration command.</span></span>

## <span data-ttu-id="facf4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="facf4-110">PARAMETERS</span></span>

### <span data-ttu-id="facf4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="facf4-111">-DefaultProfile</span></span>
<span data-ttu-id="facf4-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="facf4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="facf4-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="facf4-113">-Name</span></span>
<span data-ttu-id="facf4-114">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="facf4-114">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="facf4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="facf4-115">-ResourceGroupName</span></span>
<span data-ttu-id="facf4-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="facf4-116">The resource group name.</span></span>

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

### <span data-ttu-id="facf4-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="facf4-117">-Confirm</span></span>
<span data-ttu-id="facf4-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="facf4-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="facf4-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="facf4-119">-WhatIf</span></span>
<span data-ttu-id="facf4-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="facf4-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="facf4-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="facf4-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="facf4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="facf4-122">CommonParameters</span></span>
<span data-ttu-id="facf4-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="facf4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="facf4-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="facf4-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="facf4-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="facf4-125">INPUTS</span></span>

### <span data-ttu-id="facf4-126">System. String</span><span class="sxs-lookup"><span data-stu-id="facf4-126">System.String</span></span>

## <span data-ttu-id="facf4-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="facf4-127">OUTPUTS</span></span>

### <span data-ttu-id="facf4-128">Microsoft. Azure. Commands. Network. Models. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="facf4-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="facf4-129">Note</span><span class="sxs-lookup"><span data-stu-id="facf4-129">NOTES</span></span>

## <span data-ttu-id="facf4-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="facf4-130">RELATED LINKS</span></span>
