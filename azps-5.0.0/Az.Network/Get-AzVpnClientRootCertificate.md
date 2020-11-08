---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 16754F70-9619-4F68-86E9-5C8B27812707
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRootCertificate.md
ms.openlocfilehash: 3cf1bea87824320b659def722d0d0f0166fa177d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203146"
---
# <span data-ttu-id="ce21f-101">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ce21f-101">Get-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="ce21f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ce21f-102">SYNOPSIS</span></span>
<span data-ttu-id="ce21f-103">Ottiene informazioni sui certificati radice VPN.</span><span class="sxs-lookup"><span data-stu-id="ce21f-103">Gets information about VPN root certificates.</span></span>

## <span data-ttu-id="ce21f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ce21f-104">SYNTAX</span></span>

```
Get-AzVpnClientRootCertificate [-VpnClientRootCertificateName <String>] -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce21f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ce21f-105">DESCRIPTION</span></span>
<span data-ttu-id="ce21f-106">Il cmdlet **Get-AzVpnClientRootCertificate** restituisce informazioni sui certificati radice assegnati a un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="ce21f-106">The **Get-AzVpnClientRootCertificate** cmdlet returns information about the root certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="ce21f-107">I certificati radice sono certificati X. 509 che identificano l'autorità di certificazione radice: tutti gli altri certificati usati nel gateway considerano attendibile il certificato radice.</span><span class="sxs-lookup"><span data-stu-id="ce21f-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="ce21f-108">Per impostazione predefinita, **Get-AzVpnClientRootCertificate** restituisce informazioni su tutti i certificati radice assegnati a un gateway.</span><span class="sxs-lookup"><span data-stu-id="ce21f-108">By default, **Get-AzVpnClientRootCertificate** returns information about all the root certificates assigned to a gateway.</span></span>
<span data-ttu-id="ce21f-109">I gateway possono avere più di un certificato radice. Tuttavia, includendo il parametro **VpnClientRootCertificateName** , puoi limitare i dati restituiti a un certificato specifico.</span><span class="sxs-lookup"><span data-stu-id="ce21f-109">(Gateways can have more than one root certificate.) However, by including the **VpnClientRootCertificateName** parameter you can limit the returned data to a specific certificate.</span></span>

## <span data-ttu-id="ce21f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ce21f-110">EXAMPLES</span></span>

### <span data-ttu-id="ce21f-111">Esempio 1: ottenere informazioni su tutti i certificati radice</span><span class="sxs-lookup"><span data-stu-id="ce21f-111">Example 1: Get information about all root certificates</span></span>
```
PS C:\>Get-AzVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="ce21f-112">Questo comando consente di ottenere informazioni su tutti i certificati radice assegnati a un gateway di rete virtuale denominato ContosoVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="ce21f-112">This command gets information about all the root certificates assigned to a virtual network gateway named ContosoVirtualNetwork.</span></span>

### <span data-ttu-id="ce21f-113">Esempio 2: ottenere informazioni su certificati radice specifici</span><span class="sxs-lookup"><span data-stu-id="ce21f-113">Example 2: Get information about specific root certificates</span></span>
```
PS C:\>Get-AzVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRootCertificateName "ContosoRootClientCertificate"
```

<span data-ttu-id="ce21f-114">Questo comando è una variante del comando mostrato nell'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="ce21f-114">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="ce21f-115">In questo caso, tuttavia, il parametro *VpnClientRootCertificateName* viene incluso per limitare i dati restituiti a un certificato radice specifico: ContosoRootClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="ce21f-115">In this case, however, the *VpnClientRootCertificateName* parameter is included in order to limit the returned data to a specific root certificate: ContosoRootClientCertificate.</span></span>

## <span data-ttu-id="ce21f-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ce21f-116">PARAMETERS</span></span>

### <span data-ttu-id="ce21f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce21f-117">-DefaultProfile</span></span>
<span data-ttu-id="ce21f-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ce21f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce21f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce21f-119">-ResourceGroupName</span></span>
<span data-ttu-id="ce21f-120">Specifica il nome del gruppo di risorse a cui è assegnato il gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="ce21f-120">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="ce21f-121">I gruppi di risorse categorizzano gli elementi per semplificare la gestione delle scorte e l'amministrazione generale di Azure.</span><span class="sxs-lookup"><span data-stu-id="ce21f-121">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="ce21f-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="ce21f-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="ce21f-123">Specifica il nome del gateway di rete virtuale in cui è assegnato il certificato radice.</span><span class="sxs-lookup"><span data-stu-id="ce21f-123">Specifies the name of the virtual network gateway where the root certificate is assigned.</span></span>

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

### <span data-ttu-id="ce21f-124">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="ce21f-124">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="ce21f-125">Specifica il nome del certificato radice client ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce21f-125">Specifies the name of the client root certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ce21f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce21f-126">CommonParameters</span></span>
<span data-ttu-id="ce21f-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce21f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce21f-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce21f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce21f-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ce21f-129">INPUTS</span></span>

### <span data-ttu-id="ce21f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ce21f-130">System.String</span></span>

## <span data-ttu-id="ce21f-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ce21f-131">OUTPUTS</span></span>

### <span data-ttu-id="ce21f-132">Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ce21f-132">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="ce21f-133">Note</span><span class="sxs-lookup"><span data-stu-id="ce21f-133">NOTES</span></span>

## <span data-ttu-id="ce21f-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ce21f-134">RELATED LINKS</span></span>

[<span data-ttu-id="ce21f-135">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ce21f-135">Add-AzVpnClientRootCertificate</span></span>](./Add-AzVpnClientRootCertificate.md)

[<span data-ttu-id="ce21f-136">New-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ce21f-136">New-AzVpnClientRootCertificate</span></span>](./New-AzVpnClientRootCertificate.md)

[<span data-ttu-id="ce21f-137">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ce21f-137">Remove-AzVpnClientRootCertificate</span></span>](./Remove-AzVpnClientRootCertificate.md)


