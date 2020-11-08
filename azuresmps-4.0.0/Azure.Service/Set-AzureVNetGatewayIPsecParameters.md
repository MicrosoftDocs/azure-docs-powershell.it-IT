---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: C85576C1-182B-467E-9620-A475728E20D2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3715b07c66d76c824e684976f18de4ecea64cdb1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029498"
---
# <span data-ttu-id="91998-101">Set-AzureVNetGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="91998-101">Set-AzureVNetGatewayIPsecParameters</span></span>

## <span data-ttu-id="91998-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="91998-102">SYNOPSIS</span></span>
<span data-ttu-id="91998-103">Imposta i parametri IPsec per la connessione tra un gateway di rete virtuale e un sito di rete locale.</span><span class="sxs-lookup"><span data-stu-id="91998-103">Sets IPsec parameters for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="91998-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="91998-104">SYNTAX</span></span>

```
Set-AzureVNetGatewayIPsecParameters -VNetName <String> -LocalNetworkSiteName <String>
 [-EncryptionType <String>] [-PfsGroup <String>] [-SADataSizeKilobytes <Int32>] [-SALifetimeSeconds <Int32>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="91998-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91998-105">DESCRIPTION</span></span>
<span data-ttu-id="91998-106">Il cmdlet **set-AzureVNetGatewayIPsecParameters** imposta i parametri Internet Protocol Security (IPSec) e Internet Key Exchange (IKE) per la connessione tra un gateway di rete virtuale e un sito di rete locale.</span><span class="sxs-lookup"><span data-stu-id="91998-106">The **Set-AzureVNetGatewayIPsecParameters** cmdlet sets Internet Protocol security (IPsec) and Internet Key Exchange (IKE) parameters for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="91998-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="91998-107">EXAMPLES</span></span>

## <span data-ttu-id="91998-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="91998-108">PARAMETERS</span></span>

### <span data-ttu-id="91998-109">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="91998-109">-EncryptionType</span></span>
<span data-ttu-id="91998-110">Specifica il tipo di crittografia per il gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="91998-110">Specifies the encryption type for the virtual network gateway.</span></span>
<span data-ttu-id="91998-111">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="91998-111">Valid values are:</span></span> 

- <span data-ttu-id="91998-112">NoEncryption</span><span class="sxs-lookup"><span data-stu-id="91998-112">NoEncryption</span></span> 
- <span data-ttu-id="91998-113">RequireEncryption</span><span class="sxs-lookup"><span data-stu-id="91998-113">RequireEncryption</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91998-114">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="91998-114">-LocalNetworkSiteName</span></span>
<span data-ttu-id="91998-115">Specifica il nome della connessione al sito di rete locale in cui questo cmdlet configura i parametri IPsec e IKE.</span><span class="sxs-lookup"><span data-stu-id="91998-115">Specifies the name of the local network site connection on which this cmdlet configures the IPsec and IKE parameters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91998-116">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="91998-116">-PfsGroup</span></span>
<span data-ttu-id="91998-117">Specifica il gruppo di segretezza avanzata (PFS) ideale.</span><span class="sxs-lookup"><span data-stu-id="91998-117">Specifies the perfect forward secrecy (PFS) group.</span></span>
<span data-ttu-id="91998-118">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="91998-118">Valid values are:</span></span> 

- <span data-ttu-id="91998-119">PFS1</span><span class="sxs-lookup"><span data-stu-id="91998-119">PFS1</span></span> 
- <span data-ttu-id="91998-120">Nessuno</span><span class="sxs-lookup"><span data-stu-id="91998-120">None</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91998-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="91998-121">-Profile</span></span>
<span data-ttu-id="91998-122">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91998-122">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="91998-123">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="91998-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91998-124">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="91998-124">-SADataSizeKilobytes</span></span>
<span data-ttu-id="91998-125">Specifica le dimensioni, in kilobyte, dell'associazione di sicurezza (SA).</span><span class="sxs-lookup"><span data-stu-id="91998-125">Specifies the size, in kilobytes, of the security association (SA).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91998-126">-SALifetimeSeconds</span><span class="sxs-lookup"><span data-stu-id="91998-126">-SALifetimeSeconds</span></span>
<span data-ttu-id="91998-127">Specifica il periodo, in secondi, dell'associazione di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="91998-127">Specifies the period, in seconds, of the security association.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91998-128">-VNetName</span><span class="sxs-lookup"><span data-stu-id="91998-128">-VNetName</span></span>
<span data-ttu-id="91998-129">Specifica la rete virtuale per cui questo cmdlet imposta i parametri IPsec per la connessione.</span><span class="sxs-lookup"><span data-stu-id="91998-129">Specifies the virtual network for which this cmdlet sets IPsec parameters for the connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91998-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91998-130">CommonParameters</span></span>
<span data-ttu-id="91998-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91998-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91998-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91998-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91998-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="91998-133">INPUTS</span></span>

## <span data-ttu-id="91998-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="91998-134">OUTPUTS</span></span>

## <span data-ttu-id="91998-135">Note</span><span class="sxs-lookup"><span data-stu-id="91998-135">NOTES</span></span>

## <span data-ttu-id="91998-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="91998-136">RELATED LINKS</span></span>

[<span data-ttu-id="91998-137">Get-AzureVNetGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="91998-137">Get-AzureVNetGatewayIPsecParameters</span></span>](./Get-AzureVNetGatewayIPsecParameters.md)


