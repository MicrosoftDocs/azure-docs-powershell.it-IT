---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientConfiguration.md
ms.openlocfilehash: c91b42620d98cae3ecc5dcbd1f8a769c96675ade
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93853074"
---
# <span data-ttu-id="f40bb-101">Get-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="f40bb-101">Get-AzVpnClientConfiguration</span></span>

## <span data-ttu-id="f40bb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f40bb-102">SYNOPSIS</span></span>
<span data-ttu-id="f40bb-103">Consente agli utenti di scaricare facilmente il pacchetto del profilo VPN generato tramite la New-AzVpnClientConfiguration unifiedgroup.</span><span class="sxs-lookup"><span data-stu-id="f40bb-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzVpnClientConfiguration commandlet.</span></span>

## <span data-ttu-id="f40bb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f40bb-104">SYNTAX</span></span>

```
Get-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f40bb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f40bb-105">DESCRIPTION</span></span>
<span data-ttu-id="f40bb-106">Il Get-AzVpnClientConfiguration restituisce l'URL in cui è possibile scaricare il client VPN.</span><span class="sxs-lookup"><span data-stu-id="f40bb-106">The Get-AzVpnClientConfiguration returns the URL where the VPN client can be downloaded from.</span></span>

## <span data-ttu-id="f40bb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f40bb-107">EXAMPLES</span></span>

### <span data-ttu-id="f40bb-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f40bb-108">Example 1</span></span>
```
PS C:\> New-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="f40bb-109">Ottiene l'URL per scaricare un profilo VpnClient che in precedenza è stato generato tramite il comando New-AzVpnClientConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f40bb-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzVpnClientConfiguration command.</span></span>

## <span data-ttu-id="f40bb-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f40bb-110">PARAMETERS</span></span>

### <span data-ttu-id="f40bb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f40bb-111">-DefaultProfile</span></span>
<span data-ttu-id="f40bb-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f40bb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f40bb-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="f40bb-113">-Name</span></span>
<span data-ttu-id="f40bb-114">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="f40bb-114">The resource name.</span></span>

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

### <span data-ttu-id="f40bb-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f40bb-115">-ResourceGroupName</span></span>
<span data-ttu-id="f40bb-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f40bb-116">The resource group name.</span></span>

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

### <span data-ttu-id="f40bb-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f40bb-117">-Confirm</span></span>
<span data-ttu-id="f40bb-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f40bb-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f40bb-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f40bb-119">-WhatIf</span></span>
<span data-ttu-id="f40bb-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f40bb-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f40bb-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f40bb-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f40bb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f40bb-122">CommonParameters</span></span>
<span data-ttu-id="f40bb-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f40bb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f40bb-124">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f40bb-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f40bb-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f40bb-125">INPUTS</span></span>

### <span data-ttu-id="f40bb-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f40bb-126">System.String</span></span>

## <span data-ttu-id="f40bb-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f40bb-127">OUTPUTS</span></span>

### <span data-ttu-id="f40bb-128">Microsoft. Azure. Commands. Network. Models. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="f40bb-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="f40bb-129">Note</span><span class="sxs-lookup"><span data-stu-id="f40bb-129">NOTES</span></span>

## <span data-ttu-id="f40bb-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f40bb-130">RELATED LINKS</span></span>

[<span data-ttu-id="f40bb-131">New-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="f40bb-131">New-AzVpnClientConfiguration</span></span>](./New-AzVpnClientConfiguration.md)
