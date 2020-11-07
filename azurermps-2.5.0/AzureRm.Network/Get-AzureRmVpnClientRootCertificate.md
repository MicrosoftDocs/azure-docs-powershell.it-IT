---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 16754F70-9619-4F68-86E9-5C8B27812707
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientrootcertificate
schema: 2.0.0
ms.openlocfilehash: 7c3ee4e2c640417a7ba3d6cd78c2c8ea0691fff3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866271"
---
# <span data-ttu-id="67c28-101">Get-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="67c28-101">Get-AzureRmVpnClientRootCertificate</span></span>

## <span data-ttu-id="67c28-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="67c28-102">SYNOPSIS</span></span>
<span data-ttu-id="67c28-103">Ottiene informazioni sui certificati radice VPN.</span><span class="sxs-lookup"><span data-stu-id="67c28-103">Gets information about VPN root certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67c28-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="67c28-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientRootCertificate [-VpnClientRootCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="67c28-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="67c28-105">DESCRIPTION</span></span>
<span data-ttu-id="67c28-106">Il cmdlet **Get-AzureRmVpnClientRootCertificate** restituisce informazioni sui certificati radice assegnati a un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="67c28-106">The **Get-AzureRmVpnClientRootCertificate** cmdlet returns information about the root certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="67c28-107">I certificati radice sono certificati X. 509 che identificano l'autorità di certificazione radice: tutti gli altri certificati usati nel gateway considerano attendibile il certificato radice.</span><span class="sxs-lookup"><span data-stu-id="67c28-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>

<span data-ttu-id="67c28-108">Per impostazione predefinita, **Get-AzureRmVpnClientRootCertificate** restituisce informazioni su tutti i certificati radice assegnati a un gateway.</span><span class="sxs-lookup"><span data-stu-id="67c28-108">By default, **Get-AzureRmVpnClientRootCertificate** returns information about all the root certificates assigned to a gateway.</span></span>
<span data-ttu-id="67c28-109">I gateway possono avere più di un certificato radice. Tuttavia, includendo il parametro **VpnClientRootCertificateName** , puoi limitare i dati restituiti a un certificato specifico.</span><span class="sxs-lookup"><span data-stu-id="67c28-109">(Gateways can have more than one root certificate.) However, by including the **VpnClientRootCertificateName** parameter you can limit the returned data to a specific certificate.</span></span>

## <span data-ttu-id="67c28-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="67c28-110">EXAMPLES</span></span>

### <span data-ttu-id="67c28-111">Esempio 1: ottenere informazioni su tutti i certificati radice</span><span class="sxs-lookup"><span data-stu-id="67c28-111">Example 1: Get information about all root certificates</span></span>
```
PS C:\>Get-AzureRmVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="67c28-112">Questo comando consente di ottenere informazioni su tutti i certificati radice assegnati a un gateway di rete virtuale denominato ContosoVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="67c28-112">This command gets information about all the root certificates assigned to a virtual network gateway named ContosoVirtualNetwork.</span></span>

### <span data-ttu-id="67c28-113">Esempio 2: ottenere informazioni su certificati radice specifici</span><span class="sxs-lookup"><span data-stu-id="67c28-113">Example 2: Get information about specific root certificates</span></span>
```
PS C:\>Get-AzureRmVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRootCertificateName "ContosoRootClientCertificate"
```

<span data-ttu-id="67c28-114">Questo comando è una variante del comando mostrato nell'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="67c28-114">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="67c28-115">In questo caso, tuttavia, il parametro *VpnClientRootCertificateName* viene incluso per limitare i dati restituiti a un certificato radice specifico: ContosoRootClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="67c28-115">In this case, however, the *VpnClientRootCertificateName* parameter is included in order to limit the returned data to a specific root certificate: ContosoRootClientCertificate.</span></span>

## <span data-ttu-id="67c28-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="67c28-116">PARAMETERS</span></span>

### <span data-ttu-id="67c28-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67c28-117">-DefaultProfile</span></span>
<span data-ttu-id="67c28-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="67c28-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67c28-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67c28-119">-ResourceGroupName</span></span>
<span data-ttu-id="67c28-120">Specifica il nome del gruppo di risorse a cui è assegnato il gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="67c28-120">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="67c28-121">I gruppi di risorse categorizzano gli elementi per semplificare la gestione delle scorte e l'amministrazione generale di Azure.</span><span class="sxs-lookup"><span data-stu-id="67c28-121">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="67c28-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="67c28-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="67c28-123">Specifica il nome del gateway di rete virtuale in cui è assegnato il certificato radice.</span><span class="sxs-lookup"><span data-stu-id="67c28-123">Specifies the name of the virtual network gateway where the root certificate is assigned.</span></span>

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

### <span data-ttu-id="67c28-124">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="67c28-124">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="67c28-125">Specifica il nome del certificato radice client ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67c28-125">Specifies the name of the client root certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="67c28-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67c28-126">CommonParameters</span></span>
<span data-ttu-id="67c28-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67c28-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67c28-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67c28-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67c28-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="67c28-129">INPUTS</span></span>

## <span data-ttu-id="67c28-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="67c28-130">OUTPUTS</span></span>

###  
<span data-ttu-id="67c28-131">**Get-AzureRmVpnClientRootCertificate** ottiene le istanze dell'oggetto **Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate** .</span><span class="sxs-lookup"><span data-stu-id="67c28-131">**Get-AzureRmVpnClientRootCertificate** gets instances of the **Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate** object.</span></span>

## <span data-ttu-id="67c28-132">Note</span><span class="sxs-lookup"><span data-stu-id="67c28-132">NOTES</span></span>

## <span data-ttu-id="67c28-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="67c28-133">RELATED LINKS</span></span>

[<span data-ttu-id="67c28-134">Add-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="67c28-134">Add-AzureRmVpnClientRootCertificate</span></span>](./Add-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="67c28-135">New-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="67c28-135">New-AzureRmVpnClientRootCertificate</span></span>](./New-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="67c28-136">Remove-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="67c28-136">Remove-AzureRmVpnClientRootCertificate</span></span>](./Remove-AzureRmVpnClientRootCertificate.md)


