---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 706CBF65-C796-4525-BAEB-AAFAD44C0464
online version: ''
schema: 2.0.0
ms.openlocfilehash: d37c2ce3b32d23f7c5bb682d2116de84cc90f047
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029481"
---
# <span data-ttu-id="26a52-101">Stop-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="26a52-101">Stop-AzureVNetGatewayDiagnostics</span></span>

## <span data-ttu-id="26a52-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="26a52-102">SYNOPSIS</span></span>
<span data-ttu-id="26a52-103">Interrompe una sessione di diagnostica del gateway VPN in uso.</span><span class="sxs-lookup"><span data-stu-id="26a52-103">Stops a running VPN gateway diagnostics session.</span></span>

## <span data-ttu-id="26a52-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="26a52-104">SYNTAX</span></span>

```
Stop-AzureVNetGatewayDiagnostics -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="26a52-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26a52-105">DESCRIPTION</span></span>
<span data-ttu-id="26a52-106">Il cmdlet **Stop-AzureVNetGatewayDiagnostics** interrompe una sessione di diagnostica del gateway VPN (Virtual Private Network) in uso.</span><span class="sxs-lookup"><span data-stu-id="26a52-106">The **Stop-AzureVNetGatewayDiagnostics** cmdlet stops a running virtual private network (VPN) gateway diagnostics session.</span></span>
<span data-ttu-id="26a52-107">Questo comando Salva i risultati della sessione di diagnostica nell'account di archiviazione specificato dal cmdlet **Start-AzureVNetGatewayDiagnostics** .</span><span class="sxs-lookup"><span data-stu-id="26a52-107">This command saves the results of the diagnostics session to the storage account that the **Start-AzureVNetGatewayDiagnostics** cmdlet specifies.</span></span>

## <span data-ttu-id="26a52-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="26a52-108">EXAMPLES</span></span>

## <span data-ttu-id="26a52-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="26a52-109">PARAMETERS</span></span>

### <span data-ttu-id="26a52-110">-Profile</span><span class="sxs-lookup"><span data-stu-id="26a52-110">-Profile</span></span>
<span data-ttu-id="26a52-111">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26a52-111">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="26a52-112">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="26a52-112">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="26a52-113">-VNetName</span><span class="sxs-lookup"><span data-stu-id="26a52-113">-VNetName</span></span>
<span data-ttu-id="26a52-114">Specifica la rete virtuale che contiene un gateway di rete virtuale per cui questo cmdlet interrompe la diagnostica.</span><span class="sxs-lookup"><span data-stu-id="26a52-114">Specifies the virtual network that contains a virtual network gateway for which this cmdlet stops diagnostics.</span></span>

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

### <span data-ttu-id="26a52-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26a52-115">CommonParameters</span></span>
<span data-ttu-id="26a52-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26a52-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26a52-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26a52-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26a52-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="26a52-118">INPUTS</span></span>

## <span data-ttu-id="26a52-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="26a52-119">OUTPUTS</span></span>

## <span data-ttu-id="26a52-120">Note</span><span class="sxs-lookup"><span data-stu-id="26a52-120">NOTES</span></span>

## <span data-ttu-id="26a52-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="26a52-121">RELATED LINKS</span></span>

[<span data-ttu-id="26a52-122">Get-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="26a52-122">Get-AzureVNetGatewayDiagnostics</span></span>](./Get-AzureVNetGatewayDiagnostics.md)

[<span data-ttu-id="26a52-123">Start-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="26a52-123">Start-AzureVNetGatewayDiagnostics</span></span>](./Start-AzureVNetGatewayDiagnostics.md)


