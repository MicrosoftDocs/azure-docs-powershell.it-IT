---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 9E7A170D-512A-4117-85C3-3AA4D6341C6B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 97fe847fd183caa7de281b358da579e8df4d5831
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023698"
---
# <span data-ttu-id="0831e-101">Stop-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="0831e-101">Stop-AzureVirtualNetworkGatewayDiagnostics</span></span>

## <span data-ttu-id="0831e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0831e-102">SYNOPSIS</span></span>
<span data-ttu-id="0831e-103">Interrompe una sessione di diagnostica del gateway di rete virtuale in uso.</span><span class="sxs-lookup"><span data-stu-id="0831e-103">Stops a running virtual network gateway diagnostics session.</span></span>

## <span data-ttu-id="0831e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0831e-104">SYNTAX</span></span>

```
Stop-AzureVirtualNetworkGatewayDiagnostics -GatewayId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0831e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0831e-105">DESCRIPTION</span></span>
<span data-ttu-id="0831e-106">Il cmdlet **Stop-AzureVirtualNetworkGatewayDiagnostics** interrompe una sessione di diagnostica del gateway di rete virtuale in corso.</span><span class="sxs-lookup"><span data-stu-id="0831e-106">The **Stop-AzureVirtualNetworkGatewayDiagnostics** cmdlet stops a running virtual network gateway diagnostics session.</span></span>
<span data-ttu-id="0831e-107">Questo comando Salva i risultati della sessione di diagnostica nell'account di archiviazione specificato dal cmdlet Start-AzureVirtualNetworkGatewayDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="0831e-107">This command saves the results of the diagnostics session to the storage account that the Start-AzureVirtualNetworkGatewayDiagnostics cmdlet specifies.</span></span>

## <span data-ttu-id="0831e-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0831e-108">EXAMPLES</span></span>

## <span data-ttu-id="0831e-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0831e-109">PARAMETERS</span></span>

### <span data-ttu-id="0831e-110">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="0831e-110">-GatewayId</span></span>
<span data-ttu-id="0831e-111">Specifica l'ID di un gateway.</span><span class="sxs-lookup"><span data-stu-id="0831e-111">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="0831e-112">-Profile</span><span class="sxs-lookup"><span data-stu-id="0831e-112">-Profile</span></span>
<span data-ttu-id="0831e-113">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0831e-113">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="0831e-114">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="0831e-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0831e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0831e-115">CommonParameters</span></span>
<span data-ttu-id="0831e-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0831e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0831e-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0831e-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0831e-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0831e-118">INPUTS</span></span>

## <span data-ttu-id="0831e-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0831e-119">OUTPUTS</span></span>

## <span data-ttu-id="0831e-120">Note</span><span class="sxs-lookup"><span data-stu-id="0831e-120">NOTES</span></span>

## <span data-ttu-id="0831e-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0831e-121">RELATED LINKS</span></span>

[<span data-ttu-id="0831e-122">Get-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="0831e-122">Get-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Get-AzureVirtualNetworkGatewayDiagnostics.md)

[<span data-ttu-id="0831e-123">Start-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="0831e-123">Start-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Start-AzureVirtualNetworkGatewayDiagnostics.md)


