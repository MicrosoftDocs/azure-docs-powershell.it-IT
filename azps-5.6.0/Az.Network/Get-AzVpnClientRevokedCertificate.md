---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 05626BF7-F886-4C76-8FC2-DDF783DEB539
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: c5ceef5ec70ac337180c8e2fcf6bb567c68391a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952206"
---
# <span data-ttu-id="12d03-101">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="12d03-101">Get-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="12d03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12d03-102">SYNOPSIS</span></span>
<span data-ttu-id="12d03-103">Recupera informazioni sui certificati di revoca client VPN.</span><span class="sxs-lookup"><span data-stu-id="12d03-103">Gets information about VPN client-revocation certificates.</span></span>

## <span data-ttu-id="12d03-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="12d03-104">SYNTAX</span></span>

```
Get-AzVpnClientRevokedCertificate [-VpnClientRevokedCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="12d03-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="12d03-105">DESCRIPTION</span></span>
<span data-ttu-id="12d03-106">Il cmdlet **Get-AzVpnClientRevokedCertificate** restituisce informazioni sui certificati di revoca client assegnati a un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="12d03-106">The **Get-AzVpnClientRevokedCertificate** cmdlet returns information about the client-revocation certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="12d03-107">I certificati di revoca client impediscono ai computer client di usare il certificato specificato per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="12d03-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="12d03-108">**Get-AzVpnClientRevokedCertificate** consente di restituire informazioni su tutti i certificati di revoca client nel gateway oppure, usando il parametro *VpnClientRevokedCertificateName,* per ottenere informazioni su un singolo certificato.</span><span class="sxs-lookup"><span data-stu-id="12d03-108">**Get-AzVpnClientRevokedCertificate** enables you to return information about all the client-revocation certificates on the gateway or, by using the *VpnClientRevokedCertificateName* parameter, to get information about a single certificate.</span></span>

## <span data-ttu-id="12d03-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="12d03-109">EXAMPLES</span></span>

### <span data-ttu-id="12d03-110">Esempio 1: Ottenere informazioni su tutti i certificati di revoca client</span><span class="sxs-lookup"><span data-stu-id="12d03-110">Example 1: Get information about all client-revocation certificates</span></span>
```
PS C:\>Get-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="12d03-111">Questo comando recupera informazioni su tutti i certificati di revoca client associati al gateway di rete virtuale denominato ContosoVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="12d03-111">This command gets information about all the client-revocation certificates associated with the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>

### <span data-ttu-id="12d03-112">Esempio 2: Ottenere informazioni su specifici certificati di revoca client</span><span class="sxs-lookup"><span data-stu-id="12d03-112">Example 2: Get information about specific client-revocation certificates</span></span>
```
PS C:\>Get-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"
```

<span data-ttu-id="12d03-113">Questo comando è una variante del comando mostrato nell'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="12d03-113">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="12d03-114">In questo caso, tuttavia, il parametro *VpnClientRevokedCertificateName* viene usato per limitare i dati restituiti a uno specifico certificato revocato dal client: il certificato con il nome ContosoRevokedClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="12d03-114">In this case, however, the *VpnClientRevokedCertificateName* parameter is used to limit the returned data to a specific client-revoked certificate: the certificate with the name ContosoRevokedClientCertificate.</span></span>

## <span data-ttu-id="12d03-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12d03-115">PARAMETERS</span></span>

### <span data-ttu-id="12d03-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12d03-116">-DefaultProfile</span></span>
<span data-ttu-id="12d03-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="12d03-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12d03-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12d03-118">-ResourceGroupName</span></span>
<span data-ttu-id="12d03-119">Specifica il nome del gruppo di risorse a cui è assegnato il gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="12d03-119">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="12d03-120">I gruppi di risorse categorizzano gli articoli per semplificare la gestione dell'inventario e l'amministrazione generale di Azure.</span><span class="sxs-lookup"><span data-stu-id="12d03-120">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="12d03-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="12d03-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="12d03-122">Specifica il nome del gateway di rete virtuale a cui vengono assegnate le informazioni sul certificato revocato.</span><span class="sxs-lookup"><span data-stu-id="12d03-122">Specifies the name of the virtual network gateway where the revoked certificate information is assigned.</span></span>

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

### <span data-ttu-id="12d03-123">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="12d03-123">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="12d03-124">Specifica il nome del certificato client VPN che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12d03-124">Specifies the name of the VPN client certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="12d03-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12d03-125">CommonParameters</span></span>
<span data-ttu-id="12d03-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12d03-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12d03-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="12d03-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12d03-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="12d03-128">INPUTS</span></span>

### <span data-ttu-id="12d03-129">System.String</span><span class="sxs-lookup"><span data-stu-id="12d03-129">System.String</span></span>

## <span data-ttu-id="12d03-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="12d03-130">OUTPUTS</span></span>

### <span data-ttu-id="12d03-131">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="12d03-131">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="12d03-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="12d03-132">NOTES</span></span>

## <span data-ttu-id="12d03-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="12d03-133">RELATED LINKS</span></span>

[<span data-ttu-id="12d03-134">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="12d03-134">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="12d03-135">New-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="12d03-135">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="12d03-136">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="12d03-136">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


