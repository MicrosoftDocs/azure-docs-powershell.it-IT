---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 16754F70-9619-4F68-86E9-5C8B27812707
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRootCertificate.md
ms.openlocfilehash: 6211b422e9dfc16358303d766edecf437b44240d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102016205"
---
# <span data-ttu-id="45b87-101">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="45b87-101">Get-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="45b87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45b87-102">SYNOPSIS</span></span>
<span data-ttu-id="45b87-103">Recupera informazioni sui certificati radice VPN.</span><span class="sxs-lookup"><span data-stu-id="45b87-103">Gets information about VPN root certificates.</span></span>

## <span data-ttu-id="45b87-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="45b87-104">SYNTAX</span></span>

```
Get-AzVpnClientRootCertificate [-VpnClientRootCertificateName <String>] -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45b87-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="45b87-105">DESCRIPTION</span></span>
<span data-ttu-id="45b87-106">Il cmdlet **Get-AzVpnClientRootCertificate** restituisce informazioni sui certificati radice assegnati a un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="45b87-106">The **Get-AzVpnClientRootCertificate** cmdlet returns information about the root certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="45b87-107">I certificati radice sono certificati X.509 che identificano l'Autorità di certificazione radice: tutti gli altri certificati usati nel gateway considera attendibili il certificato radice.</span><span class="sxs-lookup"><span data-stu-id="45b87-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="45b87-108">Per impostazione predefinita, **Get-AzVpnClientRootCertificate** restituisce informazioni su tutti i certificati radice assegnati a un gateway.</span><span class="sxs-lookup"><span data-stu-id="45b87-108">By default, **Get-AzVpnClientRootCertificate** returns information about all the root certificates assigned to a gateway.</span></span>
<span data-ttu-id="45b87-109">I gateway possono avere più certificati radice. Tuttavia, includendo il **parametro VpnClientRootCertificateName,** è possibile limitare i dati restituiti a un certificato specifico.</span><span class="sxs-lookup"><span data-stu-id="45b87-109">(Gateways can have more than one root certificate.) However, by including the **VpnClientRootCertificateName** parameter you can limit the returned data to a specific certificate.</span></span>

## <span data-ttu-id="45b87-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="45b87-110">EXAMPLES</span></span>

### <span data-ttu-id="45b87-111">Esempio 1: Ottenere informazioni su tutti i certificati radice</span><span class="sxs-lookup"><span data-stu-id="45b87-111">Example 1: Get information about all root certificates</span></span>
```
PS C:\>Get-AzVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="45b87-112">Questo comando recupera informazioni su tutti i certificati radice assegnati a un gateway di rete virtuale denominato ContosoVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="45b87-112">This command gets information about all the root certificates assigned to a virtual network gateway named ContosoVirtualNetwork.</span></span>

### <span data-ttu-id="45b87-113">Esempio 2: Ottenere informazioni su certificati radice specifici</span><span class="sxs-lookup"><span data-stu-id="45b87-113">Example 2: Get information about specific root certificates</span></span>
```
PS C:\>Get-AzVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRootCertificateName "ContosoRootClientCertificate"
```

<span data-ttu-id="45b87-114">Questo comando è una variante del comando mostrato nell'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="45b87-114">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="45b87-115">In questo caso, tuttavia, il parametro *VpnClientRootCertificateName* è incluso per limitare i dati restituiti a uno specifico certificato radice: ContosoRootClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="45b87-115">In this case, however, the *VpnClientRootCertificateName* parameter is included in order to limit the returned data to a specific root certificate: ContosoRootClientCertificate.</span></span>

## <span data-ttu-id="45b87-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45b87-116">PARAMETERS</span></span>

### <span data-ttu-id="45b87-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45b87-117">-DefaultProfile</span></span>
<span data-ttu-id="45b87-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="45b87-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45b87-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45b87-119">-ResourceGroupName</span></span>
<span data-ttu-id="45b87-120">Specifica il nome del gruppo di risorse a cui è assegnato il gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="45b87-120">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="45b87-121">I gruppi di risorse categorizzano gli articoli per semplificare la gestione dell'inventario e l'amministrazione generale di Azure.</span><span class="sxs-lookup"><span data-stu-id="45b87-121">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="45b87-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="45b87-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="45b87-123">Specifica il nome del gateway di rete virtuale a cui è assegnato il certificato radice.</span><span class="sxs-lookup"><span data-stu-id="45b87-123">Specifies the name of the virtual network gateway where the root certificate is assigned.</span></span>

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

### <span data-ttu-id="45b87-124">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="45b87-124">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="45b87-125">Specifica il nome del certificato radice client che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45b87-125">Specifies the name of the client root certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="45b87-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45b87-126">CommonParameters</span></span>
<span data-ttu-id="45b87-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45b87-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45b87-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="45b87-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45b87-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="45b87-129">INPUTS</span></span>

### <span data-ttu-id="45b87-130">System.String</span><span class="sxs-lookup"><span data-stu-id="45b87-130">System.String</span></span>

## <span data-ttu-id="45b87-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="45b87-131">OUTPUTS</span></span>

### <span data-ttu-id="45b87-132">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="45b87-132">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="45b87-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="45b87-133">NOTES</span></span>

## <span data-ttu-id="45b87-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="45b87-134">RELATED LINKS</span></span>

[<span data-ttu-id="45b87-135">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="45b87-135">Add-AzVpnClientRootCertificate</span></span>](./Add-AzVpnClientRootCertificate.md)

[<span data-ttu-id="45b87-136">New-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="45b87-136">New-AzVpnClientRootCertificate</span></span>](./New-AzVpnClientRootCertificate.md)

[<span data-ttu-id="45b87-137">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="45b87-137">Remove-AzVpnClientRootCertificate</span></span>](./Remove-AzVpnClientRootCertificate.md)


