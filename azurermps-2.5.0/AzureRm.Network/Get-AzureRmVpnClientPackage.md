---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2B4A3E2A-1868-492F-9F77-932319D2CE6D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientpackage
schema: 2.0.0
ms.openlocfilehash: 193353a3e578ec0f644be605498214d5bf4944c6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866272"
---
# <span data-ttu-id="39575-101">Get-AzureRmVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="39575-101">Get-AzureRmVpnClientPackage</span></span>

## <span data-ttu-id="39575-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="39575-102">SYNOPSIS</span></span>
<span data-ttu-id="39575-103">Ottiene informazioni su un pacchetto client VPN.</span><span class="sxs-lookup"><span data-stu-id="39575-103">Gets information about a VPN client package.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39575-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="39575-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientPackage -ResourceGroupName <String> -VirtualNetworkGatewayName <String>
 -ProcessorArchitecture <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39575-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="39575-105">DESCRIPTION</span></span>
<span data-ttu-id="39575-106">Il cmdlet **Get-AzureRmVpnClientPackage** ottiene le informazioni sui pacchetti del client VPN disponibili in un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="39575-106">The **Get-AzureRmVpnClientPackage** cmdlet gets information about the VPN client packages available from a virtual network gateway.</span></span>
<span data-ttu-id="39575-107">I pacchetti client contengono dati di configurazione che consentono a un computer client di creare una connessione VPN a una rete virtuale di Azure; i computer client devono avere installato il pacchetto di configurazione corretto per creare una connessione VPN.</span><span class="sxs-lookup"><span data-stu-id="39575-107">Client packages contain configuration data that enable a client computer to make a VPN connection to an Azure virtual network; client computers must have the correct configuration package installed in order to make a VPN connection.</span></span>
<span data-ttu-id="39575-108">Sono disponibili pacchetti di configurazione diversi basati sulla versione di Windows del computer client, ad esempio Windows 7 o Windows 10, e sull'architettura del processore del computer client (AMD64 o x86).</span><span class="sxs-lookup"><span data-stu-id="39575-108">Different configuration packages are available based on the client computer's version of Windows (for example, Windows 7 or Windows 10) and on the client computer's processor architecture (AMD64 or x86).</span></span>
<span data-ttu-id="39575-109">Devi specificare il tipo di architettura durante l'uso **di Get-AzureRmVpnClientPackage**.</span><span class="sxs-lookup"><span data-stu-id="39575-109">You must specify the architecture type when running **Get-AzureRmVpnClientPackage**.</span></span>

## <span data-ttu-id="39575-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="39575-110">EXAMPLES</span></span>

### <span data-ttu-id="39575-111">Esempio 1: ottenere informazioni su un pacchetto client VPN per l'architettura del processore</span><span class="sxs-lookup"><span data-stu-id="39575-111">Example 1: Get information about a processor architecture VPN client package</span></span>
```
PS C:\>Get-AzureRmVpnClientPackage -ProcessorArchitecture -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -ProcessorArchitecture "Amd64"
```

<span data-ttu-id="39575-112">Questo comando consente di ottenere informazioni sui pacchetti del client VPN AMD64 archiviati nel gateway di rete virtuale denominato ContosoVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="39575-112">This command gets information about the AMD64 VPN client packages stored on the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>
<span data-ttu-id="39575-113">Per ottenere informazioni sui pacchetti client x86, imposta il valore del parametro *processorArchitecture* su x86.</span><span class="sxs-lookup"><span data-stu-id="39575-113">To get information about the x86 client packages, set the value of the *ProcessorArchitecture* parameter to x86.</span></span>

## <span data-ttu-id="39575-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="39575-114">PARAMETERS</span></span>

### <span data-ttu-id="39575-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39575-115">-DefaultProfile</span></span>
<span data-ttu-id="39575-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="39575-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39575-117">-ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="39575-117">-ProcessorArchitecture</span></span>
<span data-ttu-id="39575-118">Specifica il tipo di architettura della CPU per cui è progettato il pacchetto client.</span><span class="sxs-lookup"><span data-stu-id="39575-118">Specifies the type of CPU architecture that the client package is designed for.</span></span>
<span data-ttu-id="39575-119">I valori validi sono amd64 e x86.</span><span class="sxs-lookup"><span data-stu-id="39575-119">Valid values are Amd64 and X86.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Amd64, X86

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39575-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39575-120">-ResourceGroupName</span></span>
<span data-ttu-id="39575-121">Specifica il nome del gruppo di risorse a cui è assegnato il gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="39575-121">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="39575-122">I gruppi di risorse categorizzano gli elementi per semplificare la gestione delle scorte e l'amministrazione generale di Azure.</span><span class="sxs-lookup"><span data-stu-id="39575-122">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39575-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="39575-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="39575-124">Specifica il nome del gateway di rete virtuale in cui sono archiviate le informazioni sul pacchetto client.</span><span class="sxs-lookup"><span data-stu-id="39575-124">Specifies the name of the virtual network gateway where the client package information is stored.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39575-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39575-125">CommonParameters</span></span>
<span data-ttu-id="39575-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39575-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39575-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39575-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39575-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="39575-128">INPUTS</span></span>

### <span data-ttu-id="39575-129">Stringa</span><span class="sxs-lookup"><span data-stu-id="39575-129">String</span></span>
<span data-ttu-id="39575-130">Il parametro ' ResourceGroupName ' accetta il valore di tipo ' String ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="39575-130">Parameter 'ResourceGroupName' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="39575-131">Stringa</span><span class="sxs-lookup"><span data-stu-id="39575-131">String</span></span>
<span data-ttu-id="39575-132">Il parametro ' VirtualNetworkGatewayName ' accetta il valore di tipo ' String ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="39575-132">Parameter 'VirtualNetworkGatewayName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="39575-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="39575-133">OUTPUTS</span></span>

###  
<span data-ttu-id="39575-134">**Get-AzureRmVpnClientPackage** restituisce le istanze dell'oggetto System. String.</span><span class="sxs-lookup"><span data-stu-id="39575-134">**Get-AzureRmVpnClientPackage** returns instances of the System.String object.</span></span>

## <span data-ttu-id="39575-135">Note</span><span class="sxs-lookup"><span data-stu-id="39575-135">NOTES</span></span>

## <span data-ttu-id="39575-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="39575-136">RELATED LINKS</span></span>

[<span data-ttu-id="39575-137">Ridimensionare-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="39575-137">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="39575-138">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="39575-138">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md)


