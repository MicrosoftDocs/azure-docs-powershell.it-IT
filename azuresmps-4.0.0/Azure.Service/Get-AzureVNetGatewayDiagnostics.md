---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 22E8CB18-8CDD-4992-AB81-E1BB400E6BC7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 294e931529b7de939a6a5c20181d48b18da1e892
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029739"
---
# <span data-ttu-id="d3cc0-101">Get-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="d3cc0-101">Get-AzureVNetGatewayDiagnostics</span></span>

## <span data-ttu-id="d3cc0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d3cc0-102">SYNOPSIS</span></span>
<span data-ttu-id="d3cc0-103">Ottiene lo stato corrente della diagnostica per un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="d3cc0-103">Gets the current state of diagnostics for a virtual network gateway.</span></span>

## <span data-ttu-id="d3cc0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d3cc0-104">SYNTAX</span></span>

```
Get-AzureVNetGatewayDiagnostics -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d3cc0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3cc0-105">DESCRIPTION</span></span>
<span data-ttu-id="d3cc0-106">Il cmdlet **Get-AzureVNetGatewayDiagnostics** ottiene lo stato corrente della diagnostica per un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="d3cc0-106">The **Get-AzureVNetGatewayDiagnostics** cmdlet gets the current state of diagnostics for a virtual network gateway.</span></span>
<span data-ttu-id="d3cc0-107">Se esiste un oggetto binario di grandi dimensioni (BLOB) in cui l' **inizio-AzureVNetGatewayDiagnostics** ha salvato una sessione di diagnostica precedente, questo cmdlet restituisce anche l'URL del BLOB in cui tale cmdlet ha salvato la sessione di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="d3cc0-107">If a binary large object (blob) exists where the **Start-AzureVNetGatewayDiagnostics** saved a previous diagnostics session, this cmdlet also returns the URL of the blob where that cmdlet saved that diagnostics session.</span></span>

## <span data-ttu-id="d3cc0-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d3cc0-108">EXAMPLES</span></span>

## <span data-ttu-id="d3cc0-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d3cc0-109">PARAMETERS</span></span>

### <span data-ttu-id="d3cc0-110">-Profile</span><span class="sxs-lookup"><span data-stu-id="d3cc0-110">-Profile</span></span>
<span data-ttu-id="d3cc0-111">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3cc0-111">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="d3cc0-112">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="d3cc0-112">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d3cc0-113">-VNetName</span><span class="sxs-lookup"><span data-stu-id="d3cc0-113">-VNetName</span></span>
<span data-ttu-id="d3cc0-114">Specifica la rete virtuale che contiene un gateway di rete virtuale per cui questo cmdlet ottiene la diagnostica.</span><span class="sxs-lookup"><span data-stu-id="d3cc0-114">Specifies the virtual network that contains a virtual network gateway for which this cmdlet gets diagnostics.</span></span>

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

### <span data-ttu-id="d3cc0-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3cc0-115">CommonParameters</span></span>
<span data-ttu-id="d3cc0-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3cc0-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3cc0-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3cc0-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3cc0-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d3cc0-118">INPUTS</span></span>

## <span data-ttu-id="d3cc0-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d3cc0-119">OUTPUTS</span></span>

## <span data-ttu-id="d3cc0-120">Note</span><span class="sxs-lookup"><span data-stu-id="d3cc0-120">NOTES</span></span>

## <span data-ttu-id="d3cc0-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d3cc0-121">RELATED LINKS</span></span>

[<span data-ttu-id="d3cc0-122">Start-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="d3cc0-122">Start-AzureVNetGatewayDiagnostics</span></span>](./Start-AzureVNetGatewayDiagnostics.md)

[<span data-ttu-id="d3cc0-123">Stop-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="d3cc0-123">Stop-AzureVNetGatewayDiagnostics</span></span>](./Stop-AzureVNetGatewayDiagnostics.md)


