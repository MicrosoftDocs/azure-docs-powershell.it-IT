---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: DA5689DF-AA4A-4161-89B0-8055BF384274
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7b71367ac18a753fad5425d0073b55cacb413e4b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023730"
---
# <span data-ttu-id="0b7ae-101">Start-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="0b7ae-101">Start-AzureVirtualNetworkGatewayDiagnostics</span></span>

## <span data-ttu-id="0b7ae-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0b7ae-102">SYNOPSIS</span></span>
<span data-ttu-id="0b7ae-103">Avvia la diagnostica per un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="0b7ae-103">Starts diagnostics for a virtual network gateway.</span></span>

## <span data-ttu-id="0b7ae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0b7ae-104">SYNTAX</span></span>

```
Start-AzureVirtualNetworkGatewayDiagnostics -GatewayId <String> [-CaptureDurationInSeconds <Int32>]
 [-ContainerName <String>] [-StorageContext <AzureStorageContext>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="0b7ae-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b7ae-105">DESCRIPTION</span></span>
<span data-ttu-id="0b7ae-106">Il cmdlet **Start-AzureVirtualNetworkGatewayDiagnostics** avvia una nuova sessione di diagnostica del gateway per un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="0b7ae-106">The **Start-AzureVirtualNetworkGatewayDiagnostics** cmdlet starts a new gateway diagnostics session for a virtual network gateway.</span></span>
<span data-ttu-id="0b7ae-107">Può essere eseguita una sola sessione di diagnostica del gateway alla volta.</span><span class="sxs-lookup"><span data-stu-id="0b7ae-107">Only one gateway diagnostics session can run at a time.</span></span>
<span data-ttu-id="0b7ae-108">Se si esegue questo cmdlet durante l'esecuzione di una sessione di diagnostica del gateway, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="0b7ae-108">If you run this cmdlet while a gateway diagnostics session is running, this cmdlet returns an error.</span></span>

## <span data-ttu-id="0b7ae-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0b7ae-109">EXAMPLES</span></span>

## <span data-ttu-id="0b7ae-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0b7ae-110">PARAMETERS</span></span>

### <span data-ttu-id="0b7ae-111">-CaptureDurationInSeconds</span><span class="sxs-lookup"><span data-stu-id="0b7ae-111">-CaptureDurationInSeconds</span></span>
<span data-ttu-id="0b7ae-112">Specifica la durata dell'acquisizione in secondi.</span><span class="sxs-lookup"><span data-stu-id="0b7ae-112">Specifies the capture duration in seconds.</span></span>

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

### <span data-ttu-id="0b7ae-113">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="0b7ae-113">-ContainerName</span></span>
<span data-ttu-id="0b7ae-114">Specifica il nome di un contenitore di Azure.</span><span class="sxs-lookup"><span data-stu-id="0b7ae-114">Specifies the name of an Azure container.</span></span>
<span data-ttu-id="0b7ae-115">Questo cmdlet archivia i risultati nel contenitore specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="0b7ae-115">This cmdlet stores results in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="0b7ae-116">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="0b7ae-116">-GatewayId</span></span>
<span data-ttu-id="0b7ae-117">Specifica l'ID di un gateway.</span><span class="sxs-lookup"><span data-stu-id="0b7ae-117">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="0b7ae-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="0b7ae-118">-Profile</span></span>
<span data-ttu-id="0b7ae-119">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b7ae-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="0b7ae-120">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="0b7ae-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0b7ae-121">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="0b7ae-121">-StorageContext</span></span>
<span data-ttu-id="0b7ae-122">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="0b7ae-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="0b7ae-123">Questo cmdlet archivia i risultati usando il contesto di archiviazione specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="0b7ae-123">This cmdlet stores results by using the storage context that this parameter specifies.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b7ae-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b7ae-124">CommonParameters</span></span>
<span data-ttu-id="0b7ae-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b7ae-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b7ae-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b7ae-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b7ae-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0b7ae-127">INPUTS</span></span>

## <span data-ttu-id="0b7ae-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0b7ae-128">OUTPUTS</span></span>

## <span data-ttu-id="0b7ae-129">Note</span><span class="sxs-lookup"><span data-stu-id="0b7ae-129">NOTES</span></span>

## <span data-ttu-id="0b7ae-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0b7ae-130">RELATED LINKS</span></span>

[<span data-ttu-id="0b7ae-131">Get-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="0b7ae-131">Get-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Get-AzureVirtualNetworkGatewayDiagnostics.md)

[<span data-ttu-id="0b7ae-132">Stop-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="0b7ae-132">Stop-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Stop-AzureVirtualNetworkGatewayDiagnostics.md)


