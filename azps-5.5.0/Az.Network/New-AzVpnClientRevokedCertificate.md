---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 973E1E53-983F-45A7-A7CF-18A8D96EC4E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: ba9715b6f29cd45ba25f8b2d2ab85ba0d7ef7979
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193542"
---
# <span data-ttu-id="33338-101">New-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="33338-101">New-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="33338-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33338-102">SYNOPSIS</span></span>
<span data-ttu-id="33338-103">Crea un nuovo certificato di revoca client VPN.</span><span class="sxs-lookup"><span data-stu-id="33338-103">Creates a new VPN client-revocation certificate.</span></span>

## <span data-ttu-id="33338-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="33338-104">SYNTAX</span></span>

```
New-AzVpnClientRevokedCertificate -Name <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33338-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="33338-105">DESCRIPTION</span></span>
<span data-ttu-id="33338-106">Il cmdlet **New-AzVpnClientRevokedCertificate** crea un nuovo certificato di revoca client di rete privata virtuale (VPN) da usare in un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="33338-106">The **New-AzVpnClientRevokedCertificate** cmdlet creates a new virtual private network (VPN) client-revocation certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="33338-107">I certificati di revoca client impediscono ai computer client di usare il certificato specificato per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="33338-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="33338-108">Questo cmdlet crea un certificato autonomo non assegnato a un gateway virtuale.</span><span class="sxs-lookup"><span data-stu-id="33338-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="33338-109">Il certificato creato da **New-AzVpnClientRevokedCertificate** viene invece usato insieme al cmdlet New-AzVirtualNetworkGateway quando crea un nuovo gateway.</span><span class="sxs-lookup"><span data-stu-id="33338-109">Instead, the certificate created by **New-AzVpnClientRevokedCertificate** is used in conjunction with the New-AzVirtualNetworkGateway cmdlet when it creates a new gateway.</span></span>
<span data-ttu-id="33338-110">Si supponga, ad esempio, di creare un nuovo certificato e di archiviarlo in una variabile denominata $Certificate.</span><span class="sxs-lookup"><span data-stu-id="33338-110">For instance, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="33338-111">È quindi possibile usare tale oggetto certificato quando si crea un nuovo gateway virtuale.</span><span class="sxs-lookup"><span data-stu-id="33338-111">You can then use that certificate object when you create a new virtual gateway.</span></span>
<span data-ttu-id="33338-112">Ad esempio, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`</span><span class="sxs-lookup"><span data-stu-id="33338-112">For instance, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`</span></span>
<span data-ttu-id="33338-113">Per altre informazioni, vedere la documentazione del cmdlet New-AzVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="33338-113">For more information, see the documentation for the New-AzVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="33338-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="33338-114">EXAMPLES</span></span>

### <span data-ttu-id="33338-115">Esempio 1: Creare un nuovo certificato revocato dal client</span><span class="sxs-lookup"><span data-stu-id="33338-115">Example 1: Create a new client-revoked certificate</span></span>
```
PS C:\>$Certificate = New-AzVpnClientRevokedCertificate -Name "ContosoClientRevokedCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="33338-116">Questo comando crea un nuovo certificato revocato dal client e archivia l'oggetto certificato in una variabile denominata $Certificate.</span><span class="sxs-lookup"><span data-stu-id="33338-116">This command creates a new client-revoked certificate and stores the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="33338-117">Questa variabile può quindi essere usata dal cmdlet **New-AzVirtualNetworkGateway** per aggiungere il certificato a un nuovo gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="33338-117">This variable can then be used by the **New-AzVirtualNetworkGateway** cmdlet to add the certificate to a new virtual network gateway.</span></span>

## <span data-ttu-id="33338-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33338-118">PARAMETERS</span></span>

### <span data-ttu-id="33338-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33338-119">-DefaultProfile</span></span>
<span data-ttu-id="33338-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="33338-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33338-121">-Name</span><span class="sxs-lookup"><span data-stu-id="33338-121">-Name</span></span>
<span data-ttu-id="33338-122">Specifica un nome univoco per il nuovo certificato di revoca client.</span><span class="sxs-lookup"><span data-stu-id="33338-122">Specifies a unique name for the new client-revocation certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33338-123">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="33338-123">-Thumbprint</span></span>
<span data-ttu-id="33338-124">Specifica l'identificatore univoco del certificato da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="33338-124">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="33338-125">È possibile restituire informazioni sull'impronta digitale per i certificati usando un comando di Windows PowerShell simile al seguente: `Get-ChildItem -Path Cert:\LocalMachine\Root`</span><span class="sxs-lookup"><span data-stu-id="33338-125">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`</span></span>
<span data-ttu-id="33338-126">Il comando precedente restituisce le informazioni per tutti i certificati del computer locale trovati nell'archivio certificati radice.</span><span class="sxs-lookup"><span data-stu-id="33338-126">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33338-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33338-127">CommonParameters</span></span>
<span data-ttu-id="33338-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33338-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33338-129">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33338-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33338-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="33338-130">INPUTS</span></span>

### <span data-ttu-id="33338-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="33338-131">None</span></span>

## <span data-ttu-id="33338-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="33338-132">OUTPUTS</span></span>

### <span data-ttu-id="33338-133">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="33338-133">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="33338-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="33338-134">NOTES</span></span>

## <span data-ttu-id="33338-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="33338-135">RELATED LINKS</span></span>

[<span data-ttu-id="33338-136">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="33338-136">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="33338-137">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="33338-137">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="33338-138">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="33338-138">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


