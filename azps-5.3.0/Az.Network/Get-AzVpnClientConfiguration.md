---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientConfiguration.md
ms.openlocfilehash: ba73b61d34e0f6422defb9e9d6f84c22945ec124
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379693"
---
# <span data-ttu-id="16506-101">Get-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="16506-101">Get-AzVpnClientConfiguration</span></span>

## <span data-ttu-id="16506-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="16506-102">SYNOPSIS</span></span>
<span data-ttu-id="16506-103">Consente agli utenti di scaricare facilmente il pacchetto del profilo VPN generato tramite la New-AzVpnClientConfiguration unifiedgroup.</span><span class="sxs-lookup"><span data-stu-id="16506-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzVpnClientConfiguration commandlet.</span></span>

## <span data-ttu-id="16506-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="16506-104">SYNTAX</span></span>

```
Get-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16506-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16506-105">DESCRIPTION</span></span>
<span data-ttu-id="16506-106">Il Get-AzVpnClientConfiguration restituisce l'URL in cui è possibile scaricare il client VPN.</span><span class="sxs-lookup"><span data-stu-id="16506-106">The Get-AzVpnClientConfiguration returns the URL where the VPN client can be downloaded from.</span></span>

## <span data-ttu-id="16506-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="16506-107">EXAMPLES</span></span>

### <span data-ttu-id="16506-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="16506-108">Example 1</span></span>
```
PS C:\> New-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="16506-109">Ottiene l'URL per scaricare un profilo VpnClient che in precedenza è stato generato tramite il comando New-AzVpnClientConfiguration.</span><span class="sxs-lookup"><span data-stu-id="16506-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzVpnClientConfiguration command.</span></span>

## <span data-ttu-id="16506-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="16506-110">PARAMETERS</span></span>

### <span data-ttu-id="16506-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16506-111">-DefaultProfile</span></span>
<span data-ttu-id="16506-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="16506-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16506-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="16506-113">-Name</span></span>
<span data-ttu-id="16506-114">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="16506-114">The resource name.</span></span>

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

### <span data-ttu-id="16506-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16506-115">-ResourceGroupName</span></span>
<span data-ttu-id="16506-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="16506-116">The resource group name.</span></span>

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

### <span data-ttu-id="16506-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="16506-117">-Confirm</span></span>
<span data-ttu-id="16506-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16506-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16506-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16506-119">-WhatIf</span></span>
<span data-ttu-id="16506-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="16506-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="16506-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="16506-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16506-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16506-122">CommonParameters</span></span>
<span data-ttu-id="16506-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16506-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16506-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="16506-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16506-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="16506-125">INPUTS</span></span>

### <span data-ttu-id="16506-126">System. String</span><span class="sxs-lookup"><span data-stu-id="16506-126">System.String</span></span>

## <span data-ttu-id="16506-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="16506-127">OUTPUTS</span></span>

### <span data-ttu-id="16506-128">Microsoft. Azure. Commands. Network. Models. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="16506-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="16506-129">Note</span><span class="sxs-lookup"><span data-stu-id="16506-129">NOTES</span></span>

## <span data-ttu-id="16506-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="16506-130">RELATED LINKS</span></span>

[<span data-ttu-id="16506-131">New-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="16506-131">New-AzVpnClientConfiguration</span></span>](./New-AzVpnClientConfiguration.md)
