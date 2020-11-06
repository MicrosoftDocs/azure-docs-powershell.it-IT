---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 16754F70-9619-4F68-86E9-5C8B27812707
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientRootCertificate.md
ms.openlocfilehash: 14fcaa1d52d2491d807e654d98308236bf901d3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514696"
---
# <span data-ttu-id="a4c54-101">Get-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a4c54-101">Get-AzureRmVpnClientRootCertificate</span></span>

## <span data-ttu-id="a4c54-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a4c54-102">SYNOPSIS</span></span>
<span data-ttu-id="a4c54-103">Ottiene informazioni sui certificati radice VPN.</span><span class="sxs-lookup"><span data-stu-id="a4c54-103">Gets information about VPN root certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4c54-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a4c54-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientRootCertificate [-VpnClientRootCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4c54-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a4c54-105">DESCRIPTION</span></span>
<span data-ttu-id="a4c54-106">Il cmdlet **Get-AzureRmVpnClientRootCertificate** restituisce informazioni sui certificati radice assegnati a un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="a4c54-106">The **Get-AzureRmVpnClientRootCertificate** cmdlet returns information about the root certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="a4c54-107">I certificati radice sono certificati X. 509 che identificano l'autorità di certificazione radice: tutti gli altri certificati usati nel gateway considerano attendibile il certificato radice.</span><span class="sxs-lookup"><span data-stu-id="a4c54-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>

<span data-ttu-id="a4c54-108">Per impostazione predefinita, **Get-AzureRmVpnClientRootCertificate** restituisce informazioni su tutti i certificati radice assegnati a un gateway.</span><span class="sxs-lookup"><span data-stu-id="a4c54-108">By default, **Get-AzureRmVpnClientRootCertificate** returns information about all the root certificates assigned to a gateway.</span></span>
<span data-ttu-id="a4c54-109">I gateway possono avere più di un certificato radice. Tuttavia, includendo il parametro **VpnClientRootCertificateName** , puoi limitare i dati restituiti a un certificato specifico.</span><span class="sxs-lookup"><span data-stu-id="a4c54-109">(Gateways can have more than one root certificate.) However, by including the **VpnClientRootCertificateName** parameter you can limit the returned data to a specific certificate.</span></span>

## <span data-ttu-id="a4c54-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a4c54-110">EXAMPLES</span></span>

### <span data-ttu-id="a4c54-111">Esempio 1: ottenere informazioni su tutti i certificati radice</span><span class="sxs-lookup"><span data-stu-id="a4c54-111">Example 1: Get information about all root certificates</span></span>
```
PS C:\>Get-AzureRmVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="a4c54-112">Questo comando consente di ottenere informazioni su tutti i certificati radice assegnati a un gateway di rete virtuale denominato ContosoVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="a4c54-112">This command gets information about all the root certificates assigned to a virtual network gateway named ContosoVirtualNetwork.</span></span>

### <span data-ttu-id="a4c54-113">Esempio 2: ottenere informazioni su certificati radice specifici</span><span class="sxs-lookup"><span data-stu-id="a4c54-113">Example 2: Get information about specific root certificates</span></span>
```
PS C:\>Get-AzureRmVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRootCertificateName "ContosoRootClientCertificate"
```

<span data-ttu-id="a4c54-114">Questo comando è una variante del comando mostrato nell'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="a4c54-114">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="a4c54-115">In questo caso, tuttavia, il parametro *VpnClientRootCertificateName* viene incluso per limitare i dati restituiti a un certificato radice specifico: ContosoRootClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="a4c54-115">In this case, however, the *VpnClientRootCertificateName* parameter is included in order to limit the returned data to a specific root certificate: ContosoRootClientCertificate.</span></span>

## <span data-ttu-id="a4c54-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a4c54-116">PARAMETERS</span></span>

### <span data-ttu-id="a4c54-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4c54-117">-ResourceGroupName</span></span>
<span data-ttu-id="a4c54-118">Specifica il nome del gruppo di risorse a cui è assegnato il gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="a4c54-118">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="a4c54-119">I gruppi di risorse categorizzano gli elementi per semplificare la gestione delle scorte e l'amministrazione generale di Azure.</span><span class="sxs-lookup"><span data-stu-id="a4c54-119">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="a4c54-120">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="a4c54-120">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="a4c54-121">Specifica il nome del gateway di rete virtuale in cui è assegnato il certificato radice.</span><span class="sxs-lookup"><span data-stu-id="a4c54-121">Specifies the name of the virtual network gateway where the root certificate is assigned.</span></span>

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

### <span data-ttu-id="a4c54-122">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="a4c54-122">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="a4c54-123">Specifica il nome del certificato radice client ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4c54-123">Specifies the name of the client root certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a4c54-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4c54-124">-DefaultProfile</span></span>
<span data-ttu-id="a4c54-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a4c54-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4c54-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4c54-126">CommonParameters</span></span>
<span data-ttu-id="a4c54-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4c54-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4c54-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4c54-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4c54-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a4c54-129">INPUTS</span></span>

## <span data-ttu-id="a4c54-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a4c54-130">OUTPUTS</span></span>

###  
<span data-ttu-id="a4c54-131">**Get-AzureRmVpnClientRootCertificate** ottiene le istanze dell'oggetto **Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate** .</span><span class="sxs-lookup"><span data-stu-id="a4c54-131">**Get-AzureRmVpnClientRootCertificate** gets instances of the **Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate** object.</span></span>

## <span data-ttu-id="a4c54-132">Note</span><span class="sxs-lookup"><span data-stu-id="a4c54-132">NOTES</span></span>

## <span data-ttu-id="a4c54-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a4c54-133">RELATED LINKS</span></span>

[<span data-ttu-id="a4c54-134">Add-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a4c54-134">Add-AzureRmVpnClientRootCertificate</span></span>](./Add-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="a4c54-135">New-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a4c54-135">New-AzureRmVpnClientRootCertificate</span></span>](./New-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="a4c54-136">Remove-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a4c54-136">Remove-AzureRmVpnClientRootCertificate</span></span>](./Remove-AzureRmVpnClientRootCertificate.md)


