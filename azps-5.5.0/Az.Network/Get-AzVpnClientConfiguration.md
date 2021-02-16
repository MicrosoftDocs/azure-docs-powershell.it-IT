---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientConfiguration.md
ms.openlocfilehash: ba73b61d34e0f6422defb9e9d6f84c22945ec124
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191919"
---
# <span data-ttu-id="0ad4a-101">Get-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="0ad4a-101">Get-AzVpnClientConfiguration</span></span>

## <span data-ttu-id="0ad4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ad4a-102">SYNOPSIS</span></span>
<span data-ttu-id="0ad4a-103">Consente agli utenti di scaricare facilmente il pacchetto del profilo Vpn generato con il New-AzVpnClientConfiguration let.</span><span class="sxs-lookup"><span data-stu-id="0ad4a-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzVpnClientConfiguration commandlet.</span></span>

## <span data-ttu-id="0ad4a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0ad4a-104">SYNTAX</span></span>

```
Get-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ad4a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0ad4a-105">DESCRIPTION</span></span>
<span data-ttu-id="0ad4a-106">LGet-AzVpnClientConfiguration restituisce l'URL da cui è possibile scaricare il client VPN.</span><span class="sxs-lookup"><span data-stu-id="0ad4a-106">The Get-AzVpnClientConfiguration returns the URL where the VPN client can be downloaded from.</span></span>

## <span data-ttu-id="0ad4a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0ad4a-107">EXAMPLES</span></span>

### <span data-ttu-id="0ad4a-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0ad4a-108">Example 1</span></span>
```
PS C:\> New-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="0ad4a-109">Recupera l'URL per scaricare un profilo VpnClient generato in precedenza con il comando New-AzVpnClientConfiguration></span><span class="sxs-lookup"><span data-stu-id="0ad4a-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzVpnClientConfiguration command.</span></span>

## <span data-ttu-id="0ad4a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ad4a-110">PARAMETERS</span></span>

### <span data-ttu-id="0ad4a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ad4a-111">-DefaultProfile</span></span>
<span data-ttu-id="0ad4a-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0ad4a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ad4a-113">-Name</span><span class="sxs-lookup"><span data-stu-id="0ad4a-113">-Name</span></span>
<span data-ttu-id="0ad4a-114">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="0ad4a-114">The resource name.</span></span>

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

### <span data-ttu-id="0ad4a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ad4a-115">-ResourceGroupName</span></span>
<span data-ttu-id="0ad4a-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0ad4a-116">The resource group name.</span></span>

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

### <span data-ttu-id="0ad4a-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0ad4a-117">-Confirm</span></span>
<span data-ttu-id="0ad4a-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ad4a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ad4a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ad4a-119">-WhatIf</span></span>
<span data-ttu-id="0ad4a-120">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0ad4a-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0ad4a-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0ad4a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ad4a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ad4a-122">CommonParameters</span></span>
<span data-ttu-id="0ad4a-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ad4a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ad4a-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0ad4a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ad4a-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="0ad4a-125">INPUTS</span></span>

### <span data-ttu-id="0ad4a-126">System.String</span><span class="sxs-lookup"><span data-stu-id="0ad4a-126">System.String</span></span>

## <span data-ttu-id="0ad4a-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0ad4a-127">OUTPUTS</span></span>

### <span data-ttu-id="0ad4a-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="0ad4a-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="0ad4a-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="0ad4a-129">NOTES</span></span>

## <span data-ttu-id="0ad4a-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0ad4a-130">RELATED LINKS</span></span>

[<span data-ttu-id="0ad4a-131">New-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="0ad4a-131">New-AzVpnClientConfiguration</span></span>](./New-AzVpnClientConfiguration.md)
