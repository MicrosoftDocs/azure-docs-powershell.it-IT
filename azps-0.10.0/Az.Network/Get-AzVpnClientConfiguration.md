---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVpnClientConfiguration.md
ms.openlocfilehash: 63b044c4a9736aca72e9713cd8ec5833e7b056ab
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860638"
---
# <span data-ttu-id="e2da1-101">Get-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2da1-101">Get-AzVpnClientConfiguration</span></span>

## <span data-ttu-id="e2da1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e2da1-102">SYNOPSIS</span></span>
<span data-ttu-id="e2da1-103">Consente agli utenti di scaricare facilmente il pacchetto del profilo VPN generato tramite la New-AzVpnClientConfiguration unifiedgroup.</span><span class="sxs-lookup"><span data-stu-id="e2da1-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzVpnClientConfiguration commandlet.</span></span>

## <span data-ttu-id="e2da1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e2da1-104">SYNTAX</span></span>

```
Get-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2da1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e2da1-105">DESCRIPTION</span></span>
<span data-ttu-id="e2da1-106">{{Fill nella descrizione}}</span><span class="sxs-lookup"><span data-stu-id="e2da1-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="e2da1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e2da1-107">EXAMPLES</span></span>

### <span data-ttu-id="e2da1-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e2da1-108">Example 1</span></span>
```
PS C:\> New-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="e2da1-109">Ottiene l'URL per scaricare un profilo VpnClient che in precedenza è stato generato tramite il comando New-AzVpnClientConfiguration.</span><span class="sxs-lookup"><span data-stu-id="e2da1-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzVpnClientConfiguration command.</span></span>

## <span data-ttu-id="e2da1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e2da1-110">PARAMETERS</span></span>

### <span data-ttu-id="e2da1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2da1-111">-DefaultProfile</span></span>
<span data-ttu-id="e2da1-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e2da1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
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

### <span data-ttu-id="e2da1-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="e2da1-113">-Name</span></span>
<span data-ttu-id="e2da1-114">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="e2da1-114">The resource name.</span></span>

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

### <span data-ttu-id="e2da1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2da1-115">-ResourceGroupName</span></span>
<span data-ttu-id="e2da1-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e2da1-116">The resource group name.</span></span>

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

### <span data-ttu-id="e2da1-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e2da1-117">-Confirm</span></span>
<span data-ttu-id="e2da1-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2da1-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2da1-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2da1-119">-WhatIf</span></span>
<span data-ttu-id="e2da1-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e2da1-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e2da1-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e2da1-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2da1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2da1-122">CommonParameters</span></span>
<span data-ttu-id="e2da1-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2da1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2da1-124">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2da1-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2da1-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e2da1-125">INPUTS</span></span>

### <span data-ttu-id="e2da1-126">System. String</span><span class="sxs-lookup"><span data-stu-id="e2da1-126">System.String</span></span>

## <span data-ttu-id="e2da1-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e2da1-127">OUTPUTS</span></span>

### <span data-ttu-id="e2da1-128">Microsoft. Azure. Commands. Network. Models. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="e2da1-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="e2da1-129">Note</span><span class="sxs-lookup"><span data-stu-id="e2da1-129">NOTES</span></span>

## <span data-ttu-id="e2da1-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e2da1-130">RELATED LINKS</span></span>

