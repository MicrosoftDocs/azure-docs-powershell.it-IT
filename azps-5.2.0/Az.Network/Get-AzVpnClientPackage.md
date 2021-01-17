---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B4A3E2A-1868-492F-9F77-932319D2CE6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientPackage.md
ms.openlocfilehash: 8eba8d26bcac5de16be3e2cda5e8ca80356aea11
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372539"
---
# <span data-ttu-id="890b8-101">Get-AzVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="890b8-101">Get-AzVpnClientPackage</span></span>

## <span data-ttu-id="890b8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="890b8-102">SYNOPSIS</span></span>
<span data-ttu-id="890b8-103">Ottiene informazioni su un pacchetto client VPN.</span><span class="sxs-lookup"><span data-stu-id="890b8-103">Gets information about a VPN client package.</span></span>

## <span data-ttu-id="890b8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="890b8-104">SYNTAX</span></span>

```
Get-AzVpnClientPackage -ResourceGroupName <String> -VirtualNetworkGatewayName <String>
 -ProcessorArchitecture <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="890b8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="890b8-105">DESCRIPTION</span></span>
<span data-ttu-id="890b8-106">Il cmdlet **Get-AzVpnClientPackage** ottiene le informazioni sui pacchetti del client VPN disponibili in un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="890b8-106">The **Get-AzVpnClientPackage** cmdlet gets information about the VPN client packages available from a virtual network gateway.</span></span>
<span data-ttu-id="890b8-107">I pacchetti client contengono dati di configurazione che consentono a un computer client di creare una connessione VPN a una rete virtuale di Azure; i computer client devono avere installato il pacchetto di configurazione corretto per creare una connessione VPN.</span><span class="sxs-lookup"><span data-stu-id="890b8-107">Client packages contain configuration data that enable a client computer to make a VPN connection to an Azure virtual network; client computers must have the correct configuration package installed in order to make a VPN connection.</span></span>
<span data-ttu-id="890b8-108">Sono disponibili pacchetti di configurazione diversi basati sulla versione di Windows del computer client, ad esempio Windows 7 o Windows 10, e sull'architettura del processore del computer client (AMD64 o x86).</span><span class="sxs-lookup"><span data-stu-id="890b8-108">Different configuration packages are available based on the client computer's version of Windows (for example, Windows 7 or Windows 10) and on the client computer's processor architecture (AMD64 or x86).</span></span>
<span data-ttu-id="890b8-109">Devi specificare il tipo di architettura durante l'uso **di Get-AzVpnClientPackage**.</span><span class="sxs-lookup"><span data-stu-id="890b8-109">You must specify the architecture type when running **Get-AzVpnClientPackage**.</span></span>

## <span data-ttu-id="890b8-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="890b8-110">EXAMPLES</span></span>

### <span data-ttu-id="890b8-111">Esempio 1: ottenere informazioni su un pacchetto client VPN per l'architettura del processore</span><span class="sxs-lookup"><span data-stu-id="890b8-111">Example 1: Get information about a processor architecture VPN client package</span></span>
```
PS C:\>Get-AzVpnClientPackage -ProcessorArchitecture -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -ProcessorArchitecture "Amd64"
```

<span data-ttu-id="890b8-112">Questo comando consente di ottenere informazioni sui pacchetti del client VPN AMD64 archiviati nel gateway di rete virtuale denominato ContosoVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="890b8-112">This command gets information about the AMD64 VPN client packages stored on the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>
<span data-ttu-id="890b8-113">Per ottenere informazioni sui pacchetti client x86, imposta il valore del parametro *processorArchitecture* su x86.</span><span class="sxs-lookup"><span data-stu-id="890b8-113">To get information about the x86 client packages, set the value of the *ProcessorArchitecture* parameter to x86.</span></span>

## <span data-ttu-id="890b8-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="890b8-114">PARAMETERS</span></span>

### <span data-ttu-id="890b8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="890b8-115">-DefaultProfile</span></span>
<span data-ttu-id="890b8-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="890b8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="890b8-117">-ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="890b8-117">-ProcessorArchitecture</span></span>
<span data-ttu-id="890b8-118">Specifica il tipo di architettura della CPU per cui è progettato il pacchetto client.</span><span class="sxs-lookup"><span data-stu-id="890b8-118">Specifies the type of CPU architecture that the client package is designed for.</span></span>
<span data-ttu-id="890b8-119">I valori validi sono amd64 e x86.</span><span class="sxs-lookup"><span data-stu-id="890b8-119">Valid values are Amd64 and X86.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Amd64, X86

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="890b8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="890b8-120">-ResourceGroupName</span></span>
<span data-ttu-id="890b8-121">Specifica il nome del gruppo di risorse a cui è assegnato il gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="890b8-121">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="890b8-122">I gruppi di risorse categorizzano gli elementi per semplificare la gestione delle scorte e l'amministrazione generale di Azure.</span><span class="sxs-lookup"><span data-stu-id="890b8-122">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="890b8-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="890b8-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="890b8-124">Specifica il nome del gateway di rete virtuale in cui sono archiviate le informazioni sul pacchetto client.</span><span class="sxs-lookup"><span data-stu-id="890b8-124">Specifies the name of the virtual network gateway where the client package information is stored.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="890b8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="890b8-125">CommonParameters</span></span>
<span data-ttu-id="890b8-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="890b8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="890b8-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="890b8-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="890b8-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="890b8-128">INPUTS</span></span>

### <span data-ttu-id="890b8-129">System. String</span><span class="sxs-lookup"><span data-stu-id="890b8-129">System.String</span></span>

## <span data-ttu-id="890b8-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="890b8-130">OUTPUTS</span></span>

### <span data-ttu-id="890b8-131">System. String</span><span class="sxs-lookup"><span data-stu-id="890b8-131">System.String</span></span>

## <span data-ttu-id="890b8-132">Note</span><span class="sxs-lookup"><span data-stu-id="890b8-132">NOTES</span></span>

## <span data-ttu-id="890b8-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="890b8-133">RELATED LINKS</span></span>

[<span data-ttu-id="890b8-134">Ridimensionare-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="890b8-134">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="890b8-135">Set-AzVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="890b8-135">Set-AzVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)


