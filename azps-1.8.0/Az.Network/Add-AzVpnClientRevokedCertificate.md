---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 90FB7B88-844E-4783-A10F-04D7BA47C030
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 041fc967bc5834ba21f96e75e2f5cdc3687d234c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678641"
---
# <span data-ttu-id="3ba68-101">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="3ba68-101">Add-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="3ba68-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3ba68-102">SYNOPSIS</span></span>
<span data-ttu-id="3ba68-103">Aggiunge un certificato di revoca client VPN.</span><span class="sxs-lookup"><span data-stu-id="3ba68-103">Adds a VPN client-revocation certificate.</span></span>

## <span data-ttu-id="3ba68-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3ba68-104">SYNTAX</span></span>

```
Add-AzVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3ba68-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ba68-105">DESCRIPTION</span></span>
<span data-ttu-id="3ba68-106">Il cmdlet **Add-AzVpnClientRevokedCertificate** assegna un certificato di revoca client a un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="3ba68-106">The **Add-AzVpnClientRevokedCertificate** cmdlet assigns a client-revocation certificate to a virtual network gateway.</span></span>
<span data-ttu-id="3ba68-107">I certificati di revoca client impediscono ai computer client di usare il certificato specificato per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="3ba68-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="3ba68-108">Per usare questo cmdlet, è necessario specificare sia il nome del certificato che l'identificazione personale del certificato.</span><span class="sxs-lookup"><span data-stu-id="3ba68-108">You need to specify both the certificate name and the certificate thumbprint to use this cmdlet.</span></span>

## <span data-ttu-id="3ba68-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3ba68-109">EXAMPLES</span></span>

### <span data-ttu-id="3ba68-110">Esempio 1: aggiungere un nuovo certificato di revoca client a un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="3ba68-110">Example 1: Add a new client-revocation certificate to a virtual network gateway</span></span>
```
PS C:\>Add-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="3ba68-111">Questo comando aggiunge un nuovo certificato di revoca client al gateway di rete virtuale denominato ContosoVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="3ba68-111">This command adds a new client-revocation certificate to the virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="3ba68-112">Per aggiungere il certificato, è necessario specificare sia il nome del certificato che l'identificazione personale del certificato.</span><span class="sxs-lookup"><span data-stu-id="3ba68-112">In order to add the certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="3ba68-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3ba68-113">PARAMETERS</span></span>

### <span data-ttu-id="3ba68-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ba68-114">-DefaultProfile</span></span>
<span data-ttu-id="3ba68-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3ba68-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ba68-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ba68-116">-ResourceGroupName</span></span>
<span data-ttu-id="3ba68-117">Specifica il nome del gruppo di risorse a cui è assegnato il gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="3ba68-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="3ba68-118">I gruppi di risorse categorizzano gli elementi per semplificare la gestione delle scorte e l'amministrazione generale di Azure.</span><span class="sxs-lookup"><span data-stu-id="3ba68-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="3ba68-119">-Identificazione personale</span><span class="sxs-lookup"><span data-stu-id="3ba68-119">-Thumbprint</span></span>
<span data-ttu-id="3ba68-120">Specifica l'identificatore univoco del certificato aggiunto.</span><span class="sxs-lookup"><span data-stu-id="3ba68-120">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="3ba68-121">Ad esempio:-identificazione personale "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" per ottenere informazioni personali per i certificati, è possibile usare un comando di Windows PowerShell simile al seguente: `Get-ChildItem -Path Cert:\LocalMachine\Root` .</span><span class="sxs-lookup"><span data-stu-id="3ba68-121">For example: -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" You can get thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`.</span></span>
<span data-ttu-id="3ba68-122">Il comando precedente consente di ottenere informazioni per tutti i certificati del computer locale presenti nell'archivio certificati radice.</span><span class="sxs-lookup"><span data-stu-id="3ba68-122">The preceding command gets information for all the local computer certificates found in the root certificate store.</span></span>

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

### <span data-ttu-id="3ba68-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="3ba68-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="3ba68-124">Specifica il nome del gateway di rete virtuale in cui deve essere aggiunto il certificato.</span><span class="sxs-lookup"><span data-stu-id="3ba68-124">Specifies the name of the virtual network gateway where the certificate should be added.</span></span>

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

### <span data-ttu-id="3ba68-125">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="3ba68-125">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="3ba68-126">Specifica il nome del certificato client VPN da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="3ba68-126">Specifies the name of the VPN client certificate to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ba68-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ba68-127">CommonParameters</span></span>
<span data-ttu-id="3ba68-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ba68-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ba68-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ba68-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ba68-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3ba68-130">INPUTS</span></span>

### <span data-ttu-id="3ba68-131">System. String</span><span class="sxs-lookup"><span data-stu-id="3ba68-131">System.String</span></span>

## <span data-ttu-id="3ba68-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3ba68-132">OUTPUTS</span></span>

### <span data-ttu-id="3ba68-133">Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="3ba68-133">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="3ba68-134">Note</span><span class="sxs-lookup"><span data-stu-id="3ba68-134">NOTES</span></span>

## <span data-ttu-id="3ba68-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3ba68-135">RELATED LINKS</span></span>

[<span data-ttu-id="3ba68-136">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="3ba68-136">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="3ba68-137">New-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="3ba68-137">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="3ba68-138">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="3ba68-138">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


